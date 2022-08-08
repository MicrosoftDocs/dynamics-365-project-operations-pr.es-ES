---
title: Integración de estimaciones y datos reales de proyectos
description: Este artículo proporciona información sobre la integración de escritura dual de Project Operations para estimaciones y dataos reales de proyectos.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029101"
---
# <a name="project-estimates-and-actuals-integration"></a>Integración de estimaciones y datos reales de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo proporciona información sobre la integración de escritura dual de Project Operations para estimaciones y dataos reales de proyectos.

## <a name="project-estimates"></a>Estimaciones de proyecto

Las estimaciones de mano de obra, gastos y materiales del proyecto se crean y mantienen en Microsoft Dataverse y se sincronizan con las aplicaciones de finanzas y operaciones para fines contables. Las operaciones de creación, actualización y eliminación no se admiten a través de las aplicaciones de finanzas y operaciones.

La creación de estimaciones requiere una configuración de contabilidad válida para el proyecto. Los proyectos que están asociados con líneas de contrato deben tener un perfil de ingresos y costos de proyecto válido definido en las reglas de perfil de costos e ingresos del proyecto. Para más información, vea [Configurar contabilidad para proyectos facturables](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimaciones de mano de obra

Las estimaciones de mano de obra son creadas por el Jefe de proyecto o el Administrador de recursos, quien también asigna un recurso genérico o con nombre a la tarea del proyecto. Los registros de asignación de recursos se pueden revisar en la pestaña **Asignaciones de recursos** de la página **Detalles del proyecto** en Dataverse. Los registros de asignación de recursos en Dataverse crean registros de previsión de horas en aplicaciones de finanzas y operaciones usando **Entidad de integración de Project Operations para estimaciones de horas (msdyn\_resourceassignments)**.

   ![Integración de estimaciones de mano de obra.](./Media/DW4LaborEstimates.png)

La doble escritura sincroniza registros de asignación de recursos con la tabla de preparación (**ProjCDSEstimateHoursImport**) y luego utiliza la lógica de negocios para crear y actualizar registros de previsión de horas (**ProjForecastEmpl**).

El contable del proyecto revisa los registros de horas previstas creados en las aplicaciones de finanzas y operaciones yendo a **Gestión de proyectos y contabilidad** > **Todos los proyectos** > **Plan** > **Previsiones de horas**.

## <a name="expense-estimates"></a>Estimaciones de gastos

Las estimaciones de gastos son creadas por el administrador del proyecto en la pestaña **Estimaciones de gastos** de la página **Detalles del proyecto** en Dataverse. Los registros de estimaciones de gastos se almacenan en la entidad **Línea de estimación** en Dataverse. Estos registros de estimación tienen clase de transacción, **Gastos** y se sincronizan con los registros de previsión de gastos en las aplicaciones de finanzas y operaciones mediante **Entidad de integración de Project Operations para estimaciones de gastos (msdyn\_estimatelines)**.

   ![Integración de estimaciones de gastos.](./Media/DW4ExpenseEstimates.png)

La doble escritura sincroniza registros de estimación de gastos con la tabla de preparación, **ProjCDSEstimateExpenseImport)**, y luego utiliza la lógica de negocios para crear y actualizar registros de previsión de gastos (**ProjForecastCost**). Las líneas de estimación almacenan los registros de estimación de ventas y estimación de costos por separado. La lógica empresarial de las aplicaciones de finanzas y operaciones rellena un solo registro de previsión de gastos utilizando este detalle en la tabla de almacenamiento provisional.

El contable del proyecto puede revisar los registros de gastos previstos creados en las aplicaciones de finanzas y operaciones yendo a **Gestión de proyectos y contabilidad** > **Todos los proyectos** > **Plan** > **Previsiones de gastos**.

## <a name="material-estimates"></a>Estimaciones de materiales

Las estimaciones de materiales son creadas por el administrador del proyecto en la pestaña **Estimaciones de materiales** de la página **Detalles del proyecto** en Dataverse. Los registros de estimaciones de materiales se almacenan en la entidad **Línea de estimación** en Dataverse. Estos registros de estimación tienen clase de transacción, **Material** y se sincronizan con los registros de previsión de artículos en las aplicaciones de finanzas y operaciones mediante **Tabla de integración de proyectos para estimaciones de materiales (msdyn\_estimatelines)**.

   ![Integración de estimaciones de materiales.](./Media/DW4MaterialEstimates.png)

La doble escritura sincroniza registros de estimación de materiales con la tabla de preparación, **ProjForecastSalesImpor**, y luego utiliza la lógica de negocios para crear y actualizar registros de previsión de artículos (**ForecastSales**). Las líneas de estimación almacenan los registros de estimación de ventas y estimación de costos por separado. La lógica empresarial de las aplicaciones de finanzas y operaciones rellena un solo registro de previsión de artículos utilizando este detalle en la tabla de almacenamiento provisional.

El contable del proyecto puede revisar los registros de artículos previstos creados en las aplicaciones de finanzas y operaciones yendo a **Gestión de proyectos y contabilidad** > **Todos los proyectos** > **Plan** > **Previsiones de artículos**.

## <a name="project-actuals"></a>Datos reales del proyecto

Los datos reales del proyecto se crean en Dataverse, según el tiempo, los gastos, el material y la actividad de facturación. Todos los atributos operativos de estas transacciones, incluida la cantidad, el precio de coste, el precio de venta y el proyecto, se capturan en esta entidad Dataverse. Para obtener más información, consulte [Datos reales](../actuals/actuals-overview.md). Los registros reales se sincronizan con las aplicaciones de finanzas y operaciones mediante el mapa de tablas de doble escritura **Datos reales de integración de operaciones de Project Operations (msdyn\_actuals)** para la contabilidad posterior.

   ![Integración de datos reales.](./Media/DW4Actuals.png)

La asignación de tabla **Datos reales de integración de Project Operations** sincroniza todos los registros de la entidad **Datos reales** en Dataverse, con el atributo **Omitir sincronización (solo para uso interno)** establecido como **False**. Este valor de atributo se establece en Dataverse automáticamente cuando se crea el registro. Ejemplos en los que este atributo se establece como **True** son:

  - Datos reales de costes del proyecto para transacciones de empresas vinculadas. Para obtener más información, consulte [Crear transacciones de empresas vinculadas](../project-accounting/create-intercompany-transactions.md). Estos registros se omiten porque el sistema vuelve a crear el coste real del proyecto en las aplicaciones de finanzas y operaciones cuando se registra la factura del proveedor de empresas vinculadas.
  - Se crean registros negativos de ventas no facturadas cuando se confirma la factura proforma. Estos registros se omiten porque el libro auxiliar del proyecto en las aplicaciones de finanzas y operaciones no revierte el registro de ventas no facturadas en la facturación, sino que cambia el estado a totalmente facturado.

La asignación de tabla de doble escritura sincroniza los registros de datos reales con la tabla de preparación, **ProjCDSActualsImport**. Estos registros son procesados por el proceso periódico **Importar desde la tabla de preparación** al crear líneas de diario de integración de Project Operations y líneas de propuesta de factura de proyecto. Para más información, vea [Diario de integración en Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse también captura los vínculos entre las transacciones reales del proyecto en la entidad **Conexión de transacciones**. Para más información, vea [Vincular datos reales con registros originales](../actuals/linkingactuals.md). Los enlaces entre las transacciones reales también se sincronizan con las aplicaciones de finanzas y operaciones mediante el mapa de tablas de doble escritura **Entidad de integración para relaciones de transacciones de proyectos (msdyn\_transactionconnections)**. Estos registros son utilizados por el proceso periódico **Importar desde la tabla de preparación** al crear líneas de diario de integración de Project Operations y líneas de propuesta de factura de proyecto.

El registro de un diario de integración de Project Operations y una propuesta de factura de proyecto desencadena una actualización en los registros respectivos en la tabla de preparación, **ProjCDSActualsImport**. El sistema captura y registra los siguientes atributos contables para transacciones reales:

- Importe de divisa de contabilidad
- Tipo de cambio
- Número de asiento
- Importe del impuesto sobre las ventas

La asignación de tabla **Datos reales de integración de Project Operations** actualiza los respectivos registros de datos reales en Dataverse con esta información.
