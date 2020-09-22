---
title: Configuración del proyecto
description: En este tema se proporciona información sobre la configuración de administración del proyecto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755981"
---
# <a name="project-settings"></a><span data-ttu-id="58984-103">Configuración del proyecto</span><span class="sxs-lookup"><span data-stu-id="58984-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="58984-104">Use la siguiente configuración para obtener acceso a las características de planificación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="58984-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="58984-105">Plantilla de trabajo</span><span class="sxs-lookup"><span data-stu-id="58984-105">Work template</span></span>

<span data-ttu-id="58984-106">Para crear una programación de proyecto, cree una plantilla de calendario de proyecto que defina la cantidad de horas de trabajo por día y los cierres de negocios.</span><span class="sxs-lookup"><span data-stu-id="58984-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="58984-107">Para crear una plantilla de calendario de proyecto, asocie una plantilla de trabajo con el campo **Plantilla de calendario** para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="58984-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="58984-108">Siga estos pasos para crear una plantilla de trabajo.</span><span class="sxs-lookup"><span data-stu-id="58984-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="58984-109">En PSA, en el panel de navegación izquierdo, haga clic en **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="58984-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="58984-110">En la página de la lista **Recursos**, abra un registro de usuario y, a continuación, seleccione **Mostrar horas laborables**.</span><span class="sxs-lookup"><span data-stu-id="58984-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="58984-111">Asegúrese de permitir ventanas emergentes en la página del explorador.</span><span class="sxs-lookup"><span data-stu-id="58984-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="58984-112">Esto le permitirá ver las horas de trabajo establecidas para el recurso.</span><span class="sxs-lookup"><span data-stu-id="58984-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="58984-113">En la pestaña **Vista mensual** , haga clic en **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="58984-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="58984-114">Aparecerá una lista con tres opciones:</span><span class="sxs-lookup"><span data-stu-id="58984-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="58984-115">Nueva programación semanal</span><span class="sxs-lookup"><span data-stu-id="58984-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="58984-116">Programación de trabajo para un día</span><span class="sxs-lookup"><span data-stu-id="58984-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="58984-117">Tiempo libre</span><span class="sxs-lookup"><span data-stu-id="58984-117">Time Off</span></span>

> ![Opciones de configuración](media/project-13.png)

4. <span data-ttu-id="58984-119">Seleccione **Nueva programación semanal** y, a continuación, establezca las opciones para esta programación del recurso.</span><span class="sxs-lookup"><span data-stu-id="58984-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="58984-120">Puede establecer una programación semanal recurrente, parámetros de horas diarias, cierres comerciales, etc.</span><span class="sxs-lookup"><span data-stu-id="58984-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="58984-121">Establezca el rango de fechas, seleccione **Guardar** y, a continuación, haga clic en **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="58984-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="58984-122">Vuelva a la página de lista **Recursos** y seleccione el recurso para el que estableció las horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="58984-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="58984-123">Seleccione **Establecer calendario como** para establecer la plantilla de trabajo.</span><span class="sxs-lookup"><span data-stu-id="58984-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="58984-124">En el cuadro de diálogo **Plantilla de trabajo**, introduzca un nombre para la plantilla de trabajo y, a continuación, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="58984-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="58984-125">Ahora puede asociar la plantilla de trabajo con una plantilla de calendario de proyecto.</span><span class="sxs-lookup"><span data-stu-id="58984-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="58984-126">Roles de recursos</span><span class="sxs-lookup"><span data-stu-id="58984-126">Resource roles</span></span>

<span data-ttu-id="58984-127">El término *rol de recurso* hace referencia al conjunto de conocimientos, competencias y certificaciones que una persona necesitará para poder realizar un conjunto específico de tareas en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="58984-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="58984-128">PSA le permite establecer el coste y facturar el tiempo de un recurso en función del rol al que está asociado el recurso.</span><span class="sxs-lookup"><span data-stu-id="58984-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="58984-129">Cada organización debe configurar estos roles mediante la navegación izquierda en el menú **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="58984-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="58984-130">Cada organización debe configurar estos roles en la página **Categorías de recursos activas**.</span><span class="sxs-lookup"><span data-stu-id="58984-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="58984-131">Para abrir esta página, en el panel de navegación izquierdo, seleccione **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="58984-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="58984-132">Listas de precios</span><span class="sxs-lookup"><span data-stu-id="58984-132">Price lists</span></span>

<span data-ttu-id="58984-133">Las listas de precios le permiten establecer costes y precios de venta para roles de recursos, categorías de gastos, productos y otros elementos en una organización.</span><span class="sxs-lookup"><span data-stu-id="58984-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="58984-134">Antes de establecer estimaciones financieras para el trabajo que deben realizarse para un proyecto, debe crear un coste de apoyo y una lista de precios de venta.</span><span class="sxs-lookup"><span data-stu-id="58984-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="58984-135">En la sección de parámetros, también debe configurar una lista predeterminada de costes y precios de venta que se aplique a todos los proyectos que se crean en la organización.</span><span class="sxs-lookup"><span data-stu-id="58984-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="58984-136">En la página **Parámetros de proyecto activos**, asegúrese de configurar una lista predeterminada de costes y precios de venta.</span><span class="sxs-lookup"><span data-stu-id="58984-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
