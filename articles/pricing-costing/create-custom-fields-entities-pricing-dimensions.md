---
title: Crear campos y entidades personalizados como dimensiones de precios
description: En este tema se proporciona información sobre cómo crear entidades o conjuntos de opciones personalizados.
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130914"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="d6a4c-103">Crear campos y entidades personalizados como dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="d6a4c-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="d6a4c-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="d6a4c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d6a4c-105">Complete los pasos siguientes siempre que desee crear una entidad o un conjunto de opciones personalizado.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6a4c-106">Se recomienda realizar todos los cambios de dimensión de precios personalizados en una solución independiente.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="d6a4c-107">Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o quitar cambios según sea necesario. Esto le ayudará a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d6a4c-108">Tras realizar todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizar la configuración de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="d6a4c-109">Crear una solución personalizada para las dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="d6a4c-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="d6a4c-110">Vaya a **Configuración** > **Soluciones** y después seleccione **Nuevo** para crear una nueva solución.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="d6a4c-111">Asigne un nombre a la solución, **dimensiones de precios de \<your organization name>**, especifique la información restante necesaria y después seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="d6a4c-112">Crear campos personalizados y conjuntos de opciones en la solución de la dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="d6a4c-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="d6a4c-113">Las dimensiones de precios pueden ser una entidad o un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="d6a4c-114">Ambas cosas deben crearse en su solución de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="d6a4c-115">Los pasos de este procedimiento explican cómo crear dimensiones basadas en entidades y dimensiones basadas en conjuntos de opciones.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="d6a4c-116">Dimensiones basadas en entidades</span><span class="sxs-lookup"><span data-stu-id="d6a4c-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="d6a4c-117">Vaya a **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="d6a4c-118">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="d6a4c-119">Seleccione **Nuevo** para crear una nueva entidad con el nombre **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="d6a4c-120">Especifique la información necesaria restante y después seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="d6a4c-121">Dimensiones basadas en conjuntos de opciones</span><span class="sxs-lookup"><span data-stu-id="d6a4c-121">Option set-based dimensions</span></span> 
<span data-ttu-id="d6a4c-122">Puede crear dos dimensiones basadas en conjuntos de opciones.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="d6a4c-123">Utilice **Ubicación de trabajo del recurso** para realizar el seguimiento del precio del trabajo de la ubicación **Domicilio** y del trabajo **In situ** y utilice **Horas de trabajo del recurso** con los valores **Regular** y **Horas extra** para aplicar un incremento cuando se complete el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="d6a4c-124">Vaya a **Configuración** > **Soluciones** y haga doble clic en **dimensiones de precios de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d6a4c-125">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Conjuntos de opciones**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="d6a4c-126">Seleccione **Nuevo** para crear un nuevo conjunto de opciones, especifique la información necesaria restante y después seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="d6a4c-127">Crear datos para las dimensiones basadas en entidades</span><span class="sxs-lookup"><span data-stu-id="d6a4c-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="d6a4c-128">Puede crear datos para las dimensiones basadas en entidades manualmente, o bien mediante llamadas de servicio o importaciones de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="d6a4c-129">Use los pasos de este procedimiento para crear dos títulos estándar, **Ingeniero de sistemas** e **Ingeniero de sistemas sénior** desde la dimensión basada en entidades **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="d6a4c-130">Si el tamaño de los datos que desea crear es pequeño, como en el siguiente ejemplo, puede usar un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="d6a4c-131">Seleccione **Búsqueda avanzada**, seleccione la entidad **Título estándar** y luego seleccione **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="d6a4c-132">Se mostrarán todas las filas de la entidad **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="d6a4c-133">Seleccione **Nuevo** y, en el campo **Nombre**, escriba "Ingeniero de sistemas" y seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="d6a4c-134">Cerrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-134">Close the form.</span></span> 
4. <span data-ttu-id="d6a4c-135">Repita los pasos del 1 al 3 para crear el otro título estándar “Ingeniero de sistemas sénior”.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d6a4c-136">Agregue todas las entidades necesarias y los componentes relacionados a la solución de dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="d6a4c-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="d6a4c-137">Deberá agregar las siguientes entidades a su solución de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="d6a4c-138">Use los pasos de este procedimiento para realizar cambios de esquema importantes en la solución de cálculo de precios para que las entidades estén al tanto de las nuevas dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="d6a4c-139">Seleccione **Configuración** > **Soluciones** y haga doble clic en **dimensiones de precios de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d6a4c-140">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Agregar existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="d6a4c-141">En el cuadro de diálogo **Componentes de la solución**, seleccione las siguientes entidades:</span><span class="sxs-lookup"><span data-stu-id="d6a4c-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="d6a4c-142">Real</span><span class="sxs-lookup"><span data-stu-id="d6a4c-142">Actual</span></span>
  - <span data-ttu-id="d6a4c-143">Recurso que se puede reservar</span><span class="sxs-lookup"><span data-stu-id="d6a4c-143">Bookable Resource</span></span>
  - <span data-ttu-id="d6a4c-144">Línea de estimación</span><span class="sxs-lookup"><span data-stu-id="d6a4c-144">Estimate Line</span></span>
  - <span data-ttu-id="d6a4c-145">Detalle de línea de factura</span><span class="sxs-lookup"><span data-stu-id="d6a4c-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="d6a4c-146">Línea del diario</span><span class="sxs-lookup"><span data-stu-id="d6a4c-146">Journal Line</span></span>
  - <span data-ttu-id="d6a4c-147">Detalle de línea de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="d6a4c-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="d6a4c-148">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="d6a4c-148">Project Team Member</span></span>
  - <span data-ttu-id="d6a4c-149">Detalle de línea de oferta</span><span class="sxs-lookup"><span data-stu-id="d6a4c-149">Quote Line Detail</span></span>
  - <span data-ttu-id="d6a4c-150">Incremento del precio de rol</span><span class="sxs-lookup"><span data-stu-id="d6a4c-150">Role Price Markup</span></span>
  - <span data-ttu-id="d6a4c-151">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="d6a4c-151">Role Price</span></span> 
  - <span data-ttu-id="d6a4c-152">Entrada de tiempo</span><span class="sxs-lookup"><span data-stu-id="d6a4c-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="d6a4c-153">Asegúrese de incluir todos los formularios y las vistas de cada una de las entidades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="d6a4c-154">Cuando se le pida que incluya las entidades dependientes para las entidades seleccionadas anteriormente, seleccione **No**.</span><span class="sxs-lookup"><span data-stu-id="d6a4c-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

