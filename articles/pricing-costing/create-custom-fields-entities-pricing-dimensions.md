---
title: Crear campos y entidades personalizados como dimensiones de precios
description: En este tema se proporciona información sobre cómo crear entidades o conjuntos de opciones personalizados.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275649"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="a448d-103">Crear campos y entidades personalizados como dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="a448d-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="a448d-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="a448d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a448d-105">Complete los siguientes pasos cuando desee crear una entidad o conjunto de opciones personalizada para usarla como dimensión de precios.</span><span class="sxs-lookup"><span data-stu-id="a448d-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="a448d-106">Para obtener más información, consulte la [Información general de dimensiones de precios](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a448d-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="a448d-107">Se recomienda realizar todos los cambios de dimensión de precios personalizados en una solución independiente.</span><span class="sxs-lookup"><span data-stu-id="a448d-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="a448d-108">Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o eliminar cambios según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a448d-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="a448d-109">Esto también ayudará con la reutilización de su trabajo y facilitará la transferencia de estos cambios a otra instancia. Una vez que haya realizado todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para reutilizar su configuración de precios.</span><span class="sxs-lookup"><span data-stu-id="a448d-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="a448d-110">Crear campos personalizados y conjuntos de opciones en la solución de la dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="a448d-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="a448d-111">Las dimensiones de precios pueden ser una entidad o un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="a448d-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="a448d-112">Ambas cosas deben crearse en su solución de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="a448d-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="a448d-113">Los pasos de este procedimiento explican cómo crear dimensiones basadas en entidades y dimensiones basadas en conjuntos de opciones.</span><span class="sxs-lookup"><span data-stu-id="a448d-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="a448d-114">Dimensiones basadas en entidades</span><span class="sxs-lookup"><span data-stu-id="a448d-114">Entity-based dimensions</span></span>
<span data-ttu-id="a448d-115">Para crear dimensiones basadas en entidades, siga los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="a448d-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="a448d-116">Vaya a **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="a448d-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="a448d-117">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="a448d-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="a448d-118">Seleccione **Nuevo** para crear una nueva entidad con el nombre **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="a448d-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="a448d-119">Especifique la información necesaria restante y después seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="a448d-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definición de entidad de título estándar](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="a448d-121">Dimensiones basadas en conjuntos de opciones</span><span class="sxs-lookup"><span data-stu-id="a448d-121">Option set-based dimensions</span></span> 
<span data-ttu-id="a448d-122">Puede crear dos dimensiones basadas en conjuntos de opciones.</span><span class="sxs-lookup"><span data-stu-id="a448d-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="a448d-123">Use la **Ubicación de trabajo del recurso** para realizar un seguimiento del precio del trabajo de la ubicación **Hogar** e **In situ**.</span><span class="sxs-lookup"><span data-stu-id="a448d-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="a448d-124">Use **Horas de trabajo del recurso** con los valores **Regular** y **Horas extra** para aplicar un incremento cuando finalice el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a448d-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="a448d-125">El siguiente gráfico proporciona una vista de la dimensión **Ubicación de trabajo del recurso**.</span><span class="sxs-lookup"><span data-stu-id="a448d-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimensión de precios basada en conjuntos de opciones con el nombre Ubicación de trabajo del recurso](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="a448d-127">El siguiente gráfico proporciona una vista de la dimensión **Horas de trabajo del recurso**.</span><span class="sxs-lookup"><span data-stu-id="a448d-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimensión de precios basada en conjuntos de opciones con el nombre Horas de trabajo del recurso](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="a448d-129">Vaya a **Configuración** > **Soluciones** y haga doble clic en **dimensiones de precios de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="a448d-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="a448d-130">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Conjuntos de opciones**.</span><span class="sxs-lookup"><span data-stu-id="a448d-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="a448d-131">Seleccione **Nuevo** para crear un nuevo conjunto de opciones, especifique la información necesaria restante y después seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="a448d-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="a448d-132">Crear datos para las dimensiones basadas en entidades</span><span class="sxs-lookup"><span data-stu-id="a448d-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="a448d-133">Puede crear datos para las dimensiones basadas en entidades manualmente, o bien mediante llamadas de servicio o importaciones de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a448d-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="a448d-134">Use los pasos de este procedimiento para crear dos títulos estándar, **Ingeniero de sistemas** e **Ingeniero de sistemas sénior** desde la dimensión basada en entidades **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="a448d-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="a448d-135">Si el tamaño de los datos que desea crear es pequeño, como en el siguiente ejemplo, puede usar un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="a448d-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="a448d-136">Seleccione **Búsqueda avanzada**.</span><span class="sxs-lookup"><span data-stu-id="a448d-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="a448d-137">Seleccione la entidad **Título estándar** y, a continuación, **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="a448d-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="a448d-138">Se mostrarán todas las filas de la entidad **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="a448d-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="a448d-139">Seleccione **Nuevo** y, en el campo **Nombre**, escriba "Ingeniero de sistemas" y seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="a448d-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="a448d-140">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="a448d-140">Close the page.</span></span> 
5. <span data-ttu-id="a448d-141">Repita los pasos del 1 al 3 para crear el otro título estándar “Ingeniero de sistemas sénior”.</span><span class="sxs-lookup"><span data-stu-id="a448d-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Datos de ejemplo para la entidad Título estándar](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]