---
title: Realizar un seguimiento del estado de un proyecto
description: Cómo hacer seguimiento del estado de un proyecto en Project Service
author: ruhercul
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014407"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="c0c04-103">Seguir el estado de un proyecto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c0c04-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c0c04-104">Use las [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] para realizar un seguimiento del progreso del proyecto de un cliente.</span><span class="sxs-lookup"><span data-stu-id="c0c04-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="c0c04-105">A medida que la participación progresa, las fases del proyecto se actualizan para reflejar la fase de la participación:</span><span class="sxs-lookup"><span data-stu-id="c0c04-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="c0c04-106">**Nuevo**</span><span class="sxs-lookup"><span data-stu-id="c0c04-106">**New**</span></span>    | <span data-ttu-id="c0c04-107">Cuando cree un proyecto, la fase se establece como **Nueva**.</span><span class="sxs-lookup"><span data-stu-id="c0c04-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="c0c04-108">Si creó el proyecto desde una plantilla, en esta etapa el proyecto pude tener una programación, estimaciones, y datos del equipo.</span><span class="sxs-lookup"><span data-stu-id="c0c04-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="c0c04-109">De lo contrario, será la información general del proyecto y deberá especificar manualmente el resto de los componentes del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c0c04-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="c0c04-110">**Oferta**</span><span class="sxs-lookup"><span data-stu-id="c0c04-110">**Quote**</span></span>   |      <span data-ttu-id="c0c04-111">Cuando asocia un proyecto a una oferta o lo crea desde una oferta, la fase del proyecto se establece en **Oferta** y las fechas de inicio y finalización estimadas también se actualizan.</span><span class="sxs-lookup"><span data-stu-id="c0c04-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="c0c04-112">Cuando el proyecto está en la fase de oferta, los detalles de la oferta se muestran en la pestaña **Ventas** en la página **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c0c04-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="c0c04-113">**Planificar**</span><span class="sxs-lookup"><span data-stu-id="c0c04-113">**Plan**</span></span>   |                                     <span data-ttu-id="c0c04-114">Si gana una oferta asociada a un proyecto y, cuando la participación progresa a la fase de contrato, la fase del proyecto se actualiza a **Plan**.</span><span class="sxs-lookup"><span data-stu-id="c0c04-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="c0c04-115">Los detalles del contrato se muestran en la pestaña **Ventas** en la página **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c0c04-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="c0c04-116">**Completada**</span><span class="sxs-lookup"><span data-stu-id="c0c04-116">**Complete**</span></span> |                    <span data-ttu-id="c0c04-117">Cuando se completa el trabajo del proyecto, puede cambiar la fase a **Completado**.</span><span class="sxs-lookup"><span data-stu-id="c0c04-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="c0c04-118">Cuando la fase del proyecto se establece como completada, se entiende que el trabajo se ha completado al 100% pero el proyecto se mantiene abierto para cualquier entrada de tiempo o gasto pendiente de registrar.</span><span class="sxs-lookup"><span data-stu-id="c0c04-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="c0c04-119">**Cerrar**</span><span class="sxs-lookup"><span data-stu-id="c0c04-119">**Close**</span></span>   |           <span data-ttu-id="c0c04-120">Cuando todas las transacciones se han registrado en el proyecto y no espera que se registren más, puede establecer manualmente la fase a **Cierre**.</span><span class="sxs-lookup"><span data-stu-id="c0c04-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="c0c04-121">Cuando el proyecto se establece en **Cierre**, no puede registrar más transacciones en el proyecto y el proyecto será de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c0c04-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="c0c04-122">Para realizar un seguimiento del estado de un proyecto</span><span class="sxs-lookup"><span data-stu-id="c0c04-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="c0c04-123">Vaya a **Project Service > Proyectos**.</span><span class="sxs-lookup"><span data-stu-id="c0c04-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="c0c04-124">Haga clic en el proyecto en el que desea trabajar.</span><span class="sxs-lookup"><span data-stu-id="c0c04-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="c0c04-125">En la barra en la parte superior de la pantalla, seleccione la flecha hacia abajo junto al nombre del proyecto y, después, haga clic en **Seguimiento de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c0c04-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="c0c04-126">Seleccione **Seguimiento del esfuerzo** o **Seguimiento de costes** en la lista desplegable situada encima de la lista de tareas.</span><span class="sxs-lookup"><span data-stu-id="c0c04-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="c0c04-127">Haga doble clic en cualquier tarea para editarla.</span><span class="sxs-lookup"><span data-stu-id="c0c04-127">Double-click any task to edit it.</span></span> <span data-ttu-id="c0c04-128">También puede mover o cambiar el tamaño de las barras en el diagrama de Gantt para cambiar el tiempo y el progreso para una tarea.</span><span class="sxs-lookup"><span data-stu-id="c0c04-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="c0c04-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0c04-129">See Also</span></span>  
 [<span data-ttu-id="c0c04-130">Guía del jefe de proyecto</span><span class="sxs-lookup"><span data-stu-id="c0c04-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]