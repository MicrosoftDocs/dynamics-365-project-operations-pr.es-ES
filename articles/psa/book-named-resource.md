---
title: Reservar recursos con nombre desde los requisitos de recursos
description: En este artículo se proporciona información sobre la reserva de recursos con nombre para un requisito de recurso genérico.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916263"
---
# <a name="book-named-resources-from-resource-requirements"></a>Reservar recursos con nombre desde los requisitos de recursos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Puede para reservar un recurso con nombre para reemplazar el recurso genérico que tiene un requisito de recursos.

1. En Project Service Automation (PSA), en la página **Proyectos**, haga clic en la pestaña **Equipo**.
2. Seleccione el recurso genérico que tiene algún requisito de recursos de la lista y después haga clic en **Reservar**. O bien, abra el requisito del recurso y después haga clic en **Reservar**.


![Reserva de un miembro del equipo genérico.](media/RM-how-to-14.png)


3. En la página **Asistente de programación**, seleccione el recurso con nombre que desee reservar para su equipo de proyecto y después haga clic en **Reservar**.

![Reserva de un miembro de equipo genérico con el asistente de programación.](media/RM-how-to-15.png)

Cuando se completa la reserva y se cumple con un recurso con nombre, el recurso genérico se reemplaza por el recurso con nombre.

![Miembro del equipo con nombre que reemplaza a un miembro del equipo genérico.](media/RM-how-to-16.png)

Las asignaciones de la programación también se actualizan con el recurso con nombre.

![Miembro del equipo con nombre asignado a las tareas del proyecto.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Cumplir un recurso genérico con varios recursos con nombre
Cumplir un requisito de recurso genérico con varios recursos con nombre es similar a asignar un único recurso con nombre. Por ejemplo, supongamos que hay una tarea con una duración de cinco días y 120 horas de esfuerzo. Esta tarea no la puede completar un recurso que trabaje durante una jornada normal de ocho horas y cinco días a la semana. 

![Tarea que necesita 120 horas de esfuerzo durante cinco días.](media/RM-how-to-21.png)

El requisito es de 120 horas de ingeniería robótica durante cinco días, lo que equivale a 24 horas al día.

![Requisito por día.](media/RM-how-to-22.png)

Este es un ejemplo de situación en la que se necesitan varios recursos con nombre para cumplir una solicitud de recursos genéricos. Deberá para reservar varios recursos para cumplir el requisito.

![Reserva de varios recursos para cumplir el requisito.](media/RM-how-to-23.png)

La diferencia principal en este escenario es que el recurso genérico permanece en el equipo asignado a la tarea y los miembros del equipo de recursos con nombre reservados no se asignan como parte de la posición. El jefe del proyecto puede asignar el trabajo según sea necesario a los recursos con nombre. La vista **Conciliación** puede ayudar a un jefe de proyecto a dividir las reservas de distintos recursos en asignaciones de tarea. Esto no se realiza automáticamente porque en escenarios más complejos que el descrito anteriormente, como, por ejemplo, cuando el requisito se compone de una agrupación de tareas, el sistema tiene que suponer la intención con la que el jefe de proyecto desea realizar la asignación. Dado que el sistema no puede comprender la intención, es posible que las suposiciones sean distintas de las reales y que, por lo tanto, se obtenga un resultado incorrecto o imprevisible. El resultado previsible es que el recurso genérico permanecerá asignado hasta que el jefe de proyecto cree asignaciones de manera intencionada con la ayuda de la vista **Conciliación**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
