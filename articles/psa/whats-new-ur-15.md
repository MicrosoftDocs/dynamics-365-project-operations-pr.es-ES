---
title: Novedades o cambios en la versión de actualización 15, V3, de Project Service Automation
description: Este tema proporciona información sobre las novedades de la versión de actualización 15 de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 0ec6746c0d3a1a03ee56440c73d044df844046f8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143984"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="eb959-103">Versión de actualización de Project Service Automation 15, V3</span><span class="sxs-lookup"><span data-stu-id="eb959-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="eb959-104">Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="eb959-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="eb959-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="eb959-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eb959-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="eb959-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eb959-107">Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="eb959-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="eb959-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="eb959-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eb959-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 15.</span><span class="sxs-lookup"><span data-stu-id="eb959-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="eb959-110">Esta versión tiene un número de compilación de V3.10.5.28 y está disponible con carácter general a través de una actualización automática en enero de 2020.</span><span class="sxs-lookup"><span data-stu-id="eb959-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="eb959-111">Versión de actualización 15</span><span class="sxs-lookup"><span data-stu-id="eb959-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="eb959-112">Mejoras</span><span class="sxs-lookup"><span data-stu-id="eb959-112">Enhancements</span></span>

- <span data-ttu-id="eb959-113">Administración del proyecto</span><span class="sxs-lookup"><span data-stu-id="eb959-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="eb959-114">Solución de errores</span><span class="sxs-lookup"><span data-stu-id="eb959-114">Bug fixes</span></span>

- <span data-ttu-id="eb959-115">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="eb959-115">Time and Expense</span></span>

  - <span data-ttu-id="eb959-116">Corregido: Agregar el manejo de errores en carga en la vista de conciliación.</span><span class="sxs-lookup"><span data-stu-id="eb959-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="eb959-117">Corregido: Centro de recursos de proyecto: Cambiar de nombre **Importe** para reducir la ambigüedad.</span><span class="sxs-lookup"><span data-stu-id="eb959-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="eb959-118">Corregido: Ajustar la vista **Copiar columnas de entrada de tiempo** para incluir el tipo.</span><span class="sxs-lookup"><span data-stu-id="eb959-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="eb959-119">Corregido: la edición de la duración de la entrada de tiempo en la vista de cuadrícula utilizando números decimales genera un error desconocido para algunos números.</span><span class="sxs-lookup"><span data-stu-id="eb959-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="eb959-120">Administración del proyecto</span><span class="sxs-lookup"><span data-stu-id="eb959-120">Project Management</span></span>

  - <span data-ttu-id="eb959-121">Corregido: El menú desplegable para **Usar en la vista de seguimiento** ahora se amplía según el ancho de las opciones.</span><span class="sxs-lookup"><span data-stu-id="eb959-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="eb959-122">Corregido: Al administrar proyectos en la zona horaria +13, los cálculos de tareas pueden mostrar resultados imprecisos.</span><span class="sxs-lookup"><span data-stu-id="eb959-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="eb959-123">Corregido: **Hora de finalización del miembro del equipo** se ha corregido al usar un calendario de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="eb959-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="eb959-124">Corregido: Se ha reactivado el **BPF** en el formulario principal de **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="eb959-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="eb959-125">Corregido: El cálculo de asignaciones ya no ignora un día.</span><span class="sxs-lookup"><span data-stu-id="eb959-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="eb959-126">Corregido: Se ha agregado un nuevo banner de notificación al formulario del proyecto cuando la zona horaria difiere entre el usuario y el proyecto.</span><span class="sxs-lookup"><span data-stu-id="eb959-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="eb959-127">Sales</span><span class="sxs-lookup"><span data-stu-id="eb959-127">Sales</span></span>

  - <span data-ttu-id="eb959-128">Corregido: La búsqueda de categoría de estimación de gastos se puede usar para filtrar duplicados.</span><span class="sxs-lookup"><span data-stu-id="eb959-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="eb959-129">Corregido: El código en **PluginDomain.ExecuteIn TryCatchBlock (..)** ya no oculta el origen de la excepción.</span><span class="sxs-lookup"><span data-stu-id="eb959-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="eb959-130">Corregido: Ya no aparece un mensaje de error en **Búsqueda de proyectos** en el formulario **Línea de oferta** cuando hay más de 1000 proyectos.</span><span class="sxs-lookup"><span data-stu-id="eb959-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="eb959-131">Corregido: La cuadrícula **Estimaciones** para estimaciones de mano de obra y estimaciones de gastos ahora muestra el símbolo de moneda correcto.</span><span class="sxs-lookup"><span data-stu-id="eb959-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="eb959-132">Corregido: Después de que una organización actualice PSA de la versión de actualización 14 a la versión de actualización 15, la pestaña **Programación** ya no aparece en blanco en el formulario **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="eb959-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
