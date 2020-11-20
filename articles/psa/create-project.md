---
title: Crear un proyecto
description: Cómo crear un pojecto en Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: de26bb4c3fa0ee8abf6edf5494968d1d0403266a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133119"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="31fda-103">Crear un proyecto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="31fda-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="31fda-104">Cree un proyecto usando las capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] cuando desea crear una oportunidad, una oferta o un contrato para servicios basados en proyecto.</span><span class="sxs-lookup"><span data-stu-id="31fda-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="31fda-105">La capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ayudan a administrar el proyecto desde la oportunidad hasta su conclusión.</span><span class="sxs-lookup"><span data-stu-id="31fda-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="31fda-106">Cuando cree un proyecto, también creará una estructura de descomposición del trabajo, que afecta a las ofertas, valoraciones de costo, y administración de recursos.</span><span class="sxs-lookup"><span data-stu-id="31fda-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="31fda-107">Vaya a **Project Service > Proyectos**.</span><span class="sxs-lookup"><span data-stu-id="31fda-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="31fda-108">Haga clic en **Nuevo proyecto**.</span><span class="sxs-lookup"><span data-stu-id="31fda-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="31fda-109">En el área **Resumen**, escriba un nombre para el proyecto y a continuación, especifique tantos detalles como pueda.</span><span class="sxs-lookup"><span data-stu-id="31fda-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="31fda-110">Los elementos marcados con un asterisco rojo (\*) son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="31fda-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="31fda-111">Haga clic en **Guardar** para crear el proyecto para que pueda seguir editándolo.</span><span class="sxs-lookup"><span data-stu-id="31fda-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="31fda-112">A continuación, creará una estructura de descomposición del trabajo para el proyecto para definir las tareas, el tiempo, y los roles de recursos necesarios para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="31fda-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="31fda-113">Al programar, Project Service Automation respeta la zona horaria de la plantilla **Hora de trabajo** aplicada.</span><span class="sxs-lookup"><span data-stu-id="31fda-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="31fda-114">Sin embargo, al visualizar las tareas programadas, las fechas de inicio y finalización de una tarea se mostrarán en la zona horaria del usuario.</span><span class="sxs-lookup"><span data-stu-id="31fda-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="31fda-115">Esto se aplica a otras vistas en fases de tiempo en el formulario **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="31fda-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="31fda-116">Si la zona horaria del usuario no coincide con la zona horaria de la plantilla de hora de trabajo aplicada al proyecto, se producirá una advertencia que explica la diferencia.</span><span class="sxs-lookup"><span data-stu-id="31fda-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="31fda-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="31fda-117">See Also</span></span>  
 [<span data-ttu-id="31fda-118">Guía del jefe de proyecto</span><span class="sxs-lookup"><span data-stu-id="31fda-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
