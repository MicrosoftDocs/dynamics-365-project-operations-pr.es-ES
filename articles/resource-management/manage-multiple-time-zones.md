---
title: Administrar zonas horarias
description: Cuando se crea un proyecto, su zona horaria se basa en la zona horaria definida en la plantilla de horas de trabajo aplicada.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961954"
---
# <a name="manage-time-zones"></a>Administrar zonas horarias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


## <a name="projects"></a>Proyectos

Cuando se crea un proyecto, su zona horaria se basa en la zona horaria definida en la plantilla de horas de trabajo aplicada. En el **Proyecto**, las fechas son siempre relativas a la zona horaria del usuario que está conectado en cada pestaña, excepto la pestaña **Tarea**. Cuando vea la estructura de descomposición del trabajo, las fechas siempre se mostrarán en la zona horaria del proyecto.

## <a name="tasks"></a>Tareas

Cuando se crea una tarea, la hora de inicio, la hora de finalización y las horas/día se controlan mediante las horas de trabajo del proyecto. Por ejemplo, si se crea una tarea con un proyecto cuya zona horaria es -8 PST y tiene las siguientes horas de trabajo: de 9:00 a. m. a 5:00 p. m, de lunes a viernes, cualquier tarea creada sin una asignación respetará la hora de inicio y hora de finalización del calendario del proyecto.

## <a name="manage-resources-with-time-zones"></a>Administrar recursos con zonas horarias

Para obtener resultados precisos y predecibles al usar **Ampliar reserva**, hay dos requisitos previos clave que deben cumplirse:  

- El usuario debe configurar la zona horaria de su dispositivo para que coincida con la zona horaria definida en la **Configuración de personalización** del sistema.
 
  ![Configuración de zona horaria en Windows 10](media/reconcile-assignments-03.png)

  ![Configuración de la zona horaria en la configuración de personalización](media/reconcile-assignments-04.png)
 
- El recurso reservable debe tener al menos un minuto de tiempo de trabajo que se superponga con los contornos que se utilizan para definir la extensión solicitada. Por ejemplo, los siguientes recursos con horas de trabajo comprendidas entre las 9:00 a. m. y las 7:00 p. m. 

  ![Comparación de contornos de recursos](media/reconcile-assignments-05.png)

En la tabla siguiente se muestra:

- Plantilla de calendario de proyecto
- Recurso A: Este recurso tiene el mismo calendario y se encuentra en la misma zona horaria que el proyecto. La hora de inicio de las reservas será las 9 de la mañana.
- Recurso B: este recurso se encuentra en una zona horaria diferente a la del proyecto y comienza a las 7:00 a.m. en su zona horaria. Sin embargo, las reservas comenzarán a las 9 de la mañana, ya que es la primera hora de inicio del contorno de la tarea.
- Recursos C y D: los recursos están ubicados en diferentes zonas horarias, ambas diferentes entre sí y del proyecto, y sus reservas no comienzan antes de sus respectivas horas de inicio disponibles.

|Entidad  |Calendario  |
|-|-|
|Plantilla de calendario de proyecto   | ![calendario de proyecto](media/reconcile-assignments-06.png) |
|Recurso A  | ![Calendario de recurso A](media/reconcile-assignments-06.png) |
|Recurso B  |  ![Calendario de recurso B](media/reconcile-assignments-07.png) |
|Recurso C  |  ![Calendario de recurso C](media/reconcile-assignments-08.png) |
|Recurso D  | ![Calendario de recurso D](media/reconcile-assignments-09.png)  |
 
Cuando navega a la vista **Conciliación**, se muestran las asignaciones de recursos y la escasez de reservas asociada.

![Vista de conciliación antes de la extensión](media/reconcile-assignments-10.png)

Una vez que se ha utilizado la funcionalidad de extensión de reserva para cada recurso, las reservas se extienden con éxito para cada recurso porque las horas de trabajo de cada recurso se superponen con los contornos de la escasez.

![Vista de conciliación después de la ampliación de reserva](media/reconcile-assignments-11.png) 

Observe que una mirada más detallada a los detalles de las reservas muestra diferencias en la hora de inicio de las reservas. Las reservas no comienzan antes de la hora de inicio del contorno de asignación ni antes de la hora de inicio disponible del recurso.

![Nuevas reservas de los recursos en el tablero de programación](media/reconcile-assignments-12.png)
