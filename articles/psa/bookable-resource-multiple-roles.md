---
title: Estimar los costes y las ventas de proyecto cuando un recurso que se puede reservar completa varios roles en un proyecto
description: En este tema se proporciona información sobre cómo usar las dimensiones de precios a fin de respaldar los precios y costes para un recurso que desempeñe varios roles en un proyecto.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291010"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="84af0-103">Estimar los costes y las ventas de proyecto cuando un recurso que se puede reservar completa varios roles en un proyecto</span><span class="sxs-lookup"><span data-stu-id="84af0-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="84af0-104">Las empresas basadas en proyectos a menudo tienen la necesidad de que un recurso desempeñe varios roles en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="84af0-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="84af0-105">Cada uno de estos roles podría tener un precio y un coste diferente, lo que significa que el tiempo del mismo recurso en el proyecto podría obtener una estimación financiera diferente según las tasas de facturación y coste para cada uno de los roles.</span><span class="sxs-lookup"><span data-stu-id="84af0-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="84af0-106">Project Service Automation permite configurar los valores en el registro del miembro del equipo para el recurso nombrado y permite diferentes anulaciones en cada una de las tareas a las que está asignado el miembro del equipo.</span><span class="sxs-lookup"><span data-stu-id="84af0-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="84af0-107">El siguiente ejemplo explica cómo la simple anulación de este valor permite que un recurso tenga varios roles en un proyecto con diferentes tasas de coste y facturación.</span><span class="sxs-lookup"><span data-stu-id="84af0-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="84af0-108">Crear tareas</span><span class="sxs-lookup"><span data-stu-id="84af0-108">Create tasks</span></span>
<span data-ttu-id="84af0-109">Cree dos tareas de proyecto de 40 horas cada una, la Tarea A y la Tarea B. Seleccione la Tarea A como predecesora de la Tarea B.</span><span class="sxs-lookup"><span data-stu-id="84af0-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="84af0-110">Configurar Rol y Unidad organizativa para un miembro del equipo genérico del proyecto</span><span class="sxs-lookup"><span data-stu-id="84af0-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="84af0-111">En la página **Programar**, seleccione la fila **Tarea** para la Tarea A.</span><span class="sxs-lookup"><span data-stu-id="84af0-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="84af0-112">En el campo **Recursos**, seleccione **Crear** en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="84af0-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="84af0-113">En la página **Creación rápida de miembros del equipo**, especifique los atributos del miembro del equipo genérico que puede realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="84af0-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="84af0-114">Seleccione el rol y la unidad organizativa apropiada y luego seleccione **Guardar y cerrar**.</span><span class="sxs-lookup"><span data-stu-id="84af0-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="84af0-115">Se crea un miembro del equipo genérico y se asigna a esta tarea.</span><span class="sxs-lookup"><span data-stu-id="84af0-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="84af0-116">Repita estos pasos para la Tarea B y asegúrese de que el rol y la unidad organizativa del miembro del equipo genérico creado para la Tarea B sea diferente a la Tarea A.</span><span class="sxs-lookup"><span data-stu-id="84af0-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="84af0-117">Configure el rol y la unidad organizativa para una tarea del proyecto</span><span class="sxs-lookup"><span data-stu-id="84af0-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="84af0-118">Después de crear la Tarea A, seleccione la tarea y luego seleccione **Editar tarea**.</span><span class="sxs-lookup"><span data-stu-id="84af0-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="84af0-119">En la página **Detalles de la tarea**, encuentre los campos **Rol** y **Unidad organizativa**, y agregue los valores que se requieren de un recurso que realizaría esta tarea.</span><span class="sxs-lookup"><span data-stu-id="84af0-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="84af0-120">Si está completando estos escenarios con los datos de demostración de Project Service Automation, seleccione **Jefe de consultoría** para el rol y **Fabrikam US** como unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="84af0-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="84af0-121">Seleccione la Tarea B y, a continuación, seleccione **Editar tarea**.</span><span class="sxs-lookup"><span data-stu-id="84af0-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="84af0-122">En la página **Detalles de la tarea**, encuentre los campos **Rol** y **Unidad organizativa**, y agregue los valores que se requieren de un recurso que realizaría esta tarea.</span><span class="sxs-lookup"><span data-stu-id="84af0-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="84af0-123">Asegúrese de que los valores de los campos **Rol** y **Unidad organizativa** para la Tarea B son diferentes de los valores para la Tarea A.</span><span class="sxs-lookup"><span data-stu-id="84af0-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="84af0-124">Si está completando estos escenarios con los datos de demostración de Project Service Automation, seleccione **Técnico de red** para el rol y **Fabrikam US** como unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="84af0-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="84af0-125">Seleccione y cierre la página **Detalles de la tarea**.</span><span class="sxs-lookup"><span data-stu-id="84af0-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="84af0-126">Miembro del equipo y comportamiento de estimaciones</span><span class="sxs-lookup"><span data-stu-id="84af0-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="84af0-127">En la página **Detalles de la tarea**, en el **Miembro del equipo**, seleccione los dos miembros del equipo genéricos y luego seleccione **Generar requisitos**.</span><span class="sxs-lookup"><span data-stu-id="84af0-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="84af0-128">Seleccione la fila del miembro del equipo para **Jefe de consultoría** y luego seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="84af0-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="84af0-129">El tablero de programación se abre y reserva un recurso para ese requisito.</span><span class="sxs-lookup"><span data-stu-id="84af0-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="84af0-130">Seleccione la fila del miembro del equipo para **Técnico de red** y seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="84af0-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="84af0-131">El tablero de programación se abre y reserva el mismo recurso en ese requisito.</span><span class="sxs-lookup"><span data-stu-id="84af0-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="84af0-132">Cuadrícula Miembro del equipo</span><span class="sxs-lookup"><span data-stu-id="84af0-132">Team Member grid</span></span> 
<span data-ttu-id="84af0-133">En la cuadrícula **Miembro del equipo**, observe que se eliminan los dos registros de miembros del equipo genéricos y se reemplazan por un recurso.</span><span class="sxs-lookup"><span data-stu-id="84af0-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="84af0-134">Hay un conjunto de valores para ese recurso que muestra un conjunto predeterminado de valores para **Rol** y **Unidad organizativa**.</span><span class="sxs-lookup"><span data-stu-id="84af0-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="84af0-135">Cuando amplía la fila de ese registro de miembro del equipo, puede ver distintas asignaciones en el registro de miembro del equipo para ambas tareas.</span><span class="sxs-lookup"><span data-stu-id="84af0-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="84af0-136">Cada fila de asignación tiene valores específicos de tarea para **Rol** y **Unidad organizativa**.</span><span class="sxs-lookup"><span data-stu-id="84af0-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="84af0-137">Cuadrícula Estimaciones</span><span class="sxs-lookup"><span data-stu-id="84af0-137">Estimates grid</span></span> 
<span data-ttu-id="84af0-138">Cuando navega a la cuadrícula **Estimaciones**, observará que ambas asignaciones para el mismo recurso tienen un precio diferente.</span><span class="sxs-lookup"><span data-stu-id="84af0-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="84af0-139">Se asignan precios a la asignación para el recurso en la Tarea A mediante el valor de atributo **Rol** de **Jefe de consultoría**.</span><span class="sxs-lookup"><span data-stu-id="84af0-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="84af0-140">Se asignan precios a la asignación para el mismo recurso en la Tarea B mediante el valor de atributo **Rol** de **Técnico de red**.</span><span class="sxs-lookup"><span data-stu-id="84af0-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]