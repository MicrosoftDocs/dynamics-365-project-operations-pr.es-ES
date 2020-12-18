---
title: Aprovisionar un entorno nuevo
description: Este tema proporciona información sobre cómo aprovisionar un nuevo entorno de Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643013"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="f772b-103">Aprovisionar un entorno nuevo</span><span class="sxs-lookup"><span data-stu-id="f772b-103">Provision a new environment</span></span>

<span data-ttu-id="f772b-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="f772b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f772b-105">Este tema proporciona información sobre cómo aprovisionar un nuevo entorno de Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.</span><span class="sxs-lookup"><span data-stu-id="f772b-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="f772b-106">Habilitear el aprovisionamiento automatizado de Project Operations en un proyecto LCS</span><span class="sxs-lookup"><span data-stu-id="f772b-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="f772b-107">Utilice los siguientes pasos para habilitar el flujo de aprovisionamiento automatizado de Project Operations para su proyecto LCS.</span><span class="sxs-lookup"><span data-stu-id="f772b-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="f772b-108">Vaya a [LCS](https://lcs.dynamics.com/v2) y seleccione el icono **Gestión de funciones de vista previa**.</span><span class="sxs-lookup"><span data-stu-id="f772b-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="f772b-109">En la lista **Característica de vista previa**, seleccione **Característica de Project Operations** y después seleccione **Función de vista previa habilitada** para habilitar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f772b-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f772b-110">Este paso se realiza solo una vez por proyecto LCS.</span><span class="sxs-lookup"><span data-stu-id="f772b-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="f772b-111">Aprovisionar un entorno de Project Operations</span><span class="sxs-lookup"><span data-stu-id="f772b-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="f772b-112">Abra un nuevo despliegue de Dynamics 365 Finance de [entorno de demostración](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [entorno de espacio aislado/producción](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="f772b-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="f772b-113">Siga el asistente de **Aprovisionamiento de entornos**.</span><span class="sxs-lookup"><span data-stu-id="f772b-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="f772b-114">Asegúrese de que la versión de la aplicación seleccionada sea 10.0.13 o superior.</span><span class="sxs-lookup"><span data-stu-id="f772b-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="f772b-115">Para aprovisionar Project Operations, en **Configuración avanzada**, seleccione **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="f772b-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="f772b-116">Habilite la **Opción Common Data Service** seleccionando **Sí** y luego introduzca información en los campos obligatorios:</span><span class="sxs-lookup"><span data-stu-id="f772b-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="f772b-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="f772b-117">Name</span></span>
  - <span data-ttu-id="f772b-118">Región</span><span class="sxs-lookup"><span data-stu-id="f772b-118">Region</span></span>
  - <span data-ttu-id="f772b-119">Lenguaje</span><span class="sxs-lookup"><span data-stu-id="f772b-119">Language</span></span>
  - <span data-ttu-id="f772b-120">Divisa</span><span class="sxs-lookup"><span data-stu-id="f772b-120">Currency</span></span>
 
5. <span data-ttu-id="f772b-121">En el campo **Plantilla de Common Data Service**, seleccione **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="f772b-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="f772b-122">Seleccione el tipo de entorno de su implementación.</span><span class="sxs-lookup"><span data-stu-id="f772b-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="f772b-123">Una prueba basada en suscripción le permitirá implementar un entorno CDS durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="f772b-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configuración de implementación](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="f772b-125">Seleccione **Aceptar** para reconocer los términos de servicio y luego seleccione **Listo** para volver a la configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="f772b-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentimiento de implementación](./media/2DeploymentConsent.png)

7. <span data-ttu-id="f772b-127">Complete los campos obligatorios restantes en el asistente y confirme la implementación.</span><span class="sxs-lookup"><span data-stu-id="f772b-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="f772b-128">El tiempo de aprovisionamiento del entorno varía según el tipo de entorno.</span><span class="sxs-lookup"><span data-stu-id="f772b-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="f772b-129">El aprovisionamiento puede tardar hasta seis horas.</span><span class="sxs-lookup"><span data-stu-id="f772b-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="f772b-130">Una vez que la implementación se completa correctamente, el entorno se mostrará como **Implementado**.</span><span class="sxs-lookup"><span data-stu-id="f772b-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="f772b-131">Para confirmar que el entorno se ha implementado correctamente, seleccione **Iniciar sesión** e inicie sesión en el entorno para confirmar.</span><span class="sxs-lookup"><span data-stu-id="f772b-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalles del entorno de](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="f772b-133">Aplicar datos de demostración de Project Operations Finance (paso opcional)</span><span class="sxs-lookup"><span data-stu-id="f772b-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="f772b-134">Aplique los datos de demostración de Project Operations Finance al entorno alojado en la nube de la versión de servicio 10.0.13, como se describe en [este artículo](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="f772b-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="f772b-135">Aplique actualizaciones al entorno de Finance</span><span class="sxs-lookup"><span data-stu-id="f772b-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="f772b-136">Project Operations requiere un entorno de Finance con versión de la aplicación **10.0.13 (10.0.569.20009)** o superior.</span><span class="sxs-lookup"><span data-stu-id="f772b-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="f772b-137">Es posible que deba aplicar actualizaciones de calidad a su entorno de Finance para recibir esta versión.</span><span class="sxs-lookup"><span data-stu-id="f772b-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="f772b-138">En LCS, en la página **Detalles del entorno**, en la sección **Actualizaciones disponibles**, seleccione **Ver actualización**.</span><span class="sxs-lookup"><span data-stu-id="f772b-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Ver actualizaciones](./media/5ViewUpdates.png)

2. <span data-ttu-id="f772b-140">En la página **Actualizaciones binarias**, seleccione **Guardar paquete.**</span><span class="sxs-lookup"><span data-stu-id="f772b-140">On the **Binary updates** page, select **Save package.**</span></span>

![Guardar paquete](./media/6SavePackage.png)

3. <span data-ttu-id="f772b-142">Haga clic en **Seleccionar todo** y luego en **Guardar paquete**.</span><span class="sxs-lookup"><span data-stu-id="f772b-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar y guardar actualizaciones](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="f772b-144">Introduzca un nombre y una descripción del paquete y luego seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f772b-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="f772b-145">Dependiendo de la conexión a Internet, este proceso puede llevar algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="f772b-145">Depending on the internet connection, this process might take some time.</span></span>

![Cargar paquete a la biblioteca de activos](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="f772b-147">Una vez guardado el paquete, seleccione **Hecho** y guarde este paquete en la biblioteca de activos de su proyecto LCS.</span><span class="sxs-lookup"><span data-stu-id="f772b-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="f772b-148">Guardar y validar el paquete puede tardar unos 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="f772b-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="f772b-149">Para aplicar la actualización, vaya a la página **Detalles del entorno** en LCS y seleccione **Mantener** > **Aplicar actualizaciones**.</span><span class="sxs-lookup"><span data-stu-id="f772b-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Mantener entornos](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="f772b-151">En la lista de actualizaciones, seleccione el paquete que creó y seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="f772b-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar actualizaciones](./media/10ApplyUpdates.png)

<span data-ttu-id="f772b-153">El mantenimiento del entorno llevará algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="f772b-153">Environment servicing will take some time.</span></span> <span data-ttu-id="f772b-154">Una vez que se haya completado, el entorno volverá a un estado implementado.</span><span class="sxs-lookup"><span data-stu-id="f772b-154">After it is complete, the environment will return to a deployed state.</span></span>

![Entorno implementado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="f772b-156">Establecer una conexión de escritura dual</span><span class="sxs-lookup"><span data-stu-id="f772b-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="f772b-157">En su proyecto LCS, vaya a la página **Detalles del entorno**.</span><span class="sxs-lookup"><span data-stu-id="f772b-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="f772b-158">En **Información de entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="f772b-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="f772b-159">Una vez completado el vínculo, seleccione **Vincular a CDS para aplicaciones** otra vez.</span><span class="sxs-lookup"><span data-stu-id="f772b-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="f772b-160">Se le redirigirá a Escritura dual en Finance.</span><span class="sxs-lookup"><span data-stu-id="f772b-160">You will be redirected to Dual Write in Finance.</span></span>

![Vincular con CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="f772b-162">Seleccione **Aplicar solución** para acceder a las entidades que se asignarán en la integración.</span><span class="sxs-lookup"><span data-stu-id="f772b-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar soluciones](./media/13ApplySolutions.png)

5. <span data-ttu-id="f772b-164">Seleccione ambas soluciones, **Asignación de tablas de doble escritura de Dynamics 365 Finance and Operations** y **Asignación de tablas de doble escritura de Dynamics 365 Project Operations** y luego seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="f772b-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar soluciones](./media/14ConfirmSolutions.png)

<span data-ttu-id="f772b-166">Una vez aplicadas las soluciones, las entidades de escritura dual se aplican al entorno.</span><span class="sxs-lookup"><span data-stu-id="f772b-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicación de soluciones](./media/15ApplyingSolutions.png)

<span data-ttu-id="f772b-168">Una vez aplicadas las entidades, todas las asignaciones disponibles se enumeran en el entorno.</span><span class="sxs-lookup"><span data-stu-id="f772b-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapas de doble escritura](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="f772b-170">Actualizar las entidades de datos después de la actualización</span><span class="sxs-lookup"><span data-stu-id="f772b-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="f772b-171">En Finance, vaya al área de trabajo **Administración de datos**.</span><span class="sxs-lookup"><span data-stu-id="f772b-171">In Finance, go to the **Data management** workspace.</span></span>

![Espacio de trabajo de administración de datos](./media/16DataManagement.png)

2. <span data-ttu-id="f772b-173">Seleccione el icono **Parámetros del marco**.</span><span class="sxs-lookup"><span data-stu-id="f772b-173">Select the **Framework parameters** tile.</span></span>

![Parámetros del marco](./media/17FrameworkParameters.png)

3. <span data-ttu-id="f772b-175">En la página **Configuración de entidad**, seleccione **Refrescar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="f772b-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualizar lista de entidades](./media/18RefreshEntityList.png)

<span data-ttu-id="f772b-177">La actualización tomará aproximadamente 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="f772b-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="f772b-178">Recibirá una alerta cuando termine.</span><span class="sxs-lookup"><span data-stu-id="f772b-178">You will receive an alert when it is complete.</span></span>

![Confirmación de actualización](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="f772b-180">Ejecutar asignaciones de escritura doble de Project Operations</span><span class="sxs-lookup"><span data-stu-id="f772b-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="f772b-181">En su proyecto LCS, vaya a la página **Detalles del entorno**.</span><span class="sxs-lookup"><span data-stu-id="f772b-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="f772b-182">En **Información de entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones.**</span><span class="sxs-lookup"><span data-stu-id="f772b-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="f772b-183">Después de seleccionar el vínculo, se le redirigirá a la lista de entidades de las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="f772b-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="f772b-184">Comience las asignaciones como se describe en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f772b-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="f772b-185">Asegúrese de seguir la secuencia indicada.</span><span class="sxs-lookup"><span data-stu-id="f772b-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="f772b-186">**Asignación de entidad**</span><span class="sxs-lookup"><span data-stu-id="f772b-186">**Entity Map**</span></span> | <span data-ttu-id="f772b-187">**Actualizar entidad**</span><span class="sxs-lookup"><span data-stu-id="f772b-187">**Refresh entity**</span></span> | <span data-ttu-id="f772b-188">**Sincronización inicial**</span><span class="sxs-lookup"><span data-stu-id="f772b-188">**Initial sync**</span></span> | <span data-ttu-id="f772b-189">**Maestro para sincronización inicial**</span><span class="sxs-lookup"><span data-stu-id="f772b-189">**Master for initial sync**</span></span> | <span data-ttu-id="f772b-190">**Ejecutar requisitos previos**</span><span class="sxs-lookup"><span data-stu-id="f772b-190">**Run prerequisites**</span></span> | <span data-ttu-id="f772b-191">**Sincronización inicial de requisitos previos**</span><span class="sxs-lookup"><span data-stu-id="f772b-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="f772b-192">**Roles de recursos del proyecto para todas las empresas (categorías de recursos reservables)**</span><span class="sxs-lookup"><span data-stu-id="f772b-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="f772b-193">No</span><span class="sxs-lookup"><span data-stu-id="f772b-193">No</span></span> | <span data-ttu-id="f772b-194">Sí</span><span class="sxs-lookup"><span data-stu-id="f772b-194">Yes</span></span> | <span data-ttu-id="f772b-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f772b-195">Common Data Service</span></span> | <span data-ttu-id="f772b-196">No</span><span class="sxs-lookup"><span data-stu-id="f772b-196">No</span></span> | <span data-ttu-id="f772b-197">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-197">N\A</span></span> |
| <span data-ttu-id="f772b-198">**Entidades legales (empresas\_cdm)**</span><span class="sxs-lookup"><span data-stu-id="f772b-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="f772b-199">No</span><span class="sxs-lookup"><span data-stu-id="f772b-199">No</span></span> | <span data-ttu-id="f772b-200">Sí</span><span class="sxs-lookup"><span data-stu-id="f772b-200">Yes</span></span> | <span data-ttu-id="f772b-201">Aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f772b-201">Finance and Operations apps</span></span> | <span data-ttu-id="f772b-202">No</span><span class="sxs-lookup"><span data-stu-id="f772b-202">No</span></span> | <span data-ttu-id="f772b-203">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-203">N\A</span></span> |
| <span data-ttu-id="f772b-204">**Libro mayor (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="f772b-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="f772b-205">No</span><span class="sxs-lookup"><span data-stu-id="f772b-205">No</span></span> | <span data-ttu-id="f772b-206">Sí</span><span class="sxs-lookup"><span data-stu-id="f772b-206">Yes</span></span> | <span data-ttu-id="f772b-207">Aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f772b-207">Finance and Operations apps</span></span> | <span data-ttu-id="f772b-208">Sí</span><span class="sxs-lookup"><span data-stu-id="f772b-208">Yes</span></span> | <span data-ttu-id="f772b-209">Si, aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f772b-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="f772b-210">**Datos reales de integración de Project Operations (datos reales de\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="f772b-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="f772b-211">No</span><span class="sxs-lookup"><span data-stu-id="f772b-211">No</span></span> | <span data-ttu-id="f772b-212">No</span><span class="sxs-lookup"><span data-stu-id="f772b-212">No</span></span> | <span data-ttu-id="f772b-213">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-213">N\A</span></span> | <span data-ttu-id="f772b-214">Sí</span><span class="sxs-lookup"><span data-stu-id="f772b-214">Yes</span></span> | <span data-ttu-id="f772b-215">No</span><span class="sxs-lookup"><span data-stu-id="f772b-215">No</span></span> |
| <span data-ttu-id="f772b-216">**Líneas de contrato de proyecto (detalles de pedidos de ventas)**</span><span class="sxs-lookup"><span data-stu-id="f772b-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="f772b-217">No</span><span class="sxs-lookup"><span data-stu-id="f772b-217">No</span></span> | <span data-ttu-id="f772b-218">No</span><span class="sxs-lookup"><span data-stu-id="f772b-218">No</span></span> | <span data-ttu-id="f772b-219">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-219">N\A</span></span> | <span data-ttu-id="f772b-220">No</span><span class="sxs-lookup"><span data-stu-id="f772b-220">No</span></span> | <span data-ttu-id="f772b-221">No</span><span class="sxs-lookup"><span data-stu-id="f772b-221">No</span></span> |
| <span data-ttu-id="f772b-222">**Entidad de integración para las relaciones de transacciones del proyecto (conexiones de transacción\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="f772b-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="f772b-223">No</span><span class="sxs-lookup"><span data-stu-id="f772b-223">No</span></span> | <span data-ttu-id="f772b-224">No</span><span class="sxs-lookup"><span data-stu-id="f772b-224">No</span></span> | <span data-ttu-id="f772b-225">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-225">N\A</span></span> | <span data-ttu-id="f772b-226">No</span><span class="sxs-lookup"><span data-stu-id="f772b-226">No</span></span> | <span data-ttu-id="f772b-227">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-227">N\A</span></span> |
| <span data-ttu-id="f772b-228">**Hitos de la línea de contrato de integración de Project Operations (programación de valores de líneas de contrato\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="f772b-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="f772b-229">No</span><span class="sxs-lookup"><span data-stu-id="f772b-229">No</span></span> | <span data-ttu-id="f772b-230">No</span><span class="sxs-lookup"><span data-stu-id="f772b-230">No</span></span> | <span data-ttu-id="f772b-231">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-231">N\A</span></span> | <span data-ttu-id="f772b-232">No</span><span class="sxs-lookup"><span data-stu-id="f772b-232">No</span></span> | <span data-ttu-id="f772b-233">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-233">N\A</span></span> |
| <span data-ttu-id="f772b-234">**Entidad de integración de operaciones de proyecto para estimaciones de gastos (líneas de estimaciones\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="f772b-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="f772b-235">No</span><span class="sxs-lookup"><span data-stu-id="f772b-235">No</span></span> | <span data-ttu-id="f772b-236">No</span><span class="sxs-lookup"><span data-stu-id="f772b-236">No</span></span> | <span data-ttu-id="f772b-237">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-237">N\A</span></span> | <span data-ttu-id="f772b-238">No</span><span class="sxs-lookup"><span data-stu-id="f772b-238">No</span></span> | <span data-ttu-id="f772b-239">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-239">N\A</span></span> |
| <span data-ttu-id="f772b-240">**Entidad de exportación de categorías gastos de proyecto de integración de Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="f772b-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="f772b-241">No</span><span class="sxs-lookup"><span data-stu-id="f772b-241">No</span></span> | <span data-ttu-id="f772b-242">No</span><span class="sxs-lookup"><span data-stu-id="f772b-242">No</span></span> | <span data-ttu-id="f772b-243">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-243">N\A</span></span> | <span data-ttu-id="f772b-244">No</span><span class="sxs-lookup"><span data-stu-id="f772b-244">No</span></span> | <span data-ttu-id="f772b-245">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-245">N\A</span></span> |
| <span data-ttu-id="f772b-246">**Entidad de exportación de gastos de proyecto de integración de Project Operations (gastos\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="f772b-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="f772b-247">Sí</span><span class="sxs-lookup"><span data-stu-id="f772b-247">Yes</span></span> | <span data-ttu-id="f772b-248">No</span><span class="sxs-lookup"><span data-stu-id="f772b-248">No</span></span> | <span data-ttu-id="f772b-249">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-249">N\A</span></span> | <span data-ttu-id="f772b-250">No</span><span class="sxs-lookup"><span data-stu-id="f772b-250">No</span></span> | <span data-ttu-id="f772b-251">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-251">N\A</span></span> |
| <span data-ttu-id="f772b-252">**Entidad de integración de operaciones de proyecto para estimaciones de tiempo (asignaciones de recursos\_msdyn)**</span><span class="sxs-lookup"><span data-stu-id="f772b-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="f772b-253">Sí</span><span class="sxs-lookup"><span data-stu-id="f772b-253">Yes</span></span> | <span data-ttu-id="f772b-254">No</span><span class="sxs-lookup"><span data-stu-id="f772b-254">No</span></span> | <span data-ttu-id="f772b-255">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-255">N\A</span></span> | <span data-ttu-id="f772b-256">No</span><span class="sxs-lookup"><span data-stu-id="f772b-256">No</span></span> | <span data-ttu-id="f772b-257">N/D</span><span class="sxs-lookup"><span data-stu-id="f772b-257">N\A</span></span> |


4. <span data-ttu-id="f772b-258">Para actualizar la entidad, seleccione el nombre del mapa y luego seleccione **Actualizar entidades**.</span><span class="sxs-lookup"><span data-stu-id="f772b-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Actualizar Mapa](./media/20RefreshMapping.png)

5. <span data-ttu-id="f772b-260">Tras completar la actualización, ejecute el mapa.</span><span class="sxs-lookup"><span data-stu-id="f772b-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="f772b-261">Antes de habilitar el siguiente mapa, verifique que el mapa de la tabla esté en un estado de **Ejecución**.</span><span class="sxs-lookup"><span data-stu-id="f772b-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="f772b-262">La ejecución de mapas con una mayor cantidad de requisitos previos puede llevar algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="f772b-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="f772b-263">Para ejecutar un mapa con requisitos previos, habilite la alternancia **Mostrar mapas de entidades relacionadas**.</span><span class="sxs-lookup"><span data-stu-id="f772b-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="f772b-264">Si la tabla indica que **Sincronización inicial de requisitos previos** tiene el valor **No**, verifique que el indicador **Sincronización inicial** esté en **Desactivado** en todos los mapas de requisitos previos antes de ejecutarlo.</span><span class="sxs-lookup"><span data-stu-id="f772b-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Ejecutar mapa](./media/21RunMap.png)

6. <span data-ttu-id="f772b-266">Valide que todos los mapas relacionados con el proyecto estén en estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f772b-266">Validate all project related maps are in the running state.</span></span>

![Todos los mapas en ejecución](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="f772b-268">Aplicar datos de configuración en CDS para Project Operations (opcional)</span><span class="sxs-lookup"><span data-stu-id="f772b-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="f772b-269">Si ha aplicado datos de demostración al entorno financiero, consulte [Configurar y aplicar datos de configuración en Common Data Service para Project Operations](resource-apply-pro-setup-config-data.md) para aplicar datos de demostración al entorno CDS.</span><span class="sxs-lookup"><span data-stu-id="f772b-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="f772b-270">Su entorno de Project Operations ya está aprovisionado y configurado.</span><span class="sxs-lookup"><span data-stu-id="f772b-270">Your Project Operations environment is now provisioned and configured.</span></span> 
