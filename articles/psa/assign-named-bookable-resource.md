---
title: Reservar recursos con nombre que se pueden reservar para un equipo de proyecto y asignar tareas
description: En este tema se proporciona información sobre cómo reservar recursos con nombre para equipos de proyectos y asignarlos a tareas.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 8568921dd16472f10a7043c5fe3f58b9f5cd3989ad39e3a3bdf269b0c7203ae2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998662"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Reservar recursos con nombre que se pueden reservar para un equipo de proyecto y asignar tareas 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Puede agregar un recurso con nombre a su equipo de proyecto reservándolo directamente en el equipo. Para ello, complete los pasos que se indican a continuación.

1. En Project Service Automation, vaya a **Proyectos** y seleccione el proyecto abierto para el que desea realizar la reserva.
2. En la página **Proyecto**, en la pestaña **Equipo**, haga clic en **Nuevo**. 

![Agregar un miembro de equipo desde la pestaña del equipo.](media/RM-how-to-1.png)

3. En el cuadro de diálogo **Creación rápida: Miembro del equipo del proyecto**, seleccione el recurso reservable. El campo **Rol** se completará con el rol predeterminado del recurso si tiene alguno asignado. Puede cambiar el rol si fuera necesario. 
4. Seleccione las fechas de inicio y finalización del tiempo que será necesario el recurso y seleccione el método de asignación de capacidad del recurso. 
5. Si desea que el miembro del equipo sea un aprobador de proyecto, seleccione **Sí** en el campo **Aprobador de proyecto**. Esto significa que el miembro del equipo podrá aprobar las entradas de gastos y de tiempo que se envíen para este proyecto. 
6. Haga clic en **Guardar**.

![Agregar un miembro de equipo en el formulario de creación rápida.](media/RM-how-to-2.png)


Ahora puede asignar el recurso reservado a las tareas del proyecto. En la página **Proyecto**, haga clic en la pestaña **Programación** para asignar tareas al nuevo recurso. El selector de recursos que se inicia desde el campo **Recursos** de la cuadrícula de tareas mostrará los miembros de equipo que se pueden seleccionar.

![Asignación de un miembro de equipo a una tarea en la pestaña de programación.](media/RM-how-to-3.png)

En la versión 3 de Project Service Automation (PSA), las reservas de recursos y las asignaciones de tareas no están emparejadas firmemente. Esto significa que al usar el selector de recursos en la programación, puede asignar tareas a los miembros del equipo por más horas de las cubren sus reservas en el proyecto.
Puede ver las diferencias que hay entre las asignaciones y las reservas de los miembros de equipo en la pestaña **Equipo** o en la pestaña **Conciliación de recursos**. También puede conciliar las diferencias entre las reservas y las asignaciones de los recursos en un nivel más detallado.

![Pestaña Conciliación de recursos.](media/RM-how-to-4.png)

También puede usar el selector de recursos de la pestaña **Programación** para buscar y seleccionar recursos que se pueden reservar que ya no formen parte del equipo del proyecto. Estos se muestran en el selector de recursos como **Otros recursos**.

![Asignación de un recurso que no es miembro del equipo a una tarea.](media/RM-how-to-5.png)

En este tipo de asignaciones, el recurso se agrega al equipo del proyecto y se asigna a la tarea, pero no se genera ninguna reserva.

![Miembro del equipo con asignaciones y sin reservas.](media/RM-how-to-6.png)

Puede usar la capacidad de ampliación de reserva de la pestaña **Reconciliación** o el **Tablero de programación** para reservar la capacidad del recurso para el proyecto.

![Ampliación de la reserva de un miembro del equipo en la pestaña Conciliación de recursos.](media/RM-how-to-7.png)

Tras reservar un miembro de equipo en su proyecto, podrá mantener las reservas o utilizar el Tablero de programación directamente para administrar las reservas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]