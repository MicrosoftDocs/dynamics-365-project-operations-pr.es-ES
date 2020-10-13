---
title: Líneas de oportunidad basadas en productos
description: Este tema proporciona información sobre artículos de líneas de oportunidades basadas en proyectos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896257"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="3dd2e-103">Líneas de oportunidad basadas en productos</span><span class="sxs-lookup"><span data-stu-id="3dd2e-103">Product-based opportunity lines</span></span>

<span data-ttu-id="3dd2e-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="3dd2e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3dd2e-105">Las líneas de oportunidad basadas en productos son elementos de línea de la oportunidad.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="3dd2e-106">Estas líneas se entregan al cliente como artículos de línea distintos en la factura final sin ningún otro servicio de valor agregado.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="3dd2e-107">El gasto y el consumo asociados no se registran en las tareas de ningún proyecto relacionado.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="3dd2e-108">Las líneas basadas en productos pueden ser artículos de catálogo o productos fuera de catálogo.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="3dd2e-109">La mayor parte de la funcionalidad de las líneas basadas en productos de una oportunidad sigue la funcionalidad proporcionada por la aplicación Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="3dd2e-110">Para obtener más información sobre las líneas de oportunidad basadas en productos, consulte [Agregar productos a una oportunidad](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="3dd2e-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="3dd2e-111">Un concepto sobre las líneas de oportunidades basadas en productos que es específico de las oportunidades basadas en proyectos es **Presupuesto del cliente**.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="3dd2e-112">Utilice este campo para realizar un seguimiento de la cantidad que el cliente está dispuesto a pagar por el artículo de línea.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="3dd2e-113">Si el método de ingresos del resumen de oportunidades se establece en **Calculado por el sistema**, los valores del presupuesto del cliente en las líneas basadas en productos y proyectos se resumen para calcular los ingresos estimados.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
