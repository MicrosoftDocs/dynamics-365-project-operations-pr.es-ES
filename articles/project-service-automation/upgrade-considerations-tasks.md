---
title: Consideraciones de actualización para la estructura de descomposición del trabajo
description: En este tema se proporciona información sobre cómo actualizar la estructura de descomposición del trabajo de Project Service Automation 2.x a 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756042"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="18ec7-103">Consideraciones de actualización para la estructura de descomposición del trabajo</span><span class="sxs-lookup"><span data-stu-id="18ec7-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="18ec7-104">En este tema se proporciona información sobre cómo actualizar la estructura de descomposición del trabajo de Project Service Automation 2.x a 3.x.</span><span class="sxs-lookup"><span data-stu-id="18ec7-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="18ec7-105">Este tema define el estado correcto de un proyecto en Project Service Automation (PSA) necesario para realizar una actualización correcta.</span><span class="sxs-lookup"><span data-stu-id="18ec7-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="18ec7-106">También incluye información sobre las condiciones de bloqueo comunes que harán que se produzca un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="18ec7-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="18ec7-107">Para obtener más información sobre cómo definir las tareas del proyecto y sus funciones dentro de una programación del proyecto, consulte [Programaciones del proyecto](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="18ec7-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="18ec7-108">Entidades clave</span><span class="sxs-lookup"><span data-stu-id="18ec7-108">Key entities</span></span>
<span data-ttu-id="18ec7-109">Para una estructura de descomposición del trabajo precisa que ya esté cargada de recursos, se requieren las siguientes entidades:</span><span class="sxs-lookup"><span data-stu-id="18ec7-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="18ec7-110">Proyecto</span><span class="sxs-lookup"><span data-stu-id="18ec7-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="18ec7-111">Equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="18ec7-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="18ec7-112">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="18ec7-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="18ec7-113">Asignaciones de recursos</span><span class="sxs-lookup"><span data-stu-id="18ec7-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="18ec7-114">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="18ec7-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="18ec7-115">Recursos que se pueden reservar</span><span class="sxs-lookup"><span data-stu-id="18ec7-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="18ec7-116">Para definir una estructura de descomposición del trabajo cargada de recursos, debe completar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="18ec7-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="18ec7-117">Crear un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-117">Create a new project.</span></span> <span data-ttu-id="18ec7-118">Para obtener más información sobre cómo crear un nuevo proyecto, consulte [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="18ec7-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="18ec7-119">Crear una o varias tareas.</span><span class="sxs-lookup"><span data-stu-id="18ec7-119">Create one or more tasks.</span></span> <span data-ttu-id="18ec7-120">Para obtener más información sobre cómo crear una tarea, consulte [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="18ec7-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="18ec7-121">Definir las dependencias entre tareas.</span><span class="sxs-lookup"><span data-stu-id="18ec7-121">Define the task dependencies.</span></span> <span data-ttu-id="18ec7-122">Para obtener más información, consulte [Dependencia de tareas de proyecto](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="18ec7-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="18ec7-123">Asignar miembros del equipo de proyecto al proyecto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-123">Assign project team members to the project.</span></span> <span data-ttu-id="18ec7-124">Para obtener más información, consulte [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="18ec7-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="18ec7-125">Asignar miembros del equipo de proyecto a las tareas.</span><span class="sxs-lookup"><span data-stu-id="18ec7-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="18ec7-126">Para obtener más información, consulte [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="18ec7-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="18ec7-127">Relaciones del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="18ec7-127">Project team relationships</span></span>

<span data-ttu-id="18ec7-128">Para garantizar una actualización correcta, deben conservarse correctamente las siguientes relaciones:</span><span class="sxs-lookup"><span data-stu-id="18ec7-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="18ec7-129">Todos los miembros del equipo del proyecto deben asociarse con un recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="18ec7-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="18ec7-130">Todos los miembros del equipo del proyecto deben asociarse con el mismo proyecto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="18ec7-131">Relaciones de tareas del proyecto</span><span class="sxs-lookup"><span data-stu-id="18ec7-131">Project task relationships</span></span>
<span data-ttu-id="18ec7-132">Para garantizar una actualización correcta, deben conservarse correctamente las siguientes relaciones:</span><span class="sxs-lookup"><span data-stu-id="18ec7-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="18ec7-133">Cualquier tarea relacionada debe estar asociada al mismo proyecto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="18ec7-134">Cada tarea de línea debe tener una tarea principal.</span><span class="sxs-lookup"><span data-stu-id="18ec7-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="18ec7-135">Cada tarea de línea debe tener un proyecto principal.</span><span class="sxs-lookup"><span data-stu-id="18ec7-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="18ec7-136">Condiciones válidas</span><span class="sxs-lookup"><span data-stu-id="18ec7-136">Valid conditions</span></span>

- <span data-ttu-id="18ec7-137">Todas las duraciones de la tarea deben ser superiores o iguales a (>=) una hora e inferiores a 1 800 000 minutos (1250 días).\*</span><span class="sxs-lookup"><span data-stu-id="18ec7-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="18ec7-138">Todas las tareas deben tener una fecha de inicio no anterior al 01/01/2000.\*</span><span class="sxs-lookup"><span data-stu-id="18ec7-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="18ec7-139">Todas las tareas deben tener una fecha de inicio no posterior a 17 años desde el día actual.\*</span><span class="sxs-lookup"><span data-stu-id="18ec7-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="18ec7-140">Todas las tareas deben tener una fecha de inicio anterior o igual a la fecha de finalización.</span><span class="sxs-lookup"><span data-stu-id="18ec7-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="18ec7-141">Todos los tipos de transacciones en las clasificaciones (Gastos, Material, Impuestos y Tiempo) deben tener valores para **Unidad predeterminada** y **Unidad de venta**.</span><span class="sxs-lookup"><span data-stu-id="18ec7-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="18ec7-142">Se deben evitar los formatos de fecha con letras.</span><span class="sxs-lookup"><span data-stu-id="18ec7-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="18ec7-143">Pasos de mitigación potenciales</span><span class="sxs-lookup"><span data-stu-id="18ec7-143">Potential mitigation steps</span></span>
- <span data-ttu-id="18ec7-144">Use la Búsqueda avanzada para identificar Tareas de proyecto que no contengan un Id. de proyecto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="18ec7-145">Use la Búsqueda avanzada para identificar Tareas de proyecto donde la duración programada sea superior a > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="18ec7-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="18ec7-146">Antes de realizar cambios en los datos, debe investigar cualquier personalización asociada a la entidad que pueda haber ocasionado el mal estado de los datos.</span><span class="sxs-lookup"><span data-stu-id="18ec7-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="18ec7-147">Estas personalizaciones deben abordarse antes de continuar con cualquier actualización relacionada con los datos.</span><span class="sxs-lookup"><span data-stu-id="18ec7-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="18ec7-148">Para las tareas identificadas que han quedado huérfanas, considere eliminar estas tareas si no son necesarias o si deberían asociarse al proyecto primario correcto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="18ec7-149">Para cualquier tarea donde la duración sea superior a 1250 días, considere agregar varias tareas para representar la duración total, si es viable.</span><span class="sxs-lookup"><span data-stu-id="18ec7-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="18ec7-150">Los elementos señalados con un asterisco (\*) tienen límites que se deben al hecho de que la administración de relaciones con el cliente (CRM) solo admite 7320 expansiones recurrentes.</span><span class="sxs-lookup"><span data-stu-id="18ec7-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="18ec7-151">Debe mantenerse por debajo de este límite.</span><span class="sxs-lookup"><span data-stu-id="18ec7-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="18ec7-152">Relaciones de asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="18ec7-152">Resource Assignment relationships</span></span>
<span data-ttu-id="18ec7-153">Para garantizar una actualización correcta, deben conservarse correctamente las siguientes relaciones:</span><span class="sxs-lookup"><span data-stu-id="18ec7-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="18ec7-154">Todas las asignaciones de recursos en una estructura de descomposición del trabajo deben estar relacionadas con el mismo proyecto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="18ec7-155">Todas las asignaciones de recursos en una estructura de descomposición del trabajo deben estar asociadas a los miembros del equipo del proyecto en el mismo proyecto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="18ec7-156">Pasos de mitigación potenciales</span><span class="sxs-lookup"><span data-stu-id="18ec7-156">Potential mitigation steps</span></span>
- <span data-ttu-id="18ec7-157">Identifique todas las tareas que se encuentra fuera de las condiciones descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18ec7-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="18ec7-158">Debe eliminarse cualquier asignación de recursos que ya no sea válida.</span><span class="sxs-lookup"><span data-stu-id="18ec7-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="18ec7-159">Relaciones de dependencia de tareas del proyecto</span><span class="sxs-lookup"><span data-stu-id="18ec7-159">Project task dependency relationships</span></span>
<span data-ttu-id="18ec7-160">Para garantizar una actualización correcta, deben conservarse correctamente las siguientes relaciones:</span><span class="sxs-lookup"><span data-stu-id="18ec7-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="18ec7-161">Todas las dependencias de tareas del proyecto deben estar relacionadas con el mismo proyecto.</span><span class="sxs-lookup"><span data-stu-id="18ec7-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="18ec7-162">Una tarea no puede tener la misma dependencia referenciada más de una vez.</span><span class="sxs-lookup"><span data-stu-id="18ec7-162">A task can't have the same dependency referenced more than once.</span></span>
