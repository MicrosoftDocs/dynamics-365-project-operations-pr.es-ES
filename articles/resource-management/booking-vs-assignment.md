---
title: Reservas frente a asignaciones
description: Este tema proporciona información sobre las diferencias entre las reservas de recursos y las asignaciones de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130239"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="74ff3-103">Reservas frente a asignaciones</span><span class="sxs-lookup"><span data-stu-id="74ff3-103">Bookings vs assignments</span></span>

<span data-ttu-id="74ff3-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="74ff3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="74ff3-105">Las reservas son la asignación manual o automática de recursos a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="74ff3-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="74ff3-106">Las reservas manuales consumen la capacidad de un recurso.</span><span class="sxs-lookup"><span data-stu-id="74ff3-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="74ff3-107">Las reservas representan conceptos organizativos para los equipos para que puedan comprender cómo se utilizarán los recursos en varios proyectos.</span><span class="sxs-lookup"><span data-stu-id="74ff3-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="74ff3-108">Dynamics 365 Project Operations considera las reservas como un concepto a nivel de proyecto.</span><span class="sxs-lookup"><span data-stu-id="74ff3-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="74ff3-109">A diferencia de las reservas, las asignaciones son el compromiso de recursos a las tareas del proyecto en la programación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="74ff3-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="74ff3-110">Los recursos pueden tener nombre o ser genéricos.</span><span class="sxs-lookup"><span data-stu-id="74ff3-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="74ff3-111">Normalmente, la suma de las reservas de un recurso será igual a la suma de las asignaciones del recurso en una o varias tareas.</span><span class="sxs-lookup"><span data-stu-id="74ff3-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="74ff3-112">Sin embargo, Project Operations no obliga a que se cumpla este contrato.</span><span class="sxs-lookup"><span data-stu-id="74ff3-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="74ff3-113">La vista **Conciliación** muestra los lugares de un jefe de proyecto donde las reservas y asignaciones de un recurso no coinciden.</span><span class="sxs-lookup"><span data-stu-id="74ff3-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
