---
title: Implementar Project Operations (lite)
description: 'Este tema proporciona información sobre cómo instalar la implementación simplificada de Project Operations: de oferta a facturación proforma.'
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0af8067fc0673890a317ac6f4e62d74b7f4eebca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290110"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="66084-103">Implementar Project Operations (lite)</span><span class="sxs-lookup"><span data-stu-id="66084-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="66084-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="66084-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="66084-105">Project Operations admite varios modelos de implementación.</span><span class="sxs-lookup"><span data-stu-id="66084-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="66084-106">Para determinar el mejor modelo de implementación, consulte [Tipos de implementación](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="66084-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="66084-107">Esta implementación, la implementación simplificada: de oferta a facturación proforma, produce una **implementación solo de Common Data Service de Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="66084-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="66084-108">Instalar Project Operations en un nuevo entorno CDS</span><span class="sxs-lookup"><span data-stu-id="66084-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="66084-109">Instalar en un entorno CDS existente</span><span class="sxs-lookup"><span data-stu-id="66084-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="66084-110">Instalar Project Operations en un nuevo entorno CDS</span><span class="sxs-lookup"><span data-stu-id="66084-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="66084-111">Como [Administrador global o de Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, cree un nuevo entorno CDS en el [Centro de administración de PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="66084-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="66084-112">Asegúrese de que **Base de datos CDS** y **Aplicaciones de Dynamics 365** están habilitados.</span><span class="sxs-lookup"><span data-stu-id="66084-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="66084-113">Para obtener más información, consulte [Crear y administrar entornos en el centro de administración de Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="66084-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="66084-114">Seleccione **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="66084-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="66084-115">Instalar Project Operations en un entorno CDS existente</span><span class="sxs-lookup"><span data-stu-id="66084-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="66084-116">Como [Administrador global o de Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, ubique el entorno en el [centro de administración de PowerPlatform](https://admin.powerplatform.com) donde desea instalar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="66084-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="66084-117">Instale **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="66084-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="66084-118">Para obtener más información, consulte [Administrar aplicaciones de Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="66084-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]