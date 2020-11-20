---
title: Cumplimiento del requisito de recursos genéricos
description: En este tema se proporciona información cómo reservar recursos con nombre para un requisito de recurso genérico.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130329"
---
# <a name="generic-resource-requirement-fulfillment"></a>Cumplimiento del requisito de recursos genéricos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede para reservar un recurso con nombre para reemplazar el recurso genérico que tiene un requisito de recursos.

1. En la página **Proyectos**, seleccione la pestaña **Equipo**.
2. Seleccione el recurso genérico que tiene algún requisito de recursos de la lista y después seleccione **Reservar**. O bien, abra el requisito del recurso y después haga clic en **Reservar**.
3. En la página **Asistente de programación**, seleccione el recurso con nombre que desee reservar para su equipo de proyecto y después seleccione **Reservar**.

Cuando se completa la reserva y se cumple con un recurso con nombre, el recurso genérico se reemplaza por el recurso con nombre.

Las asignaciones de la programación también se actualizan con el recurso con nombre.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Cumplir un recurso genérico con varios recursos con nombre
Cumplir un requisito de recurso genérico con varios recursos con nombre es similar a asignar un único recurso con nombre. Por ejemplo, supongamos que hay una tarea con una duración de cinco días y 120 horas de esfuerzo. Esta tarea no la puede completar un recurso que trabaje durante una jornada normal de ocho horas y cinco días a la semana. 

El requisito es de 120 horas de ingeniería robótica durante cinco días, lo que equivale a 24 horas al día.

Este es un ejemplo de situación en la que se necesitan varios recursos con nombre para cumplir una solicitud de recursos genéricos. Deberá para reservar varios recursos para cumplir el requisito.

La diferencia principal en este escenario es que el recurso genérico permanece en el equipo asignado a la tarea y los miembros del equipo de recursos con nombre reservados no se asignan como parte de la posición. El jefe del proyecto puede asignar el trabajo según sea necesario a los recursos con nombre. La vista **Conciliación** puede ayudar a un jefe de proyecto a dividir las reservas de distintos recursos en asignaciones de tarea. Esto no se realiza automáticamente porque en escenarios más complejos que el descrito anteriormente, como, por ejemplo, cuando el requisito se compone de una agrupación de tareas o el sistema tiene que suponer la intención con la que el jefe de proyecto desea realizar la asignación. Debido a que el sistema no puede entender la intención, es probable que las suposiciones sean diferentes de lo previsto y se producirá un resultado incorrecto o impredecible. El resultado previsible es que el recurso genérico permanecerá asignado hasta que el jefe de proyecto cree asignaciones de manera intencionada con la ayuda de la vista **Conciliación**.

