---
title: Novedades o cambios en la versión de actualización 23, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 23, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150059"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="a8b13-103">Versión de actualización de Project Service Automation 23, V3</span><span class="sxs-lookup"><span data-stu-id="a8b13-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a8b13-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a8b13-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a8b13-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="a8b13-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a8b13-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a8b13-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a8b13-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="a8b13-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a8b13-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a8b13-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a8b13-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 23.</span><span class="sxs-lookup"><span data-stu-id="a8b13-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="a8b13-110">Esta versión tiene un número de compilación de V 3.10.34.30 y está disponible con carácter general a través de una actualización automática en agosto de 2020.</span><span class="sxs-lookup"><span data-stu-id="a8b13-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="a8b13-111">Versión de actualización 23</span><span class="sxs-lookup"><span data-stu-id="a8b13-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a8b13-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="a8b13-112">Bug fixes</span></span>

<span data-ttu-id="a8b13-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="a8b13-113">**Time and Expense**</span></span>

<span data-ttu-id="a8b13-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="a8b13-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="a8b13-115">Gestione un caso perimetral en **Eliminación de miembro del equipo del proyecto** para proporcionar una excepción significativa.</span><span class="sxs-lookup"><span data-stu-id="a8b13-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="a8b13-116">La importación de asignaciones da como resultado una pantalla de eliminación en blanco.</span><span class="sxs-lookup"><span data-stu-id="a8b13-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="a8b13-117">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="a8b13-117">**Resource Management**</span></span>

<span data-ttu-id="a8b13-118">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="a8b13-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a8b13-119">La **Tarjeta de recursos de la cuadrícula de utilización de recursos** muestra datos incorrectos cuando la escala de tiempo es superior a cinco días.</span><span class="sxs-lookup"><span data-stu-id="a8b13-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="a8b13-120">Cuando los clientes crean un recurso que se puede reservar, el complemento genera un error intermitentemente al agregar automáticamente el recurso a un grupo de Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="a8b13-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="a8b13-121">La vista **Conciliación** muestra los contornos manuales incorrectamente en la vista **Semana** o **Mes**.</span><span class="sxs-lookup"><span data-stu-id="a8b13-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="a8b13-122">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="a8b13-122">**Project Management**</span></span>

<span data-ttu-id="a8b13-123">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="a8b13-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="a8b13-124">Un número excesivo de entidades **RetrieveMultiple para usersettings** están causando un rendimiento degradado para aprobaciones de proyectos y otras operaciones.</span><span class="sxs-lookup"><span data-stu-id="a8b13-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="a8b13-125">La búsqueda de recursos de la cuadrícula **Planificación de tareas** se limita a mostrar solo hasta cinco miembros del equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a8b13-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="a8b13-126">La búsqueda de recursos de la cuadrícula **Planificación de tareas** no filtra los recursos inactivos.</span><span class="sxs-lookup"><span data-stu-id="a8b13-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="a8b13-127">El modo manual no funciona como se esperaba en la estructura de descomposición del trabajo de planificación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a8b13-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="a8b13-128">La cuadrícula **Planificación de tareas** muestra **Categorías de transacciones inactivas**.</span><span class="sxs-lookup"><span data-stu-id="a8b13-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="a8b13-129">La cuadrícula **Asignación de recursos** se redondea incorrectamente cuando una tarea tiene varias asignaciones.</span><span class="sxs-lookup"><span data-stu-id="a8b13-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="a8b13-130">Los valores de redondeo son diferentes entre el coste planificado y el coste real para una única tarea.</span><span class="sxs-lookup"><span data-stu-id="a8b13-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="a8b13-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a8b13-131">**Sales**</span></span>

<span data-ttu-id="a8b13-132">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="a8b13-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="a8b13-133">Hacer doble clic en **Capturar todas las categorías de transacciones** crea varias líneas.</span><span class="sxs-lookup"><span data-stu-id="a8b13-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
