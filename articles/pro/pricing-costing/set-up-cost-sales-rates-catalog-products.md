---
title: Configurar tarifas de costes y ventas para productos de catálogo
description: Este tema proporciona información sobre cómo configurar las tasas de costes y ventas para las elementos en un catálogo de producto.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085215"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="e1f1a-103">Configurar tarifas de costes y ventas para productos de catálogo</span><span class="sxs-lookup"><span data-stu-id="e1f1a-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="e1f1a-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="e1f1a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e1f1a-105">La configuración de precios para los artículos del catálogo de productos en Dynamics 365 Project Operations es la misma que en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="e1f1a-106">Debido a que los productos no se pueden estimar ni utilizar en proyectos en Project Operations, no es necesario establecer precios de catálogo de productos en las listas de precios del proyecto para cotizaciones y contratos.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="e1f1a-107">Los precios del catálogo de productos deben configurarse en el campo **Precio del producto** de una cotización, contrato o cuenta.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="e1f1a-108">No configure precios de catálogo de productos en las listas de precios del proyecto para estas entidades.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="e1f1a-109">Las listas de precios del proyecto son exclusivas de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="e1f1a-110">Existe una lógica empresarial específica de la aplicación que copia las listas de precios de una cotización a un contrato.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="e1f1a-111">El resultado es una lista de precios de un proyecto específico del contrato.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="e1f1a-112">La operación de copia puede retrasar el proceso de obtención de cotización si la lista de precios del proyecto en la cotización es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="e1f1a-113">Las listas de precios de productos no se copian para crear listas de precios personalizadas en los contratos.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="e1f1a-114">Esto significa que las listas de precios de los productos no afectan el rendimiento del proceso de cotización.</span><span class="sxs-lookup"><span data-stu-id="e1f1a-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
