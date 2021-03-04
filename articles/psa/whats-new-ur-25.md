---
title: Novedades o cambios en la versión de actualización 25, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 25, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143802"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="9ccd7-103">Novedades o cambios en la versión de actualización 25, V3, de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9ccd7-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9ccd7-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9ccd7-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9ccd7-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9ccd7-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9ccd7-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9ccd7-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9ccd7-109">Este tema enumera las características y correcciones nuevas o modificadas para Project Service Automation V3, Update Release 25. Esta versión tiene un número de compilación de V 3.10.43.76 y generalmente está disponible a través de una actualización automática en octubre de 2020.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="9ccd7-110">Versión de actualización 25</span><span class="sxs-lookup"><span data-stu-id="9ccd7-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9ccd7-111">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="9ccd7-111">Bug fixes</span></span>

<span data-ttu-id="9ccd7-112">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="9ccd7-112">**Time and Expense**</span></span>

<span data-ttu-id="9ccd7-113">Se ha resuelto el siguiente problema:</span><span class="sxs-lookup"><span data-stu-id="9ccd7-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="9ccd7-114">Gráfico de entrada de tiempo que muestra datos adicionales basados en un intervalo demasiado grande que se está recuperando.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="9ccd7-115">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="9ccd7-115">**Resource Management**</span></span>

<span data-ttu-id="9ccd7-116">Se ha resuelto el siguiente problema:</span><span class="sxs-lookup"><span data-stu-id="9ccd7-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="9ccd7-117">Se agregó el código de Package Deployer para omitir la importación del parche de Universal Resource Scheduling si ya existe un parche de versión superior.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="9ccd7-118">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="9ccd7-118">**Project Management**</span></span>

<span data-ttu-id="9ccd7-119">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="9ccd7-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="9ccd7-120">Se corrigieron las discrepancias de redondeo y tipo de cambio que dieron como resultado un costo planificado incorrecto en la cuadrícula de seguimiento del proyecto.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="9ccd7-121">Admite la capacidad de mostrar dos o más cuadrículas de reacción en el formulario del **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="9ccd7-122">Se proporcionó validación para abordar la capacidad de asignar una tarea después de la fecha de finalización del calendario, lo que da como resultado una asignación de recursos fallida.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="9ccd7-123">Manejo de errores mejorado para abordar la excepción de referencia nula generada a partir de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ccd7-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="9ccd7-124">Complemento **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="9ccd7-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="9ccd7-125">**PreValidateProjectTaskCreate** cuando se crea una tarea de proyecto sin un proyecto asociado</span><span class="sxs-lookup"><span data-stu-id="9ccd7-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="9ccd7-126">Complemento **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="9ccd7-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="9ccd7-127">Complemento **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="9ccd7-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="9ccd7-128">Complemento **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="9ccd7-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="9ccd7-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9ccd7-129">**Sales**</span></span>

<span data-ttu-id="9ccd7-130">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="9ccd7-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="9ccd7-131">Manejo de errores mejorado para abordar las excepciones de referencia nulas generadas **Copiar proyecto: Asistente de estimaciones Gestión de recursos**.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="9ccd7-132">**No listo para facturar** en un **Backlog de facturación de tiempo y material** no borra el estado de facturación.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="9ccd7-133">Corregidos los botones **Precios** mal etiquetados en la pestaña **Precio del rol** y **Artículos del catálogo**.</span><span class="sxs-lookup"><span data-stu-id="9ccd7-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
