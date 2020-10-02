---
title: Facturas corregidas
description: En este tema se proporciona información sobre las facturas corregidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898102"
---
# <a name="corrected-invoices"></a><span data-ttu-id="46c0e-103">Facturas corregidas</span><span class="sxs-lookup"><span data-stu-id="46c0e-103">Corrected invoices</span></span>

<span data-ttu-id="46c0e-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="46c0e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46c0e-105">Las facturas confirmadas se pueden editar.</span><span class="sxs-lookup"><span data-stu-id="46c0e-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="46c0e-106">Cuando se edita una factura confirmada, se crea un borrador de la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="46c0e-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="46c0e-107">Puesto que se da por sentado que desea revertir todas las transacciones y las cantidades de factura original, la factura corregida incluye todas las transacciones de la factura original y todas sus cantidades son iguales a cero (0).</span><span class="sxs-lookup"><span data-stu-id="46c0e-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="46c0e-108">Cuando las transacciones no requieren corrección, puede quitarlas del borrador de la factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="46c0e-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="46c0e-109">Para revertir o devolver solo una cantidad parcial, puede editar el campo Cantidad en el detalle de la línea.</span><span class="sxs-lookup"><span data-stu-id="46c0e-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="46c0e-110">Si abre el detalle de la línea de factura, podrá ver la cantidad de la factura original.</span><span class="sxs-lookup"><span data-stu-id="46c0e-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="46c0e-111">A continuación, podrá editar la cantidad de la factura actual para que sea superior o inferior a la cantidad de la factura original.</span><span class="sxs-lookup"><span data-stu-id="46c0e-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="46c0e-112">Cuando se confirma una factura correctiva, el dato real de ventas facturadas originales se revierte y se crea un nuevo dato real de ventas facturadas.</span><span class="sxs-lookup"><span data-stu-id="46c0e-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="46c0e-113">Si la cantidad se redujo, la diferencia también generará un nuevo dato real de ventas sin facturar.</span><span class="sxs-lookup"><span data-stu-id="46c0e-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="46c0e-114">Por ejemplo, si la venta facturada original ascendía a ocho horas y el detalle de línea de factura corregida tenía una cantidad reducida de seis horas, se revierte la línea de ventas facturadas originales y se crean dos nuevos datos reales:</span><span class="sxs-lookup"><span data-stu-id="46c0e-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="46c0e-115">Un dato real de ventas facturadas por seis horas.</span><span class="sxs-lookup"><span data-stu-id="46c0e-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="46c0e-116">Un dato real de ventas sin facturar por las dos horas restantes.</span><span class="sxs-lookup"><span data-stu-id="46c0e-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="46c0e-117">Esta transacción se puede facturar más adelante o se puede marcar como no imputable, en función de las negociaciones con el cliente.</span><span class="sxs-lookup"><span data-stu-id="46c0e-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
