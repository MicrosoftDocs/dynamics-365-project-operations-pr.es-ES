---
title: Asignar un recurso a una tarea
description: En este tema se proporciona información sobre cómo asignar recursos a tareas.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085337"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="6f71e-103">Asignar un recurso a una tarea</span><span class="sxs-lookup"><span data-stu-id="6f71e-103">Assign a resource to a task</span></span>

<span data-ttu-id="6f71e-104">Hay tres formas de asignar un recurso a una tarea en Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6f71e-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="6f71e-105">Reservar un recurso como miembro del equipo y después asignar el recurso a una tarea.</span><span class="sxs-lookup"><span data-stu-id="6f71e-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="6f71e-106">Puede agregar un recurso al equipo del proyecto y después asignar el recurso a tareas en la programación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6f71e-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="6f71e-107">En la pestaña **Miembro del equipo** , agregue un nuevo miembro del equipo seleccionando **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="6f71e-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="6f71e-108">Se abrirá el panel **Creación rápida de miembros del equipo** , donde podrá seleccionar el nombre del recurso que se puede reservar y definir un rol.</span><span class="sxs-lookup"><span data-stu-id="6f71e-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="6f71e-109">Seleccione uno de los siguientes métodos de asignación para la reservar del recurso:</span><span class="sxs-lookup"><span data-stu-id="6f71e-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="6f71e-110">**Plena capacidad** reserva la capacidad completa del recurso para fechas especificadas de inicio y fin.</span><span class="sxs-lookup"><span data-stu-id="6f71e-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="6f71e-111">**Porcentaje de capacidad** reserva el recurso para un porcentaje de capacidad del recurso para las fechas especificadas de inicio y fin.</span><span class="sxs-lookup"><span data-stu-id="6f71e-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="6f71e-112">**Por horas: distribuir equitativamente** reserva el recurso durante un número específico de horas de manera uniforme por día durante el periodo especificado entre las fechas de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="6f71e-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="6f71e-113">**Por horas: cargo por adelantado** reserva el recurso para un número especificado de horas, cargando por adelantado las horas diarias a lo largo de las fechas de inicio y fin especificadas.</span><span class="sxs-lookup"><span data-stu-id="6f71e-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="6f71e-114">**Ninguno** agrega el recurso al equipo, pero no crea ninguna reserva que absorba su capacidad.</span><span class="sxs-lookup"><span data-stu-id="6f71e-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="6f71e-115">En la cuadrícula **Programación** de una tarea, seleccione el icono **Recurso** en la celda de recursos y después, en **Miembros del equipo** , seleccione el miembro del equipo que acaba de agregar.</span><span class="sxs-lookup"><span data-stu-id="6f71e-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="6f71e-116">En las pestañas **Miembro del equipo** y **Conciliación** , el recurso muestra las horas reservadas y las horas asignadas.</span><span class="sxs-lookup"><span data-stu-id="6f71e-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="6f71e-117">Las horas deben ser las mismas, pero no necesariamente, ya que las reservas y las asignaciones no están emparejadas firmemente.</span><span class="sxs-lookup"><span data-stu-id="6f71e-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="6f71e-118">La pestaña **Conciliación** proporciona detalles cuando son diferentes, como cuando se asigna un recurso por más horas de las que se ha reservado.</span><span class="sxs-lookup"><span data-stu-id="6f71e-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="6f71e-119">Si es necesario, puede corregir la información ampliando las reservas del recurso, o bien modificando la asignación.</span><span class="sxs-lookup"><span data-stu-id="6f71e-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="6f71e-120">Crear un miembro del equipo genérico con la asignación de tareas</span><span class="sxs-lookup"><span data-stu-id="6f71e-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="6f71e-121">Cuando cree un miembro del equipo genérico mediante la asignación de tareas, cree un marcador de posición o un recurso genérico que describa las características del recurso con nombre que desea que trabaje en las tareas.</span><span class="sxs-lookup"><span data-stu-id="6f71e-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="6f71e-122">A continuación, genere un requisito (o envíe una solicitud con el requisito) que se usará para buscar y reservar el recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="6f71e-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="6f71e-123">En la cuadrícula **Programación** de una tarea, seleccione el icono **Recurso** en la celda del recurso.</span><span class="sxs-lookup"><span data-stu-id="6f71e-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="6f71e-124">Escriba un nombre que sirva como nombre del recurso de marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="6f71e-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="6f71e-125">Por ejemplo, Administrador de programas.</span><span class="sxs-lookup"><span data-stu-id="6f71e-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="6f71e-126">Seleccione **Crear** y, en el campo **Creación rápida de miembro del equipo de proyecto** , defina el rol para el recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="6f71e-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="6f71e-127">Puede continuar asignando tareas a este recurso de marcador de posición seleccionando el recurso en el **Selector de recursos** para la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f71e-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="6f71e-128">Aparecen en **Miembros del equipo**.</span><span class="sxs-lookup"><span data-stu-id="6f71e-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="6f71e-129">Cuando termine de asignar el recurso genérico, seleccione el recurso genérico en la pestaña **Equipo** y después seleccione **Generar requisito** para crear un requisito de recursos para el recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="6f71e-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="6f71e-130">Seleccione **Reservar** para el recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="6f71e-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="6f71e-131">Puede usar posteriormente el Tablero de programación para buscar y reservar un recurso real.</span><span class="sxs-lookup"><span data-stu-id="6f71e-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="6f71e-132">También puede enviar el requisito para que lo satisfaga un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f71e-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="6f71e-133">Cuando el recurso genérico se satisfaga con un recurso con nombre, se quitará el recurso genérico del equipo y las asignaciones de tarea para el recurso genérico se asignarán al recurso con nombre que satisfizo el requisito del recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="6f71e-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="6f71e-134">Asignar un recurso con nombre de la lista de todos los recursos reservables</span><span class="sxs-lookup"><span data-stu-id="6f71e-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="6f71e-135">Puede usar el cuadro de búsqueda en el **Selector de recursos** para buscar todos los recursos reservables y asignarlos a una tarea.</span><span class="sxs-lookup"><span data-stu-id="6f71e-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="6f71e-136">Los recursos asignados de esta manera se agregan al equipo sin ninguna reserva.</span><span class="sxs-lookup"><span data-stu-id="6f71e-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="6f71e-137">Esto es similar a agregar un miembro del equipo y seleccionar Ninguno como método de asignación.</span><span class="sxs-lookup"><span data-stu-id="6f71e-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="6f71e-138">El recurso se muestra en las pestañas **Equipo** y **Conciliación** como recursos solo con asignaciones y un déficit de reserva.</span><span class="sxs-lookup"><span data-stu-id="6f71e-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="6f71e-139">Resérvelos si desea usar su disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="6f71e-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="6f71e-140">En la cuadrícula **Programación** de una tarea, seleccione el icono **Recurso** en la celda del recurso.</span><span class="sxs-lookup"><span data-stu-id="6f71e-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="6f71e-141">Empiece a escribir un nombre.</span><span class="sxs-lookup"><span data-stu-id="6f71e-141">Start typing a name.</span></span> <span data-ttu-id="6f71e-142">Los resultados de búsqueda del nombre se muestran en el **Selector de recursos** en **Otros recursos**.</span><span class="sxs-lookup"><span data-stu-id="6f71e-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="6f71e-143">Seleccione el recurso que desee asignar a la tarea.</span><span class="sxs-lookup"><span data-stu-id="6f71e-143">Select the resource that you want to assign to the task.</span></span>

