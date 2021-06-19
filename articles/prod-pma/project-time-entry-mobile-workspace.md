---
title: Espacio de trabajo móvil de entrada de tiempo del proyecto
description: En este tema se proporciona información sobre el espacio de trabajo móvil Entrada de tiempo del proyecto. Este espacio de trabajo permite a los usuarios especificar y ahorrar tiempo en un proyecto mediante el uso de su dispositivo móvil.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f087e15780272fd376a14b42ed9e00420f86a61f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009952"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="fb7a4-104">Espacio de trabajo móvil de entrada de tiempo del proyecto</span><span class="sxs-lookup"><span data-stu-id="fb7a4-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb7a4-105">En este tema se proporciona información sobre el espacio de trabajo móvil **Entrada de tiempo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="fb7a4-106">Este espacio de trabajo permite a los usuarios especificar y ahorrar tiempo en un proyecto mediante el uso de su dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="fb7a4-107">Este espacio de trabajo móvil está diseñado para utilizarse con la aplicación móvil de operaciones unificadas de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="fb7a4-108">Información general</span><span class="sxs-lookup"><span data-stu-id="fb7a4-108">Overview</span></span>
<span data-ttu-id="fb7a4-109">Como parte de su trabajo diario, los recursos del proyecto a menudo se encuentran en el sitio o están en movimiento.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="fb7a4-110">El espacio de trabajo móvil **Entrada de tiempo del proyecto** permite a los usuarios introducir su tiempo facturable o no facturable en un proyecto en el dispositivo móvil de su elección.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="fb7a4-111">Por lo tanto, los recursos del proyecto pueden registrar entradas de tiempo en cualquier momento y lugar.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="fb7a4-112">También pueden ver las entradas de tiempo que ya se han registrado.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="fb7a4-113">Concretamente, en el espacio de trabajo móvil **Entrada de tiempo del proyecto**, los usuarios pueden realizar estas tareas:</span><span class="sxs-lookup"><span data-stu-id="fb7a4-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="fb7a4-114">Para cualquier fecha seleccionada, introducir el número de horas que dedicó a una tarea determinada.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="fb7a4-115">Buscar por nombre de proyecto o cliente para encontrar el proyecto en el que introducir el tiempo.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="fb7a4-116">Especificar la categoría y la actividad del tiempo que dedicó.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="fb7a4-117">Registre el tiempo como facturable o no facturable para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="fb7a4-118">Opcionalmente, especifique cualquier comentario externo o interno.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fb7a4-119">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fb7a4-119">Prerequisites</span></span>
<span data-ttu-id="fb7a4-120">Los requisitos previos varían según la versión de Microsoft Dynamics 365 que se haya implementado en la organización.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="fb7a4-121">Requisitos previos si usa Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="fb7a4-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="fb7a4-122">Si se ha implementado Finance para la organización, el administrador del sistema debe publicar el espacio de trabajo para dispositivos móviles **Entrada de tiempo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="fb7a4-123">Para obtener instrucciones, consulte [Publicar espacios de trabajo para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-123">For instructions, see [Publish a mobile workspace](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="fb7a4-124">Requisitos previos si usa la versión 1611 con Platform update 3 o posterior</span><span class="sxs-lookup"><span data-stu-id="fb7a4-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="fb7a4-125">Si se implementó la versión 1611 con Platform update 3 o posterior para su organización, el administrador del sistema debe completar los siguientes requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fb7a4-126">Requisito previo</span><span class="sxs-lookup"><span data-stu-id="fb7a4-126">Prerequisite</span></span></th>
<th><span data-ttu-id="fb7a4-127">Rol</span><span class="sxs-lookup"><span data-stu-id="fb7a4-127">Role</span></span></th>
<th><span data-ttu-id="fb7a4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb7a4-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="fb7a4-129">Implementar KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="fb7a4-130">Administrador del sistema</span><span class="sxs-lookup"><span data-stu-id="fb7a4-130">System administrator</span></span></td>
<td><span data-ttu-id="fb7a4-131">KB 4018050 es una actualización de X++ o revisión de metadatos que contiene el espacio de trabajo para dispositivos móviles <strong>Entrada de tiempo del proyecto</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="fb7a4-132">Para implementar KB 4018050, su administrador del sistema debe seguir estos pasos.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="fb7a4-133"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Descargue la revisión de metadatos de Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-133"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="fb7a4-134"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instale la revisión de metadatos</a>.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-134"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="fb7a4-135"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Cree un paquete que se pueda implementar</a> que contiene los modelos <strong>ApplicationSuite</strong> y <strong>ProjectMobile</strong> y luego cargue el paquete que se puede implementar en LCS.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-135"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="fb7a4-136"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplique el paquete que se puede implementar</a>.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-136"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb7a4-137">Publique el espacio de trabajo para dispositivos móviles <strong>Entrada de tiempo del proyecto</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="fb7a4-138">Administrador del sistema</span><span class="sxs-lookup"><span data-stu-id="fb7a4-138">System administrator</span></span></td>
<td><span data-ttu-id="fb7a4-139">Consulte <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar espacios de trabajo para dispositivos móviles</a>.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-139">See <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="fb7a4-140">Descargar e instalar la aplicación móvil</span><span class="sxs-lookup"><span data-stu-id="fb7a4-140">Download and install the mobile app</span></span>

<span data-ttu-id="fb7a4-141">Descargar e instalar la aplicación móvil Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="fb7a4-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="fb7a4-142">Para teléfonos Android</span><span class="sxs-lookup"><span data-stu-id="fb7a4-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="fb7a4-143">Para iPhones</span><span class="sxs-lookup"><span data-stu-id="fb7a4-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="fb7a4-144">Iniciar sesión en la aplicación móvil</span><span class="sxs-lookup"><span data-stu-id="fb7a4-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="fb7a4-145">Inicie la aplicación en el dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="fb7a4-146">Introduzca la URL de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="fb7a4-147">La primera vez que inicie sesión, se le solicitará su nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="fb7a4-148">Especifique sus credenciales.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="fb7a4-149">Después de iniciar sesión, se muestran los espacios de trabajo disponibles para su empresa.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="fb7a4-150">Tenga en cuenta que si el administrador del sistema publica un nuevo espacio de trabajo más tarde, deberá actualizar la lista de espacios de trabajo para dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="fb7a4-151">[![Deslizar para actualizar](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="fb7a4-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="fb7a4-152">Especificar el tiempo utilizando el espacio de trabajo para dispositivos móviles Entrada de tiempo del proyecto</span><span class="sxs-lookup"><span data-stu-id="fb7a4-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="fb7a4-153">En su dispositivo móvil, seleccione el espacio de trabajo **Entrada de tiempo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="fb7a4-154">Seleccione **Entrada de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-154">Select **Time entry**.</span></span> <span data-ttu-id="fb7a4-155">Se muestran las fechas del calendario de la semana actual.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="fb7a4-156">Para una fecha seleccionada, seleccione **Acciones** &gt; **Nueva entrada**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="fb7a4-157">Escriba el número de horas que desea registrar.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="fb7a4-158">Seleccione el proyecto para la entrada de horas.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-158">Select the project for the time entry.</span></span> <span data-ttu-id="fb7a4-159">Una lista muestra los proyectos que se cargan en su aplicación para su uso sin conexión.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="fb7a4-160">De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="fb7a4-161">Para obtener más información, consulte [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-161">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="fb7a4-162">Si su proyecto no está en la lista, seleccione **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="fb7a4-163">Busque por nombre o cambie para buscar por nombre de proyecto o cliente.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="fb7a4-164">Seleccione una categoría.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-164">Select a category.</span></span> <span data-ttu-id="fb7a4-165">Una lista muestra las categorías que se cargan en su aplicación para su uso sin conexión.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="fb7a4-166">De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="fb7a4-167">Para obtener más información, consulte [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-167">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="fb7a4-168">Si su categoría no está en la lista, seleccione **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="fb7a4-169">Busque por categoría o cambie para buscar por nombre de categoría.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="fb7a4-170">Seleccione una actividad.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-170">Select an activity.</span></span> <span data-ttu-id="fb7a4-171">Una lista muestra las actividades que se cargan en su aplicación para su uso sin conexión.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="fb7a4-172">De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="fb7a4-173">Para obtener más información, consulte [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-173">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="fb7a4-174">Si su actividad no está en la lista, seleccione **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="fb7a4-175">Busque por número de actividad o cambie para buscar por propósito.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="fb7a4-176">Seleccione la propiedad de línea.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-176">Select the line property.</span></span>
12. <span data-ttu-id="fb7a4-177">Opcionalmente: especifique cualquier comentario externo e interno.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="fb7a4-178">Seleccione **Listo**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]