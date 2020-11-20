---
title: Fases del proyecto
description: En este tema se proporciona información sobre las fases del proyecto que están disponibles en Microsoft Dynamics Project Operations.
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127494"
---
# <a name="project-stages"></a><span data-ttu-id="e44a9-103">Fases del proyecto</span><span class="sxs-lookup"><span data-stu-id="e44a9-103">Project stages</span></span>

<span data-ttu-id="e44a9-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="e44a9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e44a9-105">Las fases de un proyecto se diseñan para reflejar el estado del proyecto a medida que avanza.</span><span class="sxs-lookup"><span data-stu-id="e44a9-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="e44a9-106">Las personalizaciones se pueden utilizar para actualizar automáticamente las etapas con los flujos de procesos comerciales, Power Automate o extensiones de complementos.</span><span class="sxs-lookup"><span data-stu-id="e44a9-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="e44a9-107">Se definen las siguientes fases en el flujo de proceso de negocio predeterminado:</span><span class="sxs-lookup"><span data-stu-id="e44a9-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="e44a9-108">Nueva</span><span class="sxs-lookup"><span data-stu-id="e44a9-108">New</span></span>
- <span data-ttu-id="e44a9-109">Oferta</span><span class="sxs-lookup"><span data-stu-id="e44a9-109">Quote</span></span>
- <span data-ttu-id="e44a9-110">Plan</span><span class="sxs-lookup"><span data-stu-id="e44a9-110">Plan</span></span>
- <span data-ttu-id="e44a9-111">Entregar</span><span class="sxs-lookup"><span data-stu-id="e44a9-111">Deliver</span></span>
- <span data-ttu-id="e44a9-112">Completa</span><span class="sxs-lookup"><span data-stu-id="e44a9-112">Complete</span></span>
- <span data-ttu-id="e44a9-113">Cerrada</span><span class="sxs-lookup"><span data-stu-id="e44a9-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="e44a9-114">Nueva</span><span class="sxs-lookup"><span data-stu-id="e44a9-114">New</span></span>

<span data-ttu-id="e44a9-115">Cuando cree un proyecto, la fase del proyecto se establece como **Nueva**.</span><span class="sxs-lookup"><span data-stu-id="e44a9-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="e44a9-116">Si el proyecto se creó a partir de una plantilla, podría tener datos de programación, estimación y equipo.</span><span class="sxs-lookup"><span data-stu-id="e44a9-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="e44a9-117">De lo contrario, es un perfil del proyecto y se deben introducir los componentes restantes.</span><span class="sxs-lookup"><span data-stu-id="e44a9-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="e44a9-118">Oferta</span><span class="sxs-lookup"><span data-stu-id="e44a9-118">Quote</span></span>

<span data-ttu-id="e44a9-119">Cuando asocia un proyecto a una oferta o lo crea desde una oferta, la fase del proyecto se establece en **Oferta** y las fechas de inicio y finalización estimadas se actualizan.</span><span class="sxs-lookup"><span data-stu-id="e44a9-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="e44a9-120">Cuando el proyecto se encuentra en la fase **Oferta**, la pestaña **Ventas** en la página **Entidad del proyecto** muestra detalles de la oferta.</span><span class="sxs-lookup"><span data-stu-id="e44a9-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="e44a9-121">Planear</span><span class="sxs-lookup"><span data-stu-id="e44a9-121">Plan</span></span>

<span data-ttu-id="e44a9-122">Cuando gana una oferta asociada a un proyecto, y el proyecto se mueve a la fase **Contrato**, la fase del proyecto se actualiza a **Planificar**.</span><span class="sxs-lookup"><span data-stu-id="e44a9-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="e44a9-123">Cuando el proyecto se encuentra en la fase **Planificar**, la página **Entidad del proyecto** muestra detalles del contrato.</span><span class="sxs-lookup"><span data-stu-id="e44a9-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="e44a9-124">Entregar</span><span class="sxs-lookup"><span data-stu-id="e44a9-124">Deliver</span></span>

<span data-ttu-id="e44a9-125">Cuando se completa el plan del proyecto y está listo para comenzar el proyecto, el jefe de proyecto debe actualizar la fase del proyecto a **Entregar** para mostrar que el proyecto ha comenzado.</span><span class="sxs-lookup"><span data-stu-id="e44a9-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="e44a9-126">Completo</span><span class="sxs-lookup"><span data-stu-id="e44a9-126">Complete</span></span> 

<span data-ttu-id="e44a9-127">Cuando se completa el trabajo para el proyecto, el administrador del proyecto puede actualizar la fase a **Completo**.</span><span class="sxs-lookup"><span data-stu-id="e44a9-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="e44a9-128">Al actualizar la fase del proyecto a **Completo**, el administrador del proyecto indica que el trabajo se ha completado al cien por cien, pero que el proyecto se mantiene abierto para que se puedan registrar las entradas de tiempo o gastos pendientes.</span><span class="sxs-lookup"><span data-stu-id="e44a9-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="e44a9-129">Cerrar</span><span class="sxs-lookup"><span data-stu-id="e44a9-129">Close</span></span>

<span data-ttu-id="e44a9-130">Cuando se registran todas las transacciones para el proyecto, el administrador del proyecto puede actualizar la fase a **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e44a9-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="e44a9-131">A partir de ese momento, no se podrán registrar transacciones y el proyecto quedará configurado como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e44a9-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

