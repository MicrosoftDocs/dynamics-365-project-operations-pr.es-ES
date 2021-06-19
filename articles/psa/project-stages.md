---
title: Tipos de fases del proyecto
description: En este tema se proporciona información sobre las fases del proyecto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ed725d8ea2f671c45a7a19bb017bbb08c41f42db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009007"
---
# <a name="project-stage-types"></a><span data-ttu-id="688c1-103">Tipos de fases del proyecto</span><span class="sxs-lookup"><span data-stu-id="688c1-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="688c1-104">Las fases de un proyecto se diseñan para reflejar el estado del proyecto a medida que avanza.</span><span class="sxs-lookup"><span data-stu-id="688c1-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="688c1-105">Las personalizaciones se pueden utilizar para actualizar automáticamente las etapas con los flujos de procesos comerciales, Power Automate o extensiones de complementos.</span><span class="sxs-lookup"><span data-stu-id="688c1-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="688c1-106">Se definen las siguientes fases en el BPF predeterminado:</span><span class="sxs-lookup"><span data-stu-id="688c1-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="688c1-107">Nueva</span><span class="sxs-lookup"><span data-stu-id="688c1-107">New</span></span>
- <span data-ttu-id="688c1-108">Oferta</span><span class="sxs-lookup"><span data-stu-id="688c1-108">Quote</span></span>
- <span data-ttu-id="688c1-109">Planear</span><span class="sxs-lookup"><span data-stu-id="688c1-109">Plan</span></span>
- <span data-ttu-id="688c1-110">Entregar</span><span class="sxs-lookup"><span data-stu-id="688c1-110">Deliver</span></span>
- <span data-ttu-id="688c1-111">Completo</span><span class="sxs-lookup"><span data-stu-id="688c1-111">Complete</span></span>
- <span data-ttu-id="688c1-112">Cerrar</span><span class="sxs-lookup"><span data-stu-id="688c1-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="688c1-113">Nuevo</span><span class="sxs-lookup"><span data-stu-id="688c1-113">New</span></span>

<span data-ttu-id="688c1-114">Cuando cree un proyecto, la fase del proyecto se establece como **Nueva**.</span><span class="sxs-lookup"><span data-stu-id="688c1-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="688c1-115">Si el proyecto se creó a partir de una plantilla, podría tener datos de programación, estimación y equipo.</span><span class="sxs-lookup"><span data-stu-id="688c1-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="688c1-116">De lo contrario, es solo un perfil del proyecto y se deben introducir los componentes restantes.</span><span class="sxs-lookup"><span data-stu-id="688c1-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="688c1-117">Oferta</span><span class="sxs-lookup"><span data-stu-id="688c1-117">Quote</span></span>

<span data-ttu-id="688c1-118">Cuando asocia un proyecto a una oferta o lo crea desde una oferta, la fase del proyecto se establece en **Oferta** y las fechas de inicio y finalización estimadas se actualizan.</span><span class="sxs-lookup"><span data-stu-id="688c1-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="688c1-119">Cuando el proyecto se encuentra en la fase **Oferta**, la pestaña **Ventas** en la página **Entidad del proyecto** muestra detalles de la oferta.</span><span class="sxs-lookup"><span data-stu-id="688c1-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="688c1-120">Planear</span><span class="sxs-lookup"><span data-stu-id="688c1-120">Plan</span></span>

<span data-ttu-id="688c1-121">Cuando gana una oferta asociada a un proyecto, y el proyecto se mueve a la fase **Contrato**, la fase del proyecto se actualiza a **Planificar**.</span><span class="sxs-lookup"><span data-stu-id="688c1-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="688c1-122">Cuando el proyecto se encuentra en la fase **Planificar**, la página **Entidad del proyecto** muestra detalles del contrato.</span><span class="sxs-lookup"><span data-stu-id="688c1-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="688c1-123">Entregar</span><span class="sxs-lookup"><span data-stu-id="688c1-123">Deliver</span></span>

<span data-ttu-id="688c1-124">Cuando se completa el plan del proyecto y está listo para comenzar el proyecto, el jefe de proyecto debe actualizar la fase del proyecto a **Entregar** para mostrar que el proyecto ha comenzado.</span><span class="sxs-lookup"><span data-stu-id="688c1-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="688c1-125">Completo</span><span class="sxs-lookup"><span data-stu-id="688c1-125">Complete</span></span> 

<span data-ttu-id="688c1-126">Cuando se completa el trabajo para el proyecto, el administrador del proyecto puede actualizar la fase a **Completo**.</span><span class="sxs-lookup"><span data-stu-id="688c1-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="688c1-127">Al actualizar la fase del proyecto a **Completo**, el administrador del proyecto indica que el trabajo se ha completado al cien por cien, pero que el proyecto se mantiene abierto para que se puedan registrar las entradas de tiempo o gastos pendientes.</span><span class="sxs-lookup"><span data-stu-id="688c1-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="688c1-128">Cerrar</span><span class="sxs-lookup"><span data-stu-id="688c1-128">Close</span></span>

<span data-ttu-id="688c1-129">Cuando se registran todas las transacciones para el proyecto, el administrador del proyecto puede actualizar la fase a **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="688c1-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="688c1-130">A partir de ese momento, no se podrán registrar transacciones y el proyecto quedará configurado como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="688c1-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]