---
title: Progreso y costes del proyecto
description: En este tema se proporciona información sobre cómo realizar un seguimiento del progreso y los costes del proyecto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756064"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="bc4a3-103">Progreso y costes del proyecto</span><span class="sxs-lookup"><span data-stu-id="bc4a3-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bc4a3-104">La necesidad de realizar un seguimiento del progreso de acuerdo con una programación varía según el sector.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="bc4a3-105">Algunos sectores realizan un seguimiento de nivel granular, mientras que otros realizan uno de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="bc4a3-106">Este tema muestra cómo realizar una programación para cumplir con los requisitos de su organización.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="bc4a3-107">Vista de seguimiento del esfuerzo</span><span class="sxs-lookup"><span data-stu-id="bc4a3-107">Effort tracking view</span></span>

<span data-ttu-id="bc4a3-108">La vista **Seguimiento del esfuerzo** rastrea el progreso de las tareas en la programación.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="bc4a3-109">Compara las horas de esfuerzo reales que se han dedicado a una tarea con las horas de esfuerzo planificadas para esa tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="bc4a3-110">PSA utiliza las siguientes fórmulas para calcular las métricas de seguimiento:</span><span class="sxs-lookup"><span data-stu-id="bc4a3-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="bc4a3-111">Porcentaje de progreso = Esfuerzo real realizado hasta la fecha ÷ Esfuerzo planificado para la tarea</span><span class="sxs-lookup"><span data-stu-id="bc4a3-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="bc4a3-112">Estimación de finalización (ETC) = Esfuerzo planificado - Esfuerzo real realizado hasta la fecha</span><span class="sxs-lookup"><span data-stu-id="bc4a3-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="bc4a3-113">Estimación al finalizar (EAF) = Esfuerzo restante + Esfuerzo real realizado hasta la fecha</span><span class="sxs-lookup"><span data-stu-id="bc4a3-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="bc4a3-114">Variación del esfuerzo proyectado = Esfuerzo planificado - EAF</span><span class="sxs-lookup"><span data-stu-id="bc4a3-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="bc4a3-115">PSA muestra una proyección de la variación del esfuerzo en la tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="bc4a3-116">Si el EAF es superior al esfuerzo planificado, se prevé que la tarea tardará más tiempo del planificado originalmente.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="bc4a3-117">Por lo tanto, se llevará a cabo después de lo programado.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="bc4a3-118">Si el EAF es inferior al esfuerzo planificado, se prevé que la tarea tardará menos tiempo del planificado originalmente.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="bc4a3-119">Por lo tanto, se llevará a cabo antes de lo programado.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="bc4a3-120">Reproyección de esfuerzo</span><span class="sxs-lookup"><span data-stu-id="bc4a3-120">Re-projecting effort</span></span>

<span data-ttu-id="bc4a3-121">Es frecuente que un administrador de proyecto revise las estimaciones originales de una tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="bc4a3-122">Las reproyecciones de proyectos son la percepción de las estimaciones de un administrador de proyecto según estado actual de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="bc4a3-123">Sin embargo, no recomendamos que los jefes de proyecto cambien los números de línea de base, ya que la línea de base del proyecto representa la fuente de verdad establecida para la programación y la estimación de costes del proyecto, y todos los interesados en el proyecto la han aceptado.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="bc4a3-124">Existen dos formas en las que un jefe de proyecto puede reproyectar el esfuerzo en las tareas:</span><span class="sxs-lookup"><span data-stu-id="bc4a3-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="bc4a3-125">Anular el ETC predeterminado con una nueva estimación del esfuerzo restante real en la tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="bc4a3-126">Anular el porcentaje de progreso predeterminado con una nueva estimación del progreso real de la tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="bc4a3-127">Cada uno de estos enfoques genera un nuevo cálculo del ETC, EAF y porcentaje de progreso de la tarea, y la variación del esfuerzo proyectado en una tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="bc4a3-128">El EAF, ETC y el porcentaje de progreso en las tareas de resumen también se recalculan y producen una nueva proyección de la variación del esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="bc4a3-129">Reproyección de esfuerzo en tareas de resumen</span><span class="sxs-lookup"><span data-stu-id="bc4a3-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="bc4a3-130">El esfuerzo en tareas de resumen o tareas de contenedor se puede reproyectar.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="bc4a3-131">Independientemente de si el usuario efectúa la reproyección mediante el esfuerzo restante o el porcentaje de progreso en las tareas de resumen, se inicia el siguiente conjunto de cálculos:</span><span class="sxs-lookup"><span data-stu-id="bc4a3-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="bc4a3-132">Se calculan el EAF, el ETC y el porcentaje de progreso en la tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="bc4a3-133">El nuevo EAF se distribuye a las tareas secundarias en la misma proporción que el EAF original de la tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="bc4a3-134">Se calcula el nuevo EAF en cada una de las tareas individuales hasta las tareas del nodo hoja.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="bc4a3-135">Las tareas secundarias afectadas hasta los nodos hoja tienen su ETC y su porcentaje de progreso recalculado en función del valor de EAF.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="bc4a3-136">Esto da como resultado una nueva proyección para la variación de esfuerzo de la tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="bc4a3-137">Se vuelven a calcular los EAF de las tareas de resumen hasta el nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="bc4a3-138">Vista de seguimiento de costes</span><span class="sxs-lookup"><span data-stu-id="bc4a3-138">Cost tracking view</span></span> 

<span data-ttu-id="bc4a3-139">La vista **Seguimiento de costes** compara el coste real que se gastó en una tarea con el coste planificado en una tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="bc4a3-140">Esta vista muestra solo los costes laborales y no incluye los costes de las estimaciones de gastos.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="bc4a3-141">PSA utiliza las siguientes fórmulas para calcular las métricas de seguimiento:</span><span class="sxs-lookup"><span data-stu-id="bc4a3-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="bc4a3-142">Porcentaje del coste consumido = Coste real gastado hasta la fecha ÷ Coste planificado para la tarea</span><span class="sxs-lookup"><span data-stu-id="bc4a3-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="bc4a3-143">Coste de finalización (CTC) = Coste planificado - Coste real gastado hasta la fecha</span><span class="sxs-lookup"><span data-stu-id="bc4a3-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="bc4a3-144">EAF = CTC + Coste real gastado hasta la fecha</span><span class="sxs-lookup"><span data-stu-id="bc4a3-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="bc4a3-145">Variación del coste proyectado = coste planificado - EAF</span><span class="sxs-lookup"><span data-stu-id="bc4a3-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="bc4a3-146">Se muestra una proyección de la variación de coste en la tarea.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="bc4a3-147">Si el EAF es superior al coste planificado, se prevé que la tarea costará más de lo planificado originalmente.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="bc4a3-148">Por lo tanto, la tendencia es que se supere el presupuesto.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="bc4a3-149">Si el EAF es inferior al coste planificado, se prevé que la tarea costará menos de lo planificado originalmente.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="bc4a3-150">Por lo tanto, la tendencia es que no se supere el presupuesto.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="bc4a3-151">Reproyección del coste del jefe de proyecto</span><span class="sxs-lookup"><span data-stu-id="bc4a3-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="bc4a3-152">Cuando se reproyecta el esfuerzo, el CTC, el EAF, el porcentaje de coste consumido y la variación del coste proyectado se recalculan en la vista **Seguimiento de costes**.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="bc4a3-153">Resumen del estado del proyecto</span><span class="sxs-lookup"><span data-stu-id="bc4a3-153">Project status summary</span></span>

<span data-ttu-id="bc4a3-154">Los datos de seguimiento en las vistas **Seguimiento del esfuerzo** y **Seguimiento de costes** muestran el progreso y el consumo de costes en el nodo raíz del proyecto, las tareas de resumen y los niveles de tareas del nodo hoja.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="bc4a3-155">La sección **Estado** en la página **Entidad de proyecto** muestra un resumen del estado a nivel de proyecto.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="bc4a3-156">Campos de resumen de estado</span><span class="sxs-lookup"><span data-stu-id="bc4a3-156">Status summary fields</span></span>

<span data-ttu-id="bc4a3-157">El campo **Estado general del proyecto** es un campo editable que muestra el estado general del proyecto.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="bc4a3-158">Utiliza códigos de colores, como verde, amarillo y rojo, para indicar un riesgo creciente.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="bc4a3-159">El campo **Comentarios** permite al jefe de proyecto introducir comentarios específicos sobre el estado.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="bc4a3-160">El campo **Última actualización del estado el** no es editable y el valor es una marca de tiempo que indica cuándo se actualizó por última vez.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="bc4a3-161">Los campos **Rendimiento de programación** y **Rendimiento de coste** se establecen desde la fecha de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="bc4a3-162">Cuando la programación y la variación de costes para el nodo raíz en la vista **Seguimiento del esfuerzo** son positivas, puede establecer estos campos en **Adelantado**.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="bc4a3-163">Cuando la programación y la variación de coste para el nodo raíz sean negativas, puede establecerlas en **Retrasado**.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
