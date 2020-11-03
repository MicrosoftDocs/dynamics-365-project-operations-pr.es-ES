---
title: Requisitos de reservas automáticas
description: En este tema se ofrece información sobre cómo cumplir los requisitos de reservas automáticas.
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
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085358"
---
# <a name="soft-book-requirements"></a>Requisitos de reservas automáticas

Se puede realizar una reserva manual de un requisito de recurso. Una reserva manual crea una propuesta que consume la capacidad de un recurso. La propuesta se envía después al solicitante para su aprobación. Una reserva automática agrega provisionalmente un recurso a un equipo del proyecto y tiene un estado diferente en el tablero de programación, pero no consume la capacidad del recurso. Para realizar una reserva automática de un recurso desde el tablero de programación, establezca el campo **Estado de reserva** en **Automática**.

![Estado de reserva establecido en Automática](media/Resource-Management-image77.png)

Cuando la pestaña **Equipo** está en la vista **Miembros del equipo con nombre** , aparece el recurso. Las horas de reserva automática se notifican en la columna **Horas reservadas automáticamente**.

![Horas reservadas automáticamente en la vista Miembros del equipo con nombre](media/Resource-Management-image78.png)

Los miembros del equipo reservados automáticamente no se pueden asignar a tareas.

![Miembro del equipo reservado automáticamente asignado a una tarea](media/Resource-Management-image79.png)

En la pestaña **Conciliación** no se muestran reservas para un recurso de reserva manual, ya que la pestaña **Conciliación** solo tiene en cuenta las reservas manuales.

![Recursos de reserva automática sin reservas en la pestaña Conciliación](media/Resource-Management-image80.png)

> [!NOTE]
> No puede realizar una reserva automática de un recurso desde un requisito generado por un miembro del equipo genérico.

En el tablero de programación, se utiliza un color diferente para las reservas automáticas de un recurso.

![Reservas automáticas en el tablero de programación](media/Resource-Management-image81.png)

Para convertir una reserva automática en una manual, en el tablero de programación, haga clic con el botón secundario en la reserva automática y, a continuación, seleccione **Cambiar estado** \> **Reserva manual** \> **Manual**.

![Cambio del estado de la reservar a Manual](media/Resource-Management-image82.png)

Se modifica la reserva y se cambia el estado en el tablero de programación. Como el estado de la reserva ahora es **Manual** , el recurso se muestra como reservado y se ajusta la capacidad y la disponibilidad.

Puede usar el mismo método para cancelar una reserva manual o una reserva automática desde el tablero de programación.

Para convertir un recurso reservado automáticamente en la pestaña **Equipo** , seleccione el recurso y, a continuación, seleccione **Confirmar**.

![Confirmación del comando](media/Resource-Management-image83.png)
