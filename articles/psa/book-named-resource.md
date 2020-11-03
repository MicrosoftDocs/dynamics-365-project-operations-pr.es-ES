---
title: Reservar recursos con nombre desde los requisitos de recursos
description: En este tema se proporciona información sobre la reserva de recursos con nombre para un requisito de recurso genérico.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085353"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="03c3d-103">Reservar recursos con nombre desde los requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="03c3d-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="03c3d-104">Puede para reservar un recurso con nombre para reemplazar el recurso genérico que tiene un requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="03c3d-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="03c3d-105">En Project Service Automation (PSA), en la página **Proyectos** , haga clic en la pestaña **Equipo**.</span><span class="sxs-lookup"><span data-stu-id="03c3d-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="03c3d-106">Seleccione el recurso genérico que tiene algún requisito de recursos de la lista y después haga clic en **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="03c3d-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="03c3d-107">O bien, abra el requisito del recurso y después haga clic en **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="03c3d-107">Or, open the resource requirement and then click **Book**.</span></span>


![Reserva de un miembro del equipo genérico](media/RM-how-to-14.png)


3. <span data-ttu-id="03c3d-109">En la página **Asistente de programación** , seleccione el recurso con nombre que desee reservar para su equipo de proyecto y después haga clic en **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="03c3d-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Reserva de un miembro de equipo genérico con el asistente de programación](media/RM-how-to-15.png)

<span data-ttu-id="03c3d-111">Cuando se completa la reserva y se cumple con un recurso con nombre, el recurso genérico se reemplaza por el recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="03c3d-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Miembro del equipo con nombre que reemplaza a un miembro del equipo genérico.](media/RM-how-to-16.png)

<span data-ttu-id="03c3d-113">Las asignaciones de la programación también se actualizan con el recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="03c3d-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Miembro del equipo con nombre asignado a las tareas del proyecto.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="03c3d-115">Cumplir un recurso genérico con varios recursos con nombre</span><span class="sxs-lookup"><span data-stu-id="03c3d-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="03c3d-116">Cumplir un requisito de recurso genérico con varios recursos con nombre es similar a asignar un único recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="03c3d-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="03c3d-117">Por ejemplo, supongamos que hay una tarea con una duración de cinco días y 120 horas de esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="03c3d-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="03c3d-118">Esta tarea no la puede completar un recurso que trabaje durante una jornada normal de ocho horas y cinco días a la semana.</span><span class="sxs-lookup"><span data-stu-id="03c3d-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Tarea que necesita 120 horas de esfuerzo durante cinco días.](media/RM-how-to-21.png)

<span data-ttu-id="03c3d-120">El requisito es de 120 horas de ingeniería robótica durante cinco días, lo que equivale a 24 horas al día.</span><span class="sxs-lookup"><span data-stu-id="03c3d-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Requisito por día](media/RM-how-to-22.png)

<span data-ttu-id="03c3d-122">Este es un ejemplo de situación en la que se necesitan varios recursos con nombre para cumplir una solicitud de recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="03c3d-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="03c3d-123">Deberá para reservar varios recursos para cumplir el requisito.</span><span class="sxs-lookup"><span data-stu-id="03c3d-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Reserva de varios recursos para cumplir el requisito](media/RM-how-to-23.png)

<span data-ttu-id="03c3d-125">La diferencia principal en este escenario es que el recurso genérico permanece en el equipo asignado a la tarea y los miembros del equipo de recursos con nombre reservados no se asignan como parte de la posición.</span><span class="sxs-lookup"><span data-stu-id="03c3d-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="03c3d-126">El jefe del proyecto puede asignar el trabajo según sea necesario a los recursos con nombre.</span><span class="sxs-lookup"><span data-stu-id="03c3d-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="03c3d-127">La vista **Conciliación** puede ayudar a un jefe de proyecto a dividir las reservas de distintos recursos en asignaciones de tarea.</span><span class="sxs-lookup"><span data-stu-id="03c3d-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="03c3d-128">Esto no se realiza automáticamente porque en escenarios más complejos que el descrito anteriormente, como, por ejemplo, cuando el requisito se compone de una agrupación de tareas, el sistema tiene que suponer la intención con la que el jefe de proyecto desea realizar la asignación.</span><span class="sxs-lookup"><span data-stu-id="03c3d-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="03c3d-129">Dado que el sistema no puede comprender la intención, es posible que las suposiciones sean distintas de las reales y que, por lo tanto, se obtenga un resultado incorrecto o imprevisible.</span><span class="sxs-lookup"><span data-stu-id="03c3d-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="03c3d-130">El resultado previsible es que el recurso genérico permanecerá asignado hasta que el jefe de proyecto cree asignaciones de manera intencionada con la ayuda de la vista **Conciliación**.</span><span class="sxs-lookup"><span data-stu-id="03c3d-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


