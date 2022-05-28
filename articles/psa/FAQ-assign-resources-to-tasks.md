---
title: Asignar un recurso a una tarea
description: En este tema se proporciona información sobre cómo asignar recursos a tareas.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 42363814a8ef395652ed8f8a79d0e6f02f2f5177
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586181"
---
# <a name="assign-a-resource-to-a-task"></a>Asignar un recurso a una tarea

[!include [banner](../includes/psa-now-project-operations.md)]

Hay tres formas de asignar un recurso a una tarea en Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservar un recurso como miembro del equipo y después asignar el recurso a una tarea.

Puede agregar un recurso al equipo del proyecto y después asignar el recurso a tareas en la programación del proyecto.

1. En la pestaña **Miembro del equipo**, agregue un nuevo miembro del equipo seleccionando **Nuevo**. 

2. Se abrirá el panel **Creación rápida de miembros del equipo**, donde podrá seleccionar el nombre del recurso que se puede reservar y definir un rol. 

    Seleccione uno de los siguientes métodos de asignación para la reservar del recurso:

    - **Plena capacidad** reserva la capacidad completa del recurso para fechas especificadas de inicio y fin.
    - **Porcentaje de capacidad** reserva el recurso para un porcentaje de capacidad del recurso para las fechas especificadas de inicio y fin.
    - **Por horas: distribuir equitativamente** reserva el recurso durante un número específico de horas de manera uniforme por día durante el periodo especificado entre las fechas de inicio y finalización.
    - **Por horas: cargo por adelantado** reserva el recurso para un número especificado de horas, cargando por adelantado las horas diarias a lo largo de las fechas de inicio y fin especificadas.
    - **Ninguno** agrega el recurso al equipo, pero no crea ninguna reserva que absorba su capacidad.

3. En la cuadrícula **Programación** de una tarea, seleccione el icono **Recurso** en la celda de recursos y después, en **Miembros del equipo**, seleccione el miembro del equipo que acaba de agregar. 

> [!NOTE]
> En las pestañas **Miembro del equipo** y **Conciliación**, el recurso muestra las horas reservadas y las horas asignadas. Las horas deben ser las mismas, pero no necesariamente, ya que las reservas y las asignaciones no están emparejadas firmemente. La pestaña **Conciliación** proporciona detalles cuando son diferentes, como cuando se asigna un recurso por más horas de las que se ha reservado. Si es necesario, puede corregir la información ampliando las reservas del recurso, o bien modificando la asignación.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un miembro del equipo genérico con la asignación de tareas

Cuando cree un miembro del equipo genérico mediante la asignación de tareas, cree un marcador de posición o un recurso genérico que describa las características del recurso con nombre que desea que trabaje en las tareas. A continuación, genere un requisito (o envíe una solicitud con el requisito) que se usará para buscar y reservar el recurso con nombre.

1. En la cuadrícula **Programación** de una tarea, seleccione el icono **Recurso** en la celda del recurso.

2. Escriba un nombre que sirva como nombre del recurso de marcador de posición. Por ejemplo, Administrador de programas.

3. Seleccione **Crear** y, en el campo **Creación rápida de miembro del equipo de proyecto**, defina el rol para el recurso genérico.

4. Puede continuar asignando tareas a este recurso de marcador de posición seleccionando el recurso en el **Selector de recursos** para la tarea. Aparecen en **Miembros del equipo**.

5. Cuando termine de asignar el recurso genérico, seleccione el recurso genérico en la pestaña **Equipo** y después seleccione **Generar requisito** para crear un requisito de recursos para el recurso genérico.

6. Seleccione **Reservar** para el recurso genérico. Puede usar posteriormente el Tablero de programación para buscar y reservar un recurso real. También puede enviar el requisito para que lo satisfaga un administrador de recursos.

7. Cuando el recurso genérico se satisfaga con un recurso con nombre, se quitará el recurso genérico del equipo y las asignaciones de tarea para el recurso genérico se asignarán al recurso con nombre que satisfizo el requisito del recurso genérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Asignar un recurso con nombre de la lista de todos los recursos reservables

Puede usar el cuadro de búsqueda en el **Selector de recursos** para buscar todos los recursos reservables y asignarlos a una tarea.

Los recursos asignados de esta manera se agregan al equipo sin ninguna reserva. Esto es similar a agregar un miembro del equipo y seleccionar Ninguno como método de asignación. El recurso se muestra en las pestañas **Equipo** y **Conciliación** como recursos solo con asignaciones y un déficit de reserva. Resérvelos si desea usar su disponibilidad.

1. En la cuadrícula **Programación** de una tarea, seleccione el icono **Recurso** en la celda del recurso.

2. Empiece a escribir un nombre. Los resultados de búsqueda del nombre se muestran en el **Selector de recursos** en **Otros recursos**.

3. Seleccione el recurso que desee asignar a la tarea.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
