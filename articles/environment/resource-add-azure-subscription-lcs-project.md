---
title: Agregar una suscripción de Azure al proyecto de LCS
description: Este tema proporciona información sobre cómo conectar su suscripción de Azure a un proyecto LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085019"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a><span data-ttu-id="2b500-103">Agregar una suscripción de Azure al proyecto de LCS</span><span class="sxs-lookup"><span data-stu-id="2b500-103">Add an Azure subscription to LCS project</span></span>

<span data-ttu-id="2b500-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="2b500-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2b500-105">Los entornos alojados en la nube deben implementarse mediante una suscripción de Azure existente.</span><span class="sxs-lookup"><span data-stu-id="2b500-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="2b500-106">Este tema explica cómo conectar su suscripción exisente de Azure a un proyecto LCS.</span><span class="sxs-lookup"><span data-stu-id="2b500-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="2b500-107">Conceder consentimiento del administrador</span><span class="sxs-lookup"><span data-stu-id="2b500-107">Grant admin consent</span></span>

1. <span data-ttu-id="2b500-108">En su proyecto LCS, en la sección **Ambientes** , seleccione **Configuración de Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="2b500-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Configuración de Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="2b500-110">En la página **Configuración del proyecto** , en la pestaña **Conectores de Azure** , seleccione **Autorizar**.</span><span class="sxs-lookup"><span data-stu-id="2b500-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="2b500-111">Esto permite implementar entornos en este proyecto.</span><span class="sxs-lookup"><span data-stu-id="2b500-111">This allows environments to be deployed to this project.</span></span>

![Conectores de Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="2b500-113">Seleccione **Autorizar** nuevamente para conceder el consentimiento del administrador.</span><span class="sxs-lookup"><span data-stu-id="2b500-113">Select **Authorize** again to provide admin consent.</span></span>

![Conceder consentimiento del administrador](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="2b500-115">Acepta la solicitud de permisos.</span><span class="sxs-lookup"><span data-stu-id="2b500-115">Accept the permissions request.</span></span>

![Aceptar solicitud de permiso](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="2b500-117">La autorización ya está completa.</span><span class="sxs-lookup"><span data-stu-id="2b500-117">The authorization is now complete.</span></span> 

![Autorización corrrecta](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="2b500-119">Proporcionar acceso a Dynamics Deployment Services a su suscripción de Azure</span><span class="sxs-lookup"><span data-stu-id="2b500-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="2b500-120">Vaya a [Facturación de Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) y seleccione su suscripción.</span><span class="sxs-lookup"><span data-stu-id="2b500-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="2b500-121">Dynamics Deployment Services necesita acceder a esta suscripción para poder implementar entornos.</span><span class="sxs-lookup"><span data-stu-id="2b500-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Detalles de suscripción a Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="2b500-123">Seleccione **Control de acceso (IAM)** en el panel de navegación y luego seleccione **Agregar asignación de roles**.</span><span class="sxs-lookup"><span data-stu-id="2b500-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="2b500-124">En el control deslizante del lado derecho, seleccione **Rol de colaborador** y, en la lista provista, busque y seleccione **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="2b500-124">In the slider on the right side, select **Contributor role** , and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="2b500-125">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="2b500-125">Select **Save**.</span></span>

![Acceso a suscripción](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="2b500-127">Agregar un conector de suscripcióna un proyecto LCS</span><span class="sxs-lookup"><span data-stu-id="2b500-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="2b500-128">En su proyecto LCS, en la página **Configuración de Microsoft Azure** , seleccione **Añadir** para agregar un nuevo conector.</span><span class="sxs-lookup"><span data-stu-id="2b500-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="2b500-129">Escriba su Id. de suscripción de Azure.</span><span class="sxs-lookup"><span data-stu-id="2b500-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="2b500-130">Puede encontrar su Id. de suscripción de Azure en el [Portal de Azure](https://ms.portal.azure.com/), en **Configuración** , en la parte inferior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2b500-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="2b500-131">En el campo **Configurar para usar Azure Resource Manager** , seleccione **Sí**.</span><span class="sxs-lookup"><span data-stu-id="2b500-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="2b500-132">Asegúrese de que el dominio de inquilino AAD de suscripción de Azure coincida con la suscripción de Azure propietaria del dominio que está usando y seleccione **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="2b500-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="2b500-133">En la pantalla **Configuración de Microsoft Azure** , seleccione **Siguiente** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="2b500-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="2b500-134">Si recibe un error en esta pantalla, regrese a la sección [Proporcionar acceso a Dynamics Deployment Services a la suscripción de Azure](#provide) de este tema y asegúrese de haber completado todos los pasos.</span><span class="sxs-lookup"><span data-stu-id="2b500-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="2b500-135">Descargue el Certificado de administración de Azure en una carpeta local de su equipo y luego cárguelo en el Portal de administración de Azure yendo a **Configuración** > **Certificados de administración**.</span><span class="sxs-lookup"><span data-stu-id="2b500-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="2b500-136">Este certificado permitirá a LCS comunicarse con Azure en su nombre.</span><span class="sxs-lookup"><span data-stu-id="2b500-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="2b500-137">Puede omitir este paso si su usuario tiene acceso a la suscripción.</span><span class="sxs-lookup"><span data-stu-id="2b500-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="2b500-138">Seleccione **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="2b500-138">Select  **Next**.</span></span>
8. <span data-ttu-id="2b500-139">Seleccione la región de Azure para implementar y seleccione un centro de datos que esté cerca de dónde planea usar este sistema.</span><span class="sxs-lookup"><span data-stu-id="2b500-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="2b500-140">Seleccione **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="2b500-140">Select  **Connect**.</span></span>

<span data-ttu-id="2b500-141">Ha conectado correctamente su suscripción de Azure.</span><span class="sxs-lookup"><span data-stu-id="2b500-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="2b500-142">Ahora puede implementar entornos alojados en la nube de Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2b500-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


