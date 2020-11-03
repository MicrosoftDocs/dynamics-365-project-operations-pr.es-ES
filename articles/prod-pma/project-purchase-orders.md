---
title: Pedidos de compra para un proyecto
description: Este artículo describe los distintos métodos que puede utilizar para crear órdenes de compra para un proyecto. El método que utilice depende del propósito del pedido de compra y cuándo los artículos comprados se utilizan y cargan en un proyecto.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085136"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="729a8-104">Pedidos de compra para un proyecto</span><span class="sxs-lookup"><span data-stu-id="729a8-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="729a8-105">Este artículo describe los distintos métodos que puede utilizar para crear órdenes de compra para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="729a8-106">El método que utilice depende del propósito del pedido de compra y cuándo los artículos comprados se utilizan y cargan en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="729a8-107">Métodos para crear pedido de compra</span><span class="sxs-lookup"><span data-stu-id="729a8-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="729a8-108">Puede utilizar uno de los siguientes métodos para crear un pedido de compra en Gestión de proyectos y contabilidad.</span><span class="sxs-lookup"><span data-stu-id="729a8-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="729a8-109">El propósito del pedido de compra determina cuándo se utiliza el pedido de compra y, por lo tanto, cuándo se cargan los artículos en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="729a8-110">Método</span><span class="sxs-lookup"><span data-stu-id="729a8-110">Method</span></span></th>
<th><span data-ttu-id="729a8-111">Finalidad</span><span class="sxs-lookup"><span data-stu-id="729a8-111">Purpose</span></span></th>
<th><span data-ttu-id="729a8-112">Uso de artículos</span><span class="sxs-lookup"><span data-stu-id="729a8-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="729a8-113">Crear un pedido de compra directamente desde un proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="729a8-114">Utilice este método para comprar artículos a un proveedor externo para su utilización en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="729a8-115">Puede crear el pedido de compra de dos formas:</span><span class="sxs-lookup"><span data-stu-id="729a8-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="729a8-116">Desde el propio proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-116">From the project itself.</span></span> <span data-ttu-id="729a8-117">En este caso, el proyecto ya está definido para la orden de compra.</span><span class="sxs-lookup"><span data-stu-id="729a8-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="729a8-118">Yendo hasta la orden de compra del proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="729a8-119">Debe seleccionar tanto el proveedor como el proyecto para los que crear el pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="729a8-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="729a8-120">Los artículos se usan cuando se actualiza la factura del proveedor.</span><span class="sxs-lookup"><span data-stu-id="729a8-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="729a8-121">Crear un pedido de compra desde un pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="729a8-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="729a8-122">Utilice este método para comprar artículos cuando cree un pedido de venta a partir de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="729a8-123">Los artículos se consumen cuando el pedido de venta se factura al cliente.</span><span class="sxs-lookup"><span data-stu-id="729a8-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="729a8-124">Cree un pedido de compra a partir de un artículo requerido.</span><span class="sxs-lookup"><span data-stu-id="729a8-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="729a8-125">Utilice este método para comprar artículos cuando cree un requisito de elemento a partir de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="729a8-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="729a8-126">Los artículos se consumen cuando se actualiza el albarán de requisitos del artículo.</span><span class="sxs-lookup"><span data-stu-id="729a8-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="729a8-127">Cuando actualiza la factura del proveedor o el albarán, se le solicita que actualice el albarán en el requisito del artículo.</span><span class="sxs-lookup"><span data-stu-id="729a8-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="729a8-128">Para más información, consulte [Recibir artículos según el pedido de compra desde un requisito de artículo](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="729a8-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

