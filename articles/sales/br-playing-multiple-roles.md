---
title: Estimar los costes y las ventas de proyecto cuando un recurso que se puede reservar completa varios roles en un proyecto
description: En este tema se explica cómo usar las dimensiones de precios para admitir las estimaciones de precios y costes para un recurso que cumpla varios roles en un proyecto.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ef9765b7db1c6650fb0599bf5fb4b4b6304be69
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013687"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimar los costes y las ventas de proyecto cuando un recurso que se puede reservar completa varios roles en un proyecto 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos en existencias, implementación Lite - trato a facturación proforma y Project Operations para escenarios basados en existencias/producción_ 

Las empresas basadas en proyectos a menudo tienen la necesidad de que un desempeñe varios roles en un proyecto. Cada rol puede tener un precio y un coste diferentes. Esto significa que el tiempo del mismo recurso en un proyecto podría obtener una estimación financiera diferente según la factura y las tarifas de coste para cada rol. Puede configurar los valores en el registro de miembro del equipo para el recurso nombrado con diferentes reemplazos en cada una de las tareas a las que está asignado el miembro del equipo.

El siguiente ejemplo le muestra cómo el simple reemplazo de un valor permite que un recurso tenga varios roles en un proyecto con diferentes costes y tasas de facturación.

## <a name="create-tasks"></a>Crear tareas
Para crear tareas, debe agregar tareas, así como tareas de resumen, después de lo cual debe asignar la tarea antes de agregar la duración de la tarea. 

### <a name="add-tasks-and-summary-tasks"></a>Agregar tareas y tareas de resumen
Para agregar una tarea, complete los pasos que se indican a continuación.

1. Vaya a **Proyectos** y abra el proyecto al que desea agregar tareas.
2. Seleccione **Agregar nueva tarea**. Proporcione un nombre a la tarea y presione **Entrar**.
3. Escriba otro nombre de tarea y presione **Entrar**. Repita esto hasta que tenga una lista completa de tareas.
3. Para aplicar sangría debajo de las tareas de **Resumen**, seleccione los tres puntos verticales junto al nombre de la tarea y, a continuación, **Crear subtarea**. 

  > [!TIP]
  > Para seleccionar más de una tarea, seleccione una tarea, mantenga presionada la tecla **Ctrl** y luego seleccione otra tarea.
  >
  > También puede elegir **Promocionar subtarea** para mover tareas desde debajo de las tareas de **Resumen**.

### <a name="assign-tasks"></a>Asignar tareas

Para asignar tareas, complete los siguientes pasos.

1. En la columna **Asignado a** para una tarea, seleccione el icono de persona.
2. Elija un miembro del equipo de la lista o escriba texto para buscar un nombre.

### <a name="add-task-duration-and-columns"></a>Agregar la duración y las columnas de la tarea

A menudo, es más sencillo comenzar a construir su proyecto con duración. Para agregar una duración de tarea, complete los pasos que se indican a continuación.

1. En la columna **Duración** para una tarea, escriba el número de días que cree que se tardará en completar la tarea. Si desea usar una unidad de tiempo diferente, escriba un número más la palabra **horas**, **semanas** o **meses**.
2. Si desea que su tarea aparezca como un hito en forma de diamante en la vista **Escala de tiempo**, en la columna **Duración**, introduzca **0 días**.
3. Presione **Entrar** para ir al campo **Duración** de la siguiente tareas y continúe introduciendo duraciones.

  > [!NOTE]
  > No puede introducir una duración para tareas de resumen.

Puede agregar columnas a su proyecto para proporcionar más detalles. Para ello, seleccione **Agregar columna**. 

Para obtener más información, consulte [Crear un proyecto](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar el rol y la unidad organizativa para un miembro de equipo de proyecto genérico
Complete los siguientes pasos para configurar un rol y una unidad organizativa para un miembro de equipo genérico.

1. En la página **Tareas**, seleccione la fila **Tarea** para la **Tarea A**. 
2. En **Asignado a**, seleccione **Agregar recurso genérico**. Se abrirá la página **Creación rápida de miembros del equipo**.
3. En la página **Creación rápida de miembros del equipo**, especifique los atributos del miembro del equipo genérico que puede realizar esta tarea.
4. Seleccione el rol y la unidad organizativa apropiada y luego seleccione **Guardar y cerrar**. Se crea un miembro del equipo genérico y se asigna a esta tarea. 
5. Repita los pasos del 1 al 4 para la **Tarea B**. Sin embargo, la **Tarea B** debe tener un rol y una unidad organizativa asignados para el miembro del equipo genérico diferentes a los de la **Tarea A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Configurar el rol y la unidad organizativa para una tarea de proyecto
Complete los siguientes pasos para configurar un rol y una unidad organizativa para una tarea.

1. Después de crear la **Tarea A**, seleccione la tarea y luego seleccione el icono **i** para abrir el panel **Detalles de la tarea**. 
2. En el panel **Detalles de la tarea**, desplácese hasta la parte inferior y seleccione **Ver detalles** para abrir la página **Detalles de la tarea**.
3. En la página **Detalles de la tarea**, en **Rol** y **Unidad organizativa**, agregue los valores necesarios para realizar esta tarea para el recurso. 

  > [!NOTE]
  > Si completa este escenario utilizando los datos de demostración de Project Operations, seleccione **Líder de consultoría** para el rol y **Fabrikam US** como la unidad organizativa.

4. Seleccione la **Tarea B** y, a continuación, seleccione la tarea.
5. Seleccione el icono **i** para abrir el panel **Detalles de la tarea**. 
6. En el panel **Detalles de la tarea**, desplácese hasta la parte inferior y seleccione **Ver detalles** para abrir la página **Detalles de la tarea**.
7. En la página **Detalles de la tarea**, en **Rol** y **Unidad organizativa**, agregue los valores necesarios de un recurso que realizaría esta tarea. Los valores de **Rol** y **Unidad organizativa** para la **Tarea B** deben ser diferentes de los de la **Tarea A**. 

  > [!NOTE]
  > Si completa este escenario utilizando los datos de demostración de Project Operations, seleccione **Técnico de red** para el rol y **Fabrikam US** como la unidad organizativa.

8. Seleccione y cierre la página **Detalles de la tarea**. 

## <a name="team-member-and-estimates-behavior"></a>Miembro del equipo y comportamiento de estimaciones 
Para comprender el comportamiento de la cuadrícula **Miembro del equipo** y las estimaciones, complete los siguientes pasos.

1. En la cuadrícula **Miembro del equipo**, seleccione los dos miembros genéricos del equipo y, a continuación, **Generar requisitos**. Esto generará los requisitos de recursos. 
2. Seleccione la fila del miembro del equipo para **Jefe de consultoría** y, a continuación, **Reservar**. El tablero de programación se abre con una lista de recursos. Seleccione un recurso y, a continuación, **Reservar** para reservar el recurso para ese requisito.
3. Seleccione la fila del miembro del equipo para **Técnico de red** y, a continuación, **Reservar**. El tablero de programación se abre con una lista de recursos. Seleccione el mismo recurso que arriba y, a continuación, **Reservar** para reservar el recurso para ese requisito.

### <a name="team-member-grid"></a>Cuadrícula Miembro del equipo 

En la cuadrícula **Miembro del equipo**, se eliminan los dos registros genéricos de miembros del equipo y se reemplazan por un solo recurso. Hay un conjunto de valores para ese recurso, que son un conjunto predeterminado de valores para **Rol** y **Unidad organizativa**.

Cuando expande la fila para ese registro de miembro del equipo, puede ver asignaciones distintas en el registro de miembro del equipo para ambas tareas. Cada fila de asignación tiene valores específicos de tarea para **Rol** y **Unidad organizativa**. 

### <a name="estimates-grid"></a>Cuadrícula Estimaciones 

En la cuadrícula **Estimaciones**, ambas asignaciones para el mismo recurso tienen un precio diferente. Se asignan precios a la asignación para el recurso en la **Tarea** A mediante el valor de atributo **Rol** de **Jefe de consultoría**. Se asignan precios a la asignación para el mismo recurso en la **Tarea B** mediante el valor de atributo **Rol** de **Técnico de red**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]