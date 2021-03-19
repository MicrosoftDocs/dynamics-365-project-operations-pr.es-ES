---
title: Revisar recursos propuestos
description: En este tema se proporciona información sobre cómo proponer recursos de proyecto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279294"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="ac572-103">Revisar recursos propuestos</span><span class="sxs-lookup"><span data-stu-id="ac572-103">Review proposed resources</span></span>

<span data-ttu-id="ac572-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="ac572-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ac572-105">Los administradores de recursos pueden proponer un recurso al administrador del proyecto mediante una solicitud de recurso.</span><span class="sxs-lookup"><span data-stu-id="ac572-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="ac572-106">Desde la cuadrícula de solicitud o la propia solicitud, seleccione **Buscar recursos**.</span><span class="sxs-lookup"><span data-stu-id="ac572-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="ac572-107">En la página **Asistente de programación**, seleccione el recurso y, a continuación, en el panel **Crear reserva de recursos**, en el campo **Estado de reserva**, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="ac572-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="ac572-108">Se producen las siguientes actualizaciones de estado:</span><span class="sxs-lookup"><span data-stu-id="ac572-108">The following status updates occur:</span></span>

- <span data-ttu-id="ac572-109">En la página **Asistente de programación**, los indicadores de estado se actualizan para indicar que la reserva se propone, no se reserva manualmente.</span><span class="sxs-lookup"><span data-stu-id="ac572-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="ac572-110">En la solicitud del recurso, el estado cambia a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="ac572-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="ac572-111">En la pestaña **Equipo** del proyecto, el valor de **Estado de la solicitud** del miembro del equipo genérico cambia a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="ac572-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="ac572-112">El jefe de proyecto puede aceptar o rechazar la propuesta.</span><span class="sxs-lookup"><span data-stu-id="ac572-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="ac572-113">Cuando los administradores de recursos procesan las solicitudes de recursos, pueden usar cualquiera de los siguientes enfoques:</span><span class="sxs-lookup"><span data-stu-id="ac572-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="ac572-114">Proponer múltiples recursos para satisfacer la demanda si no hay un solo recurso disponible para cubrir las horas requeridas.</span><span class="sxs-lookup"><span data-stu-id="ac572-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="ac572-115">Las horas propuestas se dividen entre varios recursos que pueden satisfacer las horas necesarias.</span><span class="sxs-lookup"><span data-stu-id="ac572-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="ac572-116">En este escenario, las horas no pueden superponerse.</span><span class="sxs-lookup"><span data-stu-id="ac572-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="ac572-117">Proponer menos recursos de los necesarios.</span><span class="sxs-lookup"><span data-stu-id="ac572-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="ac572-118">En este escenario, la capacidad de recursos propuesta es menor que las horas requeridas que especificó el solicitante.</span><span class="sxs-lookup"><span data-stu-id="ac572-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="ac572-119">Por lo tanto, cuando el solicitante acepta los recursos propuestos, se crea un requisito de recursos sin cumplir para capturar la demanda restante.</span><span class="sxs-lookup"><span data-stu-id="ac572-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="ac572-120">Reservar múltiples recursos para satisfacer la demanda si no hay un solo recurso disponible para completar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ac572-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="ac572-121">Reservar menos recursos de los necesarios.</span><span class="sxs-lookup"><span data-stu-id="ac572-121">Book fewer resources than are required.</span></span> <span data-ttu-id="ac572-122">En este escenario, las horas reservadas son menos que las necesarias.</span><span class="sxs-lookup"><span data-stu-id="ac572-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="ac572-123">El sistema le guía para proponer recursos en lugar de reservas, de modo que el solicitante pueda verificar y realizar un seguimiento de la petición restante.</span><span class="sxs-lookup"><span data-stu-id="ac572-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="ac572-124">Disponibilidad de recursos</span><span class="sxs-lookup"><span data-stu-id="ac572-124">Resource availability</span></span>

<span data-ttu-id="ac572-125">Es fundamental que los administradores de recursos puedan ver la disponibilidad de recursos y actualizar las reservas.</span><span class="sxs-lookup"><span data-stu-id="ac572-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="ac572-126">En algunos casos, no existe una petición formal (solicitud de recursos), pero un administrador de recursos debe responder a una petición no planificada que llegue a través de canales como un correo electrónico, una llamada telefónica o un mensaje instantáneo.</span><span class="sxs-lookup"><span data-stu-id="ac572-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="ac572-127">Los administradores de recursos usan el tablero de programación para actualizar recursos y reservas.</span><span class="sxs-lookup"><span data-stu-id="ac572-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="ac572-128">Las horas de trabajo de los recursos se utilizan como base para calcular la disponibilidad de un recurso.</span><span class="sxs-lookup"><span data-stu-id="ac572-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="ac572-129">Las reservas de recursos consumen la capacidad de los recursos.</span><span class="sxs-lookup"><span data-stu-id="ac572-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="ac572-130">El tablero de programación utiliza colores y sombras para mostrar las reservas, la disponibilidad y las reservas excesivas, y también el estado de las reservas.</span><span class="sxs-lookup"><span data-stu-id="ac572-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="ac572-131">Una configuración en la configuración del tablero de programación le permite mostrar una leyenda.</span><span class="sxs-lookup"><span data-stu-id="ac572-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="ac572-132">Si aparece una flecha que apunta hacia la derecha al lado de un recurso individual que se puede reservar en el tablero de programación, el recurso se puede expandir para mostrar detalles del trabajo en el que se reserva el recurso.</span><span class="sxs-lookup"><span data-stu-id="ac572-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="ac572-133">Puesto que Dynamics 365 Project Operations utiliza el motor Universal Resource Scheduling, si ya dispone de Dynamics 365 Field Service instalado, puede ver los detalles de las reservas de recursos para proyectos, órdenes de trabajo y cualquier otra entidad a la que haya extendido la programación.</span><span class="sxs-lookup"><span data-stu-id="ac572-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="ac572-134">Para ver más detalles sobre un recurso individual, haga clic con el botón secundario en él para abrir la tarjeta de recursos.</span><span class="sxs-lookup"><span data-stu-id="ac572-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]