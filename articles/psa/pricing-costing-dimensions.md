---
title: Página principal de dimensiones de precios y costes
description: En este tema se proporciona una descripción general de las dimensiones de precios.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368902"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="42836-103">Página principal de dimensiones de precios y costes</span><span class="sxs-lookup"><span data-stu-id="42836-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="42836-104">Las dimensiones utilizadas para establecer el precio y el coste de la mano de obra en organizaciones basadas en proyectos dependen de los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="42836-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="42836-105">Personas que realizan un trabajo similar a su experiencia, rol o geografía</span><span class="sxs-lookup"><span data-stu-id="42836-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="42836-106">Trabajo a realizar similar a su complejidad o hora del día</span><span class="sxs-lookup"><span data-stu-id="42836-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="42836-107">Dada la naturaleza típica de estos atributos del trabajo y las personas necesarias para realizar el trabajo, existen dos tipos de valores de dimensión de precios disponibles en Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="42836-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="42836-108">**Conjuntos de opciones**: atributos que son enumeraciones fijas para un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="42836-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="42836-109">**Valores basados en entidades**: atributos que pueden tener un conjunto variado de valores que son finitos pero que pueden cambiar con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="42836-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="42836-110">Dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="42836-110">Pricing dimensions</span></span>

<span data-ttu-id="42836-111">PSA se envía con un conjunto predeterminado de dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="42836-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="42836-112">Puede verlos yendo a **Project Service** > **Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="42836-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="42836-113">En el registro de parámetros, en la pestaña **Dimensión de precios basados en importes**, verifique que el rol **msdyn_resourcecategory** y la unidad organizativa de recursos **msdyn_organizationalunit** tenga los campos **Aplicable a ventas** y **Aplicable a costes** establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="42836-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="42836-114">Esto le permitirá configurar el precio y el coste de cada combinación de roles y unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="42836-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captura de pantalla de los parámetros Project Service con la opción "Aplicable a ventas" resaltada](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="42836-116">Si ha estado utilizando campos listos para usar de rol y unidad organizativa como dimensiones de precios antes de la versión 3 de PSA, no habrá ningún cambio observable.</span><span class="sxs-lookup"><span data-stu-id="42836-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="42836-117">Puede continuar utilizando Project Service como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="42836-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="42836-118">Si necesita fijar el precio o el coste de sus recursos mediante atributos adicionales, puede crear campos, entidades y dimensiones personalizados.</span><span class="sxs-lookup"><span data-stu-id="42836-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="42836-119">Para obtener más información, consulte los siguientes temas. Sin embargo, tenga en cuenta que debe completar los procedimientos en el orden que se detalla a continuación:</span><span class="sxs-lookup"><span data-stu-id="42836-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="42836-120">Creación de campos y entidades</span><span class="sxs-lookup"><span data-stu-id="42836-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="42836-121">Adición de campos personalizados a la configuración de precios y entidades transaccionales</span><span class="sxs-lookup"><span data-stu-id="42836-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="42836-122">Configurar campos personalizados como dimensiones de precios </span><span class="sxs-lookup"><span data-stu-id="42836-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="42836-123">Actualización de atributos de complemento para incluir nuevas dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="42836-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="42836-124">Precios del tiempo de recursos humanos</span><span class="sxs-lookup"><span data-stu-id="42836-124">Pricing human resource time</span></span>
<span data-ttu-id="42836-125">La forma en que una organización establece el precio para el tiempo de los recursos humanos es a menudo una consideración estratégica importante que afecta directamente la rentabilidad de la organización.</span><span class="sxs-lookup"><span data-stu-id="42836-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="42836-126">Trabaje con los equipos de finanzas y los directores de práctica cuando su organización esté lista para identificar cómo quiere establecer las tarifas y los costes del tiempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="42836-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="42836-127">Otras consideraciones para los precios incluyen si se deben reutilizar campos o entidades que actualmente no son dimensiones de precios, pero que se aplican como una dimensión de precios para su organización.</span><span class="sxs-lookup"><span data-stu-id="42836-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="42836-128">Los campos como **Categoría de transacción** (**msdyn_transactioncategory**) y **Recurso que se puede reservar** (**bookableresource**) son ejemplos de dimensiones candidatas.</span><span class="sxs-lookup"><span data-stu-id="42836-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="42836-129">Considere si su dimensión de precios debe ser una tabla o un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="42836-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="42836-130">Si prevé cambios en los valores de una dimensión que supere 10 o 12 y necesita atributos adicionales en estos valores, cree una entidad en lugar de un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="42836-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="42836-131">Mantener un conjunto de opciones, como agregar o eliminar valores, requiere un administrador o desarrollador, mientras que la mayoría de los usuarios profesionales pueden agregar nuevas filas a una tabla.</span><span class="sxs-lookup"><span data-stu-id="42836-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="42836-132">El siguiente ejemplo muestra las tasas de facturación que se configuran en función del rol y la unidad organizativa de recursos a la que pertenece el recurso.</span><span class="sxs-lookup"><span data-stu-id="42836-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="42836-133">Las tasas de costes generalmente se basan en la banda salarial del empleado y la unidad organizativa a la que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="42836-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="42836-134">En este ejemplo, las tablas de tasa de facturación y tasa de coste tendrán el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="42836-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="42836-135">**Tasas de facturación de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="42836-135">**Sample bill rates**</span></span>

| <span data-ttu-id="42836-136">Rol</span><span class="sxs-lookup"><span data-stu-id="42836-136">Role</span></span>        | <span data-ttu-id="42836-137">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="42836-137">Org Unit</span></span>    |<span data-ttu-id="42836-138">Unidad</span><span class="sxs-lookup"><span data-stu-id="42836-138">Unit</span></span>      |<span data-ttu-id="42836-139">Precio</span><span class="sxs-lookup"><span data-stu-id="42836-139">Price</span></span>      |<span data-ttu-id="42836-140">Moneda</span><span class="sxs-lookup"><span data-stu-id="42836-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="42836-141">Desarrollador</span><span class="sxs-lookup"><span data-stu-id="42836-141">Developer</span></span>   | <span data-ttu-id="42836-142">Contoso EE. UU.</span><span class="sxs-lookup"><span data-stu-id="42836-142">Contoso US</span></span>  |<span data-ttu-id="42836-143">Hora</span><span class="sxs-lookup"><span data-stu-id="42836-143">Hour</span></span> | <span data-ttu-id="42836-144">200</span><span class="sxs-lookup"><span data-stu-id="42836-144">200</span></span>|<span data-ttu-id="42836-145">USD</span><span class="sxs-lookup"><span data-stu-id="42836-145">USD</span></span>     |
| <span data-ttu-id="42836-146">Desarrollador</span><span class="sxs-lookup"><span data-stu-id="42836-146">Developer</span></span>   | <span data-ttu-id="42836-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="42836-147">Contoso India</span></span> |<span data-ttu-id="42836-148">Hora</span><span class="sxs-lookup"><span data-stu-id="42836-148">Hour</span></span>|   <span data-ttu-id="42836-149">112</span><span class="sxs-lookup"><span data-stu-id="42836-149">112</span></span>|<span data-ttu-id="42836-150">USD</span><span class="sxs-lookup"><span data-stu-id="42836-150">USD</span></span>     |


<span data-ttu-id="42836-151">**Tasas de costes de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="42836-151">**Sample cost rates**</span></span>

| <span data-ttu-id="42836-152">Banda salarial</span><span class="sxs-lookup"><span data-stu-id="42836-152">Salary Band</span></span>     | <span data-ttu-id="42836-153">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="42836-153">Org Unit</span></span>    |<span data-ttu-id="42836-154">Unidad</span><span class="sxs-lookup"><span data-stu-id="42836-154">Unit</span></span>      |<span data-ttu-id="42836-155">Precio</span><span class="sxs-lookup"><span data-stu-id="42836-155">Price</span></span>      |<span data-ttu-id="42836-156">Moneda</span><span class="sxs-lookup"><span data-stu-id="42836-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="42836-157">Mi empresa_Banda1</span><span class="sxs-lookup"><span data-stu-id="42836-157">My company_Band1</span></span> | <span data-ttu-id="42836-158">Contoso EE. UU.</span><span class="sxs-lookup"><span data-stu-id="42836-158">Contoso US</span></span>  |<span data-ttu-id="42836-159">Hora</span><span class="sxs-lookup"><span data-stu-id="42836-159">Hour</span></span> | <span data-ttu-id="42836-160">145</span><span class="sxs-lookup"><span data-stu-id="42836-160">145</span></span>|<span data-ttu-id="42836-161">USD</span><span class="sxs-lookup"><span data-stu-id="42836-161">USD</span></span>     |
| <span data-ttu-id="42836-162">Mi empresa_Banda2</span><span class="sxs-lookup"><span data-stu-id="42836-162">My company_Band2</span></span> | <span data-ttu-id="42836-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="42836-163">Contoso India</span></span> |<span data-ttu-id="42836-164">Hora</span><span class="sxs-lookup"><span data-stu-id="42836-164">Hour</span></span>|   <span data-ttu-id="42836-165">67</span><span class="sxs-lookup"><span data-stu-id="42836-165">67</span></span>|<span data-ttu-id="42836-166">USD</span><span class="sxs-lookup"><span data-stu-id="42836-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]