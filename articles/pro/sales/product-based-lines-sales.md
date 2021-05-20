---
title: Líneas de oportunidad basadas en productos (lite)
description: Este tema proporciona información sobre artículos de líneas de oportunidades basadas en proyectos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f7dfabd068e180c7122ede0f79aaebfe220250a1
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949565"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="3d1fd-103">Líneas de oportunidad basadas en productos (lite)</span><span class="sxs-lookup"><span data-stu-id="3d1fd-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="3d1fd-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="3d1fd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3d1fd-105">Las líneas de oportunidad basadas en productos son elementos de línea de la oportunidad.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="3d1fd-106">Estos elementos de línea distintos se encuentran en la factura final que se proporciona al cliente.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="3d1fd-107">La factura no incluye ningún servicio adicional.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="3d1fd-108">El gasto y el consumo asociados no se registran en las tareas de ningún proyecto relacionado.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="3d1fd-109">Las líneas basadas en productos pueden ser artículos de catálogo o productos fuera de catálogo.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="3d1fd-110">La mayor parte de la funcionalidad de las líneas basadas en productos de una oportunidad sigue la funcionalidad proporcionada por la aplicación Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="3d1fd-111">Para obtener más información sobre las líneas de oportunidad basadas en productos, consulte [Agregar productos a una oportunidad](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="3d1fd-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="3d1fd-112">**Presupuesto del cliente** es un concepto específico de las líneas de oportunidad basadas en proyecto.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="3d1fd-113">El campo **Presupuesto del cliente** hace un seguimiento de la cantidad que el cliente está dispuesto a pagar por el artículo.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="3d1fd-114">Cuando el método de ingresos del Resumen de oportunidad es **Calculado por el sistema**, se resumen los valores del presupuesto del cliente en las líneas de oportunidad para calcular los ingresos previstos.</span><span class="sxs-lookup"><span data-stu-id="3d1fd-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]