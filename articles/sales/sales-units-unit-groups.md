---
title: Unidades y unidades de venta
description: En este tema se proporciona información sobre cómo crear unidades y unidades de venta en Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085271"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="2ff00-103">Unidades y unidades de venta</span><span class="sxs-lookup"><span data-stu-id="2ff00-103">Units and unit groups</span></span>

<span data-ttu-id="2ff00-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="2ff00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2ff00-105">Las unidades son las cantidades o medidas en las que vende sus productos o servicios.</span><span class="sxs-lookup"><span data-stu-id="2ff00-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="2ff00-106">Por ejemplo, si vende suministros para jardinería, es posible que venda semillas en unidades de paquetes, cajas y pallets.</span><span class="sxs-lookup"><span data-stu-id="2ff00-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="2ff00-107">Una unidad de venta constituye el conjunto de estas diferentes unidades.</span><span class="sxs-lookup"><span data-stu-id="2ff00-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="2ff00-108">Para completar los pasos de este tema, asegúrese de que se le haya asignado el rol de Administrador del sistema o Administrador de Sales Professional o tenga permisos equivalentes.</span><span class="sxs-lookup"><span data-stu-id="2ff00-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="2ff00-109">Creación de unidades de venta</span><span class="sxs-lookup"><span data-stu-id="2ff00-109">Create a unit group</span></span>

1. <span data-ttu-id="2ff00-110">En el mapa del sitio, seleccione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="2ff00-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="2ff00-111">Seleccione **Nuevo** y, en el cuadro de diálogo, **Crear unidad de venta** , introduzca el nombre de la unidad.</span><span class="sxs-lookup"><span data-stu-id="2ff00-111">Select **New** , and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="2ff00-112">En el campo **Unidad principal** , introduzca la unidad de medida mínima común por la que se venderá el producto.</span><span class="sxs-lookup"><span data-stu-id="2ff00-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="2ff00-113">Por ejemplo, puede introducir "pieza" u "onza".</span><span class="sxs-lookup"><span data-stu-id="2ff00-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="2ff00-114">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2ff00-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="2ff00-115">Agregar unidades a una unidad de venta</span><span class="sxs-lookup"><span data-stu-id="2ff00-115">Add units to a unit group</span></span>

1. <span data-ttu-id="2ff00-116">Abra una unidad de venta y en la pestaña **Relacionado** , seleccione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="2ff00-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="2ff00-117">Verá que la unidad principal ya está agregada.</span><span class="sxs-lookup"><span data-stu-id="2ff00-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="2ff00-118">Seleccione **Agregar nueva unidad** y, en la página **Creación rápida: unidad** , en el campo **Nombre** , introduzca el nombre de la unidad.</span><span class="sxs-lookup"><span data-stu-id="2ff00-118">Select **Add New Unit** , and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="2ff00-119">En el campo **Cantidad** , introduzca la cantidad que contendrá la unidad.</span><span class="sxs-lookup"><span data-stu-id="2ff00-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="2ff00-120">Por ejemplo, si una caja contiene dos piezas, introduzca "2".</span><span class="sxs-lookup"><span data-stu-id="2ff00-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="2ff00-121">En el campo **Unidad base** , seleccione una unidad base para establecer la unidad de medida más baja para la unidad.</span><span class="sxs-lookup"><span data-stu-id="2ff00-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="2ff00-122">Por ejemplo, puede seleccionar "Pieza".</span><span class="sxs-lookup"><span data-stu-id="2ff00-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="2ff00-123">Seleccione **Guardar** :</span><span class="sxs-lookup"><span data-stu-id="2ff00-123">Select **Save** :</span></span>
