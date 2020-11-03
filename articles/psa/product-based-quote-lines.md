---
title: Líneas de oferta basadas en producto
description: En este tema se proporciona información sobre líneas de oferta basadas en productos.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085328"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="bfff9-103">Líneas de oferta basadas en producto</span><span class="sxs-lookup"><span data-stu-id="bfff9-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="bfff9-104">Puede crear líneas de oferta basadas en productos en Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bfff9-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="bfff9-105">Las líneas de oferta basadas en productos pueden ser líneas de "escritura" o artículos del catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="bfff9-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="bfff9-106">Catálogo de productos</span><span class="sxs-lookup"><span data-stu-id="bfff9-106">Product catalog</span></span>

<span data-ttu-id="bfff9-107">Los productos de un catálogo de productos de Dynamics 365 tienen una unidad de venta y una unidad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bfff9-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="bfff9-108">Si varios productos comparten el mismo conjunto de atributos, puede crear una familia de productos que también tenga esos atributos.</span><span class="sxs-lookup"><span data-stu-id="bfff9-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="bfff9-109">Todos los productos de una familia de productos heredan el mismo conjunto de atributos.</span><span class="sxs-lookup"><span data-stu-id="bfff9-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="bfff9-110">Por ejemplo, una empresa vende licencias de suscripción para una variedad de software.</span><span class="sxs-lookup"><span data-stu-id="bfff9-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="bfff9-111">Por lo tanto, todo el software de suscripción tendrá los siguientes dos atributos:</span><span class="sxs-lookup"><span data-stu-id="bfff9-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="bfff9-112">Número de usuarios</span><span class="sxs-lookup"><span data-stu-id="bfff9-112">Number of users</span></span> 
- <span data-ttu-id="bfff9-113">Duración de la suscripción (en meses)</span><span class="sxs-lookup"><span data-stu-id="bfff9-113">Subscription duration (in months)</span></span>

<span data-ttu-id="bfff9-114">Una buena forma de mantener este tipo de catálogo es crear una familia de productos que se denomine **Software de suscripción** y que tenga como atributos **Número de usuarios** y **Duración de la suscripción**.</span><span class="sxs-lookup"><span data-stu-id="bfff9-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software** , and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="bfff9-115">A continuación, puede agregar productos individuales, como **Dynamics 365 Sales** o **Dynamics 365 Field Service** a la familia de productos de **Software de suscripción**.</span><span class="sxs-lookup"><span data-stu-id="bfff9-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="bfff9-116">Adición de artículos del catálogo de productos a una oferta de proyecto</span><span class="sxs-lookup"><span data-stu-id="bfff9-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="bfff9-117">Las páginas de oferta y contrato de proyecto tienen secciones para dos tipos de líneas: líneas basadas en proyectos y líneas basadas en productos.</span><span class="sxs-lookup"><span data-stu-id="bfff9-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="bfff9-118">Para líneas basadas en productos, Dynamics 365 se usa para agregar artículos de un catálogo de productos a una oferta.</span><span class="sxs-lookup"><span data-stu-id="bfff9-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="bfff9-119">La lista desplegable en la línea de oferta o en la línea de contrato del proyecto incluye todos los productos y unidades en la lista de precios de productos que se adjunta a la oferta o contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="bfff9-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="bfff9-120">También puede agregar productos que no forman parte de la lista de precios de productos de la oferta.</span><span class="sxs-lookup"><span data-stu-id="bfff9-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="bfff9-121">Además, puede seleccionar productos de otras listas de precios, o puede elegir productos directamente desde el catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="bfff9-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="bfff9-122">Cuando seleccione productos directamente de un catálogo de productos, la lista de precios predeterminada de ese producto se utilizará para obtener el precio de venta del producto.</span><span class="sxs-lookup"><span data-stu-id="bfff9-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="bfff9-123">Si no se establece una lista de precios predeterminada, el precio se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="bfff9-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="bfff9-124">Si una línea de oferta se basa en un catálogo de productos, puede reemplazar el precio de venta directamente en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="bfff9-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="bfff9-125">Tenga en cuenta que una línea de oferta en Dynamics 365 tiene un campo **Precios**.</span><span class="sxs-lookup"><span data-stu-id="bfff9-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="bfff9-126">Hay dos valores disponibles:</span><span class="sxs-lookup"><span data-stu-id="bfff9-126">Two values are available:</span></span>

- <span data-ttu-id="bfff9-127">Reemplazar precio</span><span class="sxs-lookup"><span data-stu-id="bfff9-127">Override pricing</span></span>  
- <span data-ttu-id="bfff9-128">Usar valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="bfff9-128">Use default</span></span>

<span data-ttu-id="bfff9-129">Si establece este campo en **Reemplazar precio** , Dynamics 365 no establece un precio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bfff9-129">If you set this field to **Override pricing** , Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="bfff9-130">Debe escribir un precio para el producto en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="bfff9-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="bfff9-131">Si establece este campo en **Usar valor predeterminado** , Dynamics 365 usa el precio de venta predeterminado y bloquea el campo para evitar la edición.</span><span class="sxs-lookup"><span data-stu-id="bfff9-131">If you set this field to **Use default** , Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="bfff9-132">Después de instalar PSA, los precios de venta predeterminados se introducen en las líneas basadas en productos en una oferta.</span><span class="sxs-lookup"><span data-stu-id="bfff9-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="bfff9-133">El campo **Precios** se establece en **Reemplazar precio** para que pueda editar el precio predeterminado en las líneas de oferta.</span><span class="sxs-lookup"><span data-stu-id="bfff9-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Configuración de Reemplazar precio](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="bfff9-135">Factores de cantidad para productos</span><span class="sxs-lookup"><span data-stu-id="bfff9-135">Quantity factors for products</span></span>

<span data-ttu-id="bfff9-136">PSA utiliza factores de cantidad para respaldar la venta de productos basados ​​en suscripción.</span><span class="sxs-lookup"><span data-stu-id="bfff9-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="bfff9-137">Para productos basados ​​en suscripción, la cantidad en la línea de oferta o contrato del proyecto se expresa como el número de meses de usuario.</span><span class="sxs-lookup"><span data-stu-id="bfff9-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="bfff9-138">Por lo general, el precio del software de suscripción se almacena en el catálogo como el precio por usuario por mes.</span><span class="sxs-lookup"><span data-stu-id="bfff9-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="bfff9-139">Sin embargo, puede utilizar otras descripciones de tiempo en su lugar.</span><span class="sxs-lookup"><span data-stu-id="bfff9-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="bfff9-140">Durante el proceso de venta, el precio en la línea de oferta suele ser el precio por usuario, por mes que negoció y descontó el agente de ventas de TI.</span><span class="sxs-lookup"><span data-stu-id="bfff9-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="bfff9-141">Cada operación tiene un número diferente de usuarios y un número diferente de meses de suscripción.</span><span class="sxs-lookup"><span data-stu-id="bfff9-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="bfff9-142">La cantidad que se utiliza para calcular la cantidad de la línea de oferta es un producto de la cantidad de usuarios y la cantidad de meses de suscripción.</span><span class="sxs-lookup"><span data-stu-id="bfff9-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="bfff9-143">Para respaldar este tipo de venta, PSA introdujo el concepto de factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="bfff9-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="bfff9-144">Los factores de cantidad dependen de los atributos del producto en Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bfff9-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="bfff9-145">Cuando configura propiedades específicas para un producto, PSA le permite marcar un subconjunto de esas propiedades, o todas las propiedades, como factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="bfff9-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="bfff9-146">PSA valida que solo las propiedades numéricas o las propiedades del producto que tienen un tipo de datos numéricos se marcan como factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="bfff9-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="bfff9-147">Cuando un producto para el que se configuran los factores de cantidad se agrega a una línea de oferta, el campo **Cantidad** en la línea de oferta se convierte en un campo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bfff9-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="bfff9-148">Después de introducir valores para las propiedades del producto que son factores de cantidad, PSA calcula la cantidad de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="bfff9-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="bfff9-149">Por ejemplo, Dynamics 365 podría tener las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="bfff9-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="bfff9-150">**Número de usuarios** : el número de usuarios.</span><span class="sxs-lookup"><span data-stu-id="bfff9-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="bfff9-151">**Número de meses** : el número de meses de suscripción.</span><span class="sxs-lookup"><span data-stu-id="bfff9-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="bfff9-152">**SKU de producto**</span><span class="sxs-lookup"><span data-stu-id="bfff9-152">**Product SKU**</span></span> 

<span data-ttu-id="bfff9-153">Las propiedades **Número de usuarios** y **Número de meses** se pueden marcar como factores de cantidad editando las propiedades de la línea de productos.</span><span class="sxs-lookup"><span data-stu-id="bfff9-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Marcado de Número de usuarios y Número de meses como factores de calidad](media/basic-guide-11.png)
 
