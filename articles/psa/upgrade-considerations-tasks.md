---
title: Consideraciones de actualización para la estructura de descomposición del trabajo
description: En este tema se proporciona información sobre cómo actualizar la estructura de descomposición del trabajo de Project Service Automation 2.x a 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149564"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Consideraciones de actualización para la estructura de descomposición del trabajo

[!include [banner](../includes/psa-now-project-operations.md)]

En este tema se proporciona información sobre cómo actualizar la estructura de descomposición del trabajo de Project Service Automation 2.x a 3.x. Este tema define el estado correcto de un proyecto en Project Service Automation (PSA) necesario para realizar una actualización correcta. También incluye información sobre las condiciones de bloqueo comunes que harán que se produzca un error en la actualización. Para obtener más información sobre cómo definir las tareas del proyecto y sus funciones dentro de una programación del proyecto, consulte [Programaciones del proyecto](project-creating.md).

## <a name="key-entities"></a>Entidades clave
Para una estructura de descomposición del trabajo precisa que ya esté cargada de recursos, se requieren las siguientes entidades:

- [Proyecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Equipo del proyecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Tarea de proyecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Asignaciones de recursos](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dependencia de tareas de proyecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Recursos que se pueden reservar](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Para definir una estructura de descomposición del trabajo cargada de recursos, debe completar los siguientes pasos:

1. Crear un nuevo proyecto. Para obtener más información sobre cómo crear un nuevo proyecto, consulte [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Crear una o varias tareas. Para obtener más información sobre cómo crear una tarea, consulte [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definir las dependencias entre tareas. Para obtener más información, consulte [Dependencia de tareas de proyecto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Asignar miembros del equipo de proyecto al proyecto. Para obtener más información, consulte [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Asignar miembros del equipo de proyecto a las tareas. Para obtener más información, consulte [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relaciones del equipo del proyecto

Para garantizar una actualización correcta, deben conservarse correctamente las siguientes relaciones:
- Todos los miembros del equipo del proyecto deben asociarse con un recurso que se puede reservar.
- Todos los miembros del equipo del proyecto deben asociarse con el mismo proyecto. 

## <a name="project-task-relationships"></a>Relaciones de tareas del proyecto
Para garantizar una actualización correcta, deben conservarse correctamente las siguientes relaciones:

- Cualquier tarea relacionada debe estar asociada al mismo proyecto.
- Cada tarea de línea debe tener una tarea principal.
- Cada tarea de línea debe tener un proyecto principal.

### <a name="valid-conditions"></a>Condiciones válidas

- Todas las duraciones de la tarea deben ser superiores o iguales a (>=) una hora e inferiores a 1 800 000 minutos (1250 días).*
- Todas las tareas deben tener una fecha de inicio no anterior al 01/01/2000.*
- Todas las tareas deben tener una fecha de inicio no posterior a 17 años desde el día actual.*
- Todas las tareas deben tener una fecha de inicio anterior o igual a la fecha de finalización.
- Todos los tipos de transacciones en las clasificaciones (Gastos, Material, Impuestos y Tiempo) deben tener valores para **Unidad predeterminada** y **Unidad de venta**.
- Se deben evitar los formatos de fecha con letras.

### <a name="potential-mitigation-steps"></a>Pasos de mitigación potenciales
- Use la Búsqueda avanzada para identificar Tareas de proyecto que no contengan un Id. de proyecto.
- Use la Búsqueda avanzada para identificar Tareas de proyecto donde la duración programada sea superior a > 1.800.000.
- Antes de realizar cambios en los datos, debe investigar cualquier personalización asociada a la entidad que pueda haber ocasionado el mal estado de los datos. Estas personalizaciones deben abordarse antes de continuar con cualquier actualización relacionada con los datos.
- Para las tareas identificadas que han quedado huérfanas, considere eliminar estas tareas si no son necesarias o si deberían asociarse al proyecto primario correcto.
- Para cualquier tarea donde la duración sea superior a 1250 días, considere agregar varias tareas para representar la duración total, si es viable.

> [!NOTE]
> Los elementos señalados con un asterisco (\*) tienen límites que se deben al hecho de que la administración de relaciones con el cliente (CRM) solo admite 7320 expansiones recurrentes. Debe mantenerse por debajo de este límite.

## <a name="resource-assignment-relationships"></a>Relaciones de asignación de recursos
Para garantizar una actualización correcta, deben conservarse correctamente las siguientes relaciones:

- Todas las asignaciones de recursos en una estructura de descomposición del trabajo deben estar relacionadas con el mismo proyecto.
- Todas las asignaciones de recursos en una estructura de descomposición del trabajo deben estar asociadas a los miembros del equipo del proyecto en el mismo proyecto.

### <a name="potential-mitigation-steps"></a>Pasos de mitigación potenciales
- Identifique todas las tareas que se encuentra fuera de las condiciones descritas anteriormente.  
- Debe eliminarse cualquier asignación de recursos que ya no sea válida.

## <a name="project-task-dependency-relationships"></a>Relaciones de dependencia de tareas del proyecto
Para garantizar una actualización correcta, deben conservarse correctamente las siguientes relaciones:

- Todas las dependencias de tareas del proyecto deben estar relacionadas con el mismo proyecto.
- Una tarea no puede tener la misma dependencia referenciada más de una vez.
