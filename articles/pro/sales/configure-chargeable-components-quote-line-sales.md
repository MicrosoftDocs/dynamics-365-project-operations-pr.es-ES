---
title: Configurar los componentes facturables de una línea de cotización
description: Este tema proporciona información sobre cómo configurar componentes facturables y no facturables en una línea de presupuesto basada en proyectos.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003787"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="23874-103">Configurar los componentes facturables de una línea de oferta</span><span class="sxs-lookup"><span data-stu-id="23874-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="23874-104">_**Se aplica a:** Implementación lite: acuerdo para factura proforma, Project Operations para escenarios basados en recursos/no mantenidos_</span><span class="sxs-lookup"><span data-stu-id="23874-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="23874-105">Una línea de contrato basada en proyectos tiene el concepto de componentes *incluidos* y componentes *facturables*.</span><span class="sxs-lookup"><span data-stu-id="23874-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="23874-106">Los componentes incluidos están sujetos a:</span><span class="sxs-lookup"><span data-stu-id="23874-106">Included components are subject to:</span></span>

  - <span data-ttu-id="23874-107">Método de facturación y divisiones de clientes</span><span class="sxs-lookup"><span data-stu-id="23874-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="23874-108">Límites a no exceder</span><span class="sxs-lookup"><span data-stu-id="23874-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="23874-109">Configuración de frecuencia de facturación definida en la línea de oferta basada en proyecto</span><span class="sxs-lookup"><span data-stu-id="23874-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="23874-110">Un subconjunto de los componentes incluidos se puede marcar como facturable usando el campo **Tipo de facturación**.</span><span class="sxs-lookup"><span data-stu-id="23874-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="23874-111">El campo **Tipo de facturación** es un conjunto de opciones que permite los siguientes valores en el contexto de una línea de oferta:</span><span class="sxs-lookup"><span data-stu-id="23874-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="23874-112">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-112">Chargeable</span></span>
  - <span data-ttu-id="23874-113">No facturable</span><span class="sxs-lookup"><span data-stu-id="23874-113">Non-chargeable</span></span>

<span data-ttu-id="23874-114">Los componentes facturables se pueden definir en tareas, roles y categorías de transacciones.</span><span class="sxs-lookup"><span data-stu-id="23874-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="23874-115">La facturabilidad se define en las tareas de una línea de oferta de proyecto y se aplica a todas las clases de transacciones incluidas en esa línea.</span><span class="sxs-lookup"><span data-stu-id="23874-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="23874-116">Si el campo **Incluir tareas** en una línea de contrato está en blanco o configurado en **Proyecto entero**, la pestaña **Tareas facturables** no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="23874-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="23874-117">La imputabilidad está definida en roles para una línea de oferta y solo se aplica a la clase de transacción **Hora**.</span><span class="sxs-lookup"><span data-stu-id="23874-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="23874-118">Si el campo **Incluir tiempo** en una línea de oferta de proyecto está configurado en **No**, la pestaña **Roles facturables** no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="23874-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="23874-119">La imputabilidad se define en categorías de transacción para una línea de oferta y solo se aplica a la clase de transacción **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="23874-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="23874-120">Si el campo **Incluir gastos** en una línea de oferta de proyecto está configurado en **No**, la pestaña **Categorías facturables** no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="23874-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="23874-121">Actualizar una tarea del proyecto para ser facturable o no facturable</span><span class="sxs-lookup"><span data-stu-id="23874-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="23874-122">Una tarea de proyecto puede ser facturable o no facturable en el contexto de una línea de cotización basada en proyecto, lo que posibilita la siguiente configuración.</span><span class="sxs-lookup"><span data-stu-id="23874-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="23874-123">Si una línea de cotización basada en un proyecto incluye **Hora** y la tarea **T1**, la tarea se asocia a la línea de cotización como facturable.</span><span class="sxs-lookup"><span data-stu-id="23874-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="23874-124">Si hay una segunda línea de oferta que incluye **Gastos**, puede asociar la tarea **T1** en la línea de oferta como no facturable.</span><span class="sxs-lookup"><span data-stu-id="23874-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="23874-125">El resultado es que todo el tiempo registrado en la tarea es imputable y todos los gastos registrados en la tarea no son facturables.</span><span class="sxs-lookup"><span data-stu-id="23874-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="23874-126">El tipo de facturación de una tarea se puede configurar en la pestaña **Tareas con cargo** de la línea de oferta basada en proyecto actualizando el campo **Tipo de facturación** en la subcuadrícula **Tareas de la línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="23874-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="23874-127">Alternativamente, puede actualizar el tipo de facturación en el campo **Tipo de facturación** de la subcuadrícula en la configuración de facturación de tareas de un proyecto que muestra las líneas de oferta asociadas a una tarea.</span><span class="sxs-lookup"><span data-stu-id="23874-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="23874-128">Actualizar un rol para ser facturable o no facturable</span><span class="sxs-lookup"><span data-stu-id="23874-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="23874-129">Un rol puede ser facturable o no facturable en el contexto de una línea de cotización específica basada en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="23874-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="23874-130">El tipo de facturación de un rol se puede configurar en la pestaña **Roles con cargo** de la línea de oferta basada en proyecto actualizando el campo **Tipo de facturación** en la subcuadrícula **Roles con cargo**.</span><span class="sxs-lookup"><span data-stu-id="23874-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="23874-131">Actualizar una categoría de transacción para ser facturable o no facturable</span><span class="sxs-lookup"><span data-stu-id="23874-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="23874-132">Una categoría de transacción puede ser facturable o no facturable en una línea de oferta específica.</span><span class="sxs-lookup"><span data-stu-id="23874-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="23874-133">El tipo de facturación de una transacción se puede configurar en la pestaña **Categorías con cargo** de la línea de oferta basada en proyecto actualizando el campo **Tipo de facturación** en la subcuadrícula **Categorías con cargo**.</span><span class="sxs-lookup"><span data-stu-id="23874-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="23874-134">Resolver imputabilidad</span><span class="sxs-lookup"><span data-stu-id="23874-134">Resolve chargeability</span></span>
<span data-ttu-id="23874-135">Un cálculo o dato real creado para el tiempo solo se considerará imputable si:</span><span class="sxs-lookup"><span data-stu-id="23874-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="23874-136">El **Tiempo** se incluye en la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="23874-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="23874-137">El **Rol** está configurado como imputable en la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="23874-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="23874-138">Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="23874-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="23874-139">Si estas tres cosas son ciertas, la **Tarea** también se configura como imputable.</span><span class="sxs-lookup"><span data-stu-id="23874-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="23874-140">Un cálculo o dato real creado para el gasto solo se considera imputable si:</span><span class="sxs-lookup"><span data-stu-id="23874-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="23874-141">El **Gasto** se incluye en la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="23874-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="23874-142">La **Categoría de transacción** está configurada como imputable en la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="23874-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="23874-143">Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="23874-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="23874-144">Si estas tres cosas son ciertas, la **Tarea** también se configura como imputable.</span><span class="sxs-lookup"><span data-stu-id="23874-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="23874-145">Un cálculo o dato real creado para el material solo se considerará imputable si:</span><span class="sxs-lookup"><span data-stu-id="23874-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="23874-146">Los **materiales** se incluyen en la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="23874-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="23874-147">Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="23874-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="23874-148">Si estas dos tres cosas son ciertas, la **Tarea** también deben configurarse como imputables.</span><span class="sxs-lookup"><span data-stu-id="23874-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="23874-149">
                    <strong>Incluye tiempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="23874-150">
                    <strong>Incluye gasto</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="23874-151">
                    <strong>Incluye materiales</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="23874-152">
                    <strong>Tareas incluidas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-153">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23874-154">
                    <strong>Categoría</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-155">
                    <strong>Tarea</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="23874-156">
                    <strong>Impacto de imputabilidad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-157">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-158">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-159">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-160">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="23874-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-161">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-162">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-163">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-164">Facturación a tiempo real: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-165">Tipo de facturación en gastos actuales: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-166">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-167">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-168">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-169">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-170">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="23874-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-171">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-172">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-173">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-174">Facturación a tiempo real: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-175">Tipo de facturación en gastos actuales: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-176">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-177">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-178">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-179">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-180">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="23874-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-181">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-182">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-183">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-184">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-185">Tipo de facturación en gastos actuales: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-186">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-187">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-188">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-189">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-190">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="23874-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-191">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-192">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-193">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-194">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-195">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-196">Tipo de facturación en material real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-197">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-198">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-199">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-200">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="23874-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-201">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-202">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-203">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-204">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-205">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-206">Tipo de facturación en material real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-207">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-208">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-209">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-210">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="23874-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-211">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23874-212">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-213">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-214">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-215">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-216">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="23874-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-218">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-219">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-220">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="23874-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-221">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23874-222">
                    <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-223">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-224">Facturación a tiempo real: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-225">Tipo de facturación en gastos actuales: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-226">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="23874-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-228">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-229">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-230">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="23874-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-231">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23874-232">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-233">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-234">Facturación a tiempo real: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-235">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-236">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-237">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="23874-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-239">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-240">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="23874-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-241">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-242">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-243">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-244">Facturación a tiempo real: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-245">Tipo de facturación en gastos reales: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-246">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-247">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="23874-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23874-249">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-250">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="23874-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-251">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-252">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-253">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-254">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-255">Tipo de facturación en gastos reales: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-256">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-257">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-258">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="23874-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-260">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="23874-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-261">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-262">Imputable</span><span class="sxs-lookup"><span data-stu-id="23874-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-263">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-264">Facturación a tiempo real: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-265">Tipo de facturación en gastos actuales: Facturable</span><span class="sxs-lookup"><span data-stu-id="23874-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23874-266">Tipo de facturación en material real: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23874-267">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23874-268">Sí</span><span class="sxs-lookup"><span data-stu-id="23874-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="23874-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23874-270">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="23874-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23874-271">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23874-272">
                    <strong>No facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23874-273">No se puede configurar</span><span class="sxs-lookup"><span data-stu-id="23874-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23874-274">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-275">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="23874-276">Tipo de facturación en material real: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23874-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
