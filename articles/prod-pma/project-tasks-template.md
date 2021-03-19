---
title: Sincronizar las tareas del proyecto y los proyectos directamente desde Project Service Automation a Finance and Operations
description: Este tema describe la plantilla y la tarea subyacentes que se utilizan para sincronizar las tareas del proyecto directamente desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288940"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f0656-103">Sincronizar las tareas del proyecto y los proyectos directamente desde Project Service Automation a Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0656-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f0656-104">Este tema describe la plantilla y la tarea subyacentes que se utilizan para sincronizar las tareas del proyecto directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f0656-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="f0656-105">La integración de tareas del proyecto, las categorías de transacciones de gastos, las estimaciones de horas, las estimaciones de gastos y el bloqueo de funciones están disponibles en la versión 8.0.</span><span class="sxs-lookup"><span data-stu-id="f0656-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="f0656-106">Si utiliza la Enterprise Edition7.3.0, después de instalar KB 4132657 y KB 4132660, podrá usar las plantillas para integrar tareas del proyecto, categorías de transacciones de gastos, estimaciones de horas, estimaciones de gastos y datos reales, y para configurar el bloqueo de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="f0656-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="f0656-107">Si debe restablecer las distribuciones contables, le recomendamos que también instale KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="f0656-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="f0656-108">Las integraciones de datos reales están disponibles a partir de la versión 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="f0656-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="f0656-109">Flujo de datos para Project Service Automation con Finance</span><span class="sxs-lookup"><span data-stu-id="f0656-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="f0656-110">La solución de integración de Project Service Automation con Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Project Service Automation y Finance.</span><span class="sxs-lookup"><span data-stu-id="f0656-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="f0656-111">La plantilla de integración que está disponibles con la función de integración de datos permite el flujo de datos sobre las tareas del proyecto desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="f0656-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f0656-112">La siguiente ilustración muestra cómo se sincronizan los datos entre Project Service Automation y Finance.</span><span class="sxs-lookup"><span data-stu-id="f0656-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="f0656-113">[![Flujo de datos para la integración de Project Service Automation con Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f0656-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="f0656-114">Plantilla y tarea</span><span class="sxs-lookup"><span data-stu-id="f0656-114">Template and task</span></span>

<span data-ttu-id="f0656-115">Para tener acceso a la plantilla, en el centro de administración de Microsoft Power Apps, seleccione **Proyectos** y luego, en la esquina superior derecha, seleccione **Nuevo proyecto** para seleccionar plantillas públicas.</span><span class="sxs-lookup"><span data-stu-id="f0656-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f0656-116">La siguiente plantilla y la tarea subyacentes se utilizan para sincronizar las tareas del proyecto de Project Service Automation a Finance:</span><span class="sxs-lookup"><span data-stu-id="f0656-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="f0656-117">**Nombre de la plantilla en Integración de datos**: tareas del proyecto (PSA a Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f0656-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f0656-118">**Nombre de la tarea en el proyecto**: tareas del proyecto</span><span class="sxs-lookup"><span data-stu-id="f0656-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="f0656-119">Antes de poder realizar la sincronización de tareas, debe sincronizar los contratos de proyecto y los proyectos.</span><span class="sxs-lookup"><span data-stu-id="f0656-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="f0656-120">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="f0656-120">Entity set</span></span>

| <span data-ttu-id="f0656-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f0656-121">Project Service Automation</span></span> | <span data-ttu-id="f0656-122">Finanzas</span><span class="sxs-lookup"><span data-stu-id="f0656-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="f0656-123">Tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="f0656-123">Project Tasks</span></span>              | <span data-ttu-id="f0656-124">Entidad de integración para la tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="f0656-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="f0656-125">Flujo de entidades</span><span class="sxs-lookup"><span data-stu-id="f0656-125">Entity flow</span></span>

<span data-ttu-id="f0656-126">Las tareas proyecto se administran en Project Service Automation y se sincronizan con Finance como actividades de proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0656-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f0656-127">Requisitos previos y configuración de las asignaciones</span><span class="sxs-lookup"><span data-stu-id="f0656-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="f0656-128">Antes de poder realizar la sincronización de tareas, debe sincronizar los contratos de proyecto y los proyectos.</span><span class="sxs-lookup"><span data-stu-id="f0656-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="f0656-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="f0656-129">Power Query</span></span>

<span data-ttu-id="f0656-130">Debe usar Microsoft Power Query para Excel para filtrar datos si se cumple esta condición:</span><span class="sxs-lookup"><span data-stu-id="f0656-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="f0656-131">Tiene registros específicos de recursos en una tarea de proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0656-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="f0656-132">Si debe usar Power Query, siga estas pautas:</span><span class="sxs-lookup"><span data-stu-id="f0656-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="f0656-133">La plantilla de tareas de proyecto (PSA a Fin and Ops) tiene un filtro predeterminado que excluye registros específicos de recursos de una tarea de proyecto estableciendo el filtro en **IsLineTask** a **Falso**.</span><span class="sxs-lookup"><span data-stu-id="f0656-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="f0656-134">Si crea su propia plantilla, debe agregar este filtro.</span><span class="sxs-lookup"><span data-stu-id="f0656-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f0656-135">Asignación de plantillas en la integración de datos</span><span class="sxs-lookup"><span data-stu-id="f0656-135">Template mapping in Data integration</span></span>

<span data-ttu-id="f0656-136">La siguiente ilustración muestra un ejemplo de las asignaciones de tareas de plantilla en Integración de datos.</span><span class="sxs-lookup"><span data-stu-id="f0656-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="f0656-137">La asignación muestra la información del campo que se sincronizará de Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="f0656-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f0656-138">[![Asignación de plantillas](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="f0656-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]