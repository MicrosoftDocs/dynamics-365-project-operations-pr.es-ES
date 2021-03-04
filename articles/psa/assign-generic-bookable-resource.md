---
title: Asignar recursos genéricos que se pueden reservar a un equipo de proyecto y tareas
description: En este tema se proporciona información sobre cómo reservar recursos genéricos para equipos de proyectos y tareas.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145424"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="e8c80-103">Asignar recursos genéricos que se pueden reservar a una tarea y generar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="e8c80-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e8c80-104">Además de reservar y asignar a su proyecto recursos reales o con nombre, también puede asignar recursos genéricos a las tareas de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="e8c80-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="e8c80-105">Estos recursos pueden servir como marcadores de posición para los recursos con nombre hasta que esté listo para proporcionar recursos con nombre a su proyecto.</span><span class="sxs-lookup"><span data-stu-id="e8c80-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="e8c80-106">En Project Service Automation (PSA), abra la página **Proyecto** y, en la pestaña **Programación**, escriba el nombre de la posición del recurso genérico en la celda **Recurso** de la programación.</span><span class="sxs-lookup"><span data-stu-id="e8c80-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="e8c80-107">O bien, haga clic en el icono **Recurso** de la celda para abrir el selector de recursos y especificar el nombre del recurso genérico que desee crear.</span><span class="sxs-lookup"><span data-stu-id="e8c80-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Creación y asignación de un miembro del equipo genérico](media/RM-how-to-9.png)

<span data-ttu-id="e8c80-109">Se abrirá el panel **Creación rápida: Miembro del equipo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="e8c80-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="e8c80-110">Escriba el rol y la unidad organizativa miembro del equipo del recurso genérico y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="e8c80-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Creación rápida del miembro del equipo genérico](media/RM-how-to-10.png)

3. <span data-ttu-id="e8c80-112">Tras crear el nuevo miembro del equipo de recurso genérico, se le asignará la tarea.</span><span class="sxs-lookup"><span data-stu-id="e8c80-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="e8c80-113">Puede seguir asignando ese recurso genérico a otras tareas de la programación de tareas.</span><span class="sxs-lookup"><span data-stu-id="e8c80-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Asignación de un miembro del equipo genérico existente a las tareas](media/RM-how-to-11.png)

4. <span data-ttu-id="e8c80-115">Tras asignar el recurso genérico, puede generar un requisito de recurso y cumplirlo directamente reservando o enviando una solicitud de recurso a un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="e8c80-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generación de un requisito para un miembro del equipo genérico](media/RM-how-to-12.png)

<span data-ttu-id="e8c80-117">En la cuadrícula del miembro del equipo, además de poder usar el selector de recursos tal como se indicó anteriormente, también podrá agregar recursos genéricos directamente.</span><span class="sxs-lookup"><span data-stu-id="e8c80-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="e8c80-118">Los recursos se agregan con un requisito de recursos que se basa en las fechas de inicio y de finalización y con el método de asignación que se especifica en el panel **Creación rápida: Miembro del equipo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="e8c80-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="e8c80-119">Puede ver diferencias si agrega el miembro del equipo genérico directamente y después asigna más tareas al recurso genérico y se superan las horas disponibles para realizarlas.</span><span class="sxs-lookup"><span data-stu-id="e8c80-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="e8c80-120">Haga click en **Generar requisito** para regenerar el requisito de equilibrar las horas necesarias con respecto a las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="e8c80-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="e8c80-121">También puede hacer clic en el vínculo **Requisito de recurso** en la cuadrícula de equipo para abrir el requisito y agregar conocimientos, recursos preferidos, etc.</span><span class="sxs-lookup"><span data-stu-id="e8c80-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Requisito de recursos](media/RM-how-to-13.png)

