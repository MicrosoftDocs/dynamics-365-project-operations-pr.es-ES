---
title: Métodos de asignación de reservas en Project Service Automation
description: En este tema se proporciona información sobre las distintas formas que puede reservar asignaciones.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: f0f4f5c68698fbe88de968e65a65b316b10872d9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590137"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Métodos de asignación de reservas en Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Tanto si agrega un miembro del equipo directamente a un proyecto en la pestaña **Equipo** como si reserva un recurso para un proyecto o requisito desde el tablero Programación, hay varios métodos de asignación de reservas que puede usar. En este tema se explica cómo funciona cada método y qué métodos podrían producir saturación exceso de reserva en los recursos.

## <a name="full-capacity"></a>Plena capacidad 
El método Plena capacidad reserva la capacidad completa del recurso para las fechas especificadas de inicio y fin. Por ejemplo, si un recurso tiene un calendario establecido para trabajar ocho horas por día, cinco días a la semana, al establecer una fecha de inicio y finalización que cubra cinco días laborables, se reservará el recurso por 40 horas. La reserva se realiza sin tener en cuenta la capacidad restante del recurso. Si un recurso ya está reservado en ese periodo en otros proyectos, las 40 horas se reservan como horas adicionales, lo que potencialmente puede producir exceso de reserva.

## <a name="remaining-capacity"></a>Capacidad restante
Este método Capacidad restante solo está disponible cuando se reserva directamente para un proyecto con el tablero Programación. El método reserva la capacidad disponible del recurso en el intervalo de fechas especificado. Por ejemplo, si un recurso tiene una capacidad de 40 horas por semana y se ha reservado ya 10 horas, la reserva para la misma semana dará como resultado una reserva por las 30 horas restantes de capacidad para dicha semana.

## <a name="percentage-capacity"></a>Porcentaje de capacidad
El método Porcentaje de capacidad reserva el recurso por un porcentaje de capacidad para las fechas especificadas de inicio y finalización. Por ejemplo, si el calendario de un recurso está establecido para trabajar ocho horas por día, cinco días a la semana, al establecer una fecha de inicio y finalización que cubra cinco días laborables a una capacidad del 50 %, se reservaría el recurso por 20 horas. Las reservas individuales por día se distribuyen por igual a lo largo del período, por ejemplo, cuatro horas por día en este ejemplo. La reserva se hace sin tener en cuenta la capacidad restante del recurso. Si el recurso ya está reservado durante ese periodo en otros proyectos, las 20 horas se reservan como horas adicionales, lo que potencialmente puede producir exceso de reserva.

## <a name="evenly-distribute-hours"></a>Horas distribuidas equitativamente
El método Horas distribuidas equitativamente reserva el recurso durante un número específico de horas, distribuyendo el tiempo de manera uniforme en cada día durante el periodo comprendido entre las fechas de inicio y finalización especificadas. Por ejemplo, si reserva un recurso para 20 horas durante un período de cinco días, este método distribuye las 20 horas de manera uniforme en cuatro horas al día. La reserva se realiza sin tener en cuenta la capacidad restante del recurso. Si el recurso ya está reservado durante ese periodo en otros proyectos, las 20 horas se reservan como horas adicionales, lo que potencialmente puede producir exceso de reserva.

## <a name="front-load-hours"></a>Concentrar al principio
El método Concentrar al principio reserva el recurso durante un número especificado de horas, concentrando al principio las horas diarias durante el periodo comprendido entre las fechas de inicio y finalización especificadas. La carga frontal consume la capacidad disponible del recurso en orden de “primero en llegar, primero en consumir". Por ejemplo, si la programación de trabajo de un recurso es de ocho horas por día, cinco días por semana y no tiene ninguna reserva actual, la reserva del recurso durante 20 horas a lo largo de un periodo de cinco días laborables produce el siguiente patrón de reserva diario: 

|         Reservas          |    Día 1    |    Día 2    |    Día 3    |    Día 4    |    Día 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Reservas existentes    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nueva reserva          |    8        |    8        |    4        |    0        |    0        |    20       |

El método de carga por adelantado toma en consideración las reservas existentes y la capacidad disponible. Por ejemplo, si el mismo recurso ya tiene 20 horas de reservas en la semana laboral, las nuevas reservas consumen la capacidad restante de la siguiente manera:

|   Reservas          | Día 1 | Día 2 | Día 3 | Día 4 | Día 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| Reservas existentes | 8     | 8     | 4     | 0     | 0     | 20    |
| Nueva reserva       | 0     | 0     | 4     | 8     | 8     | 20    |

Puesto que se considera la capacidad disponible, puede obtener un mensaje de error si el recurso no tiene capacidad restante que pueda absorber la reserva. Con este método, no puede reservar en exceso.

## <a name="none"></a>Ninguno
El método Ninguno solo está disponible cuando se reserva desde la pestaña **Equipo** en un proyecto. Este método agrega el recurso como integrante del equipo del proyecto, pero no crea ninguna reserva que absorba la capacidad del recurso. Este método se usa cuando el integrante del equipo jefe del proyecto predeterminado se agrega cuando se crea un proyecto. El usuario jefe de proyecto que creó el proyecto se agrega de forma predeterminada al proyecto, de modo que el registro de la entidad de proyecto tenga un propietario y haya un aprobador en el proyecto. Puesto que este usuario no tiene ninguna reserva, si desea reservar el recurso puede eliminarlo y después volver a agregarlo mediante otro método de asignación, o bien agregar el recurso a tareas y después usar **Ampliar reservas** en la pestaña **Conciliación** para crear reservas para las asignaciones.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Métodos de asignación que producen reserva excesiva
En resumen, los siguientes métodos de asignación producen reserva excesiva si el recurso ya está comprometido en otros proyectos (o para otras órdenes de trabajo o entidades programables):

- Plena capacidad
- Porcentaje de capacidad
- Horas distribuidas equitativamente

Cuando se usa uno de estos tres métodos de asignación no se le notificará si el recurso se ha reservado en exceso. Para corregir el exceso de reserva, deberá usar al tablero Programación.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
