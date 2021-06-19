---
title: Crear un proyecto
description: En este tema se proporciona información sobre cómo crear un proyecto nuevo.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006262"
---
# <a name="create-a-new-project"></a><span data-ttu-id="aef16-103">Crear un proyecto</span><span class="sxs-lookup"><span data-stu-id="aef16-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aef16-104">Para crear un nuevo proyecto, siga los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="aef16-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="aef16-105">En la página **Gestión de proyectos**, seleccione **Nuevo proyecto**, e indique los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="aef16-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="aef16-106">**Tipo de proyecto**: Tiempo y material</span><span class="sxs-lookup"><span data-stu-id="aef16-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="aef16-107">**Nombre del proyecto**: Fase 2 de la actualización XYZ</span><span class="sxs-lookup"><span data-stu-id="aef16-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="aef16-108">**Grupo de proyecto**: TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="aef16-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="aef16-109">**Id. de contrato de proyecto**: 00000002</span><span class="sxs-lookup"><span data-stu-id="aef16-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="aef16-110">Seleccione **Crear proyecto**.</span><span class="sxs-lookup"><span data-stu-id="aef16-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="aef16-111">Asignar un recurso a un proyecto</span><span class="sxs-lookup"><span data-stu-id="aef16-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="aef16-112">En la página **Trabajadores**, en la lista **Trabajadores**, seleccione el registro del trabajador para el que definió las competencias anteriormente y abra el registro del trabajador.</span><span class="sxs-lookup"><span data-stu-id="aef16-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="aef16-113">En el panel de acciones, en la pestaña **Proyecto**, en el grupo **Configurar**, seleccione **Asignar proyectos**.</span><span class="sxs-lookup"><span data-stu-id="aef16-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="aef16-114">En la página **Asignaciones de proyectos de validación de recursos**, en la pestaña **Proyectos**, en el campo **Agregar el proyecto a los proyectos seleccionados**, filtrar en el proyecto **Fase 2 de la actualización XYZ**.</span><span class="sxs-lookup"><span data-stu-id="aef16-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="aef16-115">En el panel **Proyectos restantes**, seleccione un proyecto y luego seleccione el botón de flecha para agregarlo al panel **Proyectos seleccionados**.</span><span class="sxs-lookup"><span data-stu-id="aef16-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="aef16-116">También puede asignar categorías para un recurso según lo requiera.</span><span class="sxs-lookup"><span data-stu-id="aef16-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="aef16-117">El tipo de categoría es **Coste** o **Ingresos**.</span><span class="sxs-lookup"><span data-stu-id="aef16-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="aef16-118">El tipo de categoría lo determina su organización.</span><span class="sxs-lookup"><span data-stu-id="aef16-118">The category type is determined by your organization.</span></span> <span data-ttu-id="aef16-119">Si no se asignan categorías para un recurso, Finance busca la categoría predeterminada en precios por hora para costes e ingresos.</span><span class="sxs-lookup"><span data-stu-id="aef16-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="aef16-120">Configurar las características de los roles y los recursos del proyecto</span><span class="sxs-lookup"><span data-stu-id="aef16-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="aef16-121">Un jefe de proyecto puede utilizar la funcionalidad de dotación de recursos de proyecto para crear los roles necesarios para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="aef16-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="aef16-122">Los roles se pueden usar si los recursos confirmados aún se desconocen cuando se reservan los recursos.</span><span class="sxs-lookup"><span data-stu-id="aef16-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="aef16-123">Los roles se pueden reservar temporalmente como recursos planificados, para que pueda continuar con las etapas de planificación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="aef16-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="aef16-124">[![Ejemplo de un rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="aef16-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="aef16-125">**Escenario:** Contoso fue contratado para completar un proyecto de tiempo y material que tiene un estatuto de proyecto aprobado.</span><span class="sxs-lookup"><span data-stu-id="aef16-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="aef16-126">El jefe de proyecto junior aún está completando el alcance del proyecto.</span><span class="sxs-lookup"><span data-stu-id="aef16-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="aef16-127">El administrador de recursos actualmente está identificando recursos específicos que se reservarán para trabajar en el nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="aef16-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="aef16-128">Debido a la naturaleza crítica del proyecto, el patrocinador del proyecto solicitó jefe de proyecto senior como uno de los roles.</span><span class="sxs-lookup"><span data-stu-id="aef16-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="aef16-129">El administrador de recursos debe adquirir el nuevo recurso y definir el rol en el sistema en caso de que el jefe de proyectos junior requiera la información de recursos durante la planificación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="aef16-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="aef16-130">Los siguientes pasos muestran cómo el administrador de recursos puede configurar el rol de jefe de proyectos senior y asociar características de recursos con él.</span><span class="sxs-lookup"><span data-stu-id="aef16-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="aef16-131">Posteriormente, el rol se puede utilizar para buscar recursos disponibles que coincidan con las competencias de recursos requeridas.</span><span class="sxs-lookup"><span data-stu-id="aef16-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="aef16-132">En la página **Configurar roles**, seleccione **Nuevo**, e indique los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="aef16-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="aef16-133">**Id. del rol**: jefe de proyectos sénior</span><span class="sxs-lookup"><span data-stu-id="aef16-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="aef16-134">**Descripción**: jefe de proyectos sénior</span><span class="sxs-lookup"><span data-stu-id="aef16-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="aef16-135">Seleccione **Crear**.</span><span class="sxs-lookup"><span data-stu-id="aef16-135">Select **Create**.</span></span>
3. <span data-ttu-id="aef16-136">Selecciona el rol **Jefe de proyectos sénior** y luego seleccione **Configurar características**.</span><span class="sxs-lookup"><span data-stu-id="aef16-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="aef16-137">En el campo **Tipo de característica**, seleccione **Aptitud**.</span><span class="sxs-lookup"><span data-stu-id="aef16-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="aef16-138">En el campo **Características disponibles**, indique la aptitud que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="aef16-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="aef16-139">En el campo **Tipo de característica**, seleccione **Certificado**.</span><span class="sxs-lookup"><span data-stu-id="aef16-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="aef16-140">En el campo **Características disponibles**, indique el tipo de certificado que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="aef16-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="aef16-141">Asignar un recurso de proyecto a un proyecto</span><span class="sxs-lookup"><span data-stu-id="aef16-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="aef16-142">En la página **Todos los proyectos**, seleccione el proyecto **Fase 2 de la actualización XYZ**.</span><span class="sxs-lookup"><span data-stu-id="aef16-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="aef16-143">En la pestaña **Equipo de proyecto y programación**, seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="aef16-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="aef16-144">En el campo **Rol** campo, seleccione **Miembro del equipo**.</span><span class="sxs-lookup"><span data-stu-id="aef16-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="aef16-145">Seleccione **Reservar en el calendario**.</span><span class="sxs-lookup"><span data-stu-id="aef16-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="aef16-146">En la página **Disponibilidad de recursos**, seleccione **Ver configuraciones**.</span><span class="sxs-lookup"><span data-stu-id="aef16-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="aef16-147">En la página **Ajustar la configuración de la vista**, escriba los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="aef16-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="aef16-148">**Formato para la vista de rango de fechas**: Día</span><span class="sxs-lookup"><span data-stu-id="aef16-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="aef16-149">**Mostrar descripciones de disponibilidad**: Sí</span><span class="sxs-lookup"><span data-stu-id="aef16-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="aef16-150">**Mostrar capacidad restante**: Sí</span><span class="sxs-lookup"><span data-stu-id="aef16-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="aef16-151">En la lista de recursos, seleccione un recurso.</span><span class="sxs-lookup"><span data-stu-id="aef16-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="aef16-152">Seleccione **Reserva manual** y **Capacidad completa**.</span><span class="sxs-lookup"><span data-stu-id="aef16-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="aef16-153">Asignar un recurso a un rol predeterminado</span><span class="sxs-lookup"><span data-stu-id="aef16-153">Assign a resource to a default role</span></span>

<span data-ttu-id="aef16-154">Para ayudar a los administradores de proyectos o recursos pueden explorar en profundidad más sobre los recursos que se pueden reservar para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="aef16-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="aef16-155">Puede asociar un rol predeterminado con un recurso existente o un recurso recién adquirido.</span><span class="sxs-lookup"><span data-stu-id="aef16-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="aef16-156">Por ejemplo, cuando contrataron a Daniel, tenía la experiencia y las aptitudes para ocupar el puesto de analista comercial.</span><span class="sxs-lookup"><span data-stu-id="aef16-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="aef16-157">El administrador de recursos asignó este rol como el rol predeterminado de Daniel.</span><span class="sxs-lookup"><span data-stu-id="aef16-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="aef16-158">Por lo tanto, el administrador de recursos agregó a Daniel a un grupo de analistas comerciales que están disponibles para trabajar en proyectos.</span><span class="sxs-lookup"><span data-stu-id="aef16-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="aef16-159">Durante la reserva de recursos, los jefes de proyecto pueden filtrar los recursos de roles que están disponibles para trabajar en proyectos.</span><span class="sxs-lookup"><span data-stu-id="aef16-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="aef16-160">Pueden utilizar esta información como un criterio cuando realizan análisis de decisiones de criterios múltiples durante la ejecución de los recursos.</span><span class="sxs-lookup"><span data-stu-id="aef16-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="aef16-161">También pueden agregar otras características de recursos al filtro para buscar recursos que tengan aptitudes, educación y experiencia específicas para un proyecto determinado.</span><span class="sxs-lookup"><span data-stu-id="aef16-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="aef16-162">**Escenario**: se ha iniciado un proyecto aprobado y se reservó el rol de jefe de proyecto sénior como recurso planificado durante la etapa de planificación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="aef16-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="aef16-163">El administrador de recursos ahora ha adquirido un recurso para ejecutar el rol de jefe de proyectos senior.</span><span class="sxs-lookup"><span data-stu-id="aef16-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="aef16-164">En la página **Lista de recursos**, seleccione **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="aef16-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="aef16-165">En la página **Rol del recurso**, seleccione **Nuevo**, e indique los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="aef16-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="aef16-166">**Vigencia a partir de**: indique la fecha actual.</span><span class="sxs-lookup"><span data-stu-id="aef16-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="aef16-167">**Vencimiento**: especificar **Nunca**.</span><span class="sxs-lookup"><span data-stu-id="aef16-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="aef16-168">**Rol**: especifique **Jefe de proyectos sénior**.</span><span class="sxs-lookup"><span data-stu-id="aef16-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="aef16-169">Seleccione **Guardar** y cierre la página.</span><span class="sxs-lookup"><span data-stu-id="aef16-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="aef16-170">En la pestaña **Competencias**, agregue la aptitud **ProjectMgmt** y el certificado **PMP**.</span><span class="sxs-lookup"><span data-stu-id="aef16-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]