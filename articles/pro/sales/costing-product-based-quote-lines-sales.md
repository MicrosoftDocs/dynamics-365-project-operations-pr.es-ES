---
title: Líneas de ofertas basadas en productos de gestión de costes
description: En este tema se proporciona información sobre la aplicación de un precio de coste a una línea de oferta basada en producto.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003472"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="39043-103">Líneas de ofertas basadas en productos de gestión de costes</span><span class="sxs-lookup"><span data-stu-id="39043-103">Costing product-based quote lines</span></span>

<span data-ttu-id="39043-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="39043-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="39043-105">Líneas de cotización basadas en productos en Dynamics 365 Project Operations también tengo un campo **Precio de coste** campo.</span><span class="sxs-lookup"><span data-stu-id="39043-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="39043-106">Este campo se usa para seguir el precio de coste del producto en la línea de oferta y para los cálculos de rentabilidad posteriores.</span><span class="sxs-lookup"><span data-stu-id="39043-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="39043-107">Cuando se crea una línea de oferta basada en productos para un producto de catálogo, el coste de la línea de oferta basada en producto se toma de forma predeterminada del campo **Coste estándar** del catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="39043-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="39043-108">El campo de coste estándar del catálogo de productos se configura en la divisa base de la organización.</span><span class="sxs-lookup"><span data-stu-id="39043-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="39043-109">El coste unitario predeterminado en la línea de oferta basada en producto se convierte a la moneda de venta en la oferta.</span><span class="sxs-lookup"><span data-stu-id="39043-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="39043-110">Coste unitario de línea de oferta basada en producto</span><span class="sxs-lookup"><span data-stu-id="39043-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="39043-111">El propósito de tener un coste unitario en una línea de oferta basada en producto es permitir diferentes costes para un producto para cada venta.</span><span class="sxs-lookup"><span data-stu-id="39043-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="39043-112">Este no es un escenario habitual, pero a veces el proveedor puede descontar el coste del producto dependiendo del cliente de la venta final.</span><span class="sxs-lookup"><span data-stu-id="39043-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="39043-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="39043-113">For example:</span></span>

<span data-ttu-id="39043-114">Fabrikam Robotics está instalando brazos robóticos en las líneas de montaje de A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="39043-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="39043-115">Fabrikam proporciona servicios de instalación, pero los brazos robóticos se obtienen de Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="39043-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="39043-116">Si la instalación de brazos robóticos en A Datum Corporation abre una nueva industria vertical para los brazos robóticos de Trey, Trey podría ofrecer un descuento especial para esta oferta a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="39043-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="39043-117">En este caso, Fabrikam creará una línea de oferta basada en el producto para Robotic Arms e ingresará un coste unitario especial para esta oferta.</span><span class="sxs-lookup"><span data-stu-id="39043-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="39043-118">Este coste es diferente del coste estándar de Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="39043-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]