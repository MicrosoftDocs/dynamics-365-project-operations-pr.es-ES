---
title: Reservar recursos con nombre que se pueden reservar para un equipo de proyecto y asignar tareas
description: En este tema se proporciona información sobre cómo reservar recursos con nombre para equipos de proyectos y asignarlos a tareas.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145379"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="973ce-103">Reservar recursos con nombre que se pueden reservar para un equipo de proyecto y asignar tareas</span><span class="sxs-lookup"><span data-stu-id="973ce-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="973ce-104">Puede agregar un recurso con nombre a su equipo de proyecto reservándolo directamente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="973ce-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="973ce-105">Para ello, complete los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="973ce-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="973ce-106">En Project Service Automation, vaya a **Proyectos** y seleccione el proyecto abierto para el que desea realizar la reserva.</span><span class="sxs-lookup"><span data-stu-id="973ce-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="973ce-107">En la página **Proyecto**, en la pestaña **Equipo**, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="973ce-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Agregar un miembro de equipo desde la pestaña del equipo](media/RM-how-to-1.png)

3. <span data-ttu-id="973ce-109">En el cuadro de diálogo **Creación rápida: Miembro del equipo del proyecto**, seleccione el recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="973ce-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="973ce-110">El campo **Rol** se completará con el rol predeterminado del recurso si tiene alguno asignado.</span><span class="sxs-lookup"><span data-stu-id="973ce-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="973ce-111">Puede cambiar el rol si fuera necesario.</span><span class="sxs-lookup"><span data-stu-id="973ce-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="973ce-112">Seleccione las fechas de inicio y finalización del tiempo que será necesario el recurso y seleccione el método de asignación de capacidad del recurso.</span><span class="sxs-lookup"><span data-stu-id="973ce-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="973ce-113">Si desea que el miembro del equipo sea un aprobador de proyecto, seleccione **Sí** en el campo **Aprobador de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="973ce-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="973ce-114">Esto significa que el miembro del equipo podrá aprobar las entradas de gastos y de tiempo que se envíen para este proyecto.</span><span class="sxs-lookup"><span data-stu-id="973ce-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="973ce-115">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="973ce-115">Click **Save**.</span></span>

![Agregar un miembro de equipo en el formulario de creación rápida](media/RM-how-to-2.png)


<span data-ttu-id="973ce-117">Ahora puede asignar el recurso reservado a las tareas del proyecto.</span><span class="sxs-lookup"><span data-stu-id="973ce-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="973ce-118">En la página **Proyecto**, haga clic en la pestaña **Programación** para asignar tareas al nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="973ce-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="973ce-119">El selector de recursos que se inicia desde el campo **Recursos** de la cuadrícula de tareas mostrará los miembros de equipo que se pueden seleccionar.</span><span class="sxs-lookup"><span data-stu-id="973ce-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Asignación de un miembro de equipo a una tarea en la pestaña de programación](media/RM-how-to-3.png)

<span data-ttu-id="973ce-121">En la versión 3 de Project Service Automation (PSA), las reservas de recursos y las asignaciones de tareas no están emparejadas firmemente.</span><span class="sxs-lookup"><span data-stu-id="973ce-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="973ce-122">Esto significa que al usar el selector de recursos en la programación, puede asignar tareas a los miembros del equipo por más horas de las cubren sus reservas en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="973ce-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="973ce-123">Puede ver las diferencias que hay entre las asignaciones y las reservas de los miembros de equipo en la pestaña **Equipo** o en la pestaña **Conciliación de recursos**. También puede conciliar las diferencias entre las reservas y las asignaciones de los recursos en un nivel más detallado.</span><span class="sxs-lookup"><span data-stu-id="973ce-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Pestaña Conciliación de recursos](media/RM-how-to-4.png)

<span data-ttu-id="973ce-125">También puede usar el selector de recursos de la pestaña **Programación** para buscar y seleccionar recursos que se pueden reservar que ya no formen parte del equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="973ce-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="973ce-126">Estos se muestran en el selector de recursos como **Otros recursos**.</span><span class="sxs-lookup"><span data-stu-id="973ce-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Asignación de un recurso que no es miembro del equipo a una tarea](media/RM-how-to-5.png)

<span data-ttu-id="973ce-128">En este tipo de asignaciones, el recurso se agrega al equipo del proyecto y se asigna a la tarea, pero no se genera ninguna reserva.</span><span class="sxs-lookup"><span data-stu-id="973ce-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Miembro del equipo con asignaciones y sin reservas](media/RM-how-to-6.png)

<span data-ttu-id="973ce-130">Puede usar la capacidad de ampliación de reserva de la pestaña **Reconciliación** o el **Tablero de programación** para reservar la capacidad del recurso para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="973ce-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Ampliación de la reserva de un miembro del equipo en la pestaña Conciliación de recursos](media/RM-how-to-7.png)

<span data-ttu-id="973ce-132">Tras reservar un miembro de equipo en su proyecto, podrá mantener las reservas o utilizar el Tablero de programación directamente para administrar las reservas.</span><span class="sxs-lookup"><span data-stu-id="973ce-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
