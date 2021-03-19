---
title: Administrar proyectos y reservas en su calendario de Office 365
description: Administración de proyectos y reservas en su calendario de Office 365
author: ruhercul
manager: kfend
ms.service: project-operations
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 1df4864ca8dbf6948ca88a7c82a6c0a676e3bd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275064"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Administrar proyectos y reservas en su calendario (Project Service)

> [!Note]
> EN DESUSO: Esta característica está en desuso y ya no está disponible.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Vista citas personales, reservas de trabajo de proyectos y asignaciones de orden de trabajo de servicio de campo mediante el calendario [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Con todo en un solo lugar, es más fácil administrar la jornada. Las reuniones, citas, reservas y tareas están disponibles en su calendario [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Si usa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], también puede especificar citas personales en la vista de entrada de tiempo de Project Service. Esto permite a los administradores de proyectos y recursos conocer la disponibilidad para proyectos. También permite ahorrar tiempo, porque no tiene que especificar información sobre las citas personales dos veces. Puede importar simplemente las citas personales del calendario a la vista de entrada de tiempo de Project Service.  
  
 El calendario sincronizará las reservas de órdenes de trabajo y proyectos desde hoy hasta las cuatro próximas semanas. Este ajuste no se puede cambiar.  
  
 La sincronización solo se admite de una forma, de PSA a su calendario de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Puede sincronizar en el orden inverso. 
  
 Para aprender a usar su calendario [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], consulte [Calendario en Outlook en la web para la empresas](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Programa de instalación  
 Antes de poder ver y administrar sus reservas en su calendario [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], necesita configurar algunas tareas.  
  
- Deberá tener credenciales de administrador del sistema o administrador global de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- Su administrador también deberá configurar el perfil de servidor de correo electrónico y cada usuario deberá configurar su buzón. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Establecer procesamiento de correo electrónico mediante sincronización del lado del servidor](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Activar la sincronización de la organización (tarea de administración)  
  
1.  En el menú principal, haga clic en **Configuración** > **Administración**.  
  
2.  Haga clic en **Configuración del sistema**.  
  
3.  Haga clic en la pestaña **Sincronización**.  
  
4.  En **Seleccione si desea habilitar la sincronización de las reservas de recursos con Outlook**, active **Sincronizar las reservas de recursos con Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Activar la sincronización para su perfil de usuario (tarea de usuario)  
  
1.  Haga clic en el botón **Configuración** en la esquina superior derecha de la pantalla.  
  
2.  Haga clic en **Opciones**.  
  
3.  Haga clic en la pestaña **Sincronización**.  
  
4.  En **Sincronizar las reservas de recursos con Outlook**, active **Sincronizar las reservas de recursos con Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importar las citas personales (tarea de usuario)  
 Puede importar las citas personales del calendario a la vista de entrada de tiempo de Project Service Automation.  
  
1. Abra el calendario [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] y haga clic en **Importar datos**.  
  
2. En la pantalla Filtros, seleccione **Citas de Exchange** y después haga clic en **Aplicar**.  
  
3. El sistema extraerá citas en la vista de entrada de tiempo como entradas sugeridas de la semana actual. Para agregar entradas para otra semana, haga clic en **Anterior** o **Siguiente**.  
  
4. Seleccione la cita que desea agregar a la vista de entrada de tiempo de Project Service Automation.  
  
5. En el cuadro emergente **Entrada de tiempo**, seleccione las opciones correspondientes para convertir la cita en una vista de entrada de tiempo de Project Service Automation.  
  
6. Haga clic en **Guardar**.  
  
### <a name="see-also"></a>Vea también  
 [Guía de tiempo, gastos y colaboración](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]