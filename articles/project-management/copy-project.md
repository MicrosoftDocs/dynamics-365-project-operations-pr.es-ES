---
title: Copiar un proyecto
description: En este tema se proporciona información sobre la copia de proyectos en Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479540"
---
# <a name="copy-a-project"></a><span data-ttu-id="53c89-103">Copiar un proyecto</span><span class="sxs-lookup"><span data-stu-id="53c89-103">Copy a project</span></span>

<span data-ttu-id="53c89-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="53c89-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="53c89-105">Con Dynamics 365 Project Operations, puede crear rápidamente nuevos proyectos seleccionando **Copiar proyecto** en el formulario **Proyectos**.</span><span class="sxs-lookup"><span data-stu-id="53c89-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="53c89-106">Para copiar un proyecto, abra el proyecto que desea copiar y luego seleccione **Copiar proyecto**.</span><span class="sxs-lookup"><span data-stu-id="53c89-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="53c89-107">La acción copiará:</span><span class="sxs-lookup"><span data-stu-id="53c89-107">The action will copy:</span></span>

- <span data-ttu-id="53c89-108">Propiedades del proyecto (la fecha de inicio estimada se copia del proyecto de origen)</span><span class="sxs-lookup"><span data-stu-id="53c89-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="53c89-109">La estructura de descomposición del trabajo</span><span class="sxs-lookup"><span data-stu-id="53c89-109">The Work breakdown structure</span></span>
- <span data-ttu-id="53c89-110">Miembros del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="53c89-110">Project team members</span></span>
- <span data-ttu-id="53c89-111">Estimaciones de proyecto</span><span class="sxs-lookup"><span data-stu-id="53c89-111">Project estimates</span></span>
- <span data-ttu-id="53c89-112">Estimaciones de gastos del proyecto</span><span class="sxs-lookup"><span data-stu-id="53c89-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="53c89-113">Propiedades del proyecto</span><span class="sxs-lookup"><span data-stu-id="53c89-113">Project properties</span></span>

<span data-ttu-id="53c89-114">Cuando se copia el proyecto, se copian los valores de los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="53c89-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="53c89-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="53c89-115">Name</span></span>
- <span data-ttu-id="53c89-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="53c89-116">Description</span></span>
- <span data-ttu-id="53c89-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="53c89-117">Customer</span></span>
- <span data-ttu-id="53c89-118">Plantilla de calendario</span><span class="sxs-lookup"><span data-stu-id="53c89-118">Calendar Template</span></span>
- <span data-ttu-id="53c89-119">Divisa</span><span class="sxs-lookup"><span data-stu-id="53c89-119">Currency</span></span>
- <span data-ttu-id="53c89-120">Unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="53c89-120">Contracting Unit</span></span>
- <span data-ttu-id="53c89-121">Jefe de proyecto</span><span class="sxs-lookup"><span data-stu-id="53c89-121">Project Manager</span></span>
- <span data-ttu-id="53c89-122">Estado</span><span class="sxs-lookup"><span data-stu-id="53c89-122">Status</span></span>
- <span data-ttu-id="53c89-123">Estado general del proyecto</span><span class="sxs-lookup"><span data-stu-id="53c89-123">Overall Project Status</span></span>
- <span data-ttu-id="53c89-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53c89-124">Comments</span></span>
- <span data-ttu-id="53c89-125">Estimaciones</span><span class="sxs-lookup"><span data-stu-id="53c89-125">Estimates</span></span>
- <span data-ttu-id="53c89-126">Fecha de inicio estimada</span><span class="sxs-lookup"><span data-stu-id="53c89-126">Estimated Start Date</span></span>
- <span data-ttu-id="53c89-127">Fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="53c89-127">Finish Date</span></span>
- <span data-ttu-id="53c89-128">Esfuerzo (horas)</span><span class="sxs-lookup"><span data-stu-id="53c89-128">Effort (Hours)</span></span>
- <span data-ttu-id="53c89-129">Coste estimado de la mano de obra</span><span class="sxs-lookup"><span data-stu-id="53c89-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="53c89-130">Coste estimado de los gastos</span><span class="sxs-lookup"><span data-stu-id="53c89-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="53c89-131">Estructura de descomposición del trabajo</span><span class="sxs-lookup"><span data-stu-id="53c89-131">Work breakdown structure</span></span>

<span data-ttu-id="53c89-132">Cuando se copia el proyecto, se copia toda la estructura de descomposición del trabajo cargada por los recursos.</span><span class="sxs-lookup"><span data-stu-id="53c89-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="53c89-133">Los recursos con nombre se sustituyen por recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="53c89-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="53c89-134">Si los recursos con nombre no tienen las mismas horas de trabajo que el recurso genérico, la programación se volverá a calcular y la duración de las tareas puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="53c89-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="53c89-135">Miembros del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="53c89-135">Project team members</span></span>

<span data-ttu-id="53c89-136">Cuando un equipo de proyecto se copia desde el proyecto de origen, se copian los recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="53c89-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="53c89-137">Las asignaciones de recursos genéricos también se mantienen como si estuvieran en el proyecto de origen.</span><span class="sxs-lookup"><span data-stu-id="53c89-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="53c89-138">Los recursos con nombre se convertirán en miembros del equipo genéricos.</span><span class="sxs-lookup"><span data-stu-id="53c89-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="53c89-139">Estimaciones</span><span class="sxs-lookup"><span data-stu-id="53c89-139">Estimates</span></span>

<span data-ttu-id="53c89-140">Cuando se copia el proyecto, las líneas de estimación de recursos y gastos se copian del proyecto de origen.</span><span class="sxs-lookup"><span data-stu-id="53c89-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="53c89-141">Para obtener información sobre cómo acceder mediante programación a Copiar proyecto, consulte [Desarrollar plantillas de proyectos con Copy Project](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="53c89-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
