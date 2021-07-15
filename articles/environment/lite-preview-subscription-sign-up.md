---
title: Registrarse para una suscripción de versión preliminar (lite)
description: 'Este tema proporciona información sobre cómo suscribirse y realizar la implementación simplificada de Project Operations: de oferta a facturación proforma.'
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334803"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="aada3-103">Registrarse para una suscripción de versión preliminar (lite)</span><span class="sxs-lookup"><span data-stu-id="aada3-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="aada3-104">Este tema explica cómo suscribirse a la oferta de prueba e implementar la implementación simplificada de Dynamics 365 Project Operations: del acuerdo a la facturación proforma.</span><span class="sxs-lookup"><span data-stu-id="aada3-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="aada3-105">Este proceso cambiará en las próximas versiones de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="aada3-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aada3-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aada3-106">Prerequisites</span></span>
- <span data-ttu-id="aada3-107">El usuario que implementa la vista previa debe tener derechos de administrador global de inquilinos de Azure.</span><span class="sxs-lookup"><span data-stu-id="aada3-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="aada3-108">Puede crear un inquilino durante el primer caje de oferta.</span><span class="sxs-lookup"><span data-stu-id="aada3-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aada3-109">Solo una persona, el inquilino administrador, necesita realizar esta tarea en una organización.</span><span class="sxs-lookup"><span data-stu-id="aada3-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="aada3-110">Si no es el suscriptor de esta versión, espere hasta que su organización se haya registrado y haya recibido sus credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="aada3-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="aada3-111">Las pruebas son de un solo uso en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="aada3-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="aada3-112">Solo puede ejecutar una prueba una vez.</span><span class="sxs-lookup"><span data-stu-id="aada3-112">You can only run a trial one time.</span></span> <span data-ttu-id="aada3-113">Le recomendamos que cree un nuevo inquilino para la prueba.</span><span class="sxs-lookup"><span data-stu-id="aada3-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="aada3-114">Prueba de Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="aada3-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="aada3-115">Antes de comenzar, asegúrese de haber iniciado sesión en un navegador con la cuenta de trabajo del usuario en el inquilino donde desea la vista previa de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="aada3-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="aada3-116">Vaya a [Prueba de Project Operations](https://aka.ms/try-po) para canjear el primer código de oferta, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="aada3-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="aada3-117">Confirme su pedido.</span><span class="sxs-lookup"><span data-stu-id="aada3-117">Confirm your order.</span></span>

  <span data-ttu-id="aada3-118">Verá que la oferta de confirmación se canjeó correctamente.</span><span class="sxs-lookup"><span data-stu-id="aada3-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="aada3-119">Asignación de licencias</span><span class="sxs-lookup"><span data-stu-id="aada3-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aada3-120">Necesitará acceso administrativo al Portal de Microsoft 365 de la organización para completar los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="aada3-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="aada3-121">Vaya al [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar las licencias a sus usuarios.</span><span class="sxs-lookup"><span data-stu-id="aada3-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="aada3-122">En la página **Usuarios activos**, seleccione los usuarios a los que desea asignar una licencia.</span><span class="sxs-lookup"><span data-stu-id="aada3-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="aada3-123">Verifique que la licencia de **Dynamics 365 Project Operations** está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="aada3-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="aada3-124">Seleccione **Guardar cambios**.</span><span class="sxs-lookup"><span data-stu-id="aada3-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="aada3-125">Crear un nuevo entorno de Dataverse</span><span class="sxs-lookup"><span data-stu-id="aada3-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="aada3-126">Aprovisione un nuevo entorno de implementación de Dataverse de Project Operations siguiendo las instrucciones del tema [Modelo de implementación Dataverse](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="aada3-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="aada3-127">Cuando seleccione el tipo de entorno, asegúrese de utilizar **Prueba (basada en suscripción)**.</span><span class="sxs-lookup"><span data-stu-id="aada3-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Nuevo entorno](./media/19CreateEnvironment.png)

2. <span data-ttu-id="aada3-129">Seleccione la opción **Habilitar aplicaciones de Dynamics 365** y deje **Implementar automáticamente estas aplicaciones** en blanco.</span><span class="sxs-lookup"><span data-stu-id="aada3-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="aada3-130">Seleccione **Guardar** para crear el entorno.</span><span class="sxs-lookup"><span data-stu-id="aada3-130">Select **Save** to create the environment.</span></span>

  ![Agregar base de datos](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="aada3-132">Una vez creado el entorno, instale la solución **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="aada3-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instalación de la solución](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="aada3-134">Instalar una configuración CDS y datos de demostración de configuración</span><span class="sxs-lookup"><span data-stu-id="aada3-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="aada3-135">Instale la configuración CDS y configure los datos de demostración siguiendo las instrucciones del tema [Aplicar datos de configuración y configuración de demostración](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="aada3-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
