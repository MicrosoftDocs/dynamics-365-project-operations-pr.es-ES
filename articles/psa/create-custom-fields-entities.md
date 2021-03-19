---
title: Crear campos y entidades personalizados
description: En este tema se explica cómo crear conjuntos de opciones y entidades en su propia solución de la plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290559"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="db367-103">Crear campos y entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="db367-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="db367-104">Complete los pasos siguientes siempre que desee crear una entidad o un conjunto de opciones personalizado en la plataforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="db367-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="db367-105">Los procedimientos que se describen en este tema se deben completar mediante la interfaz web de Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="db367-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db367-106">Se recomienda realizar todos los cambios de dimensión de precios personalizados en una solución independiente.</span><span class="sxs-lookup"><span data-stu-id="db367-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="db367-107">Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o quitar cambios según sea necesario. Esto le ayudará a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias.</span><span class="sxs-lookup"><span data-stu-id="db367-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="db367-108">Tras realizar todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizar la configuración de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="db367-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="db367-109">Crear campos personalizados y conjuntos de opciones en la solución de la dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="db367-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="db367-110">Las dimensiones de precios pueden ser una entidad o un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="db367-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="db367-111">Ambas cosas deben crearse en su solución de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="db367-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="db367-112">Los pasos de este procedimiento explican cómo crear dimensiones basadas en entidades y dimensiones basadas en conjuntos de opciones.</span><span class="sxs-lookup"><span data-stu-id="db367-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="db367-113">Dimensiones basadas en entidades</span><span class="sxs-lookup"><span data-stu-id="db367-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="db367-114">En PSA, haga clic en **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="db367-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="db367-115">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="db367-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="db367-116">Haga clic en **Nuevo** para crear una nueva entidad con el nombre **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="db367-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="db367-117">Especifique la información necesaria restante y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="db367-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definición de entidad de título estándar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="db367-119">Dimensiones basadas en conjuntos de opciones</span><span class="sxs-lookup"><span data-stu-id="db367-119">Option set-based dimensions</span></span> 
<span data-ttu-id="db367-120">Puede crear dos dimensiones basadas en conjuntos de opciones.</span><span class="sxs-lookup"><span data-stu-id="db367-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="db367-121">Utilice **Ubicación de trabajo del recurso** para realizar el seguimiento del precio del trabajo de la ubicación **Domicilio** y del trabajo **In situ** y utilice **Horas de trabajo del recurso** con los valores **Regular** y **Horas extra** para aplicar un incremento cuando se complete el trabajo.</span><span class="sxs-lookup"><span data-stu-id="db367-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="db367-122">En PSA, haga clic en **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="db367-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="db367-123">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Conjuntos de opciones**.</span><span class="sxs-lookup"><span data-stu-id="db367-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="db367-124">Haga clic en **Nuevo** para crear un nuevo conjunto de opciones, especifique la información necesaria restante y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="db367-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="db367-125">Dimensión de precios basada en conjuntos de opciones con el nombre Ubicación de trabajo del recurso</span><span class="sxs-lookup"><span data-stu-id="db367-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="db367-126">Dimensión de precios basada en conjuntos de opciones con el nombre Horas de trabajo del recurso</span><span class="sxs-lookup"><span data-stu-id="db367-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="db367-127">Crear datos para las dimensiones basadas en entidades</span><span class="sxs-lookup"><span data-stu-id="db367-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="db367-128">Puede crear datos para las dimensiones basadas en entidades manualmente, o bien mediante llamadas de servicio o importaciones de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="db367-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="db367-129">Use los pasos de este procedimiento para crear dos títulos estándar, **Ingeniero de sistemas** e **Ingeniero de sistemas sénior** desde la dimensión basada en entidades **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="db367-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="db367-130">Si el tamaño de los datos que desea crear es pequeño, como en el siguiente ejemplo, puede usar un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="db367-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="db367-131">En PSA, haga clic en **Búsqueda avanzada**.</span><span class="sxs-lookup"><span data-stu-id="db367-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="db367-132">Seleccione la entidad **Título estándar** y después haga clic en **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="db367-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="db367-133">Se mostrarán todas las filas de la entidad **Título estándar**.</span><span class="sxs-lookup"><span data-stu-id="db367-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="db367-134">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="db367-134">Click **New**.</span></span> <span data-ttu-id="db367-135">En el campo **Nombre**, escriba "Ingeniero de sistemas" y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="db367-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="db367-136">Cierre el formulario .</span><span class="sxs-lookup"><span data-stu-id="db367-136">Close the form.</span></span> 
4. <span data-ttu-id="db367-137">Repita los pasos del 1 al 3 para crear el otro título estándar “Ingeniero de sistemas sénior”.</span><span class="sxs-lookup"><span data-stu-id="db367-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="db367-138">Datos de ejemplo para la entidad Título estándar</span><span class="sxs-lookup"><span data-stu-id="db367-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]