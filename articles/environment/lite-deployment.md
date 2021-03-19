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
# <a name="deploy-project-operations---lite"></a>Implementar Project Operations (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations admite varios modelos de implementación. Para determinar el mejor modelo de implementación, consulte [Tipos de implementación](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implementación, la implementación simplificada: de oferta a facturación proforma, produce una **implementación solo de Common Data Service de Project Operations**.

- [Instalar Project Operations en un nuevo entorno CDS](#new)
- [Instalar en un entorno CDS existente](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Instalar Project Operations en un nuevo entorno CDS

1. Como [Administrador global o de Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, cree un nuevo entorno CDS en el [Centro de administración de PowerPlatform](https://admin.powerplatform.com). Asegúrese de que **Base de datos CDS** y **Aplicaciones de Dynamics 365** están habilitados. Para obtener más información, consulte [Crear y administrar entornos en el centro de administración de Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Seleccione **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Instalar Project Operations en un entorno CDS existente

1. Como [Administrador global o de Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, ubique el entorno en el [centro de administración de PowerPlatform](https://admin.powerplatform.com) donde desea instalar Project Operations.
2. Instale **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365. Para obtener más información, consulte [Administrar aplicaciones de Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]