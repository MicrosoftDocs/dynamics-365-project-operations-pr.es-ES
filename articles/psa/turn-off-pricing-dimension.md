---
title: Desactivación de una dimensión de precios
description: En este tema se muestra cómo configurar dimensiones de precios en la solución de Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281859"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="73832-103">Desactivación de una dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="73832-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="73832-104">Es posible que deba revisar y actualizar su estrategia de precios cada pocos años.</span><span class="sxs-lookup"><span data-stu-id="73832-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="73832-105">Cualquier actualización que realice puede precisar que tenga que desactivar una dimensión de precios existente y crear una nueva.</span><span class="sxs-lookup"><span data-stu-id="73832-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="73832-106">Por ejemplo, es posible que antes haya fijado el precio por **Rol**, pero que ahora decida fijar el precio por **Experiencia laboral**.</span><span class="sxs-lookup"><span data-stu-id="73832-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="73832-107">Esto puede requerir que desactive el **Rol** como dimensión de precios y cree **Experiencia laboral** como una nueva dimensión de precios.</span><span class="sxs-lookup"><span data-stu-id="73832-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="73832-108">La desactivación de una dimensión de precios, sin importar si es de fábrica o personalizada, se puede hacer mediante el establecimiento de los campos **Aplicable a costes** y **Aplicable a ventas** de la dimensión de precios en **No**.</span><span class="sxs-lookup"><span data-stu-id="73832-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="73832-109">Sin embargo, cuando realice este procedimiento, es posible que reciba el siguiente mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="73832-109">However, when you do this, you might receive the following error message.</span></span>

![Error de proceso de negocio probable al desactivar una dimensión de precios](media/Business-Process-Error.png)


<span data-ttu-id="73832-111">Este mensaje de error indica que hay registros de precios que se configuraron previamente para la dimensión que se está desactivando.</span><span class="sxs-lookup"><span data-stu-id="73832-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="73832-112">Todos los registros **Precio de rol** e **Incremento del precio de rol** que hacen referencia a una dimensión deben eliminarse antes de que la aplicabilidad de la dimensión pueda fijarse en **No**.</span><span class="sxs-lookup"><span data-stu-id="73832-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="73832-113">Esta regla se aplica tanto a las dimensiones de precios listas para usar como a las dimensiones de precios personalizadas que pueda haber creado.</span><span class="sxs-lookup"><span data-stu-id="73832-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="73832-114">La razón de esta validación se debe a que Project Service tiene la restricción de que cada registro **Precio de rol** debe tener una combinación única de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="73832-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="73832-115">Por ejemplo, en una lista de precios llamada **Tasas de costes de Estados Unidos en 2018**, tendrá las siguientes filas **Precio de rol**.</span><span class="sxs-lookup"><span data-stu-id="73832-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="73832-116">Título estándar</span><span class="sxs-lookup"><span data-stu-id="73832-116">Standard Title</span></span>         | <span data-ttu-id="73832-117">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="73832-117">Org Unit</span></span>    |<span data-ttu-id="73832-118">Unidad</span><span class="sxs-lookup"><span data-stu-id="73832-118">Unit</span></span>   |<span data-ttu-id="73832-119">Precio</span><span class="sxs-lookup"><span data-stu-id="73832-119">Price</span></span>  |<span data-ttu-id="73832-120">Divisa</span><span class="sxs-lookup"><span data-stu-id="73832-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="73832-121">Ingeniero de sistemas</span><span class="sxs-lookup"><span data-stu-id="73832-121">Systems Engineer</span></span>|<span data-ttu-id="73832-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="73832-122">Contoso US</span></span>|<span data-ttu-id="73832-123">Hour</span><span class="sxs-lookup"><span data-stu-id="73832-123">Hour</span></span>| <span data-ttu-id="73832-124">100</span><span class="sxs-lookup"><span data-stu-id="73832-124">100</span></span>|<span data-ttu-id="73832-125">USD</span><span class="sxs-lookup"><span data-stu-id="73832-125">USD</span></span>|
| <span data-ttu-id="73832-126">Ingeniero de sistemas sénior</span><span class="sxs-lookup"><span data-stu-id="73832-126">Senior Systems Engineer</span></span>|<span data-ttu-id="73832-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="73832-127">Contoso US</span></span>|<span data-ttu-id="73832-128">Hour</span><span class="sxs-lookup"><span data-stu-id="73832-128">Hour</span></span>| <span data-ttu-id="73832-129">150</span><span class="sxs-lookup"><span data-stu-id="73832-129">150</span></span>| <span data-ttu-id="73832-130">USD</span><span class="sxs-lookup"><span data-stu-id="73832-130">USD</span></span>|


<span data-ttu-id="73832-131">Cuando desactive **Título estándar** como la dimensión de precios, y el motor de precios de Project Service busque un precio, solo utilizará el valor de **Unidad organizativa** del contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="73832-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="73832-132">Si la **Unidad organizativa** del contexto de entrada es "Contoso Estados Unidos", el resultado será no determinista porque ambas filas coincidirán.</span><span class="sxs-lookup"><span data-stu-id="73832-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="73832-133">Para evitar este escenario, cuando cree registros **Precio de rol**, Project Service validará que la combinación de dimensiones sea única.</span><span class="sxs-lookup"><span data-stu-id="73832-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="73832-134">Si la dimensión se desactiva después de que se creen los registros de **Precio de rol**, esta restricción se podrá infringir.</span><span class="sxs-lookup"><span data-stu-id="73832-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="73832-135">Por lo tanto, es necesario que antes de desactivar una dimensión, elimine todas las filas de **Precio de rol** y **Incremento del precio de rol** que tienen ese valor de dimensión completo.</span><span class="sxs-lookup"><span data-stu-id="73832-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]