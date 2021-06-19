---
title: Reservas frente a asignaciones
description: Este tema proporciona información sobre las diferencias entre las reservas de recursos y las asignaciones de recursos.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012787"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="51264-103">Reservas frente a asignaciones</span><span class="sxs-lookup"><span data-stu-id="51264-103">Bookings vs assignments</span></span>

<span data-ttu-id="51264-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="51264-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="51264-105">Las reservas son la asignación manual o automática de recursos a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="51264-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="51264-106">Las reservas en firme consumen la capacidad de un recurso.</span><span class="sxs-lookup"><span data-stu-id="51264-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="51264-107">Las reservas representan conceptos organizativos para los equipos de modo que puedan comprender cómo se utilizarán los recursos en varios proyectos.</span><span class="sxs-lookup"><span data-stu-id="51264-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="51264-108">Dynamics 365 Project Operations considera las reservas como un concepto en el nivel de proyecto.</span><span class="sxs-lookup"><span data-stu-id="51264-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="51264-109">A diferencia de las reservas, las asignaciones son el compromiso de recursos genéricos para las tareas del proyecto en la programación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="51264-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="51264-110">Los recursos pueden tener nombre o ser genéricos.</span><span class="sxs-lookup"><span data-stu-id="51264-110">The resources can be named or generic.</span></span>  <span data-ttu-id="51264-111">Cuando se deriva un requisito de recursos de las asignaciones de tareas de proyecto, Project Operations utiliza los perfiles de esfuerzo de la asignación de recursos para crear los perfiles de los detalles del requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="51264-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="51264-112">Sin embargo, no se mantiene una referencia a las asignaciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="51264-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="51264-113">Las actualizaciones de las reservas derivadas del requisito de recursos no actualizan ninguna asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="51264-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="51264-114">Normalmente, la suma de las reservas de un recurso será igual a la suma de las asignaciones del recurso en una o varias tareas.</span><span class="sxs-lookup"><span data-stu-id="51264-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="51264-115">Sin embargo, Project Operations no obliga a que se cumpla este contrato.</span><span class="sxs-lookup"><span data-stu-id="51264-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="51264-116">La vista **Conciliación** muestra los lugares de un jefe de proyecto donde las reservas y asignaciones de un recurso no coinciden.</span><span class="sxs-lookup"><span data-stu-id="51264-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]