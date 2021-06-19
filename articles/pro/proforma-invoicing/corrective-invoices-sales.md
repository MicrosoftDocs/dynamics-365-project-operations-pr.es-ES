---
title: Facturas de proyecto correctivas
description: Este tema proporciona información sobre cómo crear y confirmar facturas correctivas en Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004102"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="3b869-103">Facturas de proyecto correctivas</span><span class="sxs-lookup"><span data-stu-id="3b869-103">Corrective project invoices</span></span>

<span data-ttu-id="3b869-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="3b869-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3b869-105">Una factura de proyecto confirmada se puede corregir para procesar cambios o créditos según se negocie con el cliente y el gerente de proyecto.</span><span class="sxs-lookup"><span data-stu-id="3b869-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="3b869-106">Para realizar modificaciones en una factura confirmada, abra la factura confirmada y seleccione **Corregir esta factura**.</span><span class="sxs-lookup"><span data-stu-id="3b869-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="3b869-107">Esta selección no está disponible a menos que se confirme la factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="3b869-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="3b869-108">Se crea un nuevo borrador de factura a partir de la factura confirmada.</span><span class="sxs-lookup"><span data-stu-id="3b869-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="3b869-109">Todos los detalles de la línea de factura de la factura previamente confirmada se copian en el nuevo borrador.</span><span class="sxs-lookup"><span data-stu-id="3b869-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="3b869-110">Los siguientes son algunos de los puntos clave que debe comprender acerca de los detalles de la línea en la nueva factura corregida:</span><span class="sxs-lookup"><span data-stu-id="3b869-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="3b869-111">Todas las cantidades se actualizan a cero.</span><span class="sxs-lookup"><span data-stu-id="3b869-111">All quantities are updated to zero.</span></span> <span data-ttu-id="3b869-112">La aplicación asume que todos los artículos facturados se abonan por completo.</span><span class="sxs-lookup"><span data-stu-id="3b869-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="3b869-113">Si es necesario, puede actualizar manualmente estas cantidades para reflejar la cantidad que se está facturando y no la cantidad que se está acreditando.</span><span class="sxs-lookup"><span data-stu-id="3b869-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="3b869-114">Según la cantidad que introduce, la aplicación calcula la cantidad acreditada.</span><span class="sxs-lookup"><span data-stu-id="3b869-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="3b869-115">Esta cantidad se refleja en los datos reales que se crean cuando se confirma la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="3b869-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="3b869-116">Si está realizando cambios en la cantidad del impuesto, debe introducir el monto del impuesto correcto y no el del impuesto que se acredita.</span><span class="sxs-lookup"><span data-stu-id="3b869-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="3b869-117">Las líneas de contrato basadas en productos previamente confirmadas no se copian.</span><span class="sxs-lookup"><span data-stu-id="3b869-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="3b869-118">No se admite el procesamiento de correcciones en una factura de proyecto basada en productos.</span><span class="sxs-lookup"><span data-stu-id="3b869-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="3b869-119">Las correcciones de hitos siempre se procesan como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="3b869-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="3b869-120">Los montos de anticipo o anticipo pueden corregirse si al cliente se le facturó un monto incorrecto.</span><span class="sxs-lookup"><span data-stu-id="3b869-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="3b869-121">Las conciliaciones de retenciones y anticipos se pueden corregir si se utilizó una cantidad incorrecta para conciliar los cargos en una factura previamente confirmada.</span><span class="sxs-lookup"><span data-stu-id="3b869-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b869-122">Los detalles de la línea de la factura que son correcciones a otros cargos ya facturados tienen el campo **Corrección** establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="3b869-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="3b869-123">Las facturas que tienen detalles de línea de factura corregidos tienen un campo llamado **Tiene correcciones** que también está configurado en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="3b869-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="3b869-124">Datos reales creados cuando se confirma una factura correctiva</span><span class="sxs-lookup"><span data-stu-id="3b869-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="3b869-125">La siguiente tabla enumera los datos reales que se crean cuando se confirma una factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="3b869-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="3b869-126">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3b869-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="3b869-127">
                    <strong>Datos reales creados en la confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3b869-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="3b869-128">Confirmar la corrección de un anticipo o anticipo facturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3b869-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-129">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="3b869-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="3b869-130">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="3b869-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-131">Se crea una reversión real de ventas facturadas por el monto del anticipo o anticipo para revertir las ventas facturadas originales.</span><span class="sxs-lookup"><span data-stu-id="3b869-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-132">Se crea un nuevo real de ventas facturadas para el monto corregido en el anticipo o en la línea de factura corregida basada en anticipos.</span><span class="sxs-lookup"><span data-stu-id="3b869-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-133">Una venta no facturada real del monto negativo del anticipo o línea de factura corregida basada en anticipos, que se utilizará para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="3b869-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="3b869-134">Una confirmación de la corrección de un anticipo o anticipo previamente conciliado.</span><span class="sxs-lookup"><span data-stu-id="3b869-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-135">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="3b869-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="3b869-136">Este monto es positivo y está destinado a cancelar el negativo que se creó cuando tuvo lugar la conciliación anterior.</span><span class="sxs-lookup"><span data-stu-id="3b869-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-137">Una reversión real de las ventas facturadas por el importe de la factura anterior.</span><span class="sxs-lookup"><span data-stu-id="3b869-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-138">Una nueva venta facturada real para la cantidad corregida del anticipo que se aplicará en la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="3b869-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-139">Una venta no facturada real con un monto negativo del resto del anticipo o avance corregido que se usará para la reconciliación en facturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="3b869-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3b869-140">Facturación del crédito total de una transacción de tiempo facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-141">Una reversión de ventas facturadas por las horas y el monto en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="3b869-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-142">Una venta nueva real sin facturar por las horas y el monto en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="3b869-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3b869-143">Facturación del crédito parcial en una transacción a tiempo.</span><span class="sxs-lookup"><span data-stu-id="3b869-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-144">Una reversión de ventas facturadas por las horas y el monto facturado en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="3b869-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-145">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="3b869-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-146">Un nuevo real de ventas no facturadas que se cobra por las horas restantes y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="3b869-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3b869-147">Facturación del crédito total de una transacción de gastos facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-148">Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los gastos.</span><span class="sxs-lookup"><span data-stu-id="3b869-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-149">Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los gastos.</span><span class="sxs-lookup"><span data-stu-id="3b869-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3b869-150">Facturación del crédito parcial de una transacción de gastos facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-151">Una reversión de ventas facturadas por la cantidad y el monto facturado en el detalle de la línea de factura original por unos gastos.</span><span class="sxs-lookup"><span data-stu-id="3b869-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-152">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="3b869-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-153">Un nuevo real de ventas no facturadas que se cobra por la cantidad restante y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="3b869-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3b869-154">Facturación del crédito total de una transacción de material facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-155">Una anulación de ventas facturada por la cantidad y el importe en el detalle de línea de factura original en concepto de material.</span><span class="sxs-lookup"><span data-stu-id="3b869-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-156">Un nuevo valor real de ventas sin facturar por la cantidad y el importe en el detalle de línea de factura original en concepto de material.</span><span class="sxs-lookup"><span data-stu-id="3b869-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3b869-157">Facturación del abono parcial de una transacción de material.</span><span class="sxs-lookup"><span data-stu-id="3b869-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-158">Una anulación de ventas facturada por la cantidad y el importe facturados en el detalle de línea de factura original en concepto de material.</span><span class="sxs-lookup"><span data-stu-id="3b869-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-159">Un nuevo valor real de ventas no facturadas que es imputable por la cantidad y el importe en el detalle de la línea de factura editada, una reversión de esto y un valor real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="3b869-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-160">Un nuevo real de ventas no facturadas que se cobra por la cantidad restante y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="3b869-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3b869-161">Facturación del crédito total de una transacción de precio facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-162">Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="3b869-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-163">Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="3b869-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3b869-164">Facturación del crédito parcial de una transacción de precio facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-165">Una reversión de ventas facturadas por la cantidad y el monto facturados en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="3b869-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-166">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida editada, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="3b869-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="3b869-167">Facturación del crédito total de un hito facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-168">Una reversión de ventas facturadas por el monto en el detalle de la línea de factura original para el hito.</span><span class="sxs-lookup"><span data-stu-id="3b869-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="3b869-169">El estado de la factura del hito se actualiza desde <b>Factura del cliente registrada</b> hasta <b>Listo para facturar</b>.</span><span class="sxs-lookup"><span data-stu-id="3b869-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="3b869-170">Facturación del crédito parcial de un hito facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-171">Incompatible</span><span class="sxs-lookup"><span data-stu-id="3b869-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="3b869-172">Créditos y correcciones de una línea de contrato basado en producto facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="3b869-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3b869-173">Incompatible</span><span class="sxs-lookup"><span data-stu-id="3b869-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
