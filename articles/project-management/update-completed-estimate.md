---
title: Actualizar estimado al finalizar
description: En este tema se proporciona información sobre cómo actualizar la proyección de esfuerzo en un proyecto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127224"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="7393c-103">Actualizar estimado al finalizar</span><span class="sxs-lookup"><span data-stu-id="7393c-103">Update estimate at completion</span></span>

<span data-ttu-id="7393c-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="7393c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7393c-105">Es frecuente que un administrador de proyecto revise las estimaciones originales de una tarea.</span><span class="sxs-lookup"><span data-stu-id="7393c-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="7393c-106">Las reproyecciones de proyectos son la percepción de las estimaciones de un administrador de proyecto según estado actual de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="7393c-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="7393c-107">Sin embargo, no recomendamos que los jefes de proyecto cambien los números de línea de base, ya que la línea de base del proyecto representa la fuente de verdad establecida para la programación y la estimación de costes del proyecto, y todos los interesados en el proyecto la han aceptado.</span><span class="sxs-lookup"><span data-stu-id="7393c-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="7393c-108">Existen dos formas en las que un jefe de proyecto puede reproyectar el esfuerzo en las tareas:</span><span class="sxs-lookup"><span data-stu-id="7393c-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="7393c-109">Anule la estimación para finalizar (ETC) predeterminada con una nueva estimación del esfuerzo restante real en la tarea.</span><span class="sxs-lookup"><span data-stu-id="7393c-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="7393c-110">Anular el porcentaje de progreso predeterminado con una nueva estimación del progreso real de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7393c-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="7393c-111">Cada uno de estos enfoques genera un nuevo cálculo del ETC, la estimación al finalizar (EAF) y el porcentaje de progreso de la tarea, y la variación del esfuerzo proyectado en una tarea.</span><span class="sxs-lookup"><span data-stu-id="7393c-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="7393c-112">El EAF, ETC y el porcentaje de progreso en las tareas de resumen se recalculan y producen una nueva proyección de la variación del esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="7393c-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
