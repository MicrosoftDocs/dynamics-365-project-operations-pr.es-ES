---
title: Novedades o cambios en la versión de actualización 32, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 32, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129687"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="cc1de-103">Novedades o cambios en la versión de actualización 32, V3, de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc1de-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cc1de-104">Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cc1de-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="cc1de-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="cc1de-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc1de-106">Es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cc1de-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc1de-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización.</span><span class="sxs-lookup"><span data-stu-id="cc1de-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="cc1de-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc1de-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc1de-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 32.</span><span class="sxs-lookup"><span data-stu-id="cc1de-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="cc1de-110">Esta versión tiene un número de compilación de V3.10.53.108 y estará disponible de manera general a través de una actualización automática en junio de 2021.</span><span class="sxs-lookup"><span data-stu-id="cc1de-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="cc1de-111">Versión de actualización 32</span><span class="sxs-lookup"><span data-stu-id="cc1de-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc1de-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="cc1de-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="cc1de-113">General</span><span class="sxs-lookup"><span data-stu-id="cc1de-113">General</span></span>

- <span data-ttu-id="cc1de-114">Cuando falla una actualización importante, solo se deben bloquear los puntos de entrada de la aplicación principal para garantizar que las entidades compartidas sigan siendo accesibles.</span><span class="sxs-lookup"><span data-stu-id="cc1de-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="cc1de-115">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="cc1de-115">Time and Expense</span></span>

<span data-ttu-id="cc1de-116">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="cc1de-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc1de-117">**TimeEntriesImportFromResourceAssignment** no mantiene las horas de inicio y finalización del segmento de perfil de asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc1de-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="cc1de-118">Si selecciona **Entrada abierta** en la cuadrícula **Entrada de tiempo**, es posible que no pueda seleccionar otros formularios.</span><span class="sxs-lookup"><span data-stu-id="cc1de-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="cc1de-119">Mientras importa asignaciones en entradas de tiempo, la consulta del código del cliente podría generar una URL larga que falle en la consulta.</span><span class="sxs-lookup"><span data-stu-id="cc1de-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="cc1de-120">En la cuadrícula **Entrada de tiempo**, después de eliminar un valor de una celda, el foco no permanece en la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="cc1de-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="cc1de-121">El botón **Rechazar** ha sido eliminado de la vista **Aprobaciones de procesamiento** de las aprobaciones modernas.</span><span class="sxs-lookup"><span data-stu-id="cc1de-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="cc1de-122">La estabilidad y el rendimiento de la aprobación masiva de entrada de tiempo se ven afectados por interbloqueos y por un fallo en el manejo adecuado de las personalizaciones relacionadas con la entidad **Entrada de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="cc1de-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="cc1de-123">Planificación de proyectos</span><span class="sxs-lookup"><span data-stu-id="cc1de-123">Project Planning</span></span>

- <span data-ttu-id="cc1de-124">Se genera una excepción de referencia nula cuando actualiza un proyecto que tiene un valor nulo en el campo **Unidad de contratación**.</span><span class="sxs-lookup"><span data-stu-id="cc1de-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="cc1de-125">**Actualizar totales del proyecto** calcula incorrectamente el coste restante y las ventas restantes en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="cc1de-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="cc1de-126">Los cálculos de precios redundantes afectan al rendimiento relacionado con las actualizaciones en los contornos de asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc1de-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="cc1de-127">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="cc1de-127">Resource Management</span></span>

<span data-ttu-id="cc1de-128">Se ha resuelto el siguiente problema:</span><span class="sxs-lookup"><span data-stu-id="cc1de-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="cc1de-129">Cuando la capacidad de calendario de un recurso que se puede reservar es superior a 1, Project Service Automation reconoce incorrectamente la capacidad como 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="cc1de-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="cc1de-130">Por lo tanto, se produce un bucle infinito en la vista de programación.</span><span class="sxs-lookup"><span data-stu-id="cc1de-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="cc1de-131">Ventas</span><span class="sxs-lookup"><span data-stu-id="cc1de-131">Sales</span></span>

<span data-ttu-id="cc1de-132">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="cc1de-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc1de-133">Cuando se crea una línea de diario que tiene un tipo de transacción personalizado, se produce la siguiente excepción de referencia nula: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="cc1de-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="cc1de-134">Los roles y categorías que se desactivan antes de copiar un presupuesto no deben agregarse a los roles y categorías imputables del presupuesto recién copiado.</span><span class="sxs-lookup"><span data-stu-id="cc1de-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="cc1de-135">La fecha del documento y la fecha contable no están alineadas con la fecha de inicio que se proporciona en un detalle de línea de factura que se crea directamente en un borrador de factura.</span><span class="sxs-lookup"><span data-stu-id="cc1de-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="cc1de-136">Las excepciones de referencias nulas se generan en escenarios relacionados con la inactivación de roles y categorías antes de que se copie un presupuesto.</span><span class="sxs-lookup"><span data-stu-id="cc1de-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="cc1de-137">La acción **Actualizar precios** de la página **Proyectos** no actualiza las estimaciones de gastos ni las estimaciones de materiales.</span><span class="sxs-lookup"><span data-stu-id="cc1de-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
