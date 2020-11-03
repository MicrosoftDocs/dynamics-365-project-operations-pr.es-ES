---
title: Configuración de lista de precios de venta
description: En este tema se proporciona información sobre las listas de precios de ventas para precios de proyecto.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085203"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="6726f-103">Configuración de lista de precios de venta</span><span class="sxs-lookup"><span data-stu-id="6726f-103">Sales price list setup</span></span>

<span data-ttu-id="6726f-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="6726f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6726f-105">Para los contratos y las ofertas de proyecto, la lista de precios de proyectos cuenta con un patrón de reemplazo de precios distinto que el de la lista de precios de productos.</span><span class="sxs-lookup"><span data-stu-id="6726f-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="6726f-106">En una línea de oferta basada en un catálogo de productos, puede reemplazar el precio de los roles y las categorías directamente en la línea de oferta, porque cada línea de la oferta apunta exactamente a un elemento del catálogo.</span><span class="sxs-lookup"><span data-stu-id="6726f-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="6726f-107">Sin embargo, en una línea de oferta basada en un proyecto, no puede reemplazar el precio de los roles y las categorías directamente en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="6726f-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="6726f-108">Puede utilizar la lista de precios de proyecto para trabajar con los dos patrones de reemplazo distintos.</span><span class="sxs-lookup"><span data-stu-id="6726f-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="6726f-109">Se recomienda disponer de una lista de precios independiente para sus recursos de proyecto y sus elementos del catálogo debido a las diferencias de comportamiento entre las dos al reemplazar el cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="6726f-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="6726f-110">Cada una de las siguientes entidades puede tener una o varias listas de precios de ventas asociadas para el cálculo de precios de proyecto:</span><span class="sxs-lookup"><span data-stu-id="6726f-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="6726f-111">Cliente (cuenta)</span><span class="sxs-lookup"><span data-stu-id="6726f-111">Customer (account)</span></span> 
- <span data-ttu-id="6726f-112">Oportunidad</span><span class="sxs-lookup"><span data-stu-id="6726f-112">Opportunity</span></span> 
- <span data-ttu-id="6726f-113">Oferta</span><span class="sxs-lookup"><span data-stu-id="6726f-113">Quote</span></span> 
- <span data-ttu-id="6726f-114">Contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="6726f-114">Project Contract</span></span>

<span data-ttu-id="6726f-115">La asociación de estas entidades a una lista de precios se indica con las listas de precios de proyecto.</span><span class="sxs-lookup"><span data-stu-id="6726f-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="6726f-116">Puede asociar una o más listas de precios a las entidades de ventas Cliente, Oportunidad, Oferta y Contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="6726f-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="6726f-117">La lista de precios de proyecto predeterminada no se introduce automáticamente en los registros de cliente.</span><span class="sxs-lookup"><span data-stu-id="6726f-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="6726f-118">Sin embargo, puede adjuntar manualmente una lista de precios de proyecto al registro de cliente.</span><span class="sxs-lookup"><span data-stu-id="6726f-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="6726f-119">No obstante, deberá adjuntar manualmente una lista de precios de proyecto solo cuando tenga un acuerdo de precios personalizado con el cliente.</span><span class="sxs-lookup"><span data-stu-id="6726f-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="6726f-120">Cuando una lista de precios de proyecto se adjunta una entidad de ventas, se valida la información siguiente:</span><span class="sxs-lookup"><span data-stu-id="6726f-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="6726f-121">Si la lista de precios tiene un contexto de **Ventas**.</span><span class="sxs-lookup"><span data-stu-id="6726f-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="6726f-122">Si la divisa de la lista de precios coincide con la divisa del cliente.</span><span class="sxs-lookup"><span data-stu-id="6726f-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="6726f-123">En un contrato de proyecto, se usa el siguiente orden de precedencia para establecer automáticamente las listas de precios de proyecto relacionadas:</span><span class="sxs-lookup"><span data-stu-id="6726f-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="6726f-124">Oferta</span><span class="sxs-lookup"><span data-stu-id="6726f-124">Quote</span></span>
2. <span data-ttu-id="6726f-125">Oportunidad</span><span class="sxs-lookup"><span data-stu-id="6726f-125">Opportunity</span></span>
3. <span data-ttu-id="6726f-126">Cliente</span><span class="sxs-lookup"><span data-stu-id="6726f-126">Customer</span></span> 
4. <span data-ttu-id="6726f-127">Configuración global</span><span class="sxs-lookup"><span data-stu-id="6726f-127">Global settings</span></span> 

<span data-ttu-id="6726f-128">Cuando una lista de precios de proyecto se especifica de forma predeterminada, el sistema valida que la divisa coincida con la divisa del cliente y que las listas de precios predeterminadas que se han especificado tengan un contexto de **Ventas**.</span><span class="sxs-lookup"><span data-stu-id="6726f-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="6726f-129">Puede asociar varias listas de precios de proyecto a las entidades Cliente, Oportunidad, Oferta y Contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="6726f-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="6726f-130">Esta funcionalidad admite precios predeterminados con fecha específica para contratos de proyectos de larga duración en los que es posible que necesite más de una lista de precios para las actualizaciones de precios que se producen debido a la inflación.</span><span class="sxs-lookup"><span data-stu-id="6726f-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="6726f-131">Sin embargo, si las listas de precios que asocie con las entidades Cliente, Oportunidad, Oferta o Contrato de proyecto tienen validez de fecha que se solapan, es posible que los precios predeterminados sean incorrectos.</span><span class="sxs-lookup"><span data-stu-id="6726f-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="6726f-132">Por lo tanto, debe asegurarse de que no se asocian a dichas entidades listas de precios de proyecto que tienen fechas de validez que se solapan.</span><span class="sxs-lookup"><span data-stu-id="6726f-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
