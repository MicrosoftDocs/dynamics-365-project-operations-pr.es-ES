---
title: Configurar tarifas de costes y ventas para productos de catálogo (lite)
description: Este tema proporciona información sobre cómo configurar las tasas de costes y ventas para las elementos en un catálogo de producto.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764584"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="71ff5-103">Configurar tarifas de costes y ventas para productos de catálogo (lite)</span><span class="sxs-lookup"><span data-stu-id="71ff5-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="71ff5-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="71ff5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="71ff5-105">La configuración de precios para artículos del catálogo de productos de Dynamics 365 Project Operations es la misma que en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="71ff5-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="71ff5-106">En Project Operations, los productos no se pueden estimar ni usar en proyectos, por lo que no es necesario establecer los precios del catálogo de productos en las listas de precios de proyecto para ofertas y contratos.</span><span class="sxs-lookup"><span data-stu-id="71ff5-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="71ff5-107">Use el campo **Precio del producto** de una oferta, un contrato o una cuenta para configurar los precios del catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="71ff5-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="71ff5-108">No configure los precios de catálogo de productos en las listas de precios de proyecto.</span><span class="sxs-lookup"><span data-stu-id="71ff5-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="71ff5-109">Las listas de precios del proyecto son exclusivas de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="71ff5-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="71ff5-110">La lógica empresarial específica de la aplicación copia las listas de precios de una oferta a un contrato.</span><span class="sxs-lookup"><span data-stu-id="71ff5-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="71ff5-111">El resultado es una lista de precios de un proyecto específico del contrato.</span><span class="sxs-lookup"><span data-stu-id="71ff5-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="71ff5-112">La operación de copia puede retrasar el proceso de obtención de cotización si la lista de precios del proyecto en la cotización es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="71ff5-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="71ff5-113">Las listas de precios de productos no se copian para crear listas de precios personalizadas en los contratos.</span><span class="sxs-lookup"><span data-stu-id="71ff5-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="71ff5-114">Como no se realiza una copia, el rendimiento del proceso de oferta no se ve afectado.</span><span class="sxs-lookup"><span data-stu-id="71ff5-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
