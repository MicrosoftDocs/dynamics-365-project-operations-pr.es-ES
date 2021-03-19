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
ms.openlocfilehash: 4f8da5258a1dd0aa4229654c0e1e222b8cf3a21a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272634"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="d5da1-103">Líneas de oportunidad basadas en productos (lite)</span><span class="sxs-lookup"><span data-stu-id="d5da1-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="d5da1-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="d5da1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5da1-105">Las líneas de oportunidad basadas en productos son elementos de línea de la oportunidad.</span><span class="sxs-lookup"><span data-stu-id="d5da1-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="d5da1-106">Estos elementos de línea distintos se encuentran en la factura final que se proporciona al cliente.</span><span class="sxs-lookup"><span data-stu-id="d5da1-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="d5da1-107">La factura no incluye ningún servicio adicional.</span><span class="sxs-lookup"><span data-stu-id="d5da1-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="d5da1-108">El gasto y el consumo asociados no se registran en las tareas de ningún proyecto relacionado.</span><span class="sxs-lookup"><span data-stu-id="d5da1-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="d5da1-109">Las líneas basadas en productos pueden ser artículos de catálogo o productos fuera de catálogo.</span><span class="sxs-lookup"><span data-stu-id="d5da1-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="d5da1-110">La mayor parte de la funcionalidad de las líneas basadas en productos de una oportunidad sigue la funcionalidad proporcionada por la aplicación Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d5da1-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="d5da1-111">Para obtener más información sobre las líneas de oportunidad basadas en productos, consulte [Agregar productos a una oportunidad](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="d5da1-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="d5da1-112">**Presupuesto del cliente** es un concepto específico de las líneas de oportunidad basadas en proyecto.</span><span class="sxs-lookup"><span data-stu-id="d5da1-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="d5da1-113">El campo **Presupuesto del cliente** hace un seguimiento de la cantidad que el cliente está dispuesto a pagar por el artículo.</span><span class="sxs-lookup"><span data-stu-id="d5da1-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="d5da1-114">Cuando el método de ingresos del Resumen de oportunidad es **Calculado por el sistema**, se resumen los valores del presupuesto del cliente en las líneas de oportunidad para calcular los ingresos previstos.</span><span class="sxs-lookup"><span data-stu-id="d5da1-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]