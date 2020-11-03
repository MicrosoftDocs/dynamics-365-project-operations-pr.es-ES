---
title: Datos reales
description: Este tema proporciona información sobre cómo trabajar con datos reales en Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085138"
---
# <a name="actuals"></a><span data-ttu-id="eb694-103">Datos reales</span><span class="sxs-lookup"><span data-stu-id="eb694-103">Actuals</span></span> 

<span data-ttu-id="eb694-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos en existencias_</span><span class="sxs-lookup"><span data-stu-id="eb694-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eb694-105">Los datos reales son la cantidad de trabajo que se ha completado en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="eb694-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="eb694-106">Se crean como resultado de movimientos de tiempo y gastos, movimientos de diario y facturas.</span><span class="sxs-lookup"><span data-stu-id="eb694-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="eb694-107">Envío de líneas de diario y tiempo</span><span class="sxs-lookup"><span data-stu-id="eb694-107">Journal lines and time submission</span></span>

<span data-ttu-id="eb694-108">Para obtener más información sobre movimientos de tiempo, consulte [Resumen de movimientos de tiempo](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eb694-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="eb694-109">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="eb694-109">Time and materials</span></span>

<span data-ttu-id="eb694-110">Cuando una entrada de tiempo que se envía está vinculada a un proyecto asignado a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.</span><span class="sxs-lookup"><span data-stu-id="eb694-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="eb694-111">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="eb694-111">Fixed price</span></span>

<span data-ttu-id="eb694-112">Cuando se envía una entrada de tiempo vinculada a un proyecto que está asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="eb694-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="eb694-113">Precios predeterminados</span><span class="sxs-lookup"><span data-stu-id="eb694-113">Default pricing</span></span>

<span data-ttu-id="eb694-114">La lógica para crear precios predeterminados se encuentra en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="eb694-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="eb694-115">Los valores de campo de la entrada de tiempo se copian a la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="eb694-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="eb694-116">Estos valores incluyen la fecha de la transacción, la línea de contrato a la que está asignado el proyecto y el resultado de la divisa en la lista de precios correspondiente.</span><span class="sxs-lookup"><span data-stu-id="eb694-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="eb694-117">Los campos que afectan a los precios predeterminados, como **Rol** y **Unidad organizativa** , se usan para determinar el precio adecuado en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="eb694-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="eb694-118">Puede agregar un campo personalizado en la entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="eb694-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="eb694-119">Si quiere que el valor de campo se propague a los datos reales, cree el campo en la entidad Datos reales y utilice las asignaciones de campos para copiar el campo de la entrada de teiempo a los datos reales.</span><span class="sxs-lookup"><span data-stu-id="eb694-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="eb694-120">Envío de líneas de diario y gastos básicos</span><span class="sxs-lookup"><span data-stu-id="eb694-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="eb694-121">Para obtener más información sobre movimientos de gastos, consulte [Resumen de gastos](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eb694-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="eb694-122">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="eb694-122">Time and materials</span></span>

<span data-ttu-id="eb694-123">Cuando una entrada de gasto básico enviada está vinculada a un proyecto asignado a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.</span><span class="sxs-lookup"><span data-stu-id="eb694-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="eb694-124">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="eb694-124">Fixed price</span></span>

<span data-ttu-id="eb694-125">Cuando una entrada de gasto básico enviada está vinculada a un proyecto asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="eb694-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="eb694-126">Precios predeterminados</span><span class="sxs-lookup"><span data-stu-id="eb694-126">Default pricing</span></span>

<span data-ttu-id="eb694-127">La lógica para introducir precios predeterminados para gastos se basa en la categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="eb694-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="eb694-128">La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada.</span><span class="sxs-lookup"><span data-stu-id="eb694-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="eb694-129">Sin embargo, de forma predeteerminada, el importe que se especifica para el propio precio se establece directamente en las líneas de diario de gastos de costes y ventas.</span><span class="sxs-lookup"><span data-stu-id="eb694-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="eb694-130">La entrada según categoría de los precios unitarios predeterminados en las entradas de gastos no está disponible.</span><span class="sxs-lookup"><span data-stu-id="eb694-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="eb694-131">Utilizar diarios de movimientos para registrar costes</span><span class="sxs-lookup"><span data-stu-id="eb694-131">Use entry journals to record costs</span></span>

<span data-ttu-id="eb694-132">Puede usar diarios de movimientos para registrar costes o ingresos en materiales, precios, tiempo, gastos o clases de transacciones de impuestos.</span><span class="sxs-lookup"><span data-stu-id="eb694-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="eb694-133">Los diarios se pueden usar para los siguientes propósitos:</span><span class="sxs-lookup"><span data-stu-id="eb694-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="eb694-134">Registrar el coste real de materiales y ventas de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="eb694-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="eb694-135">Mover datos reales de transacciones de otro sistema a Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="eb694-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="eb694-136">Registrar cotes que ocurrieron en otro sistema.</span><span class="sxs-lookup"><span data-stu-id="eb694-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="eb694-137">Estos costes pueden incluir costes de adquisición o subcontratación.</span><span class="sxs-lookup"><span data-stu-id="eb694-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb694-138">La aplicación no valida el tipo de línea del diario ni el precio relacionado que se introduce en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="eb694-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="eb694-139">Por lo tanto, solo un usuario que sea plenamente consciente del impacto contable que tienen los datos reales en el proyecto debe utilizar los diarios de movimientos para crear los datos reales.</span><span class="sxs-lookup"><span data-stu-id="eb694-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="eb694-140">Debido al impacto de este tipo de diario, debe elegir cuidadosamente quién tiene acceso a crear diarios de movimientos.</span><span class="sxs-lookup"><span data-stu-id="eb694-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="eb694-141">Registrar datos reales basados en eventos de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-141">Record actuals based on project events</span></span>

<span data-ttu-id="eb694-142">Project Operations registra las transacciones financieras que se producen durante un proyecto.</span><span class="sxs-lookup"><span data-stu-id="eb694-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="eb694-143">Estas transacciones se registran como datos reales.</span><span class="sxs-lookup"><span data-stu-id="eb694-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="eb694-144">Las siguientes tablas muestran los diferentes tipos de datos reales que se crean dependiendo de si el proyecto es un proyecto de tiempo y materiales o de precio fijo, de si se encuentra en fase de preventas o de si se trata de un proyecto interno.</span><span class="sxs-lookup"><span data-stu-id="eb694-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="eb694-145">El recurso pertenece a la misma unidad organizativa que la unidad de contratación del proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="eb694-146">Evento</span><span class="sxs-lookup"><span data-stu-id="eb694-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="eb694-147">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="eb694-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="eb694-148">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="eb694-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="eb694-149">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="eb694-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="eb694-150">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="eb694-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="eb694-151">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="eb694-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="eb694-152">Datos reales</span><span class="sxs-lookup"><span data-stu-id="eb694-152">Actuals</span></span></th>
<th><span data-ttu-id="eb694-153">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="eb694-153">Transaction currency</span></span></th>
<th><span data-ttu-id="eb694-154">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="eb694-154">Fixed price</span></span></th>
<th><span data-ttu-id="eb694-155">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="eb694-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eb694-156">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="eb694-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="eb694-157">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="eb694-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-158">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="eb694-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="eb694-159">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="eb694-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="eb694-160">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="eb694-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="eb694-161">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-161">Cost actual</span></span></td>
<td><span data-ttu-id="eb694-162">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-163">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-164">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="eb694-165">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-166">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-167">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="eb694-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="eb694-168">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb694-169">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="eb694-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="eb694-170">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-170">Cost actual</span></span></td>
<td><span data-ttu-id="eb694-171">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-172">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-173">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-174">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-175">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-176">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="eb694-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="eb694-177">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-178">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="eb694-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="eb694-179">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="eb694-180">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="eb694-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="eb694-181">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="eb694-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="eb694-182">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-183">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="eb694-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-184">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-185">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-186">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-187">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="eb694-187">Billed sales</span></span></td>
<td><span data-ttu-id="eb694-188">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb694-189">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="eb694-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="eb694-190">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="eb694-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="eb694-191">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-192">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-193">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-194">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-195">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-196">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="eb694-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="eb694-197">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-198">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="eb694-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="eb694-199">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="eb694-200">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="eb694-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="eb694-201">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="eb694-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="eb694-202">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="eb694-203">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="eb694-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="eb694-204">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="eb694-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="eb694-205">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="eb694-206">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="eb694-207">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-208">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="eb694-208">Billed sales</span></span></td>
<td><span data-ttu-id="eb694-209">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb694-210">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="eb694-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="eb694-211">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="eb694-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="eb694-212">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-213">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="eb694-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="eb694-214">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-215">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="eb694-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="eb694-216">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="eb694-217">El recurso pertenece a una unidad organizativa distinta de la unidad de contratación del proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="eb694-218">Evento</span><span class="sxs-lookup"><span data-stu-id="eb694-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="eb694-219">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="eb694-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="eb694-220">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="eb694-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="eb694-221">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="eb694-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="eb694-222">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="eb694-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="eb694-223">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="eb694-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="eb694-224">Datos reales</span><span class="sxs-lookup"><span data-stu-id="eb694-224">Actuals</span></span></th>
<th><span data-ttu-id="eb694-225">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="eb694-225">Transaction currency</span></span></th>
<th><span data-ttu-id="eb694-226">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="eb694-226">Fixed price</span></span></th>
<th><span data-ttu-id="eb694-227">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="eb694-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eb694-228">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="eb694-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="eb694-229">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="eb694-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-230">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="eb694-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="eb694-231">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="eb694-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="eb694-232">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="eb694-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="eb694-233">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-233">Cost actual</span></span></td>
<td><span data-ttu-id="eb694-234">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="eb694-235">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="eb694-236">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="eb694-237">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="eb694-238">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-239">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="eb694-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="eb694-240">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-241">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="eb694-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="eb694-242">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="eb694-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-243">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="eb694-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="eb694-244">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="eb694-245">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="eb694-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="eb694-246">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-246">Cost actual</span></span></td>
<td><span data-ttu-id="eb694-247">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="eb694-248">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="eb694-249">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="eb694-250">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="eb694-251">Coste real</span><span class="sxs-lookup"><span data-stu-id="eb694-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-252">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="eb694-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="eb694-253">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="eb694-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-254">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="eb694-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="eb694-255">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="eb694-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-256">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="eb694-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="eb694-257">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-258">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="eb694-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="eb694-259">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="eb694-260">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="eb694-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="eb694-261">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="eb694-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="eb694-262">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-263">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="eb694-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-264">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-265">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="eb694-266">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-267">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="eb694-267">Billed sales</span></span></td>
<td><span data-ttu-id="eb694-268">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb694-269">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="eb694-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="eb694-270">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="eb694-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="eb694-271">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-272">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-273">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-274">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="eb694-275">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-276">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="eb694-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="eb694-277">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-278">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="eb694-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="eb694-279">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="eb694-280">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="eb694-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="eb694-281">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="eb694-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="eb694-282">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="eb694-283">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="eb694-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="eb694-284">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="eb694-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="eb694-285">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="eb694-286">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="eb694-287">No disponible</span><span class="sxs-lookup"><span data-stu-id="eb694-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-288">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="eb694-288">Billed sales</span></span></td>
<td><span data-ttu-id="eb694-289">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb694-290">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="eb694-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="eb694-291">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="eb694-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="eb694-292">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-293">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="eb694-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="eb694-294">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb694-295">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="eb694-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="eb694-296">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="eb694-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
