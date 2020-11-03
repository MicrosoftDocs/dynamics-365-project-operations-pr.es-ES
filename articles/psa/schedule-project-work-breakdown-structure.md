---
title: Programar un proyecto con una estructura de descomposición del trabajo
description: Cómo programar un proyecto con una estructura de descomposición del trabajo en Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085330"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="1cf3f-103">Programe un proyecto con una estructura de descomposición del trabajo (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1cf3f-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1cf3f-104">Una programación del proyecto comunica el trabajo debe realizarse, qué recursos realizarán el trabajo, y el calendario en el que debe completarse ese trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="1cf3f-105">La programación del proyecto refleja todo el trabajo asociado con la entrega del proyecto a tiempo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="1cf3f-106">Uno de los primeros pasos en la fase de inicio del proyecto es elaborar una programación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="1cf3f-107">Para establecer una programación del proyecto, necesita crear una estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="1cf3f-108">Cree una estructura del proyecto con una estructura de descomposición del trabajo, lo que le ayuda a:</span><span class="sxs-lookup"><span data-stu-id="1cf3f-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="1cf3f-109">Desglosar el trabajo en tareas manejables</span><span class="sxs-lookup"><span data-stu-id="1cf3f-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="1cf3f-110">Estimar el tiempo necesario para completar una tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="1cf3f-111">Establecer dependencias y duración de tareas</span><span class="sxs-lookup"><span data-stu-id="1cf3f-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="1cf3f-112">Determinar los roles necesarios para realizar cada tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="1cf3f-113">La programación del proyecto en la estructura de descomposición del trabajo tiene una apariencia familiar e incluye un gráfico de Gantt interactivo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="1cf3f-114">Cree una estructura de descomposición del trabajo para un proyecto</span><span class="sxs-lookup"><span data-stu-id="1cf3f-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="1cf3f-115">Cree una estructura de descomposición del trabajo para representar la secuencia de tareas en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="1cf3f-116">La estructura de descomposición del trabajo incluye tareas, requisitos para cada tarea, y la información de los ingresos y costos.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="1cf3f-117">En la estructura de descomposición del trabajo, puede agregar:</span><span class="sxs-lookup"><span data-stu-id="1cf3f-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="1cf3f-118">La secuencia de tareas en una jerarquía</span><span class="sxs-lookup"><span data-stu-id="1cf3f-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="1cf3f-119">Otras tareas, en su caso, que deben completarse antes de que se pueda iniciar una tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="1cf3f-120">La fecha inicial, la fecha de finalización, y la duración de una tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="1cf3f-121">El número de horas necesarias para una tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="1cf3f-122">Las cualificaciones y educación necesarias de un trabajador</span><span class="sxs-lookup"><span data-stu-id="1cf3f-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="1cf3f-123">Los trabajadores que están asignados a una tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="1cf3f-124">Ingresos y costes estimados</span><span class="sxs-lookup"><span data-stu-id="1cf3f-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="1cf3f-125">Tipos de tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-125">Task types</span></span>  
<span data-ttu-id="1cf3f-126">Usará los siguientes tipos de tareas al crear la estructura de descomposición del trabajo:</span><span class="sxs-lookup"><span data-stu-id="1cf3f-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="1cf3f-127">**Nodo raíz del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-127">**Project root node**</span></span> | <span data-ttu-id="1cf3f-128">La tarea de resumen de nivel superior del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-128">The top-level summary task for the project.</span></span> <span data-ttu-id="1cf3f-129">El resto de las tareas del proyecto se crean por debajo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-129">All other project tasks are created under it.</span></span> <span data-ttu-id="1cf3f-130">El nombre de la tarea raíz es el nombre del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-130">The name of the root task is the project name.</span></span> <span data-ttu-id="1cf3f-131">El esfuerzo, fechas, y la duración del nodo raíz se basan en los valores de la jerarquía por debajo de él.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="1cf3f-132">No puede editar propiedades del nodo raíz ni eliminar el nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="1cf3f-133">**Tareas de informe o contenedor**</span><span class="sxs-lookup"><span data-stu-id="1cf3f-133">**Summary or container tasks**</span></span> | <span data-ttu-id="1cf3f-134">Una tarea de resumen es una tarea que tiene subtareas por debajo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="1cf3f-135">Una tarea de resumen no tiene ningún esfuerzo de trabajo ni coste propio.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="1cf3f-136">Su esfuerzo y costo de trabajo son un resumen de sus subtareas.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="1cf3f-137">Puede cambiar el nombre de una tarea de resumen, pero no puede cambiar el esfuerzo, las fechas o la duración porque se calculan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="1cf3f-138">La eliminación de una tarea de resumen elimina la tarea y todas sus subtareas.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="1cf3f-139">**Tareas del nodo hoja**</span><span class="sxs-lookup"><span data-stu-id="1cf3f-139">**Leaf node tasks**</span></span> | <span data-ttu-id="1cf3f-140">Una tarea del nodo hoja representa el trabajo más detallado en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="1cf3f-141">Tiene un esfuerzo estimado, un número previsto de recursos, fechas de inicio y finalización planeadas, y una duración.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="1cf3f-142">Jerarquía de tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-142">Task hierarchy</span></span>  
 <span data-ttu-id="1cf3f-143">Tiene las siguientes opciones cuando cree una jerarquía de tareas:</span><span class="sxs-lookup"><span data-stu-id="1cf3f-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="1cf3f-144">**Agregar tarea**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-144">**Add task**.</span></span>   <span data-ttu-id="1cf3f-145">Puede agregar una tarea en una posición que elija en la jerarquía de tareas.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="1cf3f-146">Si no selecciona una posición, la nueva tarea aparece al final.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="1cf3f-147">**Aplicar sangría a tarea**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-147">**Indent task**.</span></span>   <span data-ttu-id="1cf3f-148">Aplique sangría una tarea para convertirla en secundaria de la tarea directamente por encima de ella.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="1cf3f-149">**Anular sangría de tarea**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-149">**Outdent task**.</span></span>   <span data-ttu-id="1cf3f-150">Anule la sangría de una tarea para que deje de ser una subtarea de su tarea principal original.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="1cf3f-151">**Subir y bajar**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-151">**Move up and Move down**.</span></span>   <span data-ttu-id="1cf3f-152">Suba y baja tareas en la jerarquía de su tarea primaria.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="1cf3f-153">Subir o bajar una tarea no tiene ningún efecto en su esfuerzo, costo, fechas, o duración.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="1cf3f-154">Atributos de tareas</span><span class="sxs-lookup"><span data-stu-id="1cf3f-154">Task attributes</span></span>  
 <span data-ttu-id="1cf3f-155">Un nombre de tarea describe el trabajo que debe completarse.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="1cf3f-156">Use diferentes atributos de tarea para describir la programación y los requisitos de personal para la tarea.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="1cf3f-157">Atributos de programación</span><span class="sxs-lookup"><span data-stu-id="1cf3f-157">Schedule attributes</span></span>

 - <span data-ttu-id="1cf3f-158">Asigne valores a **Horas de esfuerzo** , **Número de recursos** , **Fecha de inicio** , **Fecha de finalización** , **Duración** para determinar la programación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-158">Assign values to **Effort hours** , **Number of resources** , **Start date** , **End date** , and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="1cf3f-159">**Esfuerzo** es una estimación de las horas que se tarda en llevar a cabo la tarea.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="1cf3f-160">**Número de recursos** es cálculo que el jefe del proyecto incluye en la tarea para ayudar a elaborar la programación mejor posible.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="1cf3f-161">**Duración** (en días) indica el número de días laborables que se requiere para llevar a cabo la tarea.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="1cf3f-162">Atributos de personal</span><span class="sxs-lookup"><span data-stu-id="1cf3f-162">Staffing attributes</span></span>

 - <span data-ttu-id="1cf3f-163">**Rol** , **Unidad organizativa de recursos** , **Número de recursos** y **Recursos** describen los requisitos de personal para la tarea.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-163">**Role** , **Resource organizational unit** , **Number of resources** , and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="1cf3f-164">**Rol** describe el tipo de recurso necesario para llevar a cabo la tarea.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="1cf3f-165">**Unidad organizativa de recursos** indica la unidad organizativa de la que debe obtenerse de recursos de personal para esa tarea; esto también afecta a la estimación costes y ventas de la tarea, ya que se contabiliza al determinar el precio de venta unitario para el recurso.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="1cf3f-166">**Recursos** contiene un recurso genérico o un recurso con nombre cuando se encuentra uno.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="1cf3f-167">Dependencias de tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-167">Task dependencies</span></span>  
 <span data-ttu-id="1cf3f-168">Puede crear relaciones de predecesor entre una o varias tareas en la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="1cf3f-169">Puede establecer uno o varios valores del campo de predecesor en tareas para indicar las tareas de las que dependerá.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="1cf3f-170">Cuando asigna un valor de predecesora a una tarea, la tarea solo se puede iniciar cuando todas las tareas predecesoras se han completado.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="1cf3f-171">Establecer esta dependencia en una tarea producirá el recálculo de la fecha de inicio planeada de la tarea como el último final de todos sus predecesoras.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="1cf3f-172">Los impactos relacionados con las predecesoras en una programación no están limitados por el modo de tarea definido en la tarea.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="1cf3f-173">Modo de tarea</span><span class="sxs-lookup"><span data-stu-id="1cf3f-173">Task mode</span></span>  
 <span data-ttu-id="1cf3f-174">El modo de tarea es uno de los factores importantes que determinan las tareas del nodo hoja de programación.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="1cf3f-175">Hay dos modos de tarea para cada tarea: modo de programación automática y modo de programación manual.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="1cf3f-176">**Programación automática**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-176">**Auto scheduling**.</span></span>   <span data-ttu-id="1cf3f-177">Cuando se establece el modo de tarea en Programado automáticamente, el motor de programación de tareas usa las reglas de programación en los siguientes atributos de tarea para determinar la programación de la tarea:</span><span class="sxs-lookup"><span data-stu-id="1cf3f-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="1cf3f-178">Predecesoras</span><span class="sxs-lookup"><span data-stu-id="1cf3f-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="1cf3f-179">Esfuerzo</span><span class="sxs-lookup"><span data-stu-id="1cf3f-179">Effort</span></span>  
  
    -   <span data-ttu-id="1cf3f-180">Número de recursos</span><span class="sxs-lookup"><span data-stu-id="1cf3f-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="1cf3f-181">Fechas de inicio y finalización</span><span class="sxs-lookup"><span data-stu-id="1cf3f-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="1cf3f-182">**Reglas de programación**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-182">**Scheduling rules**.</span></span>   <span data-ttu-id="1cf3f-183">La fecha de inicio de una tarea del nodo hoja que no tiene valores predecesores utiliza de manera predeterminada la fecha de inicio de programación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="1cf3f-184">La duración de una tarea del nodo hoja se calcula siempre como el número de días laborables entre sus fechas de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="1cf3f-185">Cuando una tarea se programa automáticamente, el motor de programación sigue estas reglas:</span><span class="sxs-lookup"><span data-stu-id="1cf3f-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="1cf3f-186">Las fechas de inicio y finalización de una tarea deben siempre ser días laborables según el calendario de programación del proyecto</span><span class="sxs-lookup"><span data-stu-id="1cf3f-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="1cf3f-187">La fecha de inicio de una tarea que tiene predecesoras utiliza de forma predeterminada la última fecha de finalización de las predecesoras</span><span class="sxs-lookup"><span data-stu-id="1cf3f-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="1cf3f-188">Esfuerzo = número de personas \* duración \* horas en un día laborable estándar de calendario del proyecto</span><span class="sxs-lookup"><span data-stu-id="1cf3f-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="1cf3f-189">**Programación manual**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-189">**Manual scheduling**.</span></span>   <span data-ttu-id="1cf3f-190">En algunos, puede convenir desviarse de estas reglas.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="1cf3f-191">En estos casos, puede establecer el modo de tarea para que la tarea sea programada manualmente.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="1cf3f-192">Esto impide que el motor de programación calcule los valores de otros atributos de programación.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="1cf3f-193">Establecer predecesores en tareas afecta siempre a la fecha de inicio de la tarea dependiente.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="1cf3f-194">Crear una estructura de descomposición del trabajo</span><span class="sxs-lookup"><span data-stu-id="1cf3f-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="1cf3f-195">Vaya a **Project Service > Proyectos**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="1cf3f-196">Haga clic en el proyecto en el que desea trabajar.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="1cf3f-197">En la barra en la parte superior de la pantalla, seleccione la flecha hacia abajo junto al nombre del proyecto, y después haga clic en Estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="1cf3f-198">Para agregar una tarea, haga clic en **Agregar tarea**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="1cf3f-199">Complete los campos de la tarea y, a continuación, haga clic o pulse en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="1cf3f-200">Siga agregando tareas hasta que se complete la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="1cf3f-201">Cuando cree la estructura de descomposición del trabajo, puede hacer lo siguiente para organizar sus tareas:</span><span class="sxs-lookup"><span data-stu-id="1cf3f-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="1cf3f-202">Seleccione una tarea y haga clic en **Sangría** para moverla debajo de otra tarea o haga clic en anular sangría para sacarla de un nivel.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="1cf3f-203">Seleccione una tarea y haga clic en **Subir** o **Bajar** para moverla arriba o abajo en la lista.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="1cf3f-204">Haga clic en **Ocultar Gantt** para ocultar el gráfico de Gantt, y haga clic en **Mostrar Gantt** para mostrarlo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="1cf3f-205">Seleccione otro período de tiempo para el gráfico de Gantt en **Escala de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="1cf3f-206">Para agregar roles que especificó en la estructura de descomposición del trabajo a los integrantes del equipo del proyecto, haga clic en **Generar el equipo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="1cf3f-207">Haga clic en **Guardar** en la esquina inferior derecha de la pantalla cuando haya terminado de realizar los cambios.</span><span class="sxs-lookup"><span data-stu-id="1cf3f-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1cf3f-208">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cf3f-208">See Also</span></span>  
 [<span data-ttu-id="1cf3f-209">Guía del jefe de proyecto</span><span class="sxs-lookup"><span data-stu-id="1cf3f-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
