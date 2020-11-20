---
title: Confirmar una factura proforma (lite)
description: Este tema proporciona información sobre confirmar facturas proforma en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176542"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="1d321-103">Confirmar una factura proforma (lite)</span><span class="sxs-lookup"><span data-stu-id="1d321-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="1d321-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="1d321-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1d321-105">Después de que se confirma una factura proforma, el estado de la factura del proyecto se actualiza a **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="1d321-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="1d321-106">Cuando se confirma una factura, pasa a ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1d321-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="1d321-107">En el futuro, la factura solo se puede corregir si hay correcciones o créditos iniciados por el cliente, o si la factura está marcada como pagada.</span><span class="sxs-lookup"><span data-stu-id="1d321-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="1d321-108">En la siguiente tabla se enumeran los datos reales creadas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="1d321-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="1d321-109">Estos datos reales se crean cuando se realizan determinadas operaciones en el borrador de la factura del proyecto antes de que se confirme.</span><span class="sxs-lookup"><span data-stu-id="1d321-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="1d321-110">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1d321-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="1d321-111">
                    <strong>Datos reales creados en la confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1d321-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1d321-112">Facturar un avance o retención</span><span class="sxs-lookup"><span data-stu-id="1d321-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-113">Un tipo real de ventas facturadas, <strong>Anticipo</strong> se crea por el monto del anticipo o adelanto.</span><span class="sxs-lookup"><span data-stu-id="1d321-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-114">Una venta no facturada real de un monto negativo del anticipo o retención para usarse para la reconciliación.</span><span class="sxs-lookup"><span data-stu-id="1d321-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1d321-115">Después de conciliar completamente un anticipo o adelanto de una factura.</span><span class="sxs-lookup"><span data-stu-id="1d321-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-116">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="1d321-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="1d321-117">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="1d321-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-118">Un real de las ventas facturadas por el importe esta factura.</span><span class="sxs-lookup"><span data-stu-id="1d321-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1d321-119">Después de conciliar parcialmente un anticipo o adelanto de una factura.</span><span class="sxs-lookup"><span data-stu-id="1d321-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-120">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="1d321-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="1d321-121">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="1d321-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-122">Un real de las ventas facturadas por el importe esta factura.</span><span class="sxs-lookup"><span data-stu-id="1d321-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-123">Una venta negativa real no facturada de la cantidad restante del anticipo o retención que se usará para la reconciliación en futuras facturas.</span><span class="sxs-lookup"><span data-stu-id="1d321-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1d321-124">Facturar una transacción de tiempo sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="1d321-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-125">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="1d321-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-126">Una venta real facturada por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="1d321-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1d321-127">Facturar una transacción de tiempo que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="1d321-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-128">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="1d321-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-129">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="1d321-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-130">Un nuevo real de ventas no facturadas que se cobra para las horas y la cantidad restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="1d321-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1d321-131">Facturar una transacción de tiempo que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="1d321-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-132">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="1d321-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-133">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="1d321-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1d321-134">Facturar una transacción de gastos sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="1d321-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-135">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="1d321-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-136">Una venta real facturada para la cantidad y la coste en la aprobación del gasto original</span><span class="sxs-lookup"><span data-stu-id="1d321-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1d321-137">Facturar una transacción de gastos que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="1d321-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-138">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="1d321-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-139">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="1d321-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-140">Un nuevo real de ventas no facturadas que se cobra para las cantidad y la cifra restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="1d321-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1d321-141">Facturar una transacción de gastos que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="1d321-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-142">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="1d321-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-143">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="1d321-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1d321-144">Facturación de una tarifa.</span><span class="sxs-lookup"><span data-stu-id="1d321-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-145">Una reversión de ventas no facturadas por la cantidad del precio en la línea del diario original.</span><span class="sxs-lookup"><span data-stu-id="1d321-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-146">Una venta real facturada para la cantidad y la coste en la aprobación de la tarifa de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="1d321-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1d321-147">Facturación de un hito.</span><span class="sxs-lookup"><span data-stu-id="1d321-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-148">Una venta facturada real por la cantidad del hito en el hito original en la línea de contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1d321-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1d321-149">Facturar una línea de contrato basada en productos.</span><span class="sxs-lookup"><span data-stu-id="1d321-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1d321-150">Ventas facturadas reales para la línea de productos con la cantidad y el monto provenientes de la línea de contrato basada en productos.</span><span class="sxs-lookup"><span data-stu-id="1d321-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
