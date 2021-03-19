---
title: Estimaciones de ventas y proyectos
description: En este tema se proporciona información sobre cómo aprovechar la programación y las estimaciones en el proceso de venta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 87dc72b76ec4f88684ef2c702718e1ab631ff936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283929"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="38b1f-103">Estimaciones de ventas y proyectos</span><span class="sxs-lookup"><span data-stu-id="38b1f-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="38b1f-104">Durante el proceso de venta, puede crear estimaciones de ventas vinculando un proyecto a una oferta de ventas.</span><span class="sxs-lookup"><span data-stu-id="38b1f-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="38b1f-105">De esta manera, la estimación determinista puede producirse durante el proceso de ventas para aprovechar las capacidades de programación y estimación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="38b1f-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="38b1f-106">Si la venta se lleva a cabo, puede usarse la programación que se utilizó para fines de estimación de ventas como base para un mayor refinamiento del plan del proyecto.</span><span class="sxs-lookup"><span data-stu-id="38b1f-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="38b1f-107">Vinculación de un proyecto a una línea de oferta</span><span class="sxs-lookup"><span data-stu-id="38b1f-107">Linking a project to a quote line</span></span>

<span data-ttu-id="38b1f-108">Cuando cree una línea de oferta basada en un proyecto, podrá crear un nuevo proyecto o asociar un proyecto existente en la página **Línea de oferta**.</span><span class="sxs-lookup"><span data-stu-id="38b1f-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulario de línea de oferta](media/project-8.png)
 
<span data-ttu-id="38b1f-110">Cuando cree un proyecto nuevo a partir de los detalles de la línea de oferta, puede aprovechar las plantillas de proyecto.</span><span class="sxs-lookup"><span data-stu-id="38b1f-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="38b1f-111">Las plantillas de proyecto son proyectos modelo que representan planes de proyecto estándar y estimaciones financieras que son típicas en una organización.</span><span class="sxs-lookup"><span data-stu-id="38b1f-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="38b1f-112">También pueden representar copias de planes de proyectos y estimaciones de proyectos pasados.</span><span class="sxs-lookup"><span data-stu-id="38b1f-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detalles de línea de oferta](media/project-9.png)
  
<span data-ttu-id="38b1f-114">Al crear el proyecto desde la oferta, el proyecto se asociará automáticamente con la línea de la oferta.</span><span class="sxs-lookup"><span data-stu-id="38b1f-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="38b1f-115">Componentes de estimaciones en un proyecto</span><span class="sxs-lookup"><span data-stu-id="38b1f-115">Components of estimates in a project</span></span>

<span data-ttu-id="38b1f-116">Una programación le permite dividir el trabajo en tareas, mantener una jerarquía de ellas, determinar los recursos necesarios para completar una y asignar una estimación del esfuerzo necesario para completarla.</span><span class="sxs-lookup"><span data-stu-id="38b1f-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="38b1f-117">Puede definir el esfuerzo de trabajo y las estimaciones de programación mediante los campos en la pestaña **Programación** de la página **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="38b1f-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="38b1f-118">Debido a que una lista de precios está asociada con el proyecto, las estimaciones financieras se calculan mediante los costes y los precios de venta definidos en la lista de precios.</span><span class="sxs-lookup"><span data-stu-id="38b1f-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="38b1f-119">Importación de estimaciones de un proyecto a una oferta</span><span class="sxs-lookup"><span data-stu-id="38b1f-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="38b1f-120">Después de definir las estimaciones del proyecto, puede importarlas en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="38b1f-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="38b1f-121">En la página **Detalles de línea de oferta**, seleccione **Importar desde estimaciones** en la cinta para resumir las estimaciones de proyecto por tipo de transacción, rol o nivel de tarea.</span><span class="sxs-lookup"><span data-stu-id="38b1f-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]