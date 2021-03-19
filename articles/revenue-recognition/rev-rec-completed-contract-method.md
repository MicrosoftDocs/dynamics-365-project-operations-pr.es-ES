---
title: Administrar estimaciones de ingresos
description: En este tema se proporciona información acerca de cómo trabajar con estimaciones de ingresos para proyectos.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279024"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="b6f8f-103">Administrar estimaciones de ingresos</span><span class="sxs-lookup"><span data-stu-id="b6f8f-103">Manage revenue estimates</span></span>

<span data-ttu-id="b6f8f-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="b6f8f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b6f8f-105">Puede crear, calcular, registrar, revertir o eliminar estimaciones de ingresos.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="b6f8f-106">Puede hacerlo manualmente o mediante un proceso periódico.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="b6f8f-107">En este tema se proporciona información acerca de cómo trabajar con estimaciones de ingresos para proyectos.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="b6f8f-108">Administrar estimaciones de ingresos manualmente</span><span class="sxs-lookup"><span data-stu-id="b6f8f-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="b6f8f-109">En el proyecto de estimación de ingresos a precio fijo o la página **Consulta de estimación** (**Gestión de proyectos y contabilidad** > **Informes y consultas** > **Estimaciones de consultas e informes**), seleccione **Estimaciones**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="b6f8f-110">Administrar estimaciones de ingresos mediante un proceso periódico</span><span class="sxs-lookup"><span data-stu-id="b6f8f-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="b6f8f-111">Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Estimaciones** y seleccione el proceso correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="b6f8f-112">Crear una estimación de ingresos</span><span class="sxs-lookup"><span data-stu-id="b6f8f-112">Create a revenue estimate</span></span>

<span data-ttu-id="b6f8f-113">Para crear una estimación de ingresos, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="b6f8f-114">Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Estimaciones**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="b6f8f-115">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-115">Select **New**.</span></span> <span data-ttu-id="b6f8f-116">En la página **Creación de estimaciones**, seleccione los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="b6f8f-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="b6f8f-117">**Código de período**: este código determina la frecuencia con la que se registran las estimaciones.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="b6f8f-118">**Fecha estimada**: la fecha en que se procesa la estimación.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="b6f8f-119">**Continuo**: seleccione esta casilla para crear estimaciones solo si se registraron estimaciones en el período anterior o si la estimación es la primera estimación que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="b6f8f-120">Si no se selecciona, se crean estimaciones incluso si las estimaciones no se registraron en el período anterior.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="b6f8f-121">**Coste para completar el método**: defina cómo estimar el trabajo restante del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="b6f8f-122">Para más información, consulte [Coste para completar métodos](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b6f8f-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="b6f8f-123">**Método de finalización**: seleccione un método de finalización entre las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="b6f8f-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="b6f8f-124">**Automático**: el porcentaje de finalización se calcula automáticamente y se basa en las líneas de coste incluidas en el cálculo.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="b6f8f-125">La plantilla de coste define las líneas de costes que se incluyen.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="b6f8f-126">**Manual**: el porcentaje de finalización es igual al porcentaje de finalización de la última estimación.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="b6f8f-127">Una vez creado la estimación, puede cambiar el **Cálculo manual** en la página **Estimaciones**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="b6f8f-128">**De la plantilla de coste**: una combinación de los métodos automático y manual.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="b6f8f-129">Esta opción se establece automática o manualmente, según el valor predeterminado de la plantilla de coste.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="b6f8f-130">**Modelo de previsión**: seleccione un modelo de previsión para la estimación.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="b6f8f-131">**Imprimir lista de estimaciones**: cree y muestre una lista de estimaciones.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="b6f8f-132">La lista contiene el estado de la función actual.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-132">The list contains the status of the current function.</span></span> <span data-ttu-id="b6f8f-133">Puede imprimir cualquier advertencia sobre la estimación en el informe.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="b6f8f-134">Las siguientes condiciones hacen que aparezcan advertencias en la lista de estimaciones:</span><span class="sxs-lookup"><span data-stu-id="b6f8f-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="b6f8f-135">Un porcentaje de finalización de más del 100 por ciento.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="b6f8f-136">Un porcentaje de finalización menor del cero por ciento.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="b6f8f-137">Un importe negativo en la columna **Para completar**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="b6f8f-138">Una estimación sin importe de contrato correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="b6f8f-139">Una estimación sin estimación de coste adjunta.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="b6f8f-140">**Mostrar registro de información**: seleccione esta opción para recibir un mensaje que contiene información acerca de los proyectos de estimaciones que se procesaron cuando se ejecutó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="b6f8f-141">Registrar trabajos en curso o acumulaciones</span><span class="sxs-lookup"><span data-stu-id="b6f8f-141">Post WIP or accruals</span></span>

<span data-ttu-id="b6f8f-142">Después de evaluar las estimaciones, se mantienen, disminuyen o aumentan.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="b6f8f-143">A continuación, puede registrar el trabajo en curso cuando trabaje con el principio de evaluación **Contrato completado**, o registre las acumulaciones cuando trabaje con el principio de evaluación **Porcentaje completado**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="b6f8f-144">El estado del período de estimación cambia de **Creado** a **Registrado**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="b6f8f-145">Trabajo en curso inverso o acumulaciones</span><span class="sxs-lookup"><span data-stu-id="b6f8f-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="b6f8f-146">Utilice la opción de inversión para acreditar trabajo en curso o acumulaciones ya registradas, y luego cree estimaciones para el período.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="b6f8f-147">Para revertir un período que se encuentra entre otros, invierta los períodos estimados necesarios y luego vuelva a registrarlos.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="b6f8f-148">Como todos los períodos posteriores dependen de las estimaciones del período anterior, no omita ningún período.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="b6f8f-149">Eliminar el proyecto de estimación y finalizar el proyecto</span><span class="sxs-lookup"><span data-stu-id="b6f8f-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="b6f8f-150">El paso final en el proceso de estimación es eliminar el proyecto de estimación y finalizar el proyecto de precio fijo cuando el porcentaje de finalización alcanza el 100 por ciento.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="b6f8f-151">Lo siguiente se produce al ejecutar la eliminación:</span><span class="sxs-lookup"><span data-stu-id="b6f8f-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="b6f8f-152">Para un proyecto de precio fijo con un contrato completado, los valores de trabajo en curso se borran de las cuentas de saldo y se registran en las cuentas de pérdidas y ganancias.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="b6f8f-153">Para un proyecto de precio fijo con un porcentaje completado, las acumulaciones se eliminan de las cuentas de pérdidas y ganancias.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="b6f8f-154">La estimación cambia el estado a **Eliminado**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="b6f8f-155">En casos especiales, el porcentaje puede extenderse más allá del 100 por cien.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="b6f8f-156">Cuando esto suceda, reduzca el porcentaje de finalización con **Establecer coste para completar en método cero** para llegar al 100 por cien.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="b6f8f-157">Invertir eliminación</span><span class="sxs-lookup"><span data-stu-id="b6f8f-157">Reverse elimination</span></span>

1. <span data-ttu-id="b6f8f-158">Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Estimaciones** > **Invertir eliminación**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="b6f8f-159">En el panel de acciones, en la pestaña **Proceso**, en el grupo **Mantener**, seleccione **Estimación**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="b6f8f-160">Seleccione **Invertir eliminación**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="b6f8f-161">Utilice esta página para invertir todas las eliminaciones con una fecha estimada especificada y con un estado estimado de **Eliminado**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="b6f8f-162">El estado de la transacción cambia después de seleccionar los campos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="b6f8f-163">Esto también cambia automáticamente el estado del proyecto a **En curso** si la fase del proyecto está establecida como finalizada.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="b6f8f-164">El estado de estimación del período del proyecto vuelve a cambiar a **Registrado**.</span><span class="sxs-lookup"><span data-stu-id="b6f8f-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]