---
title: ¿Cómo "reservo automáticamente" recursos en la versión 2.x de la aplicación?
description: En este artículo se describe cómo reservar automáticamente integrantes del equipo del proyecto con Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 413783d2386cccd98cfe216a7c7300a5b7f771ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992922"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>¿Cómo "reservo automáticamente" recursos en la aplicación web (aplicación Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Puede programar de manera provisional o “automáticamente” un recurso en un equipo del proyecto para mostrar el plan para asignar el recurso a un proyecto. Las reservas automáticas no consumen la capacidad disponible de un recurso. Los integrantes del equipo reservados automáticamente no se pueden asignar a tareas de proyecto. Solo los recursos con el estado Reservado manualmente o el Tipo de confirmación Confirmado pueden asignarse a tareas (suponiendo que tienen suficientes horas de reserva manual para cubrir el esfuerzo de asignación).

Los integrantes del equipo del proyecto reservados automáticamente aparecen en la cuadrícula Miembro del equipo con sus horas de reserva automática en la columna Reserva automática. También aparecen en el tablero de programación. Una vez más no indican ningún consumo de capacidad, ya que la reserva automática no consume capacidad de un recurso.

Hay tres formas de reservar automáticamente a un integrante del equipo en un proyecto con Project Service versión 2.x. Puede reservar automáticamente con el tablero de programación, usar la característica Mantener reservas o crear un recurso genérico. Estos métodos se describen a continuación.

## <a name="soft-book-with-the-schedule-board"></a>Reserva automática con el tablero de programación

Para reservar automáticamente con el tablero de programación, siga este procedimiento: 
1. Abrir el tablero de programación.
2. Seleccione la pestaña Proyecto en el panel inferior Requisitos de reserva del tablero de programación.
3. Busque el proyecto para el que desee reservar automáticamente un recurso. Si tiene muchos proyectos, haga clic en el encabezado de la columna Proyecto y use el filtro para encontrar el proyecto.
4. Haga clic en el proyecto, arrástrelo y colóquelo en la cuadrícula de tiempo del recurso.
5. Esto abre el panel Crear reserva de recursos a la derecha. Ajuste la fecha de inicio y de finalización, seleccione el Estado de reserva como Automático y establezca las horas. 
6. Haga clic en Reservar.
7. Al regresar al proyecto, el recurso se muestra ahora como integrante del equipo con las horas reservadas automáticamente en la columna Reserva automática.

Tenga en cuenta que no puede asignarlas a tareas en la estructura de descomposición del trabajo (WBS) ya que los recursos deben ser reservados de forma manual en el equipo al que se asignarán.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Reserva automática mediante la característica Mantener reservas

Para reservar automáticamente con Mantener reservas, siga este procedimiento:
1. En la cuadrícula de miembro del equipo, haga clic en Nuevo.
2. Seleccione el recurso reservable, rol, inicio/fin.
3. Seleccione un método de asignación distinto de Ninguno:
- Plena capacidad
- Porcentaje de capacidad
- Por horas: distribuir equitativamente
- Por horas: cargo por adelantado
4. Haga clic en Guardar. Verá el recurso en la cuadrícula del equipo y sus horas indicadas como Manuales.
5. Mantenga las reservas del recurso haciendo clic en Mantener reservas.
6. Cuando se abre el tablero de programación, expanda el recurso para mostrar sus reservas. Verá la reserva indicada como Manual.
7. Haga clic con el botón secundario en la reserva, en Cambiar estado, seleccione Reserva automática y después Automática. El estado de la reserva es ahora Automática.
8. Después de cerrar el tablero de programación, verá que las horas para el recurso han cambiado de Manual a Automática en la cuadrícula de miembros del equipo.
Tenga en cuenta que si reserva manualmente un recurso en el equipo y después les asigna tareas en WBS, cuando use Mantener reservas para cambiar el estado de Manual a Automático, se quitarán las asignaciones de las tareas para ese recurso, ya que solo pueden asignarse a tareas los recursos reservados manualmente.

## <a name="soft-book-by-creating-a-generic-resource"></a>Reservar automáticamente creando un recurso genérico

Puede crear una reserva automática generando un integrante del equipo de recurso genérico, cumpliendo el tablero de programación o Solicitud de recursos y cambiando el tipo durante la reserva.
Para ello, siga este procedimiento:

1. En la WBS del proyecto, asigne roles a tareas para las que desea generar integrantes del equipo genérico.
2. Haga clic en Generar equipo del proyecto.
3. En la cuadrícula de miembros del equipo de proyecto, seleccione el recurso genérico y haga clic en Reservar.
4. En el tablero de programación, seleccione el recurso que desea reservar.
5. En el panel Crear reserva de recursos del tablero de programación, cambie el Estado de reserva a Automática.
6. Haga clic en Reservar o en Reservar y salir.

Después de cerrar el tablero de programación, verá el recurso seleccionado agregado al equipo con horas reservadas automáticamente, así como horas asignadas. También verá que el recurso genérico permanece en el equipo como indicador de que las tareas están asignadas a un miembro del equipo reservado automáticamente.

Cuando esté listo para cambiar un recurso de miembro del equipo reservado automáticamente a miembro del equipo reservado manualmente para poder asignarle a tareas, haga lo siguiente:

1. Seleccione ese recurso y haga clic en Mantener reservas.
2. Cuando se abre el tablero de programación, expanda el recurso para mostrar sus reservas. Verá la reserva marcada como Automática.
3. Haga clic con el botón secundario en la reserva, en Cambiar estado, seleccione Reserva manual y después Manual. El estado de la reserva es ahora Manual.
4. Después de cerrar el tablero de programación, verá que las horas para el recurso han cambiado de Automática a Manual en la cuadrícula de miembros del equipo. Ahora puede asignar el recurso a tareas (siempre que haya alineación entre las horas reservadas manualmente y las horas de esfuerzo de la tarea para asignación). Tenga en cuenta que si siguió los pasos de cumplimiento de recursos genéricos en el elemento #3 de arriba, cuando cambie el estado del recurso reservado automáticamente a manual, se quitará el integrante del equipo genérico del equipo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]