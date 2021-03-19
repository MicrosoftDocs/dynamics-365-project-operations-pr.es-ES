---
title: Cumplimiento del requisito de recursos genéricos
description: En este tema se proporciona información cómo reservar recursos con nombre para un requisito de recurso genérico.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279609"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="b0e38-103">Cumplimiento del requisito de recursos genéricos</span><span class="sxs-lookup"><span data-stu-id="b0e38-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="b0e38-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="b0e38-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b0e38-105">Puede para reservar un recurso con nombre para reemplazar el recurso genérico que tiene un requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0e38-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="b0e38-106">En la página **Proyectos**, seleccione la pestaña **Equipo**.</span><span class="sxs-lookup"><span data-stu-id="b0e38-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="b0e38-107">Seleccione el recurso genérico que tiene algún requisito de recursos de la lista y después seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="b0e38-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="b0e38-108">O bien, abra el requisito del recurso y después haga clic en **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="b0e38-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="b0e38-109">En la página **Asistente de programación**, seleccione el recurso con nombre que desee reservar para su equipo de proyecto y después seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="b0e38-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="b0e38-110">Cuando se completa la reserva y se cumple con un recurso con nombre, el recurso genérico se reemplaza por el recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="b0e38-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="b0e38-111">Las asignaciones de la programación también se actualizan con el recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="b0e38-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="b0e38-112">Cumplir un recurso genérico con varios recursos con nombre</span><span class="sxs-lookup"><span data-stu-id="b0e38-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="b0e38-113">Cumplir un requisito de recurso genérico con varios recursos con nombre es similar a asignar un único recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="b0e38-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="b0e38-114">Por ejemplo, supongamos que hay una tarea con una duración de cinco días y 120 horas de esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="b0e38-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="b0e38-115">Esta tarea no la puede completar un recurso que trabaje durante una jornada normal de ocho horas y cinco días a la semana.</span><span class="sxs-lookup"><span data-stu-id="b0e38-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="b0e38-116">El requisito es de 120 horas de ingeniería robótica durante cinco días, lo que equivale a 24 horas al día.</span><span class="sxs-lookup"><span data-stu-id="b0e38-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="b0e38-117">Este es un ejemplo de situación en la que se necesitan varios recursos con nombre para cumplir una solicitud de recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="b0e38-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="b0e38-118">Deberá para reservar varios recursos para cumplir el requisito.</span><span class="sxs-lookup"><span data-stu-id="b0e38-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="b0e38-119">La diferencia principal en este escenario es que el recurso genérico permanece en el equipo asignado a la tarea y los miembros del equipo de recursos con nombre reservados no se asignan como parte de la posición.</span><span class="sxs-lookup"><span data-stu-id="b0e38-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="b0e38-120">El jefe del proyecto puede asignar el trabajo según sea necesario a los recursos con nombre.</span><span class="sxs-lookup"><span data-stu-id="b0e38-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="b0e38-121">La vista **Conciliación** puede ayudar a un jefe de proyecto a dividir las reservas de distintos recursos en asignaciones de tarea.</span><span class="sxs-lookup"><span data-stu-id="b0e38-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="b0e38-122">Esto no se realiza automáticamente porque en escenarios más complejos que el descrito anteriormente, como, por ejemplo, cuando el requisito se compone de una agrupación de tareas o el sistema tiene que suponer la intención con la que el jefe de proyecto desea realizar la asignación.</span><span class="sxs-lookup"><span data-stu-id="b0e38-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="b0e38-123">Debido a que el sistema no puede entender la intención, es probable que las suposiciones sean diferentes de lo previsto y se producirá un resultado incorrecto o impredecible.</span><span class="sxs-lookup"><span data-stu-id="b0e38-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="b0e38-124">El resultado previsible es que el recurso genérico permanecerá asignado hasta que el jefe de proyecto cree asignaciones de manera intencionada con la ayuda de la vista **Conciliación**.</span><span class="sxs-lookup"><span data-stu-id="b0e38-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]