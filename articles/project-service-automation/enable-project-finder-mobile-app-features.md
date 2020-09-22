---
title: Habilitar las características de la aplicación Project Finder Mobile
description: Cómo habilitar las características de la aplicación Project Finder Mobile para Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755940"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Habilitar las características de la aplicación Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sus recursos pueden utilizar la aplicación Project Finder Mobile en su teléfono con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para buscar nuevos proyectos para trabajar y actualizar sus conjuntos de habilidades.  
  
 La aplicación está disponible para teléfonos [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] y [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Debe configurar un par de opciones en los parámetros de su unidad organizativa para permitir que los usuarios vean los requisitos de recursos de los proyectos y actualicen sus cualificaciones.  
  
> [!NOTE]
>  La aplicación Project Finder Mobile funciona únicamente con [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], no con instalaciones locales.  
  
1. Vaya a **Project Service > Parámetros**.  
  
2. Haga clic en los parámetros que desea usar para permitir las características de la aplicación Project Finder Mobile.  
  
3. En el área **General**, establezca **Requisitos de recursos visibles para los recursos** a **Sí**.  
  
4. Establezca **Permitir actualización de cualificación por recurso** como **Sí**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Este es un valor global. Los jefes de proyecto pueden definir si un proyecto individual será visible en la página **Equipo del proyecto** del proyecto.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notificaciones por correo electrónico  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envía correos electrónicos relativos a solicitudes de recursos a los siguientes destinatarios en los siguientes momentos:  
  
|Destinatario|Evento|  
|---------------|-----------|  
|Jefe de proyecto|-   Cuando un recurso se suscribe a un proyecto con la aplicación Project Finder Mobile.|  
|Recurso|- Cuando el trabajo del proyecto que el recurso se ha registrado ya ha sido cumplido por otro recurso.<br />- Cuando se haya aprobado o rechazado su solicitud de aprobación de habilidad.<br />- Cuando se haya aprobado o rechazado su solicitud de suscripción al proyecto.|  
  
## <a name="privacy-notice"></a>Aviso de privacidad  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Vea también  
 [Configuración de recursos](../project-service/set-up-resources.md)
