---
title: Integración de gestión de gastos
description: Este tema proporciona información sobre la integración de informes de gastos en Project Operations utilizando doble escritura.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b41be519dbfa89668712bc28ccb1888cd08c38a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585813"
---
# <a name="expense-management-integration"></a>Integración de gestión de gastos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema proporciona información sobre la integración de informes de gastos en Project Operations [implementación de gasto completo](../expense/expense-overview.md) utilizando doble escritura.

## <a name="expense-categories"></a>Categorías de gasto

En una implementación de gastos completa, las categorías de gastos se crean y mantienen en las aplicaciones de finanzas y operaciones. Para crear una nueva categoría de gasto, siga estos pasos:

1. En Microsoft Dataverse, cree una categoría **Transacción**. La integración de doble escritura sincronizará esta categoría de transacción con las aplicaciones de Finanzas y operaciones. Para más información, vea [Configurar categorías de proyectos](/dynamics365/project-operations/project-accounting/configure-project-categories) y [Configuración de Project Operations e integración de datos de configuración](resource-dual-write-setup-integration.md). Como resultado de esta integración, el sistema crea cuatro registros de categorías compartidas en las aplicaciones de Finanzas y operaciones.
2. En Finance, vaya a **Administración de gastos** > **Configuración** > **Categorías compartidas** y seleccione una categoría compartida con una clase de transacción **Gasto**. Establezca el parámetro **Se puede utilizar en Gastos** como **True** y defina el tipo de gasto a utilizar.
3. Con este registro de categoría compartida, cree una nueva categoría de gastos yendo a **Administración de gastos** > **Configuración** > **Categorías de gasto** y seleccionando **Nuevo**. Cuando se guarda el registro, la doble escritura usa la asignación de tabla, **Entidad de exportación de categorías de gastos de proyecto de integración de Project Operations (msdyn\_expensecategories)** para sincronizar este registro con Dataverse.

  ![Integración de categorías de gastos.](./media/DW6ExpenseCategories.png)

Las categorías de gastos en las aplicaciones de Finanzas y operaciones son específicas de la empresa o entidad legal. Hay registros específicos de entidad legal correspondientes separados en Dataverse. Cuando un jefe de proyecto estima gastos, no puede seleccionar categorías de gastos que se crearon para un proyecto que es propiedad de una empresa diferente a la empresa propietaria del proyecto en el que está trabajando. 

## <a name="expense-reports"></a>Informes de gastos

Los informes de gastos se crean y aprueban en las aplicaciones de Finanzas y operaciones. Para más información, vea [Crear y procesar informes de gastos en Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Una vez que el jefe de proyecto aprueba el informe de gastos, se registra en contabilidad general. En Project Operations, las líneas de informes de gastos relacionadas con el proyecto se registran mediante reglas de contabilización especiales:

  - El coste relacionado con el proyecto (incluido el impuesto no recuperable) no se registra inmediatamente en la cuenta de coste del proyecto en contabilidad general, sino que se registra en la cuenta de integración de gastos. Esta cuenta se configura en **Administración y contabilidad de proyectos** > **Configuración** > **Parámetros de administración y contabilidad de proyectos**, pestaña **Project Operations en Dynamics 365 Customer engagement**.
  - La doble escritura se sincroniza con Dataverse utilizando la asignación de tabla **Entidad de exportación de gastos de proyecto de integración de Project Operations (msdyn\_expenses)** mapa de la mesa.
  - La subcontabilidad de impuestos, la subcontabilidad de proveedores y otras contabilizaciones financieras se registran según corresponda en el momento de registrar el informe de gastos.

  ![Integración de informes de gastos.](./media/DW6ExpenseReports.png)

Cuando se escribe un registro en la entidad **Gastos** en Dataverse, el sistema desencadena el proceso de aprobación automatizado del registro. Si es necesario, el estado del proceso de aprobación automatizado se puede revisar en Dataverse yendo a **Configuración avanzada** > **Sistema** > **Trabajos del sistema**. Una vez completada la aprobación, se crean registros de clases de transacciones de gastos en la entidad **Datos reales**.

Los datos reales relacionados con gastos se procesan utilizando la asignación de tabla de doble escritura, **Datos reales de integración de Project Operations (msdyn\_actuals)**. Para obtener más información, consulte [Estimaciones y datos reales del proyecto](resource-dual-write-estimates-actuals.md).

El proceso periódico **Importar desde tabla de almacenamiento provisional** crea líneas del diario relacionadas con informes de gastos el diario de integración de Project Operations. La cuenta de contrapartida tiene como valor predeterminado la cuenta de integración de gastos. El diario de integración de registros borra el saldo de la cuenta para la transacción de gastos y mueve el importe de gastos a la cuenta de coste del proyecto. El sistema también crea transacciones de subcontabilidad del proyecto para fines de facturación descendente y reconocimiento de ingresos.
