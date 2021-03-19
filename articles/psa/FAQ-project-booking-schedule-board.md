---
title: Crear una reserva de proyecto desde el tablero Programación
description: En este tema se proporciona información sobre cómo crear una reserva de proyecto desde el tablero Programación.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286134"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="c4531-103">Crear una reserva de proyecto desde el tablero Programación</span><span class="sxs-lookup"><span data-stu-id="c4531-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c4531-104">Puede reservar un recurso para un proyecto directamente desde la pestaña **Equipo** del proyecto o generando un requisito de recursos desde una asignación genérica de miembro del equipo y después cumpliendo el requisito generado mediante un miembro del equipo de proyecto.</span><span class="sxs-lookup"><span data-stu-id="c4531-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="c4531-105">También puede reservar un recurso para un proyecto directamente desde el tablero Programación.</span><span class="sxs-lookup"><span data-stu-id="c4531-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="c4531-106">Esto se puede hacer de tres maneras:</span><span class="sxs-lookup"><span data-stu-id="c4531-106">There are three ways to do this:</span></span>

- <span data-ttu-id="c4531-107">**Reservar a partir de un requisito de recurso generado**: puede generar un requisito de recursos tras crear un recurso genérico y asignar tareas en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="c4531-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="c4531-108">**Reservar desde el requisito principal:** los requisitos principales aparecen en el tablero Programación en la pestaña **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c4531-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="c4531-109">**Reservar a partir de un nuevo requisito de recurso:** puede crear un requisito de recursos desde cero y asociarlo a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="c4531-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="c4531-110">En el tablero Programación, el requisito de recurso aparece en la pestaña **Requisitos abiertos**.</span><span class="sxs-lookup"><span data-stu-id="c4531-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="c4531-111">Reserve a partir de un requisito de recurso generado</span><span class="sxs-lookup"><span data-stu-id="c4531-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="c4531-112">Puede crear un recurso genérico y asignarlo a una o varias tareas en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="c4531-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="c4531-113">A continuación, puede genere un requisito de recurso a partir del miembro de equipo genérico.</span><span class="sxs-lookup"><span data-stu-id="c4531-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="c4531-114">En el tablero Programación, este recurso aparecerá en la pestaña **Requisitos abiertos**. Puede que tenga que usar filtros de columna en la cuadrícula si tiene muchos requisitos abiertos.</span><span class="sxs-lookup"><span data-stu-id="c4531-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="c4531-115">![Pestaña Abrir requisitos en el tablero de programación](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de pantalla de la tabla de reservas y asignaciones")</span><span class="sxs-lookup"><span data-stu-id="c4531-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="c4531-116">Seleccione el requisito.</span><span class="sxs-lookup"><span data-stu-id="c4531-116">Select the requirement.</span></span> <span data-ttu-id="c4531-117">La pestaña **Buscar disponibilidad** aparecerá en la parte superior de fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="c4531-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="c4531-118">Al seleccionar la pestaña, se abrirá el modo Asistente de programación del tablero Programación y se filtrarán los recursos disponibles que cumplen los requisitos de recurso.</span><span class="sxs-lookup"><span data-stu-id="c4531-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="c4531-119">A continuación, podrá reservar un recurso.</span><span class="sxs-lookup"><span data-stu-id="c4531-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="c4531-120">También puede arrastrar y colocar fila seleccionada desde la parte inferior del tablero Programación hasta una celda de recurso en la cuadrícula superior.</span><span class="sxs-lookup"><span data-stu-id="c4531-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="c4531-121">Cuando la coloca, se abre el panel **Crear reserva de recursos** a la derecha.</span><span class="sxs-lookup"><span data-stu-id="c4531-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="c4531-122">Al seleccionar **Reservar** se reserva el recurso para el equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c4531-122">Selecting **Book** books the resource onto the project team.</span></span>

![Panel Crear reserva de recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="c4531-124">Reserva desde el requisito principal</span><span class="sxs-lookup"><span data-stu-id="c4531-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="c4531-125">Al crear un proyecto en Project Service se crea automáticamente un requisito de recurso llamado el requisito principal.</span><span class="sxs-lookup"><span data-stu-id="c4531-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="c4531-126">Se trata de un requisito vacío que se usa para reservar rápidamente un recurso con el tablero Programación sin generar ningún requisito ni crear uno desde cero.</span><span class="sxs-lookup"><span data-stu-id="c4531-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="c4531-127">Puesto que el requisito está vacío, deberá especificar fechas así como el método y las horas de asignación si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c4531-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="c4531-128">Para reservar un recurso con el Requisito principal, en el tablero Programación, seleccione la pestaña **Proyecto**. Quizá deba usar el filtro de columna en la columna **Proyecto** si tiene muchos proyectos.</span><span class="sxs-lookup"><span data-stu-id="c4531-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="c4531-129">![Filtros de columna del tablero de programación](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de pantalla de la tabla de reservas y asignaciones")</span><span class="sxs-lookup"><span data-stu-id="c4531-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="c4531-130">Seleccione el requisito que solo tiene el nombre del proyecto como nombre y tiene una duración de cero (0).</span><span class="sxs-lookup"><span data-stu-id="c4531-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="c4531-131">Seleccione la pestaña **Buscar disponibilidad** que aparece en la fila.</span><span class="sxs-lookup"><span data-stu-id="c4531-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="c4531-132">Esto pone el tablero Programación en el modo Asistente de programación y muestra los recursos disponibles que se pueden reservar para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="c4531-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="c4531-133">Dado que un **requisito principal** es un requisito vacío con duración de cero (0), necesitará establecer la duración en el panel **Crear reserva de recursos** al seleccionar y reservar un recurso.</span><span class="sxs-lookup"><span data-stu-id="c4531-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="c4531-134">También puede seleccionar el **Requisito principal del proyecto** en la parte inferior del tablero Programación y arrastrarlo y colocarlo sobre un recurso para reservarlo.</span><span class="sxs-lookup"><span data-stu-id="c4531-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="c4531-135">Dado que el **Requisito principal** es un requisito vacío con duración de cero (0), necesitará establecer la duración en el panel **Crear reserva de recursos** cuando seleccione y reserve un recurso.</span><span class="sxs-lookup"><span data-stu-id="c4531-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="c4531-136">Cuando se reserva un recurso con el **Requisito principal** en el tablero Programación, se agrega al equipo del proyecto sin ninguna asignación.</span><span class="sxs-lookup"><span data-stu-id="c4531-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="c4531-137">Reservar a partir de un nuevo requisito de recurso</span><span class="sxs-lookup"><span data-stu-id="c4531-137">Book from a new resource requirement</span></span>
<span data-ttu-id="c4531-138">Complete los pasos siguientes para reservar desde un requisito de nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="c4531-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="c4531-139">Vaya a **Requisitos de recursos** y después seleccione **Nuevo** para crear un nuevo requisito de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4531-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="c4531-140">En la pestaña **Proyecto**, seleccione un proyecto para asociar el requisito al proyecto.</span><span class="sxs-lookup"><span data-stu-id="c4531-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="c4531-141">En el tablero Programación, este nuevo requisito se muestra como un **Requisito abierto** que se puede rellenar.</span><span class="sxs-lookup"><span data-stu-id="c4531-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="c4531-142">Reserve el recurso para agregarlo al equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c4531-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="c4531-143">Ahora que el recurso está reservado, debe asignar tareas manualmente.</span><span class="sxs-lookup"><span data-stu-id="c4531-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]