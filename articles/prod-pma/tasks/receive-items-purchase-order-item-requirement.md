---
title: Recibir artículos en el pedido de compra a partir del requisito de artículo
description: Este tema explica cómo recibir artículos en un pedido de compra a partir de un requisito de artículo.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085315"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="c7dab-103">Recibir artículos en el pedido de compra a partir del requisito de artículo</span><span class="sxs-lookup"><span data-stu-id="c7dab-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7dab-104">Este tema explica cómo recibir artículos en un pedido de compra a partir de un requisito de artículo.</span><span class="sxs-lookup"><span data-stu-id="c7dab-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="c7dab-105">Al utilizar un requisito de artículo en lugar de una transacción de artículo, puede planificar la entrega justo antes de que el artículo se utilice realmente, crear una orden de compra, incluir el artículo en el marco del acuerdo comercial e incluir el requisito de artículo en la planificación de la producción.</span><span class="sxs-lookup"><span data-stu-id="c7dab-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="c7dab-106">Esta tarea utiliza el conjunto de datos de USSI.</span><span class="sxs-lookup"><span data-stu-id="c7dab-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c7dab-107">En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Proyectos > Todos los proyectos**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="c7dab-108">En la lista, seleccione el vínculo en la fila deseada.</span><span class="sxs-lookup"><span data-stu-id="c7dab-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="c7dab-109">En el Panel de acciones, seleccione **Plan**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="c7dab-110">Seleccione **Requisitos de artículo**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="c7dab-111">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-111">Select **New**.</span></span>
6. <span data-ttu-id="c7dab-112">En la nueva fila, indique o seleccione un valor en el campo **Número de artículo**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="c7dab-113">En el campo **Cantidad** , especifique un número.</span><span class="sxs-lookup"><span data-stu-id="c7dab-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="c7dab-114">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-114">Select **Save**.</span></span>
9. <span data-ttu-id="c7dab-115">En el Panel de acciones, seleccione **Gestionar**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="c7dab-116">Seleccione **Funciones**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-116">Select **Functions**.</span></span>
11. <span data-ttu-id="c7dab-117">Seleccione **Crear pedido de compra**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="c7dab-118">Seleccione la casilla **Incluir todo**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="c7dab-119">En el campo **Cuenta de proveedor** , introduzca o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="c7dab-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="c7dab-120">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-120">Select **OK**.</span></span>
15. <span data-ttu-id="c7dab-121">En el panel de navegación, vaya **Módulos > Proveedores > Pedidos de compra > Todos los pedidos de compra**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="c7dab-122">En la lista, seleccione el vínculo en la fila deseada.</span><span class="sxs-lookup"><span data-stu-id="c7dab-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="c7dab-123">En el panel de acciones, seleccione **Compra**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="c7dab-124">Seleccione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="c7dab-125">En el panel de acciones, seleccione **Recibir**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="c7dab-126">Seleccione **Recepción de producto**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="c7dab-127">En el campo **Recepción de producto** , escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="c7dab-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="c7dab-128">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c7dab-128">Select **OK**.</span></span>

