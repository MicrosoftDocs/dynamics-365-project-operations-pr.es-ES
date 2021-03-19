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
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289210"
---
# <a name="purchase-orders-for-a-project"></a>Pedidos de compra para un proyecto

[!include [banner](../includes/banner.md)]

Este artículo describe los distintos métodos que puede utilizar para crear órdenes de compra para un proyecto. El método que utilice depende del propósito del pedido de compra y cuándo los artículos comprados se utilizan y cargan en un proyecto.

### <a name="methods-for-creating-a-purchase-order"></a>Métodos para crear pedido de compra

Puede utilizar uno de los siguientes métodos para crear un pedido de compra en Gestión de proyectos y contabilidad. El propósito del pedido de compra determina cuándo se utiliza el pedido de compra y, por lo tanto, cuándo se cargan los artículos en un proyecto.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Finalidad</th>
<th>Uso de artículos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crear un pedido de compra directamente desde un proyecto.</td>
<td>Utilice este método para comprar artículos a un proveedor externo para su utilización en un proyecto. Puede crear el pedido de compra de dos formas:
<ul>
<li>Desde el propio proyecto. En este caso, el proyecto ya está definido para la orden de compra.</li>
<li>Dirigiéndose hasta el pedido de compra del proyecto. Debe seleccionar tanto el proveedor como el proyecto para el que se va a crear el pedido de compra.</li>
</ul></td>
<td>Los artículos se usan cuando se actualiza la factura del proveedor.</td>
</tr>
<tr class="even">
<td>Crear un pedido de compra desde un pedido de ventas.</td>
<td>Utilice este método para comprar artículos cuando cree un pedido de venta a partir de un proyecto.</td>
<td>Los artículos se consumen cuando el pedido de venta se factura al cliente.</td>
</tr>
<tr class="odd">
<td>Cree un pedido de compra a partir de un artículo requerido.</td>
<td>Utilice este método para comprar artículos cuando cree un requisito de elemento a partir de un proyecto.</td>
<td>Los artículos se consumen cuando se actualiza el albarán de requisitos del artículo.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Cuando actualiza la factura del proveedor o el albarán, se le solicita que actualice el albarán en el requisito del artículo.

Para más información, consulte [Recibir artículos según el pedido de compra desde un requisito de artículo](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]