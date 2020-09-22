---
title: Novedades en la versión de actualización 12, de Project Service Automation V3
description: Este tema proporciona información sobre las novedades de la versión de actualización 12 de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756006"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="6b5d6-103">Versión de actualización 12 Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="6b5d6-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="6b5d6-104">Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="6b5d6-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6b5d6-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6b5d6-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6b5d6-107">Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6b5d6-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6b5d6-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6b5d6-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 12.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="6b5d6-110">Esta versión tiene un número de compilación de V3.10.2.34 y está disponible con carácter general a través de una actualización automática en octubre de 2019.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="6b5d6-111">Versión de actualización 12</span><span class="sxs-lookup"><span data-stu-id="6b5d6-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6b5d6-112">Solución de errores</span><span class="sxs-lookup"><span data-stu-id="6b5d6-112">Bug fixes</span></span>

- <span data-ttu-id="6b5d6-113">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="6b5d6-113">Time and Expense</span></span>

    - <span data-ttu-id="6b5d6-114">Corregido: Los mensajes de error de entrada de tiempo se han actualizado con un contexto más relevante.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="6b5d6-115">Corregido: La programación y cuadrícula de entrada de tiempo muestra correctamente la barra de desplazamiento vertical cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="6b5d6-116">Corregido: Se pueden aprobar las entradas de tiempo y gasto enviadas.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="6b5d6-117">Corregido: Se ha corregido el mensaje de diálogo de confirmación de cancelación de aprobación para reflejar el estado de la aprobación cuando se cambia de **Aprobado** a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="6b5d6-118">Corregido: Los campos **Precio**, **Unidad** y **Cantidad** están ahora bloqueados en el registro Gasto después de que se haya aprobado.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="6b5d6-119">Administración del proyecto</span><span class="sxs-lookup"><span data-stu-id="6b5d6-119">Project Management</span></span>

    - <span data-ttu-id="6b5d6-120">Fijo: Se ha eliminado la acción **Nuevo** del formulario principal **Miembro del equipo**.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="6b5d6-121">Corregido: Se han actualizado las asignaciones de recursos para explicar errores de redondeo impreciso, que conducen a un cambio en la fecha de finalización de una tarea.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="6b5d6-122">Corregido: En la cuadrícula de tareas, los errores del lado del servidor relevantes aparecerán al usuario.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="6b5d6-123">Corregido: El nombre del miembro del equipo ahora se muestra en el selector de usuarios de la tarea en lugar del nombre del puesto.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="6b5d6-124">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="6b5d6-124">Resource Management</span></span>

    - <span data-ttu-id="6b5d6-125">Corregido: Los detalles de los requisitos de recursos para los proyectos creados a partir de una plantilla ahora usan el calendario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="6b5d6-126">Corregido: Las habilidades y competencias ahora pasan de manera predeterminada de los datos maestros de rol al requisito de recurso creado para ese rol.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="6b5d6-127">Sales</span><span class="sxs-lookup"><span data-stu-id="6b5d6-127">Sales</span></span>

    - <span data-ttu-id="6b5d6-128">Corregido: ID de objetos duplicados encontrados en el formulario **principal de contrato**.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="6b5d6-129">Corregido: La lógica se ha actualizado para hacer que la pestaña **Análisis de la oferta** esté visible para que muestre la configuración de metadatos de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="6b5d6-130">Corregido: La Fecha contable del registro actual ahora proviene de la fecha de entrada de tiempo/gasto y no de la fecha de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
