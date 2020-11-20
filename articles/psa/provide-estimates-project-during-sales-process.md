---
title: Proporcionar estimaciones de trabajo para un proyecto durante el proceso de ventas
description: Cómo proporcionar estimaciones de trabajo para un proyecto durante el proceso de ventas en Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120609"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="55866-103">Proporcionar estimaciones de trabajo para un proyecto durante el proceso de ventas (Project Service)</span><span class="sxs-lookup"><span data-stu-id="55866-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="55866-104">Durante el proceso de ventas, puede realizar estimaciones de ventas partiendo de cero con líneas de oferta.</span><span class="sxs-lookup"><span data-stu-id="55866-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="55866-105">Las capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] proporcionan una forma más científica y determinista de proporcionar estimaciones de ventas desglosando los elementos de trabajo y asociando los atributos relevantes que contribuyen en las estimaciones del proyecto en la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="55866-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="55866-106">Una vez que logra una venta, puede usar la estructura de descomposición del trabajo asociada en el plan del proyecto, refinándola en la medida necesaria para una correcta realización del proyecto.</span><span class="sxs-lookup"><span data-stu-id="55866-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="55866-107">Vincule un proyecto a una línea de oferta</span><span class="sxs-lookup"><span data-stu-id="55866-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="55866-108">Al crear una línea de oferta basada en proyecto, puede crear un nuevo proyecto desde la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="55866-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="55866-109">A continuación puede usar plantillas de proyectos, que son planes de proyecto y estimaciones financieras preconfiguradas estándar comunes a la organización, o una copia de un plan y estimaciones de proyecto a partir de un proyecto pasado.</span><span class="sxs-lookup"><span data-stu-id="55866-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="55866-110">Cuando crea un proyecto, seleccionar una plantilla de proyecto proporciona una base para refinar el plan del proyecto, las estimaciones y los requisitos de rol.</span><span class="sxs-lookup"><span data-stu-id="55866-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="55866-111">Al crear el proyecto desde la oferta, el proyecto se asociará automáticamente con la línea de la oferta.</span><span class="sxs-lookup"><span data-stu-id="55866-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="55866-112">Componentes estimación del proyecto</span><span class="sxs-lookup"><span data-stu-id="55866-112">Project estimate components</span></span>  
 <span data-ttu-id="55866-113">La estructura de descomposición del trabajo en un proyecto proporciona una forma de desglosar el trabajo en tareas, mantener una jerarquía de tareas y asignar una estimación de esfuerzo necesario para realizar cada tarea.</span><span class="sxs-lookup"><span data-stu-id="55866-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="55866-114">También puede asociar roles una tarea para indicar una estimación del tipo de recurso necesario para completar una tarea y una programación.</span><span class="sxs-lookup"><span data-stu-id="55866-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="55866-115">La estructura de descomposición del trabajo ayuda a determinar el esfuerzo de trabajo y las estimaciones de programación.</span><span class="sxs-lookup"><span data-stu-id="55866-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="55866-116">De forma predeterminada, el proyecto usa listas de precios predeterminadas que usted definió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="55866-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="55866-117">El coste y los precios de ventas definidos en las listas de precios ayudan a determinar las estimaciones financieras del desglose de trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="55866-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="55866-118">Si el proyecto está asociado a una oferta, y la oferta tiene una lista de precios diferente de la predeterminada, la lista de precios de la oferta se usa para realizar estimaciones financieras.</span><span class="sxs-lookup"><span data-stu-id="55866-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="55866-119">Importar estimaciones de un proyecto a una oferta</span><span class="sxs-lookup"><span data-stu-id="55866-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="55866-120">Una vez que tenga estimaciones del proyecto en el proyecto, puede importarlas en la línea de oferta:</span><span class="sxs-lookup"><span data-stu-id="55866-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="55866-121">En **Detalles de línea de oferta**, haga clic en **Importar desde estimaciones**.</span><span class="sxs-lookup"><span data-stu-id="55866-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="55866-122">Seleccione si desea importar las estimaciones resumidas por tipo de transacción, rol, o nivel de nodo de la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="55866-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="55866-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="55866-123">See Also</span></span>  
 [<span data-ttu-id="55866-124">Guía del jefe de proyecto</span><span class="sxs-lookup"><span data-stu-id="55866-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
