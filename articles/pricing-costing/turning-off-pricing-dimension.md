---
title: Desactivación de una dimensión de precios
description: En este tema se proporciona información sobre cómo desactivar dimensiones de precios.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274749"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="d5d53-103">Desactivación de una dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="d5d53-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="d5d53-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="d5d53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5d53-105">Es posible que deba revisar y actualizar su estrategia de precios cada pocos años.</span><span class="sxs-lookup"><span data-stu-id="d5d53-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="d5d53-106">Cualquier actualización que realice puede precisar que tenga que desactivar una dimensión de precios existente y crear una nueva.</span><span class="sxs-lookup"><span data-stu-id="d5d53-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="d5d53-107">Por ejemplo, es posible que antes haya fijado el precio por **Rol**, pero que ahora decida fijar el precio por **Experiencia laboral**.</span><span class="sxs-lookup"><span data-stu-id="d5d53-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="d5d53-108">Esto puede requerir que desactive el **Rol** como dimensión de precios y cree **Experiencia laboral** como una nueva dimensión de precios.</span><span class="sxs-lookup"><span data-stu-id="d5d53-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="d5d53-109">La desactivación de una dimensión de precios, sin importar si es de fábrica o personalizada, se puede hacer mediante el establecimiento de los campos **Aplicable a costes** y **Aplicable a ventas** de la dimensión de precios en **No**.</span><span class="sxs-lookup"><span data-stu-id="d5d53-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="d5d53-110">Sin embargo, al hacer esto, es posible que reciba el mensaje de error, **La dimensión de precios no se puede actualizar ni eliminar si hay registros de precios asociados.**</span><span class="sxs-lookup"><span data-stu-id="d5d53-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Error de proceso de negocio probable al desactivar una dimensión de precios](media/Business-Process-Error.png)

<span data-ttu-id="d5d53-112">Este mensaje de error indica que hay registros de precios que se configuraron previamente para la dimensión que se está desactivando.</span><span class="sxs-lookup"><span data-stu-id="d5d53-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="d5d53-113">Todos los registros **Precio de rol** e **Incremento del precio de rol** que hacen referencia a una dimensión deben eliminarse antes de que la aplicabilidad de la dimensión pueda fijarse en **No**.</span><span class="sxs-lookup"><span data-stu-id="d5d53-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="d5d53-114">Esta regla se aplica tanto a las dimensiones de precios listas para usar como a las dimensiones de precios personalizadas que pueda haber creado.</span><span class="sxs-lookup"><span data-stu-id="d5d53-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="d5d53-115">La razón de esta validación se debe a que cada registro **Precio de rol** debe tener una combinación única de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="d5d53-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="d5d53-116">Por ejemplo, en una lista de precios llamada **Tasas de costes de Estados Unidos en 2018**, tendrá las siguientes filas **Precio de rol**.</span><span class="sxs-lookup"><span data-stu-id="d5d53-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="d5d53-117">Título estándar</span><span class="sxs-lookup"><span data-stu-id="d5d53-117">Standard Title</span></span>         | <span data-ttu-id="d5d53-118">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="d5d53-118">Org Unit</span></span>    |<span data-ttu-id="d5d53-119">Unidad</span><span class="sxs-lookup"><span data-stu-id="d5d53-119">Unit</span></span>   |<span data-ttu-id="d5d53-120">Precio</span><span class="sxs-lookup"><span data-stu-id="d5d53-120">Price</span></span>  |<span data-ttu-id="d5d53-121">Divisa</span><span class="sxs-lookup"><span data-stu-id="d5d53-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="d5d53-122">Ingeniero de sistemas</span><span class="sxs-lookup"><span data-stu-id="d5d53-122">Systems Engineer</span></span>|<span data-ttu-id="d5d53-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d5d53-123">Contoso US</span></span>|<span data-ttu-id="d5d53-124">Hour</span><span class="sxs-lookup"><span data-stu-id="d5d53-124">Hour</span></span>| <span data-ttu-id="d5d53-125">100</span><span class="sxs-lookup"><span data-stu-id="d5d53-125">100</span></span>|<span data-ttu-id="d5d53-126">USD</span><span class="sxs-lookup"><span data-stu-id="d5d53-126">USD</span></span>|
| <span data-ttu-id="d5d53-127">Ingeniero de sistemas sénior</span><span class="sxs-lookup"><span data-stu-id="d5d53-127">Senior Systems Engineer</span></span>|<span data-ttu-id="d5d53-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d5d53-128">Contoso US</span></span>|<span data-ttu-id="d5d53-129">Hour</span><span class="sxs-lookup"><span data-stu-id="d5d53-129">Hour</span></span>| <span data-ttu-id="d5d53-130">150</span><span class="sxs-lookup"><span data-stu-id="d5d53-130">150</span></span>| <span data-ttu-id="d5d53-131">USD</span><span class="sxs-lookup"><span data-stu-id="d5d53-131">USD</span></span>|


<span data-ttu-id="d5d53-132">Cuando desactive **Título estándar** como la dimensión de precios, y el motor de precios busque un precio, solo utilizará el valor de **Unidad organizativa** del contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5d53-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="d5d53-133">Si la **Unidad organizativa** del contexto de entrada es "Contoso Estados Unidos", el resultado será no determinista porque ambas filas coincidirán.</span><span class="sxs-lookup"><span data-stu-id="d5d53-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="d5d53-134">Para evitar este escenario, cuando cree registros **Precio de rol**, el sistema validará que la combinación de dimensiones sea única.</span><span class="sxs-lookup"><span data-stu-id="d5d53-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="d5d53-135">Si la dimensión se desactiva después de que se creen los registros de **Precio de rol**, esta restricción se podrá infringir.</span><span class="sxs-lookup"><span data-stu-id="d5d53-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="d5d53-136">Por lo tanto, es necesario que antes de desactivar una dimensión, elimine todas las filas de **Precio de rol** y **Incremento del precio de rol** que tienen ese valor de dimensión completo.</span><span class="sxs-lookup"><span data-stu-id="d5d53-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]