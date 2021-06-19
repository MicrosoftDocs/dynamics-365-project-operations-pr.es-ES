---
title: Configurar componentes facturables de una línea de contrato basada en proyectos
description: Este tema proporciona información sobre cómo agregar componentes facturables a las líneas de contrato en Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003742"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="763b9-103">Configurar componentes facturables de una línea de contrato basada en proyectos</span><span class="sxs-lookup"><span data-stu-id="763b9-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="763b9-104">_**Se aplica a:** Implementación lite: acuerdo para factura proforma, Project Operations para escenarios basados en recursos/no mantenidos_</span><span class="sxs-lookup"><span data-stu-id="763b9-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="763b9-105">Una línea de contrato basada en proyectos tiene *incluido* componentes y componentes *facturables*.</span><span class="sxs-lookup"><span data-stu-id="763b9-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="763b9-106">Los componentes incluidos son componentes que están sujetos a:</span><span class="sxs-lookup"><span data-stu-id="763b9-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="763b9-107">Método de facturación y divisiones de clientes</span><span class="sxs-lookup"><span data-stu-id="763b9-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="763b9-108">Límites a no exceder</span><span class="sxs-lookup"><span data-stu-id="763b9-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="763b9-109">Configuración de frecuencia de facturación definida en la línea de contrato basada en proyecto</span><span class="sxs-lookup"><span data-stu-id="763b9-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="763b9-110">Un subconjunto de los componentes incluidos se puede marcar como facturable usando el campo **Tipo de facturación**.</span><span class="sxs-lookup"><span data-stu-id="763b9-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="763b9-111">El campo **Tipo de facturación** es un conjunto de opciones que permite los siguientes valores en el contexto de una línea de contrato:</span><span class="sxs-lookup"><span data-stu-id="763b9-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="763b9-112">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-112">Chargeable</span></span>
  - <span data-ttu-id="763b9-113">No facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-113">Non-chargeable</span></span>

<span data-ttu-id="763b9-114">Los componentes facturables se pueden definir en tareas, roles y categorías de transacciones.</span><span class="sxs-lookup"><span data-stu-id="763b9-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="763b9-115">La facturabilidad se define en las tareas de una línea de contrato de proyecto y se aplica a todas las clases de transacciones incluidas en la línea.</span><span class="sxs-lookup"><span data-stu-id="763b9-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="763b9-116">Si el campo **Incluir tareas** en una línea de contrato está en blanco o configurado en **Proyecto entero**, la pestaña **Tareas imputables** no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="763b9-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="763b9-117">La imputabilidad definida en roles para una línea de contrato de proyecto solo se aplica a la clase de transacción **Hora**.</span><span class="sxs-lookup"><span data-stu-id="763b9-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="763b9-118">Si el campo **Incluir tiempo** en una línea de contrato está configurado en **No**, la pestaña **Roles facturables** no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="763b9-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="763b9-119">La imputabilidad definida en categorías de transacción para una línea de contrato de proyecto solo se aplica a la clase de transacción **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="763b9-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="763b9-120">Si el campo **Incluir gastos** en una línea de contrato está configurado en **No**, la pestaña **Categorías facturables** no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="763b9-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="763b9-121">Actualizar una tarea del proyecto como facturable o no facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="763b9-122">Una tarea de proyecto puede ser facturable o no facturable en una línea de contrato específica, lo que hace posible la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="763b9-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="763b9-123">Si una línea de contrato basada en proyecto incluye **Tiempo** y una determinada tarea, **T1** está asociado como facturable.</span><span class="sxs-lookup"><span data-stu-id="763b9-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="763b9-124">Si hay una segunda línea de contrato que incluye **Gastos**, puede asociar la tarea T1 en la línea de contrato como no imputable.</span><span class="sxs-lookup"><span data-stu-id="763b9-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="763b9-125">El resultado es que todo el tiempo registrado en la tarea es imputable y todos los gastos no son imputables.</span><span class="sxs-lookup"><span data-stu-id="763b9-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="763b9-126">El tipo de facturación de una tarea se puede configurar en la pestaña **Tareas con cargo** de la línea de contrato actualizando el campo **Tipo de facturación** en la subcuadrícula de tareas de la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="763b9-127">Alternativamente, puede actualizar el campo **Tipo de facturación** en la subcuadrícula de la tarea Configuración de facturación de un proyecto que muestra las líneas de contrato asociadas a una tarea.</span><span class="sxs-lookup"><span data-stu-id="763b9-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="763b9-128">Actualizar un rol como facturable o no facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="763b9-129">Un rol puede ser facturable o no facturable en una línea de contrato específica.</span><span class="sxs-lookup"><span data-stu-id="763b9-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="763b9-130">El tipo de facturación de un rol se puede configurar en la pestaña **Roles imputables** de una línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="763b9-131">Para hacer esto, actualice el campo **Tipo de facturación** en la subcuadrícula **Funciones imputables**.</span><span class="sxs-lookup"><span data-stu-id="763b9-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="763b9-132">Actualizar una categoría de transacción como facturable o no facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="763b9-133">Una categoría de transacción puede ser facturable o no facturable en una línea de contrato específica.</span><span class="sxs-lookup"><span data-stu-id="763b9-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="763b9-134">El tipo de facturación de una transacción se puede configurar en la pestaña **Categorías imputables** de una línea de contrato basada en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="763b9-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="763b9-135">Para hacer esto, actualice el campo **Tipo de facturación** en la subcuadrícula **Categorías imputables**.</span><span class="sxs-lookup"><span data-stu-id="763b9-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="763b9-136">Resolver imputabilidad</span><span class="sxs-lookup"><span data-stu-id="763b9-136">Resolve chargeability</span></span>

<span data-ttu-id="763b9-137">Un cálculo o dato real creado para el tiempo solo se considera imputable si:</span><span class="sxs-lookup"><span data-stu-id="763b9-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="763b9-138">El **Tiempo** se incluye en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="763b9-139">El **Rol** está configurado como imputable en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="763b9-140">Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="763b9-141">Si estas tres cosas son ciertas, la tarea se configura como imputable.</span><span class="sxs-lookup"><span data-stu-id="763b9-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="763b9-142">Un cálculo o dato real creado para el gasto solo se considera imputable si:</span><span class="sxs-lookup"><span data-stu-id="763b9-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="763b9-143">El **Gasto** se incluye en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="763b9-144">La **Categoría de transacción** está configurada como imputable en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="763b9-145">Las **Tareas incluidas** se establecen en **Tarea seleccionada** en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="763b9-146">Si estas tres cosas son ciertas, la **Tarea** se configura como imputable.</span><span class="sxs-lookup"><span data-stu-id="763b9-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="763b9-147">Un cálculo o dato real creado para el material solo se considera imputable si:</span><span class="sxs-lookup"><span data-stu-id="763b9-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="763b9-148">Los **Materiales** se incluye en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="763b9-149">Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="763b9-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="763b9-150">Si estas dos cosas son ciertas, la **Tarea** se configura como imputable.</span><span class="sxs-lookup"><span data-stu-id="763b9-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="763b9-151">
                    <strong>Incluye tiempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="763b9-152">
                    <strong>Incluye gasto</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="763b9-153">
                    <strong>Incluye materiales</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="763b9-154">
                    <strong>Tareas incluidas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-155">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="763b9-156">
                    <strong>Categoría</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-157">
                    <strong>Tarea</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="763b9-158">
                    <strong>Impacto de imputabilidad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-159">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-160">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-161">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-162">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="763b9-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-163">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-164">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-165">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-166">Facturación a tiempo real: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-167">Tipo de facturación en gastos reales: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-168">Tipo de facturación en material real: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-169">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-170">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-171">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-172">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="763b9-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-173">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-174">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-175">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-176">Facturación a tiempo real: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-177">Tipo de facturación en gastos reales: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-178">Tipo de facturación en material real: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-179">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-180">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-181">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-182">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="763b9-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-183">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-184">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-185">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-186">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-187">Tipo de facturación en gastos actuales: Facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="763b9-188">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-189">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-190">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-191">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-192">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="763b9-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-193">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-194">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-195">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-196">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-197">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-198">Tipo de facturación en material real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-199">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-200">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-201">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-202">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="763b9-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-203">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-204">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-205">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-206">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-207">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-208">Tipo de facturación en material real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-209">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-210">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-211">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-212">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="763b9-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-213">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="763b9-214">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-215">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-216">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-217">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-218">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="763b9-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-220">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-221">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-222">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="763b9-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-223">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="763b9-224">
                    <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-225">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-226">Facturación a tiempo real: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-227">Tipo de facturación en gastos actuales: Facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="763b9-228">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="763b9-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-230">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-231">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-232">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="763b9-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-233">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="763b9-234">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-235">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-236">Facturación a tiempo real: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-237">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-238">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-239">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="763b9-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-241">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-242">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="763b9-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-243">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-244">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-245">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-246">Facturación a tiempo real: Facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="763b9-247">Tipo de facturación en gastos reales: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-248">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-249">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="763b9-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="763b9-251">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-252">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="763b9-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-253">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-254">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-255">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-256">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-257">Tipo de facturación en gastos reales: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-258">Tipo de facturación en material real: Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-259">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-260">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="763b9-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-262">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="763b9-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-263">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-264">Imputable</span><span class="sxs-lookup"><span data-stu-id="763b9-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-265">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-266">Facturación a tiempo real: Facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="763b9-267">Tipo de facturación en gastos actuales: Facturable</span><span class="sxs-lookup"><span data-stu-id="763b9-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="763b9-268">Tipo de facturación en material real: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="763b9-269">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="763b9-270">Sí</span><span class="sxs-lookup"><span data-stu-id="763b9-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="763b9-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="763b9-272">Proyecto entero</span><span class="sxs-lookup"><span data-stu-id="763b9-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="763b9-273">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="763b9-274">
                    <strong>No facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="763b9-275">No puede estar establecido</span><span class="sxs-lookup"><span data-stu-id="763b9-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="763b9-276">Facturación a tiempo real: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-277">Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="763b9-278">Tipo de facturación en material real: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="763b9-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
