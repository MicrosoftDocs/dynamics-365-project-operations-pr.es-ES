---
title: Implementar Project Operations (lite)
description: 'Este tema proporciona información sobre cómo instalar la implementación simplificada de Project Operations: de oferta a facturación proforma.'
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995552"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="40e47-103">Implementar Project Operations (lite)</span><span class="sxs-lookup"><span data-stu-id="40e47-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="40e47-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="40e47-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="40e47-105">Project Operations admite varios modelos de implementación.</span><span class="sxs-lookup"><span data-stu-id="40e47-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="40e47-106">Para determinar el mejor modelo de implementación, consulte [Tipos de implementación](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="40e47-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="40e47-107">Esta implementación, la implementación simplificada: de oferta a facturación proforma, produce una **implementación solo de Common Data Service de Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="40e47-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="40e47-108">Instalar Project Operations en un nuevo entorno CDS</span><span class="sxs-lookup"><span data-stu-id="40e47-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="40e47-109">Instalar en un entorno CDS existente</span><span class="sxs-lookup"><span data-stu-id="40e47-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="40e47-110">Instalar Project Operations en un nuevo entorno CDS</span><span class="sxs-lookup"><span data-stu-id="40e47-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="40e47-111">Como [Administrador global o de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, cree un nuevo entorno CDS en el [Centro de administración de PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="40e47-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="40e47-112">Asegúrese de que **Base de datos CDS** y **Aplicaciones de Dynamics 365** están habilitados.</span><span class="sxs-lookup"><span data-stu-id="40e47-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="40e47-113">Para obtener más información, consulte [Crear y administrar entornos en el centro de administración de Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="40e47-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="40e47-114">Seleccione **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="40e47-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="40e47-115">Instalar Project Operations en un entorno CDS existente</span><span class="sxs-lookup"><span data-stu-id="40e47-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="40e47-116">Como [Administrador global o de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, ubique el entorno en el [centro de administración de PowerPlatform](https://admin.powerplatform.com) donde desea instalar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="40e47-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="40e47-117">Instale **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="40e47-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="40e47-118">Para obtener más información, consulte [Administrar aplicaciones de Dynamics 365](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="40e47-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]