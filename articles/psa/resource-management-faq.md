---
title: P+F de administración de recursos
description: En este tema se proporcionan respuestas a preguntas frecuentes sobre la administración de recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085359"
---
# <a name="resource-management-faq"></a>P+F de administración de recursos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>¿Cuál es la diferencia entre un miembro del equipo y un requisito de recursos?

Un miembro del equipo del proyecto puede asignarse a tareas, reservarse o saturarse, y establecerse como un aprobador. Puede existir un requisito de recursos sin un miembro del equipo del proyecto, como un borrador de la nota de petición. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>¿Cuál es la diferencia entre las horas propuestas y las horas reservadas automáticamente?

Las horas propuestas y las horas reservadas automáticamente difieren en visibilidad. Las horas propuestas solo son visibles para los administradores de recursos y el jefe de proyecto que iniciaron la petición mediante una solicitud de recursos. Las horas reservadas automáticamente son visibles para cualquier persona que tenga acceso al tablero de programación.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>¿Cómo puedo ver las horas reservadas automáticamente para recursos en un equipo?

Cuando se reserva un requisito de recursos, se pueden crear reservas automáticas. Los recursos reservados automáticamente en un equipo del proyecto aparecen como miembros del equipo que tienen horas reservadas automáticamente. También aparecen en el tablero de programación.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>¿Cómo cambio las horas necesarias y las fechas de inicio y finalización de un recurso (genérico o con nombre) que he reservado?

Después de reservar los recursos, seleccione **Mantener reservas** para realizar los cambios necesarios.

## <a name="what-resources-types-does-project-service-automation-support"></a>¿Qué tipos de recursos admite Project Service Automation?

**Usuario** y **Contacto** son los únicos tipos de recursos admitidos en Dynamics 365 Project Service Automation. Aunque puede crear otros tipos de recursos (por ejemplo, **Equipamiento** y **Grupo** ), no se admiten casos de uso de principio a fin.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>¿Cuál es la diferencia entre una tarea y una reserva?

Las asignaciones son la asignación de recursos a las tareas del proyecto en la programación del proyecto. Los recursos pueden ser recursos reales o genéricos. Las reservas son la asignación manual o automática de recursos a un proyecto. Las reservas manuales consumen la capacidad de un recurso. Idealmente, para los recursos reales, las reservas y asignaciones deben coincidir, porque no difieren. Sin embargo, PSA no obliga a que esto se cumpla. La vista Conciliación muestra los lugares de un jefe de proyecto donde las reservas y asignaciones de un recurso no coinciden.
