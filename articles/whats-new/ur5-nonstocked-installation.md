---
title: Actualizar Project Operations en el entorno de Finance
description: Este tema proporciona información sobre cómo actualizar Project Operations en el entorno de Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011077"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="392f4-103">Actualizar Project Operations en el entorno de Finance</span><span class="sxs-lookup"><span data-stu-id="392f4-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="392f4-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="392f4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="392f4-105">Este tema proporciona información sobre cómo actualizar Dynamics 365 Project Operations en el entorno de Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="392f4-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="392f4-106">Hay tres procedimientos necesarios para actualizar las operaciones de Project Operations a la actualización 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="392f4-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="392f4-107">Importar el paquete al proyecto de versión preliminar</span><span class="sxs-lookup"><span data-stu-id="392f4-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="392f4-108">Aplicar la actualización</span><span class="sxs-lookup"><span data-stu-id="392f4-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="392f4-109">Actualizar el entorno de Dataverse</span><span class="sxs-lookup"><span data-stu-id="392f4-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="392f4-110">Importar el paquete en el proyecto de LCS</span><span class="sxs-lookup"><span data-stu-id="392f4-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="392f4-111">Inicie sesión en [Lifecycle Services (LCS)](https://lcs.dynamics.com/) como propietario del proyecto o administrador del entorno.</span><span class="sxs-lookup"><span data-stu-id="392f4-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="392f4-112">Seleccione su proyecto de LCS en la lista de proyectos.</span><span class="sxs-lookup"><span data-stu-id="392f4-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="392f4-113">En la página **Proyecto**, en el grupo **Entornos**, abra el entorno que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="392f4-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="392f4-114">Compruebe que el entorno se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="392f4-114">Verify that the environment is running.</span></span> <span data-ttu-id="392f4-115">Si no se ha inicia el entorno, inícielo.</span><span class="sxs-lookup"><span data-stu-id="392f4-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="392f4-116">En la sección **Nueva versión**, en **Actualizaciones disponibles**, seleccione **Ver actualización** para 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="392f4-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Botón Ver actualización](media/view-update.png)

6. <span data-ttu-id="392f4-118">En la página **Actualizaciones binarias**, seleccione **Guardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="392f4-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="392f4-119">En la página **Revisar y guardar actualizaciones**, seleccione **Guardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="392f4-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="392f4-120">En el panel **Guardar paquete en la biblioteca de activos** que se abre, especifique el nombre del paquete y seleccione **Guardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="392f4-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="392f4-121">Cuando LCS haya terminado de guardar el paquete, se habilita el botón **Listo**.</span><span class="sxs-lookup"><span data-stu-id="392f4-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="392f4-122">Seleccione **Listo**.</span><span class="sxs-lookup"><span data-stu-id="392f4-122">Select **Done**.</span></span> <span data-ttu-id="392f4-123">LCS comprobará el paquete.</span><span class="sxs-lookup"><span data-stu-id="392f4-123">LCS will verify the package.</span></span> <span data-ttu-id="392f4-124">La comprobación puede tardar desde unos minutos hasta una hora.</span><span class="sxs-lookup"><span data-stu-id="392f4-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="392f4-125">Aplicar la actualización del paquete</span><span class="sxs-lookup"><span data-stu-id="392f4-125">Apply the package update</span></span>

1. <span data-ttu-id="392f4-126">En LCS, en la página **Detalles del entorno**, seleccione **Mantener** > **Aplicar actualizaciones**.</span><span class="sxs-lookup"><span data-stu-id="392f4-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="392f4-127">En la lista, seleccione el paquete que guardó anteriormente y, a continuación, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="392f4-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="392f4-128">Seleccione **Sí** para confirmar que desea quitar implementar el paquete.</span><span class="sxs-lookup"><span data-stu-id="392f4-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Cuadro de diálogo Confirmar implementación del paquete](media/confirm-package-deployment.png)

4. <span data-ttu-id="392f4-130">Seleccione **Sí** para confirmar que desea actualizar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="392f4-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Cuadro de diálogo Confirmar actualización de la aplicación](media/confirm-application-update.png)

<span data-ttu-id="392f4-132">Se iniciará la implementación y la actualización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="392f4-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="392f4-133">En la página **Detalles del entorno**, en la esquina superior derecha, se actualizará el estado del entorno a **Servicio**.</span><span class="sxs-lookup"><span data-stu-id="392f4-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="392f4-134">La actualización se habrá completado en aproximadamente dos horas.</span><span class="sxs-lookup"><span data-stu-id="392f4-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="392f4-135">La información de versión de la aplicación se actualizará a **Microsoft Dynamics 365 for Finance and Operations 10.0.15** y el estado del entorno se actualizará a **Implementado**.</span><span class="sxs-lookup"><span data-stu-id="392f4-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="392f4-136">Actualizar el entorno de Dataverse</span><span class="sxs-lookup"><span data-stu-id="392f4-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="392f4-137">Inicie sesión en el [Centro de administración de Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="392f4-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="392f4-138">En la lista, busque y abra el entorno que utilizó para instalar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="392f4-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="392f4-139">En la página **Entornos**, seleccione **Recurso** > **Aplicaciones de Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="392f4-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="392f4-140">En la lista, localice **Microsoft Dynamics 365 Project Operations** y, en la columna **Estado**, seleccione **Actualización disponible**.</span><span class="sxs-lookup"><span data-stu-id="392f4-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="392f4-141">Active la casilla **Acepto los términos de servicio** y seleccione **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="392f4-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="392f4-142">Se instalará la versión más reciente de la solución.</span><span class="sxs-lookup"><span data-stu-id="392f4-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="392f4-143">Cuando se haya completado la instalación tendrá instalada la versión 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="392f4-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="392f4-144">Configurar nuevas características</span><span class="sxs-lookup"><span data-stu-id="392f4-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="392f4-145">Habilitar la asignación de doble escritura</span><span class="sxs-lookup"><span data-stu-id="392f4-145">Enable dual-write mapping</span></span>

<span data-ttu-id="392f4-146">Una vez completada la actualización de los entornos de Finance y Dataverse, puede habilitar las asignaciones de doble escritura necesarias.</span><span class="sxs-lookup"><span data-stu-id="392f4-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="392f4-147">Lleve a cabo los procedimientos siguientes para habilitar las asignaciones de doble escritura:</span><span class="sxs-lookup"><span data-stu-id="392f4-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="392f4-148">Actualizar la configuración de seguridad en el entorno de Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="392f4-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="392f4-149">Actualizar entidades de datos</span><span class="sxs-lookup"><span data-stu-id="392f4-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="392f4-150">Actualizar y ejecutar las asignaciones de doble escritura</span><span class="sxs-lookup"><span data-stu-id="392f4-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="392f4-151">Actualizar la configuración de seguridad en el entorno de Dataverse</span><span class="sxs-lookup"><span data-stu-id="392f4-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="392f4-152">Las siguientes actualizaciones de los privilegios de seguridad para las entidades son necesarios para realizar la actualización a UR5.</span><span class="sxs-lookup"><span data-stu-id="392f4-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="392f4-153">En el entorno de Dataverse, vaya a **Configuración** y, en el grupo **Sistema**, seleccione **Seguridad**.</span><span class="sxs-lookup"><span data-stu-id="392f4-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Configuración del entorno de Dataverse](media/Picture21.png)

2. <span data-ttu-id="392f4-155">Seleccione **Roles de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="392f4-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="392f4-156">En la lista de roles, seleccione **usuario de aplicación de doble escritura** y, a continuación, seleccione la pestaña **Entidades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="392f4-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="392f4-157">Compruebe que el rol tenga los permisos **Leer** y **Anexar a** para:</span><span class="sxs-lookup"><span data-stu-id="392f4-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="392f4-158">**Tipo de cambio de la divisa**</span><span class="sxs-lookup"><span data-stu-id="392f4-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="392f4-159">**Plan de cuentas**</span><span class="sxs-lookup"><span data-stu-id="392f4-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="392f4-160">**Calendario fiscal**</span><span class="sxs-lookup"><span data-stu-id="392f4-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="392f4-161">**Ledger**</span><span class="sxs-lookup"><span data-stu-id="392f4-161">**Ledger**</span></span>

5. <span data-ttu-id="392f4-162">Después de actualizar el rol de seguridad, vaya a **Configuración** > **Seguridad** > **Equipos**.</span><span class="sxs-lookup"><span data-stu-id="392f4-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="392f4-163">Compruebe que se haya aplicado al equipo el rol **usuario de la aplicación de doble escritura**.</span><span class="sxs-lookup"><span data-stu-id="392f4-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="392f4-164">Actualizar entidades de datos de la actualización</span><span class="sxs-lookup"><span data-stu-id="392f4-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="392f4-165">En el entorno de Finance, abra el área de trabajo **Gestión de datos** y, a continuación, abra la página **Parámetros del marco**.</span><span class="sxs-lookup"><span data-stu-id="392f4-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="392f4-166">En la pestaña **Configuración de entidad**, seleccione **Actualizar la lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="392f4-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="392f4-167">Seleccione **Cerrar** para confirmar la actualización de la entidad.</span><span class="sxs-lookup"><span data-stu-id="392f4-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="392f4-168">Este proceso tardará aproximadamente 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="392f4-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="392f4-169">Recibirá una notificación cuando se haya completado la actualización.</span><span class="sxs-lookup"><span data-stu-id="392f4-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="392f4-170">Asignaciones de doble escritura</span><span class="sxs-lookup"><span data-stu-id="392f4-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="392f4-171">En el área de trabajo **Administración de datos**, seleccione **Doble escritura**.</span><span class="sxs-lookup"><span data-stu-id="392f4-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="392f4-172">Seleccione **Aplicar soluciones**, seleccione ambas soluciones en la lista y, a continuación, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="392f4-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="392f4-173">En la página **Doble escritura**, seleccione las siguientes asignaciones de tablas y, a continuación, seleccione **Detener**.</span><span class="sxs-lookup"><span data-stu-id="392f4-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="392f4-174">**Datos reales de integración de Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="392f4-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="392f4-175">**Categorías de gastos de proyecto de integración de Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="392f4-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="392f4-176">**Entidad de exportación de gastos de proyecto de datos reales de integración de Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="392f4-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="392f4-177">En la página **Versión de asignación de tabla**, aplique una nueva versión de la asignación a cada una de las tres entidades.</span><span class="sxs-lookup"><span data-stu-id="392f4-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="392f4-178">En la página **Doble escritura**, seleccione ejecutar para reiniciar las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="392f4-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="392f4-179">En la lista de mapas, seleccione la asignación **Contabilidad (msdyn_ledgers)** con todos los requisitos previos y active la casilla **Sincronización inicial**.</span><span class="sxs-lookup"><span data-stu-id="392f4-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="392f4-180">En el campo **Maestro para la sincronización inicial**, seleccione **Aplicaciones de Finance and Operations** y, a continuación, seleccione **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="392f4-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sincronización de asignaciones de contabilidad](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]