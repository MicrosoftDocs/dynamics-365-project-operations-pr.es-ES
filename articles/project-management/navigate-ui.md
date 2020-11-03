---
title: Navegación por la interfaz de usuario
description: Este tema proporciona información sobre la gestión de proyectos en las operaciones de proyectos de Dynamics 365.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085066"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="88d71-103">Navegación por la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="88d71-103">Navigating the user interface</span></span>

<span data-ttu-id="88d71-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="88d71-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="88d71-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="88d71-105">Overview</span></span>

<span data-ttu-id="88d71-106">El formulario principal del proyecto se divide en varias pestañas.</span><span class="sxs-lookup"><span data-stu-id="88d71-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="88d71-107">Cada pestaña representa un nivel de detalle diferente dentro del proyecto.</span><span class="sxs-lookup"><span data-stu-id="88d71-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="88d71-108">**Resumen** : proporciona una descripción del proyecto y agrega tanto el rendimiento planificado como el real del proyecto.</span><span class="sxs-lookup"><span data-stu-id="88d71-108">**Summary** : Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Pestaña y campos de resumen](media/navigation7.png)

- <span data-ttu-id="88d71-110">**Tareas** : proporciona los detalles sobre la estructura de descomposición del trabajo representada por una vista de cuadrícula, una vista de panel y un diagrama de Gantt.</span><span class="sxs-lookup"><span data-stu-id="88d71-110">**Tasks** : Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Pestaña y campos de tareas](media/navigation8.png)

- <span data-ttu-id="88d71-112">**Equipo** : proporciona detalles sobre los participantes del proyecto.</span><span class="sxs-lookup"><span data-stu-id="88d71-112">**Team** : Provides details regarding the project participants.</span></span> <span data-ttu-id="88d71-113">El esfuerzo asignado a cada miembro del equipo también se resume en esta vista.</span><span class="sxs-lookup"><span data-stu-id="88d71-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Pestaña y campos de equipos](media/navigation9.png)

- <span data-ttu-id="88d71-115">**Asignaciones de recursos** : proporciona una vista por fases del esfuerzo para cada recurso en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="88d71-115">**Resource assignments** : Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Pestaña y campos de asignaciones de recursos](media/navigation10.png)

- <span data-ttu-id="88d71-117">**Conciliación de recursos** : proporciona una vista por fases de tiempo de las diferencias entre las asignaciones de cada recurso nombrado y sus reservas.</span><span class="sxs-lookup"><span data-stu-id="88d71-117">**Resource reconciliation** : Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Pestaña y campos de conciliación de recursos](media/navigation11.png)

- <span data-ttu-id="88d71-119">**Estimados** : proporciona una vista por fases temporales de las estimaciones de costes y ventas de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="88d71-119">**Estimates** : Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Pestaña y campos de estimaciones](media/navigation12.png)

- <span data-ttu-id="88d71-121">**Rastreo** : proporciona una vista que muestra el progreso de las tareas en estructura de descomposición del trabajo por esfuerzo, coste y ventas.</span><span class="sxs-lookup"><span data-stu-id="88d71-121">**Tracking** : Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Pestaña y campos de seguimiento](media/navigation13.png)

- <span data-ttu-id="88d71-123">**Ventas** : proporciona enlaces profundos a ofertas y contratos asociados con el proyecto.</span><span class="sxs-lookup"><span data-stu-id="88d71-123">**Sales** : Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="88d71-124">**Estimaciones de gastos** : proporciona una cuadrícula que define los gastos del proyecto en función de las categorías de gastos de la organización.</span><span class="sxs-lookup"><span data-stu-id="88d71-124">**Expense Estimates** : Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Pestaña y campos de estimaciones de gastos](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="88d71-126">Controles de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="88d71-126">Grid controls</span></span>

<span data-ttu-id="88d71-127">A continuación se ofrece una breve descripción general de los controles típicos que se encuentran en las distintas pestañas de planificación de proyectos.</span><span class="sxs-lookup"><span data-stu-id="88d71-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="88d71-128">Actualizar</span><span class="sxs-lookup"><span data-stu-id="88d71-128">Refresh</span></span>

<span data-ttu-id="88d71-129">**Actualizar** : recupera los datos más recientes del servidor si se produjeron cambios después de cargar la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="88d71-129">**Refresh** : Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Botón Actualizar](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="88d71-131">Agrupar por</span><span class="sxs-lookup"><span data-stu-id="88d71-131">Group by</span></span>

<span data-ttu-id="88d71-132">**Agrupar por** : actualiza la agrupación de filas en la cuadrícula para reflejar recursos, roles o categorías según las necesidades del usuario.</span><span class="sxs-lookup"><span data-stu-id="88d71-132">**Group by** : Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Agrupar por botón](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="88d71-134">Anterior/Siguiente</span><span class="sxs-lookup"><span data-stu-id="88d71-134">Previous/Next</span></span>

<span data-ttu-id="88d71-135">**Anterior**/**Siguiente** : actualiza los períodos de tiempo visibles en las cuadrículas de fases de tiempo.</span><span class="sxs-lookup"><span data-stu-id="88d71-135">**Previous**/**Next** : Update the visible time periods on the time-phased grids.</span></span>

![Botones Anterior y Siguiente](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="88d71-137">Escala temporal</span><span class="sxs-lookup"><span data-stu-id="88d71-137">Timescale</span></span>

<span data-ttu-id="88d71-138">**Escala de tiempo** : cambia la agregación de los datos por fases de tiempo entre días, semanas, meses y años.</span><span class="sxs-lookup"><span data-stu-id="88d71-138">**Timescale** : Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Botón de escala de tiempo](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="88d71-140">Expandir</span><span class="sxs-lookup"><span data-stu-id="88d71-140">Expand</span></span>

<span data-ttu-id="88d71-141">**Expandir** : representa la cuadrícula visible a pantalla completa, lo que brinda más capacidad para ver roles adicionales.</span><span class="sxs-lookup"><span data-stu-id="88d71-141">**Expand** : Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Botón Expandir](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="88d71-143">Fase temporal mediante</span><span class="sxs-lookup"><span data-stu-id="88d71-143">Time-phase by</span></span>

<span data-ttu-id="88d71-144">**Fase temporal mediante** : actualice la agrupación de las filas de la cuadrícula para reflejar las estimaciones de costes para las estimaciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="88d71-144">**Time-phase by** : Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="88d71-145">Este control también se aplica al script de estimación y la cuadrícula de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="88d71-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Fase temporal mediante botón](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="88d71-147">Agregar columna</span><span class="sxs-lookup"><span data-stu-id="88d71-147">Add column</span></span>

<span data-ttu-id="88d71-148">**Añadir columna** : permite al usuario definir las columnas visibles en la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="88d71-148">**Add column** : Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="88d71-149">Solo se pueden agregar columnas listas para usar a las cuadrículas en el formulario **Planificación de proyectos**.</span><span class="sxs-lookup"><span data-stu-id="88d71-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Agregar botón de columna](media/navigation5.png)
