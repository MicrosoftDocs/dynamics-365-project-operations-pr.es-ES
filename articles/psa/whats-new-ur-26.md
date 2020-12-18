---
title: Novedades o cambios en la versión de actualización 26, V3, de Project Service Automation
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643284"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="2e5e8-102">Versión de actualización de Project Service Automation 26, V3</span><span class="sxs-lookup"><span data-stu-id="2e5e8-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="2e5e8-103">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2e5e8-104">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2e5e8-105">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2e5e8-106">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2e5e8-107">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2e5e8-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2e5e8-108">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation, versión de actualización 26, V3.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="2e5e8-109">Esta versión tiene un número de compilación de V3.10.44.59 y es de lanzamiento público mediante una actualización automática desde diciembre de 2020.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="2e5e8-110">Versión de actualización 26</span><span class="sxs-lookup"><span data-stu-id="2e5e8-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="2e5e8-111">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="2e5e8-111">Bug fixes</span></span>

<span data-ttu-id="2e5e8-112">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="2e5e8-112">**Time and Expense**</span></span>

<span data-ttu-id="2e5e8-113">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="2e5e8-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="2e5e8-114">Los usuarios pueden cambiar la tarea en una entrada de tiempo que haya sido aprobada o enviada.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="2e5e8-115">Error "Referencia de objeto no establecida" al guardar la entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="2e5e8-116">La importación de entradas de tiempo desde asignaciones de recursos crea entradas de tiempo con valores de DateTime incorrectos.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="2e5e8-117">Cuando se instalan Project Service Automation y la aplicación Field Service, el botón **Nuevo** se muestra dos veces en la barra de comandos para las entradas de tiempo en la aplicación Field Service.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="2e5e8-118">Las actualizaciones de celdas de **Permitir unidad** y **Unidad de venta** ahora trabajan de la cuadrícula **Estimaciones de gastos**.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="2e5e8-119">El formulario **Actualizar edición de entrada de tiempo** incluye **Escala de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="2e5e8-120">La aprobación de tiempo para entradas de tiempo que no sean del proyecto bloquea el sistema al buscar un rol de aprobador de proyectos.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="2e5e8-121">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="2e5e8-121">**Resource Management**</span></span>

<span data-ttu-id="2e5e8-122">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="2e5e8-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="2e5e8-123">Validación agregada en el complemento **PostProjectCreate** para comprobar si hay un requisito principal antes de crear uno.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="2e5e8-124">El formulario de creación rápida **Miembro del equipo del proyecto** genera una excepción de referencia nula si los campos se eliminan del formulario.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="2e5e8-125">Se producirá un error en la generación de requisitos durante 12 horas durante 1 año.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="2e5e8-126">Se ha mejorado la excepción de referencia nula del mensaje de error durante la creación de requisitos de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="2e5e8-127">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="2e5e8-127">**Project Management**</span></span>

<span data-ttu-id="2e5e8-128">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="2e5e8-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="2e5e8-129">Validación mejorada para abordar la excepción de referencia nula generada en el complemento **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="2e5e8-130">Los proyectos publicados por el complemento de escritorio de Microsoft Project eliminan las asignaciones no asignadas.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="2e5e8-131">Se agregó una nueva validación cuando la referencia del proyecto de una tarea no es válida debido a una excepción de referencia nula en el complemento **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="2e5e8-132">La cuadrícula Miembro del equipo no muestra asignaciones distintas en el registro de miembros del equipo.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="2e5e8-133">Se agregaron nuevos mensajes de validación y error debido a una excepción de referencia nula en el complemento **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="2e5e8-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2e5e8-134">**Sales**</span></span>

<span data-ttu-id="2e5e8-135">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="2e5e8-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="2e5e8-136">Al seleccionar una línea basada en proyecto en la oferta o el contrato, el botón **Sugerencia** solo debe estar visible al seleccionar una línea basada en producto asociada a un producto existente.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="2e5e8-137">Dividir el privilegio **Create_Product** desde el privilegio **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="2e5e8-138">La eliminación de una línea de factura provoca una error de referencia nula en **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
