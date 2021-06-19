---
title: Líneas de contrato basadas en productos de coste (lite)
description: En este tema se proporciona información sobre la creación
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003562"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="49230-103">Líneas de contrato basadas en productos de coste (lite)</span><span class="sxs-lookup"><span data-stu-id="49230-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="49230-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="49230-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="49230-105">Las líneas de contrato basadas en producto de Dynamics 365 Project Operations incluyen el campo **Precio de coste**, que almacena el precio de coste del producto para los cálculos de rentabilidad posteriores.</span><span class="sxs-lookup"><span data-stu-id="49230-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="49230-106">Cuando se crea una línea de contrato basada en producto para un producto del catálogo, el coste predeterminado de la línea es **Coste estándar** en el catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="49230-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="49230-107">El campo **Coste estándar** del catálogo de productos se configura en la divisa base de la organización.</span><span class="sxs-lookup"><span data-stu-id="49230-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="49230-108">Cuando el coste unitario está por defecto en la línea del contrato, se convierte a la moneda de venta en el contrato.</span><span class="sxs-lookup"><span data-stu-id="49230-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="49230-109">Coste unitario de línea de contrato basada en producto</span><span class="sxs-lookup"><span data-stu-id="49230-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="49230-110">Tener un coste unitario en una línea de contrato basada en productos permite distintos costes de producto por cada venta de una unidad.</span><span class="sxs-lookup"><span data-stu-id="49230-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="49230-111">Si bien no siempre es necesario, existen ciertos escenarios en los que el proveedor puede descontar el costo del producto para el cliente.</span><span class="sxs-lookup"><span data-stu-id="49230-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="49230-112">Tenga en cuenta el escenario siguiente:</span><span class="sxs-lookup"><span data-stu-id="49230-112">Consider the following scenario:</span></span>

<span data-ttu-id="49230-113">Fabrikam Robotics está instalando brazos robóticos en las líneas de montaje de Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="49230-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="49230-114">Fabrikam proporciona servicios de instalación, pero los brazos robóticos son de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="49230-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="49230-115">Si la instalación de brazos robóticos en Adatum Corporation abre una nueva industria vertical para los brazos robóticos de Trey Research, estos podrían ofrecer un descuento especial para esta oferta a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="49230-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="49230-116">En este caso, Fabrikam crea una línea de contrato basada en producto para Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="49230-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="49230-117">Se especifica un coste unitario para este contrato.</span><span class="sxs-lookup"><span data-stu-id="49230-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="49230-118">El coste es diferente al de los brazos robóticos de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="49230-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]