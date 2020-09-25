---
title: Recibir artículos en el pedido de compra a partir del requisito de artículo
description: Este tema explica cómo recibir artículos en un pedido de compra a partir de un requisito de artículo.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755941"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Recibir artículos en el pedido de compra a partir del requisito de artículo

[!include [task guide banner](../../includes/task-guide-banner.md)]

Este tema explica cómo recibir artículos en un pedido de compra a partir de un requisito de artículo.

Al utilizar un requisito de artículo en lugar de una transacción de artículo, puede planificar la entrega justo antes de que el artículo se utilice realmente, crear una orden de compra, incluir el artículo en el marco del acuerdo comercial e incluir el requisito de artículo en la planificación de la producción. 

Esta tarea utiliza el conjunto de datos de USSI.

1. En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Proyectos > Todos los proyectos**.
2. En la lista, seleccione el vínculo en la fila deseada.
3. En el Panel de acciones, seleccione **Plan**.
4. Seleccione **Requisitos de artículo**.
5. Seleccione **Nuevo**.
6. En la nueva fila, indique o seleccione un valor en el campo **Número de artículo**.
7. En el campo **Cantidad**, especifique un número.
8. Seleccione **Guardar**.
9. En el Panel de acciones, seleccione **Gestionar**.
10. Seleccione **Funciones**.
11. Seleccione **Crear pedido de compra**.
12. Seleccione la casilla **Incluir todo**.
13. En el campo **Cuenta de proveedor**, introduzca o seleccione un valor.
14. Seleccione **Aceptar**.
15. En el panel de navegación, vaya **Módulos > Proveedores > Pedidos de compra > Todos los pedidos de compra**.
16. En la lista, seleccione el vínculo en la fila deseada.
17. En el panel de acciones, seleccione **Compra**.
18. Seleccione **Confirmar**.
19. En el panel de acciones, seleccione **Recibir**.
20. Seleccione **Recepción de producto**.
21. En el campo **Recepción de producto**, escriba un valor.
22. Seleccione **Aceptar**.
