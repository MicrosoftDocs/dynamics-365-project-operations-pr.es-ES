---
title: Administrar unidades complejas para líneas de contratos basadas en productos (lite)
description: Este tema proporciona información sobre cómo respaldar la venta de productos basados en suscripción.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273354"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="070e5-103">Administrar unidades complejas para líneas de contratos basadas en productos (lite)</span><span class="sxs-lookup"><span data-stu-id="070e5-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="070e5-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="070e5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="070e5-105">Dynamics 365 Project Operations utiliza factores de cantidad para respaldar la venta de productos basados ​​en suscripción.</span><span class="sxs-lookup"><span data-stu-id="070e5-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="070e5-106">Para productos basados ​​en suscripción, la cantidad en la línea de contrato o de contrato del proyecto se expresa como el número de meses de usuario.</span><span class="sxs-lookup"><span data-stu-id="070e5-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="070e5-107">El precio del software de suscripción se almacena en el catálogo como el precio por usuario, por mes.</span><span class="sxs-lookup"><span data-stu-id="070e5-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="070e5-108">Durante el proceso de venta, el precio en la línea de contrato suele ser el precio por usuario, por mes que negoció y descontó el agente de ventas.</span><span class="sxs-lookup"><span data-stu-id="070e5-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="070e5-109">Cada operación tiene un número diferente de usuarios y un número diferente de meses de suscripción.</span><span class="sxs-lookup"><span data-stu-id="070e5-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="070e5-110">La cantidad que se utiliza para calcular la cantidad de la línea de contrato es un producto de la cantidad de usuarios y la cantidad de meses de suscripción.</span><span class="sxs-lookup"><span data-stu-id="070e5-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="070e5-111">Para respaldar este tipo de venta, Project Operations admite el concepto de *factores de cantidad*.</span><span class="sxs-lookup"><span data-stu-id="070e5-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="070e5-112">Los factores de cantidad dependen de los atributos del producto.</span><span class="sxs-lookup"><span data-stu-id="070e5-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="070e5-113">Cuando configura propiedades específicas para un producto, puede marcar un subconjunto de esas propiedades, o todas las propiedades, como factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="070e5-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="070e5-114">Project Operations valida que solo las propiedades numéricas o las propiedades del producto que tienen un tipo de datos numéricos se marcan como factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="070e5-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="070e5-115">Cuando un producto con factores de cantidad configurados se agrega a una línea de contrato, el campo **Cantidad** pasa a ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="070e5-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="070e5-116">Después de introducir valores para las propiedades del producto que son factores de cantidad, Project Operations calcula la cantidad de la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="070e5-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="070e5-117">Por ejemplo, Dynamics 365 Sales podría tener las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="070e5-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="070e5-118">**Número de usuarios**: el número de usuarios.</span><span class="sxs-lookup"><span data-stu-id="070e5-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="070e5-119">**Número de meses**: el número de meses de suscripción.</span><span class="sxs-lookup"><span data-stu-id="070e5-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="070e5-120">**SKU del producto**: la unidad de mantenimiento de existencias (SKU) del producto.</span><span class="sxs-lookup"><span data-stu-id="070e5-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="070e5-121">Las propiedades **Número de usuarios** y **Número de meses** se pueden marcar como factores de cantidad editando las propiedades de la línea de productos.</span><span class="sxs-lookup"><span data-stu-id="070e5-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="070e5-122">Para crear factores de cantidad a partir de las propiedades del producto, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="070e5-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="070e5-123">Sobre **Project Operations**, seleccione **Ventas-Productos**.</span><span class="sxs-lookup"><span data-stu-id="070e5-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="070e5-124">Abra el producto para el que necesita configurar factores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="070e5-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="070e5-125">Asegúrese de que el producto ya tenga las propiedades configuradas.</span><span class="sxs-lookup"><span data-stu-id="070e5-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="070e5-126">Sobre la página **Información del proyecto**, seleccione la pestaña **Factores de cantidad**.</span><span class="sxs-lookup"><span data-stu-id="070e5-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="070e5-127">En la subcuadrícula, seleccione **+ Cálculo de nuevo campo**.</span><span class="sxs-lookup"><span data-stu-id="070e5-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="070e5-128">Introduzca el nombre del **factor de cantidad** y seleccione el valor de propiedad que se asigna al cálculo del campo.</span><span class="sxs-lookup"><span data-stu-id="070e5-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="070e5-129">Guardar y cerrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="070e5-129">Save and close the form.</span></span>
7. <span data-ttu-id="070e5-130">Repita los pasos 2 a 6 para todas las propiedades que juntas compondrán la cantidad para la línea de contrato basada en productos.</span><span class="sxs-lookup"><span data-stu-id="070e5-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="070e5-131">Con los factores de cantidad configurados, cuando el usuario crea una línea de contrato para este producto, la cantidad de la línea de contrato se bloquea.</span><span class="sxs-lookup"><span data-stu-id="070e5-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="070e5-132">Luego, la cantidad se calcula como un producto de los valores de propiedad para esa línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="070e5-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]