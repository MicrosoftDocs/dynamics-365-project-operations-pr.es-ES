---
title: Novedades o cambios en la versión de actualización 33, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 33, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334605"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="69936-103">Novedades o cambios en la versión de actualización 33, V3, de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="69936-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="69936-104">Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="69936-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="69936-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="69936-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="69936-106">Es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="69936-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="69936-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización.</span><span class="sxs-lookup"><span data-stu-id="69936-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="69936-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="69936-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="69936-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 33.</span><span class="sxs-lookup"><span data-stu-id="69936-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="69936-110">Esta versión tiene un número de compilación de V3.10.54.98 y generalmente está disponible a través de una actualización automática en julio de 2021.</span><span class="sxs-lookup"><span data-stu-id="69936-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="69936-111">Versión de actualización 33</span><span class="sxs-lookup"><span data-stu-id="69936-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="69936-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="69936-112">Bug fixes</span></span>

<span data-ttu-id="69936-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="69936-113">**Time and Expense**</span></span>

<span data-ttu-id="69936-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="69936-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="69936-115">Dos campos cerrados, **msdyn_description** y **msdyn_externaldescription**, son editables después del envío.</span><span class="sxs-lookup"><span data-stu-id="69936-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="69936-116">Aparece un mensaje de error si se crea un gasto que no está relacionado con un proyecto.</span><span class="sxs-lookup"><span data-stu-id="69936-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="69936-117">Cuando se crea una entrada de tiempo, el rol de recurso se establece de forma predeterminada a un rol inactivo.</span><span class="sxs-lookup"><span data-stu-id="69936-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="69936-118">Las líneas del diario asociadas con un gasto retirado y eliminado no se eliminan.</span><span class="sxs-lookup"><span data-stu-id="69936-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="69936-119">En el **Formulario de creación rápida de entrada de tiempo**, actualice la vista **Lista de tareas del proyecto** para cambiar la fecha que se muestra de forma predeterminada a la fecha de inicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="69936-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="69936-120">Cuando crea una entrada de tiempo desde la pestaña **Relacionados** del recurso que se puede reservar, la entrada de tiempo se crea incorrectamente para el usuario que inició sesión en lugar del recurso que se puede reservar principal.</span><span class="sxs-lookup"><span data-stu-id="69936-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="69936-121">Se agregan nuevos campos al cuadro de diálogo **MDD de aprobación en masa**.</span><span class="sxs-lookup"><span data-stu-id="69936-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="69936-122">**Planificación del proyecto**</span><span class="sxs-lookup"><span data-stu-id="69936-122">**Project planning**</span></span>

<span data-ttu-id="69936-123">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="69936-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="69936-124">Rendimiento lento en la creación de proyectos cuando se aplican plantillas de horas de trabajo del proyecto con calendarios complejos.</span><span class="sxs-lookup"><span data-stu-id="69936-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="69936-125">Cuando la fecha de inicio es mayor que la fecha final, se muestra un error en la plantilla del proyecto de texto debido a diferencias en el componente de tiempo de cada campo.</span><span class="sxs-lookup"><span data-stu-id="69936-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="69936-126">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="69936-126">**Resource management**</span></span>

<span data-ttu-id="69936-127">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="69936-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="69936-128">Se utiliza un parámetro incorrecto en la consulta de uso de recursos y el XML lleva a resultados de filtro incorrectos en la cuadrícula **Utilización de recursos**.</span><span class="sxs-lookup"><span data-stu-id="69936-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="69936-129">La confirmación **Ampliar reservas** muestra una fecha final incorrecta para las reservas.</span><span class="sxs-lookup"><span data-stu-id="69936-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="69936-130">**Ventas**</span><span class="sxs-lookup"><span data-stu-id="69936-130">**Sales**</span></span>

<span data-ttu-id="69936-131">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="69936-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="69936-132">Se produce un mensaje de error si se crea un precio de categoría al que le falten valores.</span><span class="sxs-lookup"><span data-stu-id="69936-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="69936-133">Se produce un mensaje de error si se crea un hito de línea de contrato sin una línea de pedido.</span><span class="sxs-lookup"><span data-stu-id="69936-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
