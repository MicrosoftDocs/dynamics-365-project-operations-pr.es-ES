---
title: Aceptar o rechazar un recurso de propuesto de proyecto
description: En este tema se proporciona información sobre cómo aprobar o rechazar un recurso propuesto de proyecto.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/07/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 4c10c55961c74c2dc53fabd1d041a935ca9a4870
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085312"
---
# <a name="accept-or-reject-a-proposed-project-resource"></a>Aceptar o rechazar un recurso de propuesto de proyecto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En este tema se proporciona información sobre cómo aprobar o rechazar un recurso propuesto de proyecto.

Cuando un administrador de recursos propone un recurso denominado para completar la solicitud de recurso genérico de un proyecto, el campo **Estado de la solicitud** para el integrante del equipo genérico se actualizará a **Necesita revisión**. La solicitud se enviará al jefe del proyecto para su aprobación o rechazo.

![Miembro del equipo genérico con una propuesta](media/RM-how-to-19.png)

La cuadrícula en la pestaña **Recursos propuestos** en la página **Miembro del equipo del proyecto** muestra las reservas actuales del recurso propuesto. Una vez aceptada la propuesta, la cuadrícula se actualiza para reflejar la reserva. 

Para aceptar el recurso propuesto y reservar el recurso en su equipo, haga clic en **Aceptar propuestas**.  
Para rechazar la propuesta, haga clic en **Rechazar recurso**.

![Aceptar una propuesta de recursos](media/RM-how-to-20.png) 

Al igual que ocurre cuando se cumple una solicitud de recursos genérica con un recurso con nombre, el recurso genérico se reemplazará y las tareas asignadas se actualizarán con el miembro del equipo con nombre.
