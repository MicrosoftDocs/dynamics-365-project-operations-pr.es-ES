---
title: Utilizar las API de programación para realizar operaciones con entidades de programación
description: Este tema proporciona información y ejemplos para usar las API de programación.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950825"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="d0eda-103">Utilizar las API de programación para realizar operaciones con entidades de programación</span><span class="sxs-lookup"><span data-stu-id="d0eda-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="d0eda-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="d0eda-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="d0eda-105">Parte o toda la funcionalidad que se menciona en este tema está disponible como parte de una versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="d0eda-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="d0eda-106">El contenido y la funcionalidad están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0eda-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="d0eda-107">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="d0eda-107">Scheduling entities</span></span>

<span data-ttu-id="d0eda-108">Las API de programación brindan la capacidad de realizar operaciones de creación, actualización y eliminación con **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="d0eda-109">Estas entidades se administran a través del motor de programación en Project para la web.</span><span class="sxs-lookup"><span data-stu-id="d0eda-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="d0eda-110">Crear, actualizar y eliminar operaciones con **Entidades de programación** estaba restringido en versiones anteriores de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d0eda-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="d0eda-111">La siguiente tabla proporciona una lista completa de las **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="d0eda-112">Nombre de entidad</span><span class="sxs-lookup"><span data-stu-id="d0eda-112">Entity name</span></span>  | <span data-ttu-id="d0eda-113">Nombre lógico de la entidad</span><span class="sxs-lookup"><span data-stu-id="d0eda-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="d0eda-114">Project</span><span class="sxs-lookup"><span data-stu-id="d0eda-114">Project</span></span> | <span data-ttu-id="d0eda-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="d0eda-115">msdyn_project</span></span> |
| <span data-ttu-id="d0eda-116">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-116">Project Task</span></span>  | <span data-ttu-id="d0eda-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="d0eda-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="d0eda-118">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-118">Project Task Dependency</span></span>  | <span data-ttu-id="d0eda-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="d0eda-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="d0eda-120">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="d0eda-120">Resource Assignment</span></span> | <span data-ttu-id="d0eda-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="d0eda-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="d0eda-122">Cubo de proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-122">Project Bucket</span></span>  | <span data-ttu-id="d0eda-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="d0eda-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="d0eda-124">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-124">Project Team Member</span></span> | <span data-ttu-id="d0eda-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="d0eda-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="d0eda-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="d0eda-126">OperationSet</span></span>

<span data-ttu-id="d0eda-127">OperationSet es un patrón de unidad de trabajo que se puede usar cuando se deben procesar varias solicitudes que afectan la programación dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="d0eda-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="d0eda-128">Programar las API</span><span class="sxs-lookup"><span data-stu-id="d0eda-128">Schedule APIs</span></span>

<span data-ttu-id="d0eda-129">La siguiente es una lista de las API de programación actuales.</span><span class="sxs-lookup"><span data-stu-id="d0eda-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="d0eda-130">**msdyn_CreateProjectV1**: esta API se puede utilizar para crear un proyecto.</span><span class="sxs-lookup"><span data-stu-id="d0eda-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="d0eda-131">El proyecto y el cubo del proyecto predeterminado se crean inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d0eda-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="d0eda-132">**msdyn_CreateTeamMemberV1**: esta API se puede utilizar para crear un miembro de equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d0eda-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="d0eda-133">El registro de miembro del equipo se crea inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d0eda-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="d0eda-134">**msdyn_CreateOperationSetV1**: esta API se puede utilizar para programar varias solicitudes que deben realizarse dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="d0eda-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="d0eda-135">**msdyn_PSSCreateV1**: esta API se puede utilizar para crear una entidad.</span><span class="sxs-lookup"><span data-stu-id="d0eda-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="d0eda-136">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de creación.</span><span class="sxs-lookup"><span data-stu-id="d0eda-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="d0eda-137">**msdyn_PSSUpdateV1**: esta API se puede utilizar para actualizar una entidad.</span><span class="sxs-lookup"><span data-stu-id="d0eda-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="d0eda-138">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="d0eda-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="d0eda-139">**msdyn_PSSDeleteV1**: esta API se puede utilizar para eliminar una entidad.</span><span class="sxs-lookup"><span data-stu-id="d0eda-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="d0eda-140">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="d0eda-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="d0eda-141">**msdyn_ExecuteOperationSetV1**: esta API se utiliza para ejecutar todas las operaciones dentro del conjunto de operaciones establecido.</span><span class="sxs-lookup"><span data-stu-id="d0eda-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="d0eda-142">Utilizar las API de programación con OperationSet</span><span class="sxs-lookup"><span data-stu-id="d0eda-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="d0eda-143">Porque los registros con ambos **CreateProjectV1** y **CreateTeamMemberV1** se crean inmediatamente, estas API no se pueden utilizar en **OperationSet** directamente.</span><span class="sxs-lookup"><span data-stu-id="d0eda-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="d0eda-144">Sin embargo, puede utilizar la API para crear los registros necesarios, crear un **OperationSet** y, a continuación, utilizar estos registros creados previamente en **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="d0eda-145">Operaciones admitidas</span><span class="sxs-lookup"><span data-stu-id="d0eda-145">Supported operations</span></span>

| <span data-ttu-id="d0eda-146">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="d0eda-146">Scheduling entity</span></span> | <span data-ttu-id="d0eda-147">Crear</span><span class="sxs-lookup"><span data-stu-id="d0eda-147">Create</span></span> | <span data-ttu-id="d0eda-148">Actualización</span><span class="sxs-lookup"><span data-stu-id="d0eda-148">Update</span></span> | <span data-ttu-id="d0eda-149">Delete</span><span class="sxs-lookup"><span data-stu-id="d0eda-149">Delete</span></span> | <span data-ttu-id="d0eda-150">Consideraciones importantes</span><span class="sxs-lookup"><span data-stu-id="d0eda-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="d0eda-151">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-151">Project task</span></span> | <span data-ttu-id="d0eda-152">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-152">Yes</span></span> | <span data-ttu-id="d0eda-153">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-153">Yes</span></span> | <span data-ttu-id="d0eda-154">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-154">Yes</span></span> | <span data-ttu-id="d0eda-155">Nada</span><span class="sxs-lookup"><span data-stu-id="d0eda-155">None</span></span> |
| <span data-ttu-id="d0eda-156">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-156">Project task dependency</span></span> | <span data-ttu-id="d0eda-157">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-157">Yes</span></span> | <span data-ttu-id="d0eda-158">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-158">Yes</span></span> | | <span data-ttu-id="d0eda-159">Los registros de dependencia de tareas del proyecto no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="d0eda-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="d0eda-160">En su lugar, se puede eliminar un registro antiguo y se puede crear un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="d0eda-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="d0eda-161">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="d0eda-161">Resource assignment</span></span> | <span data-ttu-id="d0eda-162">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-162">Yes</span></span> | <span data-ttu-id="d0eda-163">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-163">Yes</span></span> | | <span data-ttu-id="d0eda-164">No se admiten las operaciones con los siguientes campos: **BookableResourceID**, **Esfuerzo**, **EffortCompleted**, **EffortCompleted** y **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="d0eda-165">Los registros de asignación de recursos no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="d0eda-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="d0eda-166">En su lugar, se puede eliminar el registro antiguo y se puede crear un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="d0eda-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="d0eda-167">Cubo de proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-167">Project bucket</span></span> | <span data-ttu-id="d0eda-168">N/D</span><span class="sxs-lookup"><span data-stu-id="d0eda-168">N/A</span></span> | <span data-ttu-id="d0eda-169">N/D</span><span class="sxs-lookup"><span data-stu-id="d0eda-169">N/A</span></span> | <span data-ttu-id="d0eda-170">N/D</span><span class="sxs-lookup"><span data-stu-id="d0eda-170">N/A</span></span> | <span data-ttu-id="d0eda-171">El cubo predeterminado se crea utilizando la API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="d0eda-172">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-172">Project team member</span></span> | <span data-ttu-id="d0eda-173">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-173">Yes</span></span> | <span data-ttu-id="d0eda-174">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-174">Yes</span></span> | <span data-ttu-id="d0eda-175">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-175">Yes</span></span> | <span data-ttu-id="d0eda-176">Para la operación de creación, use la API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="d0eda-177">Project</span><span class="sxs-lookup"><span data-stu-id="d0eda-177">Project</span></span> | <span data-ttu-id="d0eda-178">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-178">Yes</span></span> | <span data-ttu-id="d0eda-179">Sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-179">Yes</span></span> | <span data-ttu-id="d0eda-180">N/D</span><span class="sxs-lookup"><span data-stu-id="d0eda-180">N/A</span></span> | <span data-ttu-id="d0eda-181">No se admiten operaciones con los siguientes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esfuerzo**, **EffortCompleted**, **EffortRemaining**, **Progreso**, **Terminar**, **TaskEarliestStart**, y **Duración**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="d0eda-182">Estas API se pueden llamar con objetos de entidad que incluyen campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="d0eda-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="d0eda-183">La propiedad del identificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="d0eda-183">The ID property is optional.</span></span> <span data-ttu-id="d0eda-184">Si se proporciona, el sistema intenta usarlo y lanza una excepción si no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="d0eda-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="d0eda-185">Si no se proporciona, el sistema lo generará.</span><span class="sxs-lookup"><span data-stu-id="d0eda-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="d0eda-186">Campos restringidos</span><span class="sxs-lookup"><span data-stu-id="d0eda-186">Restricted fields</span></span>

<span data-ttu-id="d0eda-187">Las siguientes tablas definen los campos que están restringidos para **Crear** y **Editar.**</span><span class="sxs-lookup"><span data-stu-id="d0eda-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="d0eda-188">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-188">Project task</span></span>

| <span data-ttu-id="d0eda-189">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="d0eda-189">**Logical name**</span></span>                       | <span data-ttu-id="d0eda-190">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="d0eda-190">**Can create**</span></span> | <span data-ttu-id="d0eda-191">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="d0eda-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="d0eda-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="d0eda-193">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-193">no</span></span>             | <span data-ttu-id="d0eda-194">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-194">no</span></span>               |
| <span data-ttu-id="d0eda-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="d0eda-196">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-196">no</span></span>             | <span data-ttu-id="d0eda-197">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-197">no</span></span>               |
| <span data-ttu-id="d0eda-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="d0eda-198">msdyn_actualend</span></span>                        | <span data-ttu-id="d0eda-199">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-199">no</span></span>             | <span data-ttu-id="d0eda-200">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-200">no</span></span>               |
| <span data-ttu-id="d0eda-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="d0eda-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="d0eda-202">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-202">no</span></span>             | <span data-ttu-id="d0eda-203">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-203">no</span></span>               |
| <span data-ttu-id="d0eda-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="d0eda-205">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-205">no</span></span>             | <span data-ttu-id="d0eda-206">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-206">no</span></span>               |
| <span data-ttu-id="d0eda-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="d0eda-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="d0eda-208">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-208">no</span></span>             | <span data-ttu-id="d0eda-209">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-209">no</span></span>               |
| <span data-ttu-id="d0eda-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="d0eda-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="d0eda-211">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-211">no</span></span>             | <span data-ttu-id="d0eda-212">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-212">no</span></span>               |
| <span data-ttu-id="d0eda-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="d0eda-214">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-214">no</span></span>             | <span data-ttu-id="d0eda-215">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-215">no</span></span>               |
| <span data-ttu-id="d0eda-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="d0eda-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="d0eda-217">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-217">no</span></span>             | <span data-ttu-id="d0eda-218">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-218">no</span></span>               |
| <span data-ttu-id="d0eda-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d0eda-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="d0eda-220">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-220">no</span></span>             | <span data-ttu-id="d0eda-221">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-221">no</span></span>               |
| <span data-ttu-id="d0eda-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d0eda-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="d0eda-223">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-223">no</span></span>             | <span data-ttu-id="d0eda-224">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-224">no</span></span>               |
| <span data-ttu-id="d0eda-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="d0eda-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="d0eda-226">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-226">no</span></span>             | <span data-ttu-id="d0eda-227">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-227">no</span></span>               |
| <span data-ttu-id="d0eda-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="d0eda-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="d0eda-229">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-229">no</span></span>             | <span data-ttu-id="d0eda-230">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-230">no</span></span>               |
| <span data-ttu-id="d0eda-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="d0eda-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="d0eda-232">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-232">no</span></span>             | <span data-ttu-id="d0eda-233">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-233">no</span></span>               |
| <span data-ttu-id="d0eda-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="d0eda-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="d0eda-235">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-235">no</span></span>             | <span data-ttu-id="d0eda-236">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-236">no</span></span>               |
| <span data-ttu-id="d0eda-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="d0eda-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="d0eda-238">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-238">no</span></span>             | <span data-ttu-id="d0eda-239">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-239">no</span></span>               |
| <span data-ttu-id="d0eda-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="d0eda-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="d0eda-241">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-241">no</span></span>             | <span data-ttu-id="d0eda-242">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-242">no</span></span>               |
| <span data-ttu-id="d0eda-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="d0eda-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="d0eda-244">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-244">no</span></span>             | <span data-ttu-id="d0eda-245">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-245">no</span></span>               |
| <span data-ttu-id="d0eda-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="d0eda-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="d0eda-247">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-247">no</span></span>             | <span data-ttu-id="d0eda-248">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-248">no</span></span>               |
| <span data-ttu-id="d0eda-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="d0eda-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="d0eda-250">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-250">no</span></span>             | <span data-ttu-id="d0eda-251">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-251">no</span></span>               |
| <span data-ttu-id="d0eda-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="d0eda-253">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-253">no</span></span>             | <span data-ttu-id="d0eda-254">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-254">no</span></span>               |
| <span data-ttu-id="d0eda-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="d0eda-256">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-256">no</span></span>             | <span data-ttu-id="d0eda-257">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-257">no</span></span>               |
| <span data-ttu-id="d0eda-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d0eda-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="d0eda-259">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-259">no</span></span>             | <span data-ttu-id="d0eda-260">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-260">no</span></span>               |
| <span data-ttu-id="d0eda-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="d0eda-262">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-262">no</span></span>             | <span data-ttu-id="d0eda-263">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-263">no</span></span>               |
| <span data-ttu-id="d0eda-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="d0eda-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="d0eda-265">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-265">no</span></span>             | <span data-ttu-id="d0eda-266">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-266">no</span></span>               |
| <span data-ttu-id="d0eda-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="d0eda-267">msdyn_progress</span></span>                         | <span data-ttu-id="d0eda-268">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-268">no</span></span>             | <span data-ttu-id="d0eda-269">no (sí para P4W)</span><span class="sxs-lookup"><span data-stu-id="d0eda-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="d0eda-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="d0eda-271">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-271">no</span></span>             | <span data-ttu-id="d0eda-272">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-272">no</span></span>               |
| <span data-ttu-id="d0eda-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="d0eda-274">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-274">no</span></span>             | <span data-ttu-id="d0eda-275">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-275">no</span></span>               |
| <span data-ttu-id="d0eda-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d0eda-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="d0eda-277">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-277">no</span></span>             | <span data-ttu-id="d0eda-278">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-278">no</span></span>               |
| <span data-ttu-id="d0eda-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="d0eda-280">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-280">no</span></span>             | <span data-ttu-id="d0eda-281">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-281">no</span></span>               |
| <span data-ttu-id="d0eda-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="d0eda-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="d0eda-283">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-283">no</span></span>             | <span data-ttu-id="d0eda-284">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-284">no</span></span>               |
| <span data-ttu-id="d0eda-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d0eda-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="d0eda-286">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-286">no</span></span>             | <span data-ttu-id="d0eda-287">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-287">no</span></span>               |
| <span data-ttu-id="d0eda-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="d0eda-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="d0eda-289">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-289">no</span></span>             | <span data-ttu-id="d0eda-290">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-290">no</span></span>               |
| <span data-ttu-id="d0eda-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="d0eda-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="d0eda-292">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-292">no</span></span>             | <span data-ttu-id="d0eda-293">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-293">no</span></span>               |
| <span data-ttu-id="d0eda-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="d0eda-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="d0eda-295">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-295">no</span></span>             | <span data-ttu-id="d0eda-296">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-296">no</span></span>               |
| <span data-ttu-id="d0eda-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="d0eda-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="d0eda-298">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-298">no</span></span>             | <span data-ttu-id="d0eda-299">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-299">no</span></span>               |
| <span data-ttu-id="d0eda-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d0eda-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="d0eda-301">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-301">no</span></span>             | <span data-ttu-id="d0eda-302">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-302">no</span></span>               |
| <span data-ttu-id="d0eda-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="d0eda-304">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-304">no</span></span>             | <span data-ttu-id="d0eda-305">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-305">no</span></span>               |
| <span data-ttu-id="d0eda-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="d0eda-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="d0eda-307">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-307">no</span></span>             | <span data-ttu-id="d0eda-308">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-308">no</span></span>               |
| <span data-ttu-id="d0eda-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="d0eda-310">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-310">no</span></span>             | <span data-ttu-id="d0eda-311">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-311">no</span></span>               |
| <span data-ttu-id="d0eda-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="d0eda-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="d0eda-313">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-313">no</span></span>             | <span data-ttu-id="d0eda-314">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-314">no</span></span>               |
| <span data-ttu-id="d0eda-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="d0eda-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="d0eda-316">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-316">no</span></span>             | <span data-ttu-id="d0eda-317">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-317">no</span></span>               |
| <span data-ttu-id="d0eda-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="d0eda-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="d0eda-319">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-319">no</span></span>             | <span data-ttu-id="d0eda-320">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-320">no</span></span>               |
| <span data-ttu-id="d0eda-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="d0eda-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="d0eda-322">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-322">no</span></span>             | <span data-ttu-id="d0eda-323">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-323">no</span></span>               |
| <span data-ttu-id="d0eda-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="d0eda-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="d0eda-325">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-325">no</span></span>             | <span data-ttu-id="d0eda-326">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-326">no</span></span>               |
| <span data-ttu-id="d0eda-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="d0eda-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="d0eda-328">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-328">no</span></span>             | <span data-ttu-id="d0eda-329">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-329">no</span></span>               |
| <span data-ttu-id="d0eda-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="d0eda-330">msdyn_summary</span></span>                          | <span data-ttu-id="d0eda-331">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-331">no</span></span>             | <span data-ttu-id="d0eda-332">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-332">no</span></span>               |
| <span data-ttu-id="d0eda-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="d0eda-334">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-334">no</span></span>             | <span data-ttu-id="d0eda-335">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-335">no</span></span>               |
| <span data-ttu-id="d0eda-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="d0eda-337">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-337">no</span></span>             | <span data-ttu-id="d0eda-338">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="d0eda-339">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-339">Project task dependency</span></span>

| <span data-ttu-id="d0eda-340">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="d0eda-340">**Logical name**</span></span>              | <span data-ttu-id="d0eda-341">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="d0eda-341">**Can create**</span></span> | <span data-ttu-id="d0eda-342">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="d0eda-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="d0eda-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="d0eda-343">msdyn_linktype</span></span>                | <span data-ttu-id="d0eda-344">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-344">no</span></span>             | <span data-ttu-id="d0eda-345">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-345">no</span></span>           |
| <span data-ttu-id="d0eda-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="d0eda-346">msdyn_linktypename</span></span>            | <span data-ttu-id="d0eda-347">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-347">no</span></span>             | <span data-ttu-id="d0eda-348">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-348">no</span></span>           |
| <span data-ttu-id="d0eda-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="d0eda-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="d0eda-350">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-350">yes</span></span>            | <span data-ttu-id="d0eda-351">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-351">no</span></span>           |
| <span data-ttu-id="d0eda-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="d0eda-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="d0eda-353">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-353">yes</span></span>            | <span data-ttu-id="d0eda-354">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-354">no</span></span>           |
| <span data-ttu-id="d0eda-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="d0eda-355">msdyn_project</span></span>                 | <span data-ttu-id="d0eda-356">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-356">yes</span></span>            | <span data-ttu-id="d0eda-357">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-357">no</span></span>           |
| <span data-ttu-id="d0eda-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="d0eda-358">msdyn_projectname</span></span>             | <span data-ttu-id="d0eda-359">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-359">yes</span></span>            | <span data-ttu-id="d0eda-360">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-360">no</span></span>           |
| <span data-ttu-id="d0eda-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="d0eda-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="d0eda-362">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-362">yes</span></span>            | <span data-ttu-id="d0eda-363">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-363">no</span></span>           |
| <span data-ttu-id="d0eda-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="d0eda-364">msdyn_successortask</span></span>           | <span data-ttu-id="d0eda-365">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-365">yes</span></span>            | <span data-ttu-id="d0eda-366">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-366">no</span></span>           |
| <span data-ttu-id="d0eda-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="d0eda-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="d0eda-368">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-368">yes</span></span>            | <span data-ttu-id="d0eda-369">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="d0eda-370">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="d0eda-370">Resource assignment</span></span>

| <span data-ttu-id="d0eda-371">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="d0eda-371">**Logical name**</span></span>             | <span data-ttu-id="d0eda-372">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="d0eda-372">**Can create**</span></span> | <span data-ttu-id="d0eda-373">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="d0eda-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="d0eda-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="d0eda-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="d0eda-375">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-375">yes</span></span>            | <span data-ttu-id="d0eda-376">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-376">no</span></span>           |
| <span data-ttu-id="d0eda-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="d0eda-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="d0eda-378">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-378">yes</span></span>            | <span data-ttu-id="d0eda-379">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-379">no</span></span>           |
| <span data-ttu-id="d0eda-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="d0eda-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="d0eda-381">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-381">no</span></span>             | <span data-ttu-id="d0eda-382">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-382">no</span></span>           |
| <span data-ttu-id="d0eda-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="d0eda-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="d0eda-384">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-384">no</span></span>             | <span data-ttu-id="d0eda-385">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-385">no</span></span>           |
| <span data-ttu-id="d0eda-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="d0eda-386">msdyn_committype</span></span>             | <span data-ttu-id="d0eda-387">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-387">no</span></span>             | <span data-ttu-id="d0eda-388">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-388">no</span></span>           |
| <span data-ttu-id="d0eda-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="d0eda-389">msdyn_committypename</span></span>         | <span data-ttu-id="d0eda-390">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-390">no</span></span>             | <span data-ttu-id="d0eda-391">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-391">no</span></span>           |
| <span data-ttu-id="d0eda-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d0eda-392">msdyn_effort</span></span>                 | <span data-ttu-id="d0eda-393">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-393">no</span></span>             | <span data-ttu-id="d0eda-394">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-394">no</span></span>           |
| <span data-ttu-id="d0eda-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d0eda-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="d0eda-396">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-396">no</span></span>             | <span data-ttu-id="d0eda-397">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-397">no</span></span>           |
| <span data-ttu-id="d0eda-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d0eda-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="d0eda-399">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-399">no</span></span>             | <span data-ttu-id="d0eda-400">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-400">no</span></span>           |
| <span data-ttu-id="d0eda-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d0eda-401">msdyn_finish</span></span>                 | <span data-ttu-id="d0eda-402">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-402">no</span></span>             | <span data-ttu-id="d0eda-403">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-403">no</span></span>           |
| <span data-ttu-id="d0eda-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="d0eda-405">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-405">no</span></span>             | <span data-ttu-id="d0eda-406">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-406">no</span></span>           |
| <span data-ttu-id="d0eda-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="d0eda-408">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-408">no</span></span>             | <span data-ttu-id="d0eda-409">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-409">no</span></span>           |
| <span data-ttu-id="d0eda-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="d0eda-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="d0eda-411">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-411">no</span></span>             | <span data-ttu-id="d0eda-412">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-412">no</span></span>           |
| <span data-ttu-id="d0eda-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d0eda-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="d0eda-414">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-414">no</span></span>             | <span data-ttu-id="d0eda-415">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-415">no</span></span>           |
| <span data-ttu-id="d0eda-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="d0eda-417">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-417">no</span></span>             | <span data-ttu-id="d0eda-418">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-418">no</span></span>           |
| <span data-ttu-id="d0eda-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="d0eda-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="d0eda-420">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-420">no</span></span>             | <span data-ttu-id="d0eda-421">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-421">no</span></span>           |
| <span data-ttu-id="d0eda-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="d0eda-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="d0eda-423">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-423">no</span></span>             | <span data-ttu-id="d0eda-424">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-424">no</span></span>           |
| <span data-ttu-id="d0eda-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="d0eda-425">msdyn_projectid</span></span>              | <span data-ttu-id="d0eda-426">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-426">yes</span></span>            | <span data-ttu-id="d0eda-427">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-427">no</span></span>           |
| <span data-ttu-id="d0eda-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="d0eda-428">msdyn_projectidname</span></span>          | <span data-ttu-id="d0eda-429">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-429">no</span></span>             | <span data-ttu-id="d0eda-430">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-430">no</span></span>           |
| <span data-ttu-id="d0eda-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="d0eda-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="d0eda-432">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-432">no</span></span>             | <span data-ttu-id="d0eda-433">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-433">no</span></span>           |
| <span data-ttu-id="d0eda-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="d0eda-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="d0eda-435">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-435">no</span></span>             | <span data-ttu-id="d0eda-436">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-436">no</span></span>           |
| <span data-ttu-id="d0eda-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="d0eda-437">msdyn_start</span></span>                  | <span data-ttu-id="d0eda-438">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-438">no</span></span>             | <span data-ttu-id="d0eda-439">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-439">no</span></span>           |
| <span data-ttu-id="d0eda-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="d0eda-440">msdyn_taskid</span></span>                 | <span data-ttu-id="d0eda-441">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-441">no</span></span>             | <span data-ttu-id="d0eda-442">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-442">no</span></span>           |
| <span data-ttu-id="d0eda-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="d0eda-443">msdyn_taskidname</span></span>             | <span data-ttu-id="d0eda-444">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-444">no</span></span>             | <span data-ttu-id="d0eda-445">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-445">no</span></span>           |
| <span data-ttu-id="d0eda-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="d0eda-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="d0eda-447">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-447">no</span></span>             | <span data-ttu-id="d0eda-448">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="d0eda-449">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="d0eda-449">Project team member</span></span>

| <span data-ttu-id="d0eda-450">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="d0eda-450">**Logical name**</span></span>                                 | <span data-ttu-id="d0eda-451">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="d0eda-451">**Can create**</span></span> | <span data-ttu-id="d0eda-452">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="d0eda-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="d0eda-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="d0eda-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="d0eda-454">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-454">no</span></span>             | <span data-ttu-id="d0eda-455">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-455">no</span></span>           |
| <span data-ttu-id="d0eda-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="d0eda-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="d0eda-457">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-457">no</span></span>             | <span data-ttu-id="d0eda-458">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-458">no</span></span>           |
| <span data-ttu-id="d0eda-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="d0eda-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="d0eda-460">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-460">no</span></span>             | <span data-ttu-id="d0eda-461">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-461">no</span></span>           |
| <span data-ttu-id="d0eda-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="d0eda-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="d0eda-463">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-463">no</span></span>             | <span data-ttu-id="d0eda-464">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-464">no</span></span>           |
| <span data-ttu-id="d0eda-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d0eda-465">msdyn_effort</span></span>                                     | <span data-ttu-id="d0eda-466">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-466">no</span></span>             | <span data-ttu-id="d0eda-467">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-467">no</span></span>           |
| <span data-ttu-id="d0eda-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d0eda-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="d0eda-469">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-469">no</span></span>             | <span data-ttu-id="d0eda-470">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-470">no</span></span>           |
| <span data-ttu-id="d0eda-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d0eda-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="d0eda-472">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-472">no</span></span>             | <span data-ttu-id="d0eda-473">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-473">no</span></span>           |
| <span data-ttu-id="d0eda-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d0eda-474">msdyn_finish</span></span>                                     | <span data-ttu-id="d0eda-475">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-475">no</span></span>             | <span data-ttu-id="d0eda-476">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-476">no</span></span>           |
| <span data-ttu-id="d0eda-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="d0eda-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="d0eda-478">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-478">no</span></span>             | <span data-ttu-id="d0eda-479">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-479">no</span></span>           |
| <span data-ttu-id="d0eda-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="d0eda-480">msdyn_hours</span></span>                                      | <span data-ttu-id="d0eda-481">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-481">no</span></span>             | <span data-ttu-id="d0eda-482">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-482">no</span></span>           |
| <span data-ttu-id="d0eda-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="d0eda-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="d0eda-484">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-484">no</span></span>             | <span data-ttu-id="d0eda-485">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-485">no</span></span>           |
| <span data-ttu-id="d0eda-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="d0eda-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="d0eda-487">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-487">no</span></span>             | <span data-ttu-id="d0eda-488">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-488">no</span></span>           |
| <span data-ttu-id="d0eda-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="d0eda-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="d0eda-490">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-490">no</span></span>             | <span data-ttu-id="d0eda-491">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-491">no</span></span>           |
| <span data-ttu-id="d0eda-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="d0eda-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="d0eda-493">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-493">no</span></span>             | <span data-ttu-id="d0eda-494">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-494">no</span></span>           |
| <span data-ttu-id="d0eda-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="d0eda-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="d0eda-496">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-496">no</span></span>             | <span data-ttu-id="d0eda-497">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-497">no</span></span>           |
| <span data-ttu-id="d0eda-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="d0eda-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="d0eda-499">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-499">no</span></span>             | <span data-ttu-id="d0eda-500">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-500">no</span></span>           |
| <span data-ttu-id="d0eda-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="d0eda-501">msdyn_start</span></span>                                      | <span data-ttu-id="d0eda-502">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-502">no</span></span>             | <span data-ttu-id="d0eda-503">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="d0eda-504">Project</span><span class="sxs-lookup"><span data-stu-id="d0eda-504">Project</span></span>

| <span data-ttu-id="d0eda-505">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="d0eda-505">**Logical name**</span></span>                       | <span data-ttu-id="d0eda-506">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="d0eda-506">**Can create**</span></span> | <span data-ttu-id="d0eda-507">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="d0eda-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="d0eda-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="d0eda-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="d0eda-509">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-509">no</span></span>             | <span data-ttu-id="d0eda-510">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-510">no</span></span>           |
| <span data-ttu-id="d0eda-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="d0eda-512">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-512">no</span></span>             | <span data-ttu-id="d0eda-513">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-513">no</span></span>           |
| <span data-ttu-id="d0eda-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="d0eda-515">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-515">no</span></span>             | <span data-ttu-id="d0eda-516">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-516">no</span></span>           |
| <span data-ttu-id="d0eda-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="d0eda-518">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-518">no</span></span>             | <span data-ttu-id="d0eda-519">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-519">no</span></span>           |
| <span data-ttu-id="d0eda-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="d0eda-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="d0eda-521">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-521">no</span></span>             | <span data-ttu-id="d0eda-522">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-522">no</span></span>           |
| <span data-ttu-id="d0eda-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="d0eda-524">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-524">no</span></span>             | <span data-ttu-id="d0eda-525">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-525">no</span></span>           |
| <span data-ttu-id="d0eda-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="d0eda-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="d0eda-527">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-527">yes</span></span>            | <span data-ttu-id="d0eda-528">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-528">no</span></span>           |
| <span data-ttu-id="d0eda-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="d0eda-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="d0eda-530">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-530">yes</span></span>            | <span data-ttu-id="d0eda-531">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-531">no</span></span>           |
| <span data-ttu-id="d0eda-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="d0eda-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="d0eda-533">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-533">yes</span></span>            | <span data-ttu-id="d0eda-534">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-534">no</span></span>           |
| <span data-ttu-id="d0eda-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="d0eda-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="d0eda-536">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-536">no</span></span>             | <span data-ttu-id="d0eda-537">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-537">no</span></span>           |
| <span data-ttu-id="d0eda-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d0eda-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="d0eda-539">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-539">no</span></span>             | <span data-ttu-id="d0eda-540">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-540">no</span></span>           |
| <span data-ttu-id="d0eda-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="d0eda-542">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-542">no</span></span>             | <span data-ttu-id="d0eda-543">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-543">no</span></span>           |
| <span data-ttu-id="d0eda-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="d0eda-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="d0eda-545">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-545">no</span></span>             | <span data-ttu-id="d0eda-546">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-546">no</span></span>           |
| <span data-ttu-id="d0eda-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="d0eda-548">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-548">no</span></span>             | <span data-ttu-id="d0eda-549">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-549">no</span></span>           |
| <span data-ttu-id="d0eda-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="d0eda-550">msdyn_duration</span></span>                         | <span data-ttu-id="d0eda-551">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-551">no</span></span>             | <span data-ttu-id="d0eda-552">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-552">no</span></span>           |
| <span data-ttu-id="d0eda-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d0eda-553">msdyn_effort</span></span>                           | <span data-ttu-id="d0eda-554">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-554">no</span></span>             | <span data-ttu-id="d0eda-555">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-555">no</span></span>           |
| <span data-ttu-id="d0eda-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d0eda-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="d0eda-557">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-557">no</span></span>             | <span data-ttu-id="d0eda-558">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-558">no</span></span>           |
| <span data-ttu-id="d0eda-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="d0eda-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="d0eda-560">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-560">no</span></span>             | <span data-ttu-id="d0eda-561">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-561">no</span></span>           |
| <span data-ttu-id="d0eda-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d0eda-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="d0eda-563">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-563">no</span></span>             | <span data-ttu-id="d0eda-564">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-564">no</span></span>           |
| <span data-ttu-id="d0eda-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d0eda-565">msdyn_finish</span></span>                           | <span data-ttu-id="d0eda-566">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-566">yes</span></span>            | <span data-ttu-id="d0eda-567">sí</span><span class="sxs-lookup"><span data-stu-id="d0eda-567">yes</span></span>          |
| <span data-ttu-id="d0eda-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="d0eda-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="d0eda-569">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-569">no</span></span>             | <span data-ttu-id="d0eda-570">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-570">no</span></span>           |
| <span data-ttu-id="d0eda-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="d0eda-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="d0eda-572">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-572">no</span></span>             | <span data-ttu-id="d0eda-573">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-573">no</span></span>           |
| <span data-ttu-id="d0eda-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="d0eda-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="d0eda-575">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-575">no</span></span>             | <span data-ttu-id="d0eda-576">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-576">no</span></span>           |
| <span data-ttu-id="d0eda-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="d0eda-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="d0eda-578">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-578">no</span></span>             | <span data-ttu-id="d0eda-579">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-579">no</span></span>           |
| <span data-ttu-id="d0eda-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="d0eda-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="d0eda-581">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-581">no</span></span>             | <span data-ttu-id="d0eda-582">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-582">no</span></span>           |
| <span data-ttu-id="d0eda-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="d0eda-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="d0eda-584">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-584">no</span></span>             | <span data-ttu-id="d0eda-585">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-585">no</span></span>           |
| <span data-ttu-id="d0eda-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="d0eda-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="d0eda-587">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-587">no</span></span>             | <span data-ttu-id="d0eda-588">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-588">no</span></span>           |
| <span data-ttu-id="d0eda-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="d0eda-590">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-590">no</span></span>             | <span data-ttu-id="d0eda-591">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-591">no</span></span>           |
| <span data-ttu-id="d0eda-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="d0eda-593">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-593">no</span></span>             | <span data-ttu-id="d0eda-594">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-594">no</span></span>           |
| <span data-ttu-id="d0eda-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="d0eda-596">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-596">no</span></span>             | <span data-ttu-id="d0eda-597">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-597">no</span></span>           |
| <span data-ttu-id="d0eda-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d0eda-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="d0eda-599">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-599">no</span></span>             | <span data-ttu-id="d0eda-600">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-600">no</span></span>           |
| <span data-ttu-id="d0eda-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="d0eda-602">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-602">no</span></span>             | <span data-ttu-id="d0eda-603">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-603">no</span></span>           |
| <span data-ttu-id="d0eda-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="d0eda-604">msdyn_progress</span></span>                         | <span data-ttu-id="d0eda-605">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-605">no</span></span>             | <span data-ttu-id="d0eda-606">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-606">no</span></span>           |
| <span data-ttu-id="d0eda-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="d0eda-608">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-608">no</span></span>             | <span data-ttu-id="d0eda-609">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-609">no</span></span>           |
| <span data-ttu-id="d0eda-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="d0eda-611">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-611">no</span></span>             | <span data-ttu-id="d0eda-612">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-612">no</span></span>           |
| <span data-ttu-id="d0eda-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d0eda-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="d0eda-614">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-614">no</span></span>             | <span data-ttu-id="d0eda-615">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-615">no</span></span>           |
| <span data-ttu-id="d0eda-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="d0eda-617">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-617">no</span></span>             | <span data-ttu-id="d0eda-618">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-618">no</span></span>           |
| <span data-ttu-id="d0eda-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="d0eda-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="d0eda-620">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-620">no</span></span>             | <span data-ttu-id="d0eda-621">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-621">no</span></span>           |
| <span data-ttu-id="d0eda-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="d0eda-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="d0eda-623">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-623">no</span></span>             | <span data-ttu-id="d0eda-624">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-624">no</span></span>           |
| <span data-ttu-id="d0eda-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="d0eda-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="d0eda-626">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-626">no</span></span>             | <span data-ttu-id="d0eda-627">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-627">no</span></span>           |
| <span data-ttu-id="d0eda-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="d0eda-629">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-629">no</span></span>             | <span data-ttu-id="d0eda-630">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-630">no</span></span>           |
| <span data-ttu-id="d0eda-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="d0eda-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="d0eda-632">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-632">no</span></span>             | <span data-ttu-id="d0eda-633">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-633">no</span></span>           |
| <span data-ttu-id="d0eda-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="d0eda-635">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-635">no</span></span>             | <span data-ttu-id="d0eda-636">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-636">no</span></span>           |
| <span data-ttu-id="d0eda-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="d0eda-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="d0eda-638">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-638">no</span></span>             | <span data-ttu-id="d0eda-639">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-639">no</span></span>           |
| <span data-ttu-id="d0eda-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="d0eda-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="d0eda-641">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-641">no</span></span>             | <span data-ttu-id="d0eda-642">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-642">no</span></span>           |
| <span data-ttu-id="d0eda-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="d0eda-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="d0eda-644">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-644">no</span></span>             | <span data-ttu-id="d0eda-645">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-645">no</span></span>           |
| <span data-ttu-id="d0eda-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="d0eda-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="d0eda-647">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-647">no</span></span>             | <span data-ttu-id="d0eda-648">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-648">no</span></span>           |
| <span data-ttu-id="d0eda-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="d0eda-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="d0eda-650">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-650">no</span></span>             | <span data-ttu-id="d0eda-651">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-651">no</span></span>           |
| <span data-ttu-id="d0eda-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="d0eda-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="d0eda-653">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-653">no</span></span>             | <span data-ttu-id="d0eda-654">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-654">no</span></span>           |
| <span data-ttu-id="d0eda-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="d0eda-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="d0eda-656">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-656">no</span></span>             | <span data-ttu-id="d0eda-657">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-657">no</span></span>           |
| <span data-ttu-id="d0eda-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="d0eda-659">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-659">no</span></span>             | <span data-ttu-id="d0eda-660">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-660">no</span></span>           |
| <span data-ttu-id="d0eda-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="d0eda-662">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-662">no</span></span>             | <span data-ttu-id="d0eda-663">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-663">no</span></span>           |
| <span data-ttu-id="d0eda-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="d0eda-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="d0eda-665">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-665">no</span></span>             | <span data-ttu-id="d0eda-666">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-666">no</span></span>           |
| <span data-ttu-id="d0eda-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d0eda-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="d0eda-668">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-668">no</span></span>             | <span data-ttu-id="d0eda-669">no</span><span class="sxs-lookup"><span data-stu-id="d0eda-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="d0eda-670">Limitaciones y problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="d0eda-670">Limitations and known issues</span></span>
<span data-ttu-id="d0eda-671">La siguiente es una lista de limitaciones y problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="d0eda-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="d0eda-672">Las API de programación solo pueden ser utilizadas por los **Usuarios con licencia de Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="d0eda-673">No pueden ser utilizadas por:</span><span class="sxs-lookup"><span data-stu-id="d0eda-673">They can't be used by:</span></span>
    - <span data-ttu-id="d0eda-674">Usuarios de la aplicación</span><span class="sxs-lookup"><span data-stu-id="d0eda-674">Application users</span></span>
    - <span data-ttu-id="d0eda-675">Usuarios de sistema</span><span class="sxs-lookup"><span data-stu-id="d0eda-675">System users</span></span>
    - <span data-ttu-id="d0eda-676">Usuarios de integración</span><span class="sxs-lookup"><span data-stu-id="d0eda-676">Integration users</span></span>
    - <span data-ttu-id="d0eda-677">Otros usuarios que no tienen la licencia requerida</span><span class="sxs-lookup"><span data-stu-id="d0eda-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="d0eda-678">Cada **OperationSet** solo puede tener un máximo de 100 operaciones.</span><span class="sxs-lookup"><span data-stu-id="d0eda-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="d0eda-679">Cada usuario solo puede tener un máximo de 10 operaciones **OperationSet** abiertas.</span><span class="sxs-lookup"><span data-stu-id="d0eda-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="d0eda-680">Project Operations actualmente admiten un máximo de 500 tareas en total en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="d0eda-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="d0eda-681">El estado de error y los registros de error de **OperationSet** no están disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="d0eda-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="d0eda-682">Las API de programación se ofrecen en versión preliminar pública.</span><span class="sxs-lookup"><span data-stu-id="d0eda-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="d0eda-683">Microsoft no admite el uso de estas API en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="d0eda-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="d0eda-684">Límites y límites en proyectos y tareas</span><span class="sxs-lookup"><span data-stu-id="d0eda-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="d0eda-685">Control de errores</span><span class="sxs-lookup"><span data-stu-id="d0eda-685">Error handling</span></span>

   - <span data-ttu-id="d0eda-686">Para revisar los errores generados por los conjuntos de operaciones, vaya a **Configuración** \> **Integración de programación** \> **Conjuntos de operaciones**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="d0eda-687">Para revisar los errores generados por el servicio de programación de proyectos, vaya a **Configuración** \> **Integración de programación** \> **Registros de errores de PSS**.</span><span class="sxs-lookup"><span data-stu-id="d0eda-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="d0eda-688">Escenario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0eda-688">Sample scenario</span></span>

<span data-ttu-id="d0eda-689">En este escenario, creará un proyecto, un miembro del equipo, cuatro tareas y dos asignaciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0eda-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="d0eda-690">A continuación, actualizará una tarea, actualizará el proyecto, eliminará una tarea, eliminará una asignación de recursos y creará una dependencia de tareas.</span><span class="sxs-lookup"><span data-stu-id="d0eda-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="d0eda-691">Ejemplos adicionales</span><span class="sxs-lookup"><span data-stu-id="d0eda-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
