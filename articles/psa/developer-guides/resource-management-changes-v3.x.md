---
title: Cambios en la administración de recursos (Project Service Automation 3.x)
description: En este tema se proporciona información sobre los cambios en el área de administración de recursos.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e888d55b93c40e08e51bd4480853fec37f2b6333
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007837"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Cambios en la administración de recursos (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Las secciones de este tema proporcionan información sobre los cambios que se han realizado en el área de administración de recursos de la versión 3.x de Dynamics 365 Project Service Automation.

## <a name="project-estimates"></a>Estimaciones de proyecto

En lugar de basarse en la entidad **msdyn\_projecttask** (**Tarea de proyecto**), las estimaciones de proyecto se basan en la entidad **msdyn\_resourceassignment** (**Asignación de recursos**). Las asignaciones de recursos se han convertido en el "origen de la verdad" para la programación y fijación de precios de tareas.

## <a name="line-tasks"></a>Tareas de línea

En PSA 3.x, las tareas de línea están obsoletas (en desuso). Las asignaciones ahora apuntan a la tarea completa en lugar a las tareas de línea.

El siguiente ejemplo muestra cómo se asigna una tarea denominada "Tarea de prueba" a los miembros del equipo A y B en versiones anteriores de PSA y en PSA 3.x.

- **Antes de PSA 3.x:**

    - Tarea de prueba

        - Tarea de prueba: tarea de línea 1

            - Asignación a A

        - Tarea de prueba: tarea de línea 2

            - Asignación a B

- **PSA 3.x:**

    - Tarea de prueba

        - Asignación a A
        - Asignación a B

## <a name="unassigned-assignment"></a>Asignación sin asignar

En PSA 3.x, una asignación sin asignar es una asignación que se asigna a un miembro del equipo **NULL** y a un recurso **NULL**. Las asignaciones sin asignar pueden producirse en un par de escenarios:

- Si se ha creado una tarea, pero aún no se ha asignado a ningún miembro del equipo, siempre se crea una asignación sin asignar. 
- Si se eliminan todas las personas asignadas en una tarea, se vuelve a crear una asignación sin asignar para esa tarea.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Programación de campos en la entidad Tarea de proyecto

Los campos en la entidad **msdyn\_projecttask** están en desuso o se han movido a la entidad **msdyn\_resourceassignment**, o se hace referencia a ella desde la entidad **msdyn\_projectteam** (**Miembro del equipo del proyecto**).

| Campo en desuso en msdyn\_projecttask (Tarea de proyecto) | Nuevo campo en msdyn\_resourceassignment (Asignación de recursos) | Comentario |
|---|---|---|
| msdyn\_assignedresources | Ninguno | |
| msdyn\_assignedteammembers | Ninguno | |
| msdyn\_numberofresources | Ninguno | |
| msdyn\_scheduledhours | Ninguno | |
| msdyn\_effortcontour | msdyn\_plannedwork | Se ha cambiado el formato de la estructura de datos de notación de objetos JavaScript (JSON) que se almacena en el campo. |

## <a name="schedule-contour"></a>Perfil de programación

El perfil de programación se almacena en el campo **Trabajo previsto** (**msdyn\_plannedwork**) de cada entidad **Asignación de recursos** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Estructura

La nueva estructura del perfil de programación consta de segmentos de tiempo flexibles que se definen para cada día de la programación. Cada sector de tiempo tiene las siguientes propiedades:

- **Inicio**: el inicio de las horas de trabajo del día, según el calendario del proyecto.
- **Fin**: el final de las horas de trabajo del día, según el calendario del proyecto.
- **Horas**: la cantidad de horas que se asignan en el día.

**Ejemplo**

Este ejemplo utiliza un calendario de proyecto donde el día laborable es de 9 a.m. a 5 p.m. en la zona horaria UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Programación automática y programación manual

Si una tarea se programa automáticamente, las horas se cargan por adelantado y la duración de la tarea puede reducirse.

**Ejemplo**

La siguiente tarea se programa automáticamente durante 18 horas durante tres días (del 3 de diciembre de 2018 al 5 de diciembre de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Si una tarea se programa manualmente, las horas se distribuyen uniformemente a todas las fechas.

**Ejemplo**

La siguiente tarea se programa manualmente durante 18 horas durante tres días (del 3 de diciembre de 2018 al 5 de diciembre de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unidad de asignación

La unidad de asignación se ha quedado en desuso en PSA 3.x. Las horas de esfuerzo de la tarea ahora se dividen en partes iguales, por día, entre todos los recursos asignados.

**Ejemplo**

En este ejemplo, la tarea se asigna a dos recursos y se programa automáticamente durante 36 horas durante tres días (del 3 de diciembre de 2018 al 5 de diciembre de 2018).

- Asignación 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Asignación 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensiones de precios

En PSA 3.x, los campos de dimensión de precios específicos de recursos (como **Rol** y **Unidad organizativa**) se han quitado de la entidad **msdyn\_projecttask**. Estos campos ahora se pueden recuperar del miembro del equipo del proyecto correspondiente (**msdyn\_projectteam**) de la asignación de recursos (**msdyn\_resourceassignment**) cuando se generan estimaciones de proyecto. Se ha agregado un nuevo campo, **msdyn\_organizationalunit**, a la entidad **msdyn\_projectteam**.

| Campo en desuso en msdyn\_projecttask (Tarea de proyecto) | Campo de msdyn\_projectteam (Miembro del equipo del proyecto) que se usa en su lugar |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Perfiles

Los campos de perfiles de precios y estimaciones han quedado en desuso en la entidad **msdyn\_projecttask**. Se han movido a la entidad **msdyn\_resourceassignment**.

| Campo en desuso en msdyn\_projecttask (Tarea de proyecto) | Nuevo campo en msdyn\_resourceassignment (Asignación de recursos) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Los siguientes campos se han agregado a la entidad **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Los siguientes campos para costes y ventas planificados, reales y restantes no se modifican en la entidad **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]