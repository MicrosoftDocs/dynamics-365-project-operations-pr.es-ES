---
title: Enviar una solicitud de recursos
description: Puede enviar un requisito de recurso generado como solicitud de recurso. La solicitud se envía a un administrador de recursos para su cumplimiento.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961750"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="79f3c-104">Enviar una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="79f3c-104">Submit a resource request</span></span>

<span data-ttu-id="79f3c-105">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="79f3c-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="79f3c-106">Puede enviar un requisito de recurso generado como solicitud de recurso.</span><span class="sxs-lookup"><span data-stu-id="79f3c-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="79f3c-107">La solicitud se envía a un administrador de recursos para su cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="79f3c-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="79f3c-108">En Dynamics 365 Project Operations, en la página **Proyectos**, seleccione la pestaña **Equipo** para ver una lista de recursos reservables.</span><span class="sxs-lookup"><span data-stu-id="79f3c-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="79f3c-109">Seleccione el recurso genérico que tiene algún requisito de recursos de la lista y después haga clic en **Enviar solicitud**.</span><span class="sxs-lookup"><span data-stu-id="79f3c-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="79f3c-110">El estado de la solicitud del miembro del equipo genérico cambiará a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="79f3c-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="79f3c-111">Una vez completada la solicitud, el recurso genérico se reemplaza por un recurso con nombre si el administrador de recursos rellena la solicitud reservando un recurso con nombre.</span><span class="sxs-lookup"><span data-stu-id="79f3c-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="79f3c-112">De lo contrario, si el administrador de recursos propone un recurso con nombre, el recurso genérico permanece en el equipo y el estado de la solicitud cambiará a **Necesita revisión** .</span><span class="sxs-lookup"><span data-stu-id="79f3c-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
