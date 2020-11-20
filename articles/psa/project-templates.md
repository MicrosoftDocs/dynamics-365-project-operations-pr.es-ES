---
title: Plantillas de proyecto
description: En este tema se proporciona información sobre cómo usar plantillas de proyecto para una configuración rápida del proyecto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123056"
---
# <a name="project-templates"></a><span data-ttu-id="397c8-103">Plantillas de proyecto</span><span class="sxs-lookup"><span data-stu-id="397c8-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="397c8-104">Una plantilla de proyecto es un marco predefinido que le ayuda a iniciar un proyecto de manera rápida y sencilla.</span><span class="sxs-lookup"><span data-stu-id="397c8-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="397c8-105">Puede usar una plantilla predefinida para crear un nuevo proyecto con un solo clic.</span><span class="sxs-lookup"><span data-stu-id="397c8-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="397c8-106">En cuanto a los proyectos, debe definir los requisitos previos para las plantillas de proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="397c8-107">Debe definir un calendario de proyecto para cada plantilla de proyecto, y los roles y las listas de precios deben estar predefinidos en la organización de modo que los componentes de la plantilla tengan datos útiles.</span><span class="sxs-lookup"><span data-stu-id="397c8-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="397c8-108">Una plantilla de proyecto consta de tres componentes: una programación, estimaciones del proyecto y miembros del equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="397c8-109">Programar</span><span class="sxs-lookup"><span data-stu-id="397c8-109">Schedule</span></span>

<span data-ttu-id="397c8-110">Una programación en una plantilla de proyecto tiene el mismo conjunto de elementos que una programación en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="397c8-111">Puede crear una jerarquía de tareas, asociar roles con tareas, definir atributos de programación y establecer dependencias.</span><span class="sxs-lookup"><span data-stu-id="397c8-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="397c8-112">Una programación en una plantilla de proyecto también admite modos de tarea para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="397c8-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="397c8-113">Por lo tanto, es compatible con el motor de programación.</span><span class="sxs-lookup"><span data-stu-id="397c8-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="397c8-114">Debe asociar un calendario de proyecto con el proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="397c8-115">Cuando cree una programación de trabajo, no habrá ninguna diferencia entre una plantilla de proyecto y un proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="397c8-116">Estimaciones de proyecto</span><span class="sxs-lookup"><span data-stu-id="397c8-116">Project estimates</span></span>

<span data-ttu-id="397c8-117">Las estimaciones de proyecto en una plantilla de proyecto funcionan de la misma manera que las estimaciones de proyecto en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="397c8-118">Sin embargo, el coste y los precios de venta se extraen de las listas predeterminadas de costes y precios de venta que se definen en los parámetros.</span><span class="sxs-lookup"><span data-stu-id="397c8-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="397c8-119">Creación de un proyecto a partir de una plantilla</span><span class="sxs-lookup"><span data-stu-id="397c8-119">Creating a project from a template</span></span>
 
<span data-ttu-id="397c8-120">Existen varias formas de crear un proyecto a partir de una plantilla de proyecto:</span><span class="sxs-lookup"><span data-stu-id="397c8-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="397c8-121">Cuando cree un proyecto a partir de una oferta, puede seleccionar una plantilla de proyecto en el cuadro de diálogo **Creación rápida: Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="397c8-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Cuadro de diálogo Creación rápida: Proyecto](media/project-11.png)

- <span data-ttu-id="397c8-123">Cuando cree un proyecto seleccionando **Nuevo proyecto**, la página **Proyecto** aparecerá antes de guardar el registro.</span><span class="sxs-lookup"><span data-stu-id="397c8-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="397c8-124">En el campo **Elegir una plantilla**, seleccione una de las plantillas de proyecto predefinidas en la organización.</span><span class="sxs-lookup"><span data-stu-id="397c8-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="397c8-125">Use **Crear proyecto desde una plantilla** en la página **Entidad de plantilla**.</span><span class="sxs-lookup"><span data-stu-id="397c8-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="397c8-126">Copia de componentes de una plantilla a un proyecto</span><span class="sxs-lookup"><span data-stu-id="397c8-126">Copying components of template to project</span></span>

<span data-ttu-id="397c8-127">Cuando copia los componentes de una plantilla de proyecto a un proyecto, pueden producirse algunos reemplazos según de la configuración del proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="397c8-128">Copia de la programación</span><span class="sxs-lookup"><span data-stu-id="397c8-128">Copying the schedule</span></span>

<span data-ttu-id="397c8-129">Cuando copie la programación de una plantilla de proyecto, si el proyecto tiene un calendario de proyecto diferente al de la plantilla, las horas de trabajo del calendario del proyecto se aplicarán a la programación de tareas.</span><span class="sxs-lookup"><span data-stu-id="397c8-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="397c8-130">De esta manera, la programación se ajusta para que coincida con el calendario del proyecto de apoyo.</span><span class="sxs-lookup"><span data-stu-id="397c8-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="397c8-131">Del mismo modo, la primera tarea de la programación selecciona la fecha de inicio del proyecto, y la programación del resto de la jerarquía se actualiza en función de la duración y las dependencias que se especifican en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="397c8-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="397c8-132">Copia de estimaciones de proyecto</span><span class="sxs-lookup"><span data-stu-id="397c8-132">Copying project estimates</span></span> 

<span data-ttu-id="397c8-133">Cuando copie entre líneas de estimación de proyecto, se actualizarán las listas de precios.</span><span class="sxs-lookup"><span data-stu-id="397c8-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="397c8-134">Para la lista de precios de costes, estas actualizaciones se basan en la unidad propietaria del proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="397c8-135">Para la lista de precios de venta, se basan en el cliente.</span><span class="sxs-lookup"><span data-stu-id="397c8-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="397c8-136">Para los proyectos que están asociados con una entidad de ventas, el coste unitario y los precios de venta se determinan en función de estas listas de precios.</span><span class="sxs-lookup"><span data-stu-id="397c8-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="397c8-137">Copia de un equipo de proyecto</span><span class="sxs-lookup"><span data-stu-id="397c8-137">Copying a project team</span></span>

<span data-ttu-id="397c8-138">Cuando se copia un equipo de proyecto de una plantilla de proyecto a un proyecto, se copian los recursos genéricos, junto con las habilidades y competencias que se definen en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="397c8-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="397c8-139">Las asignaciones de recursos genéricos también se mantienen como si estuvieran en la plantilla de proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="397c8-140">Los recursos con nombre no son compatibles con las plantillas de proyecto.</span><span class="sxs-lookup"><span data-stu-id="397c8-140">Named resources aren't supported in project templates.</span></span>
