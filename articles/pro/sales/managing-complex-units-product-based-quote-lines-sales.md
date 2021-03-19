---
title: Administración de unidades complejas, como por usuario, por mes para líneas de ofertas basadas en productos (lite)
description: Este tema proporciona información sobre la administración de unidades complejas para líneas de oferta basadas en productos.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272904"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="1f684-103">Administración de unidades complejas, como por usuario, por mes para líneas de ofertas basadas en productos (lite)</span><span class="sxs-lookup"><span data-stu-id="1f684-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="1f684-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="1f684-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1f684-105">Dynamics 365 Project Operations utiliza factores de cantidad para respaldar la venta de productos basados ​​en suscripción.</span><span class="sxs-lookup"><span data-stu-id="1f684-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="1f684-106">Para productos basados ​​en suscripción, la cantidad en la línea de oferta o contrato del proyecto se expresa como el número de meses de usuario.</span><span class="sxs-lookup"><span data-stu-id="1f684-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="1f684-107">Por lo general, el precio del software de suscripción se almacena en el catálogo como el precio por usuario por mes.</span><span class="sxs-lookup"><span data-stu-id="1f684-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="1f684-108">Durante el proceso de venta, el precio en la línea de oferta suele ser el precio por usuario, por mes que negoció y descontó el agente de ventas de TI.</span><span class="sxs-lookup"><span data-stu-id="1f684-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="1f684-109">Cada operación tiene un número diferente de usuarios y un número diferente de meses de suscripción.</span><span class="sxs-lookup"><span data-stu-id="1f684-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="1f684-110">La cantidad que se utiliza para calcular la línea de oferta es un producto de la cantidad de usuarios y la cantidad de meses de suscripción.</span><span class="sxs-lookup"><span data-stu-id="1f684-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="1f684-111">Para respaldar este tipo de venta, Project Operations introdujo el concepto de factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="1f684-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="1f684-112">Los factores de cantidad dependen de los atributos del producto en Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1f684-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="1f684-113">Cuando configura propiedades específicas para un producto, Project Operations le permite marcar un subconjunto de esas propiedades, o todas ellas, como factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="1f684-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="1f684-114">Project Operations valida que solo las propiedades numéricas o las propiedades del producto que tienen un tipo de datos numéricos se marcan como factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="1f684-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="1f684-115">Cuando agrega un producto con factores de cantidad a una línea de oferta, el campo **Cantidad** pasa a ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1f684-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="1f684-116">Después de introducir valores para las propiedades del producto que son factores de cantidad, Project Operations calcula la cantidad de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="1f684-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="1f684-117">Por ejemplo, Dynamics 365 Sales podría tener las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="1f684-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="1f684-118">**Número de usuarios**: el número de usuarios</span><span class="sxs-lookup"><span data-stu-id="1f684-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="1f684-119">**Número de meses**: el número de meses de suscripción</span><span class="sxs-lookup"><span data-stu-id="1f684-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="1f684-120">**SKU de producto**</span><span class="sxs-lookup"><span data-stu-id="1f684-120">**Product SKU**</span></span>

<span data-ttu-id="1f684-121">Puede marcar las propiedades **Número de usuarios** y **Número de meses** como factores de cantidad editando las propiedades de la línea de productos.</span><span class="sxs-lookup"><span data-stu-id="1f684-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="1f684-122">Para crear factores de cantidad a partir de las propiedades del producto, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="1f684-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="1f684-123">En el panel de navegación izquierdo Operaciones del proyecto, vaya a **Ventas** > **Productos**.</span><span class="sxs-lookup"><span data-stu-id="1f684-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="1f684-124">Abra el producto para el que necesita configurar factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="1f684-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="1f684-125">Asegúrese de que el producto ya tenga las propiedades configuradas.</span><span class="sxs-lookup"><span data-stu-id="1f684-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="1f684-126">En la página **Información del proyecto** del producto, seleccione la pestaña **Factores de cantidad**.</span><span class="sxs-lookup"><span data-stu-id="1f684-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="1f684-127">En la subcuadrícula, seleccione **+ Cálculo de nuevo campo**.</span><span class="sxs-lookup"><span data-stu-id="1f684-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="1f684-128">Introduzca el nombre del factor de cantidad y seleccione el valor de propiedad que se asigna al cálculo del campo.</span><span class="sxs-lookup"><span data-stu-id="1f684-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="1f684-129">Guardar y cerrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="1f684-129">Save and close the form.</span></span> <span data-ttu-id="1f684-130">Repita estos pasos para todas las propiedades que se utilizarán para calcular la cantidad de la línea de oferta basada en el producto.</span><span class="sxs-lookup"><span data-stu-id="1f684-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="1f684-131">Cuando crea una línea de oferta basada en productos para un producto, la cantidad de la línea de oferta se bloqueará.</span><span class="sxs-lookup"><span data-stu-id="1f684-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="1f684-132">La cantidad se calculará como un producto de los valores de propiedad que introduzca para esa línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="1f684-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]