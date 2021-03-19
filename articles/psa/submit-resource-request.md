---
title: Envío de una solicitud de recursos
description: En este tema se proporciona información sobre el envío de una solicitud para un recurso del proyecto.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
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
ms.openlocfilehash: 8976ca2360be8676350178059615c59995544a71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282264"
---
# <a name="submitting-a-resource-request"></a>Envío de una solicitud de recursos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Puede enviar un requisito de recurso generado como solicitud de recurso. La solicitud se envía a un administrador de recursos para su cumplimiento.

1. En Project Service Automation (PSA), en la página **Proyectos**, haga clic en la pestaña **Equipo** para ver una lista de recursos que se pueden reservar. 
2. Seleccione el recurso genérico que tiene algún requisito de recursos de la lista y después haga clic en **Enviar solicitud**.

![Envío de una solicitud de recursos](media/RM-how-to-18.png)

El estado de la solicitud del miembro del equipo genérico cambiará a **Enviado**.

Una vez que el administrador de recursos complete la solicitud, el recurso genérico se reemplazará por un recurso con nombre si el administrador de recursos cumple la solicitud con la reserva de un recurso con nombre. De lo contrario, el recurso genérico permanecerá en el equipo y el estado de la solicitud cambiará a **Necesita revisión** si el administrador de recursos ha propuesto un recurso con nombre.


[!INCLUDE[footer-include](../includes/footer-banner.md)]