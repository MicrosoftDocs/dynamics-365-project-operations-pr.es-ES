---
title: Integración Microsoft Project Client
description: La planificación y el mantenimiento del programa de un proyecto pueden ser complejos, por lo que los jefes de proyectos deben usar herramientas que les ayuden a administrar esta tarea. La integración con Microsoft Project Client brinda soporte para abrir y administrar una estructura de desglose del trabajo del proyecto.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756066"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="b2216-104">Integración Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b2216-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2216-105">La planificación y el mantenimiento del programa de un proyecto pueden ser complejos, por lo que los jefes de proyectos deben usar herramientas que les ayuden a administrar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="b2216-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="b2216-106">La integración con Microsoft Project Client brinda soporte para abrir y administrar una estructura de desglose del trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b2216-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="b2216-107">El director del proyecto puede volver a publicar cualquier cambio en la estructura de descomposición del trabajo de Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b2216-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="b2216-108">Si está utilizando la actualización de julio (versión 10.0.4), debe instalar KB 4054797 y 4055884.</span><span class="sxs-lookup"><span data-stu-id="b2216-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="b2216-109">Configurar el complemento de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b2216-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="b2216-110">Para habilitar la integración con Microsoft Project Client, es encesario instalar un complemento de Microsoft Dynamics 365 en la aplicación cliente del usuario de Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="b2216-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="b2216-111">Esto se hace abriendo el **Espacio de trabajo de gestión de proyectos**.</span><span class="sxs-lookup"><span data-stu-id="b2216-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="b2216-112">• Haga clic en **Configurar el complemento de cliente del proyecto** en la sección **Vínculos** > **Configuración** del espacio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b2216-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="b2216-113">• Haga clic en **Abrir** y luego en **Ejecutar** cuando se le solicite.</span><span class="sxs-lookup"><span data-stu-id="b2216-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="b2216-114">Abrir y editar una estructura de descomposición del trabajo en Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b2216-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="b2216-115">Si un proyecto en Dynamics 365 Finance ya tiene una estructura de desglose de trabajo creada, la estructura de descomposición del trabajo se puede abrir en la aplicación Microsoft Project Client si la estructura de descomposición del trabajo está en un estado de borrador.</span><span class="sxs-lookup"><span data-stu-id="b2216-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="b2216-116">Para abrir desde la página **Proyecto**, haga clic en el vínculo **Abrir en Microsoft Project** desde la pestaña **Plan**. Esta página también se puede abrir desde la aplicación Microsoft Project Client haciendo clic en **Abrir** en la pestaña **Microsoft Dynamics 365**. Seleccione **Entidad jurídica** y **Proyecto** desde la lista.</span><span class="sxs-lookup"><span data-stu-id="b2216-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="b2216-117">Si está usando Internet Explorer como su explorador, deberá hacer clic en **Guardar** para abrir manualmente desde la ubicación en la que se descargó el archivo.</span><span class="sxs-lookup"><span data-stu-id="b2216-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="b2216-118">O haga clic en **Guardar y abrir** para abrir el archivo en Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b2216-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="b2216-119">No cambie el nombre del archivo al guardar.</span><span class="sxs-lookup"><span data-stu-id="b2216-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="b2216-120">Antes de realizar modificaciones en el archivo con Microsoft Project Client, debe verificarlo. Haga clic **Comprobar** en la pestaña **Microsoft Dynamics 365**. Esto evitará que otros usuarios editen la estructura de descomposición del trabajo desde Finance al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b2216-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="b2216-121">Para publicar la estructura de descomposición del trabajo después de completar cualquier edición, haga clic en **Registrarse** en la pestaña **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b2216-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="b2216-122">Si ya se ha agregado un equipo de proyecto al proyecto en Finance, la lista de recursos se completará con los miembros del equipo.</span><span class="sxs-lookup"><span data-stu-id="b2216-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="b2216-123">Si aún no se ha agregado un equipo de proyecto al proyecto, puede seleccionar recursos y crear el equipo dentro de Microsoft Project Client haciendo clic en el botón **Recursos** en la pestaña **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b2216-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="b2216-124">Los siguientes datos se sincronizarán con Finance como parte del proceso de registro:</span><span class="sxs-lookup"><span data-stu-id="b2216-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="b2216-125">• Nombre de la tarea</span><span class="sxs-lookup"><span data-stu-id="b2216-125">•   Task name</span></span>

<span data-ttu-id="b2216-126">• Fecha de inicio</span><span class="sxs-lookup"><span data-stu-id="b2216-126">•   Start date</span></span>

<span data-ttu-id="b2216-127">• Fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="b2216-127">•   Finish date</span></span>

<span data-ttu-id="b2216-128">• Predecesoras</span><span class="sxs-lookup"><span data-stu-id="b2216-128">•   Predecessors</span></span>

<span data-ttu-id="b2216-129">• Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="b2216-129">•   Resource names</span></span>

<span data-ttu-id="b2216-130">• Categoría</span><span class="sxs-lookup"><span data-stu-id="b2216-130">•   Category</span></span>

<span data-ttu-id="b2216-131">• Categoría de recurso</span><span class="sxs-lookup"><span data-stu-id="b2216-131">•   Resource category</span></span>

<span data-ttu-id="b2216-132">• Horas laborables</span><span class="sxs-lookup"><span data-stu-id="b2216-132">•   Work hours</span></span>

<span data-ttu-id="b2216-133">• Notas</span><span class="sxs-lookup"><span data-stu-id="b2216-133">•   Notes</span></span>

<span data-ttu-id="b2216-134">• Prioridad</span><span class="sxs-lookup"><span data-stu-id="b2216-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="b2216-135">Si agrega otras columnas a su archivo de Microsoft Project Client, no se guardarán en el archivo y no se mostrarán cuando el archivo se abra nuevamente.</span><span class="sxs-lookup"><span data-stu-id="b2216-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="b2216-136">Crear la estructura de descomposición del trabajo para un proyecto existente utilizando Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b2216-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="b2216-137">Para crear una estructura de descomposición del trabajo nueva para un proyecto existente utilizando Microsoft Project Client, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="b2216-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="b2216-138">Abra Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b2216-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="b2216-139">En la pestaña **Microsoft Dynamics 365**, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="b2216-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="b2216-140">Seleccione la **Entidad jurídica** para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b2216-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="b2216-141">Seleccione el **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="b2216-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="b2216-142">Haga clic en **Comprobar** en la pestaña **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b2216-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="b2216-143">Cuando esté listo para publicar en Finance, haga clic en **Registrarse** en la pestaña **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b2216-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="b2216-144">Sustituir la estructura de descomposición del trabajo existente para un proyecto existente utilizando Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b2216-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="b2216-145">Para crear una nueva estructura de descomposición del trabajo con Microsoft Project Client y reemplazar una estructura de descomposición del trabajo existente para un proyecto existente, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="b2216-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="b2216-146">Abra Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b2216-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="b2216-147">Cree el programa en Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b2216-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="b2216-148">En la pestaña **Microsoft Dynamics 365**, haga clic en **Guardar cambios** > **Reemplazar proyecto existente**.</span><span class="sxs-lookup"><span data-stu-id="b2216-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="b2216-149">Seleccione la **Entidad jurídica** para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b2216-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="b2216-150">Seleccione el **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="b2216-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="b2216-151">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b2216-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="b2216-152">Cree un nuevo proyecto desde Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b2216-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="b2216-153">Abra Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b2216-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="b2216-154">Cree el programa en Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b2216-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="b2216-155">En la pestaña **Microsoft Dynamics 365**, haga clic en **Guardar cambios** > **Guardar en nuevo proyecto**.</span><span class="sxs-lookup"><span data-stu-id="b2216-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="b2216-156">Seleccione la **Entidad jurídica** para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b2216-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="b2216-157">Especifique **Id. del proyecto**, si necesario.</span><span class="sxs-lookup"><span data-stu-id="b2216-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="b2216-158">Especifique el **Nombre del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="b2216-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="b2216-159">Seleccione **Tipo de proyecto**, **Grupo de proyecto** e **Id. del contrato del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="b2216-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="b2216-160">Alternativamente, puede crear un nuevo contrato de proyecto haciendo clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="b2216-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="b2216-161">Selecciona el **Calendario** que se va a utilizar para dotar de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2216-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="b2216-162">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b2216-162">Click **OK**.</span></span>
