---
title: Crear una reserva de proyecto desde el tablero Programación
description: En este tema se proporciona información sobre cómo crear una reserva de proyecto desde el tablero Programación.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122319"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Crear una reserva de proyecto desde el tablero Programación

Puede reservar un recurso para un proyecto directamente desde la pestaña **Equipo** del proyecto o generando un requisito de recursos desde una asignación genérica de miembro del equipo y después cumpliendo el requisito generado mediante un miembro del equipo de proyecto.

También puede reservar un recurso para un proyecto directamente desde el tablero Programación. Esto se puede hacer de tres maneras:

- **Reservar a partir de un requisito de recurso generado**: puede generar un requisito de recursos tras crear un recurso genérico y asignar tareas en un proyecto.

- **Reservar desde el requisito principal:** los requisitos principales aparecen en el tablero Programación en la pestaña **Proyecto**. 

- **Reservar a partir de un nuevo requisito de recurso:** puede crear un requisito de recursos desde cero y asociarlo a un proyecto. En el tablero Programación, el requisito de recurso aparece en la pestaña **Requisitos abiertos**.

## <a name="book-from-a-generated-resource-requirement"></a>Reserve a partir de un requisito de recurso generado

Puede crear un recurso genérico y asignarlo a una o varias tareas en un proyecto. A continuación, puede genere un requisito de recurso a partir del miembro de equipo genérico. 

1.  En el tablero Programación, este recurso aparecerá en la pestaña **Requisitos abiertos**. Puede que tenga que usar filtros de columna en la cuadrícula si tiene muchos requisitos abiertos. 

    ![Pestaña Abrir requisitos en el tablero de programación](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de pantalla de la tabla de reservas y asignaciones")

2. Seleccione el requisito. La pestaña **Buscar disponibilidad** aparecerá en la parte superior de fila seleccionada.
 
3. Al seleccionar la pestaña, se abrirá el modo Asistente de programación del tablero Programación y se filtrarán los recursos disponibles que cumplen los requisitos de recurso. A continuación, podrá reservar un recurso.

4. También puede arrastrar y colocar fila seleccionada desde la parte inferior del tablero Programación hasta una celda de recurso en la cuadrícula superior. Cuando la coloca, se abre el panel **Crear reserva de recursos** a la derecha.

    Al seleccionar **Reservar** se reserva el recurso para el equipo del proyecto.

![Panel Crear reserva de recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Reserva desde el requisito principal

Al crear un proyecto en Project Service se crea automáticamente un requisito de recurso llamado el requisito principal. Se trata de un requisito vacío que se usa para reservar rápidamente un recurso con el tablero Programación sin generar ningún requisito ni crear uno desde cero. Puesto que el requisito está vacío, deberá especificar fechas así como el método y las horas de asignación si es necesario. 

1. Para reservar un recurso con el Requisito principal, en el tablero Programación, seleccione la pestaña **Proyecto**. Quizá deba usar el filtro de columna en la columna **Proyecto** si tiene muchos proyectos.

   ![Filtros de columna del tablero de programación](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de pantalla de la tabla de reservas y asignaciones")

2. Seleccione el requisito que solo tiene el nombre del proyecto como nombre y tiene una duración de cero (0).

3. Seleccione la pestaña **Buscar disponibilidad** que aparece en la fila. Esto pone el tablero Programación en el modo Asistente de programación y muestra los recursos disponibles que se pueden reservar para el proyecto.

4. Dado que un **requisito principal** es un requisito vacío con duración de cero (0), necesitará establecer la duración en el panel **Crear reserva de recursos** al seleccionar y reservar un recurso.

5. También puede seleccionar el **Requisito principal del proyecto** en la parte inferior del tablero Programación y arrastrarlo y colocarlo sobre un recurso para reservarlo.
 
    Dado que el **Requisito principal** es un requisito vacío con duración de cero (0), necesitará establecer la duración en el panel **Crear reserva de recursos** cuando seleccione y reserve un recurso.
 
    Cuando se reserva un recurso con el **Requisito principal** en el tablero Programación, se agrega al equipo del proyecto sin ninguna asignación.
 
## <a name="book-from-a-new-resource-requirement"></a>Reservar a partir de un nuevo requisito de recurso
Complete los pasos siguientes para reservar desde un requisito de nuevo recurso. 

1. Vaya a **Requisitos de recursos** y después seleccione **Nuevo** para crear un nuevo requisito de recursos.

2. En la pestaña **Proyecto**, seleccione un proyecto para asociar el requisito al proyecto.
 
    En el tablero Programación, este nuevo requisito se muestra como un **Requisito abierto** que se puede rellenar.

3. Reserve el recurso para agregarlo al equipo del proyecto.

4. Ahora que el recurso está reservado, debe asignar tareas manualmente.

