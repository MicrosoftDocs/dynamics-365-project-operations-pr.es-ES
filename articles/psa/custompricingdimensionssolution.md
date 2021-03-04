---
title: Crear soluciones personalizadas para las dimensiones de precios
description: En este tema se explica cómo crear una solución personalizada al crear dimensiones de precios personalizadas.
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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144660"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="8e421-103">Crear soluciones personalizadas para las dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="8e421-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="8e421-104">Todos los cambios de dimensiones de precios personalizadas deben realizarse en una solución independiente.</span><span class="sxs-lookup"><span data-stu-id="8e421-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="8e421-105">Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o quitar cambios según sea necesario. Esto le ayudará a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias.</span><span class="sxs-lookup"><span data-stu-id="8e421-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="8e421-106">Tras realizar los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizar la configuración de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="8e421-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="8e421-107">Seleccione **Configuración** > **Soluciones** y luego seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="8e421-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="8e421-108">Asigne un nombre a la solución, **dimensiones de precios de \<your organization name>**, especifique la información restante necesaria y después seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="8e421-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Creación de una solución personalizada para las dimensiones de precios](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="8e421-110">Agregue todas las entidades necesarias y los componentes relacionados a la solución de dimensión de precios</span><span class="sxs-lookup"><span data-stu-id="8e421-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="8e421-111">Deberá agregar las siguientes entidades de Project Service a su solución de cálculo de precios.</span><span class="sxs-lookup"><span data-stu-id="8e421-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="8e421-112">Complete los pasos de este procedimiento para realizar cambios de esquema importantes en la solución de cálculo de precios para que las entidades estén al tanto de las nuevas dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="8e421-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="8e421-113">Seleccione **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8e421-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8e421-114">En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Agregar existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="8e421-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="8e421-115">En el cuadro de diálogo **Componentes de la solución**, seleccione las siguientes entidades:</span><span class="sxs-lookup"><span data-stu-id="8e421-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="8e421-116">Real</span><span class="sxs-lookup"><span data-stu-id="8e421-116">Actual</span></span>
- <span data-ttu-id="8e421-117">Recurso que se puede reservar</span><span class="sxs-lookup"><span data-stu-id="8e421-117">Bookable Resource</span></span>
- <span data-ttu-id="8e421-118">Línea de estimación</span><span class="sxs-lookup"><span data-stu-id="8e421-118">Estimate Line</span></span>
- <span data-ttu-id="8e421-119">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="8e421-119">Project Task</span></span>
- <span data-ttu-id="8e421-120">Detalle de línea de factura</span><span class="sxs-lookup"><span data-stu-id="8e421-120">Invoice Line Detail</span></span>
- <span data-ttu-id="8e421-121">Línea de diario</span><span class="sxs-lookup"><span data-stu-id="8e421-121">Journal Line</span></span>
- <span data-ttu-id="8e421-122">Detalle de línea de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="8e421-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="8e421-123">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="8e421-123">Project Team Member</span></span>
- <span data-ttu-id="8e421-124">Detalle de línea de oferta</span><span class="sxs-lookup"><span data-stu-id="8e421-124">Quote Line Detail</span></span>
- <span data-ttu-id="8e421-125">Incremento del precio de rol</span><span class="sxs-lookup"><span data-stu-id="8e421-125">Role Price Markup</span></span>
- <span data-ttu-id="8e421-126">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="8e421-126">Role Price</span></span> 
- <span data-ttu-id="8e421-127">Entrada de tiempo</span><span class="sxs-lookup"><span data-stu-id="8e421-127">Time Entry</span></span> 

> ![Agregar entidades existentes a la solución de dimensiones de precios](media/Existing-entities-to-PD-solution.png)

> ![Seleccionar componentes de la solución](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="8e421-130">Asegúrese de incluir todos los formularios y las vistas de cada una de las entidades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="8e421-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="8e421-131">Cuando se le pida que incluya las entidades dependientes para las entidades seleccionadas, seleccione **No**.</span><span class="sxs-lookup"><span data-stu-id="8e421-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![No incluya todos los componentes relacionados.](media/Do-not-include-required.png)


