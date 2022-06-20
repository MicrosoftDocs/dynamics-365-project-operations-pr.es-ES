---
title: Agregar una suscripción de Azure a un proyecto LCS
description: Este artículo proporciona información sobre cómo conectar su suscripción de Azure a un proyecto de LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64ee8cfa7394a08c3d588c0e8f4a73185d9496cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912169"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Agregar una suscripción de Azure a un proyecto LCS

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Los entornos alojados en la nube deben implementarse mediante una suscripción de Azure existente. Este artículo explica cómo conectar su suscripción de Azure existente a un proyecto de LCS. 

## <a name="grant-admin-consent"></a>Conceder consentimiento del administrador

1. En su proyecto LCS, en la sección **Ambientes**, seleccione **Configuración de Microsoft Azure**.

![Configuración de Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. En la página **Configuración del proyecto**, en la pestaña **Conectores de Azure**, seleccione **Autorizar**. Esto permite implementar entornos en este proyecto.

![Conectores de Azure.](./media/2AzureConnectors.png)

3. Seleccione **Autorizar** nuevamente para conceder el consentimiento del administrador.

![Conceder consentimiento del administrador.](./media/3GrantAdminConsent.png)

4. Acepta la solicitud de permisos.

![Aceptar solicitud de permiso.](./media/4AcceptPermissionRequest.png)

La autorización ya está completa. 

![Autorización corrrecta.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Proporcionar acceso a Dynamics Deployment Services a su suscripción de Azure

1. Vaya a [Facturación de Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) y seleccione su suscripción. Dynamics Deployment Services necesita acceder a esta suscripción para poder implementar entornos.

![Detalles de la suscripción a Azure.](./media/6AzureSubscription.png)

2. Seleccione **Control de acceso (IAM)** en el panel de navegación y luego seleccione **Agregar asignación de roles**.
3. En el control deslizante del lado derecho, seleccione **Rol de colaborador** y, en la lista provista, busque y seleccione **Dynamics Deployment Services**. 
4. Seleccione **Guardar**.

![Acceso a la suscripción.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Agregar un conector de suscripcióna un proyecto LCS

1. En su proyecto LCS, en la página **Configuración de Microsoft Azure**, seleccione **Añadir** para agregar un nuevo conector.
2. Escriba su Id. de suscripción de Azure. Puede encontrar su Id. de suscripción de Azure en el [Portal de Azure](https://ms.portal.azure.com/), en **Configuración**, en la parte inferior izquierda de la pantalla.
3. En el campo **Configurar para usar Azure Resource Manager**, seleccione **Sí**.
4. Asegúrese de que el dominio de inquilino AAD de suscripción de Azure coincida con la suscripción de Azure propietaria del dominio que está usando y seleccione **Siguiente**.
5. En la pantalla **Configuración de Microsoft Azure**, seleccione **Siguiente** para confirmar. Si recibe un error en esta pantalla, regrese a la sección [Proporcionar acceso a Dynamics Deployment Services a la suscripción de Azure](#provide) en este artículo y asegúrese de haber completado todos los pasos.
6. Descargue el certificado de administración de Azure en una carpeta local de su equipo. Solicite a su administrador de suscripción de Azure que cargue el certificado en el Portal de administración de Azure seleccionando la suscripción y yendo a **Configuración** > **Certificados de administración**. Este certificado permite a LCS comunicarse con Azure en su nombre. Puede omitir este paso si su usuario tiene acceso a la suscripción.
7. Seleccione **Siguiente**.
8. Seleccione la región de Azure para implementar y seleccione un centro de datos que esté cerca de dónde planea usar este sistema.
9.  Seleccione **Conectar**.

Ha conectado correctamente su suscripción de Azure. Ahora puede implementar entornos hospedados en la nube de Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
