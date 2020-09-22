---
title: Crear campos y entidades personalizados
description: En este tema se explica cómo crear conjuntos de opciones y entidades en su propia solución de la plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756071"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="f5587-103">Crear campos y entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="f5587-103">Create custom fields and entities</span></span> 

<span data-ttu-id="f5587-104">Complete los pasos siguientes siempre que desee crear una entidad o un conjunto de opciones personalizado en la plataforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="f5587-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="f5587-105">Los procedimientos que se describen en este tema se deben completar mediante la interfaz web de Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="f5587-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5587-106">Se recomienda realizar todos los cambios de dimensión de precios personalizados en una solución independiente.</span><span class="sxs-lookup"><span data-stu-id="f5587-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="f5587-107">Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o quitar cambios según sea necesario. Esto le ayudará a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias.</span><span class="sxs-lookup"><span data-stu-id="f5587-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="f5587-108">Tras realizar todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizar la configuración de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="f5587-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="f5587-109">Crear una solución personalizada para las dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="f5587-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="f5587-110">En PSA, haga clic en **Configuración** > **Soluciones** y después haga clic en **Nuevo** para crear una nueva solución.</span><span class="sxs-lookup"><span data-stu-id="f5587-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="f5587-111">Asigne un nombre a la solución, **dimensiones de precios de \<nombre de su organización> de la organización**, especifique la información restante necesaria y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f5587-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Creación de una solución personalizada para las dimensiones de precios](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="f5587-113">Crear campos personalizados y conjuntos de opciones en la solución de la dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="f5587-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="f5587-114">Las dimensiones de precios pueden ser una entidad o un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="f5587-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="f5587-115">Ambas cosas deben crearse en su solución de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="f5587-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="f5587-116">Los pasos de este procedimiento explican cómo crear dimensiones basadas en entidades y dimensiones basadas en conjuntos de opciones.</span><span class="sxs-lookup"><span data-stu-id="f5587-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="f5587-117">Dimensiones basadas en entidades</span><span class="sxs-lookup"><span data-stu-id="f5587-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="f5587-118">En PSA, haga clic en **Configuración** > **Soluciones** y después haga doble clic en **Dimensiones de precios de \<nombre de su organización>**.</span><span class="sxs-lookup"><span data-stu-id="f5587-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="f5587-119">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="f5587-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="f5587-120">Haga clic en **Nuevo** para crear una nueva entidad con el nombre **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="f5587-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="f5587-121">Especifique la información necesaria restante y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f5587-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definición de entidad de título estándar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="f5587-123">Dimensiones basadas en conjuntos de opciones</span><span class="sxs-lookup"><span data-stu-id="f5587-123">Option set-based dimensions</span></span> 
<span data-ttu-id="f5587-124">Puede crear dos dimensiones basadas en conjuntos de opciones.</span><span class="sxs-lookup"><span data-stu-id="f5587-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="f5587-125">Utilice **Ubicación de trabajo del recurso** para realizar el seguimiento del precio del trabajo de la ubicación **Domicilio** y del trabajo **In situ** y utilice **Horas de trabajo del recurso** con los valores **Regular** y **Horas extra** para aplicar un incremento cuando se complete el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f5587-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="f5587-126">En PSA, haga clic en **Configuración** > **Soluciones** y después haga doble clic en **Dimensiones de precios de \<nombre de su organización>**.</span><span class="sxs-lookup"><span data-stu-id="f5587-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f5587-127">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Conjuntos de opciones**.</span><span class="sxs-lookup"><span data-stu-id="f5587-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="f5587-128">Haga clic en **Nuevo** para crear un nuevo conjunto de opciones, especifique la información necesaria restante y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f5587-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="f5587-129">Dimensión de precios basada en conjuntos de opciones con el nombre Ubicación de trabajo del recurso</span><span class="sxs-lookup"><span data-stu-id="f5587-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="f5587-130">Dimensión de precios basada en conjuntos de opciones con el nombre Horas de trabajo del recurso</span><span class="sxs-lookup"><span data-stu-id="f5587-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="f5587-131">Crear datos para las dimensiones basadas en entidades</span><span class="sxs-lookup"><span data-stu-id="f5587-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="f5587-132">Puede crear datos para las dimensiones basadas en entidades manualmente, o bien mediante llamadas de servicio o importaciones de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f5587-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="f5587-133">Use los pasos de este procedimiento para crear dos títulos estándar, **Ingeniero de sistemas** e **Ingeniero de sistemas sénior** desde la dimensión basada en entidades **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="f5587-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="f5587-134">Si el tamaño de los datos que desea crear es pequeño, como en el siguiente ejemplo, puede usar un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="f5587-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="f5587-135">En PSA, haga clic en **Búsqueda avanzada**.</span><span class="sxs-lookup"><span data-stu-id="f5587-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="f5587-136">Seleccione la entidad **Título estándar** y después haga clic en **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="f5587-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="f5587-137">Se mostrarán todas las filas de la entidad **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="f5587-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="f5587-138">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="f5587-138">Click **New**.</span></span> <span data-ttu-id="f5587-139">En el campo **Nombre**, escriba "Ingeniero de sistemas" y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f5587-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="f5587-140">Cierre el formulario .</span><span class="sxs-lookup"><span data-stu-id="f5587-140">Close the form.</span></span> 
4. <span data-ttu-id="f5587-141">Repita los pasos del 1 al 3 para crear el otro título estándar “Ingeniero de sistemas sénior”.</span><span class="sxs-lookup"><span data-stu-id="f5587-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="f5587-142">Datos de ejemplo para la entidad Título estándar</span><span class="sxs-lookup"><span data-stu-id="f5587-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="f5587-143">Agregue todas las entidades de PSA necesarias y los componentes relacionados a la solución de dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="f5587-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="f5587-144">Deberá agregar las siguientes entidades de Project Service a su solución de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="f5587-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="f5587-145">Use los pasos de este procedimiento para realizar cambios de esquema importantes en la solución de cálculo de precios para que las entidades estén al tanto de las nuevas dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="f5587-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="f5587-146">En PSA, haga clic en **Configuración** > **Soluciones** y después haga doble clic en **Dimensiones de precios de \<nombre de su organización>**.</span><span class="sxs-lookup"><span data-stu-id="f5587-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f5587-147">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Agregar existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="f5587-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="f5587-148">En el cuadro de diálogo **Componentes de la solución**, seleccione las siguientes entidades:</span><span class="sxs-lookup"><span data-stu-id="f5587-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="f5587-149">Real</span><span class="sxs-lookup"><span data-stu-id="f5587-149">Actual</span></span>
- <span data-ttu-id="f5587-150">Recurso que se puede reservar</span><span class="sxs-lookup"><span data-stu-id="f5587-150">Bookable Resource</span></span>
- <span data-ttu-id="f5587-151">Línea de estimación</span><span class="sxs-lookup"><span data-stu-id="f5587-151">Estimate Line</span></span>
- <span data-ttu-id="f5587-152">Detalle de línea de factura</span><span class="sxs-lookup"><span data-stu-id="f5587-152">Invoice Line Detail</span></span>
- <span data-ttu-id="f5587-153">Línea del diario</span><span class="sxs-lookup"><span data-stu-id="f5587-153">Journal Line</span></span>
- <span data-ttu-id="f5587-154">Detalle de línea de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="f5587-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="f5587-155">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="f5587-155">Project Team Member</span></span>
- <span data-ttu-id="f5587-156">Detalle de línea de oferta</span><span class="sxs-lookup"><span data-stu-id="f5587-156">Quote Line Detail</span></span>
- <span data-ttu-id="f5587-157">Incremento del precio de rol</span><span class="sxs-lookup"><span data-stu-id="f5587-157">Role Price Markup</span></span>
- <span data-ttu-id="f5587-158">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="f5587-158">Role Price</span></span> 
- <span data-ttu-id="f5587-159">Entrada de tiempo</span><span class="sxs-lookup"><span data-stu-id="f5587-159">Time Entry</span></span> 

> ![Agregar entidades existentes a la solución de dimensiones de precios](media/Existing-entities-to-PD-solution.png)

> ![Seleccionar componentes de la solución](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="f5587-162">Asegúrese de incluir todos los formularios y las vistas de cada una de las entidades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="f5587-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="f5587-163">Cuando se le pida que incluya las entidades dependientes para las entidades seleccionadas anteriormente, haga clic en **No**.</span><span class="sxs-lookup"><span data-stu-id="f5587-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![No incluya todos los componentes relacionados.](media/Do-not-include-required.png)


