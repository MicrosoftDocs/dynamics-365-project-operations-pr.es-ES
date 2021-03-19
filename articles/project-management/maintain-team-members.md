---
title: Mantener miembros del equipo
description: En este tema se proporciona información sobre cómo reservar recursos con nombre para equipos de proyectos y asignarlos a tareas.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286854"
---
# <a name="maintain-team-members"></a><span data-ttu-id="c304d-103">Mantener miembros del equipo</span><span class="sxs-lookup"><span data-stu-id="c304d-103">Maintain team members</span></span>

<span data-ttu-id="c304d-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="c304d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c304d-105">Puede agregar un recurso designado a su equipo de proyecto, reservándolo directamente para el equipo.</span><span class="sxs-lookup"><span data-stu-id="c304d-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="c304d-106">En Dynamics 365 Project Operations, vaya a **Proyectos** y seleccione el proyecto abierto para el que desea realizar la reserva.</span><span class="sxs-lookup"><span data-stu-id="c304d-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="c304d-107">En la página **Proyecto**, en la pestaña **Equipo**, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="c304d-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="c304d-108">En el cuadro de diálogo **Creación rápida: Miembro del equipo del proyecto**, seleccione el recurso reservable.</span><span class="sxs-lookup"><span data-stu-id="c304d-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="c304d-109">El campo **Rol** se completará con el rol predeterminado del recurso si tiene alguno asignado.</span><span class="sxs-lookup"><span data-stu-id="c304d-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="c304d-110">Puede cambiar el rol.</span><span class="sxs-lookup"><span data-stu-id="c304d-110">You can change the role.</span></span> 
4. <span data-ttu-id="c304d-111">Seleccione las fechas de inicio y finalización en que será necesario el recurso y seleccione el método de asignación de capacidad del recurso.</span><span class="sxs-lookup"><span data-stu-id="c304d-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="c304d-112">En el campo **Aprobador de proyecto**, seleccione **Sí** en caso de que desee que el miembro del equipo sea aprobador de proyecto.</span><span class="sxs-lookup"><span data-stu-id="c304d-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="c304d-113">El miembro del equipo puede aprobar las entradas de gastos y de tiempo enviadas para este proyecto.</span><span class="sxs-lookup"><span data-stu-id="c304d-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="c304d-114">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c304d-114">Select **Save**.</span></span>

<span data-ttu-id="c304d-115">Ahora puede asignar el recurso reservado a las tareas del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c304d-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="c304d-116">En la página **Proyecto**, en la pestaña **Programación**, asigne tareas al nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="c304d-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="c304d-117">El selector de recursos que se inicia desde el campo **Recursos** de la cuadrícula de tareas mostrará los miembros de equipo que se pueden seleccionar.</span><span class="sxs-lookup"><span data-stu-id="c304d-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="c304d-118">En Operaciones de proyectos, las reservas de recursos y las asignaciones de tareas no están estrechamente relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c304d-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="c304d-119">Al usar el selector de recursos en la programación, puede asignar tareas a los miembros del equipo por más horas de las que cubren sus reservas en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="c304d-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="c304d-120">Las diferencias entre las reservas y las asignaciones de los miembros del equipo se muestran en las pestañas **Equipo** y **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="c304d-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="c304d-121">También puede conciliar las diferencias entre las reservas y las asignaciones de recursos a un nivel más detallado.</span><span class="sxs-lookup"><span data-stu-id="c304d-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="c304d-122">Use el selector de recursos de la pestaña **Programación** para buscar y seleccionar recursos reservables que ya no formen parte del equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c304d-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="c304d-123">Estos recursos se muestran en el selector de recursos como **Otros recursos**.</span><span class="sxs-lookup"><span data-stu-id="c304d-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="c304d-124">Al realizar una selección, el recurso se agrega al equipo del proyecto y se asigna a la tarea, pero no se genera ninguna reserva.</span><span class="sxs-lookup"><span data-stu-id="c304d-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="c304d-125">Puede usar la capacidad de ampliación de reserva de la pestaña **Reconciliación** o el **Tablero de programación** para reservar la capacidad del recurso para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="c304d-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="c304d-126">Tras reservar un miembro de equipo en su proyecto, podrá usar **Mantener reservas** o **Panel de programación** directamente para administrar las reservas.</span><span class="sxs-lookup"><span data-stu-id="c304d-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]