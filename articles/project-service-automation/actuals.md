---
title: Datos reales
description: En este tema se proporciona información sobre datos reales del proyecto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756068"
---
# <a name="actuals"></a><span data-ttu-id="a9ae1-103">Datos reales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a9ae1-104">Los datos reales son la cantidad de trabajo que se ha completado en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="a9ae1-105">Es posible rastrear los datos reales del proyecto hasta sus documentos de origen.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="a9ae1-106">Dichos documentos de origen incluyen datos sobre el tiempo, el gasto, los movimientos de diario y también las facturas.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cómo se rastrean los datos reales del proyecto hasta los documentos de origen](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="a9ae1-108">Envío de una entrada de hora</span><span class="sxs-lookup"><span data-stu-id="a9ae1-108">Submitting a time entry</span></span>

<span data-ttu-id="a9ae1-109">En PSA, cuando se envía una entrada de hora para un proyecto que está asignado a una línea de contrato de tiempo y materiales, se crean dos líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a9ae1-110">Una línea es para el coste y la otra es para las ventas sin facturar.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a9ae1-111">Cuando se envía una entrada de hora para un proyecto que está asignado a una línea de contrato de precio fijo, solo se crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="a9ae1-112">La lógica para especificar precios predeterminados se encuentra en la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="a9ae1-113">Todos los valores de campo de una entrada de hora se copian a la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="a9ae1-114">Estos campos incluyen la fecha de la transacción, la línea de contrato a la que está asignado el proyecto y el resultado de la divisa en la lista de precios correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="a9ae1-115">Los campos que afectan a los precios predeterminados, como, por ejemplo, **Rol** y **Unidad organizativa**, hacen que se especifique el precio adecuado de manera predeterminada en la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="a9ae1-116">Si agrega un campo personalizado en la entrada de hora y desea que el valor de campo se propague a los datos reales, cree el campo en la entidad Datos reales y utilice las asignaciones de campos para copiar el campo de la entrada de hora a los datos reales.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="a9ae1-117">Envío de una entrada de gastos</span><span class="sxs-lookup"><span data-stu-id="a9ae1-117">Submitting an expense entry</span></span>

<span data-ttu-id="a9ae1-118">En PSA, cuando se envía una entrada de gastos para un proyecto que está asignado a una línea de contrato de tiempo y materiales, se crean dos líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a9ae1-119">Una línea es para el coste y la otra es para las ventas sin facturar.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a9ae1-120">Cuando se envía una entrada de gastos para un proyecto que está asignado a una línea de contrato de precio fijo, solo se crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="a9ae1-121">La lógica para especificar los precios predeterminados para los gastos se basa en la categoría de gastos seleccionada en la página **Entrada de gastos**.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="a9ae1-122">La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a9ae1-123">Sin embargo, para el precio sí mismo, el importe que especifica el usuario se establece directamente en las líneas de diario de gastos de costes y ventas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="a9ae1-124">En la versión actual de PSA, la especificación de precios predeterminados por entrada según la categoría en las entradas de gastos no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="a9ae1-125">Utilización de diarios para registrar costes</span><span class="sxs-lookup"><span data-stu-id="a9ae1-125">Using journals to record costs</span></span>

<span data-ttu-id="a9ae1-126">En PSA, los diarios permiten registrar costes o ingresos en las clases de materiales, cuotas, gastos o transacciones de impuestos.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a9ae1-127">Los diarios disponen de encabezado, líneas y la acción **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="a9ae1-128">Estos son algunas escenarios en los que puede utilizar un diario:</span><span class="sxs-lookup"><span data-stu-id="a9ae1-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="a9ae1-129">Debe registrar ventas y costes reales de materiales en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="a9ae1-130">Debe mover datos reales de transacciones de otro sistema a PSA.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="a9ae1-131">Debe registrar los costes que se han producido en otro sistema, como, por ejemplo, los costes de adquisición o subcontratación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="a9ae1-132">Registro de datos reales basados en eventos de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-132">Recording actuals based on project events</span></span>

<span data-ttu-id="a9ae1-133">El PSA registra las transacciones financieras que se producen durante un proyecto.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a9ae1-134">Estas transacciones se registran como **datos reales**.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="a9ae1-135">Las siguientes tablas muestran los diferentes tipos de datos reales que se crean dependiendo de si el proyecto es un proyecto de tiempo y materiales o de precio fijo, de si se encuentra en fase de preventas o de si se trata de un proyecto interno.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="a9ae1-136">**El recurso pertenece a la misma unidad organizativa que la unidad de contratación del proyecto**</span><span class="sxs-lookup"><span data-stu-id="a9ae1-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a9ae1-137">Evento</span><span class="sxs-lookup"><span data-stu-id="a9ae1-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a9ae1-138">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="a9ae1-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a9ae1-139">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="a9ae1-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a9ae1-140">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="a9ae1-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a9ae1-141">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a9ae1-142">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="a9ae1-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a9ae1-143">Datos reales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-143">Actuals</span></span></th>
<th><span data-ttu-id="a9ae1-144">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="a9ae1-144">Transaction currency</span></span></th>
<th><span data-ttu-id="a9ae1-145">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="a9ae1-145">Fixed price</span></span></th>
<th><span data-ttu-id="a9ae1-146">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="a9ae1-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a9ae1-147">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a9ae1-148">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-149">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a9ae1-150">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a9ae1-151">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a9ae1-152">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-152">Cost actual</span></span></td>
<td><span data-ttu-id="a9ae1-153">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-154">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-155">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a9ae1-156">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-157">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-158">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="a9ae1-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a9ae1-159">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9ae1-160">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a9ae1-161">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-161">Cost actual</span></span></td>
<td><span data-ttu-id="a9ae1-162">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-163">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-164">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-165">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-166">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-167">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="a9ae1-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a9ae1-168">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-169">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="a9ae1-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a9ae1-170">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a9ae1-171">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a9ae1-172">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="a9ae1-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a9ae1-173">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-174">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="a9ae1-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-175">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-176">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-177">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-178">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="a9ae1-178">Billed sales</span></span></td>
<td><span data-ttu-id="a9ae1-179">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9ae1-180">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a9ae1-181">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="a9ae1-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a9ae1-182">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-183">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-184">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-185">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-186">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-187">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="a9ae1-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a9ae1-188">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-189">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="a9ae1-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a9ae1-190">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a9ae1-191">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a9ae1-192">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="a9ae1-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a9ae1-193">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a9ae1-194">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="a9ae1-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a9ae1-195">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="a9ae1-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a9ae1-196">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a9ae1-197">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a9ae1-198">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-199">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="a9ae1-199">Billed sales</span></span></td>
<td><span data-ttu-id="a9ae1-200">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9ae1-201">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a9ae1-202">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="a9ae1-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a9ae1-203">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-204">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="a9ae1-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a9ae1-205">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-206">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="a9ae1-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a9ae1-207">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a9ae1-208">**El recurso pertenece a una unidad organizativa distinta de la unidad de contratación del proyecto**</span><span class="sxs-lookup"><span data-stu-id="a9ae1-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a9ae1-209">Evento</span><span class="sxs-lookup"><span data-stu-id="a9ae1-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a9ae1-210">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="a9ae1-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a9ae1-211">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="a9ae1-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a9ae1-212">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="a9ae1-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a9ae1-213">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a9ae1-214">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="a9ae1-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a9ae1-215">Datos reales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-215">Actuals</span></span></th>
<th><span data-ttu-id="a9ae1-216">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="a9ae1-216">Transaction currency</span></span></th>
<th><span data-ttu-id="a9ae1-217">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="a9ae1-217">Fixed price</span></span></th>
<th><span data-ttu-id="a9ae1-218">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="a9ae1-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a9ae1-219">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a9ae1-220">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-221">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a9ae1-222">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="a9ae1-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a9ae1-223">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a9ae1-224">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-224">Cost actual</span></span></td>
<td><span data-ttu-id="a9ae1-225">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a9ae1-226">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a9ae1-227">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a9ae1-228">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a9ae1-229">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-230">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="a9ae1-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a9ae1-231">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-232">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="a9ae1-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a9ae1-233">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="a9ae1-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-234">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="a9ae1-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a9ae1-235">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a9ae1-236">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a9ae1-237">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-237">Cost actual</span></span></td>
<td><span data-ttu-id="a9ae1-238">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a9ae1-239">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a9ae1-240">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a9ae1-241">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a9ae1-242">Coste real</span><span class="sxs-lookup"><span data-stu-id="a9ae1-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-243">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="a9ae1-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a9ae1-244">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="a9ae1-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-245">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="a9ae1-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a9ae1-246">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="a9ae1-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-247">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="a9ae1-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a9ae1-248">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-249">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="a9ae1-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a9ae1-250">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a9ae1-251">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a9ae1-252">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="a9ae1-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a9ae1-253">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-254">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="a9ae1-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-255">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-256">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a9ae1-257">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-258">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="a9ae1-258">Billed sales</span></span></td>
<td><span data-ttu-id="a9ae1-259">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9ae1-260">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a9ae1-261">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="a9ae1-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a9ae1-262">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-263">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-264">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-265">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a9ae1-266">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-267">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="a9ae1-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a9ae1-268">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-269">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="a9ae1-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a9ae1-270">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a9ae1-271">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a9ae1-272">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="a9ae1-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a9ae1-273">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a9ae1-274">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="a9ae1-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a9ae1-275">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="a9ae1-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a9ae1-276">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a9ae1-277">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a9ae1-278">No disponible</span><span class="sxs-lookup"><span data-stu-id="a9ae1-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-279">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="a9ae1-279">Billed sales</span></span></td>
<td><span data-ttu-id="a9ae1-280">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a9ae1-281">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="a9ae1-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a9ae1-282">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="a9ae1-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a9ae1-283">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-284">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="a9ae1-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a9ae1-285">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9ae1-286">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="a9ae1-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a9ae1-287">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="a9ae1-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
