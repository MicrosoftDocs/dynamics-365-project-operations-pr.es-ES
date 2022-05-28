---
title: Implementar Project Operations (lite)
description: 'Este tema proporciona información sobre cómo instalar la implementación simplificada de Project Operations: de oferta a facturación proforma.'
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580753"
---
# <a name="deploy-project-operations---lite"></a>Implementar Project Operations (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_



Project Operations admite varios modelos de implementación. Para determinar el mejor modelo de implementación, consulte [Tipos de implementación](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implementación, la implementación simplificada: de oferta a facturación proforma, produce una **implementación solo de Dataverse de Project Operations**.

- [Instalar Project Operations en un nuevo entorno de Dataverse](#new)
- [Instalar en un entorno de Dataverse existente](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Instalar Project Operations en un nuevo entorno de Dataverse

1. Como [Administrador global o de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, cree un nuevo entorno de Dataverse en el [Centro de administración de PowerPlatform](https://admin.powerplatform.com). Asegúrate de que **Crear una base de datos para este entorno** y **Aplicaciones de Dynamics 365** están habilitados. Para obtener más información, consulte [Crear y administrar entornos en el centro de administración de Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Seleccione **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalar Project Operations en un entorno de Dataverse existente
1. Asegúrese de que el entorno no se haya configurado con [doble escritura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), ya que la instalación luego instalará las capacidades de [Project Operations para escenarios basados en recursos/no en existencias](project-operations-integrated-deployment-overview.md).
2. Como [Administrador global o de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, ubique el entorno en el [centro de administración de PowerPlatform](https://admin.powerplatform.com) donde desea instalar Project Operations.
3. Instale **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365. Para obtener más información, consulte [Administrar aplicaciones de Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
