---
title: Reserva automática de un recurso
description: En este tema se proporciona información sobre cómo programar de manera provisional o reservar automáticamente miembros de equipo de un proyecto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 2675096085fc4c673d15741042ffc1b82ed3de8b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146459"
---
# <a name="soft-book-a-resource"></a>Reserva automática de un recurso

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Puede programar de manera provisional o “automáticamente” un recurso en un equipo del proyecto para mostrar el plan para asignar el recurso al proyecto. Las reservas automáticas no consumen la capacidad disponible de un recurso, y puede asignar a los integrantes del equipo reservados automáticamente a tareas del proyecto. Sin embargo, dado que la reserva automática no consume la capacidad de un recurso, puede reservar manualmente el recurso para otras tareas en el mismo período. Los recursos genéricos no se pueden reservar automáticamente y las reservas automáticas no pueden cumplir solicitudes de recursos genéricos.

Los miembros del equipo del proyecto reservados automáticamente aparecen en la pestaña **Equipo** de la página **Proyecto**, con las horas reservadas automáticamente en la columna **Horas reservadas automáticamente** en la vista **Miembros del equipo con nombre**. Los miembros del equipo reservados automáticamente también aparecen en el tablero Programación. Dado que están reservados automáticamente, el tablero Programación no muestra ningún consumo de capacidad para estos recursos. La hora de reserva automática no aparece en la pestaña **Conciliación**, ni se muestra en el campo **Ampliar reservas** de la pestaña **Conciliación** del tablero Programación. 

Hay dos formas de reservar automáticamente a un miembro del equipo para un proyecto: directamente desde el tablero Programación, o bien agregando al miembro del equipo a la pestaña **Equipo**. 

## <a name="soft-book-from-the-schedule-board"></a>Reserva automática desde el tablero Programación
Complete los pasos siguientes para reservar automáticamente un recurso desde el tablero Programación. 

1. Abra el tablero Programación y en el panel **Requisitos de reserva**, seleccione la pestaña **Proyecto**.
2. Busque el proyecto para el que desee reservar automáticamente un recurso. Si hay un gran número de proyectos en la lista, seleccione el encabezado de la columna **Proyecto** y use el filtro para buscar uno o más proyectos.
3. Seleccione el proyecto y después arrástrelo y suéltelo en la cuadrícula de tiempo del recurso.
5. En el panel **Crear reserva de recursos**, ajuste la hora de inicio y de finalización, establezca el **Estado de reserva** en **Automática** y después establezca las horas. 
6. Haga clic en **Reservar**. El recurso ahora se muestra en la pestaña **Equipo** como recurso para el proyecto. En la vista **Miembros del equipo con nombre** verá las horas reservadas automáticamente en la columna **Horas reservadas automáticamente**.

> [!NOTE]
> Ahora puede asignar la reserva automática a las tareas en la pestaña **Programación**. En la pestaña **Conciliación**, el recurso muestra un déficit de reserva en relación con la asignación de tarea, ya que la pestaña **Conciliación** solo considera las reservas manuales. Puede usar la característica **Ampliar reservas** para reservar manualmente el recurso para eliminar el déficit de reservas manuales en comparación con las asignaciones de los recursos. Tendrá que cancelar manualmente la reserva automática para el recurso mediante **Mantener reservas**.

## <a name="soft-book-on-the-team-tab"></a>Reserva automática en la pestaña Equipo

Puede agregar miembros del equipo directamente en la pestaña **Equipo** y, a continuación cambiar su estado de reserva de **Manual** a **Automática** con **Mantener reservas**. Cuando agregue un miembro del equipo de esta manera, se convierte siempre en reserva manual a menos que se seleccione el método de asignación **Ninguno**.

Para usar este método, complete los pasos que se detallan a continuación.

1. En la página **Proyecto**, en la pestaña **Equipo**, haga clic en **Nuevo**.
2. Seleccione el recurso que se puede reservar, el rol y las fechas de inicio y finalización.
3. Seleccione un método de asignación distinto de **Ninguno**.
4. Seleccione **Guardar**. Verá el recurso en la cuadrícula y sus horas en la columna **Horas reservadas manualmente**.
5. Mantenga las reservas del recurso haciendo clic en **Mantener reservas**.
6. Cuando se abre el tablero Programación, expanda el recurso para mostrar sus reservas. Verá la reserva indicada como **Manual**.
7. Haga clic con el botón secundario en la reserva y, en **Cambiar estado**, seleccione **Reserva automática** \> **Automática**. El estado de la reserva es ahora **Automática**.
8. Después de cerrar el tablero Programación, verá que las horas del recurso se han movido de la columna **Horas reservadas manualmente** a **Horas reservadas automáticamente** en la pestaña **Equipo**, cuando vea la vista **Miembros del equipo con nombre**.

> [!NOTE]
> Cuando se utiliza **Mantener reservas** para cambiar el estado de **Manual** a **Automática**, si reserva manualmente un recurso en el equipo y después le asigna tareas, las asignaciones de tareas del recurso se mantendrán. Sin embargo, en la pestaña **Conciliación**, el recurso tendrá una deficiencia de reserva, ya que solo se consideran las reservas manuales al conciliar reservas frente a asignaciones. Puede usar la característica **Ampliar reservas** en la pestaña **Conciliación** para reservar manualmente el recurso y eliminar el déficit de reservas manuales en comparación con las asignaciones de los recursos. Tendrá que cancelar la reserva automática para el recurso mediante **Mantener reservas**.

Cuando esté listo para cambiar un recurso de miembro del equipo reservado automáticamente a miembro del equipo reservado manualmente, haga lo siguiente:

1. En el tablero Programación, expanda el recurso para mostrar sus reservas. Verá la reserva marcada como **Automática**.
2. Haga clic con el botón secundario en la reserva y, en **Cambiar estado**, seleccione **Reserva manual** \> **Manual**. El estado de la reserva es ahora **Manual**.
3. Después de cerrar el tablero Programación y volver al proyecto y abrir la pestaña **Equipo**, verá que las horas del recurso se han movido de la columna **Horas reservadas automáticamente** a la columna **Horas reservadas manualmente** en la pestaña **Equipo** en la vista **Miembros del equipo con nombre**. Si el recurso se asignó a tareas, ya no mostrarán un déficit de reserva en la pestaña **Conciliación**, pues sus reservas son manuales ahora.



[!INCLUDE[footer-include](../includes/footer-banner.md)]