---
title: Diario de integración en Project Operations
description: Este artículo proporciona información sobre el trabajo con el diario de integración de Project Operations.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106296"
---
# <a name="integration-journal-in-project-operations"></a>Diario de integración en Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las entradas de tiempo, gastos, precios y material crean transacciones **reales** que representan la vista operativa del trabajo completado en un proyecto. Dynamics 365 Project Operations proporciona a los contables una herramienta para revisar transacciones y ajustar los atributos contables según sea necesario. Una vez que se completan la revisión y los ajustes, las transacciones se registran en la contabilidad general y la subcontabilidad del proyecto. Un contable puede realizar estas actividades utilizando el diario **Integración de Project Operations** (diario **Dynamics 365 Finance** > **Gestión de proyectos y contabilidad** > **Diarios** > **Diario de integración de Project Operations**).

![Flujo del diario de integración.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Crear registros en el diario Integración en Project Operations

Los registros en el diario de integración de Project Operations se crean mediante un proceso periódico, **Importar desde la tabla de preparación**. Puede ejecutar este proceso yendo a **Dynamics 365 Finance** > **Gestión de proyectos y contabilidad** > **Periódico** > **Integración de Project Operations** > **Importar desde tabla de almacenamiento provisional**. Puede ejecutar el proceso de forma interactiva o configurar el proceso para que se ejecute en segundo plano según sea necesario.

Cuando se ejecuta el proceso periódico, se encuentran los datos reales que aún no se han agregado al diario de integración de Project Operations. Se crea una línea de diario por cada transacción real.
El sistema agrupa las líneas del diario en diarios independientes en función del valor seleccionado en el campo **Unidad de período en el diario Integración de Project Operations** (**Finanzas** > **Gestión de proyectos y contabilidad** > **Configuración** > **Parámetros de gestión de proyectos y contabilidad**, en la pestaña **Project Operations on Dynamics 365 Customer Engagement**). A continuación, indicamos los posibles valores de este campo:

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
    - Si la **Categoría de transacción** no está establecida en el dato real del proyecto, el sistema utiliza el valor del campo **Valores predeterminados de categoría de proyecto**, en la pestaña **Project Operations en Dynamics 365 Customer Engagement** de la página **Administración de proyectos y parámetros contables**.
  - El campo **Recurso** representa el recurso del proyecto relacionado con esta transacción. El recurso se utiliza como referencia en las propuestas de facturas de proyectos a los clientes.
  - El campo **Tipo de cambio** toma valores predeterminados de la **Tasa de cambio de moneda** establecida en Dynamics 365 Finance. Si falta la configuración del tipo de cambio, el proceso periódico **Importar desde la puesta en escena** no agregará el registro a un diario y se agregará un mensaje de error al registro de ejecución del trabajo.
  - El campo **Propiedad de línea** representa el tipo de facturación en los datos reales del proyecto. La propiedad de línea y la asignación de tipo de facturación se definen en la pestaña **Project Operations en Dynamics 365 Customer Engagement**, en la página **Parámetros contables y de gestión de proyectos**.

Solo los siguientes atributos contables se pueden actualizar en las líneas del diario de integración de Project Operations:

- **Grupo de impuestos de ventas de facturación** y **Grupo de impuestos de ventas de artículos de facturación**.
- **Dimensiones financieras** (utilizando la acción **Distribuir cantidades**)

Las líneas de diario de integración se pueden eliminar. Sin embargo, las líneas no registradas se volverán a insertar en el diario después de volver a ejecutar el proceso periódico **Importar desde la puesta en escena**.

### <a name="post-the-project-operations-integration-journal"></a>Registrar el diario de integración de Project Operations

Cuando contabiliza el diario de integración, se crean un libro auxiliar del proyecto y las transacciones del libro mayor. Estos se utilizan en la facturación de clientes posteriores, el reconocimiento de ingresos y los informes financieros.

El diario de integración de Project Operations seleccionado se puede registrar mediante **Registrar** en la página del diario de integración de Project Operations. Todos los diarios se pueden registrar automáticamente ejecutando un proceso en **Periódicos** > **Integración de Project Operations** > **Registrar diario de integración de Project Operations**.

El registro se puede realizar de forma interactiva o en un lote. Tenga en cuenta que todos los diarios que tengan más de 100 líneas se registrarán automáticamente en un lote. Para un mejor rendimiento cuando los diarios que tienen muchas líneas se registran en un lote, habilite la característica **Registrar diario de integración de Project Operations utilizando varias tareas por lotes** en el espacio de trabajo **Administración de características**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Transferir todas las líneas que tienen errores de registro a un nuevo diario

> [!NOTE]
> Para usar esta capacidad, habilite la característica **Transferir todas las líneas con errores de registro a un nuevo diario de integración de Project Operations** en el espacio de trabajo **Administración de características**.

Durante el diario en el diario de integración de Project Operations, el sistema valida cada línea del diario. El sistema registra todas las líneas que no tienen errores y crea un nuevo diario para todas las líneas que tienen errores de registro. Para revisar los diarios que tienen líneas de error de registro, vaya a **Gestión de proyectos y contabilidad** > **Diarios** > **Diario de integración de Project Operations** y filtre los diarios mediante el campo **Diario original**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
