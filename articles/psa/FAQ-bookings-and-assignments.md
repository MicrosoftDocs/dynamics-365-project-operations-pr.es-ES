---
title: Reservas de recursos y relación con las asignaciones de tareas
description: En este tema se proporciona información sobre cómo administrar los recursos con nombre, las reservas de recursos y las asignaciones de tareas, así como su relación entre sí.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 0e4eea87bfb059a3c0be8ccbd2914a4d6c3cf46b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149969"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Reservas de recursos y relación con las asignaciones de tareas

[!include [banner](../includes/psa-now-project-operations.md)]

Los recursos con nombre se pueden reservar para un equipo de proyecto y asignar a tareas de proyecto de dos maneras:

- El recurso puede se puede reservar directamente en un proyecto y después se puede asignar a tareas de proyectos.
- Las tareas se pueden asignar un recurso genérico, que a continuación se usa para buscar y reemplazar el recurso genérico con un recurso con nombre. 

En ambos casos, el hecho de reservar el recurso reserva la capacidad del recurso.

El jefe de proyecto que planea el proyecto es propietario del plan y la programación del proyecto. Al utilizar el recurso genérico para la asignación y después generar una solicitud de recursos a partir de ella, el jefe de proyecto puede reservar recursos para el proyecto con perfiles especificados en el plan del proyecto. Puede reservar recursos para un proyecto y después asignarlos a tareas; sin embargo, no hay forma de alinear los perfiles de reserva con los perfiles de las tareas. Las reservas no afectan a la programación del proyecto.

Considere un proyecto complejo con varias tareas superpuestas en el que recursos múltiples del mismo tipo necesitan trabajar en paralelo. Si se da a un recurso un perfil que varía del agregado de sus asignaciones, es difícil modificar las tareas para ajustar el perfil de las reservas a sus tareas discretas y a sus perfiles originales.

En el siguiente ejemplo, el esfuerzo total requerido por el mismo recurso de un conjunto de cuatro tareas es 62 horas durante un período de dos semanas y hay un perfil específico. Si se reserva el recurso Bob durante 62 horas durante las dos mismas semanas pero con otro perfil, el requisito y las reservas están alineados.

| **Perfiles de tarea**    | **Horas totales** | Lu 6/4 | Ma 6/5 | Mi 6/6 | Ju 6/7 | Vi 6/8 | Sá 6/9 | Do 6/10 | Lu 6/11 | Ma 6/12 | Mi 6/13 | Ju 6/14 | Vi 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tarea 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tarea 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tarea 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tarea 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totales**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Disponibilidad de Bob
| **Reserva de recursos** | **Horas totales** | Lu 6/4 | Ma 6/5 | Mi 6/6 | Ju 6/7 | Vi 6/8 | Sá 6/9 | Do 6/10 | Lu 6/11 | Ma 6/12 | Mi 6/13 | Ju 6/14 | Vi 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Sin embargo, no hay una forma sistemática de asignar el perfil de horas reservadas a tareas para cada día. Si el jefe de proyecto está dispuesto a cambiar el calendario del proyecto para atender la disponibilidad del recurso, deberá quitar la asignación y revisar todas las tareas para que coincidan con los perfiles de la reserva.

En el caso en que una organización ha dado la tarea de planeamiento de proyecto a un jefe de proyecto y un administrador de recursos, el jefe de proyecto establece la programación, que incluye elaborar un perfil del trabajo requerido. El administrador de recursos no debe poder afectar a la programación sin el conocimiento del jefe de proyecto cambiando perfiles de esfuerzo mientras reserva recursos reales. Si el administrador de recursos cumple algo diferente de lo que ha solicitado el jefe de proyecto, deben llegar a un acuerdo sobre los cambios que se necesitan en el calendario del proyecto.

Puesto que las reservas y las asignaciones no están emparejadas firmemente, es posible reservar perfiles que sean distintos de los perfiles de tarea o cambiar las asignaciones para producir circunstancias en las que las reservas y las asignaciones queden desalineadas.

La vista **Conciliación** permite al jefe de proyecto ver las reservas y las asignaciones de cada miembro del equipo de proyecto. La vista usa colores y sombreado para mostrar dónde no hay coincidencias entre las reservas y las asignaciones de los integrantes de un equipo. Según esta información, el jefe de proyecto puede tomar medidas correctoras para ampliar las reservas de recursos para los casos donde haya asignaciones y no reservas o para cancelar reservas cuando se hayan reservado recursos pero no tengan asignaciones.

> [!NOTE]
> Si mueve una tarea para la que usted mismo ha creado un perfil, estos perfiles no se mantienen. Los perfiles se vuelven a generar de acuerdo con el calendario de proyecto para responder a los cambios en horas laborables y las vacaciones. Esto se debe al diseño, ya que el sistema no conoce el propósito del perfil original y no puede determinar si conviene conservar el perfil en un nuevo período de tiempo. Puesto que las reservas y asignaciones están desconectadas, las reservas mantienen los perfiles de reserva originales. En este caso, deberá cancelar y volver a reservar el nuevo perfil de asignación.



[!INCLUDE[footer-include](../includes/footer-banner.md)]