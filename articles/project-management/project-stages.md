---
title: Fases del proyecto
description: En este tema se proporciona información sobre las fases del proyecto que están disponibles en Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 554ad63bc44cbe5a1fe91eb47fedbb74bbedd4b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085275"
---
# <a name="project-stages"></a><span data-ttu-id="ccba0-103">Fases del proyecto</span><span class="sxs-lookup"><span data-stu-id="ccba0-103">Project stages</span></span>

<span data-ttu-id="ccba0-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="ccba0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ccba0-105">Las fases de un proyecto se diseñan para reflejar el estado del proyecto a medida que avanza.</span><span class="sxs-lookup"><span data-stu-id="ccba0-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="ccba0-106">Las personalizaciones se pueden utilizar para actualizar automáticamente las etapas con los flujos de procesos comerciales, Power Automate o extensiones de complementos.</span><span class="sxs-lookup"><span data-stu-id="ccba0-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="ccba0-107">Se definen las siguientes fases en el flujo de proceso de negocio predeterminado:</span><span class="sxs-lookup"><span data-stu-id="ccba0-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="ccba0-108">Nueva</span><span class="sxs-lookup"><span data-stu-id="ccba0-108">New</span></span>
- <span data-ttu-id="ccba0-109">Oferta</span><span class="sxs-lookup"><span data-stu-id="ccba0-109">Quote</span></span>
- <span data-ttu-id="ccba0-110">Plan</span><span class="sxs-lookup"><span data-stu-id="ccba0-110">Plan</span></span>
- <span data-ttu-id="ccba0-111">Entregar</span><span class="sxs-lookup"><span data-stu-id="ccba0-111">Deliver</span></span>
- <span data-ttu-id="ccba0-112">Completa</span><span class="sxs-lookup"><span data-stu-id="ccba0-112">Complete</span></span>
- <span data-ttu-id="ccba0-113">Cerrada</span><span class="sxs-lookup"><span data-stu-id="ccba0-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="ccba0-114">Nueva</span><span class="sxs-lookup"><span data-stu-id="ccba0-114">New</span></span>

<span data-ttu-id="ccba0-115">Cuando cree un proyecto, la fase del proyecto se establece como **Nueva**.</span><span class="sxs-lookup"><span data-stu-id="ccba0-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="ccba0-116">Si el proyecto se creó a partir de una plantilla, podría tener datos de programación, estimación y equipo.</span><span class="sxs-lookup"><span data-stu-id="ccba0-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="ccba0-117">De lo contrario, es un perfil del proyecto y se deben introducir los componentes restantes.</span><span class="sxs-lookup"><span data-stu-id="ccba0-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="ccba0-118">Oferta</span><span class="sxs-lookup"><span data-stu-id="ccba0-118">Quote</span></span>

<span data-ttu-id="ccba0-119">Cuando asocia un proyecto a una oferta o lo crea desde una oferta, la fase del proyecto se establece en **Oferta** y las fechas de inicio y finalización estimadas se actualizan.</span><span class="sxs-lookup"><span data-stu-id="ccba0-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote** , and the estimated start and end dates are updated.</span></span> <span data-ttu-id="ccba0-120">Cuando el proyecto se encuentra en la fase **Oferta** , la pestaña **Ventas** en la página **Entidad del proyecto** muestra detalles de la oferta.</span><span class="sxs-lookup"><span data-stu-id="ccba0-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="ccba0-121">Planear</span><span class="sxs-lookup"><span data-stu-id="ccba0-121">Plan</span></span>

<span data-ttu-id="ccba0-122">Cuando gana una oferta asociada a un proyecto, y el proyecto se mueve a la fase **Contrato** , la fase del proyecto se actualiza a **Planificar**.</span><span class="sxs-lookup"><span data-stu-id="ccba0-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="ccba0-123">Cuando el proyecto se encuentra en la fase **Planificar** , la página **Entidad del proyecto** muestra detalles del contrato.</span><span class="sxs-lookup"><span data-stu-id="ccba0-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="ccba0-124">Entregar</span><span class="sxs-lookup"><span data-stu-id="ccba0-124">Deliver</span></span>

<span data-ttu-id="ccba0-125">Cuando se completa el plan del proyecto y está listo para comenzar el proyecto, el jefe de proyecto debe actualizar la fase del proyecto a **Entregar** para mostrar que el proyecto ha comenzado.</span><span class="sxs-lookup"><span data-stu-id="ccba0-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="ccba0-126">Completo</span><span class="sxs-lookup"><span data-stu-id="ccba0-126">Complete</span></span> 

<span data-ttu-id="ccba0-127">Cuando se completa el trabajo para el proyecto, el administrador del proyecto puede actualizar la fase a **Completo**.</span><span class="sxs-lookup"><span data-stu-id="ccba0-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="ccba0-128">Al actualizar la fase del proyecto a **Completo** , el administrador del proyecto indica que el trabajo se ha completado al cien por cien, pero que el proyecto se mantiene abierto para que se puedan registrar las entradas de tiempo o gastos pendientes.</span><span class="sxs-lookup"><span data-stu-id="ccba0-128">By updating the project stage to **Complete** , the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="ccba0-129">Cerrar</span><span class="sxs-lookup"><span data-stu-id="ccba0-129">Close</span></span>

<span data-ttu-id="ccba0-130">Cuando se registran todas las transacciones para el proyecto, el administrador del proyecto puede actualizar la fase a **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="ccba0-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="ccba0-131">A partir de ese momento, no se podrán registrar transacciones y el proyecto quedará configurado como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ccba0-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

