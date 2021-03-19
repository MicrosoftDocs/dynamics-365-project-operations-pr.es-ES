---
title: Facturas corregidas (lite)
description: Este tema proporciona información sobre facturas corregidas en Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274254"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="f7b67-103">Facturas corregidas (lite)</span><span class="sxs-lookup"><span data-stu-id="f7b67-103">Corrected invoices - lite</span></span>

<span data-ttu-id="f7b67-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="f7b67-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7b67-105">Una factura de proyecto confirmada se puede corregir para procesar cambios o créditos según se negocie con el cliente y el gerente de proyecto.</span><span class="sxs-lookup"><span data-stu-id="f7b67-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="f7b67-106">Para realizar modificaciones en una factura confirmada, abra la factura confirmada y seleccione **Corregir esta factura**.</span><span class="sxs-lookup"><span data-stu-id="f7b67-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="f7b67-107">Esta selección no está disponible a menos que se confirme la factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="f7b67-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="f7b67-108">Se crea un nuevo borrador de factura a partir de la factura confirmada.</span><span class="sxs-lookup"><span data-stu-id="f7b67-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="f7b67-109">Todos los detalles de la línea de factura de la factura previamente confirmada se copian en el nuevo borrador.</span><span class="sxs-lookup"><span data-stu-id="f7b67-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="f7b67-110">Los siguientes son algunos de los puntos clave que debe comprender acerca de los detalles de la línea en la nueva factura corregida:</span><span class="sxs-lookup"><span data-stu-id="f7b67-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="f7b67-111">Todas las cantidades se actualizan a cero.</span><span class="sxs-lookup"><span data-stu-id="f7b67-111">All quantities are updated to zero.</span></span> <span data-ttu-id="f7b67-112">La aplicación asume que todos los artículos facturados se abonan por completo.</span><span class="sxs-lookup"><span data-stu-id="f7b67-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="f7b67-113">Si es necesario, puede actualizar manualmente estas cantidades para reflejar la cantidad que se está facturando y no la cantidad que se está acreditando.</span><span class="sxs-lookup"><span data-stu-id="f7b67-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="f7b67-114">Según la cantidad que introduce, la aplicación calcula la cantidad acreditada.</span><span class="sxs-lookup"><span data-stu-id="f7b67-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="f7b67-115">Esta cantidad se refleja en los datos reales que se crean cuando se confirma la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="f7b67-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="f7b67-116">Si está realizando cambios en la cantidad del impuesto, debe introducir el monto del impuesto correcto y no el del impuesto que se acredita.</span><span class="sxs-lookup"><span data-stu-id="f7b67-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="f7b67-117">Las líneas de contrato basadas en productos previamente confirmadas no se copian.</span><span class="sxs-lookup"><span data-stu-id="f7b67-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="f7b67-118">No se admite el procesamiento de correcciones en una factura de proyecto basada en productos.</span><span class="sxs-lookup"><span data-stu-id="f7b67-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="f7b67-119">Las correcciones de hitos siempre se procesan como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="f7b67-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="f7b67-120">Los montos de anticipo o anticipo pueden corregirse si al cliente se le facturó un monto incorrecto.</span><span class="sxs-lookup"><span data-stu-id="f7b67-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="f7b67-121">Las conciliaciones de retenciones y anticipos se pueden corregir si se utilizó una cantidad incorrecta para conciliar los cargos en una factura previamente confirmada.</span><span class="sxs-lookup"><span data-stu-id="f7b67-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7b67-122">Los detalles de la línea de la factura que son correcciones a otros cargos ya facturados tienen el campo **Corrección** establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="f7b67-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="f7b67-123">Las facturas que tienen detalles de línea de factura corregidos tienen un campo llamado **Tiene correcciones** que también está configurado en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="f7b67-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="f7b67-124">Datos reales creados en la confirmación de una factura correctiva:</span><span class="sxs-lookup"><span data-stu-id="f7b67-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="f7b67-125">A continuación se muestran los datos reales creados por la aplicación al confirmar un correctivo en función de las operaciones realizadas en el borrador de la factura correctiva antes de la confirmación.</span><span class="sxs-lookup"><span data-stu-id="f7b67-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="f7b67-126">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f7b67-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="f7b67-127">
                    <strong>Datos reales creados en la confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f7b67-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f7b67-128">Confirmar la corrección de un anticipo o anticipo facturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f7b67-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-129">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="f7b67-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f7b67-130">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="f7b67-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-131">Se crea una reversión real de ventas facturadas por el monto del anticipo o anticipo para revertir las ventas facturadas originales.</span><span class="sxs-lookup"><span data-stu-id="f7b67-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-132">Se crea un nuevo real de ventas facturadas para el monto corregido en el anticipo o en la línea de factura corregida basada en anticipos.</span><span class="sxs-lookup"><span data-stu-id="f7b67-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-133">Una venta no facturada real del monto negativo del anticipo o línea de factura corregida basada en anticipos, que se utilizará para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="f7b67-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f7b67-134">Una confirmación de la corrección de un anticipo o anticipo previamente conciliado.</span><span class="sxs-lookup"><span data-stu-id="f7b67-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-135">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="f7b67-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f7b67-136">Este monto es positivo y está destinado a cancelar el negativo que se creó cuando tuvo lugar la conciliación anterior.</span><span class="sxs-lookup"><span data-stu-id="f7b67-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-137">Una reversión real de las ventas facturadas por el importe de la factura anterior.</span><span class="sxs-lookup"><span data-stu-id="f7b67-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-138">Una nueva venta facturada real para la cantidad corregida del anticipo que se aplicará en la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="f7b67-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-139">Una venta no facturada real con un monto negativo del resto del anticipo o avance corregido que se usará para la reconciliación en facturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="f7b67-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f7b67-140">Facturación del crédito total de una transacción de tiempo facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-141">Una reversión de ventas facturadas por las horas y el monto en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="f7b67-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-142">Una venta nueva real sin facturar por las horas y el monto en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="f7b67-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f7b67-143">Facturación del crédito parcial en una transacción a tiempo.</span><span class="sxs-lookup"><span data-stu-id="f7b67-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-144">Una reversión de ventas facturadas por las horas y el monto facturado en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="f7b67-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-145">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-146">Un nuevo real de ventas no facturadas que se cobra por las horas restantes y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="f7b67-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f7b67-147">Facturación del crédito total de una transacción de gastos facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-148">Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los gastos.</span><span class="sxs-lookup"><span data-stu-id="f7b67-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-149">Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los gastos.</span><span class="sxs-lookup"><span data-stu-id="f7b67-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f7b67-150">Facturación del crédito parcial de una transacción de gastos facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-151">Una reversión de ventas facturadas por la cantidad y el monto facturado en el detalle de la línea de factura original por unos gastos.</span><span class="sxs-lookup"><span data-stu-id="f7b67-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-152">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-153">Un nuevo real de ventas no facturadas que se cobra por la cantidad restante y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="f7b67-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f7b67-154">Facturación del crédito total de una transacción de precio facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-155">Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="f7b67-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-156">Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="f7b67-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f7b67-157">Facturación del crédito parcial de una transacción de precio facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-158">Una reversión de ventas facturadas por la cantidad y el monto facturados en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="f7b67-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-159">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida editada, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f7b67-160">Facturación del crédito total de un hito facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-161">Una reversión de ventas facturadas por el monto en el detalle de la línea de factura original para el hito.</span><span class="sxs-lookup"><span data-stu-id="f7b67-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="f7b67-162">La factura de hito o el estado de facturación en la línea del contrato del proyecto se actualiza a **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="f7b67-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f7b67-163">Facturación del crédito parcial de un hito facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-164">Incompatible</span><span class="sxs-lookup"><span data-stu-id="f7b67-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f7b67-165">Créditos y correcciones de una línea de contrato basado en producto facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="f7b67-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f7b67-166">Incompatible</span><span class="sxs-lookup"><span data-stu-id="f7b67-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]