---
title: Información general del asistente de programación
description: Este tema proporciona información sobre cómo trabajar con el asistente de programación para reservar recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279249"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="33880-103">Información general del asistente de programación</span><span class="sxs-lookup"><span data-stu-id="33880-103">Schedule assistant overview</span></span>

<span data-ttu-id="33880-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="33880-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33880-105">El asistente de programación se utiliza para reservar recursos según los requisitos definidos por el gerente de proyecto.</span><span class="sxs-lookup"><span data-stu-id="33880-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="33880-106">El asistente de programación se basa en los parámetros proporcionados en el requisito de recursos para encontrar el recurso.</span><span class="sxs-lookup"><span data-stu-id="33880-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="33880-107">El asistente de programación recomienda recursos que coinciden con los requisitos relevantes, como ventanas de tiempo o habilidades necesarias.</span><span class="sxs-lookup"><span data-stu-id="33880-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="33880-108">Una vez identificados los recursos adecuados, el administrador de recursos o proyecto puede reservar el recurso para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="33880-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="33880-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="33880-109">Prerequisites</span></span>

<span data-ttu-id="33880-110">El asistente de programación es parte de la solución Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="33880-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="33880-111">Esta solución se incluye e instala con Dynamics 365 Project Operations, Dynamics 365 Field Service y Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="33880-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="33880-112">Asociar requisitos y recursos</span><span class="sxs-lookup"><span data-stu-id="33880-112">Matching requirements and resources</span></span>

<span data-ttu-id="33880-113">Un requisito de recursos generado se basa en detalles como:</span><span class="sxs-lookup"><span data-stu-id="33880-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="33880-114">Características</span><span class="sxs-lookup"><span data-stu-id="33880-114">Characteristics</span></span>
-   <span data-ttu-id="33880-115">Roles</span><span class="sxs-lookup"><span data-stu-id="33880-115">Roles</span></span>
-   <span data-ttu-id="33880-116">Unidades de negocio</span><span class="sxs-lookup"><span data-stu-id="33880-116">Business units</span></span>
-   <span data-ttu-id="33880-117">Preferencias de recursos</span><span class="sxs-lookup"><span data-stu-id="33880-117">Resource preferences</span></span>
-   <span data-ttu-id="33880-118">Contornos de esfuerzo</span><span class="sxs-lookup"><span data-stu-id="33880-118">Effort contours</span></span>
-   <span data-ttu-id="33880-119">Zona horaria</span><span class="sxs-lookup"><span data-stu-id="33880-119">Time zone</span></span>

<span data-ttu-id="33880-120">El asistente de programación utiliza estos detalles para filtrar recursos.</span><span class="sxs-lookup"><span data-stu-id="33880-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="33880-121">Iniciar el asistente de programación</span><span class="sxs-lookup"><span data-stu-id="33880-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="33880-122">Hay dos formas de iniciar el asistente de programación.</span><span class="sxs-lookup"><span data-stu-id="33880-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="33880-123">Si está utilizando el modo híbrido, en la cuadrícula de miembros del equipo puede seleccionar cualquier miembro del equipo con un requisito de recursos sin rellenar y luego seleccionar **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="33880-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="33880-124">Si está utilizando el modo central, el administrador de recursos busca y selecciona el recurso.</span><span class="sxs-lookup"><span data-stu-id="33880-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="33880-125">Filtros del asistente de programación</span><span class="sxs-lookup"><span data-stu-id="33880-125">Schedule assistant filters</span></span>

<span data-ttu-id="33880-126">Una vez que se ejecuta el asistente de programación, los detalles del requisito de recursos se muestran como valores filtrados en el panel izquierdo.</span><span class="sxs-lookup"><span data-stu-id="33880-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="33880-127">El administrador de recursos o el administrador de proyectos puede ajustar los resultados ajustando los filtros para satisfacer las necesidades de programación.</span><span class="sxs-lookup"><span data-stu-id="33880-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="33880-128">El panel de filtro muestra opciones relacionadas con el trabajo, que incluyen:</span><span class="sxs-lookup"><span data-stu-id="33880-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="33880-129">Inicio y finalización del trabajo</span><span class="sxs-lookup"><span data-stu-id="33880-129">Work start and end</span></span>
-   <span data-ttu-id="33880-130">Características</span><span class="sxs-lookup"><span data-stu-id="33880-130">Characteristics</span></span>
-   <span data-ttu-id="33880-131">Roles</span><span class="sxs-lookup"><span data-stu-id="33880-131">Roles</span></span>
-   <span data-ttu-id="33880-132">Unidades organizativas</span><span class="sxs-lookup"><span data-stu-id="33880-132">Organizational units</span></span>
-   <span data-ttu-id="33880-133">Empresa de recursos</span><span class="sxs-lookup"><span data-stu-id="33880-133">Resourcing company</span></span>
-   <span data-ttu-id="33880-134">Tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="33880-134">Resource types</span></span>
-   <span data-ttu-id="33880-135">Recursos preferidos</span><span class="sxs-lookup"><span data-stu-id="33880-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]