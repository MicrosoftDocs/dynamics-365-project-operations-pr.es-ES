---
title: Implementar Project Operations Lite
description: 'Este artículo proporciona información sobre cómo instalar Project Operations de forma simplificada: del acuerdo a la facturación proforma.'
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811000"
---
# <a name="deploy-project-operations-lite"></a>Implementar Project Operations Lite

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_



Project Operations admite varios modelos de implementación. Para determinar el mejor modelo de implementación, consulte [Tipos de implementación](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implementación, la implementación simplificada: de oferta a facturación proforma, produce una **implementación solo de Dataverse de Project Operations**.

- [Instalar Project Operations en un nuevo entorno de Dataverse](#new)
- [Instalar en un entorno de Dataverse existente](#existing)
- [Instale en un entorno existente Dataverse que tenga componentes de escritura dual](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Instalar Project Operations Lite en un nuevo entorno de Dataverse

1. Como [Administrador global o de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, cree un nuevo entorno de Dataverse en el [Centro de administración de PowerPlatform](https://admin.powerplatform.com). Asegúrate de que **Crear una base de datos para este entorno** y **Aplicaciones de Dynamics 365** están habilitados. Para obtener más información, consulte [Crear y administrar entornos en el centro de administración de Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Seleccione **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalar Project Operations Lite en un entorno de Dataverse existente 
1. Como [Administrador global o de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, ubique el entorno en el [centro de administración de PowerPlatform](https://admin.powerplatform.com) donde desea instalar Project Operations.
1. Instale **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365. Para obtener más información, consulte [Administrar aplicaciones de Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Instale Project Operations Lite en un entorno existente Dataverse donde las soluciones de escritura dual ya están presentes

Si desea continuar ejecutando Project Operations en modo Lite Deployment, debe seguir estos pasos:

1. Como [Administrador global o de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con licencia de Project Operations, ubique el entorno en el [centro de administración de PowerPlatform](https://admin.powerplatform.com) donde desea instalar Project Operations.
1. Instale **Microsoft Dynamics 365 Project Operations** en la lista de implementaciones de aplicaciones de Dynamics 365. Para obtener más información, consulte [Administrar aplicaciones de Dynamics 365](/power-platform/admin/manage-apps).
1. Debido a que su entorno tiene componentes de escritura dual que ayudan con la integración de las aplicaciones de finanzas y operaciones instaladas, la instalación de Project Operations también instalará las capacidades y extensiones necesarias para integrar los datos relacionados con el proyecto a las aplicaciones de finanzas y operaciones. Dado que desea ejecutar Project Operations en la implementación de Lite, estos componentes de integración deben eliminarse, ya que crearán restricciones y sobrecarga para los escenarios de implementación de Lite. Desinstale manualmente las soluciones **Dynamics 365 Project Operations de doble escritura** y **Mapas de entidad de Dynamics 365 Project Operations de doble escritura** para eliminar estos componentes.
1. Vaya a **Project Operations -> Configuración -> Parámetros**. Abra la página de detalles **Parámetro del proyecto** y establezca el campo **Comportamiento de actualización de la solución** en **Solo Lite**. Esto garantiza que las actualizaciones posteriores de Project Operations no recuperen los componentes de integración en Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
