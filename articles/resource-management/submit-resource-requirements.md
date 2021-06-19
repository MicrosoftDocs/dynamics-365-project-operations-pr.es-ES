---
title: Enviar una solicitud de recursos
description: Puede enviar un requisito de recurso generado como solicitud de recurso. La solicitud se envía a un administrador de recursos para su cumplimiento.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014047"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="8f527-104">Enviar una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="8f527-104">Submit a resource request</span></span>

<span data-ttu-id="8f527-105">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="8f527-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8f527-106">Puede enviar un requisito de recurso generado como solicitud de recurso.</span><span class="sxs-lookup"><span data-stu-id="8f527-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="8f527-107">Luego, la solicitud se envía a un administrador de recursos para su cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="8f527-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="8f527-108">En Dynamics 365 Project Operations, en la página **Proyectos**, seleccione la pestaña **Equipo** para ver una lista de recursos que se pueden reservar.</span><span class="sxs-lookup"><span data-stu-id="8f527-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="8f527-109">Seleccione el recurso genérico que tiene algún requisito de recursos de la lista y después haga clic en **Enviar solicitud**.</span><span class="sxs-lookup"><span data-stu-id="8f527-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="8f527-110">El estado de la solicitud del miembro del equipo genérico cambiará a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="8f527-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="8f527-111">Una vez realizada la solicitud, el recurso genérico se reemplaza por un recurso con nombre si el administrador de recursos cumple la solicitud reservando un recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="8f527-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="8f527-112">De lo contrario, si el administrador de recursos propone un recurso con nombre, el recurso genérico permanece en el equipo y el estado de la solicitud cambiará a **Necesita revisión** .</span><span class="sxs-lookup"><span data-stu-id="8f527-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]