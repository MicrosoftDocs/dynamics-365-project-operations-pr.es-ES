---
title: Propuesta de recursos de proyecto
description: En este tema se proporciona información sobre cómo proponer recursos de proyecto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdb0dcb2-4421-4ee1-b97d-89a8cdefbd8d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3a7f7c15c3c7a3c39f2b7b9eeb88b9cf0cfdc220
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756084"
---
# <a name="propose-project-resources"></a><span data-ttu-id="abbc9-103">Propuesta de recursos de proyecto</span><span class="sxs-lookup"><span data-stu-id="abbc9-103">Propose project resources</span></span>

<span data-ttu-id="abbc9-104">Los administradores de recursos pueden proponer un recurso al administrador del proyecto mediante una solicitud de recurso.</span><span class="sxs-lookup"><span data-stu-id="abbc9-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="abbc9-105">Desde la cuadrícula de solicitud o la propia solicitud, seleccione **Buscar recursos**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="abbc9-106">En la página **Asistente de programación**, seleccione el recurso y, a continuación, en el panel **Crear reserva de recursos**, en el campo **Estado de reserva**, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Recurso propuesto seleccionado](media/Resource-Management-image62.png)

<span data-ttu-id="abbc9-108">Se producen las siguientes actualizaciones de estado:</span><span class="sxs-lookup"><span data-stu-id="abbc9-108">The following status updates occur:</span></span>

- <span data-ttu-id="abbc9-109">En la página **Asistente de programación**, los indicadores de estado se actualizan para indicar que la reserva se propone, no se reserva manualmente.</span><span class="sxs-lookup"><span data-stu-id="abbc9-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indicadores de estado de la reserva propuesta en la página Asistente de programación](media/Resource-Management-image63.png)

- <span data-ttu-id="abbc9-111">En la solicitud del recurso, el estado cambia a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Estado de la solicitud del recurso cambiada a Necesita revisión](media/Resource-Management-image64.png)

- <span data-ttu-id="abbc9-113">En la pestaña **Equipo** del proyecto, el valor de **Estado de la solicitud** del miembro del equipo genérico cambia a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Estado de la solicitud del miembro del equipo genérico cambiado a Necesita revisión en la pestaña Equipo](media/Resource-Management-image48.png)

<span data-ttu-id="abbc9-115">El jefe de proyecto puede aceptar o rechazar la propuesta.</span><span class="sxs-lookup"><span data-stu-id="abbc9-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="abbc9-116">Cuando los administradores de recursos procesan las solicitudes de recursos, pueden usar cualquiera de los siguientes enfoques:</span><span class="sxs-lookup"><span data-stu-id="abbc9-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="abbc9-117">Proponer varios recursos para satisfacer la petición si no hay un solo recurso disponible para cumplir con las horas necesarias.</span><span class="sxs-lookup"><span data-stu-id="abbc9-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="abbc9-118">Las horas propuestas se dividen entre varios recursos que pueden satisfacer las horas necesarias.</span><span class="sxs-lookup"><span data-stu-id="abbc9-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="abbc9-119">En este escenario, las horas no pueden superponerse.</span><span class="sxs-lookup"><span data-stu-id="abbc9-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="abbc9-120">Proponer menos recursos de los necesarios.</span><span class="sxs-lookup"><span data-stu-id="abbc9-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="abbc9-121">En este escenario, la capacidad de recursos propuesta es menor que las horas requeridas que especificó el solicitante.</span><span class="sxs-lookup"><span data-stu-id="abbc9-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="abbc9-122">Por lo tanto, cuando el solicitante acepta los recursos propuestos, se crea un requisito de recurso no cumplido para capturar la petición restante.</span><span class="sxs-lookup"><span data-stu-id="abbc9-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="abbc9-123">Reservar varios recursos para satisfacer la petición si no hay un solo recurso disponible para completar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="abbc9-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="abbc9-124">Reservar menos recursos de los necesarios.</span><span class="sxs-lookup"><span data-stu-id="abbc9-124">Book fewer resources than are required.</span></span> <span data-ttu-id="abbc9-125">En este escenario, las horas reservadas son menos que las horas necesarias.</span><span class="sxs-lookup"><span data-stu-id="abbc9-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="abbc9-126">El sistema le guía para proponer recursos en lugar de reservas, de modo que el solicitante pueda verificar y realizar un seguimiento de la petición restante.</span><span class="sxs-lookup"><span data-stu-id="abbc9-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="abbc9-127">Uso facturable</span><span class="sxs-lookup"><span data-stu-id="abbc9-127">Billable utilization</span></span>

<span data-ttu-id="abbc9-128">Los recursos pueden tener un uso facturable objetivo.</span><span class="sxs-lookup"><span data-stu-id="abbc9-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="abbc9-129">Este uso objetivo se define como un atributo en el rol predeterminado de un recurso o se establece en el registro del recurso individual que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="abbc9-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="abbc9-130">Los cálculos de uso se basan en las horas reales informadas por los recursos mediante entradas de tiempo aprobadas.</span><span class="sxs-lookup"><span data-stu-id="abbc9-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="abbc9-131">Se utilizan las siguientes fórmulas para calcular el uso:</span><span class="sxs-lookup"><span data-stu-id="abbc9-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="abbc9-132">Uso facturable = Horas reales imputables ÷ Capacidad de recursos</span><span class="sxs-lookup"><span data-stu-id="abbc9-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="abbc9-133">Uso no facturable = Tiempo real con Id. de tipo de facturación = No imputable, Complementario o No disponible ÷ Capacidad de recursos</span><span class="sxs-lookup"><span data-stu-id="abbc9-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="abbc9-134">Interno = Tiempo real sin contrato de venta ÷ Capacidad de recursos</span><span class="sxs-lookup"><span data-stu-id="abbc9-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="abbc9-135">Capacidad de recursos = Horas de trabajo de recursos - Fuera de la oficina - Días no laborables</span><span class="sxs-lookup"><span data-stu-id="abbc9-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="abbc9-136">Puede encontrar la vista **Uso de recursos** en el panel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Vista Uso de recursos](media/Resource-Management-image65.png)

<span data-ttu-id="abbc9-138">Cada celda de la cuadrícula representa el porcentaje de uso facturable del recurso en un período, como un día, una semana o un mes.</span><span class="sxs-lookup"><span data-stu-id="abbc9-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="abbc9-139">Se usan las siguientes fórmulas para colorear las celdas:</span><span class="sxs-lookup"><span data-stu-id="abbc9-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="abbc9-140">**Verde:** Uso facturable \>= Uso objetivo del recurso</span><span class="sxs-lookup"><span data-stu-id="abbc9-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="abbc9-141">**Amarillo:** Uso objetivo – 20 \<= Uso facturable \< Uso objetivo</span><span class="sxs-lookup"><span data-stu-id="abbc9-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="abbc9-142">**Rojo:** Uso facturable \< Uso objetivo – 20</span><span class="sxs-lookup"><span data-stu-id="abbc9-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="abbc9-143">Puesto que la vista **Uso de recursos** se basa en el tablero de programación, puede usar las capacidades de filtrado del tablero de programación para filtrar sus resultados.</span><span class="sxs-lookup"><span data-stu-id="abbc9-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="abbc9-144">La cuadrícula requiere que establezca un uso objetivo en el rol o en el recurso individual.</span><span class="sxs-lookup"><span data-stu-id="abbc9-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="abbc9-145">Para realizar esta configuración, vaya a **Recursos** \> **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="abbc9-146">Además, se debe asignar un rol predeterminado a cada recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="abbc9-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="abbc9-147">Vaya a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="abbc9-148">En la pestaña **Project Service**, verifique que se haya definido un rol de recurso y que el campo **Es predeterminado** esté establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="abbc9-149">Puede agregar roles adicionales en los que **Es predeterminado = No**.</span><span class="sxs-lookup"><span data-stu-id="abbc9-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="abbc9-150">El rol en el que **Es predeterminado = Sí** se usa para evaluar el uso del recurso en relación el objetivo para ese rol.</span><span class="sxs-lookup"><span data-stu-id="abbc9-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Rol predeterminado establecido](media/Resource-Management-image67.png)

<span data-ttu-id="abbc9-152">En la pestaña **Project Service** también puede establecer un uso objetivo individual para el recurso.</span><span class="sxs-lookup"><span data-stu-id="abbc9-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="abbc9-153">El cálculo de uso utiliza después ese uso objetivo para evaluar el objetivo del recurso en lugar del objetivo del rol predeterminado del recurso.</span><span class="sxs-lookup"><span data-stu-id="abbc9-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="abbc9-154">El uso se muestra para un recurso solo si ese recurso ha aprobado el tiempo imputable durante el período que se muestra en la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="abbc9-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="abbc9-155">Disponibilidad de recursos</span><span class="sxs-lookup"><span data-stu-id="abbc9-155">Resource availability</span></span>

<span data-ttu-id="abbc9-156">Es fundamental que los administradores de recursos puedan ver la disponibilidad de recursos y actualizar las reservas.</span><span class="sxs-lookup"><span data-stu-id="abbc9-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="abbc9-157">En algunos casos, no existe una petición formal (solicitud de recursos), pero un administrador de recursos debe responder a una petición no planificada que llegue a través de canales como un correo electrónico, una llamada telefónica o un mensaje instantáneo.</span><span class="sxs-lookup"><span data-stu-id="abbc9-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="abbc9-158">Los administradores de recursos usan el tablero de programación para actualizar recursos y reservas.</span><span class="sxs-lookup"><span data-stu-id="abbc9-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="abbc9-159">Las horas de trabajo de los recursos se utilizan como base para calcular la disponibilidad de un recurso.</span><span class="sxs-lookup"><span data-stu-id="abbc9-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="abbc9-160">Las reservas de recursos consumen la capacidad de los recursos.</span><span class="sxs-lookup"><span data-stu-id="abbc9-160">Resource bookings consume the capacity of the resources.</span></span>

![Tablero de programación](media/Resource-Management-image68.png)

<span data-ttu-id="abbc9-162">El tablero de programación utiliza colores y sombras para mostrar las reservas, la disponibilidad y las reservas excesivas, y también el estado de las reservas.</span><span class="sxs-lookup"><span data-stu-id="abbc9-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="abbc9-163">Una configuración en la configuración del tablero de programación le permite mostrar una leyenda.</span><span class="sxs-lookup"><span data-stu-id="abbc9-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="abbc9-164">Si aparece una flecha que apunta hacia la derecha al lado de un recurso individual que se puede reservar en el tablero de programación, el recurso se puede expandir para mostrar detalles del trabajo en el que se reserva el recurso.</span><span class="sxs-lookup"><span data-stu-id="abbc9-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Recurso que se puede reservar expandido en el tablero de programación](media/Resource-Management-image69.png)

<span data-ttu-id="abbc9-166">Puesto que Dynamics 365 Project Service Automation utiliza el motor Universal Resource Scheduling, si ya dispone de Dynamics 365 Field Service instalado, puede ver los detalles de las reservas de recursos para proyectos, órdenes de trabajo y cualquier otra entidad a la que haya extendido la programación.</span><span class="sxs-lookup"><span data-stu-id="abbc9-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Detalles de las reservas de recursos para proyectos y órdenes de trabajo](media/Resource-Management-image70.png)

<span data-ttu-id="abbc9-168">Para ver más detalles sobre un recurso individual, haga clic con el botón secundario en él para abrir la tarjeta de recursos.</span><span class="sxs-lookup"><span data-stu-id="abbc9-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Tarjeta de recursos](media/Resource-Management-image71.png)
