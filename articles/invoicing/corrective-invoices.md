---
title: Crear facturas basadas en proyecto correctivas
description: Este tema proporciona información sobre las facturas correctivas en Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788900"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="9fb47-103">Crear facturas basadas en proyecto correctivas</span><span class="sxs-lookup"><span data-stu-id="9fb47-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="9fb47-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="9fb47-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9fb47-105">Una factura de proyecto confirmada se puede corregir para procesar cambios o créditos según se negocie con el cliente y el gerente de proyecto.</span><span class="sxs-lookup"><span data-stu-id="9fb47-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="9fb47-106">Para realizar modificaciones en una factura confirmada, abra la factura confirmada y seleccione **Corregir esta factura**.</span><span class="sxs-lookup"><span data-stu-id="9fb47-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9fb47-107">Esta selección no está disponible a menos que se confirme la factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="9fb47-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="9fb47-108">Se crea un nuevo borrador de factura a partir de la factura confirmada.</span><span class="sxs-lookup"><span data-stu-id="9fb47-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="9fb47-109">Todos los detalles de la línea de factura de la factura previamente confirmada se copian en el nuevo borrador.</span><span class="sxs-lookup"><span data-stu-id="9fb47-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="9fb47-110">Los siguientes son algunos puntos clave para ayudarle a comprender mejor los detalles de la línea en la nueva factura corregida:</span><span class="sxs-lookup"><span data-stu-id="9fb47-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="9fb47-111">Todas las cantidades se actualizan a cero.</span><span class="sxs-lookup"><span data-stu-id="9fb47-111">All quantities are updated to zero.</span></span> <span data-ttu-id="9fb47-112">Esto supone que todos los elementos facturados se abonan en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="9fb47-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="9fb47-113">Si es necesario, puede actualizar manualmente estas cantidades para reflejar la cantidad que se está facturando y no la cantidad que se está acreditando.</span><span class="sxs-lookup"><span data-stu-id="9fb47-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="9fb47-114">Según la cantidad que introduce, la aplicación calcula la cantidad acreditada.</span><span class="sxs-lookup"><span data-stu-id="9fb47-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="9fb47-115">Esta cantidad se refleja en los datos reales que se crean cuando se confirma la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="9fb47-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="9fb47-116">Si está realizando cambios en la cantidad del impuesto, debe introducir el monto del impuesto correcto y no el del impuesto que se acredita.</span><span class="sxs-lookup"><span data-stu-id="9fb47-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="9fb47-117">Las correcciones de hitos siempre se procesan como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="9fb47-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="9fb47-118">Los montos de anticipo o anticipo pueden corregirse si al cliente se le facturó un monto incorrecto.</span><span class="sxs-lookup"><span data-stu-id="9fb47-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="9fb47-119">Las conciliaciones de retenciones y anticipos se pueden corregir si se utilizó una cantidad incorrecta para conciliar los cargos en una factura previamente confirmada.</span><span class="sxs-lookup"><span data-stu-id="9fb47-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fb47-120">Los detalles de la línea de factura que son correcciones de otros cargos ya facturados tienen el campo **Corrección** establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="9fb47-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="9fb47-121">Las facturas que tienen detalles de línea de factura corregidos tienen un campo llamado **Tiene correcciones** que también está configurado en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="9fb47-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="9fb47-122">Datos reales creados en la confirmación de una factura correctiva</span><span class="sxs-lookup"><span data-stu-id="9fb47-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="9fb47-123">La siguiente tabla enumera los datos reales que se crean cuando se confirma una factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="9fb47-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9fb47-124">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9fb47-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9fb47-125">
                    <strong>Datos reales creados en la confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9fb47-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="9fb47-126">Confirmar la corrección de un anticipo o anticipo facturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9fb47-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-127">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="9fb47-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9fb47-128">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="9fb47-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-129">Se crea una reversión real de ventas facturadas por el monto del anticipo o anticipo para revertir las ventas facturadas originales.</span><span class="sxs-lookup"><span data-stu-id="9fb47-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-130">Se crea un nuevo real de ventas facturadas para el monto corregido en el anticipo o en la línea de factura corregida basada en anticipos.</span><span class="sxs-lookup"><span data-stu-id="9fb47-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-131">Una venta no facturada real del monto negativo del anticipo o línea de factura corregida basada en anticipos, que se utilizará para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="9fb47-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="9fb47-132">Una confirmación de la corrección de un anticipo o anticipo previamente conciliado.</span><span class="sxs-lookup"><span data-stu-id="9fb47-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-133">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="9fb47-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9fb47-134">Este monto es positivo y está destinado a cancelar el negativo que se creó cuando tuvo lugar la conciliación anterior.</span><span class="sxs-lookup"><span data-stu-id="9fb47-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-135">Una reversión real de las ventas facturadas por el importe de la factura anterior.</span><span class="sxs-lookup"><span data-stu-id="9fb47-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-136">Una nueva venta facturada real para la cantidad corregida del anticipo que se aplicará en la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="9fb47-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-137">Una venta no facturada real con un monto negativo del resto del anticipo o avance corregido que se usará para la reconciliación en facturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="9fb47-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9fb47-138">Facturación del crédito total de una transacción de tiempo facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-139">Una reversión de ventas facturadas por las horas y el monto en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="9fb47-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-140">Una venta nueva real sin facturar por las horas y el monto en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="9fb47-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9fb47-141">Facturación del crédito parcial en una transacción a tiempo.</span><span class="sxs-lookup"><span data-stu-id="9fb47-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-142">Una reversión de ventas facturadas por las horas y el monto facturado en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="9fb47-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-143">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-144">Un nuevo real de ventas no facturadas que se cobra por las horas restantes y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="9fb47-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9fb47-145">Facturación del crédito total de una transacción de gastos facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-146">Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los gastos.</span><span class="sxs-lookup"><span data-stu-id="9fb47-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-147">Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los gastos.</span><span class="sxs-lookup"><span data-stu-id="9fb47-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9fb47-148">Facturación del crédito parcial de una transacción de gastos facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-149">Una reversión de ventas facturadas por la cantidad y el monto facturado en el detalle de la línea de factura original por unos gastos.</span><span class="sxs-lookup"><span data-stu-id="9fb47-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-150">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-151">Un nuevo real de ventas no facturadas que se cobra por la cantidad restante y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="9fb47-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9fb47-152">Facturación del crédito total de una transacción de precio facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-153">Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="9fb47-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-154">Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="9fb47-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9fb47-155">Facturación del crédito parcial de una transacción de precio facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-156">Una reversión de ventas facturadas por la cantidad y el monto facturados en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="9fb47-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-157">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida editada, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9fb47-158">Facturación del crédito total de un hito facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-159">Una reversión de ventas facturadas por el monto en el detalle de la línea de factura original para el hito.</span><span class="sxs-lookup"><span data-stu-id="9fb47-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="9fb47-160">El estado de la factura en el hito se actualiza desde <b>Factura del cliente registrada</b> hasta <b>Listo para facturar</b>.</span><span class="sxs-lookup"><span data-stu-id="9fb47-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9fb47-161">Facturación del crédito parcial de un hito facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="9fb47-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9fb47-162">Incompatible</span><span class="sxs-lookup"><span data-stu-id="9fb47-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
