---
title: Cambios en la administración de recursos (Project Service Automation 3.x)
description: En este tema se proporciona información sobre los cambios en el área de administración de recursos.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085339"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="75b58-103">Cambios en la administración de recursos (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="75b58-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="75b58-104">Las secciones de este tema proporcionan información sobre los cambios que se han realizado en el área de administración de recursos de la versión 3.x de Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="75b58-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="75b58-105">Estimaciones de proyecto</span><span class="sxs-lookup"><span data-stu-id="75b58-105">Project estimates</span></span>

<span data-ttu-id="75b58-106">En lugar de basarse en la entidad **msdyn\_projecttask** ( **Tarea de proyecto** ), las estimaciones de proyecto se basan en la entidad **msdyn\_resourceassignment** ( **Asignación de recursos** ).</span><span class="sxs-lookup"><span data-stu-id="75b58-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="75b58-107">Las asignaciones de recursos se han convertido en el "origen de la verdad" para la programación y fijación de precios de tareas.</span><span class="sxs-lookup"><span data-stu-id="75b58-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="75b58-108">Tareas de línea</span><span class="sxs-lookup"><span data-stu-id="75b58-108">Line tasks</span></span>

<span data-ttu-id="75b58-109">En PSA 3.x, las tareas de línea están obsoletas (en desuso).</span><span class="sxs-lookup"><span data-stu-id="75b58-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="75b58-110">Las asignaciones ahora apuntan a la tarea completa en lugar a las tareas de línea.</span><span class="sxs-lookup"><span data-stu-id="75b58-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="75b58-111">El siguiente ejemplo muestra cómo se asigna una tarea denominada "Tarea de prueba" a los miembros del equipo A y B en versiones anteriores de PSA y en PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="75b58-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="75b58-112">**Antes de PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="75b58-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="75b58-113">Tarea de prueba</span><span class="sxs-lookup"><span data-stu-id="75b58-113">Test task</span></span>

        - <span data-ttu-id="75b58-114">Tarea de prueba: tarea de línea 1</span><span class="sxs-lookup"><span data-stu-id="75b58-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="75b58-115">Asignación a A</span><span class="sxs-lookup"><span data-stu-id="75b58-115">Assignment to A</span></span>

        - <span data-ttu-id="75b58-116">Tarea de prueba: tarea de línea 2</span><span class="sxs-lookup"><span data-stu-id="75b58-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="75b58-117">Asignación a B</span><span class="sxs-lookup"><span data-stu-id="75b58-117">Assignment to B</span></span>

- <span data-ttu-id="75b58-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="75b58-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="75b58-119">Tarea de prueba</span><span class="sxs-lookup"><span data-stu-id="75b58-119">Test task</span></span>

        - <span data-ttu-id="75b58-120">Asignación a A</span><span class="sxs-lookup"><span data-stu-id="75b58-120">Assignment to A</span></span>
        - <span data-ttu-id="75b58-121">Asignación a B</span><span class="sxs-lookup"><span data-stu-id="75b58-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="75b58-122">Asignación sin asignar</span><span class="sxs-lookup"><span data-stu-id="75b58-122">Unassigned assignment</span></span>

<span data-ttu-id="75b58-123">En PSA 3.x, una asignación sin asignar es una asignación que se asigna a un miembro del equipo **NULL** y a un recurso **NULL**.</span><span class="sxs-lookup"><span data-stu-id="75b58-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="75b58-124">Las asignaciones sin asignar pueden producirse en un par de escenarios:</span><span class="sxs-lookup"><span data-stu-id="75b58-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="75b58-125">Si se ha creado una tarea, pero aún no se ha asignado a ningún miembro del equipo, siempre se crea una asignación sin asignar.</span><span class="sxs-lookup"><span data-stu-id="75b58-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="75b58-126">Si se eliminan todas las personas asignadas en una tarea, se vuelve a crear una asignación sin asignar para esa tarea.</span><span class="sxs-lookup"><span data-stu-id="75b58-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="75b58-127">Programación de campos en la entidad Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="75b58-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="75b58-128">Los campos en la entidad **msdyn\_projecttask** están en desuso o se han movido a la entidad **msdyn\_resourceassignment** , o se hace referencia a ella desde la entidad **msdyn\_projectteam** ( **Miembro del equipo del proyecto** ).</span><span class="sxs-lookup"><span data-stu-id="75b58-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="75b58-129">Campo en desuso en msdyn\_projecttask (Tarea de proyecto)</span><span class="sxs-lookup"><span data-stu-id="75b58-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="75b58-130">Nuevo campo en msdyn\_resourceassignment (Asignación de recursos)</span><span class="sxs-lookup"><span data-stu-id="75b58-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="75b58-131">Comentario</span><span class="sxs-lookup"><span data-stu-id="75b58-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="75b58-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="75b58-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="75b58-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="75b58-133">None</span></span> | |
| <span data-ttu-id="75b58-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="75b58-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="75b58-135">Ninguno</span><span class="sxs-lookup"><span data-stu-id="75b58-135">None</span></span> | |
| <span data-ttu-id="75b58-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="75b58-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="75b58-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="75b58-137">None</span></span> | |
| <span data-ttu-id="75b58-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="75b58-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="75b58-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="75b58-139">None</span></span> | |
| <span data-ttu-id="75b58-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="75b58-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="75b58-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="75b58-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="75b58-142">Se ha cambiado el formato de la estructura de datos de notación de objetos JavaScript (JSON) que se almacena en el campo.</span><span class="sxs-lookup"><span data-stu-id="75b58-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="75b58-143">Perfil de programación</span><span class="sxs-lookup"><span data-stu-id="75b58-143">Schedule contour</span></span>

<span data-ttu-id="75b58-144">El perfil de programación se almacena en el campo **Trabajo previsto** ( **msdyn\_plannedwork** ) de cada entidad **Asignación de recursos** ( **msdyn\_resourceassignment** ).</span><span class="sxs-lookup"><span data-stu-id="75b58-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="75b58-145">Estructura</span><span class="sxs-lookup"><span data-stu-id="75b58-145">Structure</span></span>

<span data-ttu-id="75b58-146">La nueva estructura del perfil de programación consta de segmentos de tiempo flexibles que se definen para cada día de la programación.</span><span class="sxs-lookup"><span data-stu-id="75b58-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="75b58-147">Cada sector de tiempo tiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="75b58-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="75b58-148">**Inicio** : el inicio de las horas de trabajo del día, según el calendario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="75b58-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="75b58-149">**Fin** : el final de las horas de trabajo del día, según el calendario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="75b58-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="75b58-150">**Horas** : la cantidad de horas que se asignan en el día.</span><span class="sxs-lookup"><span data-stu-id="75b58-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="75b58-151">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="75b58-151">**Example**</span></span>

<span data-ttu-id="75b58-152">Este ejemplo utiliza un calendario de proyecto donde el día laborable es de 9 a.m. a 5 p.m. en la zona horaria UTC-8.</span><span class="sxs-lookup"><span data-stu-id="75b58-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="75b58-153">Programación automática y programación manual</span><span class="sxs-lookup"><span data-stu-id="75b58-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="75b58-154">Si una tarea se programa automáticamente, las horas se cargan por adelantado y la duración de la tarea puede reducirse.</span><span class="sxs-lookup"><span data-stu-id="75b58-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="75b58-155">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="75b58-155">**Example**</span></span>

<span data-ttu-id="75b58-156">La siguiente tarea se programa automáticamente durante 18 horas durante tres días (del 3 de diciembre de 2018 al 5 de diciembre de 2018).</span><span class="sxs-lookup"><span data-stu-id="75b58-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="75b58-157">Si una tarea se programa manualmente, las horas se distribuyen uniformemente a todas las fechas.</span><span class="sxs-lookup"><span data-stu-id="75b58-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="75b58-158">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="75b58-158">**Example**</span></span>

<span data-ttu-id="75b58-159">La siguiente tarea se programa manualmente durante 18 horas durante tres días (del 3 de diciembre de 2018 al 5 de diciembre de 2018).</span><span class="sxs-lookup"><span data-stu-id="75b58-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="75b58-160">Unidad de asignación</span><span class="sxs-lookup"><span data-stu-id="75b58-160">Assignment unit</span></span>

<span data-ttu-id="75b58-161">La unidad de asignación se ha quedado en desuso en PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="75b58-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="75b58-162">Las horas de esfuerzo de la tarea ahora se dividen en partes iguales, por día, entre todos los recursos asignados.</span><span class="sxs-lookup"><span data-stu-id="75b58-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="75b58-163">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="75b58-163">**Example**</span></span>

<span data-ttu-id="75b58-164">En este ejemplo, la tarea se asigna a dos recursos y se programa automáticamente durante 36 horas durante tres días (del 3 de diciembre de 2018 al 5 de diciembre de 2018).</span><span class="sxs-lookup"><span data-stu-id="75b58-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="75b58-165">Asignación 1:</span><span class="sxs-lookup"><span data-stu-id="75b58-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="75b58-166">Asignación 2:</span><span class="sxs-lookup"><span data-stu-id="75b58-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="75b58-167">Dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="75b58-167">Pricing dimensions</span></span>

<span data-ttu-id="75b58-168">En PSA 3.x, los campos de dimensión de precios específicos de recursos (como **Rol** y **Unidad organizativa** ) se han quitado de la entidad **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="75b58-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="75b58-169">Estos campos ahora se pueden recuperar del miembro del equipo del proyecto correspondiente ( **msdyn\_projectteam** ) de la asignación de recursos ( **msdyn\_resourceassignment** ) cuando se generan estimaciones de proyecto.</span><span class="sxs-lookup"><span data-stu-id="75b58-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="75b58-170">Se ha agregado un nuevo campo, **msdyn\_organizationalunit** , a la entidad **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="75b58-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="75b58-171">Campo en desuso en msdyn\_projecttask (Tarea de proyecto)</span><span class="sxs-lookup"><span data-stu-id="75b58-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="75b58-172">Campo de msdyn\_projectteam (Miembro del equipo del proyecto) que se usa en su lugar</span><span class="sxs-lookup"><span data-stu-id="75b58-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="75b58-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="75b58-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="75b58-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="75b58-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="75b58-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="75b58-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="75b58-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="75b58-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="75b58-177">Perfiles</span><span class="sxs-lookup"><span data-stu-id="75b58-177">Contours</span></span>

<span data-ttu-id="75b58-178">Los campos de perfiles de precios y estimaciones han quedado en desuso en la entidad **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="75b58-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="75b58-179">Se han movido a la entidad **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="75b58-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="75b58-180">Campo en desuso en msdyn\_projecttask (Tarea de proyecto)</span><span class="sxs-lookup"><span data-stu-id="75b58-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="75b58-181">Nuevo campo en msdyn\_resourceassignment (Asignación de recursos)</span><span class="sxs-lookup"><span data-stu-id="75b58-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="75b58-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="75b58-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="75b58-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="75b58-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="75b58-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="75b58-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="75b58-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="75b58-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="75b58-186">Los siguientes campos se han agregado a la entidad **msdyn\_resourceassignment** :</span><span class="sxs-lookup"><span data-stu-id="75b58-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="75b58-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="75b58-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="75b58-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="75b58-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="75b58-189">Los siguientes campos para costes y ventas planificados, reales y restantes no se modifican en la entidad **msdyn\_projecttask** :</span><span class="sxs-lookup"><span data-stu-id="75b58-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="75b58-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="75b58-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="75b58-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="75b58-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="75b58-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="75b58-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="75b58-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="75b58-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="75b58-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="75b58-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="75b58-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="75b58-195">msdyn\_remainingsales</span></span>
