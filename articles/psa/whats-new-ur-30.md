---
title: Novedades o cambios en la versión de actualización 30, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 30, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010447"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="54417-103">Novedades o cambios en la versión de actualización 30, V3, de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="54417-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="54417-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="54417-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="54417-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="54417-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="54417-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="54417-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="54417-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="54417-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="54417-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="54417-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="54417-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 30.</span><span class="sxs-lookup"><span data-stu-id="54417-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="54417-110">Esta versión tiene un número de compilación de V3.10.51.61 y generalmente está disponible a través de una actualización automática en abril de 2021.</span><span class="sxs-lookup"><span data-stu-id="54417-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="54417-111">Versión de actualización 30</span><span class="sxs-lookup"><span data-stu-id="54417-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="54417-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="54417-112">Bug fixes</span></span>

<span data-ttu-id="54417-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="54417-113">**Time and Expense**</span></span>

<span data-ttu-id="54417-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="54417-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="54417-115">Se produce un error cuando crea y guarda una entrada de tiempo en la página **Creación rápida** si campo **Rol** se elimina.</span><span class="sxs-lookup"><span data-stu-id="54417-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="54417-116">El filtro de entrada de tiempo aplica el operador de filtro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="54417-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="54417-117">Los partes de horas copiados no se muestran automáticamente cuando selecciona **Copiar semana** en el control de entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="54417-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="54417-118">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="54417-118">**Resource Management**</span></span>

<span data-ttu-id="54417-119">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="54417-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="54417-120">Cuando amplía una reserva, el estado de reserva asignado a la reserva física es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="54417-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="54417-121">La ampliación de una reserva respeta el estado de la reserva definido como **Comprometido** en los metadatos de configuración de la reserva.</span><span class="sxs-lookup"><span data-stu-id="54417-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="54417-122">Cuando no se especifica un estado de reserva válido, el mensaje de error no se localiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="54417-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="54417-123">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="54417-123">**Project Management**</span></span>

<span data-ttu-id="54417-124">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="54417-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="54417-125">Los proyectos no se pueden crear en una divisa e incluir tareas relacionadas en otra divisa.</span><span class="sxs-lookup"><span data-stu-id="54417-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="54417-126">**Ventas**</span><span class="sxs-lookup"><span data-stu-id="54417-126">**Sales**</span></span>

<span data-ttu-id="54417-127">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="54417-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="54417-128">Cuando se copia una lista de precios, los precios no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="54417-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="54417-129">El cierre de una cotización como obtenida produce errores cuando el detalle del coste tiene un valor para el origen.</span><span class="sxs-lookup"><span data-stu-id="54417-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="54417-130">En la entidad **Tarea de proyecto**, **Coste estimado** ha sido renombrado a **Coste planificado (base)**.</span><span class="sxs-lookup"><span data-stu-id="54417-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="54417-131">Se genera una excepción de referencia nula cuando se crean o eliminan facturas.</span><span class="sxs-lookup"><span data-stu-id="54417-131">A null reference exception is generated when invoices are created or deleted.</span></span>
