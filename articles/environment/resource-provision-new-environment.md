---
title: Aprovisionar un entorno nuevo
description: Este tema proporciona información sobre cómo aprovisionar un nuevo entorno de Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950555"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="428fc-103">Aprovisionar un entorno nuevo</span><span class="sxs-lookup"><span data-stu-id="428fc-103">Provision a new environment</span></span>

<span data-ttu-id="428fc-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="428fc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="428fc-105">Este tema proporciona información sobre cómo aprovisionar un nuevo entorno de Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.</span><span class="sxs-lookup"><span data-stu-id="428fc-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="428fc-106">Habilitear el aprovisionamiento automatizado de Project Operations en un proyecto LCS</span><span class="sxs-lookup"><span data-stu-id="428fc-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="428fc-107">Utilice los siguientes pasos para habilitar el flujo de aprovisionamiento automatizado de Project Operations para su proyecto LCS.</span><span class="sxs-lookup"><span data-stu-id="428fc-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="428fc-108">Vaya a [LCS](https://lcs.dynamics.com/v2) y seleccione el icono **Gestión de funciones de vista previa**.</span><span class="sxs-lookup"><span data-stu-id="428fc-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="428fc-109">En la lista **Característica de vista previa**, seleccione **Característica de Project Operations** y después seleccione **Función de vista previa habilitada** para habilitar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="428fc-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="428fc-110">Este paso se realiza solo una vez por proyecto LCS.</span><span class="sxs-lookup"><span data-stu-id="428fc-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="428fc-111">Aprovisionar un entorno de Project Operations</span><span class="sxs-lookup"><span data-stu-id="428fc-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="428fc-112">Abra un nuevo despliegue de Dynamics 365 Finance de [entorno de demostración](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [entorno de espacio aislado/producción](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="428fc-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="428fc-113">Siga el asistente de **Aprovisionamiento de entornos**.</span><span class="sxs-lookup"><span data-stu-id="428fc-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="428fc-114">Asegúrese de que la versión de la aplicación seleccionada sea 10.0.13 o superior.</span><span class="sxs-lookup"><span data-stu-id="428fc-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="428fc-115">Para aprovisionar Project Operations, en **Configuración avanzada**, seleccione **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="428fc-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="428fc-116">Habilite la **Opción Common Data Service** seleccionando **Sí** y luego introduzca información en los campos obligatorios:</span><span class="sxs-lookup"><span data-stu-id="428fc-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="428fc-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="428fc-117">Name</span></span>
  - <span data-ttu-id="428fc-118">Región</span><span class="sxs-lookup"><span data-stu-id="428fc-118">Region</span></span>
  - <span data-ttu-id="428fc-119">Lenguaje</span><span class="sxs-lookup"><span data-stu-id="428fc-119">Language</span></span>
  - <span data-ttu-id="428fc-120">Divisa</span><span class="sxs-lookup"><span data-stu-id="428fc-120">Currency</span></span>
 
5. <span data-ttu-id="428fc-121">En el campo **Plantilla de Common Data Service**, seleccione **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="428fc-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="428fc-122">Seleccione el tipo de entorno de su implementación.</span><span class="sxs-lookup"><span data-stu-id="428fc-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="428fc-123">Una prueba basada en suscripción le permitirá implementar un entorno CDS durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="428fc-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configuración de implementación](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="428fc-125">Seleccione **Aceptar** para reconocer los términos de servicio y luego seleccione **Listo** para volver a la configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="428fc-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentimiento de implementación](./media/2DeploymentConsent.png)

7. <span data-ttu-id="428fc-127">Opcional: Aplicar datos de demostración al entorno.</span><span class="sxs-lookup"><span data-stu-id="428fc-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="428fc-128">Vaya a **Configuración avanzada**, seleccione **Personalizar configuración de base de datos SQL**, y establezca **Especificar un conjunto de datos para base de datos de aplicación** en **Demostración**.</span><span class="sxs-lookup"><span data-stu-id="428fc-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="428fc-129">Complete los campos obligatorios restantes en el asistente y confirme la implementación.</span><span class="sxs-lookup"><span data-stu-id="428fc-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="428fc-130">El tiempo de aprovisionamiento del entorno varía según el tipo de entorno.</span><span class="sxs-lookup"><span data-stu-id="428fc-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="428fc-131">El aprovisionamiento puede tardar hasta seis horas.</span><span class="sxs-lookup"><span data-stu-id="428fc-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="428fc-132">Una vez que la implementación se completa correctamente, el entorno se mostrará como **Implementado**.</span><span class="sxs-lookup"><span data-stu-id="428fc-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="428fc-133">Para confirmar que el entorno se ha implementado correctamente, seleccione **Iniciar sesión** e inicie sesión en el entorno.</span><span class="sxs-lookup"><span data-stu-id="428fc-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalles del entorno de](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="428fc-135">Aplique actualizaciones al entorno de Finance</span><span class="sxs-lookup"><span data-stu-id="428fc-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="428fc-136">Project Operations requiere un entorno de Finance con versión de la aplicación **10.0.13 (10.0.569.20009)** o superior.</span><span class="sxs-lookup"><span data-stu-id="428fc-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="428fc-137">Es posible que deba aplicar actualizaciones de calidad a su entorno de Finance para recibir esta versión.</span><span class="sxs-lookup"><span data-stu-id="428fc-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="428fc-138">En LCS, en la página **Detalles del entorno**, en la sección **Actualizaciones disponibles**, seleccione **Ver actualización**.</span><span class="sxs-lookup"><span data-stu-id="428fc-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Ver actualizaciones](./media/5ViewUpdates.png)

2. <span data-ttu-id="428fc-140">En la página **Actualizaciones binarias**, seleccione **Guardar paquete.**</span><span class="sxs-lookup"><span data-stu-id="428fc-140">On the **Binary updates** page, select **Save package.**</span></span>

![Guardar paquete](./media/6SavePackage.png)

3. <span data-ttu-id="428fc-142">Haga clic en **Seleccionar todo** y luego en **Guardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="428fc-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar y guardar actualizaciones](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="428fc-144">Introduzca un nombre y una descripción del paquete y luego seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="428fc-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="428fc-145">Dependiendo de la conexión a Internet, este proceso puede llevar algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="428fc-145">Depending on the internet connection, this process might take some time.</span></span>

![Cargar paquete a la biblioteca de activos](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="428fc-147">Una vez guardado el paquete, seleccione **Hecho** y guarde este paquete en la biblioteca de activos de su proyecto LCS.</span><span class="sxs-lookup"><span data-stu-id="428fc-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="428fc-148">Guardar y validar el paquete puede tardar unos 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="428fc-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="428fc-149">Para aplicar la actualización, vaya a la página **Detalles del entorno** en LCS y seleccione **Mantener** > **Aplicar actualizaciones**.</span><span class="sxs-lookup"><span data-stu-id="428fc-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Mantener entornos](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="428fc-151">En la lista de actualizaciones, seleccione el paquete que creó y seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="428fc-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar actualizaciones](./media/10ApplyUpdates.png)

<span data-ttu-id="428fc-153">El mantenimiento del entorno llevará algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="428fc-153">Environment servicing will take some time.</span></span> <span data-ttu-id="428fc-154">Una vez que se haya completado, el entorno volverá a un estado implementado.</span><span class="sxs-lookup"><span data-stu-id="428fc-154">After it is complete, the environment will return to a deployed state.</span></span>

![Entorno implementado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="428fc-156">Establecer una conexión de escritura dual</span><span class="sxs-lookup"><span data-stu-id="428fc-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="428fc-157">En su proyecto LCS, vaya a la página **Detalles del entorno**.</span><span class="sxs-lookup"><span data-stu-id="428fc-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="428fc-158">En **Información de entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="428fc-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="428fc-159">Una vez completado el vínculo, seleccione **Vincular a CDS para aplicaciones** otra vez.</span><span class="sxs-lookup"><span data-stu-id="428fc-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="428fc-160">Se le redirigirá a Escritura dual en Finance.</span><span class="sxs-lookup"><span data-stu-id="428fc-160">You will be redirected to Dual Write in Finance.</span></span>

![Vincular con CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="428fc-162">Seleccione **Aplicar solución** para acceder a las entidades que se asignarán en la integración.</span><span class="sxs-lookup"><span data-stu-id="428fc-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar soluciones](./media/13ApplySolutions.png)

5. <span data-ttu-id="428fc-164">Seleccione ambas soluciones, **Asignación de tablas de doble escritura de Dynamics 365 Finance and Operations** y **Asignación de tablas de doble escritura de Dynamics 365 Project Operations** y luego seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="428fc-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar soluciones](./media/14ConfirmSolutions.png)

<span data-ttu-id="428fc-166">Una vez aplicadas las soluciones, las entidades de escritura dual se aplican al entorno.</span><span class="sxs-lookup"><span data-stu-id="428fc-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicación de soluciones](./media/15ApplyingSolutions.png)

<span data-ttu-id="428fc-168">Una vez aplicadas las entidades, todas las asignaciones disponibles se enumeran en el entorno.</span><span class="sxs-lookup"><span data-stu-id="428fc-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapas de doble escritura](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="428fc-170">Actualizar las entidades de datos después de la actualización</span><span class="sxs-lookup"><span data-stu-id="428fc-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="428fc-171">En Finance, vaya al área de trabajo **Administración de datos**.</span><span class="sxs-lookup"><span data-stu-id="428fc-171">In Finance, go to the **Data management** workspace.</span></span>

![Espacio de trabajo de administración de datos](./media/16DataManagement.png)

2. <span data-ttu-id="428fc-173">Seleccione el icono **Parámetros del marco**.</span><span class="sxs-lookup"><span data-stu-id="428fc-173">Select the **Framework parameters** tile.</span></span>

![Parámetros del marco](./media/17FrameworkParameters.png)

3. <span data-ttu-id="428fc-175">En la página **Configuración de entidad**, seleccione **Refrescar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="428fc-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualizar lista de entidades](./media/18RefreshEntityList.png)

<span data-ttu-id="428fc-177">La actualización tomará aproximadamente 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="428fc-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="428fc-178">Recibirá una alerta cuando termine.</span><span class="sxs-lookup"><span data-stu-id="428fc-178">You will receive an alert when it is complete.</span></span>

![Confirmación de actualización](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="428fc-180">Actualizar la configuración de seguridad de Project Operations en Dataverse</span><span class="sxs-lookup"><span data-stu-id="428fc-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="428fc-181">Vaya a Project Operations en el entorno de Dataverse.</span><span class="sxs-lookup"><span data-stu-id="428fc-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="428fc-182">Vaya a **Configuración** > **Seguridad** > **Roles de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="428fc-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="428fc-183">En la página **Roles de seguridad**, en la lista de roles, seleccione **usuario de aplicación de doble escritura** y, a continuación, seleccione la pestaña **Entidades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="428fc-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="428fc-184">Compruebe que el rol tenga los permisos **Leer** y **Anexar a** para:</span><span class="sxs-lookup"><span data-stu-id="428fc-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="428fc-185">**Tipo de cambio de la divisa**</span><span class="sxs-lookup"><span data-stu-id="428fc-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="428fc-186">**Plan de cuentas**</span><span class="sxs-lookup"><span data-stu-id="428fc-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="428fc-187">**Calendario fiscal**</span><span class="sxs-lookup"><span data-stu-id="428fc-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="428fc-188">**Ledger**</span><span class="sxs-lookup"><span data-stu-id="428fc-188">**Ledger**</span></span>

5. <span data-ttu-id="428fc-189">Una vez que se haya actualizado el rol de seguridad, vaya a **Configuración** > **Seguridad** > **Equipos** y seleccione el equipo predeterminado en la vista de equipo **Propietario de empresa local**.</span><span class="sxs-lookup"><span data-stu-id="428fc-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="428fc-190">Seleccione **Administrar roles** y compruebe que se haya aplicado el privilegio de seguridad **usuario de aplicación de doble escritura** a este equipo.</span><span class="sxs-lookup"><span data-stu-id="428fc-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="428fc-191">Ejecutar asignaciones de escritura doble de Project Operations</span><span class="sxs-lookup"><span data-stu-id="428fc-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="428fc-192">En su proyecto LCS, vaya a la página **Detalles del entorno**.</span><span class="sxs-lookup"><span data-stu-id="428fc-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="428fc-193">En **Información de entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones.**</span><span class="sxs-lookup"><span data-stu-id="428fc-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="428fc-194">Después de seleccionar el vínculo, se le redirigirá a la lista de entidades de las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="428fc-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="428fc-195">Comience las asignaciones como se describe en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="428fc-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="428fc-196">Asegúrese de seguir la secuencia indicada.</span><span class="sxs-lookup"><span data-stu-id="428fc-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="428fc-197">**Asignación de entidad**</span><span class="sxs-lookup"><span data-stu-id="428fc-197">**Entity Map**</span></span> | <span data-ttu-id="428fc-198">**Actualizar entidad**</span><span class="sxs-lookup"><span data-stu-id="428fc-198">**Refresh entity**</span></span> | <span data-ttu-id="428fc-199">**Sincronización inicial**</span><span class="sxs-lookup"><span data-stu-id="428fc-199">**Initial sync**</span></span> | <span data-ttu-id="428fc-200">**Maestro para sincronización inicial**</span><span class="sxs-lookup"><span data-stu-id="428fc-200">**Master for initial sync**</span></span> | <span data-ttu-id="428fc-201">**Ejecutar requisitos previos**</span><span class="sxs-lookup"><span data-stu-id="428fc-201">**Run prerequisites**</span></span> | <span data-ttu-id="428fc-202">**Sincronización inicial de requisitos previos**</span><span class="sxs-lookup"><span data-stu-id="428fc-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="428fc-203">**Roles de recursos del proyecto para todas las empresas (categorías de recursos reservables)**</span><span class="sxs-lookup"><span data-stu-id="428fc-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="428fc-204">No</span><span class="sxs-lookup"><span data-stu-id="428fc-204">No</span></span> | <span data-ttu-id="428fc-205">Sí</span><span class="sxs-lookup"><span data-stu-id="428fc-205">Yes</span></span> | <span data-ttu-id="428fc-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="428fc-206">Common Data Service</span></span> | <span data-ttu-id="428fc-207">No</span><span class="sxs-lookup"><span data-stu-id="428fc-207">No</span></span> | <span data-ttu-id="428fc-208">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-208">N\A</span></span> |
| <span data-ttu-id="428fc-209">**Entidades legales (empresas\_cdm)**</span><span class="sxs-lookup"><span data-stu-id="428fc-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="428fc-210">No</span><span class="sxs-lookup"><span data-stu-id="428fc-210">No</span></span> | <span data-ttu-id="428fc-211">Sí</span><span class="sxs-lookup"><span data-stu-id="428fc-211">Yes</span></span> | <span data-ttu-id="428fc-212">Aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="428fc-212">Finance and Operations apps</span></span> | <span data-ttu-id="428fc-213">No</span><span class="sxs-lookup"><span data-stu-id="428fc-213">No</span></span> | <span data-ttu-id="428fc-214">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-214">N\A</span></span> |
| <span data-ttu-id="428fc-215">**Libro mayor (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="428fc-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="428fc-216">No</span><span class="sxs-lookup"><span data-stu-id="428fc-216">No</span></span> | <span data-ttu-id="428fc-217">Sí</span><span class="sxs-lookup"><span data-stu-id="428fc-217">Yes</span></span> | <span data-ttu-id="428fc-218">Aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="428fc-218">Finance and Operations apps</span></span> | <span data-ttu-id="428fc-219">Sí</span><span class="sxs-lookup"><span data-stu-id="428fc-219">Yes</span></span> | <span data-ttu-id="428fc-220">Si, aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="428fc-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="428fc-221">**Datos reales de integración de Project Operations (datos reales de\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="428fc-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="428fc-222">No</span><span class="sxs-lookup"><span data-stu-id="428fc-222">No</span></span> | <span data-ttu-id="428fc-223">No</span><span class="sxs-lookup"><span data-stu-id="428fc-223">No</span></span> | <span data-ttu-id="428fc-224">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-224">N\A</span></span> | <span data-ttu-id="428fc-225">Sí</span><span class="sxs-lookup"><span data-stu-id="428fc-225">Yes</span></span> | <span data-ttu-id="428fc-226">No</span><span class="sxs-lookup"><span data-stu-id="428fc-226">No</span></span> |
| <span data-ttu-id="428fc-227">**Líneas de contrato de proyecto (detalles de pedidos de ventas)**</span><span class="sxs-lookup"><span data-stu-id="428fc-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="428fc-228">No</span><span class="sxs-lookup"><span data-stu-id="428fc-228">No</span></span> | <span data-ttu-id="428fc-229">No</span><span class="sxs-lookup"><span data-stu-id="428fc-229">No</span></span> | <span data-ttu-id="428fc-230">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-230">N\A</span></span> | <span data-ttu-id="428fc-231">No</span><span class="sxs-lookup"><span data-stu-id="428fc-231">No</span></span> | <span data-ttu-id="428fc-232">No</span><span class="sxs-lookup"><span data-stu-id="428fc-232">No</span></span> |
| <span data-ttu-id="428fc-233">**Entidad de integración para las relaciones de transacciones del proyecto (conexiones de transacción\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="428fc-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="428fc-234">No</span><span class="sxs-lookup"><span data-stu-id="428fc-234">No</span></span> | <span data-ttu-id="428fc-235">No</span><span class="sxs-lookup"><span data-stu-id="428fc-235">No</span></span> | <span data-ttu-id="428fc-236">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-236">N\A</span></span> | <span data-ttu-id="428fc-237">No</span><span class="sxs-lookup"><span data-stu-id="428fc-237">No</span></span> | <span data-ttu-id="428fc-238">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-238">N\A</span></span> |
| <span data-ttu-id="428fc-239">**Hitos de la línea de contrato de integración de Project Operations (programación de valores de líneas de contrato\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="428fc-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="428fc-240">No</span><span class="sxs-lookup"><span data-stu-id="428fc-240">No</span></span> | <span data-ttu-id="428fc-241">No</span><span class="sxs-lookup"><span data-stu-id="428fc-241">No</span></span> | <span data-ttu-id="428fc-242">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-242">N\A</span></span> | <span data-ttu-id="428fc-243">No</span><span class="sxs-lookup"><span data-stu-id="428fc-243">No</span></span> | <span data-ttu-id="428fc-244">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-244">N\A</span></span> |
| <span data-ttu-id="428fc-245">**Entidad de integración de operaciones de proyecto para estimaciones de gastos (líneas de estimaciones\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="428fc-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="428fc-246">No</span><span class="sxs-lookup"><span data-stu-id="428fc-246">No</span></span> | <span data-ttu-id="428fc-247">No</span><span class="sxs-lookup"><span data-stu-id="428fc-247">No</span></span> | <span data-ttu-id="428fc-248">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-248">N\A</span></span> | <span data-ttu-id="428fc-249">No</span><span class="sxs-lookup"><span data-stu-id="428fc-249">No</span></span> | <span data-ttu-id="428fc-250">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-250">N\A</span></span> |
| <span data-ttu-id="428fc-251">**Entidad de exportación de categorías gastos de proyecto de integración de Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="428fc-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="428fc-252">No</span><span class="sxs-lookup"><span data-stu-id="428fc-252">No</span></span> | <span data-ttu-id="428fc-253">No</span><span class="sxs-lookup"><span data-stu-id="428fc-253">No</span></span> | <span data-ttu-id="428fc-254">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-254">N\A</span></span> | <span data-ttu-id="428fc-255">No</span><span class="sxs-lookup"><span data-stu-id="428fc-255">No</span></span> | <span data-ttu-id="428fc-256">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-256">N\A</span></span> |
| <span data-ttu-id="428fc-257">**Entidad de exportación de gastos de proyecto de integración de Project Operations (gastos\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="428fc-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="428fc-258">Sí</span><span class="sxs-lookup"><span data-stu-id="428fc-258">Yes</span></span> | <span data-ttu-id="428fc-259">No</span><span class="sxs-lookup"><span data-stu-id="428fc-259">No</span></span> | <span data-ttu-id="428fc-260">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-260">N\A</span></span> | <span data-ttu-id="428fc-261">No</span><span class="sxs-lookup"><span data-stu-id="428fc-261">No</span></span> | <span data-ttu-id="428fc-262">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-262">N\A</span></span> |
| <span data-ttu-id="428fc-263">**Entidad de integración de operaciones de proyecto para estimaciones de tiempo (asignaciones de recursos\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="428fc-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="428fc-264">Sí</span><span class="sxs-lookup"><span data-stu-id="428fc-264">Yes</span></span> | <span data-ttu-id="428fc-265">No</span><span class="sxs-lookup"><span data-stu-id="428fc-265">No</span></span> | <span data-ttu-id="428fc-266">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-266">N\A</span></span> | <span data-ttu-id="428fc-267">No</span><span class="sxs-lookup"><span data-stu-id="428fc-267">No</span></span> | <span data-ttu-id="428fc-268">N/D</span><span class="sxs-lookup"><span data-stu-id="428fc-268">N\A</span></span> |


4. <span data-ttu-id="428fc-269">Para actualizar la entidad, seleccione el nombre del mapa y luego seleccione **Actualizar entidades**.</span><span class="sxs-lookup"><span data-stu-id="428fc-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Actualizar Mapa](./media/20RefreshMapping.png)

5. <span data-ttu-id="428fc-271">Tras completar la actualización, ejecute el mapa.</span><span class="sxs-lookup"><span data-stu-id="428fc-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="428fc-272">Antes de habilitar el siguiente mapa, verifique que el mapa de la tabla esté en un estado de **Ejecución**.</span><span class="sxs-lookup"><span data-stu-id="428fc-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="428fc-273">La ejecución de mapas con una mayor cantidad de requisitos previos puede llevar algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="428fc-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="428fc-274">Para ejecutar un mapa con requisitos previos, habilite la alternancia **Mostrar mapas de entidades relacionadas**.</span><span class="sxs-lookup"><span data-stu-id="428fc-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="428fc-275">Si la tabla indica que **Sincronización inicial de requisitos previos** tiene el valor **No**, verifique que el indicador **Sincronización inicial** esté en **Desactivado** en todos los mapas de requisitos previos antes de ejecutarlo.</span><span class="sxs-lookup"><span data-stu-id="428fc-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Ejecutar mapa](./media/21RunMap.png)

6. <span data-ttu-id="428fc-277">Valide que todos los mapas relacionados con el proyecto estén en estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="428fc-277">Validate all project related maps are in the running state.</span></span>

![Todos los mapas en ejecución](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="428fc-279">Aplicar datos de configuración en CDS para Project Operations (opcional)</span><span class="sxs-lookup"><span data-stu-id="428fc-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="428fc-280">Si ha aplicado datos de demostración al entorno financiero, consulte [Configurar y aplicar datos de configuración en Common Data Service para Project Operations](resource-apply-pro-setup-config-data.md) para aplicar datos de demostración al entorno CDS.</span><span class="sxs-lookup"><span data-stu-id="428fc-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="428fc-281">Su entorno de Project Operations ya está aprovisionado y configurado.</span><span class="sxs-lookup"><span data-stu-id="428fc-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]