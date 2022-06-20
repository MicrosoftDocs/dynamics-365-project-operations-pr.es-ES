---
title: Crear asignaciones de recursos
description: Este artículo proporciona información sobre cómo crear asignaciones de recursos genéricas y con nombre.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 31404fc35d72acb9ad791ef8a755f23108f528ad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933513"
---
# <a name="create-resource-assignments"></a>Crear asignaciones de recursos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


Una asignación de recurso es la asociación directa de un miembro del equipo del proyecto a una tarea de nodo hoja. En este artículo se proporciona información sobre las distintas formas de asignar recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un miembro del equipo genérico con la asignación de tareas


Al crear un miembro genérico del equipo mediante la asignación de tareas, crea un marcador de posición o un recurso genérico. Este recurso genérico describe las características del recurso con nombre en el que en definitiva desea trabajar en las tareas. A continuación, genere un requisito, o envíe una solicitud con el requisito, que se usará para buscar y reservar el recurso con nombre.

1. En la cuadrícula Programación de una tarea, seleccione el icono Recurso en la celda **Recurso**.
2. Escriba un nombre que sirva como nombre del recurso de marcador de posición. Por ejemplo, Administrador de programas.
3. Seleccione **Crear** y, en el campo **Creación rápida de miembro del equipo de proyecto**, defina el rol para el recurso genérico.
4. Asigne tareas, según sea necesario, a este recurso de marcador de posición seleccionando el recurso en el **Selector de recursos** para la tarea. Los recursos aparecen en **Miembros del equipo**.
5. Cuando haya terminado de asignar el recurso genérico, seleccione el recurso genérico en la pestaña **Equipo** y después seleccione **Generar requisito** para crear un requisito de recursos para el recurso genérico.
6. Seleccione **Reservar** para el recurso genérico, y entonces use el panel Programación para buscar y reservar un recurso real. También puede enviar el requisito para que lo satisfaga un administrador de recursos.
7. Cuando el recurso genérico se satisface por completo (el cumplimiento parcial de los requisitos del recurso no dará como resultado una asignación de recursos) con un recurso con nombre, el recurso genérico se elimina del equipo. Las asignaciones de tareas para el recurso genérico se asignan al recurso con nombre que cumplió con el requisito del recurso genérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Asignar un recurso con nombre de la lista de todos los recursos reservables

Puede usar el cuadro de búsqueda de **Selector de recursos** para buscar todos los recursos activos y asignarlos a cualquier tarea de nodo hoja. Los recursos asignados de esta manera se agregan al equipo sin ninguna reserva. Esto es similar a agregar un miembro del equipo y seleccionar **Ninguno** como método de asignación. El recurso se muestra en las pestañas **Equipo**, **Asignación de recursos** y **Conciliación** como un recurso solo con asignaciones y un déficit de reserva. Resérvelos si desea usar su disponibilidad.

1. Desde la cuadrícula de tareas, el panel o la escala de tiempo, navegue hasta la celda **Asignado a**.
2. En el cuadro de búsqueda, comience a escribir un nombre. Los resultados de búsqueda del nombre se muestran en el **Selector de recursos** en **Otros recursos**.
3. Seleccione el recurso que desea asignar a la tarea o seleccione el nombre del recurso en **Otros recursos del equipo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]