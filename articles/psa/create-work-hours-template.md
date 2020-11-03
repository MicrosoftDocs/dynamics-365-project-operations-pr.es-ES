---
title: Crear una plantilla de horas laborables
description: Cómo crear una plantilla de horas laborables en Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085158"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="fcf18-103">Crear una plantilla de horas laborables (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fcf18-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fcf18-104">Antes de crear programaciones de proyecto, debe configurar un calendario del proyecto que defina el número de horas laborables que tendrá un día en la programación y los cierres de la empresa.</span><span class="sxs-lookup"><span data-stu-id="fcf18-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="fcf18-105">Esto se realiza con una plantilla de horas laborables, que contiene detalles de horas laborables por día, días libres y otros cierres de la empresa.</span><span class="sxs-lookup"><span data-stu-id="fcf18-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="fcf18-106">Cuando cree un proyecto, asocie una plantilla de trabajo al calendario del proyecto para aplicar la programación para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="fcf18-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="fcf18-107">Hay dos formas de crear una plantilla de horas laborables:</span><span class="sxs-lookup"><span data-stu-id="fcf18-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="fcf18-108">Cree una plantilla de horas laborables basada en el calendario de un recurso.</span><span class="sxs-lookup"><span data-stu-id="fcf18-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="fcf18-109">Cree una nueva plantilla de horas laborables.</span><span class="sxs-lookup"><span data-stu-id="fcf18-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="fcf18-110">Para crear una plantilla de horas laborables basada en el calendario de un recurso</span><span class="sxs-lookup"><span data-stu-id="fcf18-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="fcf18-111">Vaya a **Project Service > Recursos**.</span><span class="sxs-lookup"><span data-stu-id="fcf18-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="fcf18-112">Seleccione el recurso en el que desea basar las horas laborables.</span><span class="sxs-lookup"><span data-stu-id="fcf18-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="fcf18-113">Haga clic en **Guardar calendario como** , escriba un nombre para la plantilla de horas laborables y, a continuación haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="fcf18-113">Click **Save Calendar As** , enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="fcf18-114">Cuando termine de cambiar opciones, haga clic **Guardar y cerrar**.</span><span class="sxs-lookup"><span data-stu-id="fcf18-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="fcf18-115">Haga clic en el botón **Guardar** en la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fcf18-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="fcf18-116">Para crear una nueva plantilla de horas laborables</span><span class="sxs-lookup"><span data-stu-id="fcf18-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="fcf18-117">Vaya a **Project Service > Plantillas de horas laborables**.</span><span class="sxs-lookup"><span data-stu-id="fcf18-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="fcf18-118">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="fcf18-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="fcf18-119">Escriba un nombre para la plantilla de horas laborables.</span><span class="sxs-lookup"><span data-stu-id="fcf18-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="fcf18-120">Seleccione un recurso en el que basar las horas laborables y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="fcf18-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fcf18-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcf18-121">See Also</span></span>  
 [<span data-ttu-id="fcf18-122">Configuración de recursos</span><span class="sxs-lookup"><span data-stu-id="fcf18-122">Set up resources</span></span>](../psa/set-up-resources.md)
