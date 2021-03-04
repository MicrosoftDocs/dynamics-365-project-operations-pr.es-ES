---
title: Novedades o cambios en la versión de actualización 12, V3, de Project Service Automation
description: Este tema proporciona información sobre las novedades de la versión de actualización 12 de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143849"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="e5a4c-103">Versión de actualización de Project Service Automation 12, V3</span><span class="sxs-lookup"><span data-stu-id="e5a4c-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e5a4c-104">Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e5a4c-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e5a4c-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e5a4c-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e5a4c-107">Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e5a4c-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e5a4c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e5a4c-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 12.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="e5a4c-110">Esta versión tiene un número de compilación de V3.10.2.34 y está disponible con carácter general a través de una actualización automática en octubre de 2019.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="e5a4c-111">Versión de actualización 12</span><span class="sxs-lookup"><span data-stu-id="e5a4c-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e5a4c-112">Solución de errores</span><span class="sxs-lookup"><span data-stu-id="e5a4c-112">Bug fixes</span></span>

- <span data-ttu-id="e5a4c-113">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="e5a4c-113">Time and Expense</span></span>

    - <span data-ttu-id="e5a4c-114">Corregido: Los mensajes de error de entrada de tiempo se han actualizado con un contexto más relevante.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="e5a4c-115">Corregido: La programación y cuadrícula de entrada de tiempo muestra correctamente la barra de desplazamiento vertical cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="e5a4c-116">Corregido: Se pueden aprobar las entradas de tiempo y gasto enviadas.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="e5a4c-117">Corregido: Se ha corregido el mensaje de diálogo de confirmación de cancelación de aprobación para reflejar el estado de la aprobación cuando se cambia de **Aprobado** a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="e5a4c-118">Corregido: Los campos **Precio**, **Unidad** y **Cantidad** están ahora bloqueados en el registro Gasto después de que se haya aprobado.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="e5a4c-119">Administración del proyecto</span><span class="sxs-lookup"><span data-stu-id="e5a4c-119">Project Management</span></span>

    - <span data-ttu-id="e5a4c-120">Fijo: Se ha eliminado la acción **Nuevo** del formulario principal **Miembro del equipo**.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="e5a4c-121">Corregido: Se han actualizado las asignaciones de recursos para explicar errores de redondeo impreciso, que conducen a un cambio en la fecha de finalización de una tarea.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="e5a4c-122">Corregido: En la cuadrícula de tareas, los errores del lado del servidor relevantes aparecerán al usuario.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="e5a4c-123">Corregido: El nombre del miembro del equipo ahora se muestra en el selector de usuarios de la tarea en lugar del nombre del puesto.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="e5a4c-124">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="e5a4c-124">Resource Management</span></span>

    - <span data-ttu-id="e5a4c-125">Corregido: Los detalles de los requisitos de recursos para los proyectos creados a partir de una plantilla ahora usan el calendario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="e5a4c-126">Corregido: Las habilidades y competencias ahora pasan de manera predeterminada de los datos maestros de rol al requisito de recurso creado para ese rol.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="e5a4c-127">Sales</span><span class="sxs-lookup"><span data-stu-id="e5a4c-127">Sales</span></span>

    - <span data-ttu-id="e5a4c-128">Corregido: ID de objetos duplicados encontrados en el formulario **principal de contrato**.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="e5a4c-129">Corregido: La lógica se ha actualizado para hacer que la pestaña **Análisis de la oferta** esté visible para que muestre la configuración de metadatos de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="e5a4c-130">Corregido: La Fecha contable del registro actual ahora proviene de la fecha de entrada de tiempo/gasto y no de la fecha de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="e5a4c-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
