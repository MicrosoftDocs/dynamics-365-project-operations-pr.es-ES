---
title: Página principal de dimensiones de precios y costes
description: En este tema se proporciona una descripción general de las dimensiones de precios.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755987"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="131a8-103">Página principal de dimensiones de precios y costes</span><span class="sxs-lookup"><span data-stu-id="131a8-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="131a8-104">Las dimensiones que se utilizan en los recursos humanos para establecer los precios y los costes se dividen en dos categorías:</span><span class="sxs-lookup"><span data-stu-id="131a8-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="131a8-105">Personas</span><span class="sxs-lookup"><span data-stu-id="131a8-105">People</span></span>
- <span data-ttu-id="131a8-106">Trabajo previsto</span><span class="sxs-lookup"><span data-stu-id="131a8-106">Planned work</span></span>

<span data-ttu-id="131a8-107">Debido a esto, hay dos tipos de valores de dimensión de precios disponibles en Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="131a8-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="131a8-108">**Conjuntos de opciones**: dimensiones que son enumeraciones fijas para un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="131a8-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="131a8-109">**Valores basados en entidad**: dimensiones que son enumeraciones fijas para un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="131a8-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="131a8-110">Dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="131a8-110">Pricing dimensions</span></span>

<span data-ttu-id="131a8-111">PSA se envía con un conjunto predeterminado de dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="131a8-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="131a8-112">Puede verlos yendo a **Project Service** > **Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="131a8-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="131a8-113">En el registro de parámetros, en la pestaña **Dimensión de precios basados en importes**, verifique que el rol **msdyn_resourcecategory** y la unidad organizativa de recursos **msdyn_organizationalunit** tenga los campos **Aplicable a ventas** y **Aplicable a costes** establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="131a8-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="131a8-114">Esto le permitirá configurar el precio y el coste de cada combinación de roles y unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="131a8-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captura de pantalla de los parámetros Project Service con la opción "Aplicable a ventas" resaltada](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="131a8-116">Si ha estado utilizando campos listos para usar de rol y unidad organizativa como dimensiones de precios antes de la versión 3 de PSA, no habrá ningún cambio observable.</span><span class="sxs-lookup"><span data-stu-id="131a8-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="131a8-117">Puede continuar utilizando Project Service como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="131a8-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="131a8-118">Si necesita fijar el precio o el coste de sus recursos mediante atributos adicionales, puede crear campos, entidades y dimensiones personalizados.</span><span class="sxs-lookup"><span data-stu-id="131a8-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="131a8-119">Para obtener más información, consulte los siguientes temas. Sin embargo, tenga en cuenta que debe completar los procedimientos en el orden que se detalla a continuación:</span><span class="sxs-lookup"><span data-stu-id="131a8-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="131a8-120">Creación de campos y entidades</span><span class="sxs-lookup"><span data-stu-id="131a8-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="131a8-121">Adición de campos personalizados a la configuración de precios y entidades transaccionales</span><span class="sxs-lookup"><span data-stu-id="131a8-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="131a8-122">Configuración de campos personalizados como dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="131a8-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="131a8-123">Actualización de atributos de complemento para incluir nuevas dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="131a8-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="131a8-124">Precios del tiempo de recursos humanos</span><span class="sxs-lookup"><span data-stu-id="131a8-124">Pricing human resource time</span></span>
<span data-ttu-id="131a8-125">La forma en que una organización establece el precio para el tiempo de los recursos humanos es a menudo una consideración estratégica importante que afecta directamente la rentabilidad de la organización.</span><span class="sxs-lookup"><span data-stu-id="131a8-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="131a8-126">Trabaje con los equipos de finanzas y los directores de práctica cuando su organización esté lista para identificar cómo quiere establecer las tarifas y los costes del tiempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="131a8-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="131a8-127">Otras consideraciones para los precios incluyen si se deben reutilizar campos o entidades que actualmente no son dimensiones de precios, pero que se aplican como una dimensión de precios para su organización.</span><span class="sxs-lookup"><span data-stu-id="131a8-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="131a8-128">Los campos como **Categoría de transacción** (**msdyn_transactioncategory**) y **Recurso que se puede reservar** (**bookableresource**) son ejemplos de dimensiones candidatas.</span><span class="sxs-lookup"><span data-stu-id="131a8-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="131a8-129">También debe considerar si su dimensión de precios debe ser una tabla o un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="131a8-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="131a8-130">Si prevé cambios en los valores de una dimensión que supere 10 o 12 y necesita atributos adicionales en estos valores, puede crear una entidad en lugar de un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="131a8-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="131a8-131">Mantener un conjunto de opciones, como agregar o eliminar valores, requiere un administrador o desarrollador, mientras que la mayoría de los usuarios pueden agregar nuevas filas a una tabla.</span><span class="sxs-lookup"><span data-stu-id="131a8-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="131a8-132">El siguiente ejemplo muestra las tasas de facturación que se configuran en función del rol y la unidad organizativa de recursos a la que pertenece el recurso.</span><span class="sxs-lookup"><span data-stu-id="131a8-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="131a8-133">Las tasas de costes generalmente se basan en la banda salarial del empleado y la unidad organizativa a la que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="131a8-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="131a8-134">En este ejemplo, las tablas de tasa de facturación y tasa de coste tendrán el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="131a8-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="131a8-135">**Tasas de facturación de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="131a8-135">**Sample bill rates**</span></span>

| <span data-ttu-id="131a8-136">Rol</span><span class="sxs-lookup"><span data-stu-id="131a8-136">Role</span></span>        | <span data-ttu-id="131a8-137">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="131a8-137">Org Unit</span></span>    |<span data-ttu-id="131a8-138">Unidad</span><span class="sxs-lookup"><span data-stu-id="131a8-138">Unit</span></span>      |<span data-ttu-id="131a8-139">Precio</span><span class="sxs-lookup"><span data-stu-id="131a8-139">Price</span></span>      |<span data-ttu-id="131a8-140">Divisa</span><span class="sxs-lookup"><span data-stu-id="131a8-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="131a8-141">Desarrollador</span><span class="sxs-lookup"><span data-stu-id="131a8-141">Developer</span></span>   | <span data-ttu-id="131a8-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="131a8-142">Contoso US</span></span>  |<span data-ttu-id="131a8-143">Hour</span><span class="sxs-lookup"><span data-stu-id="131a8-143">Hour</span></span> | <span data-ttu-id="131a8-144">200</span><span class="sxs-lookup"><span data-stu-id="131a8-144">200</span></span>|<span data-ttu-id="131a8-145">USD</span><span class="sxs-lookup"><span data-stu-id="131a8-145">USD</span></span>     |
| <span data-ttu-id="131a8-146">Desarrollador</span><span class="sxs-lookup"><span data-stu-id="131a8-146">Developer</span></span>   | <span data-ttu-id="131a8-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="131a8-147">Contoso India</span></span> |<span data-ttu-id="131a8-148">Hour</span><span class="sxs-lookup"><span data-stu-id="131a8-148">Hour</span></span>|   <span data-ttu-id="131a8-149">112</span><span class="sxs-lookup"><span data-stu-id="131a8-149">112</span></span>|<span data-ttu-id="131a8-150">USD</span><span class="sxs-lookup"><span data-stu-id="131a8-150">USD</span></span>     |


<span data-ttu-id="131a8-151">**Tasas de costes de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="131a8-151">**Sample cost rates**</span></span>

| <span data-ttu-id="131a8-152">Banda salarial</span><span class="sxs-lookup"><span data-stu-id="131a8-152">Salary Band</span></span>     | <span data-ttu-id="131a8-153">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="131a8-153">Org Unit</span></span>    |<span data-ttu-id="131a8-154">Unidad</span><span class="sxs-lookup"><span data-stu-id="131a8-154">Unit</span></span>      |<span data-ttu-id="131a8-155">Precio</span><span class="sxs-lookup"><span data-stu-id="131a8-155">Price</span></span>      |<span data-ttu-id="131a8-156">Divisa</span><span class="sxs-lookup"><span data-stu-id="131a8-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="131a8-157">Mi empresa_Banda1</span><span class="sxs-lookup"><span data-stu-id="131a8-157">My company_Band1</span></span> | <span data-ttu-id="131a8-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="131a8-158">Contoso US</span></span>  |<span data-ttu-id="131a8-159">Hour</span><span class="sxs-lookup"><span data-stu-id="131a8-159">Hour</span></span> | <span data-ttu-id="131a8-160">145</span><span class="sxs-lookup"><span data-stu-id="131a8-160">145</span></span>|<span data-ttu-id="131a8-161">USD</span><span class="sxs-lookup"><span data-stu-id="131a8-161">USD</span></span>     |
| <span data-ttu-id="131a8-162">Mi empresa_Banda2</span><span class="sxs-lookup"><span data-stu-id="131a8-162">My company_Band2</span></span> | <span data-ttu-id="131a8-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="131a8-163">Contoso India</span></span> |<span data-ttu-id="131a8-164">Hour</span><span class="sxs-lookup"><span data-stu-id="131a8-164">Hour</span></span>|   <span data-ttu-id="131a8-165">67</span><span class="sxs-lookup"><span data-stu-id="131a8-165">67</span></span>|<span data-ttu-id="131a8-166">USD</span><span class="sxs-lookup"><span data-stu-id="131a8-166">USD</span></span>     |
