---
title: Líneas de contrato basadas en productos de gestión de costes
description: En este tema se proporciona información sobre la creación
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "4085379"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="d0861-103">Líneas de contrato basadas en productos de gestión de costes</span><span class="sxs-lookup"><span data-stu-id="d0861-103">Costing product-based contract lines</span></span>

<span data-ttu-id="d0861-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="d0861-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d0861-105">Las líneas de contrato basadas en productos en Dynamics 365 Project Operations incluyen **Precio de coste** campo, que almacena el precio de costo del producto para los cálculos de rentabilidad posteriores.</span><span class="sxs-lookup"><span data-stu-id="d0861-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="d0861-106">Cuando se crea una línea de contrato basada en productos para un producto de catálogo, el costo de la línea de contrato basada en producto se toma de forma predeterminada del campo **Coste estándar** del catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="d0861-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="d0861-107">El campo **Coste estándar** del catálogo de productos se configura en la divisa base de la organización.</span><span class="sxs-lookup"><span data-stu-id="d0861-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="d0861-108">Cuando el coste unitario está por defecto en la línea del contrato, se convierte a la moneda de venta en el contrato.</span><span class="sxs-lookup"><span data-stu-id="d0861-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="d0861-109">Coste unitario de línea de contrato basada en producto</span><span class="sxs-lookup"><span data-stu-id="d0861-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="d0861-110">Tener un coste unitario en una línea de contrato basada en productos permite distintos costes de producto por cada venta de una unidad.</span><span class="sxs-lookup"><span data-stu-id="d0861-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="d0861-111">Si bien no siempre es necesario, existen ciertos escenarios en los que el proveedor puede descontar el costo del producto para el cliente.</span><span class="sxs-lookup"><span data-stu-id="d0861-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="d0861-112">Tenga en cuenta el escenario siguiente:</span><span class="sxs-lookup"><span data-stu-id="d0861-112">Consider the following scenario:</span></span>

<span data-ttu-id="d0861-113">Fabrikam Robotics está instalando brazos robóticos en las líneas de montaje de Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="d0861-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="d0861-114">Fabrikam proporciona servicios de instalación, pero los brazos robóticos se obtienen de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="d0861-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="d0861-115">Si la instalación de brazos robóticos en Adatum Corporation abre una nueva industria vertical para los brazos robóticos de Trey Research, estos podrían ofrecer un descuento especial para esta oferta a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="d0861-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="d0861-116">En este caso, Fabrikam crea una línea de contrato basada en productos para Robotic Arms e ingresa un costo por unidad para este contrato que es diferente del costo estándar de los brazos robóticos de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="d0861-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
