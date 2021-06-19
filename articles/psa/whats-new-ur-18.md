---
title: Novedades o cambios en la versión de actualización 18, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 18, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006667"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="79a9c-103">Versión de actualización de Project Service Automation 18, V3</span><span class="sxs-lookup"><span data-stu-id="79a9c-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="79a9c-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="79a9c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="79a9c-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="79a9c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="79a9c-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="79a9c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="79a9c-107">Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea, página de soluciones para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="79a9c-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="79a9c-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="79a9c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="79a9c-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 18.</span><span class="sxs-lookup"><span data-stu-id="79a9c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="79a9c-110">Esta versión tiene un número de compilación de V3.10.8.12 y generalmente está disponible a través de una actualización automática en abril de 2020.</span><span class="sxs-lookup"><span data-stu-id="79a9c-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="79a9c-111">Versión de actualización 18</span><span class="sxs-lookup"><span data-stu-id="79a9c-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="79a9c-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="79a9c-112">Bug fixes</span></span>

<span data-ttu-id="79a9c-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="79a9c-113">**Time and Expense**</span></span>

- <span data-ttu-id="79a9c-114">Corregido: los flujos **Recordar**, **Solicitud** y **Cancelar aprobación** arrojan excepciones con mensajes de error poco claros.</span><span class="sxs-lookup"><span data-stu-id="79a9c-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="79a9c-115">Corregido: cuando **Cancelar aprobación** falla por un gasto, no se produce un error de excepción relevante.</span><span class="sxs-lookup"><span data-stu-id="79a9c-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="79a9c-116">Corregido: la cuadrícula de entrada de tiempo gestiona incorrectamente los días no laborables en Australia después del cambio de horario de verano (DST) en octubre.</span><span class="sxs-lookup"><span data-stu-id="79a9c-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="79a9c-117">Corregido: la lógica de incumplimiento incorrecta impide el envío de gastos.</span><span class="sxs-lookup"><span data-stu-id="79a9c-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="79a9c-118">Corregido: cuando falla la aprobación de entrada de tiempo, la aprobación permanece en un estado de **Pendiente**.</span><span class="sxs-lookup"><span data-stu-id="79a9c-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="79a9c-119">Corregido: errores de SQL en aprobaciones masivas (interbloqueo/tiempo de espera).</span><span class="sxs-lookup"><span data-stu-id="79a9c-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="79a9c-120">Corregido: problemas de rendimiento significativos en la experiencia del usuario causados por la actualización de los miembros del equipo al aprobar las entradas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="79a9c-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="79a9c-121">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="79a9c-121">**Project Management**</span></span>

- <span data-ttu-id="79a9c-122">Corregido: notificación de zona horaria movida desde la vista **Reconciliación** al formulario principal de **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="79a9c-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="79a9c-123">Corregido: la plantilla del calendario no se configura en sus valores predeterminados de manera correcta cuando se abre un nuevo formulario de proyecto.</span><span class="sxs-lookup"><span data-stu-id="79a9c-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="79a9c-124">Corregido: para los navegadores basados en cromo, los usuarios no pueden seleccionar fácilmente las tareas predecesoras para eliminar.</span><span class="sxs-lookup"><span data-stu-id="79a9c-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="79a9c-125">Corregido: crear o copiar **Proyecto desde una plantilla vacía** captura asignaciones no relacionadas.</span><span class="sxs-lookup"><span data-stu-id="79a9c-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="79a9c-126">Corregido: en casos extremos específicos, la creación de una nueva asignación a partir de la cuadrícula de tareas produce una creación de registros duplicados.</span><span class="sxs-lookup"><span data-stu-id="79a9c-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="79a9c-127">Corregido: en modo manual, los usuarios no pueden actualizar las fechas de inicio de las tareas para que sean posteriores a la fecha actual guardada.</span><span class="sxs-lookup"><span data-stu-id="79a9c-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="79a9c-128">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="79a9c-128">**Resource Management**</span></span>

- <span data-ttu-id="79a9c-129">Corregido: la fila del subtotal de la vista **Reconciliación** calcula incorrectamente la varianza de las reservas después de extender las reservas.</span><span class="sxs-lookup"><span data-stu-id="79a9c-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="79a9c-130">Corregido: la vista **Reconciliación** muestra incorrectamente las asignaciones de recursos cuando el recurso que se puede reservar tiene un calendario que no coincide con el calendario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="79a9c-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="79a9c-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="79a9c-131">**Sales**</span></span>

- <span data-ttu-id="79a9c-132">Corregido: cuando las entradas de tiempo se vuelven a aprobar (**Aprobar > Cancelar >**, aprobar nuevamente), se crea un duplicado real no imputable.</span><span class="sxs-lookup"><span data-stu-id="79a9c-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]