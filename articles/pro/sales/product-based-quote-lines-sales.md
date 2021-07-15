---
title: Información general sobre líneas de ofertas basadas en productos (lite)
description: En este tema se proporciona información sobre el trabajo con líneas de oferta basadas en producto.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369847"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="95f32-103">Información general sobre líneas de ofertas basadas en productos (lite)</span><span class="sxs-lookup"><span data-stu-id="95f32-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="95f32-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="95f32-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="95f32-105">Puede crear líneas de oferta basadas en productos en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="95f32-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="95f32-106">Las líneas de oferta basadas en productos pueden agregarse manualmente o ser artículos del catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="95f32-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="95f32-107">Catálogo de productos</span><span class="sxs-lookup"><span data-stu-id="95f32-107">Product catalog</span></span>

<span data-ttu-id="95f32-108">Cada producto de un catálogo de productos tiene una unidad de venta y una unidad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="95f32-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="95f32-109">Si varios productos comparten el mismo conjunto de atributos, puede crear una familia de productos que comparta esos atributos.</span><span class="sxs-lookup"><span data-stu-id="95f32-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="95f32-110">Por ejemplo, una empresa vende licencias de suscripción para distintas clases de software.</span><span class="sxs-lookup"><span data-stu-id="95f32-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="95f32-111">Por lo tanto, todo el software de suscripción tendrá los siguientes dos atributos:</span><span class="sxs-lookup"><span data-stu-id="95f32-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="95f32-112">Número de usuarios</span><span class="sxs-lookup"><span data-stu-id="95f32-112">Number of users</span></span>
- <span data-ttu-id="95f32-113">Una duración de suscripción medida en meses</span><span class="sxs-lookup"><span data-stu-id="95f32-113">A subscription duration measured in months</span></span>

<span data-ttu-id="95f32-114">Para mantener este tipo de catálogo, cree una familia de productos que se denomine **Software de suscripción** y agregue el número de usuarios y la duración de la suscripción como atributos.</span><span class="sxs-lookup"><span data-stu-id="95f32-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="95f32-115">A continuación, puede agregar productos individuales a la familia de productos **Software de suscripción**.</span><span class="sxs-lookup"><span data-stu-id="95f32-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="95f32-116">Agregar artículos del catálogo de productos a una oferta de proyecto</span><span class="sxs-lookup"><span data-stu-id="95f32-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="95f32-117">Las páginas **Oferta de proyecto** y **Contrato de proyecto** tienen secciones para dos tipos de líneas: líneas basadas en proyectos y líneas basadas en productos.</span><span class="sxs-lookup"><span data-stu-id="95f32-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="95f32-118">Para las líneas basadas en producto, la lista desplegable en la línea de oferta o en la línea de contrato del proyecto incluye todos los productos y unidades en la lista de precios de productos.</span><span class="sxs-lookup"><span data-stu-id="95f32-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="95f32-119">También puede agregar productos que no forman parte de la lista de precios de productos.</span><span class="sxs-lookup"><span data-stu-id="95f32-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="95f32-120">Además, puede seleccionar productos de otras listas de precios o directamente desde el catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="95f32-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="95f32-121">Cuando seleccione productos directamente de un catálogo de productos, la lista de precios predeterminada de ese producto se utilizará para obtener el precio de venta del producto.</span><span class="sxs-lookup"><span data-stu-id="95f32-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="95f32-122">Si no se establece una lista de precios predeterminada, el precio se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="95f32-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="95f32-123">Cuando una línea de oferta se basa en un catálogo de productos, puede reemplazar el precio de venta directamente en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="95f32-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="95f32-124">Una línea de oferta del campo **Precios** con dos valores disponibles:</span><span class="sxs-lookup"><span data-stu-id="95f32-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="95f32-125">**Reemplazar precios**</span><span class="sxs-lookup"><span data-stu-id="95f32-125">**Override Pricing**</span></span>
- <span data-ttu-id="95f32-126">**Usar valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="95f32-126">**Use Default**</span></span>

<span data-ttu-id="95f32-127">Si selecciona **Anular precios**, el precio predeterminado no está establecido.</span><span class="sxs-lookup"><span data-stu-id="95f32-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="95f32-128">En su lugar, debe escribir un precio para el producto en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="95f32-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="95f32-129">Si selecciona **Uso por defecto**, se utiliza el precio de venta predeterminado y el campo se bloquea para su edición.</span><span class="sxs-lookup"><span data-stu-id="95f32-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="95f32-130">Los precios de venta predeterminados se introducen en las líneas basadas en productos de una oferta.</span><span class="sxs-lookup"><span data-stu-id="95f32-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="95f32-131">El campo **Precios** se establece en **Reemplazar precios** para que pueda editar el precio predeterminado en las líneas de oferta.</span><span class="sxs-lookup"><span data-stu-id="95f32-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="95f32-132">Se trata de una invalidación específica de Project Operations para el comportamiento de las líneas basadas en productos en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="95f32-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]