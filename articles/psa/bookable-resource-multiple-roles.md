---
title: Estime las ventas y los costes del proyecto cuando un recurso que se puede reservar cumple varios roles en un proyecto
description: En este tema se proporciona información sobre cómo se pueden usar las dimensiones de precios para respaldar los precios y costes de un recurso que cumple varios roles en un proyecto.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085200"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Estime las ventas y los costes del proyecto cuando un recurso que se puede reservar cumple varios roles en un proyecto 

Las empresas basadas en proyectos a menudo necesitan un recurso para desempeñar varios roles en un proyecto. Cada uno de estos roles podría tener un precio y un coste diferente, lo que significa que el tiempo del mismo recurso en el proyecto podría obtener una estimación financiera diferente según las tasas de facturación y coste para cada uno de los roles. Project Service Automation permite configurar los valores en el registro del miembro del equipo para el recurso nombrado y permite diferentes anulaciones en cada una de las tareas a las que está asignado el miembro del equipo.

El siguiente ejemplo explica cómo la simple anulación de este valor permite que un recurso tenga varios roles en un proyecto con diferentes tasas de coste y facturación.

## <a name="create-tasks"></a>Crear tareas
Cree dos tareas de proyecto de 40 horas cada una, la Tarea A y la Tarea B. Seleccione la Tarea A como predecesora de la Tarea B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar Rol y Unidad organizativa para un miembro del equipo genérico del proyecto

1. En la página **Programar** , seleccione la fila **Tarea** para la Tarea A. 
2. En el campo **Recursos** , seleccione **Crear** en la lista desplegable.
3. En la página **Creación rápida de miembros del equipo** , especifique los atributos del miembro del equipo genérico que puede realizar esta tarea.
4. Seleccione el rol y la unidad organizativa apropiada y luego seleccione **Guardar y cerrar**. Se crea un miembro del equipo genérico y se asigna a esta tarea. 

Repita estos pasos para la Tarea B y asegúrese de que el rol y la unidad organizativa del miembro del equipo genérico creado para la Tarea B sea diferente a la Tarea A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Configure el rol y la unidad organizativa para una tarea del proyecto

1. Después de crear la Tarea A, seleccione la tarea y luego seleccione **Editar tarea**.
2. En la página **Detalles de la tarea** , encuentre los campos **Rol** y **Unidad organizativa** , y agregue los valores que se requieren de un recurso que realizaría esta tarea. 

  > [!NOTE]
  > Si está completando estos escenarios con los datos de demostración de Project Service Automation, seleccione **Jefe de consultoría** para el rol y **Fabrikam US** como unidad organizativa.

3. Seleccione la Tarea B y, a continuación, seleccione **Editar tarea**.
4. En la página **Detalles de la tarea** , encuentre los campos **Rol** y **Unidad organizativa** , y agregue los valores que se requieren de un recurso que realizaría esta tarea. Asegúrese de que los valores en los campos **Rol** y **Unidad organizativa** de la Tarea B son diferentes a los de la Tarea A. 

  > [!NOTE]
  > Si está completando estos escenarios con los datos de demostración de Project Service Automation, seleccione **Técnico de red** para el rol y **Fabrikam US** como unidad organizativa.

5. Seleccione y cierre la página **Detalles de la tarea**. 

## <a name="team-member-and-estimates-behaviour"></a>Miembro del equipo y comportamiento de estimaciones 

1. En la página **Detalles de la tarea** , en el **Miembro del equipo** , seleccione los dos miembros del equipo genéricos y luego seleccione **Generar requisitos**. Esto generará los requisitos de recursos. 
2. Seleccione la fila del miembro del equipo para **Jefe de consultoría** y luego seleccione **Reservar**. El tablero de programación se abre y reserva un recurso para ese requisito.
3. Seleccione la fila del miembro del equipo para **Técnico de red** y seleccione **Reservar**. El tablero de programación se abre y reserva el mismo recurso en ese requisito.

### <a name="team-member-grid"></a>Cuadrícula Miembro del equipo 
En la cuadrícula **Miembro del equipo** , observe que se eliminan los dos registros de miembros del equipo genéricos y se reemplazan por un recurso. Hay un conjunto de valores para ese recurso que muestra un conjunto predeterminado de valores para **Rol** y **Unidad organizativa**.
Cuando amplía la fila de ese registro de miembro del equipo, puede ver distintas asignaciones en el registro de miembro del equipo para ambas tareas. Cada fila de asignación tiene valores específicos de la tarea para **Rol** y **Unidad organizativa**. 

### <a name="estimates-grid"></a>Cuadrícula Estimaciones 
Cuando navega a la cuadrícula **Estimaciones** , observará que ambas asignaciones para el mismo recurso tienen un precio diferente.
Se asignan precios a la asignación para el recurso en la Tarea A mediante el valor de atributo **Rol** de **Jefe de consultoría**. Se asignan precios a la asignación para el mismo recurso en la Tarea B mediante el valor de atributo **Rol** de **Técnico de red**.





