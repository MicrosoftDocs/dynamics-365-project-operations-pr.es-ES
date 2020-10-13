---
title: Estimaciones de recursos
description: En este tema se proporciona información sobre cómo se calculan las estimaciones de recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928610"
---
# <a name="resource-estimates"></a><span data-ttu-id="bd1de-103">Estimaciones de recursos</span><span class="sxs-lookup"><span data-stu-id="bd1de-103">Resource estimates</span></span>

<span data-ttu-id="bd1de-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="bd1de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bd1de-105">Las estimaciones de recursos provienen del esfuerzo por fases que se define en la estructura de descomposición del trabajo, junto con las dimensiones de precios aplicables.</span><span class="sxs-lookup"><span data-stu-id="bd1de-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="bd1de-106">Normalmente, el cálculo es **tarifa/hora para cada rol x horas.**</span><span class="sxs-lookup"><span data-stu-id="bd1de-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="bd1de-107">El esfuerzo por fases de tiempo para cada recurso se almacena en el registro de asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd1de-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="bd1de-108">El precio se almacena en una lista de precios predefinida.</span><span class="sxs-lookup"><span data-stu-id="bd1de-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="bd1de-109">La conversión de unidades se aplica según la lista de precios aplicable.</span><span class="sxs-lookup"><span data-stu-id="bd1de-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimaciones de recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="bd1de-111">Valores predeterminados de precio y divisa de coste</span><span class="sxs-lookup"><span data-stu-id="bd1de-111">Default cost price and cost currency</span></span>

<span data-ttu-id="bd1de-112">Los precios de coste se predeterminan desde la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="bd1de-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="bd1de-113">Tarifa de facturación y divisa de ventas predeterminadas</span><span class="sxs-lookup"><span data-stu-id="bd1de-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="bd1de-114">Los precios de venta se aplican una vez por oferta.</span><span class="sxs-lookup"><span data-stu-id="bd1de-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="bd1de-115">La jerarquía para la lista de precios de venta predeterminada es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="bd1de-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="bd1de-116">Organización</span><span class="sxs-lookup"><span data-stu-id="bd1de-116">Organization</span></span>
2. <span data-ttu-id="bd1de-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="bd1de-117">Customer</span></span>
3. <span data-ttu-id="bd1de-118">Oferta/contrato</span><span class="sxs-lookup"><span data-stu-id="bd1de-118">Quote/contract</span></span>
