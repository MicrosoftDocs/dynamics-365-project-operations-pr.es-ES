---
title: Unidades y unidades de venta
description: Este tema proporciona información sobre cómo crear unidades y unidades de venta en Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277359"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="4ba21-103">Unidades y unidades de venta</span><span class="sxs-lookup"><span data-stu-id="4ba21-103">Units and unit groups</span></span>

<span data-ttu-id="4ba21-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="4ba21-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ba21-105">Las unidades son las cantidades o medidas en las que vende sus productos o servicios.</span><span class="sxs-lookup"><span data-stu-id="4ba21-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="4ba21-106">Por ejemplo, si vende suministros para jardinería, es posible que venda semillas en unidades de paquetes, cajas y pallets.</span><span class="sxs-lookup"><span data-stu-id="4ba21-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="4ba21-107">Una unidad de venta constituye el conjunto de estas diferentes unidades.</span><span class="sxs-lookup"><span data-stu-id="4ba21-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="4ba21-108">Para completar los pasos de este tema, asegúrese de que se le haya asignado el rol de Administrador del sistema o Administrador de Sales Professional o tenga permisos equivalentes.</span><span class="sxs-lookup"><span data-stu-id="4ba21-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="4ba21-109">Creación de unidades de venta</span><span class="sxs-lookup"><span data-stu-id="4ba21-109">Create a unit group</span></span>

1. <span data-ttu-id="4ba21-110">En el mapa del sitio, seleccione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="4ba21-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="4ba21-111">Seleccione **Nuevo** y, en el cuadro de diálogo, **Crear unidad de venta**, introduzca el nombre de la unidad.</span><span class="sxs-lookup"><span data-stu-id="4ba21-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="4ba21-112">En el campo **Unidad principal**, introduzca la unidad de medida mínima común por la que se venderá el producto.</span><span class="sxs-lookup"><span data-stu-id="4ba21-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="4ba21-113">Por ejemplo, puede introducir "pieza" u "onza".</span><span class="sxs-lookup"><span data-stu-id="4ba21-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="4ba21-114">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="4ba21-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="4ba21-115">Agregar unidades a una unidad de venta</span><span class="sxs-lookup"><span data-stu-id="4ba21-115">Add units to a unit group</span></span>

1. <span data-ttu-id="4ba21-116">Abra una unidad de venta y en la pestaña **Relacionado**, seleccione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="4ba21-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="4ba21-117">Verá que la unidad principal ya está agregada.</span><span class="sxs-lookup"><span data-stu-id="4ba21-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="4ba21-118">Seleccione **Agregar nueva unidad** y, en la página **Creación rápida: unidad**, en el campo **Nombre**, introduzca el nombre de la unidad.</span><span class="sxs-lookup"><span data-stu-id="4ba21-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="4ba21-119">En el campo **Cantidad**, introduzca la cantidad que contendrá la unidad.</span><span class="sxs-lookup"><span data-stu-id="4ba21-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="4ba21-120">Por ejemplo, si una caja contiene dos piezas, introduzca "2".</span><span class="sxs-lookup"><span data-stu-id="4ba21-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="4ba21-121">En el campo **Unidad base**, seleccione una unidad base para establecer la unidad de medida más baja para la unidad.</span><span class="sxs-lookup"><span data-stu-id="4ba21-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="4ba21-122">Por ejemplo, puede seleccionar "Pieza".</span><span class="sxs-lookup"><span data-stu-id="4ba21-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="4ba21-123">Seleccione **Guardar**:</span><span class="sxs-lookup"><span data-stu-id="4ba21-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]