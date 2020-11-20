---
title: Configurar tarifas de costes y ventas para productos de catálogo (lite)
description: Este tema proporciona información sobre cómo configurar las tasas de costes y ventas para las elementos en un catálogo de producto.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176722"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="470b2-103">Configurar tarifas de costes y ventas para productos de catálogo (lite)</span><span class="sxs-lookup"><span data-stu-id="470b2-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="470b2-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="470b2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="470b2-105">La configuración de precios para los artículos del catálogo de productos en Dynamics 365 Project Operations es la misma que en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="470b2-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="470b2-106">Debido a que los productos no se pueden estimar ni utilizar en proyectos en Project Operations, no es necesario establecer precios de catálogo de productos en las listas de precios del proyecto para cotizaciones y contratos.</span><span class="sxs-lookup"><span data-stu-id="470b2-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="470b2-107">Los precios del catálogo de productos deben configurarse en el campo **Precio del producto** de una cotización, contrato o cuenta.</span><span class="sxs-lookup"><span data-stu-id="470b2-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="470b2-108">No configure precios de catálogo de productos en las listas de precios del proyecto para estas entidades.</span><span class="sxs-lookup"><span data-stu-id="470b2-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="470b2-109">Las listas de precios del proyecto son exclusivas de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="470b2-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="470b2-110">Existe una lógica empresarial específica de la aplicación que copia las listas de precios de una cotización a un contrato.</span><span class="sxs-lookup"><span data-stu-id="470b2-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="470b2-111">El resultado es una lista de precios de un proyecto específico del contrato.</span><span class="sxs-lookup"><span data-stu-id="470b2-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="470b2-112">La operación de copia puede retrasar el proceso de obtención de cotización si la lista de precios del proyecto en la cotización es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="470b2-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="470b2-113">Las listas de precios de productos no se copian para crear listas de precios personalizadas en los contratos.</span><span class="sxs-lookup"><span data-stu-id="470b2-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="470b2-114">Esto significa que las listas de precios de los productos no afectan el rendimiento del proceso de cotización.</span><span class="sxs-lookup"><span data-stu-id="470b2-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
