---
title: Crear asignaciones de recursos
description: Este artículo proporciona información sobre cómo crear asignaciones de recursos genéricas y con nombre.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812015"
---
# <a name="create-resource-assignments"></a>Crear asignaciones de recursos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


Una asignación de recurso es la asociación directa de un miembro del equipo del proyecto a una tarea de nodo hoja. En este artículo se proporciona información sobre las distintas formas de asignar recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un miembro del equipo genérico con la asignación de tareas


Al crear un miembro genérico del equipo mediante la asignación de tareas, crea un marcador de posición o un recurso genérico. Este recurso genérico describe las características del recurso con nombre que en definitiva desea para trabajar en las tareas. A continuación, genere un requisito, o envíe una solicitud con el requisito, que se usará para buscar y reservar el recurso con nombre.

1. En la cuadrícula Programación de una tarea, seleccione el icono Recurso en la celda **Recurso**.
2. Escriba un nombre que sirva como nombre del recurso de marcador de posición. Por ejemplo, Administrador de programas.
3. Seleccione **Crear** y, en el campo **Creación rápida de miembro del equipo de proyecto**, defina el rol para el recurso genérico.
4. Asigne tareas, según sea necesario, a este recurso de marcador de posición seleccionando el recurso en el **Selector de recursos** para la tarea. Los recursos aparecen en **Miembros del equipo**.
5. Cuando haya terminado de asignar el recurso genérico, seleccione el recurso genérico en la pestaña **Equipo** y después seleccione **Generar requisito** para crear un requisito de recursos para el recurso genérico.
6. Seleccione **Reservar** para el recurso genérico, y entonces use el panel Programación para buscar y reservar un recurso real. También puede enviar el requisito para que lo satisfaga un administrador de recursos.
7. Cuando se completa el recurso genérico totalmente con un recurso con nombre, el recurso genérico se quita del eqiupo. (El cumplimiento parcial del requisito de recursos no dará como resultado una asignación de recursos). Las asignaciones de tareas para el recurso genérico se asignan al recurso con nombre que cumplió con el requisito de recursos del recurso genérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Asignar un recurso con nombre de la lista de todos los recursos reservables

Puede usar el cuadro de búsqueda de **Selector de recursos** para buscar todos los recursos activos y asignarlos a cualquier tarea de nodo hoja. Los recursos asignados de esta manera se agregan al equipo sin ninguna reserva. Esto es similar a agregar un miembro del equipo y seleccionar **Ninguno** como método de asignación. El recurso se muestra en las pestañas **Equipo**, **Asignación de recursos** y **Conciliación** como un recurso solo con asignaciones y un déficit de reserva. Resérvelos si desea usar su disponibilidad.

1. Desde la cuadrícula de tareas, el panel o la escala de tiempo, navegue hasta la celda **Asignado a**.
2. En el cuadro de búsqueda, comience a escribir un nombre. Los resultados de búsqueda del nombre se muestran en el **Selector de recursos** en **Otros recursos**.
3. Seleccione el recurso que desea asignar a la tarea o seleccione el nombre del recurso en **Otros recursos del equipo**.

## <a name="editing-resource-assignment-contours"></a>Edición de contornos de asignación de recursos

De forma predeterminada, cuando los recursos se asignan a una tarea en el cronograma, su esfuerzo se distribuye linealmente a cada recurso, según las horas de trabajo de ese recurso y el modo de cronograma del proyecto. Un administrador de proyectos puede usar la cuadrícula de asignación de recursos para refinar las estimaciones de esfuerzo de cada recurso que se asigna a una o varias tareas en las diferentes escalas de tiempo. Esta característica ayuda a los gerentes de proyectos a producir estimaciones de costos y ventas más precisas, que se basan en los contornos de asignación de recursos que se generan cuando se asigna un recurso a una tarea. Además, los administradores de proyectos pueden reflejar más fácilmente la demanda de recursos necesaria para crear la demanda en un requisito de recursos.

### <a name="navigation"></a>Navigation

Para acceder a la cuadrícula de edición de contornos, el administrador del proyecto primero selecciona la pestaña **Tareas** en la página principal del proyecto y luego selecciona la pestaña **Asignaciones**.

![Pestaña Asignaciones en la pestaña Tareas de la página principal del proyecto.](media/AssignmentGrid.png)

La cuadrícula admite dos métodos de agrupación: **agrupar por recurso** y **agrupar por tarea**. A diferencia de la vista de cuadrícula, las columnas no se pueden configurar. Las únicas columnas visibles son **Asignado a**, **Nombre de la tarea**, **Inicio de la tarea**, **Terminación de la tarea** y **Esfuerzo de la tarea**.

Cuando la cuadrícula se renderiza inicialmente, comienza en el primer contorno de asignación. Si su horario no contiene ninguna tarea que requiera esfuerzo, la cuadrícula estará en blanco y no generará nada.

![Cuadrícula de asignación en blanco.](media/emptyassignmentgrid.png)

Si desea ver sus contornos y diferentes escalas de tiempo, también están disponibles la cuadrícula de asignación de recursos de solo lectura y la cuadrícula de reconciliación de recursos.

### <a name="resource-calendars"></a>Calendarios de recursos

La capacidad de editar un contorno para un día específico se rige por los días laborables del recurso, tal como se refleja en su calendario. Si una celda está deshabilitada para un recurso determinado, ese recurso no tiene días hábiles durante ese período.

Los contornos de un recurso pueden extenderse más allá de las fechas de inicio y finalización actuales de la tarea asignada. Si se actualiza un contorno para que sea posterior a la última fecha de finalización de una tarea o la fecha de inicio más temprana de una tarea, la fecha de finalización o la fecha de inicio de la tarea se cambiarán según corresponda. Sin embargo, si se actualiza un contorno para que sea anterior a la fecha de inicio de una tarea que está vinculada a un predecesor, la actualización fallará porque la asignación activará el inicio de la tarea antes de que se complete su predecesor, y ese comportamiento no es actualmente soportado.

### <a name="co-authoring"></a>Creación conjunta

Los cambios en la cuadrícula de asignación de recursos se reflejan automáticamente en las vistas asociadas, incluidas las vistas de gráfico, escala de tiempo, tablero y cuadrícula. Si varios usuarios están revisando el proyecto al mismo tiempo, cualquier cambio que haga un usuario se reflejará en la cuadrícula. Por el contrario, cualquier cambio que se realice en la cuadrícula de asignación de recursos se mostrará a todos los demás usuarios que estén viendo el proyecto en la misma sesión.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
