---
title: Conciliación de reservas y asignaciones
description: En este tema se proporciona información sobre datos reales.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 9528bd983e6e18197138f0720abccdc6d6fa1ed5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147944"
---
# <a name="reconcile-bookings-and-assignments"></a>Conciliación de reservas y asignaciones

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Las reservas de proyectos de un miembro del equipo del proyecto y las asignaciones de tareas del proyecto están unidas libremente. Por lo tanto, un recurso puede tener asignaciones de tareas que no se corresponden con reservas y reservas que no corresponden con asignaciones de tareas. Idealmente, las reservas y asignaciones de proyectos están alineadas de modo que los recursos tengan la capacidad comprometida para realizar sus asignaciones de tareas. Sin embargo, la realidad es que las reservas pueden producirse en función de la disponibilidad, y los tiempos de las tareas pueden cambiar a medida que el proyecto continúa durante su ciclo de vida. Por lo tanto, el emparejamiento flexible permite flexibilidad.

Debido al emparejamiento flexible de las reservas de proyectos y las asignaciones de tareas, se incluye una pestaña **Conciliación** en la entidad de proyecto. Esta pestaña ayuda a los jefes de proyecto a conciliar las reservas de los miembros del equipo y sus asignaciones para su equipo de proyecto.

Para cada miembro del equipo nombrado, la pestaña **Conciliación** muestra las reservas y las asignaciones hasta la tarea individual. Muestra horas en celdas que pueden representar períodos de meses a días.

En el campo **Escala temporal**, puede seleccionar **Mes**, **Semana** o **Día**. Se selecciona **Semana** por defecto. Sin embargo, puede cambiar el valor predeterminado seleccionando el botón **Configuración**. Cuando se abre la pestaña **Conciliación**, se muestra la fecha actual, pero puede usar el control de calendario para avanzar o retroceder en el tiempo. Cuando un proyecto tiene una fecha de inicio en el futuro, la pestaña muestra esa fecha cuando se abre. El control de calendario también tiene opciones que le permiten pasar a las fechas de inicio y finalización del proyecto.

Puede usar los controles de expansión en cada recurso para mostrar los detalles de las reservas de ese recurso. También puede expandir las asignaciones de cada recurso al nivel de la tarea individual.

La parte inferior de la pestaña **Conciliación** muestra un total neto total para el proyecto, y la pestaña también incluye una columna de total. Para cada recurso, la pestaña selecciona la diferencia entre las reservas de un miembro del equipo en el proyecto y el resumen de las asignaciones de tareas de ese miembro del equipo. Idealmente, la diferencia debería ser 0 (cero). Es decir, no debería haber diferencia entre las reservas del recurso y sus asignaciones de tareas. Cualquier diferencia se indica con color y sombreado para indicar dos condiciones:

- **Escasez de reservas**: la escasez de reservas se produce cuando un recurso tiene más asignaciones que reservas. Puesto que esta capacidad no se ha reservado, un jefe de proyecto puede corregir esa condición extendiendo las reservas del recurso para cubrir la escasez.
- **Reservas en exceso**: las reservas en exceso se producen cuando se ha reservado un recurso para el proyecto, pero no se ha asignado a tareas. Esta condición podría ser aceptable si, por ejemplo, el recurso se ha reservado antes de que se produzca la a asignación de tareas. Sin embargo, en otros casos, el recurso podría no estar planificado para asignarse. En estos casos, el jefe de proyecto debería considerar cancelar las reservas del recurso de modo que la capacidad pueda utilizarse para otro proyecto.

> [!NOTE]
> La leyenda de estas condiciones podría estar oculta para dejar más espacio para la cuadrícula. En este caso, puede hacer que la leyenda sea visible seleccionando el botón **Configuración**.

En algunos casos, cuando el campo **Escala temporal** se establece en un nivel superior a **Día**, las diferencias pueden calcularse como 0 (cero). Por ejemplo, en el nivel **Mes**, la diferencia neta para un recurso podría ser 0 (cero) para indicar que las reservas equivalen a asignaciones. Sin embargo, si observa el nivel **Semana**, puede ver que hay asignaciones de 0 (cero) horas y reservas de 40 horas en la primera semana del mes, y asignaciones de 40 horas y reservas de 0 (cero) horas en la segunda semana del mes. Aunque el total de reservas y asignaciones para el mes son iguales, difieren por semana.

Cuando vea niveles de tiempo más altos, la pestaña **Conciliación** mostrará un indicador de celda para notificarle que hay diferencias en los niveles de tiempo más bajos. Por ejemplo, en la siguiente ilustración, aparece un indicador de celda en la celda para el mes de octubre de 2018 para el recurso denominado Lidia Valladares. Por lo tanto, puede ver que, a pesar de que las reservas y asignaciones del recurso son iguales cuando se agregan a nivel de **Mes**, no coinciden en niveles inferiores.

![Reservas y asignaciones no coincidentes a nivel mensual](media/reconcile-assignments-01.JPG)

Haga doble clic en una celda para acercar el siguiente nivel inferior y ver la diferencia. Por ejemplo, si hace doble clic en la diferencia de octubre de 2018 para Lidia Valladares, explorará en profundidad hasta el nivel **Semana**. Luego podrá ver que el recurso tiene reservas de 16 horas, pero no asignaciones en las primeras dos semanas de octubre, y 16 horas de asignaciones pero no reservas en la tercera semana de octubre.

![Reservas y asignaciones no coincidentes a nivel semanal](media/reconcile-assignments-02.JPG)

Puede hacer clic con el botón derecho en una celda para alejar el siguiente nivel superior. Puede, además, apagar el indicador de celda seleccionando el botón **Configuración**. 

También puede usar los botones **Anterior** y **Siguiente** sobre la cuadrícula para moverse a través de cualquier diferencia en su proyecto. Para usar esos botones, primero debe seleccionar un recurso. Seleccione **Siguiente** para pasar a la siguiente diferencia entre reservas y asignaciones para ese recurso. Seleccione **Anterior** para ir a la diferencia anterior.

En situaciones en las que tiene asignaciones de tareas para un recurso pero no tiene reservas, puede seleccionar la escasez de reservas y luego seleccionar **Ampliar reservas**. Después puede ver la reserva necesaria para solucionar la escasez de recursos. También puede ver las reservas del recurso en el proyecto actual y otros proyectos. Seleccione **Aceptar** para crear la reserva del recurso sin tener en cuenta la disponibilidad actual. El jefe de proyecto o el administrador de recursos pueden usar el tablero de programación para administrar situaciones en las que un recurso se ha saturado más allá de su capacidad debido a que se extendieron sus reservas.

## <a name="managing-with-time-zones"></a>Administrar con zonas horarias
Para garantizar resultados precisos y predecibles al usar Ampliar reserva, hay dos requisitos previos clave que se deben cumplir:  

- El usuario debe configurar la zona horaria de su dispositivo para que coincida con la zona horaria definida en la Configuración de personalización de su sistema.
 
  ![Configuración de zona horaria en Windows 10](media/reconcile-assignments-03.png)

  ![Configuración de la zona horaria en la configuración de personalización](media/reconcile-assignments-04.png)
 
- El Recurso que se puede reservar debe tener al menos un minuto de tiempo de trabajo que se superponga con los contornos que se utilizan para definir la extensión solicitada. Por ejemplo, en el siguiente ejemplo se muestran recursos de revisión con horas de trabajo que se encuentran entre las 9 de la mañana y las 7 de la tarde. 

  ![Comparación de contornos de recursos](media/reconcile-assignments-05.png)

En la tabla siguiente se muestra:

- Una plantilla de calendario de proyecto.
- Recurso A: Este recurso tiene el mismo calendario y se encuentra en la misma zona horaria que el proyecto. La hora de inicio de las reservas será las 9 de la mañana.
- Recursos B: Este recurso se encuentra en una zona horaria diferente de la del proyecto y, por tanto, comienza a las 7 de la mañana en su zona horaria. Sin embargo, las reservas comenzarán a las 9 de la mañana, ya que es la primera hora de inicio del contorno de la tarea.
- Recursos C y D: los recursos también se encuentran en diferentes zonas horarias, tanto diferentes entre sí como del proyecto, y sus reservas comienzan no antes de sus respectivas horas de inicio disponibles.

|Entidad  |Calendario  |
|-|-|
|Plantilla de calendario de proyecto   | ![calendario de proyecto](media/reconcile-assignments-06.png) |
|Recurso A  | ![Calendario de recurso A](media/reconcile-assignments-06.png) |
|Recurso B  |  ![Calendario de recurso B](media/reconcile-assignments-07.png) |
|Recurso C  |  ![Calendario de recurso C](media/reconcile-assignments-08.png) |
|Recurso D  | ![Calendario de recurso D](media/reconcile-assignments-09.png)  |
 
Cuando navegue hasta la vista de conciliación, se mostrarán las asignaciones de recursos y la escasez de reserva asociada.
 ![Vista de conciliación antes de la extensión](media/reconcile-assignments-10.png)

Una vez que se ha ejecutado la funcionalidad Ampliar reserva en cada recurso, las reservas se amplían correctamente para cada recurso. Esto se debe a la superposición de las horas de trabajo de cada recurso con los contornos de la escasez.
 ![Vista de conciliación después de la ampliación de reserva](media/reconcile-assignments-11.png) 

Sin embargo, examinando los detalles de las reservas más de cerca se muestran las diferencias en la hora de inicio de las reservas. Las reservas comenzarán no antes de la hora de inicio del contorno de la tarea y no antes de la hora de inicio disponible del recurso.
 ![Nuevas reservas de los recursos en el tablero de programación](media/reconcile-assignments-12.png)
