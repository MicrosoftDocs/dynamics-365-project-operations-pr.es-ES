---
title: Administrar zonas horarias
description: Cuando se crea un proyecto, su zona horaria se basa en la zona horaria definida en la plantilla de horas de trabajo aplicada.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961954"
---
# <a name="manage-time-zones"></a><span data-ttu-id="6fbce-103">Administrar zonas horarias</span><span class="sxs-lookup"><span data-stu-id="6fbce-103">Manage time zones</span></span>

<span data-ttu-id="6fbce-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="6fbce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="6fbce-105">Proyectos</span><span class="sxs-lookup"><span data-stu-id="6fbce-105">Projects</span></span>

<span data-ttu-id="6fbce-106">Cuando se crea un proyecto, su zona horaria se basa en la zona horaria definida en la plantilla de horas de trabajo aplicada.</span><span class="sxs-lookup"><span data-stu-id="6fbce-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="6fbce-107">En el **Proyecto**, las fechas son siempre relativas a la zona horaria del usuario que está conectado en cada pestaña, excepto la pestaña **Tarea**. Cuando vea la estructura de descomposición del trabajo, las fechas siempre se mostrarán en la zona horaria del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6fbce-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="6fbce-108">Tareas</span><span class="sxs-lookup"><span data-stu-id="6fbce-108">Tasks</span></span>

<span data-ttu-id="6fbce-109">Cuando se crea una tarea, la hora de inicio, la hora de finalización y las horas/día se controlan mediante las horas de trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6fbce-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="6fbce-110">Por ejemplo, si se crea una tarea con un proyecto cuya zona horaria es -8 PST y tiene las siguientes horas de trabajo: de 9:00 a. m. a 5:00 p. m, de lunes a viernes, cualquier tarea creada sin una asignación respetará la hora de inicio y hora de finalización del calendario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6fbce-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="6fbce-111">Administrar recursos con zonas horarias</span><span class="sxs-lookup"><span data-stu-id="6fbce-111">Manage resources with time zones</span></span>

<span data-ttu-id="6fbce-112">Para obtener resultados precisos y predecibles al usar **Ampliar reserva**, hay dos requisitos previos clave que deben cumplirse:</span><span class="sxs-lookup"><span data-stu-id="6fbce-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="6fbce-113">El usuario debe configurar la zona horaria de su dispositivo para que coincida con la zona horaria definida en la **Configuración de personalización** del sistema.</span><span class="sxs-lookup"><span data-stu-id="6fbce-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Configuración de zona horaria en Windows 10](media/reconcile-assignments-03.png)

  ![Configuración de la zona horaria en la configuración de personalización](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="6fbce-116">El recurso reservable debe tener al menos un minuto de tiempo de trabajo que se superponga con los contornos que se utilizan para definir la extensión solicitada.</span><span class="sxs-lookup"><span data-stu-id="6fbce-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="6fbce-117">Por ejemplo, los siguientes recursos con horas de trabajo comprendidas entre las 9:00 a. m. y las 7:00 p. m.</span><span class="sxs-lookup"><span data-stu-id="6fbce-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Comparación de contornos de recursos](media/reconcile-assignments-05.png)

<span data-ttu-id="6fbce-119">En la tabla siguiente se muestra:</span><span class="sxs-lookup"><span data-stu-id="6fbce-119">The following table shows:</span></span>

- <span data-ttu-id="6fbce-120">Plantilla de calendario de proyecto</span><span class="sxs-lookup"><span data-stu-id="6fbce-120">A project calendar template</span></span>
- <span data-ttu-id="6fbce-121">Recurso A: Este recurso tiene el mismo calendario y se encuentra en la misma zona horaria que el proyecto.</span><span class="sxs-lookup"><span data-stu-id="6fbce-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="6fbce-122">La hora de inicio de las reservas será las 9 de la mañana.</span><span class="sxs-lookup"><span data-stu-id="6fbce-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="6fbce-123">Recurso B: este recurso se encuentra en una zona horaria diferente a la del proyecto y comienza a las 7:00 a.m. en su zona horaria.</span><span class="sxs-lookup"><span data-stu-id="6fbce-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="6fbce-124">Sin embargo, las reservas comenzarán a las 9 de la mañana, ya que es la primera hora de inicio del contorno de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6fbce-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="6fbce-125">Recursos C y D: los recursos están ubicados en diferentes zonas horarias, ambas diferentes entre sí y del proyecto, y sus reservas no comienzan antes de sus respectivas horas de inicio disponibles.</span><span class="sxs-lookup"><span data-stu-id="6fbce-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="6fbce-126">Entidad</span><span class="sxs-lookup"><span data-stu-id="6fbce-126">Entity</span></span>  |<span data-ttu-id="6fbce-127">Calendario</span><span class="sxs-lookup"><span data-stu-id="6fbce-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="6fbce-128">Plantilla de calendario de proyecto</span><span class="sxs-lookup"><span data-stu-id="6fbce-128">Project calendar template</span></span>   | ![calendario de proyecto](media/reconcile-assignments-06.png) |
|<span data-ttu-id="6fbce-130">Recurso A</span><span class="sxs-lookup"><span data-stu-id="6fbce-130">Resource A</span></span>  | ![Calendario de recurso A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="6fbce-132">Recurso B</span><span class="sxs-lookup"><span data-stu-id="6fbce-132">Resource B</span></span>  |  ![Calendario de recurso B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="6fbce-134">Recurso C</span><span class="sxs-lookup"><span data-stu-id="6fbce-134">Resource C</span></span>  |  ![Calendario de recurso C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="6fbce-136">Recurso D</span><span class="sxs-lookup"><span data-stu-id="6fbce-136">Resource D</span></span>  | ![Calendario de recurso D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="6fbce-138">Cuando navega a la vista **Conciliación**, se muestran las asignaciones de recursos y la escasez de reservas asociada.</span><span class="sxs-lookup"><span data-stu-id="6fbce-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Vista de conciliación antes de la extensión](media/reconcile-assignments-10.png)

<span data-ttu-id="6fbce-140">Una vez que se ha utilizado la funcionalidad de extensión de reserva para cada recurso, las reservas se extienden con éxito para cada recurso porque las horas de trabajo de cada recurso se superponen con los contornos de la escasez.</span><span class="sxs-lookup"><span data-stu-id="6fbce-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Vista de conciliación después de la ampliación de reserva](media/reconcile-assignments-11.png) 

<span data-ttu-id="6fbce-142">Observe que una mirada más detallada a los detalles de las reservas muestra diferencias en la hora de inicio de las reservas.</span><span class="sxs-lookup"><span data-stu-id="6fbce-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="6fbce-143">Las reservas no comienzan antes de la hora de inicio del contorno de asignación ni antes de la hora de inicio disponible del recurso.</span><span class="sxs-lookup"><span data-stu-id="6fbce-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nuevas reservas de los recursos en el tablero de programación](media/reconcile-assignments-12.png)
