---
title: Reservas frente a asignaciones
description: Este tema proporciona información sobre las diferencias entre las reservas de recursos y las asignaciones de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896032"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="2eb78-103">Reservas frente a asignaciones</span><span class="sxs-lookup"><span data-stu-id="2eb78-103">Bookings vs assignments</span></span>

<span data-ttu-id="2eb78-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="2eb78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2eb78-105">Las reservas son la asignación manual o automática de recursos a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="2eb78-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="2eb78-106">Las reservas manuales consumen la capacidad de un recurso.</span><span class="sxs-lookup"><span data-stu-id="2eb78-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="2eb78-107">Las asignaciones son la asignación de recursos a las tareas del proyecto en la programación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="2eb78-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="2eb78-108">Los recursos pueden ser reales o genéricos.</span><span class="sxs-lookup"><span data-stu-id="2eb78-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="2eb78-109">Idealmente, para los recursos reales, las reservas y asignaciones deben coincidir, porque no difieren.</span><span class="sxs-lookup"><span data-stu-id="2eb78-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="2eb78-110">Sin embargo, Microsoft Dynamics Project Operations no obliga a que se cumpla este contrato.</span><span class="sxs-lookup"><span data-stu-id="2eb78-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="2eb78-111">La vista **Conciliación** muestra los lugares de un administrador de proyecto donde las reservas y asignaciones de un recurso no coinciden.</span><span class="sxs-lookup"><span data-stu-id="2eb78-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
