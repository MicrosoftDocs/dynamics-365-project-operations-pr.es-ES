---
title: Confirmar una factura de proyecto proforma
description: Este tema proporciona información sobre cómo confirmar las facturas proforma del proyecto en Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004147"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="275d4-103">Confirmar una factura de proyecto proforma</span><span class="sxs-lookup"><span data-stu-id="275d4-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="275d4-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="275d4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="275d4-105">Después de que se confirma una factura proforma, el estado de la factura del proyecto se actualiza a **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="275d4-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="275d4-106">Cuando se confirma una factura, pasa a ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="275d4-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="275d4-107">En el futuro, la factura solo se puede corregir si hay correcciones o créditos iniciados por el cliente.</span><span class="sxs-lookup"><span data-stu-id="275d4-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="275d4-108">En la siguiente tabla se enumeran los datos reales creadas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="275d4-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="275d4-109">Estos datos reales se crean cuando se realizan determinadas operaciones en el borrador de la factura del proyecto antes de que se confirme.</span><span class="sxs-lookup"><span data-stu-id="275d4-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="275d4-110">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="275d4-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="275d4-111">
                    <strong>Datos reales creados en la confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="275d4-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-112">Facturar un avance o retención</span><span class="sxs-lookup"><span data-stu-id="275d4-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-113">Un tipo real de ventas facturadas, <strong>Anticipo</strong> se crea por el monto del anticipo o adelanto.</span><span class="sxs-lookup"><span data-stu-id="275d4-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-114">Una venta no facturada real de un monto negativo del anticipo o retención para usarse para la reconciliación.</span><span class="sxs-lookup"><span data-stu-id="275d4-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-115">Después de conciliar completamente un anticipo o adelanto de una factura.</span><span class="sxs-lookup"><span data-stu-id="275d4-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-116">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="275d4-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="275d4-117">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="275d4-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-118">Un real de las ventas facturadas por el importe esta factura.</span><span class="sxs-lookup"><span data-stu-id="275d4-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="275d4-119">Después de conciliar parcialmente un anticipo o adelanto de una factura.</span><span class="sxs-lookup"><span data-stu-id="275d4-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-120">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="275d4-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="275d4-121">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="275d4-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-122">Un real de las ventas facturadas por el importe esta factura.</span><span class="sxs-lookup"><span data-stu-id="275d4-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-123">Una venta negativa real no facturada de la cantidad restante del anticipo o retención que se usará para la reconciliación en futuras facturas.</span><span class="sxs-lookup"><span data-stu-id="275d4-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-124">Facturar una transacción de tiempo sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="275d4-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-125">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="275d4-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-126">Una venta real facturada por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="275d4-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="275d4-127">Facturar una transacción de tiempo que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="275d4-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-128">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="275d4-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-129">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-130">Un nuevo real de ventas no facturadas que se cobra para las horas y la cantidad restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-131">Facturar una transacción de tiempo que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="275d4-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-132">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="275d4-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-133">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-134">Facturar una transacción de gastos sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="275d4-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-135">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="275d4-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-136">Una venta real facturada para la cantidad y la coste en la aprobación del gasto original</span><span class="sxs-lookup"><span data-stu-id="275d4-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="275d4-137">Facturar una transacción de gastos que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="275d4-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-138">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="275d4-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-139">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-140">Un nuevo real de ventas no facturadas que se cobra para las cantidad y la cifra restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-141">Facturar una transacción de gastos que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="275d4-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-142">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="275d4-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-143">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-144">Facturar una transacción de material sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="275d4-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-145">Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de utilización de material original.</span><span class="sxs-lookup"><span data-stu-id="275d4-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-146">Un valor real de ventas facturado por la cantidad y el importe de la aprobación de utilización de material original.</span><span class="sxs-lookup"><span data-stu-id="275d4-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="275d4-147">Facturar una transacción de material que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="275d4-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-148">Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de tiempo original.</span><span class="sxs-lookup"><span data-stu-id="275d4-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-149">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-150">Un nuevo real de ventas no facturadas que se cobra para las cantidad y la cifra restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-151">Facturar una transacción de material que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="275d4-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-152">Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de utilización de material original.</span><span class="sxs-lookup"><span data-stu-id="275d4-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-153">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="275d4-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="275d4-154">Facturación de una tarifa.</span><span class="sxs-lookup"><span data-stu-id="275d4-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-155">Una reversión de ventas no facturadas por la cantidad del precio en la línea del diario original.</span><span class="sxs-lookup"><span data-stu-id="275d4-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-156">Una venta real facturada para la cantidad y la coste en la aprobación de la tarifa de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="275d4-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="275d4-157">Facturación de un hito.</span><span class="sxs-lookup"><span data-stu-id="275d4-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-158">Una venta facturada real por la cantidad del hito en el hito original en la línea de contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="275d4-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="275d4-159">Facturar una línea de contrato basada en productos.</span><span class="sxs-lookup"><span data-stu-id="275d4-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="275d4-160">Ventas facturadas reales para la línea de productos con la cantidad y el monto provenientes de la línea de contrato basada en productos.</span><span class="sxs-lookup"><span data-stu-id="275d4-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
