---
title: Requisitos de reservas automáticas
description: En este tema se ofrece información sobre cómo cumplir los requisitos de reservas automáticas.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085358"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="67b5c-103">Requisitos de reservas automáticas</span><span class="sxs-lookup"><span data-stu-id="67b5c-103">Soft-book requirements</span></span>

<span data-ttu-id="67b5c-104">Se puede realizar una reserva manual de un requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="67b5c-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="67b5c-105">Una reserva manual crea una propuesta que consume la capacidad de un recurso.</span><span class="sxs-lookup"><span data-stu-id="67b5c-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="67b5c-106">La propuesta se envía después al solicitante para su aprobación.</span><span class="sxs-lookup"><span data-stu-id="67b5c-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="67b5c-107">Una reserva automática agrega provisionalmente un recurso a un equipo del proyecto y tiene un estado diferente en el tablero de programación, pero no consume la capacidad del recurso.</span><span class="sxs-lookup"><span data-stu-id="67b5c-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="67b5c-108">Para realizar una reserva automática de un recurso desde el tablero de programación, establezca el campo **Estado de reserva** en **Automática**.</span><span class="sxs-lookup"><span data-stu-id="67b5c-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Estado de reserva establecido en Automática](media/Resource-Management-image77.png)

<span data-ttu-id="67b5c-110">Cuando la pestaña **Equipo** está en la vista **Miembros del equipo con nombre** , aparece el recurso.</span><span class="sxs-lookup"><span data-stu-id="67b5c-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="67b5c-111">Las horas de reserva automática se notifican en la columna **Horas reservadas automáticamente**.</span><span class="sxs-lookup"><span data-stu-id="67b5c-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Horas reservadas automáticamente en la vista Miembros del equipo con nombre](media/Resource-Management-image78.png)

<span data-ttu-id="67b5c-113">Los miembros del equipo reservados automáticamente no se pueden asignar a tareas.</span><span class="sxs-lookup"><span data-stu-id="67b5c-113">Soft-booked team members can be assigned to tasks.</span></span>

![Miembro del equipo reservado automáticamente asignado a una tarea](media/Resource-Management-image79.png)

<span data-ttu-id="67b5c-115">En la pestaña **Conciliación** no se muestran reservas para un recurso de reserva manual, ya que la pestaña **Conciliación** solo tiene en cuenta las reservas manuales.</span><span class="sxs-lookup"><span data-stu-id="67b5c-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Recursos de reserva automática sin reservas en la pestaña Conciliación](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="67b5c-117">No puede realizar una reserva automática de un recurso desde un requisito generado por un miembro del equipo genérico.</span><span class="sxs-lookup"><span data-stu-id="67b5c-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="67b5c-118">En el tablero de programación, se utiliza un color diferente para las reservas automáticas de un recurso.</span><span class="sxs-lookup"><span data-stu-id="67b5c-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Reservas automáticas en el tablero de programación](media/Resource-Management-image81.png)

<span data-ttu-id="67b5c-120">Para convertir una reserva automática en una manual, en el tablero de programación, haga clic con el botón secundario en la reserva automática y, a continuación, seleccione **Cambiar estado** \> **Reserva manual** \> **Manual**.</span><span class="sxs-lookup"><span data-stu-id="67b5c-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Cambio del estado de la reservar a Manual](media/Resource-Management-image82.png)

<span data-ttu-id="67b5c-122">Se modifica la reserva y se cambia el estado en el tablero de programación.</span><span class="sxs-lookup"><span data-stu-id="67b5c-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="67b5c-123">Como el estado de la reserva ahora es **Manual** , el recurso se muestra como reservado y se ajusta la capacidad y la disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="67b5c-123">Because the booking status is now **Hard** , the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="67b5c-124">Puede usar el mismo método para cancelar una reserva manual o una reserva automática desde el tablero de programación.</span><span class="sxs-lookup"><span data-stu-id="67b5c-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="67b5c-125">Para convertir un recurso reservado automáticamente en la pestaña **Equipo** , seleccione el recurso y, a continuación, seleccione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="67b5c-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Confirmación del comando](media/Resource-Management-image83.png)
