---
title: Guía del administrador de recursos
description: Guía para la administración de proyectos en  Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756081"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="a90f0-103">Guía del administrador de projectos (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a90f0-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a90f0-104">Las capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] de [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ayudan a encontrar los recursos correctos en el momento adecuado para el proyecto correcto y a asegurarse de que todos los recursos se usan eficazmente.</span><span class="sxs-lookup"><span data-stu-id="a90f0-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="a90f0-105">Implemente los consultores de su empresa de manera eficaz con[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a90f0-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="a90f0-106">Esto le proporcionan las herramientas que necesita para programar recursos en función de los requisitos y las programaciones de proyectos de consultoría y de las cualificaciones y la disponibilidad de los consultores.</span><span class="sxs-lookup"><span data-stu-id="a90f0-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="a90f0-107">Puede encontrar rápidamente los consultores más cualificados que estén disponibles para trabajar en proyectos, y puede ver fácilmente cómo programarlos mejor en el transcurso de cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="a90f0-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="a90f0-108">La programación de recursos ayuda a hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a90f0-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="a90f0-109">Asociar recursos a proyectos, en función del grado de coincidencia de las cualificaciones y los niveles de competencia con los requisitos de los recursos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a90f0-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="a90f0-110">Asocie la programación de un recurso con un calendario de proyecto, en función de su disponibilidad y del tiempo libre programado.</span><span class="sxs-lookup"><span data-stu-id="a90f0-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="a90f0-111">El calendario con código de color da indicadores visuales acerca de disponibilidad de recursos.</span><span class="sxs-lookup"><span data-stu-id="a90f0-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="a90f0-112">Revise la capacidad de cada consultor y determine cómo esa capacidad se utiliza actualmente.</span><span class="sxs-lookup"><span data-stu-id="a90f0-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="a90f0-113">Esto puede ayudar a encontrar un consultor que pueda estar infra o sobreutilizado o que trabaje a plena capacidad.</span><span class="sxs-lookup"><span data-stu-id="a90f0-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="a90f0-114">Asigne un porcentaje o un número específico de horas por la capacidad de un trabajador a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="a90f0-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="a90f0-115">Cree reservas de recursos de grupo.</span><span class="sxs-lookup"><span data-stu-id="a90f0-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="a90f0-116">Recursos de tentativa de reservas o reservas en firme y convierta las tentativas de reserva de horas en reservas en firme de horas en un paso.</span><span class="sxs-lookup"><span data-stu-id="a90f0-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="a90f0-117">Forme automáticamente un equipo del proyecto en función de los recursos definidos en una estructura de descomposición del trabajo para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="a90f0-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="a90f0-118">Atienda las solicitudes de recursos (reserva, propuesta, búsqueda de recursos de sustitución).</span><span class="sxs-lookup"><span data-stu-id="a90f0-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="a90f0-119">Asigne recursos de acuerdo con un modelo central (el administrador de recursos asigna) o híbrido (el administrador de recursos y otros administradores pueden asignar).</span><span class="sxs-lookup"><span data-stu-id="a90f0-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="a90f0-120">Para obtener más información acerca de cómo configurar una central con modelo de administración de recursos híbrido, consulte [Configure las opciones adicionales de los parámetros (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a90f0-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="a90f0-121">Puede administrar los recursos eficazmente entre proyectos y asegurarse de que los proyectos está dotados del personal adecuado.</span><span class="sxs-lookup"><span data-stu-id="a90f0-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="a90f0-122">Deberá realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a90f0-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="a90f0-123">[Administre solicitudes de recursos](../project-service/manage-resource-requests.md)</span><span class="sxs-lookup"><span data-stu-id="a90f0-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="a90f0-124">Asociar las cualificaciones y competencias de sus consultores a los proyectos correctos.</span><span class="sxs-lookup"><span data-stu-id="a90f0-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="a90f0-125">[Ver disponibilidad de los recursos](../project-service/view-resource-availability.md)</span><span class="sxs-lookup"><span data-stu-id="a90f0-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="a90f0-126">Comprobar la disponibilidad de los consultores en una vista de calendario.</span><span class="sxs-lookup"><span data-stu-id="a90f0-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="a90f0-127">[Ver uso de recursos](../project-service/view-resource-utilization.md)</span><span class="sxs-lookup"><span data-stu-id="a90f0-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="a90f0-128">Ver el porcentaje de tiempo que sus consultores están reservados actualmente.</span><span class="sxs-lookup"><span data-stu-id="a90f0-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="a90f0-129">[Programe recursos para un proyecto](../project-service/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="a90f0-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="a90f0-130">Programe consultores para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="a90f0-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="a90f0-131">Para obtener más información sobre el envío de solicitudes de recursos para proyectos individuales, consulte [Envío de solicitudes de recursos](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="a90f0-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a90f0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a90f0-132">See Also</span></span>  
 <span data-ttu-id="a90f0-133">[Información general de Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="a90f0-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="a90f0-134">[Guía del administrador](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a90f0-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="a90f0-135">[Guía de administrador de cuentas](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a90f0-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="a90f0-136">[Guía del jefe de proyecto](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a90f0-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="a90f0-137">Guía de tiempo, gastos y colaboración</span><span class="sxs-lookup"><span data-stu-id="a90f0-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
