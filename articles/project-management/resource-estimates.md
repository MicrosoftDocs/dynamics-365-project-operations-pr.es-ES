---
title: Estimaciones de recursos
description: En este tema se proporciona información sobre cómo se calculan las estimaciones de recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286539"
---
# <a name="resource-estimates"></a><span data-ttu-id="dd4f6-103">Estimaciones de recursos</span><span class="sxs-lookup"><span data-stu-id="dd4f6-103">Resource estimates</span></span>

<span data-ttu-id="dd4f6-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="dd4f6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd4f6-105">Las estimaciones de recursos provienen del esfuerzo por fases que se define en la estructura de descomposición del trabajo, junto con las dimensiones de precios aplicables.</span><span class="sxs-lookup"><span data-stu-id="dd4f6-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="dd4f6-106">Normalmente, el cálculo es **tarifa/hora para cada rol x horas.**</span><span class="sxs-lookup"><span data-stu-id="dd4f6-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="dd4f6-107">El esfuerzo por fases de tiempo para cada recurso se almacena en el registro de asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd4f6-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="dd4f6-108">El precio se almacena en una lista de precios predefinida.</span><span class="sxs-lookup"><span data-stu-id="dd4f6-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="dd4f6-109">La conversión de unidades se aplica según la lista de precios aplicable.</span><span class="sxs-lookup"><span data-stu-id="dd4f6-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimaciones de recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="dd4f6-111">Valores predeterminados de precio y divisa de coste</span><span class="sxs-lookup"><span data-stu-id="dd4f6-111">Default cost price and cost currency</span></span>

<span data-ttu-id="dd4f6-112">Los precios de coste se predeterminan desde la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="dd4f6-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="dd4f6-113">Tarifa de facturación y divisa de ventas predeterminadas</span><span class="sxs-lookup"><span data-stu-id="dd4f6-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="dd4f6-114">Los precios de venta se aplican una vez por oferta.</span><span class="sxs-lookup"><span data-stu-id="dd4f6-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="dd4f6-115">La jerarquía para la lista de precios de venta predeterminada es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd4f6-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="dd4f6-116">Organización</span><span class="sxs-lookup"><span data-stu-id="dd4f6-116">Organization</span></span>
2. <span data-ttu-id="dd4f6-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="dd4f6-117">Customer</span></span>
3. <span data-ttu-id="dd4f6-118">Oferta/contrato</span><span class="sxs-lookup"><span data-stu-id="dd4f6-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]