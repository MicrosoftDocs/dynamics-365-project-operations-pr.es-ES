---
title: Asignar proyectos y tareas a una línea de oferta basada en proyecto
description: Este tema proporciona información sobre cómo asignar proyectos y tareas a una línea de tareas basada en proyectos.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d1c98d6a903393a0afc0e94d7f9859d55b9dc1f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994607"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="f0369-103">Asignar proyectos y tareas a una línea de oferta basada en proyecto</span><span class="sxs-lookup"><span data-stu-id="f0369-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="f0369-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="f0369-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f0369-105">En las líneas de oferta basadas en proyectos, puede asignar las tareas específicas de un proyecto que ya está asociado a una línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="f0369-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="f0369-106">Cuando asigna tareas a una línea de oferta, los siguientes elementos que definió en la línea de oferta solo se aplicarán a esas tareas:</span><span class="sxs-lookup"><span data-stu-id="f0369-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="f0369-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="f0369-107">Billing method</span></span>
- <span data-ttu-id="f0369-108">Opciones de imputabilidad</span><span class="sxs-lookup"><span data-stu-id="f0369-108">Chargeability options</span></span>
- <span data-ttu-id="f0369-109">Límites a no exceder</span><span class="sxs-lookup"><span data-stu-id="f0369-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="f0369-110">Clientes</span><span class="sxs-lookup"><span data-stu-id="f0369-110">Customers</span></span>

<span data-ttu-id="f0369-111">Por ejemplo, puede tener un proyecto en el que una fase es de precio fijo y todas las demás fases son de tiempo y materiales.</span><span class="sxs-lookup"><span data-stu-id="f0369-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="f0369-112">En este caso, puede asociar la primera fase, y todas sus tareas secundarias, a la línea de oferta para esa fase con un método de facturación de precio fijo.</span><span class="sxs-lookup"><span data-stu-id="f0369-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="f0369-113">A continuación, puede asociar todas las demás fases a la línea de oferta basada en tiempo y materiales.</span><span class="sxs-lookup"><span data-stu-id="f0369-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="f0369-114">Asociar tareas a líneas de oferta basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="f0369-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="f0369-115">Puede asociar tareas con líneas de oferta de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="f0369-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="f0369-116">Página **Proyecto** > Pestaña **Facturación de tareas** (óptimo)</span><span class="sxs-lookup"><span data-stu-id="f0369-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="f0369-117">Página **Línea de oferta** > Pestaña **Tareas cargables**</span><span class="sxs-lookup"><span data-stu-id="f0369-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="f0369-118">Desde la página del proyecto</span><span class="sxs-lookup"><span data-stu-id="f0369-118">From the Project page</span></span>

<span data-ttu-id="f0369-119">La página **Proyecto** proporciona la experiencia óptima para asociar tareas a líneas de oferta.</span><span class="sxs-lookup"><span data-stu-id="f0369-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="f0369-120">Puede usar esta página para seleccionar varias tareas y asociarlas todas, más sus tareas secundarias, a la línea de oferta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f0369-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="f0369-121">En la pestaña **General** de una línea de oferta basada en proyecto, verifique que el campo **Proyecto** esté relleno.</span><span class="sxs-lookup"><span data-stu-id="f0369-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="f0369-122">En el campo **Tareas incluidas**, seleccione **Solo tareas seleccionadas**.</span><span class="sxs-lookup"><span data-stu-id="f0369-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="f0369-123">Guarde la línea de oferta basadas en proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0369-123">Save the project-based quote line.</span></span> <span data-ttu-id="f0369-124">Cuando el formulario se actualiza, aparece la pestaña **Tareas cargables**.</span><span class="sxs-lookup"><span data-stu-id="f0369-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="f0369-125">En la pestaña **General**, seleccione el vínculo del proyecto en el campo **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="f0369-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="f0369-126">En la página **Proyecto**, seleccione la pestaña **Facturación de tareas**.</span><span class="sxs-lookup"><span data-stu-id="f0369-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="f0369-127">En la segunda cuadrícula, que se aplica a la configuración de facturación específica de la tarea, seleccione una o más tareas y luego seleccione **Líneas de oferta asociadas**.</span><span class="sxs-lookup"><span data-stu-id="f0369-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="f0369-128">En la página de diálogo que aparece, seleccione una línea de oferta que muestre líneas de oferta basadas en proyecto de la oferta.</span><span class="sxs-lookup"><span data-stu-id="f0369-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="f0369-129">En el campo **Tipo de facturación**, indique si estas tareas son cargables o no.</span><span class="sxs-lookup"><span data-stu-id="f0369-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="f0369-130">Seleccione la casilla de verificación para indicar si la asociación debe incluir tareas secundarias de las tareas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="f0369-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="f0369-131">Al marcar la casilla, se asociarán las tareas secundarias de las tareas seleccionadas a la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="f0369-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="f0369-132">Seleccione **Aceptar** para cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f0369-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="f0369-133">Desde la página de la línea de oferta</span><span class="sxs-lookup"><span data-stu-id="f0369-133">From the Quote line page</span></span>

<span data-ttu-id="f0369-134">Puede asociar las tareas del proyecto a las líneas de oferta desde la pestaña **Tareas cargables** de la página **Línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="f0369-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="f0369-135">El lugar óptimo para asociar las tareas del proyecto a las líneas de oferta es la pestaña **Facturación de tareas** de la página **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="f0369-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="f0369-136">Si asocia tareas de la pestaña **Tareas cargables** de la página **Línea de oferta**, debe asociar manualmente cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0369-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="f0369-137">En la pestaña **General** de una línea de oferta basada en proyecto, verifique que haya un proyecto seleccionado en el campo **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="f0369-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="f0369-138">En el campo **Tareas incluidas**, seleccione **Solo tareas seleccionadas**.</span><span class="sxs-lookup"><span data-stu-id="f0369-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="f0369-139">Guarde la línea de oferta basadas en proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0369-139">Save the project-based quote line.</span></span> <span data-ttu-id="f0369-140">Cuando el formulario se actualiza, aparece la pestaña **Tareas cargables**.</span><span class="sxs-lookup"><span data-stu-id="f0369-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="f0369-141">En la pestaña **Tareas cargables**, seleccione **Agregar una tarea de línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="f0369-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="f0369-142">En la página **Tarea de línea de oferta**, en el campo **Tareas**, seleccione la tarea, y en el campo **Tipo de facturación**, seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f0369-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="f0369-143">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="f0369-143">Close the page.</span></span> <span data-ttu-id="f0369-144">La tarea seleccionada ahora está asociada a la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="f0369-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="f0369-145">Disociar tareas de líneas de oferta basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="f0369-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="f0369-146">Desde la página del proyecto</span><span class="sxs-lookup"><span data-stu-id="f0369-146">From the Project page</span></span>

<span data-ttu-id="f0369-147">Este método proporciona la experiencia óptima para disociar tareas de líneas de oferta.</span><span class="sxs-lookup"><span data-stu-id="f0369-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="f0369-148">Puede seleccionar varias tareas y disociarlas todas, más sus tareas secundarias, de la línea de oferta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f0369-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="f0369-149">En la pestaña **General** de una línea de oferta basada en proyecto, en el campo **Proyecto**, seleccione el vínculo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0369-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="f0369-150">En la página **Proyecto**, seleccione la pestaña **Facturación de tareas**.</span><span class="sxs-lookup"><span data-stu-id="f0369-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="f0369-151">En la segunda cuadrícula, que se aplica a la configuración de facturación específica de tareas, seleccione una o más tareas y luego seleccione **Dosociar oferta**.</span><span class="sxs-lookup"><span data-stu-id="f0369-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="f0369-152">En la página de diálogo que aparece, seleccione una línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="f0369-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="f0369-153">Seleccione la casilla para indicar si la asociación debe también quitarse de las tareas secundarias de las tareas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="f0369-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="f0369-154">Al marcar la casilla, se disociarán también las tareas secundarias de las tareas seleccionadas de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="f0369-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="f0369-155">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f0369-155">Select **OK**.</span></span> <span data-ttu-id="f0369-156">Un mensaje de advertencia le informa de que, si elimina esta asociación, los datos reales registrados previamente en la tarea podrían revertirse.</span><span class="sxs-lookup"><span data-stu-id="f0369-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="f0369-157">Seleccione **Aceptar** para continuar y eliminar la asociación entre la tarea y la línea de oferta basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0369-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="f0369-158">Desde la página de la línea de oferta</span><span class="sxs-lookup"><span data-stu-id="f0369-158">From the Quote line page</span></span>

<span data-ttu-id="f0369-159">Puede disociar también las tareas del proyecto de las líneas de oferta desde la pestaña **Tareas cargables** de la página **Línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="f0369-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="f0369-160">En la pestaña **Tareas cargables**, seleccione **Eliminar una tarea de línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="f0369-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="f0369-161">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f0369-161">Select **OK**.</span></span> <span data-ttu-id="f0369-162">Un mensaje de advertencia le informa de que, si elimina esta asociación, los datos reales registrados previamente en la tarea podrían revertirse.</span><span class="sxs-lookup"><span data-stu-id="f0369-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="f0369-163">Seleccione **Aceptar** para continuar y eliminar la asociación entre la tarea y la línea de oferta basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0369-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="f0369-164">Este procedimiento no elimina la tarea del proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0369-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="f0369-165">Solo elimina la asociación de tareas de la línea de oferta basada en proyecto.</span><span class="sxs-lookup"><span data-stu-id="f0369-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]