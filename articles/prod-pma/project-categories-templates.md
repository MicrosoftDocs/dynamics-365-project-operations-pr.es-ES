---
title: Sincronizar las categorías de gastos del proyecto entre Finance and Operations y Project Service Automation
description: Este tema describe las plantillas y las tareas subyacentes que se utilizan para sincronizar las categorías de gastos del proyecto entre Microsoft Dynamics 365 Finance y Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289660"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="22855-103">Sincronizar las categorías de gastos del proyecto entre Finance and Operations y Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="22855-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="22855-104">Este tema describe las plantillas y las tareas subyacentes que se utilizan para sincronizar las categorías de gastos del proyecto entre Dynamics 365 Finance y Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22855-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="22855-105">La integración de tareas del proyecto, las categorías de transacciones de gastos, las estimaciones de horas, las estimaciones de gastos y el bloqueo de funciones están disponibles en la versión 8.0.</span><span class="sxs-lookup"><span data-stu-id="22855-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="22855-106">Las integraciones de datos reales están disponibles a partir de la versión 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="22855-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="22855-107">Si utiliza la Enterprise Edition7.3.0, después de instalar KB 4132657 y KB 4132660, podrá usar las plantillas para integrar tareas del proyecto, categorías de transacciones de gastos, estimaciones de horas, estimaciones de gastos y datos reales, y para configurar el bloqueo de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="22855-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="22855-108">Si debe restablecer las distribuciones contables, le recomendamos que también instale KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="22855-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="22855-109">Flujo de datos para Project Service Automation y Finance</span><span class="sxs-lookup"><span data-stu-id="22855-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="22855-110">La solución de integración de Project Service Automation y Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Project Service Automation y Finance.</span><span class="sxs-lookup"><span data-stu-id="22855-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="22855-111">Las plantillas de integración que están disponibles con la función de integración de datos permiten el flujo de datos sobre las categorías de transacciones de gastos entre Finance y Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22855-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="22855-112">Si las categorías de gastos del proyecto se gestionan en Finance, el flujo de integración primero va desde Finance hasta Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22855-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="22855-113">Los identificadores de integración de las categorías de gastos del proyecto se actualizan a través de la sincronización de Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="22855-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="22855-114">Si las categorías de gastos del proyecto se gestionan en Project Service Automation, el flujo de integración primero va desde Project Service Automation hasta Finance.</span><span class="sxs-lookup"><span data-stu-id="22855-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="22855-115">Las categorías de proyectos ya deben estar configuradas en Finance antes de la sincronización desde Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22855-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="22855-116">Luego, sincronice de Finance a Project Service Automation, y luego de Project Service Automation a Finance nuevamente.</span><span class="sxs-lookup"><span data-stu-id="22855-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="22855-117">De esta manera, ayuda a garantizar que las categorías estén vinculadas y que no se creen duplicados.</span><span class="sxs-lookup"><span data-stu-id="22855-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="22855-118">Normalmente, las categorías de gastos del proyecto se gestionan en Finance.</span><span class="sxs-lookup"><span data-stu-id="22855-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="22855-119">Sin embargo, si no es así, o si las categorías de gastos ya se han creado en Project Service Automation, primero debe sincronizar mediante la plantilla de categorías de transacciones de gastos del proyecto (PSA a Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="22855-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="22855-120">Luego, sincronice utilizando la plantilla de categorías de transacciones de gastos del proyecto (Fin and Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="22855-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="22855-121">Luego, debe ejecutar la sincronización de Project Service Automation a Finance una vez más.</span><span class="sxs-lookup"><span data-stu-id="22855-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="22855-122">Si sincroniza primero desde Project Service Automation, se deben cumplir los siguientes requisitos en Finance antes de que se ejecute la sincronización:</span><span class="sxs-lookup"><span data-stu-id="22855-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="22855-123">La categoría compartida que coincide con la categoría de proyecto que se configura en Project Service Automation debe existir y debe estar habilitada para ambos **Proyecto** y **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="22855-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="22855-124">Para cada entidad jurídica de Finance con la que se debe integrar, deben existir las siguientes categorías de proyectos:</span><span class="sxs-lookup"><span data-stu-id="22855-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="22855-125">Existe **Categoría de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="22855-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="22855-126">**Uso en gastos** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="22855-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="22855-127">**Activo en diario** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="22855-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="22855-128">**Tipo de transacción** está establecida en **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="22855-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="22855-129">La siguiente ilustración muestra cómo se sincronizan los datos entre Project Service Automation y Finance.</span><span class="sxs-lookup"><span data-stu-id="22855-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="22855-130">[![Flujo de datos para la integración de Project Service Automation con Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="22855-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="22855-131">Sincronización de las categorías de gastos del proyecto desde Finance a Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="22855-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="22855-132">Plantilla y tarea</span><span class="sxs-lookup"><span data-stu-id="22855-132">Template and task</span></span>

<span data-ttu-id="22855-133">Para tener acceso a la plantilla, en el centro de administración de Microsoft Power Apps, seleccione **Proyectos** y luego, en la esquina superior derecha, seleccione **Nuevo proyecto** para seleccionar plantillas públicas.</span><span class="sxs-lookup"><span data-stu-id="22855-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="22855-134">La siguiente plantilla y la tarea subyacentes se utilizan para sincronizar las categorías de gastos del proyecto de Finance a Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="22855-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="22855-135">**Nombre de la plantilla en Integración de datos**: categorías de transacción de gatos del proyecto (Fin and Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="22855-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="22855-136">**Nombre de la tarea en el proyecto**: sincronizar categorías a PSA.</span><span class="sxs-lookup"><span data-stu-id="22855-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="22855-137">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="22855-137">Entity set</span></span>

| <span data-ttu-id="22855-138">Finanzas</span><span class="sxs-lookup"><span data-stu-id="22855-138">Finance</span></span>                           | <span data-ttu-id="22855-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="22855-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="22855-140">Entidad de integración para categorías</span><span class="sxs-lookup"><span data-stu-id="22855-140">Integration entity for categories</span></span> | <span data-ttu-id="22855-141">Categorías de transacciones</span><span class="sxs-lookup"><span data-stu-id="22855-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="22855-142">Flujo de entidades</span><span class="sxs-lookup"><span data-stu-id="22855-142">Entity flow</span></span>

<span data-ttu-id="22855-143">Las categorías de gastos del proyecto se administran en Finance y se sincronizan con Project Service Automation como categorías de transacciones.</span><span class="sxs-lookup"><span data-stu-id="22855-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="22855-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="22855-144">Power Query</span></span>

<span data-ttu-id="22855-145">Cuando sincroniza con Project Service Automation, debe usar Microsoft Power Query para Excel para establecer el tipo de facturación en la categoría de transacción.</span><span class="sxs-lookup"><span data-stu-id="22855-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="22855-146">La plantilla de categorías de transacciones de gastos del proyecto (Fin and Ops a PSA) proporciona una columna y una asignación predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="22855-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="22855-147">Si crea su propia plantilla, debe agregar una columna condicional en Power Query.</span><span class="sxs-lookup"><span data-stu-id="22855-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="22855-148">Siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="22855-148">Follow these steps.</span></span>

1. <span data-ttu-id="22855-149">Haga clic en la flecha para abrir la asignación de la tarea de categorías de gastos del proyecto en la plantilla de categorías de transacciones de gastos del proyecto (Fin and Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="22855-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="22855-150">Haga clic en el vínculo **Consulta y filtrado avanzados** para abrir Power Query.</span><span class="sxs-lookup"><span data-stu-id="22855-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="22855-151">Seleccione **Agregar columna condicional**.</span><span class="sxs-lookup"><span data-stu-id="22855-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="22855-152">Especifique un nombre para la nueva columna, como **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="22855-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="22855-153">Especifique la siguiente condición: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="22855-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="22855-154">Haga clic en **Aceptar** en la columna.</span><span class="sxs-lookup"><span data-stu-id="22855-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="22855-155">Asegúrese de asignar esta nueva columna en la página de asignaciones.</span><span class="sxs-lookup"><span data-stu-id="22855-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="22855-156">La siguiente ilustración muestra un ejemplo de la asignación de tareas de plantilla en Integración de datos.</span><span class="sxs-lookup"><span data-stu-id="22855-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="22855-157">La asignación muestra la información del campo que se sincronizará de Finance a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22855-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="22855-158">[![Sincronización de las categorías de gastos a la asignación de plantilla de Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="22855-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="22855-159">Sincronización de las categorías de gastos del proyecto desde Project Service Automation a Finance</span><span class="sxs-lookup"><span data-stu-id="22855-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="22855-160">Plantilla y tarea</span><span class="sxs-lookup"><span data-stu-id="22855-160">Template and task</span></span>

<span data-ttu-id="22855-161">La siguiente plantilla y la tarea subyacentes se utilizan para sincronizar las categorías de gastos del proyecto de Project Service Automation a Finance:</span><span class="sxs-lookup"><span data-stu-id="22855-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="22855-162">**Nombre de la plantilla en Integración de datos**: categorías de transacción de gatos del proyecto (PSA A Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="22855-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="22855-163">**Nombre de la tarea en el proyecto**: sincronizar categorías a Fin and Ops.</span><span class="sxs-lookup"><span data-stu-id="22855-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="22855-164">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="22855-164">Entity set</span></span>

| <span data-ttu-id="22855-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="22855-165">Project Service Automation</span></span> | <span data-ttu-id="22855-166">Finanzas</span><span class="sxs-lookup"><span data-stu-id="22855-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="22855-167">Categorías de transacciones</span><span class="sxs-lookup"><span data-stu-id="22855-167">Transaction categories</span></span>     | <span data-ttu-id="22855-168">Entidad de integración para categorías</span><span class="sxs-lookup"><span data-stu-id="22855-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="22855-169">Flujo de entidades</span><span class="sxs-lookup"><span data-stu-id="22855-169">Entity flow</span></span>

<span data-ttu-id="22855-170">Las categorías de gastos del proyecto se administran en Finance y se sincronizan con Project Service Automation como categorías de transacciones.</span><span class="sxs-lookup"><span data-stu-id="22855-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="22855-171">La sincronización de nuevo a Finance actualiza la categoría del proyecto en Finance con el identificador de integración desde Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22855-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="22855-172">Asignación de plantillas en la integración de datos</span><span class="sxs-lookup"><span data-stu-id="22855-172">Template mapping in Data integration</span></span>

<span data-ttu-id="22855-173">La siguiente ilustración muestra un ejemplo de la asignación de tareas de plantilla en Integración de datos.</span><span class="sxs-lookup"><span data-stu-id="22855-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="22855-174">La asignación muestra la información del campo que se sincronizará de Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="22855-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="22855-175">[![Project Service Automation a asignación de plantilla de Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="22855-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]