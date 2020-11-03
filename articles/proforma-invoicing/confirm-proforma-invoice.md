---
title: Confirmar una factura proforma
description: Este tema proporciona información sobre cómo confirmar una factura proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084993"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="d2536-103">Confirmar una factura proforma</span><span class="sxs-lookup"><span data-stu-id="d2536-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="d2536-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="d2536-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d2536-105">Después de que se confirma una factura proforma, el estado de la factura del proyecto se actualiza a **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="d2536-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="d2536-106">Cuando se confirma una factura, pasa a ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2536-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="d2536-107">En el futuro, la factura solo se puede corregir si hay correcciones o créditos iniciados por el cliente, o cuando se marca como pagada.</span><span class="sxs-lookup"><span data-stu-id="d2536-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="d2536-108">En la siguiente tabla se enumeran los datos reales creadas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="d2536-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="d2536-109">Estos datos reales se crean cuando se realizan determinadas operaciones en el borrador de la factura del proyecto antes de que se confirme.</span><span class="sxs-lookup"><span data-stu-id="d2536-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="d2536-110">
                    <strong>Escenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d2536-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="d2536-111">
                    <strong>Datos reales creados en la confirmación</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d2536-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2536-112">Facturar una transacción de tiempo sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="d2536-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-113">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="d2536-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-114">Una venta real facturada por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="d2536-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2536-115">Facturar una transacción de tiempo que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="d2536-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-116">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="d2536-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-117">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="d2536-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-118">Un nuevo real de ventas no facturadas que se cobra para las horas y la cantidad restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="d2536-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2536-119">Facturar una transacción de tiempo que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="d2536-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-120">Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.</span><span class="sxs-lookup"><span data-stu-id="d2536-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-121">Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="d2536-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2536-122">Facturar una transacción de gastos sin modificaciones en el borrador de la factura.</span><span class="sxs-lookup"><span data-stu-id="d2536-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-123">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="d2536-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-124">Una venta real facturada para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="d2536-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2536-125">Facturar una transacción de gastos que se editó para reducir la cantidad.</span><span class="sxs-lookup"><span data-stu-id="d2536-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-126">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="d2536-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-127">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="d2536-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-128">Un nuevo real de ventas no facturadas que se cobra para las cantidad y la cifra restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="d2536-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2536-129">Facturar una transacción de gastos que se editó para aumentar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="d2536-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-130">Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.</span><span class="sxs-lookup"><span data-stu-id="d2536-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-131">Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="d2536-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2536-132">Facturación de una tarifa.</span><span class="sxs-lookup"><span data-stu-id="d2536-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-133">Una reversión de ventas no facturadas por la cantidad del precio en la línea del diario original.</span><span class="sxs-lookup"><span data-stu-id="d2536-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-134">Una venta real facturada para la cantidad y la coste en la aprobación de la tarifa de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="d2536-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d2536-135">Facturación de un hito.</span><span class="sxs-lookup"><span data-stu-id="d2536-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2536-136">Una venta facturada real por la cantidad del hito en el hito original en la línea de contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d2536-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
