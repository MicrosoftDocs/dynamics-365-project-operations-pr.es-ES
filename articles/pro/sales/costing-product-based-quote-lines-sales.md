---
title: Líneas de ofertas basadas en productos de gestión de costes
description: En este tema se proporciona información sobre la aplicación de un precio de coste a una línea de oferta basada en producto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118949"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="22b4a-103">Líneas de ofertas basadas en productos de gestión de costes</span><span class="sxs-lookup"><span data-stu-id="22b4a-103">Costing product-based quote lines</span></span>

<span data-ttu-id="22b4a-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="22b4a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="22b4a-105">Las líneas de oferta basadas en productos en Dynamics 365 Project Operations también tienen un campo **Precio de coste**.</span><span class="sxs-lookup"><span data-stu-id="22b4a-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="22b4a-106">Este campo se usa para seguir el precio de coste del producto en la línea de oferta y para los cálculos de rentabilidad posteriores.</span><span class="sxs-lookup"><span data-stu-id="22b4a-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="22b4a-107">Cuando se crea una línea de oferta basada en productos para un producto de catálogo, el coste de la línea de oferta basada en producto se toma de forma predeterminada del campo **Coste estándar** del catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="22b4a-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="22b4a-108">El campo de coste estándar del catálogo de productos se configura en la divisa base de la organización.</span><span class="sxs-lookup"><span data-stu-id="22b4a-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="22b4a-109">El coste unitario predeterminado en la línea de oferta basada en producto se convierte a la moneda de venta en la oferta.</span><span class="sxs-lookup"><span data-stu-id="22b4a-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="22b4a-110">Coste unitario de línea de oferta basada en producto</span><span class="sxs-lookup"><span data-stu-id="22b4a-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="22b4a-111">El propósito de tener un coste unitario en una línea de oferta basada en producto es permitir diferentes costes para un producto para cada venta.</span><span class="sxs-lookup"><span data-stu-id="22b4a-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="22b4a-112">Este no es un escenario habitual, pero a veces el proveedor puede descontar el coste del producto dependiendo del cliente de la venta final.</span><span class="sxs-lookup"><span data-stu-id="22b4a-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="22b4a-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="22b4a-113">For example:</span></span>

<span data-ttu-id="22b4a-114">Fabrikam Robotics está instalando brazos robóticos en las líneas de montaje de A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="22b4a-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="22b4a-115">Fabrikam proporciona servicios de instalación, pero los brazos robóticos se obtienen de Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="22b4a-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="22b4a-116">Si la instalación de brazos robóticos en A Datum Corporation abre una nueva industria vertical para los brazos robóticos de Trey, Trey podría ofrecer un descuento especial para esta oferta a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="22b4a-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="22b4a-117">En este caso, Fabrikam creará una línea de oferta basada en el producto para Robotic Arms e ingresará un coste unitario especial para esta oferta.</span><span class="sxs-lookup"><span data-stu-id="22b4a-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="22b4a-118">Este coste es diferente del coste estándar de Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="22b4a-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
