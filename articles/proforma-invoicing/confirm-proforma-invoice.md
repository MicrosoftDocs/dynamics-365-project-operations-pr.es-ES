---
title: Confirmar una factura basada en proyecto proforma
description: Este tema proporciona información sobre cómo confirmar las facturas basadas en un proyecto proforma.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867152"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="b3a7e-103">Confirmar una factura basada en proyecto proforma</span><span class="sxs-lookup"><span data-stu-id="b3a7e-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="b3a7e-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="b3a7e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b3a7e-105">Después de que se confirma una factura proforma, el estado de la factura del proyecto se actualiza a **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="b3a7e-106">Cuando se confirma una factura, pasa a ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="b3a7e-107">En el futuro, la factura solo se puede corregir si hay correcciones o créditos iniciados por el cliente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="b3a7e-108">En la siguiente tabla se enumeran los datos reales creadas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="b3a7e-109">Estos datos reales se crean cuando se realizan determinadas operaciones en el borrador de la factura del proyecto antes de que se confirme.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="b3a7e-110">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b3a7e-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="b3a7e-111">
                    <strong>Datos reales creados en la confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b3a7e-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-112">Facturar un avance o retención</span><span class="sxs-lookup"><span data-stu-id="b3a7e-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-113">Un tipo real de ventas facturadas, <strong>Anticipo</strong> se crea por el monto del anticipo o adelanto.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-114">Las ventas reales no facturadas con un importe negativo del anticipo o avance que se utilizará para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-115">Después de conciliar completamente un anticipo o adelanto de una factura.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-116">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="b3a7e-117">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-118">Un real de las ventas facturadas por el importe esta factura.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b3a7e-119">Después de conciliar parcialmente un anticipo o adelanto de una factura.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-120">Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="b3a7e-121">Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-122">Un real de las ventas facturadas por el importe esta factura.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-123">Una venta negativa real no facturada de la cantidad restante del anticipo o retención que se usará para la reconciliación en futuras facturas.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-124">Facturar una transacción de tiempo sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-125">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-126">Una venta real facturada por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b3a7e-127">Facturar una transacción de tiempo que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-128">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-129">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-130">Un nuevo valor real de ventas no facturadas que no es imputable por las horas restantes y el importe después de deducir las cifras corregidas en el detalle de la línea de factura editada, una reversión de los valores reales de las ventas y un valor real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-131">Facturar una transacción de tiempo que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-132">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-133">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-134">Facturar una transacción de gastos sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-135">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-136">Una venta real facturada para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b3a7e-137">Facturar una transacción de gastos que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-138">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-139">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-140">Un nuevo real de ventas no facturadas que se cobra para las cantidad y la cifra restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-141">Facturar una transacción de gastos que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-142">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-143">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-144">Facturar una transacción de material sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-145">Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de utilización de material original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-146">Un valor real de ventas facturado por la cantidad y el importe de la aprobación de utilización de material original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b3a7e-147">Facturar una transacción de material que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-148">Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de tiempo original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-149">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-150">Un nuevo real de ventas no facturadas que se cobra para las cantidad y la cifra restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-151">Facturar una transacción de material que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-152">Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de utilización de material original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-153">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b3a7e-154">Facturación de una tarifa.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-155">Una reversión de ventas no facturadas por la cantidad del precio en la línea del diario original.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-156">Una venta real facturada para la cantidad y la coste en la aprobación de la tarifa de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b3a7e-157">Facturación de un hito.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b3a7e-158">Una venta facturada real por la cantidad del hito en el hito original en la línea de contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b3a7e-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
