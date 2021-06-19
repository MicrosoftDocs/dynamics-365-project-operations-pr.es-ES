---
title: Uso de un campo existente en Project Service como dimensión de precios
description: En este tema se proporciona información sobre el uso de campos existentes de Project Service como dimensiones de precios.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008107"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="be6f3-103">Uso de un campo existente en Project Service como dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="be6f3-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="be6f3-104">Project Service Automation (PSA) tiene muchos campos en la entidad **Datos reales** que se pueden usar como dimensiones de precios para precios basados en recursos en organizaciones de proyectos.</span><span class="sxs-lookup"><span data-stu-id="be6f3-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="be6f3-105">Por ejemplo, un campo común es **Recurso que se puede reservar**.</span><span class="sxs-lookup"><span data-stu-id="be6f3-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="be6f3-106">Es posible que las compañías más pequeñas, con menos de 20-30 recursos facturables, consideren que tener tasas de coste y facturas específicas para cada recurso es un enfoque más simple.</span><span class="sxs-lookup"><span data-stu-id="be6f3-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="be6f3-107">Sin embargo, a medida que crece el personal facturable, las tasas específicas podrían ser muy difíciles de mantener, ya que el coste de los recursos y las tasas de facturación comienzan a variar a medida que los recursos ascienden, adquieren más experiencia o consiguen un conjunto de habilidades diferente.</span><span class="sxs-lookup"><span data-stu-id="be6f3-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="be6f3-108">Puesto que este enfoque todavía funciona para compañías de cierto tamaño, consulte [Usar un recurso reservable como dimensión de precios](bookable-resource-pricing-dimension.md) para comprender cómo se puede usar un campo de Project Service existente como dimensión de precios.</span><span class="sxs-lookup"><span data-stu-id="be6f3-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="be6f3-109">Otro ejemplo es el de la categoría de transacción.</span><span class="sxs-lookup"><span data-stu-id="be6f3-109">Another example is that of transaction category.</span></span> <span data-ttu-id="be6f3-110">Los clientes y los implementadores han usado la categoría de transacción en PSA para clasificar el trabajo y usar el campo para determinar el precio y el coste según la categoría de trabajo.</span><span class="sxs-lookup"><span data-stu-id="be6f3-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="be6f3-111">Para obtener más información, consulte [Uso de la categoría de transacción como una dimensión de precios](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="be6f3-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]