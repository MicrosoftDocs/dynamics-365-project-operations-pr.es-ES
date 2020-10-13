---
title: Reservar para un proyecto
description: En este tema se proporciona información sobre la reserva de un recurso para un proyecto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908635"
---
# <a name="book-to-a-project"></a><span data-ttu-id="54adc-103">Reservar para un proyecto</span><span class="sxs-lookup"><span data-stu-id="54adc-103">Book to a project</span></span>

<span data-ttu-id="54adc-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="54adc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="54adc-105">Hay ocasiones en las que un administrador de proyecto o un administrador de recursos necesitará asignar un recurso al proyecto sin que un miembro genérico del equipo defina un requisito específico.</span><span class="sxs-lookup"><span data-stu-id="54adc-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="54adc-106">Esto se puede lograr de una de tres maneras.</span><span class="sxs-lookup"><span data-stu-id="54adc-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="54adc-107">Reservar desde la cuadrícula de miembros del equipo</span><span class="sxs-lookup"><span data-stu-id="54adc-107">Book from the team member grid</span></span>
- <span data-ttu-id="54adc-108">Reservar desde el tablero de programación</span><span class="sxs-lookup"><span data-stu-id="54adc-108">Book from the schedule board</span></span>
- <span data-ttu-id="54adc-109">Reservar desde el formulario **Proyecto**</span><span class="sxs-lookup"><span data-stu-id="54adc-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="54adc-110">Reservar desde la cuadrícula de miembros del equipo</span><span class="sxs-lookup"><span data-stu-id="54adc-110">Book from the team member grid</span></span>

<span data-ttu-id="54adc-111">Si su organización está operando en modo de asignación de recursos híbrido, el gerente de proyecto puede reservar un recurso directamente para el proyecto completando los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="54adc-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="54adc-112">Desde el proyecto, vaya a la cuadrícula de miembros del equipo y seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="54adc-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="54adc-113">Defina el nombre del puesto y el rol del recurso.</span><span class="sxs-lookup"><span data-stu-id="54adc-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="54adc-114">Seleccione el recurso reservable en la búsqueda disponible.</span><span class="sxs-lookup"><span data-stu-id="54adc-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="54adc-115">Después de seleccionar el recurso, defina la siguiente información de campo para reservar el recurso:</span><span class="sxs-lookup"><span data-stu-id="54adc-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="54adc-116">Fecha de inicio</span><span class="sxs-lookup"><span data-stu-id="54adc-116">Start date</span></span>
    - <span data-ttu-id="54adc-117">Fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="54adc-117">Finish date</span></span>
    - <span data-ttu-id="54adc-118">Método de asignación</span><span class="sxs-lookup"><span data-stu-id="54adc-118">Allocation method</span></span>
    - <span data-ttu-id="54adc-119">Horas, si es aplicable</span><span class="sxs-lookup"><span data-stu-id="54adc-119">Hours, if applicable</span></span>
    - <span data-ttu-id="54adc-120">Aprobador de proyecto</span><span class="sxs-lookup"><span data-stu-id="54adc-120">Project approver</span></span>

6. <span data-ttu-id="54adc-121">Seleccione **Guardar y cerrar**</span><span class="sxs-lookup"><span data-stu-id="54adc-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="54adc-122">Reservar desde el tablero de programación</span><span class="sxs-lookup"><span data-stu-id="54adc-122">Book from the schedule board</span></span>

<span data-ttu-id="54adc-123">Cuando un administrador de recursos necesita reservar un recurso directamente para un proyecto, puede usar el tablero de programación y los requisitos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="54adc-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="54adc-124">El requisito del proyecto es un requisito de recursos que siempre está disponible para reservar respecto a él.</span><span class="sxs-lookup"><span data-stu-id="54adc-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="54adc-125">Para reservar directamente para un proyecto desde el panel de programación, complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="54adc-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="54adc-126">Navegue hasta el panel de programación y, en la página de la izquierda, filtre los recursos que está considerando para el requisito.</span><span class="sxs-lookup"><span data-stu-id="54adc-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="54adc-127">En el panel inferior, seleccione la pestaña **Proyecto** para ver una lista de los requisitos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="54adc-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="54adc-128">Arrastre el requisito a un recurso y defina la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="54adc-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="54adc-129">Fecha de inicio</span><span class="sxs-lookup"><span data-stu-id="54adc-129">Start date</span></span>
    - <span data-ttu-id="54adc-130">Fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="54adc-130">Finish date</span></span>
    - <span data-ttu-id="54adc-131">Estado de reserva</span><span class="sxs-lookup"><span data-stu-id="54adc-131">Booking status</span></span>
    - <span data-ttu-id="54adc-132">Método de reserva</span><span class="sxs-lookup"><span data-stu-id="54adc-132">Booking method</span></span>
    - <span data-ttu-id="54adc-133">Duración</span><span class="sxs-lookup"><span data-stu-id="54adc-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="54adc-134">Reservar desde el formulario Proyecto</span><span class="sxs-lookup"><span data-stu-id="54adc-134">Book from the Project form</span></span>

<span data-ttu-id="54adc-135">Como gerente de proyecto, es posible que deba reservar un recurso para un proyecto, pero solo conozca los criterios en lugar del nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="54adc-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="54adc-136">Complete los siguientes pasos para utilizar el asistente de programación para encontrar un recurso en función de los atributos disponibles del recurso.</span><span class="sxs-lookup"><span data-stu-id="54adc-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="54adc-137">Navegue hasta el proyecto y seleccione **Reservar** para abrir el Asistente de programación.</span><span class="sxs-lookup"><span data-stu-id="54adc-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="54adc-138">Usando los filtros del lado izquierdo del Asistente de programación, reduzca los criterios y seleccione **Buscar.**</span><span class="sxs-lookup"><span data-stu-id="54adc-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="54adc-139">Según los recursos devueltos en los resultados, puede reservar un recurso.</span><span class="sxs-lookup"><span data-stu-id="54adc-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="54adc-140">Este método no crea ninguna reserva para el recurso.</span><span class="sxs-lookup"><span data-stu-id="54adc-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="54adc-141">En su lugar, agrega el recurso al equipo.</span><span class="sxs-lookup"><span data-stu-id="54adc-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="54adc-142">Una vez que el miembro del equipo se ha agregado al proyecto, el administrador del proyecto puede usar el mantenimiento de reservas o la extensión de reservas para agregar las reservas necesarias al recurso.</span><span class="sxs-lookup"><span data-stu-id="54adc-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
