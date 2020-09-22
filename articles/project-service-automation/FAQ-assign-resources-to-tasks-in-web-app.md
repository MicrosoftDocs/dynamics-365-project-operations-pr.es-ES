---
title: ¿Cómo asigno un recurso que se puede reservar a una tarea en la aplicación web?
description: Información general de las distintas maneras en que puede asignar recursos reservables.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756102"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>¿Cómo asignar un recurso que se puede reservar a una tarea en la aplicación web (aplicación Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Hay dos formas de asignar un recurso a una tarea en Project Service. Puede reservar un recurso como integrante del equipo y después asignarlo a una tarea. O puede crear un miembro del equipo genérico con la asignación de roles en tareas, generar un equipo y, a continuación satisfacer los requisitos de apoyo con un recurso con nombre.

Tenga en cuenta que si desea asignar un recurso que se puede reservar a una tarea, el integrante del equipo del recurso que se puede reservar debe tener suficientes reservas disponibles. El estado de la reserva debe ser Tipo de confirmación - Reserva manual y Estado confirmado. Si no hay reservas suficientes para el recurso, Project Service quita la asignación y muestra el siguiente mensaje de error:

*No se puede asignar recurso a tarea - los siguientes recursos no tienen suficientes horas reservadas para el proyecto*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reserve un recurso como integrante del equipo y después asigne el recurso a una tarea.

Con este método agrega un recurso al equipo del proyecto y después asigna tareas al recurso en el calendario del proyecto. Esta es la forma de hacerlo:
1.  En la cuadrícula de miembros del equipo, agregue un nuevo miembro del equipo seleccionando **Nuevo**.
2.  En la pantalla de creación rápida de Miembros del equipo, seleccione el nombre del recurso que se puede reservar y defina un rol.
3.  Seleccione las fechas **Desde** y **Hasta**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla de la adición de un miembro del equipo](media/FAQ-Resources-to-Tasks2-1.png "Captura de pantalla de la adición de un miembro del equipo")
 
4.  Seleccione uno de los siguientes métodos de asignación para reservar el recurso:
    - **Plena capacidad** reserva la capacidad completa del recurso para fechas especificadas de inicio y fin.
    - **Porcentaje de capacidad** reserva el recurso para un porcentaje de capacidad del recurso para las fechas especificadas de inicio y fin.
    - **Por horas: distribuir equitativamente** reserva el recurso para un número especificado de horas, distribuyéndolo uniformemente por día a lo largo de las fechas de inicio y fin especificadas.
    - **Por horas: cargo por adelantado** reserva el recurso para un número especificado de horas, cargando por adelantado las horas diarias a lo largo de las fechas de inicio y fin especificadas.

    No seleccione **Ninguno** porque agrega el recurso al equipo, pero no crea ninguna reserva que absorba la capacidad del recurso.
5.  Seleccione **Guardar**.

    Tenga en cuenta que las horas de la reserva deben ser suficientes para satisfacer las horas de esfuerzo y los intervalos de fechas de las tareas a las que asigna este recurso. Si no están alineados, no puede asignar el recurso a la tarea.

6.  En la estructura de descomposición del trabajo (WBS) para la tarea, haga clic en la lista desplegable de celdas del recurso. A continuación: 

    1. Seleccione **Agregar**.
    2. Seleccione la lista desplegable en **Recursos** y seleccione el integrante del equipo que agregó anteriormente.
    3. Seleccione **Aceptar**. Ahora el integrante del equipo está asignado a la tarea.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla de la adición de recursos con WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de pantalla de la adición de recursos con WBS")
 
En la cuadrícula de miembros del equipo, verá el agregado de las horas asignadas del recurso en Horas asignadas. Será menor o igual que las horas reservadas para el recurso. 

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de horas asignadas para un recurso](media/FAQ-Resources-to-Tasks2-3.png "Captura de pantalla de horas asignadas para un recurso")
 
Si la tarea que intenta asignar al recurso se inicia después de la fecha de finalización de las reservas de recursos, el recurso no aparecerá en la lista desplegable.

Tenga en cuenta que puede asignar un recurso a más horas que las horas reservadas si el recurso tiene capacidad restante sin asignar. En este caso el recurso solo se asignará parcialmente a sus reservas. Puede ver estas horas restantes de tarea no asignadas agregando la columna Horas sin dotación de personal a la estructura de descomposición del trabajo.

Si hay recursos asignados a sus horas reservadas (sus horas reservadas son igual a las horas asignadas), verá el siguiente mensaje de error al intentar asignarles aún más tareas:

*No se puede asignar recurso a tarea - los siguientes recursos no tienen suficientes horas reservadas para el proyecto.*

Además, el integrante del equipo jefe de proyecto predeterminado que se agrega al equipo cuando se crea el proyecto se agrega sin reservas y no se puede asignar a ninguna tarea. No aparecerá en la lista desplegable de recursos para las tareas.

Si desea asignar este recurso, debe quitarlo del equipo y después volver a agregarlo con un método de asignación distinto de Ninguno. La razón por la que se agregan al equipo cuando se crea el proyecto es que un proyecto tiene al menos un aprobador de proyecto de forma predeterminada.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Cree un miembro del equipo genérico con la asignación de roles en tareas

Este método garantiza que los recursos tienen reservas suficientes para las tareas. Primero, cree un marcador de posición o un recurso genérico que describa las características del recurso con nombre en el que en definitiva desea trabajar en las tareas generando un equipo después de asignar roles a tareas. Esta es la forma de hacerlo:

1. En la estructura de descomposición del trabajo, seleccione una tarea.
2. Seleccione el icono desplegable **Rol asignado** en la celda del recurso.
3. Seleccione el desplegable **Rol** y seleccione el rol para el recurso genérico.
4. Seleccione **Aceptar**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla del uso de WBS para agregar recurso](media/FAQ-Resources-to-Tasks2-4.png "Captura de pantalla del uso de WBS para agregar recurso")
 
Una vez finalizada la asignación de roles a las tareas en la WBS, seleccione **Generar equipo del proyecto**. Project Service crea el número mínimo de integrantes del equipo genéricos basados en roles, unidades organizativas de recursos y el calendario de proyecto agregando las asignaciones de tareas.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de la generación de equipo de proyecto](media/FAQ-Resources-to-Tasks2-5.png "Captura de pantalla de la generación de equipo de proyecto")
 
En la cuadrícula Miembro del equipo, verá recursos del tipo de Recurso genérico con el rol y el nombre del puesto. Si se necesitan dos recursos para que un rol complete el trabajo, la característica Generar equipo crea dos integrantes del equipo y usa el nombre del puesto para diferenciarlos.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de la adición de dos recursos genéricos](media/FAQ-Resources-to-Tasks2-6.png "Captura de pantalla de la adición de dos recursos genéricos")
 
Puede abrir el requisitos de recursos de apoyo para el integrante del equipo genérico seleccionando el vínculo en Requisito de recursos.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de la apertura de requisito de recursos de apoyo](media/FAQ-Resources-to-Tasks2-7.png "Captura de pantalla de la apertura de requisito de recursos de apoyo")

Seleccione **Reservar** para el recurso genérico, y entonces podrá usar el tablero de programación para buscar y reservar un recurso real. También puede enviar el requisito para que lo satisfaga un administrador de recursos seleccionando **Mostrar la solicitud**.

Cuando el recurso genérico se satisfaga con un recurso con nombre, se quitará el recurso genérico del equipo y las asignaciones de tarea para el recurso genérico se asignarán al recurso con nombre que satisfizo el requisito del recurso genérico.
 

