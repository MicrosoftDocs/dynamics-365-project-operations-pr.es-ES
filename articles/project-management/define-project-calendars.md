---
title: Definir calendarios de proyectos
description: En este tema se proporciona información sobre el uso de un calendario de proyecto para realizar un seguimiento de la programación del proyecto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131679"
---
# <a name="define-project-calendars"></a><span data-ttu-id="219e6-103">Definir calendarios de proyectos</span><span class="sxs-lookup"><span data-stu-id="219e6-103">Define project calendars</span></span>

<span data-ttu-id="219e6-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="219e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="219e6-105">Para crear una programación de proyecto, cree una plantilla de calendario de proyecto que defina la cantidad de horas de trabajo por día y los cierres de negocios.</span><span class="sxs-lookup"><span data-stu-id="219e6-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="219e6-106">Para crear una plantilla de calendario de proyecto, asocie una plantilla de trabajo con el campo **Plantilla de calendario** para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="219e6-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="219e6-107">Siga estos pasos para crear una plantilla de trabajo.</span><span class="sxs-lookup"><span data-stu-id="219e6-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="219e6-108">En el panel de navegación izquierdo, seleccione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="219e6-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="219e6-109">En la página de la lista **Recursos**, abra un registro de usuario y, a continuación, seleccione **Mostrar horas laborables**.</span><span class="sxs-lookup"><span data-stu-id="219e6-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="219e6-110">Asegúrese de permitir ventanas emergentes en la página del explorador.</span><span class="sxs-lookup"><span data-stu-id="219e6-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="219e6-111">Esto le permitirá ver las horas de trabajo establecidas para el recurso.</span><span class="sxs-lookup"><span data-stu-id="219e6-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="219e6-112">En la pestaña **Vista mensual** , seleccione **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="219e6-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="219e6-113">Aparecerá una lista con tres opciones:</span><span class="sxs-lookup"><span data-stu-id="219e6-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="219e6-114">Nueva programación semanal</span><span class="sxs-lookup"><span data-stu-id="219e6-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="219e6-115">Programación de trabajo para un día</span><span class="sxs-lookup"><span data-stu-id="219e6-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="219e6-116">Indisponibilidad</span><span class="sxs-lookup"><span data-stu-id="219e6-116">Time Off</span></span>

4. <span data-ttu-id="219e6-117">Seleccione **Nueva programación semanal** y, a continuación, establezca las opciones para esta programación del recurso.</span><span class="sxs-lookup"><span data-stu-id="219e6-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="219e6-118">Puede establecer una programación semanal recurrente, parámetros de horas diarias, cierres comerciales, etc.</span><span class="sxs-lookup"><span data-stu-id="219e6-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="219e6-119">Establezca el rango de fechas, seleccione **Guardar** y, a continuación, seleccione **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="219e6-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="219e6-120">Vuelva a la página de lista **Recursos** y seleccione el recurso para el que estableció las horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="219e6-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="219e6-121">Seleccione **Establecer calendario como** para establecer la plantilla de trabajo.</span><span class="sxs-lookup"><span data-stu-id="219e6-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="219e6-122">En el cuadro de diálogo **Plantilla de trabajo**, introduzca un nombre para la plantilla de trabajo y, a continuación, seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="219e6-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="219e6-123">Ahora puede asociar la plantilla de trabajo con una plantilla de calendario de proyecto.</span><span class="sxs-lookup"><span data-stu-id="219e6-123">You can now associate the work template with a project calendar template.</span></span>
