---
title: Diario de integración en Project Operations
description: Este tema proporciona información sobre cómo trabajar con el diario de integración en Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ebdb543560027d223715d0e5c70c864b706cb2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007162"
---
# <a name="integration-journal-in-project-operations"></a>Diario de integración en Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las entradas de tiempo y gastos crean transacciones **reales** que representan la vista operativa del trabajo completado en un proyecto. Dynamics 365 Project Operations proporciona a los contables una herramienta para revisar transacciones y ajustar los atributos contables según sea necesario. Una vez que se completan la revisión y los ajustes, las transacciones se registran en la contabilidad general y la subcontabilidad del proyecto. Un contador puede realizar estas actividades utilizando el diario **Integración de Project Operations** (**Dynamics 365 Finance** > **Gestión de proyectos y contabilidad** > **Diarios** > diario **Integración de Project Operations**.

![Flujo del diario de integración](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Crear registros en el diario Integración en Project Operations

Los registros en el diario de integración de Project Operations se crean mediante un proceso periódico, **Importar desde la tabla de preparación**. Puede ejecutar este proceso yendo a **Dynamics 365 Finance** > **Gestión de proyectos y contabilidad** > **Periódico** > **Integración de Project Operations** > **Importar desde la tabla de preparación**. Puede ejecutar el proceso de forma interactiva o configurar el proceso para que se ejecute en segundo plano según sea necesario.

Cuando se ejecuta el proceso periódico, se encuentran los datos reales que aún no se han agregado al diario de integración de Project Operations. Se crea una línea de diario por cada transacción real.
El sistema agrupa las líneas del diario en diarios separados según el valor seleccionado en el campo **Unidad de período en el diario de integración de Project Operations** (**Finanzas** > **Gestión de proyectos y contabilidad** > **Preparar** > **Parámetros contables y de gestión de proyectos**, pestaña **Project Operations en Dynamics 365 Customer Engagement**). Los posibles valores para este campo incluyen:

  - **Días**: los datos reales se agrupan por fecha de transacción. Se crea un diario independiente para cada día.
  - **Meses**: los datos reales se agrupan por mes calendario. Se crea un diario independiente para cada mes.
  - **Años**: los datos reales se agrupan por año de calendario. Se crea un diario independiente para cada año.
  - **Todas**: todas las transacciones reales se incluyen en el mismo diario de integración. Si el diario no está disponible cuando se ejecuta el proceso periódico, por ejemplo, si el diario está en proceso de contabilizar transacciones, se crea un nuevo diario.

Las líneas de diario se crean según los datos reales del proyecto. La siguiente lista incluye algunas de las reglas predeterminadas y de transformación más notables:

  - Cada transacción real del proyecto tiene una línea en el diario de integración de Project Operations. Las transacciones de ventas de costo y no facturadas por tipo de facturación de tiempo y material se muestran en líneas separadas.
  - El campo **Fecha** representa la fecha de la transacción. El campo **Fecha de contabilidad** representa la fecha en que la transacción se registra en el libro mayor. Si la fecha contable está en un [período financiero cerrado](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) y el parámetro **Establecer automáticamente la fecha de contabilidad para abrir el período del libro mayor** se establece en la pestaña **Financiero** de la página **Parámetros contables y de gestión de proyectos**, el sistema ajustará la fecha contable de la transacción a la primera fecha en el próximo período del libro mayor abierto.
  - El campo **Vale** muestra el número de comprobante de cada transacción real. La secuencia del número de cupón se define en la pestaña **Secuencias numéricas**, en la página **Parámetros contables y de gestión de proyectos**. A cada línea se le asigna un número nuevo. Después de contabilizar el comprobante, puede ver cómo se relacionan el costo y la transacción de ventas no facturadas seleccionando **Vales relacionados** en la página **Transacción de cupón**.
  - El campo **Categoría** representa una transacción de proyecto y valores predeterminados basados en la categoría de transacción para el proyecto relacionado real.
    - Si **Categoría de transacción** se establece en el proyecto real y existe una **Categoría de proyecto** relacionada en una entidad jurídica determinada, la categoría predeterminada es esta categoría de proyecto.
    - Si la **Categoría de transacción** no está configurada en el Proyecto real, el sistema usa el valor en el campo **Valores predeterminados de categoría de proyecto** en la pestaña **Project Operations en Dynamics 365 Customer Engagement** en la página **Parámetros contables y de gestión de proyectos**.
  - El campo **Recurso** representa el recurso del proyecto relacionado con esta transacción. El recurso se utiliza como referencia en las propuestas de facturas de proyectos a los clientes.
  - El campo **Tipo de cambio** usa de manera predeterminada el valor de **Tasa de cambio de moneda** establecido en Dynamics 365 Finance. Si falta la configuración del tipo de cambio, el proceso periódico **Importar desde la puesta en escena** no agregará el registro a un diario y se agregará un mensaje de error al registro de ejecución del trabajo.
  - El campo **Propiedad de línea** representa el tipo de facturación en los datos reales del proyecto. La propiedad de línea y la asignación del tipo de facturación se definen en la pestaña **Project Operations en Dynamics 365 Customer Engagement** en la página **Parámetros contables y de gestión de proyectos**.

Solo los siguientes atributos contables se pueden actualizar en las líneas del diario de integración de Project Operations:

- **Grupo de impuestos de ventas de facturación** y **Grupo de impuestos de ventas de artículos de facturación**.
- **Dimensiones financieras** (utilizando la acción **Distribuir cantidades**)

Las líneas del diario de integración se pueden eliminar; sin embargo, las líneas no publicadas se volverán a insertar en el diario después de volver a ejecutar el proceso periódico **Importar desde la puesta en escena**.

Cuando contabiliza el diario de integración, se crean un libro auxiliar del proyecto y las transacciones del libro mayor. Estos se utilizan en la facturación de clientes posteriores, el reconocimiento de ingresos y los informes financieros.


[!INCLUDE[footer-include](../includes/footer-banner.md)]