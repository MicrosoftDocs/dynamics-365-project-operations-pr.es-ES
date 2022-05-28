---
title: Realizar un seguimiento del estado de un proyecto
description: Cómo hacer seguimiento del estado de un proyecto en Project Service
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
ms.openlocfilehash: 58274886a9f9ce6ae49c64c1d7ac491e29c7d06c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593403"
---
# <a name="track-a-projects-status-project-service"></a>Seguir el estado de un proyecto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Use las [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] para realizar un seguimiento del progreso del proyecto de un cliente.  

A medida que la participación progresa, las fases del proyecto se actualizan para reflejar la fase de la participación:  

| Task | Description | 
|------------|----------|
| **New** | Cuando cree un proyecto, la fase se establece como **Nueva**. Si creó el proyecto desde una plantilla, en esta etapa el proyecto pude tener una programación, estimaciones, y datos del equipo. De lo contrario, será la información general del proyecto y deberá especificar manualmente el resto de los componentes del proyecto. |
| **Oferta** |  Cuando asocia un proyecto a una oferta o lo crea desde una oferta, la fase del proyecto se establece en **Oferta** y las fechas de inicio y finalización estimadas también se actualizan. Cuando el proyecto está en la fase de oferta, los detalles de la oferta se muestran en la pestaña **Ventas** en la página **Proyecto**. |
| **Planificar** |  Si gana una oferta asociada a un proyecto y, cuando la participación progresa a la fase de contrato, la fase del proyecto se actualiza a **Plan**. Los detalles del contrato se muestran en la pestaña **Ventas** en la página **Proyecto**. |
| **Completada** | Cuando se completa el trabajo del proyecto, puede cambiar la fase a **Completado**. Cuando la fase del proyecto se establece como completada, se entiende que el trabajo se ha completado al 100% pero el proyecto se mantiene abierto para cualquier entrada de tiempo o gasto pendiente de registrar. |
| **Cerrar** | Cuando todas las transacciones se han registrado en el proyecto y no espera que se registren más, puede establecer manualmente la fase a **Cierre**. Cuando el proyecto se establece en **Cierre**, no puede registrar más transacciones en el proyecto y el proyecto será de solo lectura. |

## <a name="to-track-a-projects-status"></a>Para realizar un seguimiento del estado de un proyecto  

1.  Vaya a **Project Service > Proyectos**.  

2.  Haga clic en el proyecto en el que desea trabajar.  

3.  En la barra en la parte superior de la pantalla, seleccione la flecha hacia abajo junto al nombre del proyecto y, después, haga clic en **Seguimiento de proyecto**.  

4.  Seleccione **Seguimiento del esfuerzo** o **Seguimiento de costes** en la lista desplegable situada encima de la lista de tareas.  

5.  Haga doble clic en cualquier tarea para editarla. También puede mover o cambiar el tamaño de las barras en el diagrama de Gantt para cambiar el tiempo y el progreso para una tarea.  

### <a name="see-also"></a>Vea también  
 [Guía del jefe de proyecto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
