---
title: Modos de programación
description: En este tema se proporciona información sobre los modos de programación.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981456"
---
# <a name="scheduling-modes"></a><span data-ttu-id="7fc69-103">Modos de programación</span><span class="sxs-lookup"><span data-stu-id="7fc69-103">Scheduling modes</span></span>

<span data-ttu-id="7fc69-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="7fc69-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7fc69-105">Dynamics 365 Project Operations proporciona a las organizaciones la capacidad de definir cómo administran los cambios en variables clave en tareas dentro de la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="7fc69-106">Según las necesidades específicas de la organización, los jefes de proyecto pueden realizar cambios en el modo de programación cuando se crea un proyecto.</span><span class="sxs-lookup"><span data-stu-id="7fc69-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="7fc69-107">Hay tres modos de programación disponibles en Project Operations:</span><span class="sxs-lookup"><span data-stu-id="7fc69-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="7fc69-108">Duración fija (este es el modo predeterminado)</span><span class="sxs-lookup"><span data-stu-id="7fc69-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="7fc69-109">Trabajo fijo</span><span class="sxs-lookup"><span data-stu-id="7fc69-109">Fixed work</span></span>
  - <span data-ttu-id="7fc69-110">Unidades fijas</span><span class="sxs-lookup"><span data-stu-id="7fc69-110">Fixed units</span></span>

<span data-ttu-id="7fc69-111">Los valores afectados por la definición de un modo de programación específico se determinan mediante la siguiente fórmula:</span><span class="sxs-lookup"><span data-stu-id="7fc69-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="7fc69-112">Esfuerzo (*Trabajo*) = Duración x Unidades</span><span class="sxs-lookup"><span data-stu-id="7fc69-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="7fc69-113">Cuando define el modo de programación de un proyecto, está configurando uno de estos valores, que luego no se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="7fc69-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="7fc69-114">Mantener este valor como constante da prioridad a ese valor, lo que notifica al sistema que no lo cambie cuando cambien los otros dos valores.</span><span class="sxs-lookup"><span data-stu-id="7fc69-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="7fc69-115">La siguiente tabla proporciona información sobre los impactos de seleccionar un modo específico.</span><span class="sxs-lookup"><span data-stu-id="7fc69-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="7fc69-116">**En esta tarea**</span><span class="sxs-lookup"><span data-stu-id="7fc69-116">**In this task**</span></span>             | <span data-ttu-id="7fc69-117">**Si revisa unidades**</span><span class="sxs-lookup"><span data-stu-id="7fc69-117">**If you revise units**</span></span>   | <span data-ttu-id="7fc69-118">**Si revisa duración**</span><span class="sxs-lookup"><span data-stu-id="7fc69-118">**If you revise duration**</span></span> | <span data-ttu-id="7fc69-119">**Si revisa esfuerzo**</span><span class="sxs-lookup"><span data-stu-id="7fc69-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="7fc69-120">Tareas de unidades fijas</span><span class="sxs-lookup"><span data-stu-id="7fc69-120">Fixed units task</span></span>     | <span data-ttu-id="7fc69-121">Se recalcula la duración.</span><span class="sxs-lookup"><span data-stu-id="7fc69-121">Duration is recalculated.</span></span> | <span data-ttu-id="7fc69-122">Se recalcula el esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-122">Effort is recalculated.</span></span>    | <span data-ttu-id="7fc69-123">Se recalcula la duración.</span><span class="sxs-lookup"><span data-stu-id="7fc69-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="7fc69-124">Tarea de esfuerzo fijo</span><span class="sxs-lookup"><span data-stu-id="7fc69-124">Fixed effort task</span></span>    | <span data-ttu-id="7fc69-125">Se recalcula la duración.</span><span class="sxs-lookup"><span data-stu-id="7fc69-125">Duration is recalculated.</span></span> | <span data-ttu-id="7fc69-126">Se recalculan las unidades.</span><span class="sxs-lookup"><span data-stu-id="7fc69-126">Units are recalculated.</span></span>    | <span data-ttu-id="7fc69-127">Se recalcula la duración.</span><span class="sxs-lookup"><span data-stu-id="7fc69-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="7fc69-128">Tarea de duración fija</span><span class="sxs-lookup"><span data-stu-id="7fc69-128">Fixed duration task</span></span>  | <span data-ttu-id="7fc69-129">Se recalcula el esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-129">Effort is recalculated.</span></span>   | <span data-ttu-id="7fc69-130">Se recalcula el esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-130">Effort is recalculated.</span></span>    | <span data-ttu-id="7fc69-131">Se recalculan las unidades.</span><span class="sxs-lookup"><span data-stu-id="7fc69-131">Units are recalculated.</span></span>   |

<span data-ttu-id="7fc69-132">Para obtener más información sobre las implicaciones de un modo determinado, consulte [Cambiar el tipo de tarea para una programación más precisa](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="7fc69-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="7fc69-133">En el tema, el término **Trabajo** se usa en lugar de **Esfuerzo**.</span><span class="sxs-lookup"><span data-stu-id="7fc69-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="7fc69-134">Cambiar el modo de programación de la organización</span><span class="sxs-lookup"><span data-stu-id="7fc69-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="7fc69-135">Complete los siguientes pasos para definir el modo de programación de una organización.</span><span class="sxs-lookup"><span data-stu-id="7fc69-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="7fc69-136">Vaya a **Configuración** \> **General** \> **Parámetros** y luego seleccione el parámetro del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7fc69-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="7fc69-137">En la página **Parámetros del proyecto**, seleccione el modo de programación predeterminado para la organización y luego defina la capacidad para que el jefe de proyecto reemplace la configuración al crear un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="7fc69-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="7fc69-138">Cambiar la configuración del modo de programación en un proyecto</span><span class="sxs-lookup"><span data-stu-id="7fc69-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="7fc69-139">Si una organización permite que el jefe de proyecto reemplace el modo de programación predeterminado, el jefe de proyecto puede realizar ese cambio cuando cree un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="7fc69-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="7fc69-140">Sin embargo, una vez que se ha guardado el proyecto, el modo de programación no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="7fc69-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="7fc69-141">Proyectos copiados</span><span class="sxs-lookup"><span data-stu-id="7fc69-141">Copied projects</span></span>

<span data-ttu-id="7fc69-142">Dado que un proyecto se crea cuando se realiza la acción de copiar proyecto, el jefe de proyecto no puede establecer el modo de programación.</span><span class="sxs-lookup"><span data-stu-id="7fc69-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="7fc69-143">El proyecto de destino siempre estará predeterminado en el modo definido a nivel organizativo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="7fc69-144">Tareas copiadas</span><span class="sxs-lookup"><span data-stu-id="7fc69-144">Copied tasks</span></span>

<span data-ttu-id="7fc69-145">Cuando se copia una tarea de un proyecto a otro, la tarea hereda el modo de programación del proyecto de destino.</span><span class="sxs-lookup"><span data-stu-id="7fc69-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
