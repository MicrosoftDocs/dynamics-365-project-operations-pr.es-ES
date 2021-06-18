---
title: Configurar los recursos del proyecto
description: En este tema se proporciona información sobre configurar o solicitar recursos de proyecto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997712"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="3f24b-103">Configurar los recursos del proyecto</span><span class="sxs-lookup"><span data-stu-id="3f24b-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f24b-104">Debe configurar un calendario y asociarlo con un empleado o un trabajador.</span><span class="sxs-lookup"><span data-stu-id="3f24b-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="3f24b-105">El calendario se utiliza para programar el proyecto y el tiempo de trabajo de los recursos que están reservados para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="3f24b-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="3f24b-106">Durante la configuración del calendario, los administradores de proyectos pueden nivelar los recursos como parte de la optimización de los recursos.</span><span class="sxs-lookup"><span data-stu-id="3f24b-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="3f24b-107">Según la programación del calendario, se pueden imponer restricciones a los recursos.</span><span class="sxs-lookup"><span data-stu-id="3f24b-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="3f24b-108">Puede configurar un calendario en la página **Calendarios**.</span><span class="sxs-lookup"><span data-stu-id="3f24b-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="3f24b-109">Cuando configura un trabajador como recurso del proyecto, puede seleccionar entre los trabajadores que trabajan en la empresa para la que está configurando los recursos.</span><span class="sxs-lookup"><span data-stu-id="3f24b-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="3f24b-110">Alternativamente, puede seleccionar trabajadores de otras empresas de su organización.</span><span class="sxs-lookup"><span data-stu-id="3f24b-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="3f24b-111">Estos trabajadores se conocen como recursos de empresas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="3f24b-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="3f24b-112">Los siguientes procedimientos explican cómo configurar un trabajador como recurso de proyecto en su empresa y cómo configurar un recurso de proyecto de empresas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="3f24b-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="3f24b-113">Configurar un trabajador como recurso de proyecto</span><span class="sxs-lookup"><span data-stu-id="3f24b-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="3f24b-114">En la página **Trabajadores**, en lista **Trabajadores**, seleccione el trabajador que está agregando como recurso del proyecto y abra el registro del trabajador.</span><span class="sxs-lookup"><span data-stu-id="3f24b-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="3f24b-115">En el panel de acciones, seleccione **Proyecto** &gt; **Configurar** &gt; **Configuración del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="3f24b-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="3f24b-116">Seleccione un calendario y cierre la página.</span><span class="sxs-lookup"><span data-stu-id="3f24b-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="3f24b-117">También puede especificar proyectos predeterminados para un recurso como un tipo de asignación previa.</span><span class="sxs-lookup"><span data-stu-id="3f24b-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="3f24b-118">Las asignaciones previas se pueden usar cuando el administrador de recursos o el administrador de proyectos sepan con anticipación en qué proyectos trabajará el recurso.</span><span class="sxs-lookup"><span data-stu-id="3f24b-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="3f24b-119">Las asignaciones previas también pueden basarse en la solicitud de un cliente o patrocinador del proyecto.</span><span class="sxs-lookup"><span data-stu-id="3f24b-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="3f24b-120">Para asignar previamente un proyecto, en la página **Asignar proyectos**, en la pestaña **Proyectos**, en la lista **Proyectos restantes**, seleccione el proyecto apropiado.</span><span class="sxs-lookup"><span data-stu-id="3f24b-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="3f24b-121">Configurar un recurso de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="3f24b-121">Set up an intercompany resource</span></span>

<span data-ttu-id="3f24b-122">Cuando configura un trabajador como recurso de empresas vinculadas, debe completar la configuración tanto en la empresa prestamista como en la empresa prestataria.</span><span class="sxs-lookup"><span data-stu-id="3f24b-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="3f24b-123">En la empresa prestamista</span><span class="sxs-lookup"><span data-stu-id="3f24b-123">In the lending company</span></span>

1. <span data-ttu-id="3f24b-124">En Finance, verifique que la empresa prestamista esté seleccionada y luego complete el procedimiento de la sección anterior, "Configurar un trabajador como recurso de proyecto".</span><span class="sxs-lookup"><span data-stu-id="3f24b-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="3f24b-125">En la página **Contabilidad de empresas vinculadas**, seleccione **+Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="3f24b-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="3f24b-126">En el campo **Id. de entidad legal**, seleccione la empresa prestamista.</span><span class="sxs-lookup"><span data-stu-id="3f24b-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="3f24b-127">Rellene los campos restantes como corresponda y seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="3f24b-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="3f24b-128">En la página **Transferir precios**, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="3f24b-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="3f24b-129">En el campo **Entidad legal prestataria**, seleccione la empresa apropiada.</span><span class="sxs-lookup"><span data-stu-id="3f24b-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="3f24b-130">Para prestar a la empresa prestataria solo el recurso que creó al principio de esta sección, en el campo **Recurso**, seleccione el nombre del recurso que creó.</span><span class="sxs-lookup"><span data-stu-id="3f24b-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="3f24b-131">Para que todos los recursos de la empresa prestamista estén disponibles para la empresa prestataria, deje el campo **Recurso** en blanco.</span><span class="sxs-lookup"><span data-stu-id="3f24b-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="3f24b-132">En la página **Parámetros de gestión de proyectos y contabilidad**, en la pestaña **Empresas vinculadas**, establezca la opción **Habilitar la programación de recursos y las hojas de horas de empresas vinculadas** en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="3f24b-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="3f24b-133">En la empresa prestataria</span><span class="sxs-lookup"><span data-stu-id="3f24b-133">In the borrowing company</span></span>

- <span data-ttu-id="3f24b-134">En la página **Lista de recursos**, en el filtro de búsqueda, especifique el nombre del recurso que creó para la empresa prestamista, para verificar que el nombre esté incluido en la lista de recursos para la empresa prestataria.</span><span class="sxs-lookup"><span data-stu-id="3f24b-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="3f24b-135">Solicitar recursos del proyecto</span><span class="sxs-lookup"><span data-stu-id="3f24b-135">Request project resources</span></span>
<span data-ttu-id="3f24b-136">La funcionalidad para la programación de recursos del proyecto solo permite a los administradores de recursos distribuir los recursos del personal en compromisos o proyectos.</span><span class="sxs-lookup"><span data-stu-id="3f24b-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="3f24b-137">Para habilitar esta funcionalidad, complete las siguientes tareas o verifique que se hayan completado:</span><span class="sxs-lookup"><span data-stu-id="3f24b-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="3f24b-138">Configurar las secuencias numéricas.</span><span class="sxs-lookup"><span data-stu-id="3f24b-138">Set up number sequences.</span></span>
- <span data-ttu-id="3f24b-139">Configurar los flujos de trabajo de gestión de proyectos y contabilidad.</span><span class="sxs-lookup"><span data-stu-id="3f24b-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="3f24b-140">Habilite los flujos de trabajo de solicitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f24b-140">Enable resource request workflows.</span></span>

<span data-ttu-id="3f24b-141">Una vez completadas las tareas anteriores, puede completar las siguientes tareas según sea necesario:</span><span class="sxs-lookup"><span data-stu-id="3f24b-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="3f24b-142">Cree una solicitud de recurso a partir de un recurso con personal reservado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="3f24b-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="3f24b-143">Supervise solicitudes de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f24b-143">Monitor resource requests.</span></span>
- <span data-ttu-id="3f24b-144">Ejecute solicitudes de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f24b-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="3f24b-145">Solicite un recurso con personal de una WBS.</span><span class="sxs-lookup"><span data-stu-id="3f24b-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="3f24b-146">Reserve recursos para un proyecto sin tener una solicitud de recursos con personal.</span><span class="sxs-lookup"><span data-stu-id="3f24b-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]