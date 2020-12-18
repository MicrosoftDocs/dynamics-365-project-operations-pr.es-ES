---
title: Crear una solución para dimensiones de precios personalizadas
description: Este tema proporciona información sobre cómo crear soluciones para dimensiones de precios personalizadas.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514027"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="90aa4-103">Crear una solución para dimensiones de precios personalizadas</span><span class="sxs-lookup"><span data-stu-id="90aa4-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="90aa4-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="90aa4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="90aa4-105">Todos los cambios de dimensiones de precios personalizadas deben realizarse en una solución independiente.</span><span class="sxs-lookup"><span data-stu-id="90aa4-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="90aa4-106">Esta importante práctica recomendada permite la flexibilidad en el futuro para actualizar o quitar cambios según sea necesario, ayuda a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias.</span><span class="sxs-lookup"><span data-stu-id="90aa4-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="90aa4-107">Tras realizar todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizarla.</span><span class="sxs-lookup"><span data-stu-id="90aa4-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="90aa4-108">Crear una solución para dimensiones de precios personalizadas</span><span class="sxs-lookup"><span data-stu-id="90aa4-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="90aa4-109">Seleccione **Configuración** > **Soluciones** y luego seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="90aa4-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="90aa4-110">Asigne un nombre a la solución, *dimensiones de precios de <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="90aa4-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="90aa4-111">Especifique la información necesaria restante y después seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="90aa4-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Creación de una solución para dimensiones de precios personalizada](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="90aa4-113">Agregue todas las entidades necesarias y los componentes relacionados a la solución de dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="90aa4-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="90aa4-114">Agregue las siguientes entidades de Project Service a su solución de precios para realizar cambios de esquema importantes en la solución de precios.</span><span class="sxs-lookup"><span data-stu-id="90aa4-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="90aa4-115">Una vez que haya completado este procedimiento, las entidades reconocerán las nuevas dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="90aa4-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="90aa4-116">Seleccione **Configuración** > **Soluciones** y después haga doble clic en el **<*nombre de su organización*> dimensiones de precios**.</span><span class="sxs-lookup"><span data-stu-id="90aa4-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="90aa4-117">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Agregar existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="90aa4-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="90aa4-118">En el cuadro de diálogo **Componentes de la solución**, seleccione las siguientes entidades:</span><span class="sxs-lookup"><span data-stu-id="90aa4-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="90aa4-119">**Real**</span><span class="sxs-lookup"><span data-stu-id="90aa4-119">**Actual**</span></span>
   - <span data-ttu-id="90aa4-120">**Recurso que se puede reservar**</span><span class="sxs-lookup"><span data-stu-id="90aa4-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="90aa4-121">**Línea de estimación**</span><span class="sxs-lookup"><span data-stu-id="90aa4-121">**Estimate Line**</span></span>
   - <span data-ttu-id="90aa4-122">**Tarea de proyecto**</span><span class="sxs-lookup"><span data-stu-id="90aa4-122">**Project Task**</span></span>
   - <span data-ttu-id="90aa4-123">**Detalle de línea de factura**</span><span class="sxs-lookup"><span data-stu-id="90aa4-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="90aa4-124">**Línea de diario**</span><span class="sxs-lookup"><span data-stu-id="90aa4-124">**Journal Line**</span></span>
   - <span data-ttu-id="90aa4-125">**Detalle de línea de contrato de proyecto**</span><span class="sxs-lookup"><span data-stu-id="90aa4-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="90aa4-126">**Miembro del equipo del proyecto**</span><span class="sxs-lookup"><span data-stu-id="90aa4-126">**Project Team Member**</span></span>
   - <span data-ttu-id="90aa4-127">**Detalle de línea de oferta**</span><span class="sxs-lookup"><span data-stu-id="90aa4-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="90aa4-128">**Incremento del precio de rol**</span><span class="sxs-lookup"><span data-stu-id="90aa4-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="90aa4-129">**Precio de rol**</span><span class="sxs-lookup"><span data-stu-id="90aa4-129">**Role Price**</span></span>
   - <span data-ttu-id="90aa4-130">**Entrada de tiempo**</span><span class="sxs-lookup"><span data-stu-id="90aa4-130">**Time Entry**</span></span>
 
   ![Agregar solución de dimensión de precios personalizada de entidades existentes](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="90aa4-132">Para cada entidad, revise los componentes que se agregan y la lista final de activos de la entidad para cada entidad.</span><span class="sxs-lookup"><span data-stu-id="90aa4-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="90aa4-133">Incluya todos los formularios y las vistas de cada una de las entidades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="90aa4-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entidades agregadas](./media/solution-component-selection.png)


5.  <span data-ttu-id="90aa4-135">Cuando se le solicite incluir cualquier entidad dependiente para las entidades seleccionadas, seleccione **No, no incluir los componentes necesarios**.</span><span class="sxs-lookup"><span data-stu-id="90aa4-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Entidades dependientes incluidas](./media/Do-not-include-required.png)
