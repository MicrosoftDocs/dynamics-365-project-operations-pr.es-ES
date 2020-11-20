---
title: P+F de administración de recursos
description: En este tema se proporcionan respuestas a preguntas frecuentes sobre la administración de recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 38d9509768323a5a1d78683a2e65ade241adc65f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120159"
---
# <a name="resource-management-faq"></a><span data-ttu-id="b8c62-103">P+F de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="b8c62-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="b8c62-104">¿Cuál es la diferencia entre un miembro del equipo y un requisito de recursos?</span><span class="sxs-lookup"><span data-stu-id="b8c62-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="b8c62-105">Un miembro del equipo del proyecto puede asignarse a tareas, reservarse o saturarse, y establecerse como un aprobador.</span><span class="sxs-lookup"><span data-stu-id="b8c62-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="b8c62-106">Puede existir un requisito de recursos sin un miembro del equipo del proyecto, como un borrador de la nota de petición.</span><span class="sxs-lookup"><span data-stu-id="b8c62-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="b8c62-107">¿Cuál es la diferencia entre las horas propuestas y las horas reservadas automáticamente?</span><span class="sxs-lookup"><span data-stu-id="b8c62-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="b8c62-108">Las horas propuestas y las horas reservadas automáticamente difieren en visibilidad.</span><span class="sxs-lookup"><span data-stu-id="b8c62-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="b8c62-109">Las horas propuestas solo son visibles para los administradores de recursos y el jefe de proyecto que iniciaron la petición mediante una solicitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8c62-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="b8c62-110">Las horas reservadas automáticamente son visibles para cualquier persona que tenga acceso al tablero de programación.</span><span class="sxs-lookup"><span data-stu-id="b8c62-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="b8c62-111">¿Cómo puedo ver las horas reservadas automáticamente para recursos en un equipo?</span><span class="sxs-lookup"><span data-stu-id="b8c62-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="b8c62-112">Cuando se reserva un requisito de recursos, se pueden crear reservas automáticas.</span><span class="sxs-lookup"><span data-stu-id="b8c62-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="b8c62-113">Los recursos reservados automáticamente en un equipo del proyecto aparecen como miembros del equipo que tienen horas reservadas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b8c62-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="b8c62-114">También aparecen en el tablero de programación.</span><span class="sxs-lookup"><span data-stu-id="b8c62-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="b8c62-115">¿Cómo cambio las horas necesarias y las fechas de inicio y finalización de un recurso (genérico o con nombre) que he reservado?</span><span class="sxs-lookup"><span data-stu-id="b8c62-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="b8c62-116">Después de reservar los recursos, seleccione **Mantener reservas** para realizar los cambios necesarios.</span><span class="sxs-lookup"><span data-stu-id="b8c62-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="b8c62-117">¿Qué tipos de recursos admite Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="b8c62-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="b8c62-118">**Usuario** y **Contacto** son los únicos tipos de recursos admitidos en Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b8c62-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="b8c62-119">Aunque puede crear otros tipos de recursos (por ejemplo, **Equipamiento** y **Grupo**), no se admiten casos de uso de principio a fin.</span><span class="sxs-lookup"><span data-stu-id="b8c62-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="b8c62-120">¿Cuál es la diferencia entre una tarea y una reserva?</span><span class="sxs-lookup"><span data-stu-id="b8c62-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="b8c62-121">Las asignaciones son la asignación de recursos a las tareas del proyecto en la programación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b8c62-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="b8c62-122">Los recursos pueden ser recursos reales o genéricos.</span><span class="sxs-lookup"><span data-stu-id="b8c62-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="b8c62-123">Las reservas son la asignación manual o automática de recursos a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="b8c62-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="b8c62-124">Las reservas manuales consumen la capacidad de un recurso.</span><span class="sxs-lookup"><span data-stu-id="b8c62-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="b8c62-125">Idealmente, para los recursos reales, las reservas y asignaciones deben coincidir, porque no difieren.</span><span class="sxs-lookup"><span data-stu-id="b8c62-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="b8c62-126">Sin embargo, PSA no obliga a que esto se cumpla.</span><span class="sxs-lookup"><span data-stu-id="b8c62-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="b8c62-127">La vista Conciliación muestra los lugares de un jefe de proyecto donde las reservas y asignaciones de un recurso no coinciden.</span><span class="sxs-lookup"><span data-stu-id="b8c62-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
