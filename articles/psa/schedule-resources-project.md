---
title: Programar recursos para un proyecto
description: Cómo programar recursos para un proyecto en Project Service
author: JohnPBurrows
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
ms.openlocfilehash: f0a234f96419bac58cd932a082010da672e7dcb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282669"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="c8e93-103">Programar recursos para un proyecto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c8e93-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c8e93-104">Puede comprobar la disponibilidad de recursos para obtener una visión general de lo reservados que están sus recursos o bien puede filtrar la vista por conocimientos, equipo, ubicación y otras opciones.</span><span class="sxs-lookup"><span data-stu-id="c8e93-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="c8e93-105">El tablero de programación muestra una lista de recursos y su disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="c8e93-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="c8e93-106">Seleccione un modo de vista para mostrar disponibilidad por **Horas**, **Día**, **Semana** o **Mes**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="c8e93-107">Antes de usar al tablero de programación, es importante configurarlo.</span><span class="sxs-lookup"><span data-stu-id="c8e93-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="c8e93-108">Para obtener más información, consulte [Configurar la tabla de programación (Field Service o Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="c8e93-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="c8e93-109">Si usa una versión anterior, para disponibilidad de recursos, consulte [Ver disponibilidad de recursos](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="c8e93-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="c8e93-110">Para usar la funcionalidad de reserva del tablero de programación, geocodificación y servicios de ubicación, debe activar los mapas.</span><span class="sxs-lookup"><span data-stu-id="c8e93-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="c8e93-111">En el menú principal, seleccione **Programación de recursos** > **Administración**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="c8e93-112">Haga clic en **Parámetros de programación**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="c8e93-113">Abra el registro y desplácese hacia abajo hasta la sección **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="c8e93-114">En el campo **Conectar con Mapas**, elija **Sí**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="c8e93-115">Acepte la términos y guarde el registro.</span><span class="sxs-lookup"><span data-stu-id="c8e93-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="c8e93-116">En el menú principal, seleccione **Project Service** > **Tabla de programación**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="c8e93-117">A partir de aquí, hay varias formas diferentes de programar manualmente un requisito de reserva.</span><span class="sxs-lookup"><span data-stu-id="c8e93-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="c8e93-118">Elija el método que funcione para usted.</span><span class="sxs-lookup"><span data-stu-id="c8e93-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="c8e93-119">Buscar recursos disponibles</span><span class="sxs-lookup"><span data-stu-id="c8e93-119">Find available resources</span></span>

1.  <span data-ttu-id="c8e93-120">De la lista **Requisitos de reserva**, haga clic con el botón secundario en una reserva no programada y seleccione una de las acciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="c8e93-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="c8e93-121">Elija **Buscar disponibilidad - Recurso actual** para buscar un recurso disponible en la lista de recursos del tablero de programación.</span><span class="sxs-lookup"><span data-stu-id="c8e93-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="c8e93-122">Elija **Buscar disponibilidad - Todos los recursos** para buscar un recurso disponible en los recursos del sistema</span><span class="sxs-lookup"><span data-stu-id="c8e93-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="c8e93-123">Al hacerlo, los filtros mostrarán las opciones del requisito de reserva seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c8e93-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="c8e93-124">Cuando vea un intervalo disponible, haga clic con el botón secundario en el intervalo de tiempo en el tablero de programación y elija **Reservar aquí**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="c8e93-125">O bien, arrastre y coloque el requisito de reserva al intervalo de tiempo disponible.</span><span class="sxs-lookup"><span data-stu-id="c8e93-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="c8e93-126">Reserve un recurso mediante la vista diaria y busque quién tiene pocas reservas</span><span class="sxs-lookup"><span data-stu-id="c8e93-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="c8e93-127">En el tablero de programación, seleccione **Modo de vista** y **Días**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="c8e93-128">Esto muestra una vista de cuadrícula del número de horas que está reservado un recurso por día y qué días está libre.</span><span class="sxs-lookup"><span data-stu-id="c8e93-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="c8e93-129">Haga clic en el nombre del recurso que desea para reservar y seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="c8e93-130">En el cuadro de diálogo **Reserva de recursos (crear)**, elija el proyecto para el que desea reservar el recurso junto con el método de reserva y las horas de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="c8e93-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="c8e93-131">Cuando esté listo, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="c8e93-132">Ver el tablero de programación</span><span class="sxs-lookup"><span data-stu-id="c8e93-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="c8e93-133">Seleccione un requisito de reserva no programado desde la lista de la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="c8e93-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="c8e93-134">Arrastre el requisito de reserva a un intervalo de tiempo/recurso disponible en el tablero de programación.</span><span class="sxs-lookup"><span data-stu-id="c8e93-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="c8e93-135">Cuando haya terminado, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="c8e93-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="c8e93-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c8e93-136">Additional resources</span></span>  
 [<span data-ttu-id="c8e93-137">Guía del administrador de recursos</span><span class="sxs-lookup"><span data-stu-id="c8e93-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]