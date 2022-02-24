---
title: Agregar una suscripción de Azure a un proyecto LCS
description: Este tema proporciona información sobre cómo conectar su suscripción de Azure a un proyecto LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880559"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Agregar una suscripción de Azure a un proyecto LCS

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Los entornos alojados en la nube deben implementarse mediante una suscripción de Azure existente. Este tema explica cómo conectar su suscripción exisente de Azure a un proyecto LCS. 

## <a name="grant-admin-consent"></a>Conceder consentimiento del administrador

1. En su proyecto LCS, en la sección **Ambientes**, seleccione **Configuración de Microsoft Azure**.

![Configuración de Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. En la página **Configuración del proyecto**, en la pestaña **Conectores de Azure**, seleccione **Autorizar**. Esto permite implementar entornos en este proyecto.

![Conectores de Azure](./media/2AzureConnectors.png)

3. Seleccione **Autorizar** nuevamente para conceder el consentimiento del administrador.

![Conceder consentimiento del administrador](./media/3GrantAdminConsent.png)

4. Acepta la solicitud de permisos.

![Aceptar solicitud de permiso](./media/4AcceptPermissionRequest.png)

La autorización ya está completa. 

![Autorización corrrecta](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Proporcionar acceso a Dynamics Deployment Services a su suscripción de Azure

1. Vaya a [Facturación de Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) y seleccione su suscripción. Dynamics Deployment Services necesita acceder a esta suscripción para poder implementar entornos.

![Detalles de suscripción a Azure](./media/6AzureSubscription.png)

2. Seleccione **Control de acceso (IAM)** en el panel de navegación y luego seleccione **Agregar asignación de roles**.
3. En el control deslizante del lado derecho, seleccione **Rol de colaborador** y, en la lista provista, busque y seleccione **Dynamics Deployment Services**. 
4. Seleccione **Guardar**.

![Acceso a suscripción](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Agregar un conector de suscripcióna un proyecto LCS

1. En su proyecto LCS, en la página **Configuración de Microsoft Azure**, seleccione **Añadir** para agregar un nuevo conector.
2. Escriba su Id. de suscripción de Azure. Puede encontrar su Id. de suscripción de Azure en el [Portal de Azure](https://ms.portal.azure.com/), en **Configuración**, en la parte inferior izquierda de la pantalla.
3. En el campo **Configurar para usar Azure Resource Manager**, seleccione **Sí**.
4. Asegúrese de que el dominio de inquilino AAD de suscripción de Azure coincida con la suscripción de Azure propietaria del dominio que está usando y seleccione **Siguiente**.
5. En la pantalla **Configuración de Microsoft Azure**, seleccione **Siguiente** para confirmar. Si recibe un error en esta pantalla, regrese a la sección [Proporcionar acceso a Dynamics Deployment Services a la suscripción de Azure](#provide) de este tema y asegúrese de haber completado todos los pasos.
6. Descargue el certificado de administración de Azure en una carpeta local de su equipo. Solicite a su administrador de suscripción de Azure que cargue el certificado en el Portal de administración de Azure seleccionando la suscripción y yendo a **Configuración** > **Certificados de administración**. Este certificado permite a LCS comunicarse con Azure en su nombre. Puede omitir este paso si su usuario tiene acceso a la suscripción.
7. Seleccione **Siguiente**.
8. Seleccione la región de Azure para implementar y seleccione un centro de datos que esté cerca de dónde planea usar este sistema.
9.  Seleccione **Conectar**.

Ha conectado correctamente su suscripción de Azure. Ahora puede implementar entornos alojados en la nube de Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
