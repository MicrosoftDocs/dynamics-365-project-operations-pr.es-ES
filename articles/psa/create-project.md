---
title: Crear un proyecto
description: Cómo crear un pojecto en Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085160"
---
# <a name="create-a-project-project-service"></a>Crear un proyecto (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Cree un proyecto usando las capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] cuando desea crear una oportunidad, una oferta o un contrato para servicios basados en proyecto. La capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ayudan a administrar el proyecto desde la oportunidad hasta su conclusión. Cuando cree un proyecto, también creará una estructura de descomposición del trabajo, que afecta a las ofertas, valoraciones de costo, y administración de recursos.  
  
1.  Vaya a **Project Service > Proyectos**.  
  
2.  Haga clic en **Nuevo proyecto**.  
  
3.  En el área **Resumen** , escriba un nombre para el proyecto y a continuación, especifique tantos detalles como pueda. Los elementos marcados con un asterisco rojo (*) son obligatorios.  
  
4.  Haga clic en **Guardar** para crear el proyecto para que pueda seguir editándolo.  
  
A continuación, creará una estructura de descomposición del trabajo para el proyecto para definir las tareas, el tiempo, y los roles de recursos necesarios para el proyecto.  

> [!NOTE]
> Al programar, Project Service Automation respeta la zona horaria de la plantilla **Hora de trabajo** aplicada. Sin embargo, al visualizar las tareas programadas, las fechas de inicio y finalización de una tarea se mostrarán en la zona horaria del usuario. Esto se aplica a otras vistas en fases de tiempo en el formulario **Proyecto**. Si la zona horaria del usuario no coincide con la zona horaria de la plantilla de hora de trabajo aplicada al proyecto, se producirá una advertencia que explica la diferencia. 
  
### <a name="see-also"></a>Vea también  
 [Guía del jefe de proyecto](../psa/project-manager-guide.md)
