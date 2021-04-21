---
title: Facturas basadas en proyecto correctivas
description: Este tema proporciona información sobre cómo crear y confirmar facturas basadas en proyectos correctivas en Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867062"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="ad2a2-103">Facturas basadas en proyecto correctivas</span><span class="sxs-lookup"><span data-stu-id="ad2a2-103">Corrective project-based invoices</span></span>

<span data-ttu-id="ad2a2-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="ad2a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ad2a2-105">Una factura de proyecto confirmada se puede corregir para procesar cambios o créditos según se negocie con el cliente y el gerente de proyecto.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="ad2a2-106">Para realizar modificaciones en una factura confirmada, abra la factura confirmada y seleccione **Corregir esta factura**.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ad2a2-107">Esta selección no está disponible a menos que se confirme una factura del proyecto o que la factura basada en el proyecto tenga anticipos o pagos a cuenta o conciliaciones de anticipos o pagos a cuenta.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="ad2a2-108">Se crea un nuevo borrador de factura a partir de la factura confirmada.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="ad2a2-109">Todos los detalles de la línea de factura de la factura previamente confirmada se copian en el nuevo borrador.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="ad2a2-110">Los siguientes son algunos de los puntos clave que debe comprender acerca de los detalles de la línea en la nueva factura corregida:</span><span class="sxs-lookup"><span data-stu-id="ad2a2-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="ad2a2-111">Todas las cantidades se actualizan a cero.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-111">All quantities are updated to zero.</span></span> <span data-ttu-id="ad2a2-112">Dynamics 365 Project Operations supone que todos los elementos facturados se abonan en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="ad2a2-113">Si es necesario, puede actualizar manualmente estas cantidades para reflejar la cantidad que se está facturando y no la cantidad que se está acreditando.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="ad2a2-114">Según la cantidad que introduce, la aplicación calcula la cantidad acreditada.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="ad2a2-115">Esta cantidad se refleja en los datos reales que se crean cuando se confirma la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="ad2a2-116">Si está realizando cambios en la cantidad del impuesto, debe introducir el monto del impuesto correcto y no el del impuesto que se acredita.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="ad2a2-117">Las correcciones de hitos siempre se procesan como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="ad2a2-118">Para los detalles de la línea de factura que son correcciones de otros cargos ya facturados, el campo **Corrección** está establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="ad2a2-119">Para las facturas con detalles de línea de factura corregida, el campo **Tiene correcciones** está establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="ad2a2-120">Datos reales creados cuando se confirma una factura correctiva</span><span class="sxs-lookup"><span data-stu-id="ad2a2-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="ad2a2-121">La siguiente tabla enumera los datos reales que se crean cuando se confirma una factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="ad2a2-122">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ad2a2-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="ad2a2-123">
                    <strong>Datos reales creados en la confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ad2a2-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ad2a2-124">Facturación del crédito total de una transacción de tiempo facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-125">Una reversión de ventas facturadas por las horas y el monto en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-126">Una venta nueva real sin facturar por las horas y el monto en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ad2a2-127">Facturación del crédito parcial en una transacción a tiempo.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-128">Una reversión de ventas facturadas por las horas y el monto facturado en el detalle de la línea de factura original por tiempo.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-129">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-130">Un nuevo real de ventas no facturadas que se cobra por las horas restantes y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ad2a2-131">Facturación del crédito total de una transacción de gastos facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-132">Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los gastos.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-133">Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los gastos.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ad2a2-134">Facturación del crédito parcial de una transacción de gastos facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-135">Una reversión de ventas facturadas por la cantidad y el monto facturado en el detalle de la línea de factura original por unos gastos.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-136">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-137">Un nuevo real de ventas no facturadas que se cobra por la cantidad restante y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ad2a2-138">Facturación del crédito total de una transacción de material facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-139">Una anulación de ventas facturada por la cantidad y el importe en el detalle de línea de factura original en concepto de material.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-140">Un nuevo valor real de ventas sin facturar por la cantidad y el importe en el detalle de línea de factura original en concepto de material.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ad2a2-141">Facturación del abono parcial de una transacción de material.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-142">Una anulación de ventas facturada por la cantidad y el importe facturados en el detalle de línea de factura original en concepto de material.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-143">Un nuevo valor real de ventas no facturadas que es imputable por la cantidad y el importe en el detalle de la línea de factura editada, una reversión de esto y un valor real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-144">Un nuevo real de ventas no facturadas que se cobra por la cantidad restante y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ad2a2-145">Facturación del crédito total de una transacción de precio facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-146">Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-147">Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ad2a2-148">Facturación del crédito parcial de una transacción de precio facturada previamente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-149">Una reversión de ventas facturadas por la cantidad y el monto facturados en el detalle de la línea de factura original por los honorarios.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-150">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida editada, una reversión de este y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ad2a2-151">Facturación del crédito total de un hito facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-152">Una reversión de ventas facturadas por el monto en el detalle de la línea de factura original para el hito.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="ad2a2-153">El estado de la factura del hito se actualiza desde <b>Factura del cliente registrada</b> hasta <b>Listo para facturar</b>.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ad2a2-154">Facturación del crédito parcial de un hito facturado previamente.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ad2a2-155">Esto escenario no es compatible.</span><span class="sxs-lookup"><span data-stu-id="ad2a2-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
