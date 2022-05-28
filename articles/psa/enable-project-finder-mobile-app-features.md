---
title: Habilitar las características de la aplicación Project Finder Mobile
description: Cómo habilitar las características de la aplicación Project Finder Mobile para Project Service
author: JohnPBurrows
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3f8f23c1f32d94a514de9ae40bd07b3d8063824c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593706"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Habilitar las características de la aplicación Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sus recursos pueden utilizar la aplicación Project Finder Mobile en el teléfono con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para buscar nuevos proyectos en los que trabajar y actualizar sus conjuntos de aptitudes.  
  
 La aplicación está disponible para teléfonos [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] y [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Para permitir que los usuarios vean los requisitos de los recursos de proyecto y actualicen sus aptitudes hay que seleccionar opciones en la configuración de parámetros de la unidad organizativa.
  
> [!NOTE]
>  La aplicación Project Finder Mobile funciona únicamente con [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], no con instalaciones locales.  
  
1. Vaya a **Project Service > Parámetros**.  
  
2. Haga clic en los parámetros que desea usar para permitir las características de la aplicación Project Finder Mobile.  
  
3. En el área **General**, establezca **Requisitos de recursos visibles para los recursos** a **Sí**.  
  
4. Establezca **Permitir actualización de cualificación por recurso** como **Sí**.  
  
   ![ProjectService_ProjectFinderEnable.](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Este es un valor global. Los jefes de proyecto pueden definir si un proyecto individual será visible en la página **Equipo del proyecto** del proyecto.  
  
   ![ProjectService_ProjectTeamVisible.](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notificaciones por correo electrónico  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envía correos electrónicos relativos a solicitudes de recursos a los siguientes destinatarios en los siguientes momentos:  
  
|Destinatario|Evento|  
|---------------|-----------|  
|Director del proyecto|- Un recurso se suscribe a un proyecto con la aplicación Project Finder Mobile.|  
|Recurso|- El trabajo del proyecto al que se ha suscrito el recurso ya lo ha realizado otro recurso.<br />- Se ha aprobado o rechazado la solicitud de aprobación de aptitud.<br />- Se ha aprobado o rechazado la solicitud de suscripción al proyecto.|  
  
## <a name="privacy-notice"></a>Aviso de privacidad  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Vea también  
 [Configuración de recursos](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
