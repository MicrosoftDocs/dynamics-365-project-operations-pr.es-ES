---
title: Novedades o cambios en la versión de actualización 16, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 16, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5d4851ed27028117d25efb0610c25a5aac9c8b70
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006802"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="fd3d0-103">Versión de actualización de Project Service Automation 16, V3</span><span class="sxs-lookup"><span data-stu-id="fd3d0-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fd3d0-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fd3d0-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="fd3d0-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fd3d0-107">Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea, página de soluciones para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="fd3d0-108">Para obtener más información, consulta [Instalar, actualizar una solución preferida](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="fd3d0-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 16.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="fd3d0-110">Esta versión tiene un número de compilación de V3.10.6.34 y está disponible con carácter general a través de una actualización automática en enero de 2020.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="fd3d0-111">Versión de actualización 16</span><span class="sxs-lookup"><span data-stu-id="fd3d0-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fd3d0-112">Solución de errores</span><span class="sxs-lookup"><span data-stu-id="fd3d0-112">Bug fixes</span></span>

-   <span data-ttu-id="fd3d0-113">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="fd3d0-113">Time and Expense</span></span>

    -   <span data-ttu-id="fd3d0-114">Corregido: Los usuarios que intenten enviar entradas de tiempo y gastos eliminados para aprobaciones ahora recibirán los mensajes de error pertinentes.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="fd3d0-115">Administración del proyecto</span><span class="sxs-lookup"><span data-stu-id="fd3d0-115">Project Management</span></span>

    -   <span data-ttu-id="fd3d0-116">Corregido: Las unidades de dotación de recursos definidas para los miembros del equipo en las plantillas se respetan y las plantillas se aplican a un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="fd3d0-117">Corregido: Se ha mejorado el manejo de la reasignación de la propiedad de los registros.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="fd3d0-118">Corregido: No se permitirá copiar los proyectos que se encuentren en proceso de copia hasta que se completen todas las operaciones de copia.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="fd3d0-119">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="fd3d0-119">Resource Management</span></span>

    -   <span data-ttu-id="fd3d0-120">Corrección: Ampliar reservas ahora maneja las duraciones cortas correctamente y ya no crea cero horas para reservas ampliadas.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="fd3d0-121">Corregido: La vista de reconciliación ahora se representa cuando la zona horaria del proyecto es +5:30 GMT y la zona horaria del usuario es diferente.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="fd3d0-122">Sales</span><span class="sxs-lookup"><span data-stu-id="fd3d0-122">Sales</span></span>

    -   <span data-ttu-id="fd3d0-123">Solucionado: Cuando se elimina un proyecto asignado a una línea de contrato y se asigna un proyecto nuevo, los registros reales del nuevo proyecto no se reevalúan en función delas reglas de facturación y precios definidas en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="fd3d0-124">Esto se ha corregido en esta versión.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-124">This has been fixed in this release.</span></span> <span data-ttu-id="fd3d0-125">Los precios y los registros reales del proyecto recién asignado se revertirán y volverán a crear correctamente según las reglas de precios y facturación de la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="fd3d0-126">Los registros reales del proyecto no mapeado también se reevaluarán y se volverán a crear como consecuencia.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="fd3d0-127">Corregido: Se ha agregado validación adicional al campo **Importe** de una línea de estimación campo para garantizar que los valores nulos no sean persistentes.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="fd3d0-128">Corregido: Cuando los datos reales se han actualizado en un proyecto, se ha agregado un botón de actualización al formulario principal del proyecto para permitir a los usuarios vuelvan a sincronizar los datos reales.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="fd3d0-129">Corregido: cuando los usuarios actualizan de 2.X a 3.X, se permitirán proyectos con un valor NULO para el nombre del proyecto.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]