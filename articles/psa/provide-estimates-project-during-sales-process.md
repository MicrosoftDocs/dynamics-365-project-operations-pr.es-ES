---
title: Proporcionar estimaciones de trabajo para un proyecto durante el proceso de ventas
description: Cómo proporcionar estimaciones de trabajo para un proyecto durante el proceso de ventas en Project Service
author: ruhercul
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
ms.openlocfilehash: da638e5ab1f75033e5a42e51d5f35307f88c5174
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594507"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Proporcionar estimaciones de trabajo para un proyecto durante el proceso de ventas (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Durante el proceso de ventas, puede realizar estimaciones de ventas partiendo de cero con líneas de oferta. Las capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] proporcionan una forma más científica y determinista de proporcionar estimaciones de ventas desglosando los elementos de trabajo y asociando los atributos relevantes que contribuyen en las estimaciones del proyecto en la estructura de descomposición del trabajo.  
  
 Una vez que logra una venta, puede usar la estructura de descomposición del trabajo asociada en el plan del proyecto, refinándola en la medida necesaria para una correcta realización del proyecto.  
  
## <a name="link-a-project-to-a-quote-line"></a>Vincule un proyecto a una línea de oferta  
 Al crear una línea de oferta basada en proyecto, puede crear un nuevo proyecto desde la línea de oferta. A continuación puede usar plantillas de proyectos, que son planes de proyecto y estimaciones financieras preconfiguradas estándar comunes a la organización, o una copia de un plan y estimaciones de proyecto a partir de un proyecto pasado. Cuando crea un proyecto, seleccionar una plantilla de proyecto proporciona una base para refinar el plan del proyecto, las estimaciones y los requisitos de rol. Al crear el proyecto desde la oferta, el proyecto se asociará automáticamente con la línea de la oferta.  
  
## <a name="project-estimate-components"></a>Componentes estimación del proyecto  
 La estructura de descomposición del trabajo en un proyecto proporciona una forma de desglosar el trabajo en tareas, mantener una jerarquía de tareas y asignar una estimación de esfuerzo necesario para realizar cada tarea. También puede asociar roles una tarea para indicar una estimación del tipo de recurso necesario para completar una tarea y una programación.  
  
 La estructura de descomposición del trabajo ayuda a determinar el esfuerzo de trabajo y las estimaciones de programación. De forma predeterminada, el proyecto usa listas de precios predeterminadas que usted definió anteriormente. El coste y los precios de ventas definidos en las listas de precios ayudan a determinar las estimaciones financieras del desglose de trabajo del proyecto.  
  
 Si el proyecto está asociado a una oferta, y la oferta tiene una lista de precios diferente de la predeterminada, la lista de precios de la oferta se usa para realizar estimaciones financieras.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importar estimaciones de un proyecto a una oferta  
 Una vez que tenga estimaciones del proyecto en el proyecto, puede importarlas en la línea de oferta:  
  
-   En **Detalles de línea de oferta**, haga clic en **Importar desde estimaciones**. 

-   Seleccione si desea importar las estimaciones resumidas por tipo de transacción, rol, o nivel de nodo de la estructura de descomposición del trabajo.  
  
### <a name="see-also"></a>Vea también  
 [Guía del jefe de proyecto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
