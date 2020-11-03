---
title: Asignar proyectos y tareas a una línea de oferta basada en proyecto
description: Este tema proporciona información sobre cómo asignar proyectos y tareas a una línea de tareas basada en proyectos.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085040"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="96fc8-103">Asignar proyectos y tareas a una línea de oferta basada en proyecto</span><span class="sxs-lookup"><span data-stu-id="96fc8-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="96fc8-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="96fc8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="96fc8-105">En las líneas de oferta basadas en proyectos, puede asignar las tareas específicas de un proyecto que ya está asociado a una línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="96fc8-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="96fc8-106">Cuando asigna tareas a una línea de oferta, los siguientes elementos que definió en la línea de oferta solo se aplicarán a esas tareas:</span><span class="sxs-lookup"><span data-stu-id="96fc8-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="96fc8-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="96fc8-107">Billing method</span></span>
- <span data-ttu-id="96fc8-108">Opciones de imputabilidad</span><span class="sxs-lookup"><span data-stu-id="96fc8-108">Chargeability options</span></span>
- <span data-ttu-id="96fc8-109">Límites a no exceder</span><span class="sxs-lookup"><span data-stu-id="96fc8-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="96fc8-110">Clientes</span><span class="sxs-lookup"><span data-stu-id="96fc8-110">Customers</span></span>

<span data-ttu-id="96fc8-111">Por ejemplo, puede tener un proyecto en el que una fase es de precio fijo y todas las demás fases son de tiempo y materiales.</span><span class="sxs-lookup"><span data-stu-id="96fc8-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="96fc8-112">En este caso, puede asociar la primera fase, y todas sus tareas secundarias, a la línea de oferta para esa fase con un método de facturación de precio fijo.</span><span class="sxs-lookup"><span data-stu-id="96fc8-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="96fc8-113">A continuación, puede asociar todas las demás fases a la línea de oferta basada en tiempo y materiales.</span><span class="sxs-lookup"><span data-stu-id="96fc8-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="96fc8-114">Asociar tareas a líneas de oferta basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="96fc8-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="96fc8-115">Puede asociar tareas con líneas de oferta de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="96fc8-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="96fc8-116">Página **Proyecto** > Pestaña **Facturación de tareas** (óptimo)</span><span class="sxs-lookup"><span data-stu-id="96fc8-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="96fc8-117">Página **Línea de oferta** > Pestaña **Tareas cargables**</span><span class="sxs-lookup"><span data-stu-id="96fc8-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="96fc8-118">Desde la página del proyecto</span><span class="sxs-lookup"><span data-stu-id="96fc8-118">From the Project page</span></span>

<span data-ttu-id="96fc8-119">La página **Proyecto** proporciona la experiencia óptima para asociar tareas a líneas de oferta.</span><span class="sxs-lookup"><span data-stu-id="96fc8-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="96fc8-120">Puede usar esta página para seleccionar varias tareas y asociarlas todas, más sus tareas secundarias, a la línea de oferta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="96fc8-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="96fc8-121">En la pestaña **General** de una línea de oferta basada en proyecto, verifique que el campo **Proyecto** esté relleno.</span><span class="sxs-lookup"><span data-stu-id="96fc8-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="96fc8-122">En el campo **Tareas incluidas** , seleccione **Solo tareas seleccionadas**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="96fc8-123">Guarde la línea de oferta basadas en proyecto.</span><span class="sxs-lookup"><span data-stu-id="96fc8-123">Save the project-based quote line.</span></span> <span data-ttu-id="96fc8-124">Cuando el formulario se actualiza, aparece la pestaña **Tareas cargables**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="96fc8-125">En la pestaña **General** , seleccione el vínculo del proyecto en el campo **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="96fc8-126">En la página **Proyecto** , seleccione la pestaña **Facturación de tareas**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="96fc8-127">En la segunda cuadrícula, que se aplica a la configuración de facturación específica de la tarea, seleccione una o más tareas y luego seleccione **Líneas de oferta asociadas**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="96fc8-128">En la página de diálogo que aparece, seleccione una línea de oferta que muestre líneas de oferta basadas en proyecto de la oferta.</span><span class="sxs-lookup"><span data-stu-id="96fc8-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="96fc8-129">En el campo **Tipo de facturación** , indique si estas tareas son cargables o no.</span><span class="sxs-lookup"><span data-stu-id="96fc8-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="96fc8-130">Seleccione la casilla de verificación para indicar si la asociación debe incluir tareas secundarias de las tareas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="96fc8-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="96fc8-131">Al marcar la casilla, se asociarán las tareas secundarias de las tareas seleccionadas a la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="96fc8-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="96fc8-132">Seleccione **Aceptar** para cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="96fc8-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="96fc8-133">Desde la página de la línea de oferta</span><span class="sxs-lookup"><span data-stu-id="96fc8-133">From the Quote line page</span></span>

<span data-ttu-id="96fc8-134">Puede asociar las tareas del proyecto a las líneas de oferta desde la pestaña **Tareas cargables** de la página **Línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="96fc8-135">El lugar óptimo para asociar las tareas del proyecto a las líneas de oferta es la pestaña **Facturación de tareas** de la página **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="96fc8-136">Si asocia tareas de la pestaña **Tareas cargables** de la página **Línea de oferta** , debe asociar manualmente cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="96fc8-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="96fc8-137">En la pestaña **General** de una línea de oferta basada en proyecto, verifique que haya un proyecto seleccionado en el campo **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="96fc8-138">En el campo **Tareas incluidas** , seleccione **Solo tareas seleccionadas**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="96fc8-139">Guarde la línea de oferta basadas en proyecto.</span><span class="sxs-lookup"><span data-stu-id="96fc8-139">Save the project-based quote line.</span></span> <span data-ttu-id="96fc8-140">Cuando el formulario se actualiza, aparece la pestaña **Tareas cargables**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="96fc8-141">En la pestaña **Tareas cargables** , seleccione **Agregar una tarea de línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="96fc8-142">En la página **Tarea de línea de oferta** , en el campo **Tareas** , seleccione la tarea, y en el campo **Tipo de facturación** , seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="96fc8-143">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="96fc8-143">Close the page.</span></span> <span data-ttu-id="96fc8-144">La tarea seleccionada ahora está asociada a la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="96fc8-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="96fc8-145">Disociar tareas de líneas de oferta basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="96fc8-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="96fc8-146">Desde la página del proyecto</span><span class="sxs-lookup"><span data-stu-id="96fc8-146">From the Project page</span></span>

<span data-ttu-id="96fc8-147">Este método proporciona la experiencia óptima para disociar tareas de líneas de oferta.</span><span class="sxs-lookup"><span data-stu-id="96fc8-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="96fc8-148">Puede seleccionar varias tareas y disociarlas todas, más sus tareas secundarias, de la línea de oferta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="96fc8-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="96fc8-149">En la pestaña **General** de una línea de oferta basada en proyecto, en el campo **Proyecto** , seleccione el vínculo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="96fc8-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="96fc8-150">En la página **Proyecto** , seleccione la pestaña **Facturación de tareas**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="96fc8-151">En la segunda cuadrícula, que se aplica a la configuración de facturación específica de tareas, seleccione una o más tareas y luego seleccione **Dosociar oferta**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="96fc8-152">En la página de diálogo que aparece, seleccione una línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="96fc8-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="96fc8-153">Seleccione la casilla para indicar si la asociación debe también quitarse de las tareas secundarias de las tareas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="96fc8-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="96fc8-154">Al marcar la casilla, se disociarán también las tareas secundarias de las tareas seleccionadas de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="96fc8-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="96fc8-155">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-155">Select **OK**.</span></span> <span data-ttu-id="96fc8-156">Un mensaje de advertencia le informa de que, si elimina esta asociación, los datos reales registrados previamente en la tarea podrían revertirse.</span><span class="sxs-lookup"><span data-stu-id="96fc8-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="96fc8-157">Seleccione **Aceptar** para continuar y eliminar la asociación entre la tarea y la línea de oferta basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="96fc8-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="96fc8-158">Desde la página de la línea de oferta</span><span class="sxs-lookup"><span data-stu-id="96fc8-158">From the Quote line page</span></span>

<span data-ttu-id="96fc8-159">Puede disociar también las tareas del proyecto de las líneas de oferta desde la pestaña **Tareas cargables** de la página **Línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="96fc8-160">En la pestaña **Tareas cargables** , seleccione **Eliminar una tarea de línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="96fc8-161">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="96fc8-161">Select **OK**.</span></span> <span data-ttu-id="96fc8-162">Un mensaje de advertencia le informa de que, si elimina esta asociación, los datos reales registrados previamente en la tarea podrían revertirse.</span><span class="sxs-lookup"><span data-stu-id="96fc8-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="96fc8-163">Seleccione **Aceptar** para continuar y eliminar la asociación entre la tarea y la línea de oferta basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="96fc8-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="96fc8-164">Este procedimiento no elimina la tarea del proyecto.</span><span class="sxs-lookup"><span data-stu-id="96fc8-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="96fc8-165">Solo elimina la asociación de tareas de la línea de oferta basada en proyecto.</span><span class="sxs-lookup"><span data-stu-id="96fc8-165">It only removes the task association from the project-based quote line.</span></span>
