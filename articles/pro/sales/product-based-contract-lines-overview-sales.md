---
title: Información general de líneas de contrato basadas en productos (lite)
description: En este tema se proporciona información sobre líneas de contrato basadas en productos.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177892"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="50b6e-103">Información general de líneas de contrato basadas en productos (lite)</span><span class="sxs-lookup"><span data-stu-id="50b6e-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="50b6e-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="50b6e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="50b6e-105">Puede crear líneas de contrato basadas en productos en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="50b6e-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="50b6e-106">Las líneas de contrato basadas en productos pueden ser líneas creadas manualmente o artículos del catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="50b6e-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="50b6e-107">Catálogo de productos</span><span class="sxs-lookup"><span data-stu-id="50b6e-107">Product catalog</span></span>

<span data-ttu-id="50b6e-108">Los productos de un catálogo de productos tienen una unidad de venta y una unidad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="50b6e-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="50b6e-109">Si varios productos comparten el mismo conjunto de atributos, puede crear una familia de productos que también tenga esos atributos.</span><span class="sxs-lookup"><span data-stu-id="50b6e-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="50b6e-110">Todos los productos de una familia de productos heredan el mismo conjunto de atributos.</span><span class="sxs-lookup"><span data-stu-id="50b6e-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="50b6e-111">Por ejemplo, una empresa vende licencias de suscripción para distintas clases de software.</span><span class="sxs-lookup"><span data-stu-id="50b6e-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="50b6e-112">Por lo tanto, todo el software de suscripción tendrá los siguientes dos atributos:</span><span class="sxs-lookup"><span data-stu-id="50b6e-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="50b6e-113">Número de usuarios</span><span class="sxs-lookup"><span data-stu-id="50b6e-113">Number of users</span></span>
- <span data-ttu-id="50b6e-114">Duración de la suscripción (en meses)</span><span class="sxs-lookup"><span data-stu-id="50b6e-114">Subscription duration (in months)</span></span>

<span data-ttu-id="50b6e-115">Para mantener este tipo de catálogo, cree una familia de productos que se denomine **Software de suscripción**.</span><span class="sxs-lookup"><span data-stu-id="50b6e-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="50b6e-116">Agregue los atributos, **Número de usuarios** y **Duración de la suscripción** a la familia de productos.</span><span class="sxs-lookup"><span data-stu-id="50b6e-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="50b6e-117">Luego, agregue productos individuales a la familia de productos **Software de suscripción**.</span><span class="sxs-lookup"><span data-stu-id="50b6e-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="50b6e-118">Agregar artículos del catálogo de productos a un contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="50b6e-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="50b6e-119">Los contratos de proyecto tienen secciones para dos clases de líneas, basadas en proyecto y basadas en productos.</span><span class="sxs-lookup"><span data-stu-id="50b6e-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="50b6e-120">Las líneas basadas en productos incluyen todos los productos y unidades en la lista de precios de productos en el contrato.</span><span class="sxs-lookup"><span data-stu-id="50b6e-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="50b6e-121">Los productos que no forman parte de la lista de productos del contrato pueden agregarse.</span><span class="sxs-lookup"><span data-stu-id="50b6e-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="50b6e-122">Puede seleccionar productos de otras listas de precios o directamente del catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="50b6e-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="50b6e-123">Cuando seleccione productos directamente de un catálogo de productos, la lista de precios predeterminada de ese producto se utilizará para el precio de venta del producto.</span><span class="sxs-lookup"><span data-stu-id="50b6e-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="50b6e-124">Si no se establece una lista de precios predeterminada, el precio se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="50b6e-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="50b6e-125">Si una línea de contrato se basa en un catálogo de productos, puede reemplazar el precio de venta directamente en la línea.</span><span class="sxs-lookup"><span data-stu-id="50b6e-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="50b6e-126">Una línea de contrato tiene el campo **Precios** con los dos valores:</span><span class="sxs-lookup"><span data-stu-id="50b6e-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="50b6e-127">**Reemplazar precio**</span><span class="sxs-lookup"><span data-stu-id="50b6e-127">**Override pricing**</span></span>
- <span data-ttu-id="50b6e-128">**Usar valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="50b6e-128">**Use default**</span></span>

<span data-ttu-id="50b6e-129">Si establece el campo **Precios** a **Reemplazar precio**, no se establece el precio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="50b6e-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="50b6e-130">Especifique el precio para el producto de línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="50b6e-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="50b6e-131">Si configura el campo en **Usar predeterminado**, se utiliza el precio de venta predeterminado y el campo no se puede editar.</span><span class="sxs-lookup"><span data-stu-id="50b6e-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="50b6e-132">Después de instalar Project Operations, los precios de venta predeterminados se introducen en las líneas basadas en productos en un contrato.</span><span class="sxs-lookup"><span data-stu-id="50b6e-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="50b6e-133">El campo **Precios** se establece en **Reemplazar precio** para que pueda editar el precio predeterminado en las líneas de contrato.</span><span class="sxs-lookup"><span data-stu-id="50b6e-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="50b6e-134">Se trata de una invalidación específica de Project Operations para el comportamiento de las líneas basadas en productos en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="50b6e-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
