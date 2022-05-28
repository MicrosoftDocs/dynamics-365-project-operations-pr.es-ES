---
title: Sincronizar las tareas de proyectos directamente desde Project Service Automation a Finanzas y operaciones
description: En este tema se describen la plantilla y la tarea subyacente que se usan para sincronizar tareas de proyectos directamente desde Microsoft Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 666e0d757969b32f16e08128d9f78a2ffe1e8357
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683331"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizar las tareas de proyectos directamente desde Project Service Automation a Finanzas y operaciones

[!include[banner](../includes/banner.md)]

En este tema se describen la plantilla y la tarea subyacente que se usan para sincronizar tareas de proyectos directamente desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE]
> - La integración de tareas del proyecto, las categorías de transacciones de gastos, las estimaciones de horas, las estimaciones de gastos y el bloqueo de funciones están disponibles en la versión 8.0.
> - Si utiliza la Enterprise Edition7.3.0, después de instalar KB 4132657 y KB 4132660, podrá usar las plantillas para integrar tareas del proyecto, categorías de transacciones de gastos, estimaciones de horas, estimaciones de gastos y datos reales, y para configurar el bloqueo de funcionalidades. Si debe restablecer las distribuciones contables, le recomendamos que también instale KB 4131710.
> - Las integraciones de datos reales están disponibles a partir de la versión 8.0.1.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flujo de datos para Project Service Automation con Finance

La solución de integración de Project Service Automation con Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Project Service Automation y Finance. La plantilla de integración que está disponibles con la función de integración de datos permite el flujo de datos sobre las tareas del proyecto desde Project Service Automation a Finance.

La siguiente ilustración muestra cómo se sincronizan los datos entre Project Service Automation y Finance.

[![Flujo de datos para la integración de Project Service Automation con Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Plantilla y tarea

Para tener acceso a la plantilla, en el centro de administración de Microsoft Power Apps, seleccione **Proyectos** y luego, en la esquina superior derecha, seleccione **Nuevo proyecto** para seleccionar plantillas públicas.

La siguiente plantilla y la tarea subyacentes se utilizan para sincronizar las tareas del proyecto de Project Service Automation a Finance:

- **Nombre de la plantilla en Integración de datos**: tareas del proyecto (PSA a Fin and Ops)
- **Nombre de la tarea en el proyecto**: tareas del proyecto

Antes de poder realizar la sincronización de tareas, debe sincronizar los contratos de proyecto y los proyectos.

## <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanzas                             |
|----------------------------|-------------------------------------|
| Tareas de proyecto              | Entidad de integración para la tarea de proyecto |

## <a name="entity-flow"></a>Flujo de entidades

Las tareas proyecto se administran en Project Service Automation y se sincronizan con Finance como actividades de proyecto.

## <a name="prerequisites-and-mapping-setup"></a>Requisitos previos y configuración de las asignaciones

Antes de poder realizar la sincronización de tareas, debe sincronizar los contratos de proyecto y los proyectos.

## <a name="power-query"></a>Power Query

Debe usar Microsoft Power Query para Excel para filtrar los datos si se cumple esta condición:

- Tiene registros específicos de recursos en una tarea de proyecto.

Si debe usar Power Query, siga estas directrices:

- La plantilla de tareas de proyecto (PSA a Fin and Ops) tiene un filtro predeterminado que excluye registros específicos de recursos de una tarea de proyecto estableciendo el filtro en **IsLineTask** a **Falso**. Si crea su propia plantilla, debe agregar este filtro.

## <a name="template-mapping-in-data-integration"></a>Asignación de plantillas en la integración de datos

La siguiente ilustración muestra un ejemplo de las asignaciones de tareas de plantilla en Integración de datos. La asignación muestra la información del campo que se sincronizará de Project Service Automation a Finance.

[![Asignación de plantillas.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]