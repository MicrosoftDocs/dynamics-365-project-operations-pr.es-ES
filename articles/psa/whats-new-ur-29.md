---
title: Novedades o cambios en la versión de actualización 29, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 29, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010492"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="46f55-103">Novedades o cambios en la versión de actualización 29, V3, de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="46f55-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="46f55-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="46f55-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="46f55-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="46f55-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="46f55-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="46f55-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="46f55-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="46f55-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="46f55-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="46f55-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="46f55-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 29.</span><span class="sxs-lookup"><span data-stu-id="46f55-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="46f55-110">Esta versión tiene el número de compilación V3.10.47.7 y está disponible de forma generalizada mediante una actualización automática desde febrero de 2021.</span><span class="sxs-lookup"><span data-stu-id="46f55-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="46f55-111">Versión de actualización 29</span><span class="sxs-lookup"><span data-stu-id="46f55-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="46f55-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="46f55-112">Bug fixes</span></span>

<span data-ttu-id="46f55-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="46f55-113">**Time and Expense**</span></span>

<span data-ttu-id="46f55-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="46f55-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="46f55-115">Los usuarios no pueden ver las horas de trabajo registradas en días no laborables en la cuadrícula de entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="46f55-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="46f55-116">Las entradas de gastos aprobadas se pueden editar en la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="46f55-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="46f55-117">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="46f55-117">**Project Management**</span></span>

<span data-ttu-id="46f55-118">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="46f55-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="46f55-119">Falta la lógica de validación para garantizar que las horas de esfuerzo de asignación de recursos no pueden ser negativas.</span><span class="sxs-lookup"><span data-stu-id="46f55-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="46f55-120">La acción personalizada, **AssignResourcesForTask** actualiza todos los campos en lugar de solo los campos modificados.</span><span class="sxs-lookup"><span data-stu-id="46f55-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="46f55-121">Al copiar un proyecto en un entorno con complementos o flujos de trabajo que están registrados en el evento **CreateProject**, el atributo **msdyn_bulkgenerationstatus** no se actualiza si el **CopyWBSToProject** falla.</span><span class="sxs-lookup"><span data-stu-id="46f55-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="46f55-122">Cuando expande el calendario del proyecto, los días laborables no se ordenan en orden ascendente, lo que provoca que fallen algunas actualizaciones de tareas del proyecto.</span><span class="sxs-lookup"><span data-stu-id="46f55-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="46f55-123">Cambiar el Gerente de Proyecto en un proyecto existente desencadena la lógica predeterminada de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="46f55-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="46f55-124">**Ventas**</span><span class="sxs-lookup"><span data-stu-id="46f55-124">**Sales**</span></span>

<span data-ttu-id="46f55-125">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="46f55-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="46f55-126">La pestaña **Ejecución del contrato** en la página **Contrato** falla silenciosamente durante la inicialización cuando no hay líneas de contrato presentes.</span><span class="sxs-lookup"><span data-stu-id="46f55-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>