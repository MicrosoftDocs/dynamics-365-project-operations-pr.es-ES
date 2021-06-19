---
title: Información general de datos reales
description: En este tema se proporciona información sobre datos reales del proyecto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014677"
---
# <a name="actuals-overview"></a><span data-ttu-id="0f659-103">Información general de datos reales</span><span class="sxs-lookup"><span data-stu-id="0f659-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0f659-104">Los datos reales son la cantidad de trabajo que se ha completado en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="0f659-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0f659-105">Es posible rastrear los datos reales del proyecto hasta sus documentos de origen.</span><span class="sxs-lookup"><span data-stu-id="0f659-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="0f659-106">Dichos documentos de origen incluyen datos sobre el tiempo, el gasto, los movimientos de diario y también las facturas.</span><span class="sxs-lookup"><span data-stu-id="0f659-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cómo se rastrean los datos reales del proyecto hasta los documentos de origen](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="0f659-108">Envío de una entrada de hora</span><span class="sxs-lookup"><span data-stu-id="0f659-108">Submitting a time entry</span></span>

<span data-ttu-id="0f659-109">En PSA, cuando se envía una entrada de hora para un proyecto que está asignado a una línea de contrato de tiempo y materiales, se crean dos líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="0f659-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0f659-110">Una línea es para el coste y la otra es para las ventas sin facturar.</span><span class="sxs-lookup"><span data-stu-id="0f659-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0f659-111">Cuando se envía una entrada de hora para un proyecto que está asignado a una línea de contrato de precio fijo, solo se crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="0f659-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="0f659-112">La lógica para especificar precios predeterminados se encuentra en la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="0f659-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="0f659-113">Todos los valores de campo de una entrada de hora se copian a la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="0f659-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="0f659-114">Estos campos incluyen la fecha de la transacción, la línea de contrato a la que está asignado el proyecto y el resultado de la divisa en la lista de precios correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0f659-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="0f659-115">Los campos que afectan a los precios predeterminados, como, por ejemplo, **Rol** y **Unidad organizativa**, hacen que se especifique el precio adecuado de manera predeterminada en la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="0f659-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="0f659-116">Si agrega un campo personalizado en la entrada de hora y desea que el valor de campo se propague a los datos reales, cree el campo en la entidad Datos reales y utilice las asignaciones de campos para copiar el campo de la entrada de hora a los datos reales.</span><span class="sxs-lookup"><span data-stu-id="0f659-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="0f659-117">Envío de una entrada de gastos</span><span class="sxs-lookup"><span data-stu-id="0f659-117">Submitting an expense entry</span></span>

<span data-ttu-id="0f659-118">En PSA, cuando se envía una entrada de gastos para un proyecto que está asignado a una línea de contrato de tiempo y materiales, se crean dos líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="0f659-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0f659-119">Una línea es para el coste y la otra es para las ventas sin facturar.</span><span class="sxs-lookup"><span data-stu-id="0f659-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0f659-120">Cuando se envía una entrada de gastos para un proyecto que está asignado a una línea de contrato de precio fijo, solo se crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="0f659-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="0f659-121">La lógica para especificar los precios predeterminados para los gastos se basa en la categoría de gastos seleccionada en la página **Entrada de gastos**.</span><span class="sxs-lookup"><span data-stu-id="0f659-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="0f659-122">La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada.</span><span class="sxs-lookup"><span data-stu-id="0f659-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0f659-123">Sin embargo, para el precio sí mismo, el importe que especifica el usuario se establece directamente en las líneas de diario de gastos de costes y ventas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0f659-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="0f659-124">En la versión actual de PSA, la especificación de precios predeterminados por entrada según la categoría en las entradas de gastos no está disponible.</span><span class="sxs-lookup"><span data-stu-id="0f659-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="0f659-125">Utilización de diarios de movimientos para registrar costes</span><span class="sxs-lookup"><span data-stu-id="0f659-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="0f659-126">En PSA, los diarios de movimientos permiten registrar el coste o ingreso en las clases de materiales, cuotas, gastos o transacciones de impuestos.</span><span class="sxs-lookup"><span data-stu-id="0f659-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0f659-127">Los diarios disponen de encabezado, líneas y la acción **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="0f659-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="0f659-128">Estos son algunas escenarios en los que puede utilizar un diario:</span><span class="sxs-lookup"><span data-stu-id="0f659-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="0f659-129">Debe registrar ventas y costes reales de materiales en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="0f659-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="0f659-130">Debe mover datos reales de transacciones de otro sistema a PSA.</span><span class="sxs-lookup"><span data-stu-id="0f659-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="0f659-131">Debe registrar los costes que se han producido en otro sistema, como, por ejemplo, los costes de adquisición o subcontratación.</span><span class="sxs-lookup"><span data-stu-id="0f659-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f659-132">Solo un usuario que sea plenamente consciente del impacto contable que tienen los datos reales en el proyecto puede usar diarios de movimientos para crear datos reales.</span><span class="sxs-lookup"><span data-stu-id="0f659-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="0f659-133">Esto se debe a que la aplicación no valida el tipo de línea del diario o el precio relacionado que se ingresa en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="0f659-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="0f659-134">Debido al impacto de este tipo de diario, tenga la debida precaución con respecto a quién tiene acceso para crear diarios de movimientos.</span><span class="sxs-lookup"><span data-stu-id="0f659-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="0f659-135">Registro de datos reales basados en eventos de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-135">Recording actuals based on project events</span></span>

<span data-ttu-id="0f659-136">El PSA registra las transacciones financieras que se producen durante un proyecto.</span><span class="sxs-lookup"><span data-stu-id="0f659-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0f659-137">Estas transacciones se registran como **datos reales**.</span><span class="sxs-lookup"><span data-stu-id="0f659-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="0f659-138">Las siguientes tablas muestran los diferentes tipos de datos reales que se crean dependiendo de si el proyecto es un proyecto de tiempo y materiales o de precio fijo, de si se encuentra en fase de preventas o de si se trata de un proyecto interno.</span><span class="sxs-lookup"><span data-stu-id="0f659-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="0f659-139">**El recurso pertenece a la misma unidad organizativa que la unidad de contratación del proyecto**</span><span class="sxs-lookup"><span data-stu-id="0f659-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0f659-140">Evento</span><span class="sxs-lookup"><span data-stu-id="0f659-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0f659-141">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="0f659-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0f659-142">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="0f659-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0f659-143">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="0f659-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0f659-144">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="0f659-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0f659-145">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="0f659-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0f659-146">Datos reales</span><span class="sxs-lookup"><span data-stu-id="0f659-146">Actuals</span></span></th>
<th><span data-ttu-id="0f659-147">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="0f659-147">Transaction currency</span></span></th>
<th><span data-ttu-id="0f659-148">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="0f659-148">Fixed price</span></span></th>
<th><span data-ttu-id="0f659-149">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="0f659-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f659-150">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="0f659-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0f659-151">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="0f659-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-152">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="0f659-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0f659-153">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="0f659-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f659-154">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0f659-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0f659-155">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-155">Cost actual</span></span></td>
<td><span data-ttu-id="0f659-156">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-157">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-158">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0f659-159">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-160">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-161">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="0f659-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0f659-162">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f659-163">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0f659-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0f659-164">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-164">Cost actual</span></span></td>
<td><span data-ttu-id="0f659-165">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-166">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-167">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-168">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-169">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-170">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="0f659-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0f659-171">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-172">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="0f659-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f659-173">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f659-174">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0f659-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0f659-175">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="0f659-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0f659-176">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-177">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="0f659-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-178">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-179">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-180">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-181">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="0f659-181">Billed sales</span></span></td>
<td><span data-ttu-id="0f659-182">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f659-183">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0f659-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0f659-184">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="0f659-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0f659-185">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-186">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-187">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-188">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-189">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-190">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="0f659-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0f659-191">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-192">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="0f659-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f659-193">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f659-194">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="0f659-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0f659-195">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="0f659-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0f659-196">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0f659-197">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="0f659-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0f659-198">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="0f659-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0f659-199">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0f659-200">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0f659-201">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-202">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="0f659-202">Billed sales</span></span></td>
<td><span data-ttu-id="0f659-203">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f659-204">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="0f659-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0f659-205">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="0f659-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0f659-206">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-207">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="0f659-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0f659-208">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-209">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="0f659-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f659-210">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f659-211">**El recurso pertenece a una unidad organizativa distinta de la unidad de contratación del proyecto**</span><span class="sxs-lookup"><span data-stu-id="0f659-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0f659-212">Evento</span><span class="sxs-lookup"><span data-stu-id="0f659-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0f659-213">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="0f659-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0f659-214">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="0f659-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0f659-215">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="0f659-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0f659-216">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="0f659-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0f659-217">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="0f659-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0f659-218">Datos reales</span><span class="sxs-lookup"><span data-stu-id="0f659-218">Actuals</span></span></th>
<th><span data-ttu-id="0f659-219">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="0f659-219">Transaction currency</span></span></th>
<th><span data-ttu-id="0f659-220">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="0f659-220">Fixed price</span></span></th>
<th><span data-ttu-id="0f659-221">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="0f659-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f659-222">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="0f659-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0f659-223">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="0f659-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-224">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="0f659-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0f659-225">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="0f659-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0f659-226">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0f659-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0f659-227">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-227">Cost actual</span></span></td>
<td><span data-ttu-id="0f659-228">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0f659-229">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0f659-230">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0f659-231">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0f659-232">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-233">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="0f659-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0f659-234">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-235">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="0f659-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0f659-236">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="0f659-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-237">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="0f659-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0f659-238">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0f659-239">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0f659-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0f659-240">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-240">Cost actual</span></span></td>
<td><span data-ttu-id="0f659-241">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0f659-242">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0f659-243">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0f659-244">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0f659-245">Coste real</span><span class="sxs-lookup"><span data-stu-id="0f659-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-246">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="0f659-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0f659-247">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="0f659-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-248">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="0f659-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0f659-249">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="0f659-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-250">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="0f659-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0f659-251">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-252">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="0f659-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f659-253">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f659-254">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0f659-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0f659-255">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="0f659-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0f659-256">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-257">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="0f659-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-258">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-259">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0f659-260">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-261">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="0f659-261">Billed sales</span></span></td>
<td><span data-ttu-id="0f659-262">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f659-263">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0f659-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0f659-264">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="0f659-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0f659-265">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-266">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-267">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-268">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f659-269">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-270">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="0f659-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0f659-271">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-272">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="0f659-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f659-273">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f659-274">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="0f659-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0f659-275">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="0f659-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0f659-276">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0f659-277">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="0f659-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0f659-278">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="0f659-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0f659-279">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0f659-280">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0f659-281">No disponible</span><span class="sxs-lookup"><span data-stu-id="0f659-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-282">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="0f659-282">Billed sales</span></span></td>
<td><span data-ttu-id="0f659-283">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f659-284">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="0f659-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0f659-285">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="0f659-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0f659-286">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-287">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="0f659-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0f659-288">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f659-289">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="0f659-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f659-290">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="0f659-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]