---
title: Información general de dimensiones de precios
description: En este tema se proporciona información sobre las dimensiones de precios en Dynamics 365 Project Operations.
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
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128484"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="b1469-103">Información general de dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="b1469-103">Pricing dimensions overview</span></span>

<span data-ttu-id="b1469-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="b1469-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b1469-105">Las dimensiones que se utilizan en los recursos humanos para establecer los precios y los costes se dividen en dos categorías:</span><span class="sxs-lookup"><span data-stu-id="b1469-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="b1469-106">Personas</span><span class="sxs-lookup"><span data-stu-id="b1469-106">People</span></span>
- <span data-ttu-id="b1469-107">Trabajo previsto</span><span class="sxs-lookup"><span data-stu-id="b1469-107">Planned work</span></span>

<span data-ttu-id="b1469-108">Debido a esto, hay dos tipos de valores de dimensión de precios disponibles:</span><span class="sxs-lookup"><span data-stu-id="b1469-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="b1469-109">**Conjuntos de opciones**: dimensiones que son enumeraciones fijas para un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="b1469-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="b1469-110">**Valores basados en entidad**: dimensiones que son enumeraciones fijas para un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="b1469-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="b1469-111">Dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="b1469-111">Pricing dimensions</span></span>

<span data-ttu-id="b1469-112">Dynamics 365 Project Operations se envía con un conjunto predeterminado de dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="b1469-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="b1469-113">Puede ver estas dimensiones de precios yendo a **Project Operations** > **Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="b1469-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="b1469-114">En el registro de parámetros, en la pestaña **Dimensión de precios basados en importes**, verifique que el rol **msdyn_resourcecategory** y la unidad organizativa de recursos **msdyn_organizationalunit** tenga los campos **Aplicable a ventas** y **Aplicable a costes** establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="b1469-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="b1469-115">Con estos cambios habilitados, puede configurar el precio y el coste de cada combinación de roles y unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="b1469-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="b1469-116">Si necesita fijar el precio o el coste de sus recursos mediante atributos adicionales, puede crear campos, entidades y dimensiones personalizados.</span><span class="sxs-lookup"><span data-stu-id="b1469-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="b1469-117">Precios del tiempo de recursos humanos</span><span class="sxs-lookup"><span data-stu-id="b1469-117">Pricing human resource time</span></span>
<span data-ttu-id="b1469-118">La forma en que una organización establece el precio para el tiempo de los recursos humanos es a menudo una consideración estratégica importante que afecta directamente la rentabilidad de la organización.</span><span class="sxs-lookup"><span data-stu-id="b1469-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="b1469-119">Trabaje con los equipos de finanzas y los directores de práctica cuando su organización esté lista para identificar cómo quiere establecer las tarifas y los costes del tiempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="b1469-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="b1469-120">Otras consideraciones para los precios incluyen si se deben reutilizar campos o entidades que actualmente no son dimensiones de precios, pero que se aplican como una dimensión de precios para su organización.</span><span class="sxs-lookup"><span data-stu-id="b1469-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="b1469-121">Los campos como **Categoría de transacción** (**msdyn_transactioncategory**) y **Recurso que se puede reservar** (**bookableresource**) son ejemplos de dimensiones candidatas.</span><span class="sxs-lookup"><span data-stu-id="b1469-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="b1469-122">Considere si su dimensión de precios debe ser una tabla o un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="b1469-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="b1469-123">Si prevé cambios en los valores de una dimensión que supere 10 o 12 y necesita atributos adicionales en estos valores, puede crear una entidad en lugar de un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="b1469-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="b1469-124">Mantener un conjunto de opciones, como agregar o eliminar valores, requiere un administrador o desarrollador, mientras que la mayoría de los usuarios pueden agregar nuevas filas a una tabla.</span><span class="sxs-lookup"><span data-stu-id="b1469-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="b1469-125">El siguiente ejemplo muestra las tasas de facturación que se configuran en función del rol y la unidad organizativa de recursos a la que pertenece el recurso.</span><span class="sxs-lookup"><span data-stu-id="b1469-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="b1469-126">Las tasas de costes generalmente se basan en la banda salarial del empleado y la unidad organizativa a la que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="b1469-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="b1469-127">En este ejemplo, las tablas de tasa de facturación y tasa de coste tendrán el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="b1469-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="b1469-128">**Tasas de facturación de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b1469-128">**Sample bill rates**</span></span>

| <span data-ttu-id="b1469-129">Rol</span><span class="sxs-lookup"><span data-stu-id="b1469-129">Role</span></span>        | <span data-ttu-id="b1469-130">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="b1469-130">Org Unit</span></span>    |<span data-ttu-id="b1469-131">Unidad</span><span class="sxs-lookup"><span data-stu-id="b1469-131">Unit</span></span>      |<span data-ttu-id="b1469-132">Precio</span><span class="sxs-lookup"><span data-stu-id="b1469-132">Price</span></span>      |<span data-ttu-id="b1469-133">Divisa</span><span class="sxs-lookup"><span data-stu-id="b1469-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="b1469-134">Desarrollador</span><span class="sxs-lookup"><span data-stu-id="b1469-134">Developer</span></span>   | <span data-ttu-id="b1469-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b1469-135">Contoso US</span></span>  |<span data-ttu-id="b1469-136">Hour</span><span class="sxs-lookup"><span data-stu-id="b1469-136">Hour</span></span> | <span data-ttu-id="b1469-137">200</span><span class="sxs-lookup"><span data-stu-id="b1469-137">200</span></span>|<span data-ttu-id="b1469-138">USD</span><span class="sxs-lookup"><span data-stu-id="b1469-138">USD</span></span>     |
| <span data-ttu-id="b1469-139">Desarrollador</span><span class="sxs-lookup"><span data-stu-id="b1469-139">Developer</span></span>   | <span data-ttu-id="b1469-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="b1469-140">Contoso India</span></span> |<span data-ttu-id="b1469-141">Hour</span><span class="sxs-lookup"><span data-stu-id="b1469-141">Hour</span></span>|   <span data-ttu-id="b1469-142">112</span><span class="sxs-lookup"><span data-stu-id="b1469-142">112</span></span>|<span data-ttu-id="b1469-143">USD</span><span class="sxs-lookup"><span data-stu-id="b1469-143">USD</span></span>     |


<span data-ttu-id="b1469-144">**Tasas de costes de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b1469-144">**Sample cost rates**</span></span>

| <span data-ttu-id="b1469-145">Banda salarial</span><span class="sxs-lookup"><span data-stu-id="b1469-145">Salary Band</span></span>     | <span data-ttu-id="b1469-146">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="b1469-146">Org Unit</span></span>    |<span data-ttu-id="b1469-147">Unidad</span><span class="sxs-lookup"><span data-stu-id="b1469-147">Unit</span></span>      |<span data-ttu-id="b1469-148">Precio</span><span class="sxs-lookup"><span data-stu-id="b1469-148">Price</span></span>      |<span data-ttu-id="b1469-149">Divisa</span><span class="sxs-lookup"><span data-stu-id="b1469-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="b1469-150">Mi empresa_Banda1</span><span class="sxs-lookup"><span data-stu-id="b1469-150">My company_Band1</span></span> | <span data-ttu-id="b1469-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b1469-151">Contoso US</span></span>  |<span data-ttu-id="b1469-152">Hour</span><span class="sxs-lookup"><span data-stu-id="b1469-152">Hour</span></span> | <span data-ttu-id="b1469-153">145</span><span class="sxs-lookup"><span data-stu-id="b1469-153">145</span></span>|<span data-ttu-id="b1469-154">USD</span><span class="sxs-lookup"><span data-stu-id="b1469-154">USD</span></span>     |
| <span data-ttu-id="b1469-155">Mi empresa_Banda2</span><span class="sxs-lookup"><span data-stu-id="b1469-155">My company_Band2</span></span> | <span data-ttu-id="b1469-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="b1469-156">Contoso India</span></span> |<span data-ttu-id="b1469-157">Hour</span><span class="sxs-lookup"><span data-stu-id="b1469-157">Hour</span></span>|   <span data-ttu-id="b1469-158">67</span><span class="sxs-lookup"><span data-stu-id="b1469-158">67</span></span>|<span data-ttu-id="b1469-159">USD</span><span class="sxs-lookup"><span data-stu-id="b1469-159">USD</span></span>     |
