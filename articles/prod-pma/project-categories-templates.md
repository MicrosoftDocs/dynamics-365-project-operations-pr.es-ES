---
title: Sincronizar las categorías de gastos del proyecto entre Finance and Operations y Project Service Automation
description: Este tema describe las plantillas y las tareas subyacentes que se utilizan para sincronizar las categorías de gastos del proyecto entre Microsoft Dynamics 365 Finance y Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999872"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sincronizar las categorías de gastos del proyecto entre Finance and Operations y Project Service Automation

[!include[banner](../includes/banner.md)]

Este tema describe las plantillas y las tareas subyacentes que se utilizan para sincronizar las categorías de gastos del proyecto entre Dynamics 365 Finance y Dynamics 365 Project Service Automation.

> [!NOTE]
> - La integración de tareas del proyecto, las categorías de transacciones de gastos, las estimaciones de horas, las estimaciones de gastos y el bloqueo de funciones están disponibles en la versión 8.0.
> - Las integraciones de datos reales están disponibles a partir de la versión 8.0.1.
> - Si utiliza la Enterprise Edition7.3.0, después de instalar KB 4132657 y KB 4132660, podrá usar las plantillas para integrar tareas del proyecto, categorías de transacciones de gastos, estimaciones de horas, estimaciones de gastos y datos reales, y para configurar el bloqueo de funcionalidades. Si debe restablecer las distribuciones contables, le recomendamos que también instale KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Flujo de datos para Project Service Automation y Finance

La solución de integración de Project Service Automation y Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Project Service Automation y Finance. Las plantillas de integración que están disponibles con la función de integración de datos permiten el flujo de datos sobre las categorías de transacciones de gastos entre Finance y Project Service Automation.

Si las categorías de gastos del proyecto se gestionan en Finance, el flujo de integración primero va desde Finance hasta Project Service Automation. Los identificadores de integración de las categorías de gastos del proyecto se actualizan a través de la sincronización de Project Service Automation a Finance.

Si las categorías de gastos del proyecto se gestionan en Project Service Automation, el flujo de integración primero va desde Project Service Automation hasta Finance. Las categorías de proyectos ya deben estar configuradas en Finance antes de la sincronización desde Project Service Automation. Luego, sincronice de Finance a Project Service Automation, y luego de Project Service Automation a Finance nuevamente. De esta manera, ayuda a garantizar que las categorías estén vinculadas y que no se creen duplicados.

> [!NOTE]
> Normalmente, las categorías de gastos del proyecto se gestionan en Finance. Sin embargo, si no es así, o si las categorías de gastos ya se han creado en Project Service Automation, primero debe sincronizar mediante la plantilla de categorías de transacciones de gastos del proyecto (PSA a Fin and Ops). Luego, sincronice utilizando la plantilla de categorías de transacciones de gastos del proyecto (Fin and Ops a PSA). Luego, debe ejecutar la sincronización de Project Service Automation a Finance una vez más.
>
> Si sincroniza primero desde Project Service Automation, se deben cumplir los siguientes requisitos en Finance antes de que se ejecute la sincronización:
>
> - La categoría compartida que coincide con la categoría de proyecto que se configura en Project Service Automation debe existir y debe estar habilitada para ambos **Proyecto** y **Gastos**.
> - Para cada entidad jurídica de Finance con la que se debe integrar, deben existir las siguientes categorías de proyectos:
>
>     - Existe **Categoría de proyecto**. 
>     - **Uso en gastos** está habilitada.
>     - **Activo en diario** está habilitada.
>     - **Tipo de transacción** está establecida en **Gastos**.

La siguiente ilustración muestra cómo se sincronizan los datos entre Project Service Automation y Finance.

[![Flujo de datos para la integración de Project Service Automation con Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sincronización de las categorías de gastos del proyecto desde Finance a Project Service Automation

### <a name="template-and-task"></a>Plantilla y tarea

Para tener acceso a la plantilla, en el centro de administración de Microsoft Power Apps, seleccione **Proyectos** y luego, en la esquina superior derecha, seleccione **Nuevo proyecto** para seleccionar plantillas públicas.

La siguiente plantilla y la tarea subyacentes se utilizan para sincronizar las categorías de gastos del proyecto de Finance a Project Service Automation:

- **Nombre de la plantilla en Integración de datos**: categorías de transacción de gatos del proyecto (Fin and Ops a PSA).
- **Nombre de la tarea en el proyecto**: sincronizar categorías a PSA.

### <a name="entity-set"></a>Conjunto de entidades

| Finanzas                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entidad de integración para categorías | Categorías de transacciones     |

### <a name="entity-flow"></a>Flujo de entidades

Las categorías de gastos del proyecto se administran en Finance y se sincronizan con Project Service Automation como categorías de transacciones.

### <a name="power-query"></a>Power Query

Cuando sincroniza con Project Service Automation, debe usar Microsoft Power Query para Excel para establecer el tipo de facturación en la categoría de transacción. La plantilla de categorías de transacciones de gastos del proyecto (Fin and Ops a PSA) proporciona una columna y una asignación predeterminadas. Si crea su propia plantilla, debe agregar una columna condicional en Power Query. Siga estos pasos.

1. Haga clic en la flecha para abrir la asignación de la tarea de categorías de gastos del proyecto en la plantilla de categorías de transacciones de gastos del proyecto (Fin and Ops a PSA).
2. Haga clic en el vínculo **Consulta y filtrado avanzados** para abrir Power Query.
2. Seleccione **Agregar columna condicional**.
3. Especifique un nombre para la nueva columna, como **BillingType**.
4. Especifique la siguiente condición: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Haga clic en **Aceptar** en la columna.
6. Asegúrese de asignar esta nueva columna en la página de asignaciones.

La siguiente ilustración muestra un ejemplo de la asignación de tareas de plantilla en Integración de datos. La asignación muestra la información del campo que se sincronizará de Finance a Project Service Automation.

[![Sincronización de las categorías de gastos a la asignación de plantilla de Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sincronización de las categorías de gastos del proyecto desde Project Service Automation a Finance

### <a name="template-and-task"></a>Plantilla y tarea

La siguiente plantilla y la tarea subyacentes se utilizan para sincronizar las categorías de gastos del proyecto de Project Service Automation a Finance:

- **Nombre de la plantilla en Integración de datos**: categorías de transacción de gatos del proyecto (PSA A Fin and Ops).
- **Nombre de la tarea en el proyecto**: sincronizar categorías a Fin and Ops.

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanzas                           |
|----------------------------|-----------------------------------|
| Categorías de transacciones     | Entidad de integración para categorías |

### <a name="entity-flow"></a>Flujo de entidades

Las categorías de gastos del proyecto se administran en Finance y se sincronizan con Project Service Automation como categorías de transacciones. La sincronización de nuevo a Finance actualiza la categoría del proyecto en Finance con el identificador de integración desde Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Asignación de plantillas en la integración de datos

La siguiente ilustración muestra un ejemplo de la asignación de tareas de plantilla en Integración de datos.

> [!NOTE]
> La asignación muestra la información del campo que se sincronizará de Project Service Automation a Finance.

[![Project Service Automation a asignación de plantilla de Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]