---
title: Información general sobre los modos de administración de recursos
description: En este tema se proporciona información sobre la función de administración de proyecto en Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279474"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="8b7e8-103">Información general sobre los modos de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="8b7e8-103">Resource management modes overview</span></span>

<span data-ttu-id="8b7e8-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="8b7e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8b7e8-105">Dynamics 365 Project Operations admite dos modos para ejecutar el flujo de las reservas en general.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="8b7e8-106">El modo de gestión se define como un parámetro del proyecto y se puede modificar si sus necesidades comerciales cambian.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="8b7e8-107">Modo central</span><span class="sxs-lookup"><span data-stu-id="8b7e8-107">Central mode</span></span>
<span data-ttu-id="8b7e8-108">Para las organizaciones que centralizan la asignación de recursos a los proyectos, el modo Central proporciona una forma de garantizar que los gerentes de proyecto puedan definir los requisitos de recursos a nivel de proyecto.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="8b7e8-109">El cumplimiento de los requisitos de recursos se delega a un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="8b7e8-110">Los administradores de proyecto pueden aceptar o rechazar los recursos propuestos por el administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Modo Central](./media/resource-management-central.png)

<span data-ttu-id="8b7e8-112">Para administrar recursos con el modo Central, consulte:</span><span class="sxs-lookup"><span data-stu-id="8b7e8-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="8b7e8-113">Asignar recursos genéricos que se pueden reservar a una tarea y generar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="8b7e8-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="8b7e8-114">Reservar recursos con nombre desde los requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="8b7e8-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="8b7e8-115">Enviar una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="8b7e8-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="8b7e8-116">Ejecutar solicitudes de recursos</span><span class="sxs-lookup"><span data-stu-id="8b7e8-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="8b7e8-117">Aceptar o rechazar un recurso de proyecto propuesto de una solicitud de recurso</span><span class="sxs-lookup"><span data-stu-id="8b7e8-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="8b7e8-118">Modo Híbrido</span><span class="sxs-lookup"><span data-stu-id="8b7e8-118">Hybrid mode</span></span>
<span data-ttu-id="8b7e8-119">Para las organizaciones que requieren flexibilidad en la asignación de recursos, el modo híbrido permite tanto a los administradores de proyectos como a los administradores de recursos la capacidad de reservar recursos.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Modo Híbrido](./media/resource-management-hybrid.png)

<span data-ttu-id="8b7e8-121">Además del proceso del modo Central admitido, consulte los siguientes temas para administrar todos los demás flujos de reserva admitidos en modo Híbrido:</span><span class="sxs-lookup"><span data-stu-id="8b7e8-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="8b7e8-122">Asignar un recurso directamente a un proyecto:</span><span class="sxs-lookup"><span data-stu-id="8b7e8-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="8b7e8-123">Reservar recursos con nombre que se pueden reservar para un equipo de proyecto y asignar tareas</span><span class="sxs-lookup"><span data-stu-id="8b7e8-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="8b7e8-124">Reservar recursos a partir de requisitos de recursos:</span><span class="sxs-lookup"><span data-stu-id="8b7e8-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="8b7e8-125">Asignar recursos genéricos que se pueden reservar a una tarea y generar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="8b7e8-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="8b7e8-126">Reservar recursos con nombre desde los requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="8b7e8-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]