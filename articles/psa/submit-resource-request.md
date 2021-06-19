---
title: Envío de una solicitud de recursos
description: En este tema se proporciona información sobre el envío de una solicitud para un recurso del proyecto.
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013192"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="58167-103">Envío de una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="58167-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="58167-104">Puede enviar un requisito de recurso generado como solicitud de recurso.</span><span class="sxs-lookup"><span data-stu-id="58167-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="58167-105">La solicitud se envía a un administrador de recursos para su cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="58167-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="58167-106">En Project Service Automation (PSA), en la página **Proyectos**, haga clic en la pestaña **Equipo** para ver una lista de recursos que se pueden reservar.</span><span class="sxs-lookup"><span data-stu-id="58167-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="58167-107">Seleccione el recurso genérico que tiene algún requisito de recursos de la lista y después haga clic en **Enviar solicitud**.</span><span class="sxs-lookup"><span data-stu-id="58167-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Envío de una solicitud de recursos](media/RM-how-to-18.png)

<span data-ttu-id="58167-109">El estado de la solicitud del miembro del equipo genérico cambiará a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="58167-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="58167-110">Una vez que el administrador de recursos complete la solicitud, el recurso genérico se reemplazará por un recurso con nombre si el administrador de recursos cumple la solicitud con la reserva de un recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="58167-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="58167-111">De lo contrario, el recurso genérico permanecerá en el equipo y el estado de la solicitud cambiará a **Necesita revisión** si el administrador de recursos ha propuesto un recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="58167-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]