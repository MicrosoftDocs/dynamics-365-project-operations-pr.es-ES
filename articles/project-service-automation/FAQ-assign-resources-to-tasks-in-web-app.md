---
title: ¿Cómo asigno un recurso que se puede reservar a una tarea en la aplicación web?
description: Información general de las distintas maneras en que puede asignar recursos reservables.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756102"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="07e5d-103">¿Cómo asignar un recurso que se puede reservar a una tarea en la aplicación web (aplicación Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="07e5d-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="07e5d-104">Hay dos formas de asignar un recurso a una tarea en Project Service.</span><span class="sxs-lookup"><span data-stu-id="07e5d-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="07e5d-105">Puede reservar un recurso como integrante del equipo y después asignarlo a una tarea.</span><span class="sxs-lookup"><span data-stu-id="07e5d-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="07e5d-106">O puede crear un miembro del equipo genérico con la asignación de roles en tareas, generar un equipo y, a continuación satisfacer los requisitos de apoyo con un recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="07e5d-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="07e5d-107">Tenga en cuenta que si desea asignar un recurso que se puede reservar a una tarea, el integrante del equipo del recurso que se puede reservar debe tener suficientes reservas disponibles.</span><span class="sxs-lookup"><span data-stu-id="07e5d-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="07e5d-108">El estado de la reserva debe ser Tipo de confirmación - Reserva manual y Estado confirmado.</span><span class="sxs-lookup"><span data-stu-id="07e5d-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="07e5d-109">Si no hay reservas suficientes para el recurso, Project Service quita la asignación y muestra el siguiente mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="07e5d-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="07e5d-110">*No se puede asignar recurso a tarea - los siguientes recursos no tienen suficientes horas reservadas para el proyecto*</span><span class="sxs-lookup"><span data-stu-id="07e5d-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="07e5d-111">Reserve un recurso como integrante del equipo y después asigne el recurso a una tarea.</span><span class="sxs-lookup"><span data-stu-id="07e5d-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="07e5d-112">Con este método agrega un recurso al equipo del proyecto y después asigna tareas al recurso en el calendario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="07e5d-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="07e5d-113">Esta es la forma de hacerlo:</span><span class="sxs-lookup"><span data-stu-id="07e5d-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="07e5d-114">En la cuadrícula de miembros del equipo, agregue un nuevo miembro del equipo seleccionando **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="07e5d-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="07e5d-115">En la pantalla de creación rápida de Miembros del equipo, seleccione el nombre del recurso que se puede reservar y defina un rol.</span><span class="sxs-lookup"><span data-stu-id="07e5d-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="07e5d-116">Seleccione las fechas **Desde** y **Hasta**.</span><span class="sxs-lookup"><span data-stu-id="07e5d-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="07e5d-117">![Captura de pantalla de la adición de un miembro del equipo](media/FAQ-Resources-to-Tasks2-1.png "Captura de pantalla de la adición de un miembro del equipo")</span><span class="sxs-lookup"><span data-stu-id="07e5d-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="07e5d-118">Seleccione uno de los siguientes métodos de asignación para reservar el recurso:</span><span class="sxs-lookup"><span data-stu-id="07e5d-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="07e5d-119">**Plena capacidad** reserva la capacidad completa del recurso para fechas especificadas de inicio y fin.</span><span class="sxs-lookup"><span data-stu-id="07e5d-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="07e5d-120">**Porcentaje de capacidad** reserva el recurso para un porcentaje de capacidad del recurso para las fechas especificadas de inicio y fin.</span><span class="sxs-lookup"><span data-stu-id="07e5d-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="07e5d-121">**Por horas: distribuir equitativamente** reserva el recurso para un número especificado de horas, distribuyéndolo uniformemente por día a lo largo de las fechas de inicio y fin especificadas.</span><span class="sxs-lookup"><span data-stu-id="07e5d-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="07e5d-122">**Por horas: cargo por adelantado** reserva el recurso para un número especificado de horas, cargando por adelantado las horas diarias a lo largo de las fechas de inicio y fin especificadas.</span><span class="sxs-lookup"><span data-stu-id="07e5d-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="07e5d-123">No seleccione **Ninguno** porque agrega el recurso al equipo, pero no crea ninguna reserva que absorba la capacidad del recurso.</span><span class="sxs-lookup"><span data-stu-id="07e5d-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="07e5d-124">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="07e5d-124">Select **Save**.</span></span>

    <span data-ttu-id="07e5d-125">Tenga en cuenta que las horas de la reserva deben ser suficientes para satisfacer las horas de esfuerzo y los intervalos de fechas de las tareas a las que asigna este recurso.</span><span class="sxs-lookup"><span data-stu-id="07e5d-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="07e5d-126">Si no están alineados, no puede asignar el recurso a la tarea.</span><span class="sxs-lookup"><span data-stu-id="07e5d-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="07e5d-127">En la estructura de descomposición del trabajo (WBS) para la tarea, haga clic en la lista desplegable de celdas del recurso.</span><span class="sxs-lookup"><span data-stu-id="07e5d-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="07e5d-128">A continuación:</span><span class="sxs-lookup"><span data-stu-id="07e5d-128">Then:</span></span> 

    1. <span data-ttu-id="07e5d-129">Seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="07e5d-129">Select **Add**.</span></span>
    2. <span data-ttu-id="07e5d-130">Seleccione la lista desplegable en **Recursos** y seleccione el integrante del equipo que agregó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="07e5d-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="07e5d-131">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="07e5d-131">Select **OK**.</span></span> <span data-ttu-id="07e5d-132">Ahora el integrante del equipo está asignado a la tarea.</span><span class="sxs-lookup"><span data-stu-id="07e5d-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="07e5d-133">![Captura de pantalla de la adición de recursos con WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de pantalla de la adición de recursos con WBS")</span><span class="sxs-lookup"><span data-stu-id="07e5d-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="07e5d-134">En la cuadrícula de miembros del equipo, verá el agregado de las horas asignadas del recurso en Horas asignadas.</span><span class="sxs-lookup"><span data-stu-id="07e5d-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="07e5d-135">Será menor o igual que las horas reservadas para el recurso.</span><span class="sxs-lookup"><span data-stu-id="07e5d-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="07e5d-136">![Captura de pantalla de horas asignadas para un recurso](media/FAQ-Resources-to-Tasks2-3.png "Captura de pantalla de horas asignadas para un recurso")</span><span class="sxs-lookup"><span data-stu-id="07e5d-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="07e5d-137">Si la tarea que intenta asignar al recurso se inicia después de la fecha de finalización de las reservas de recursos, el recurso no aparecerá en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="07e5d-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="07e5d-138">Tenga en cuenta que puede asignar un recurso a más horas que las horas reservadas si el recurso tiene capacidad restante sin asignar.</span><span class="sxs-lookup"><span data-stu-id="07e5d-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="07e5d-139">En este caso el recurso solo se asignará parcialmente a sus reservas.</span><span class="sxs-lookup"><span data-stu-id="07e5d-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="07e5d-140">Puede ver estas horas restantes de tarea no asignadas agregando la columna Horas sin dotación de personal a la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="07e5d-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="07e5d-141">Si hay recursos asignados a sus horas reservadas (sus horas reservadas son igual a las horas asignadas), verá el siguiente mensaje de error al intentar asignarles aún más tareas:</span><span class="sxs-lookup"><span data-stu-id="07e5d-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="07e5d-142">*No se puede asignar recurso a tarea - los siguientes recursos no tienen suficientes horas reservadas para el proyecto.*</span><span class="sxs-lookup"><span data-stu-id="07e5d-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="07e5d-143">Además, el integrante del equipo jefe de proyecto predeterminado que se agrega al equipo cuando se crea el proyecto se agrega sin reservas y no se puede asignar a ninguna tarea.</span><span class="sxs-lookup"><span data-stu-id="07e5d-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="07e5d-144">No aparecerá en la lista desplegable de recursos para las tareas.</span><span class="sxs-lookup"><span data-stu-id="07e5d-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="07e5d-145">Si desea asignar este recurso, debe quitarlo del equipo y después volver a agregarlo con un método de asignación distinto de Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07e5d-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="07e5d-146">La razón por la que se agregan al equipo cuando se crea el proyecto es que un proyecto tiene al menos un aprobador de proyecto de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="07e5d-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="07e5d-147">Cree un miembro del equipo genérico con la asignación de roles en tareas</span><span class="sxs-lookup"><span data-stu-id="07e5d-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="07e5d-148">Este método garantiza que los recursos tienen reservas suficientes para las tareas.</span><span class="sxs-lookup"><span data-stu-id="07e5d-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="07e5d-149">Primero, cree un marcador de posición o un recurso genérico que describa las características del recurso con nombre en el que en definitiva desea trabajar en las tareas generando un equipo después de asignar roles a tareas.</span><span class="sxs-lookup"><span data-stu-id="07e5d-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="07e5d-150">Esta es la forma de hacerlo:</span><span class="sxs-lookup"><span data-stu-id="07e5d-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="07e5d-151">En la estructura de descomposición del trabajo, seleccione una tarea.</span><span class="sxs-lookup"><span data-stu-id="07e5d-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="07e5d-152">Seleccione el icono desplegable **Rol asignado** en la celda del recurso.</span><span class="sxs-lookup"><span data-stu-id="07e5d-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="07e5d-153">Seleccione el desplegable **Rol** y seleccione el rol para el recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="07e5d-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="07e5d-154">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="07e5d-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="07e5d-155">![Captura de pantalla del uso de WBS para agregar recurso](media/FAQ-Resources-to-Tasks2-4.png "Captura de pantalla del uso de WBS para agregar recurso")</span><span class="sxs-lookup"><span data-stu-id="07e5d-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="07e5d-156">Una vez finalizada la asignación de roles a las tareas en la WBS, seleccione **Generar equipo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="07e5d-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="07e5d-157">Project Service crea el número mínimo de integrantes del equipo genéricos basados en roles, unidades organizativas de recursos y el calendario de proyecto agregando las asignaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="07e5d-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="07e5d-158">![Captura de pantalla de la generación de equipo de proyecto](media/FAQ-Resources-to-Tasks2-5.png "Captura de pantalla de la generación de equipo de proyecto")</span><span class="sxs-lookup"><span data-stu-id="07e5d-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="07e5d-159">En la cuadrícula Miembro del equipo, verá recursos del tipo de Recurso genérico con el rol y el nombre del puesto.</span><span class="sxs-lookup"><span data-stu-id="07e5d-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="07e5d-160">Si se necesitan dos recursos para que un rol complete el trabajo, la característica Generar equipo crea dos integrantes del equipo y usa el nombre del puesto para diferenciarlos.</span><span class="sxs-lookup"><span data-stu-id="07e5d-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="07e5d-161">![Captura de pantalla de la adición de dos recursos genéricos](media/FAQ-Resources-to-Tasks2-6.png "Captura de pantalla de la adición de dos recursos genéricos")</span><span class="sxs-lookup"><span data-stu-id="07e5d-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="07e5d-162">Puede abrir el requisitos de recursos de apoyo para el integrante del equipo genérico seleccionando el vínculo en Requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="07e5d-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="07e5d-163">![Captura de pantalla de la apertura de requisito de recursos de apoyo](media/FAQ-Resources-to-Tasks2-7.png "Captura de pantalla de la apertura de requisito de recursos de apoyo")</span><span class="sxs-lookup"><span data-stu-id="07e5d-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="07e5d-164">Seleccione **Reservar** para el recurso genérico, y entonces podrá usar el tablero de programación para buscar y reservar un recurso real.</span><span class="sxs-lookup"><span data-stu-id="07e5d-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="07e5d-165">También puede enviar el requisito para que lo satisfaga un administrador de recursos seleccionando **Mostrar la solicitud**.</span><span class="sxs-lookup"><span data-stu-id="07e5d-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="07e5d-166">Cuando el recurso genérico se satisfaga con un recurso con nombre, se quitará el recurso genérico del equipo y las asignaciones de tarea para el recurso genérico se asignarán al recurso con nombre que satisfizo el requisito del recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="07e5d-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

