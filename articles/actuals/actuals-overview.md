---
title: Página principal de datos reales
description: Este tema proporciona información sobre cómo trabajar con datos reales en Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907339"
---
# <a name="actuals"></a><span data-ttu-id="246f9-103">Datos reales</span><span class="sxs-lookup"><span data-stu-id="246f9-103">Actuals</span></span>

<span data-ttu-id="246f9-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos en existencias_</span><span class="sxs-lookup"><span data-stu-id="246f9-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="246f9-105">Los datos reales son la cantidad de trabajo que se ha completado en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="246f9-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="246f9-106">Se crean como resultado de movimientos de tiempo y gastos, movimientos de diario y facturas.</span><span class="sxs-lookup"><span data-stu-id="246f9-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="246f9-107">Envío de líneas de diario y tiempo</span><span class="sxs-lookup"><span data-stu-id="246f9-107">Journal lines and time submission</span></span>

<span data-ttu-id="246f9-108">Para obtener más información sobre movimientos de tiempo, consulte [Resumen de movimientos de tiempo](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="246f9-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="246f9-109">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="246f9-109">Time and materials</span></span>

<span data-ttu-id="246f9-110">Cuando una entrada de tiempo que se envía está vinculada a un proyecto asignado a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.</span><span class="sxs-lookup"><span data-stu-id="246f9-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="246f9-111">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="246f9-111">Fixed price</span></span>

<span data-ttu-id="246f9-112">Cuando se envía una entrada de tiempo vinculada a un proyecto que está asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="246f9-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="246f9-113">Precios predeterminados</span><span class="sxs-lookup"><span data-stu-id="246f9-113">Default pricing</span></span>

<span data-ttu-id="246f9-114">La lógica para crear precios predeterminados se encuentra en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="246f9-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="246f9-115">Los valores de campo de la entrada de tiempo se copian a la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="246f9-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="246f9-116">Estos valores incluyen la fecha de la transacción, la línea de contrato a la que está asignado el proyecto y el resultado de la divisa en la lista de precios correspondiente.</span><span class="sxs-lookup"><span data-stu-id="246f9-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="246f9-117">Los campos que afectan a los precios predeterminados, como **Rol** y **Unidad organizativa**, se usan para determinar el precio adecuado en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="246f9-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="246f9-118">Puede agregar un campo personalizado en la entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="246f9-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="246f9-119">Si quiere que el valor de campo se propague a los datos reales, cree el campo en la entidad Datos reales y utilice las asignaciones de campos para copiar el campo de la entrada de teiempo a los datos reales.</span><span class="sxs-lookup"><span data-stu-id="246f9-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="246f9-120">Envío de líneas de diario y gastos básicos</span><span class="sxs-lookup"><span data-stu-id="246f9-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="246f9-121">Para obtener más información sobre movimientos de gastos, consulte [Resumen de gastos](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="246f9-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="246f9-122">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="246f9-122">Time and materials</span></span>

<span data-ttu-id="246f9-123">Cuando una entrada de gasto básico enviada está vinculada a un proyecto asignado a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.</span><span class="sxs-lookup"><span data-stu-id="246f9-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="246f9-124">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="246f9-124">Fixed price</span></span>

<span data-ttu-id="246f9-125">Cuando una entrada de gasto básico enviada está vinculada a un proyecto asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="246f9-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="246f9-126">Precios predeterminados</span><span class="sxs-lookup"><span data-stu-id="246f9-126">Default pricing</span></span>

<span data-ttu-id="246f9-127">La lógica para introducir precios predeterminados para gastos se basa en la categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="246f9-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="246f9-128">La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada.</span><span class="sxs-lookup"><span data-stu-id="246f9-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="246f9-129">Sin embargo, de forma predeteerminada, el importe que se especifica para el propio precio se establece directamente en las líneas de diario de gastos de costes y ventas.</span><span class="sxs-lookup"><span data-stu-id="246f9-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="246f9-130">La entrada según categoría de los precios unitarios predeterminados en las entradas de gastos no está disponible.</span><span class="sxs-lookup"><span data-stu-id="246f9-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="246f9-131">Utilizar diarios de movimientos para registrar costes</span><span class="sxs-lookup"><span data-stu-id="246f9-131">Use entry journals to record costs</span></span>

<span data-ttu-id="246f9-132">Puede usar diarios de movimientos para registrar costes o ingresos en materiales, precios, tiempo, gastos o clases de transacciones de impuestos.</span><span class="sxs-lookup"><span data-stu-id="246f9-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="246f9-133">Los diarios se pueden usar para los siguientes propósitos:</span><span class="sxs-lookup"><span data-stu-id="246f9-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="246f9-134">Registrar el coste real de materiales y ventas de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="246f9-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="246f9-135">Mover datos reales de transacciones de otro sistema a Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="246f9-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="246f9-136">Registrar cotes que ocurrieron en otro sistema.</span><span class="sxs-lookup"><span data-stu-id="246f9-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="246f9-137">Estos costes pueden incluir costes de adquisición o subcontratación.</span><span class="sxs-lookup"><span data-stu-id="246f9-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="246f9-138">La aplicación no valida el tipo de línea del diario ni el precio relacionado que se introduce en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="246f9-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="246f9-139">Por lo tanto, solo un usuario que sea plenamente consciente del impacto contable que tienen los datos reales en el proyecto debe utilizar los diarios de movimientos para crear los datos reales.</span><span class="sxs-lookup"><span data-stu-id="246f9-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="246f9-140">Debido al impacto de este tipo de diario, debe elegir cuidadosamente quién tiene acceso a crear diarios de movimientos.</span><span class="sxs-lookup"><span data-stu-id="246f9-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="246f9-141">Registrar datos reales basados en eventos de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-141">Record actuals based on project events</span></span>

<span data-ttu-id="246f9-142">Project Operations registra las transacciones financieras que se producen durante un proyecto.</span><span class="sxs-lookup"><span data-stu-id="246f9-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="246f9-143">Estas transacciones se registran como datos reales.</span><span class="sxs-lookup"><span data-stu-id="246f9-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="246f9-144">Las siguientes tablas muestran los diferentes tipos de datos reales que se crean dependiendo de si el proyecto es un proyecto de tiempo y materiales o de precio fijo, de si se encuentra en fase de preventas o de si se trata de un proyecto interno.</span><span class="sxs-lookup"><span data-stu-id="246f9-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="246f9-145">El recurso pertenece a la misma unidad organizativa que la unidad de contratación del proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="246f9-146">Evento</span><span class="sxs-lookup"><span data-stu-id="246f9-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="246f9-147">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="246f9-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="246f9-148">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="246f9-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="246f9-149">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="246f9-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="246f9-150">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="246f9-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="246f9-151">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="246f9-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="246f9-152">Datos reales</span><span class="sxs-lookup"><span data-stu-id="246f9-152">Actuals</span></span></th>
<th><span data-ttu-id="246f9-153">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="246f9-153">Transaction currency</span></span></th>
<th><span data-ttu-id="246f9-154">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="246f9-154">Fixed price</span></span></th>
<th><span data-ttu-id="246f9-155">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="246f9-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="246f9-156">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="246f9-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="246f9-157">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="246f9-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-158">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="246f9-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="246f9-159">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="246f9-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="246f9-160">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="246f9-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="246f9-161">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-161">Cost actual</span></span></td>
<td><span data-ttu-id="246f9-162">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-163">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-164">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="246f9-165">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-166">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-167">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="246f9-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="246f9-168">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="246f9-169">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="246f9-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="246f9-170">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-170">Cost actual</span></span></td>
<td><span data-ttu-id="246f9-171">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-172">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-173">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-174">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-175">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-176">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="246f9-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="246f9-177">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-178">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="246f9-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="246f9-179">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="246f9-180">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="246f9-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="246f9-181">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="246f9-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="246f9-182">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-183">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="246f9-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-184">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-185">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-186">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-187">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="246f9-187">Billed sales</span></span></td>
<td><span data-ttu-id="246f9-188">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="246f9-189">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="246f9-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="246f9-190">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="246f9-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="246f9-191">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-192">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-193">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-194">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-195">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-196">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="246f9-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="246f9-197">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-198">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="246f9-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="246f9-199">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="246f9-200">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="246f9-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="246f9-201">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="246f9-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="246f9-202">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="246f9-203">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="246f9-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="246f9-204">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="246f9-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="246f9-205">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="246f9-206">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="246f9-207">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-208">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="246f9-208">Billed sales</span></span></td>
<td><span data-ttu-id="246f9-209">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="246f9-210">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="246f9-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="246f9-211">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="246f9-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="246f9-212">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-213">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="246f9-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="246f9-214">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-215">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="246f9-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="246f9-216">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="246f9-217">El recurso pertenece a una unidad organizativa distinta de la unidad de contratación del proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="246f9-218">Evento</span><span class="sxs-lookup"><span data-stu-id="246f9-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="246f9-219">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="246f9-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="246f9-220">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="246f9-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="246f9-221">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="246f9-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="246f9-222">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="246f9-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="246f9-223">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="246f9-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="246f9-224">Datos reales</span><span class="sxs-lookup"><span data-stu-id="246f9-224">Actuals</span></span></th>
<th><span data-ttu-id="246f9-225">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="246f9-225">Transaction currency</span></span></th>
<th><span data-ttu-id="246f9-226">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="246f9-226">Fixed price</span></span></th>
<th><span data-ttu-id="246f9-227">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="246f9-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="246f9-228">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="246f9-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="246f9-229">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="246f9-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-230">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="246f9-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="246f9-231">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="246f9-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="246f9-232">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="246f9-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="246f9-233">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-233">Cost actual</span></span></td>
<td><span data-ttu-id="246f9-234">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="246f9-235">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="246f9-236">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="246f9-237">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="246f9-238">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-239">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="246f9-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="246f9-240">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-241">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="246f9-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="246f9-242">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="246f9-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-243">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="246f9-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="246f9-244">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="246f9-245">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="246f9-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="246f9-246">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-246">Cost actual</span></span></td>
<td><span data-ttu-id="246f9-247">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="246f9-248">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="246f9-249">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="246f9-250">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="246f9-251">Coste real</span><span class="sxs-lookup"><span data-stu-id="246f9-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-252">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="246f9-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="246f9-253">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="246f9-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-254">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="246f9-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="246f9-255">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="246f9-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-256">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="246f9-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="246f9-257">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-258">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="246f9-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="246f9-259">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="246f9-260">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="246f9-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="246f9-261">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="246f9-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="246f9-262">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-263">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="246f9-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-264">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-265">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="246f9-266">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-267">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="246f9-267">Billed sales</span></span></td>
<td><span data-ttu-id="246f9-268">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="246f9-269">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="246f9-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="246f9-270">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="246f9-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="246f9-271">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-272">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-273">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-274">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="246f9-275">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-276">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="246f9-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="246f9-277">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-278">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="246f9-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="246f9-279">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="246f9-280">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="246f9-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="246f9-281">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="246f9-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="246f9-282">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="246f9-283">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="246f9-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="246f9-284">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="246f9-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="246f9-285">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="246f9-286">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="246f9-287">No disponible</span><span class="sxs-lookup"><span data-stu-id="246f9-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-288">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="246f9-288">Billed sales</span></span></td>
<td><span data-ttu-id="246f9-289">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="246f9-290">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="246f9-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="246f9-291">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="246f9-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="246f9-292">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-293">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="246f9-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="246f9-294">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="246f9-295">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="246f9-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="246f9-296">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="246f9-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
