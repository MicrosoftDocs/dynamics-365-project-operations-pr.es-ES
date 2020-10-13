---
title: Información general sobre los modos de administración de recursos
description: Este tema proporciona información sobre la funcionalidad de gestión de recursos en las Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930112"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="9128b-103">Información general sobre los modos de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="9128b-103">Resource management modes overview</span></span>

<span data-ttu-id="9128b-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="9128b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9128b-105">Dynamics 365 Project Operations admite dos modos para poder ejecutar el flujo de reserva general.</span><span class="sxs-lookup"><span data-stu-id="9128b-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="9128b-106">El modo de gestión se define como un parámetro del proyecto y se puede modificar si sus necesidades comerciales cambian.</span><span class="sxs-lookup"><span data-stu-id="9128b-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="9128b-107">Modo central</span><span class="sxs-lookup"><span data-stu-id="9128b-107">Central mode</span></span>
<span data-ttu-id="9128b-108">Para las organizaciones que centralizan la asignación de recursos a los proyectos, el modo Central proporciona una forma de garantizar que los gerentes de proyecto puedan definir los requisitos de recursos a nivel de proyecto.</span><span class="sxs-lookup"><span data-stu-id="9128b-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="9128b-109">El cumplimiento de los requisitos de recursos se delega a un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="9128b-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="9128b-110">Los administradores de proyecto pueden aceptar o rechazar los recursos propuestos por el administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="9128b-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Modo Central](./media/resource-management-central.png)

<span data-ttu-id="9128b-112">Para administrar recursos con el modo Central, consulte:</span><span class="sxs-lookup"><span data-stu-id="9128b-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="9128b-113">Asignar recursos genéricos que se pueden reservar a una tarea y generar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="9128b-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="9128b-114">Reservar recursos con nombre desde los requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="9128b-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="9128b-115">Enviar una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="9128b-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="9128b-116">Ejecutar solicitudes de recursos</span><span class="sxs-lookup"><span data-stu-id="9128b-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="9128b-117">Aceptar o rechazar un recurso de proyecto propuesto de una solicitud de recurso</span><span class="sxs-lookup"><span data-stu-id="9128b-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="9128b-118">Modo Híbrido</span><span class="sxs-lookup"><span data-stu-id="9128b-118">Hybrid mode</span></span>
<span data-ttu-id="9128b-119">Para las organizaciones que requieren flexibilidad en la asignación de recursos, el modo híbrido permite tanto a los administradores de proyectos como a los administradores de recursos la capacidad de reservar recursos.</span><span class="sxs-lookup"><span data-stu-id="9128b-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Modo Híbrido](./media/resource-management-hybrid.png)

<span data-ttu-id="9128b-121">Además del proceso del modo Central admitido, consulte los siguientes temas para administrar todos los demás flujos de reserva admitidos en modo Híbrido:</span><span class="sxs-lookup"><span data-stu-id="9128b-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="9128b-122">Asignar un recurso directamente a un proyecto:</span><span class="sxs-lookup"><span data-stu-id="9128b-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="9128b-123">Reservar recursos con nombre que se pueden reservar para un equipo de proyecto y asignar tareas</span><span class="sxs-lookup"><span data-stu-id="9128b-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="9128b-124">Reservar recursos a partir de requisitos de recursos:</span><span class="sxs-lookup"><span data-stu-id="9128b-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="9128b-125">Asignar recursos genéricos que se pueden reservar a una tarea y generar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="9128b-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="9128b-126">Reservar recursos con nombre desde los requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="9128b-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
