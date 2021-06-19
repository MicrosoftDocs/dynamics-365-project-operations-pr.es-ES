---
title: Utilizar las API de programación para realizar operaciones con entidades de programación
description: Este tema proporciona información y ejemplos para usar las API de programación.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116818"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="1a00c-103">Utilizar las API de programación para realizar operaciones con entidades de programación</span><span class="sxs-lookup"><span data-stu-id="1a00c-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="1a00c-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="1a00c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="1a00c-105">Parte o toda la funcionalidad que se menciona en este tema está disponible como parte de una versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="1a00c-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="1a00c-106">El contenido y la funcionalidad están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="1a00c-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="1a00c-107">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="1a00c-107">Scheduling entities</span></span>

<span data-ttu-id="1a00c-108">Las API de programación brindan la capacidad de realizar operaciones de creación, actualización y eliminación con **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="1a00c-109">Estas entidades se administran a través del motor de programación en Project para la web.</span><span class="sxs-lookup"><span data-stu-id="1a00c-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="1a00c-110">Crear, actualizar y eliminar operaciones con **Entidades de programación** estaba restringido en versiones anteriores de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1a00c-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="1a00c-111">La siguiente tabla proporciona una lista completa de las **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="1a00c-112">Nombre de entidad</span><span class="sxs-lookup"><span data-stu-id="1a00c-112">Entity name</span></span>  | <span data-ttu-id="1a00c-113">Nombre lógico de la entidad</span><span class="sxs-lookup"><span data-stu-id="1a00c-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="1a00c-114">Project</span><span class="sxs-lookup"><span data-stu-id="1a00c-114">Project</span></span> | <span data-ttu-id="1a00c-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="1a00c-115">msdyn_project</span></span> |
| <span data-ttu-id="1a00c-116">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-116">Project Task</span></span>  | <span data-ttu-id="1a00c-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="1a00c-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="1a00c-118">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-118">Project Task Dependency</span></span>  | <span data-ttu-id="1a00c-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="1a00c-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="1a00c-120">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="1a00c-120">Resource Assignment</span></span> | <span data-ttu-id="1a00c-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="1a00c-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="1a00c-122">Cubo de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-122">Project Bucket</span></span>  | <span data-ttu-id="1a00c-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="1a00c-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="1a00c-124">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-124">Project Team Member</span></span> | <span data-ttu-id="1a00c-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="1a00c-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="1a00c-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="1a00c-126">OperationSet</span></span>

<span data-ttu-id="1a00c-127">OperationSet es un patrón de unidad de trabajo que se puede usar cuando se deben procesar varias solicitudes que afectan la programación dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="1a00c-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="1a00c-128">Programar las API</span><span class="sxs-lookup"><span data-stu-id="1a00c-128">Schedule APIs</span></span>

<span data-ttu-id="1a00c-129">La siguiente es una lista de las API de programación actuales.</span><span class="sxs-lookup"><span data-stu-id="1a00c-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="1a00c-130">**msdyn_CreateProjectV1**: esta API se puede utilizar para crear un proyecto.</span><span class="sxs-lookup"><span data-stu-id="1a00c-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="1a00c-131">El proyecto y el cubo del proyecto predeterminado se crean inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="1a00c-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="1a00c-132">**msdyn_CreateTeamMemberV1**: esta API se puede utilizar para crear un miembro de equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1a00c-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="1a00c-133">El registro de miembro del equipo se crea inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="1a00c-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="1a00c-134">**msdyn_CreateOperationSetV1**: esta API se puede utilizar para programar varias solicitudes que deben realizarse dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="1a00c-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="1a00c-135">**msdyn_PSSCreateV1**: esta API se puede utilizar para crear una entidad.</span><span class="sxs-lookup"><span data-stu-id="1a00c-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="1a00c-136">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de creación.</span><span class="sxs-lookup"><span data-stu-id="1a00c-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="1a00c-137">**msdyn_PSSUpdateV1**: esta API se puede utilizar para actualizar una entidad.</span><span class="sxs-lookup"><span data-stu-id="1a00c-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="1a00c-138">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="1a00c-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="1a00c-139">**msdyn_PSSDeleteV1**: esta API se puede utilizar para eliminar una entidad.</span><span class="sxs-lookup"><span data-stu-id="1a00c-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="1a00c-140">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="1a00c-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="1a00c-141">**msdyn_ExecuteOperationSetV1**: esta API se utiliza para ejecutar todas las operaciones dentro del conjunto de operaciones establecido.</span><span class="sxs-lookup"><span data-stu-id="1a00c-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="1a00c-142">Utilizar las API de programación con OperationSet</span><span class="sxs-lookup"><span data-stu-id="1a00c-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="1a00c-143">Porque los registros con ambos **CreateProjectV1** y **CreateTeamMemberV1** se crean inmediatamente, estas API no se pueden utilizar en **OperationSet** directamente.</span><span class="sxs-lookup"><span data-stu-id="1a00c-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="1a00c-144">Sin embargo, puede utilizar la API para crear los registros necesarios, crear un **OperationSet** y, a continuación, utilizar estos registros creados previamente en **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="1a00c-145">Operaciones admitidas</span><span class="sxs-lookup"><span data-stu-id="1a00c-145">Supported operations</span></span>

| <span data-ttu-id="1a00c-146">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="1a00c-146">Scheduling entity</span></span> | <span data-ttu-id="1a00c-147">Crear</span><span class="sxs-lookup"><span data-stu-id="1a00c-147">Create</span></span> | <span data-ttu-id="1a00c-148">Actualización</span><span class="sxs-lookup"><span data-stu-id="1a00c-148">Update</span></span> | <span data-ttu-id="1a00c-149">Delete</span><span class="sxs-lookup"><span data-stu-id="1a00c-149">Delete</span></span> | <span data-ttu-id="1a00c-150">Consideraciones importantes</span><span class="sxs-lookup"><span data-stu-id="1a00c-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="1a00c-151">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-151">Project task</span></span> | <span data-ttu-id="1a00c-152">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-152">Yes</span></span> | <span data-ttu-id="1a00c-153">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-153">Yes</span></span> | <span data-ttu-id="1a00c-154">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-154">Yes</span></span> | <span data-ttu-id="1a00c-155">Nada</span><span class="sxs-lookup"><span data-stu-id="1a00c-155">None</span></span> |
| <span data-ttu-id="1a00c-156">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-156">Project task dependency</span></span> | <span data-ttu-id="1a00c-157">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-157">Yes</span></span> | <span data-ttu-id="1a00c-158">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-158">Yes</span></span> | | <span data-ttu-id="1a00c-159">Los registros de dependencia de tareas del proyecto no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="1a00c-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="1a00c-160">En su lugar, se puede eliminar un registro antiguo y se puede crear un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="1a00c-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="1a00c-161">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="1a00c-161">Resource assignment</span></span> | <span data-ttu-id="1a00c-162">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-162">Yes</span></span> | <span data-ttu-id="1a00c-163">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-163">Yes</span></span> | | <span data-ttu-id="1a00c-164">No se admiten las operaciones con los siguientes campos: **BookableResourceID**, **Esfuerzo**, **EffortCompleted**, **EffortCompleted** y **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="1a00c-165">Los registros de asignación de recursos no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="1a00c-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="1a00c-166">En su lugar, se puede eliminar el registro antiguo y se puede crear un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="1a00c-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="1a00c-167">Cubo de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-167">Project bucket</span></span> | <span data-ttu-id="1a00c-168">N/D</span><span class="sxs-lookup"><span data-stu-id="1a00c-168">N/A</span></span> | <span data-ttu-id="1a00c-169">N/D</span><span class="sxs-lookup"><span data-stu-id="1a00c-169">N/A</span></span> | <span data-ttu-id="1a00c-170">N/D</span><span class="sxs-lookup"><span data-stu-id="1a00c-170">N/A</span></span> | <span data-ttu-id="1a00c-171">El cubo predeterminado se crea utilizando la API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="1a00c-172">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-172">Project team member</span></span> | <span data-ttu-id="1a00c-173">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-173">Yes</span></span> | <span data-ttu-id="1a00c-174">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-174">Yes</span></span> | <span data-ttu-id="1a00c-175">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-175">Yes</span></span> | <span data-ttu-id="1a00c-176">Para la operación de creación, use la API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="1a00c-177">Project</span><span class="sxs-lookup"><span data-stu-id="1a00c-177">Project</span></span> | <span data-ttu-id="1a00c-178">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-178">Yes</span></span> | <span data-ttu-id="1a00c-179">Sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-179">Yes</span></span> | <span data-ttu-id="1a00c-180">N/D</span><span class="sxs-lookup"><span data-stu-id="1a00c-180">N/A</span></span> | <span data-ttu-id="1a00c-181">No se admiten operaciones con los siguientes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esfuerzo**, **EffortCompleted**, **EffortRemaining**, **Progreso**, **Terminar**, **TaskEarliestStart**, y **Duración**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="1a00c-182">Estas API se pueden llamar con objetos de entidad que incluyen campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="1a00c-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="1a00c-183">La propiedad del identificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="1a00c-183">The ID property is optional.</span></span> <span data-ttu-id="1a00c-184">Si se proporciona, el sistema intenta usarlo y lanza una excepción si no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="1a00c-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="1a00c-185">Si no se proporciona, el sistema lo generará.</span><span class="sxs-lookup"><span data-stu-id="1a00c-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="1a00c-186">Campos restringidos</span><span class="sxs-lookup"><span data-stu-id="1a00c-186">Restricted fields</span></span>

<span data-ttu-id="1a00c-187">Las siguientes tablas definen los campos que están restringidos para **Crear** y **Editar.**</span><span class="sxs-lookup"><span data-stu-id="1a00c-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="1a00c-188">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-188">Project task</span></span>

| <span data-ttu-id="1a00c-189">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="1a00c-189">**Logical name**</span></span>                       | <span data-ttu-id="1a00c-190">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="1a00c-190">**Can create**</span></span> | <span data-ttu-id="1a00c-191">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="1a00c-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="1a00c-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="1a00c-193">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-193">no</span></span>             | <span data-ttu-id="1a00c-194">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-194">no</span></span>               |
| <span data-ttu-id="1a00c-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="1a00c-196">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-196">no</span></span>             | <span data-ttu-id="1a00c-197">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-197">no</span></span>               |
| <span data-ttu-id="1a00c-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="1a00c-198">msdyn_actualend</span></span>                        | <span data-ttu-id="1a00c-199">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-199">no</span></span>             | <span data-ttu-id="1a00c-200">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-200">no</span></span>               |
| <span data-ttu-id="1a00c-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="1a00c-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="1a00c-202">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-202">no</span></span>             | <span data-ttu-id="1a00c-203">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-203">no</span></span>               |
| <span data-ttu-id="1a00c-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="1a00c-205">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-205">no</span></span>             | <span data-ttu-id="1a00c-206">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-206">no</span></span>               |
| <span data-ttu-id="1a00c-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="1a00c-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="1a00c-208">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-208">no</span></span>             | <span data-ttu-id="1a00c-209">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-209">no</span></span>               |
| <span data-ttu-id="1a00c-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="1a00c-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="1a00c-211">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-211">no</span></span>             | <span data-ttu-id="1a00c-212">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-212">no</span></span>               |
| <span data-ttu-id="1a00c-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="1a00c-214">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-214">no</span></span>             | <span data-ttu-id="1a00c-215">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-215">no</span></span>               |
| <span data-ttu-id="1a00c-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="1a00c-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="1a00c-217">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-217">no</span></span>             | <span data-ttu-id="1a00c-218">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-218">no</span></span>               |
| <span data-ttu-id="1a00c-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="1a00c-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="1a00c-220">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-220">no</span></span>             | <span data-ttu-id="1a00c-221">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-221">no</span></span>               |
| <span data-ttu-id="1a00c-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="1a00c-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="1a00c-223">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-223">no</span></span>             | <span data-ttu-id="1a00c-224">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-224">no</span></span>               |
| <span data-ttu-id="1a00c-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="1a00c-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="1a00c-226">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-226">no</span></span>             | <span data-ttu-id="1a00c-227">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-227">no</span></span>               |
| <span data-ttu-id="1a00c-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="1a00c-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="1a00c-229">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-229">no</span></span>             | <span data-ttu-id="1a00c-230">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-230">no</span></span>               |
| <span data-ttu-id="1a00c-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="1a00c-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="1a00c-232">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-232">no</span></span>             | <span data-ttu-id="1a00c-233">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-233">no</span></span>               |
| <span data-ttu-id="1a00c-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="1a00c-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="1a00c-235">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-235">no</span></span>             | <span data-ttu-id="1a00c-236">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-236">no</span></span>               |
| <span data-ttu-id="1a00c-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="1a00c-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="1a00c-238">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-238">no</span></span>             | <span data-ttu-id="1a00c-239">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-239">no</span></span>               |
| <span data-ttu-id="1a00c-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="1a00c-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="1a00c-241">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-241">no</span></span>             | <span data-ttu-id="1a00c-242">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-242">no</span></span>               |
| <span data-ttu-id="1a00c-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="1a00c-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="1a00c-244">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-244">no</span></span>             | <span data-ttu-id="1a00c-245">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-245">no</span></span>               |
| <span data-ttu-id="1a00c-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="1a00c-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="1a00c-247">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-247">no</span></span>             | <span data-ttu-id="1a00c-248">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-248">no</span></span>               |
| <span data-ttu-id="1a00c-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="1a00c-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="1a00c-250">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-250">no</span></span>             | <span data-ttu-id="1a00c-251">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-251">no</span></span>               |
| <span data-ttu-id="1a00c-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="1a00c-253">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-253">no</span></span>             | <span data-ttu-id="1a00c-254">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-254">no</span></span>               |
| <span data-ttu-id="1a00c-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="1a00c-256">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-256">no</span></span>             | <span data-ttu-id="1a00c-257">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-257">no</span></span>               |
| <span data-ttu-id="1a00c-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="1a00c-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="1a00c-259">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-259">no</span></span>             | <span data-ttu-id="1a00c-260">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-260">no</span></span>               |
| <span data-ttu-id="1a00c-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="1a00c-262">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-262">no</span></span>             | <span data-ttu-id="1a00c-263">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-263">no</span></span>               |
| <span data-ttu-id="1a00c-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="1a00c-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="1a00c-265">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-265">no</span></span>             | <span data-ttu-id="1a00c-266">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-266">no</span></span>               |
| <span data-ttu-id="1a00c-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="1a00c-267">msdyn_progress</span></span>                         | <span data-ttu-id="1a00c-268">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-268">no</span></span>             | <span data-ttu-id="1a00c-269">no (sí para P4W)</span><span class="sxs-lookup"><span data-stu-id="1a00c-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="1a00c-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="1a00c-271">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-271">no</span></span>             | <span data-ttu-id="1a00c-272">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-272">no</span></span>               |
| <span data-ttu-id="1a00c-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="1a00c-274">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-274">no</span></span>             | <span data-ttu-id="1a00c-275">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-275">no</span></span>               |
| <span data-ttu-id="1a00c-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="1a00c-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="1a00c-277">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-277">no</span></span>             | <span data-ttu-id="1a00c-278">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-278">no</span></span>               |
| <span data-ttu-id="1a00c-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="1a00c-280">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-280">no</span></span>             | <span data-ttu-id="1a00c-281">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-281">no</span></span>               |
| <span data-ttu-id="1a00c-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="1a00c-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="1a00c-283">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-283">no</span></span>             | <span data-ttu-id="1a00c-284">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-284">no</span></span>               |
| <span data-ttu-id="1a00c-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="1a00c-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="1a00c-286">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-286">no</span></span>             | <span data-ttu-id="1a00c-287">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-287">no</span></span>               |
| <span data-ttu-id="1a00c-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="1a00c-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="1a00c-289">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-289">no</span></span>             | <span data-ttu-id="1a00c-290">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-290">no</span></span>               |
| <span data-ttu-id="1a00c-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="1a00c-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="1a00c-292">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-292">no</span></span>             | <span data-ttu-id="1a00c-293">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-293">no</span></span>               |
| <span data-ttu-id="1a00c-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="1a00c-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="1a00c-295">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-295">no</span></span>             | <span data-ttu-id="1a00c-296">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-296">no</span></span>               |
| <span data-ttu-id="1a00c-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="1a00c-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="1a00c-298">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-298">no</span></span>             | <span data-ttu-id="1a00c-299">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-299">no</span></span>               |
| <span data-ttu-id="1a00c-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="1a00c-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="1a00c-301">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-301">no</span></span>             | <span data-ttu-id="1a00c-302">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-302">no</span></span>               |
| <span data-ttu-id="1a00c-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="1a00c-304">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-304">no</span></span>             | <span data-ttu-id="1a00c-305">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-305">no</span></span>               |
| <span data-ttu-id="1a00c-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="1a00c-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="1a00c-307">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-307">no</span></span>             | <span data-ttu-id="1a00c-308">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-308">no</span></span>               |
| <span data-ttu-id="1a00c-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="1a00c-310">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-310">no</span></span>             | <span data-ttu-id="1a00c-311">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-311">no</span></span>               |
| <span data-ttu-id="1a00c-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="1a00c-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="1a00c-313">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-313">no</span></span>             | <span data-ttu-id="1a00c-314">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-314">no</span></span>               |
| <span data-ttu-id="1a00c-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="1a00c-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="1a00c-316">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-316">no</span></span>             | <span data-ttu-id="1a00c-317">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-317">no</span></span>               |
| <span data-ttu-id="1a00c-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="1a00c-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="1a00c-319">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-319">no</span></span>             | <span data-ttu-id="1a00c-320">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-320">no</span></span>               |
| <span data-ttu-id="1a00c-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="1a00c-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="1a00c-322">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-322">no</span></span>             | <span data-ttu-id="1a00c-323">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-323">no</span></span>               |
| <span data-ttu-id="1a00c-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="1a00c-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="1a00c-325">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-325">no</span></span>             | <span data-ttu-id="1a00c-326">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-326">no</span></span>               |
| <span data-ttu-id="1a00c-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="1a00c-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="1a00c-328">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-328">no</span></span>             | <span data-ttu-id="1a00c-329">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-329">no</span></span>               |
| <span data-ttu-id="1a00c-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="1a00c-330">msdyn_summary</span></span>                          | <span data-ttu-id="1a00c-331">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-331">no</span></span>             | <span data-ttu-id="1a00c-332">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-332">no</span></span>               |
| <span data-ttu-id="1a00c-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="1a00c-334">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-334">no</span></span>             | <span data-ttu-id="1a00c-335">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-335">no</span></span>               |
| <span data-ttu-id="1a00c-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="1a00c-337">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-337">no</span></span>             | <span data-ttu-id="1a00c-338">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="1a00c-339">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-339">Project task dependency</span></span>

| <span data-ttu-id="1a00c-340">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="1a00c-340">**Logical name**</span></span>              | <span data-ttu-id="1a00c-341">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="1a00c-341">**Can create**</span></span> | <span data-ttu-id="1a00c-342">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="1a00c-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="1a00c-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="1a00c-343">msdyn_linktype</span></span>                | <span data-ttu-id="1a00c-344">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-344">no</span></span>             | <span data-ttu-id="1a00c-345">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-345">no</span></span>           |
| <span data-ttu-id="1a00c-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="1a00c-346">msdyn_linktypename</span></span>            | <span data-ttu-id="1a00c-347">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-347">no</span></span>             | <span data-ttu-id="1a00c-348">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-348">no</span></span>           |
| <span data-ttu-id="1a00c-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="1a00c-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="1a00c-350">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-350">yes</span></span>            | <span data-ttu-id="1a00c-351">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-351">no</span></span>           |
| <span data-ttu-id="1a00c-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="1a00c-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="1a00c-353">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-353">yes</span></span>            | <span data-ttu-id="1a00c-354">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-354">no</span></span>           |
| <span data-ttu-id="1a00c-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="1a00c-355">msdyn_project</span></span>                 | <span data-ttu-id="1a00c-356">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-356">yes</span></span>            | <span data-ttu-id="1a00c-357">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-357">no</span></span>           |
| <span data-ttu-id="1a00c-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="1a00c-358">msdyn_projectname</span></span>             | <span data-ttu-id="1a00c-359">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-359">yes</span></span>            | <span data-ttu-id="1a00c-360">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-360">no</span></span>           |
| <span data-ttu-id="1a00c-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="1a00c-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="1a00c-362">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-362">yes</span></span>            | <span data-ttu-id="1a00c-363">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-363">no</span></span>           |
| <span data-ttu-id="1a00c-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="1a00c-364">msdyn_successortask</span></span>           | <span data-ttu-id="1a00c-365">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-365">yes</span></span>            | <span data-ttu-id="1a00c-366">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-366">no</span></span>           |
| <span data-ttu-id="1a00c-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="1a00c-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="1a00c-368">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-368">yes</span></span>            | <span data-ttu-id="1a00c-369">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="1a00c-370">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="1a00c-370">Resource assignment</span></span>

| <span data-ttu-id="1a00c-371">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="1a00c-371">**Logical name**</span></span>             | <span data-ttu-id="1a00c-372">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="1a00c-372">**Can create**</span></span> | <span data-ttu-id="1a00c-373">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="1a00c-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="1a00c-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="1a00c-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="1a00c-375">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-375">yes</span></span>            | <span data-ttu-id="1a00c-376">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-376">no</span></span>           |
| <span data-ttu-id="1a00c-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="1a00c-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="1a00c-378">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-378">yes</span></span>            | <span data-ttu-id="1a00c-379">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-379">no</span></span>           |
| <span data-ttu-id="1a00c-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="1a00c-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="1a00c-381">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-381">no</span></span>             | <span data-ttu-id="1a00c-382">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-382">no</span></span>           |
| <span data-ttu-id="1a00c-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="1a00c-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="1a00c-384">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-384">no</span></span>             | <span data-ttu-id="1a00c-385">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-385">no</span></span>           |
| <span data-ttu-id="1a00c-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="1a00c-386">msdyn_committype</span></span>             | <span data-ttu-id="1a00c-387">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-387">no</span></span>             | <span data-ttu-id="1a00c-388">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-388">no</span></span>           |
| <span data-ttu-id="1a00c-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="1a00c-389">msdyn_committypename</span></span>         | <span data-ttu-id="1a00c-390">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-390">no</span></span>             | <span data-ttu-id="1a00c-391">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-391">no</span></span>           |
| <span data-ttu-id="1a00c-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="1a00c-392">msdyn_effort</span></span>                 | <span data-ttu-id="1a00c-393">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-393">no</span></span>             | <span data-ttu-id="1a00c-394">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-394">no</span></span>           |
| <span data-ttu-id="1a00c-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="1a00c-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="1a00c-396">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-396">no</span></span>             | <span data-ttu-id="1a00c-397">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-397">no</span></span>           |
| <span data-ttu-id="1a00c-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="1a00c-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="1a00c-399">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-399">no</span></span>             | <span data-ttu-id="1a00c-400">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-400">no</span></span>           |
| <span data-ttu-id="1a00c-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="1a00c-401">msdyn_finish</span></span>                 | <span data-ttu-id="1a00c-402">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-402">no</span></span>             | <span data-ttu-id="1a00c-403">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-403">no</span></span>           |
| <span data-ttu-id="1a00c-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="1a00c-405">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-405">no</span></span>             | <span data-ttu-id="1a00c-406">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-406">no</span></span>           |
| <span data-ttu-id="1a00c-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="1a00c-408">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-408">no</span></span>             | <span data-ttu-id="1a00c-409">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-409">no</span></span>           |
| <span data-ttu-id="1a00c-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="1a00c-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="1a00c-411">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-411">no</span></span>             | <span data-ttu-id="1a00c-412">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-412">no</span></span>           |
| <span data-ttu-id="1a00c-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="1a00c-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="1a00c-414">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-414">no</span></span>             | <span data-ttu-id="1a00c-415">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-415">no</span></span>           |
| <span data-ttu-id="1a00c-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="1a00c-417">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-417">no</span></span>             | <span data-ttu-id="1a00c-418">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-418">no</span></span>           |
| <span data-ttu-id="1a00c-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="1a00c-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="1a00c-420">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-420">no</span></span>             | <span data-ttu-id="1a00c-421">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-421">no</span></span>           |
| <span data-ttu-id="1a00c-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="1a00c-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="1a00c-423">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-423">no</span></span>             | <span data-ttu-id="1a00c-424">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-424">no</span></span>           |
| <span data-ttu-id="1a00c-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="1a00c-425">msdyn_projectid</span></span>              | <span data-ttu-id="1a00c-426">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-426">yes</span></span>            | <span data-ttu-id="1a00c-427">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-427">no</span></span>           |
| <span data-ttu-id="1a00c-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="1a00c-428">msdyn_projectidname</span></span>          | <span data-ttu-id="1a00c-429">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-429">no</span></span>             | <span data-ttu-id="1a00c-430">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-430">no</span></span>           |
| <span data-ttu-id="1a00c-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="1a00c-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="1a00c-432">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-432">no</span></span>             | <span data-ttu-id="1a00c-433">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-433">no</span></span>           |
| <span data-ttu-id="1a00c-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="1a00c-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="1a00c-435">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-435">no</span></span>             | <span data-ttu-id="1a00c-436">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-436">no</span></span>           |
| <span data-ttu-id="1a00c-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="1a00c-437">msdyn_start</span></span>                  | <span data-ttu-id="1a00c-438">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-438">no</span></span>             | <span data-ttu-id="1a00c-439">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-439">no</span></span>           |
| <span data-ttu-id="1a00c-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="1a00c-440">msdyn_taskid</span></span>                 | <span data-ttu-id="1a00c-441">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-441">no</span></span>             | <span data-ttu-id="1a00c-442">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-442">no</span></span>           |
| <span data-ttu-id="1a00c-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="1a00c-443">msdyn_taskidname</span></span>             | <span data-ttu-id="1a00c-444">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-444">no</span></span>             | <span data-ttu-id="1a00c-445">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-445">no</span></span>           |
| <span data-ttu-id="1a00c-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="1a00c-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="1a00c-447">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-447">no</span></span>             | <span data-ttu-id="1a00c-448">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="1a00c-449">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="1a00c-449">Project team member</span></span>

| <span data-ttu-id="1a00c-450">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="1a00c-450">**Logical name**</span></span>                                 | <span data-ttu-id="1a00c-451">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="1a00c-451">**Can create**</span></span> | <span data-ttu-id="1a00c-452">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="1a00c-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="1a00c-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="1a00c-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="1a00c-454">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-454">no</span></span>             | <span data-ttu-id="1a00c-455">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-455">no</span></span>           |
| <span data-ttu-id="1a00c-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="1a00c-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="1a00c-457">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-457">no</span></span>             | <span data-ttu-id="1a00c-458">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-458">no</span></span>           |
| <span data-ttu-id="1a00c-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="1a00c-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="1a00c-460">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-460">no</span></span>             | <span data-ttu-id="1a00c-461">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-461">no</span></span>           |
| <span data-ttu-id="1a00c-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="1a00c-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="1a00c-463">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-463">no</span></span>             | <span data-ttu-id="1a00c-464">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-464">no</span></span>           |
| <span data-ttu-id="1a00c-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="1a00c-465">msdyn_effort</span></span>                                     | <span data-ttu-id="1a00c-466">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-466">no</span></span>             | <span data-ttu-id="1a00c-467">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-467">no</span></span>           |
| <span data-ttu-id="1a00c-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="1a00c-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="1a00c-469">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-469">no</span></span>             | <span data-ttu-id="1a00c-470">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-470">no</span></span>           |
| <span data-ttu-id="1a00c-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="1a00c-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="1a00c-472">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-472">no</span></span>             | <span data-ttu-id="1a00c-473">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-473">no</span></span>           |
| <span data-ttu-id="1a00c-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="1a00c-474">msdyn_finish</span></span>                                     | <span data-ttu-id="1a00c-475">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-475">no</span></span>             | <span data-ttu-id="1a00c-476">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-476">no</span></span>           |
| <span data-ttu-id="1a00c-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="1a00c-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="1a00c-478">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-478">no</span></span>             | <span data-ttu-id="1a00c-479">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-479">no</span></span>           |
| <span data-ttu-id="1a00c-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="1a00c-480">msdyn_hours</span></span>                                      | <span data-ttu-id="1a00c-481">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-481">no</span></span>             | <span data-ttu-id="1a00c-482">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-482">no</span></span>           |
| <span data-ttu-id="1a00c-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="1a00c-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="1a00c-484">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-484">no</span></span>             | <span data-ttu-id="1a00c-485">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-485">no</span></span>           |
| <span data-ttu-id="1a00c-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="1a00c-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="1a00c-487">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-487">no</span></span>             | <span data-ttu-id="1a00c-488">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-488">no</span></span>           |
| <span data-ttu-id="1a00c-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="1a00c-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="1a00c-490">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-490">no</span></span>             | <span data-ttu-id="1a00c-491">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-491">no</span></span>           |
| <span data-ttu-id="1a00c-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="1a00c-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="1a00c-493">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-493">no</span></span>             | <span data-ttu-id="1a00c-494">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-494">no</span></span>           |
| <span data-ttu-id="1a00c-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="1a00c-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="1a00c-496">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-496">no</span></span>             | <span data-ttu-id="1a00c-497">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-497">no</span></span>           |
| <span data-ttu-id="1a00c-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="1a00c-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="1a00c-499">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-499">no</span></span>             | <span data-ttu-id="1a00c-500">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-500">no</span></span>           |
| <span data-ttu-id="1a00c-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="1a00c-501">msdyn_start</span></span>                                      | <span data-ttu-id="1a00c-502">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-502">no</span></span>             | <span data-ttu-id="1a00c-503">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="1a00c-504">Project</span><span class="sxs-lookup"><span data-stu-id="1a00c-504">Project</span></span>

| <span data-ttu-id="1a00c-505">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="1a00c-505">**Logical name**</span></span>                       | <span data-ttu-id="1a00c-506">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="1a00c-506">**Can create**</span></span> | <span data-ttu-id="1a00c-507">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="1a00c-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="1a00c-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="1a00c-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="1a00c-509">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-509">no</span></span>             | <span data-ttu-id="1a00c-510">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-510">no</span></span>           |
| <span data-ttu-id="1a00c-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="1a00c-512">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-512">no</span></span>             | <span data-ttu-id="1a00c-513">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-513">no</span></span>           |
| <span data-ttu-id="1a00c-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="1a00c-515">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-515">no</span></span>             | <span data-ttu-id="1a00c-516">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-516">no</span></span>           |
| <span data-ttu-id="1a00c-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="1a00c-518">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-518">no</span></span>             | <span data-ttu-id="1a00c-519">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-519">no</span></span>           |
| <span data-ttu-id="1a00c-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="1a00c-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="1a00c-521">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-521">no</span></span>             | <span data-ttu-id="1a00c-522">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-522">no</span></span>           |
| <span data-ttu-id="1a00c-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="1a00c-524">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-524">no</span></span>             | <span data-ttu-id="1a00c-525">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-525">no</span></span>           |
| <span data-ttu-id="1a00c-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="1a00c-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="1a00c-527">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-527">yes</span></span>            | <span data-ttu-id="1a00c-528">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-528">no</span></span>           |
| <span data-ttu-id="1a00c-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="1a00c-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="1a00c-530">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-530">yes</span></span>            | <span data-ttu-id="1a00c-531">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-531">no</span></span>           |
| <span data-ttu-id="1a00c-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="1a00c-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="1a00c-533">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-533">yes</span></span>            | <span data-ttu-id="1a00c-534">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-534">no</span></span>           |
| <span data-ttu-id="1a00c-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="1a00c-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="1a00c-536">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-536">no</span></span>             | <span data-ttu-id="1a00c-537">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-537">no</span></span>           |
| <span data-ttu-id="1a00c-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="1a00c-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="1a00c-539">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-539">no</span></span>             | <span data-ttu-id="1a00c-540">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-540">no</span></span>           |
| <span data-ttu-id="1a00c-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="1a00c-542">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-542">no</span></span>             | <span data-ttu-id="1a00c-543">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-543">no</span></span>           |
| <span data-ttu-id="1a00c-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="1a00c-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="1a00c-545">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-545">no</span></span>             | <span data-ttu-id="1a00c-546">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-546">no</span></span>           |
| <span data-ttu-id="1a00c-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="1a00c-548">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-548">no</span></span>             | <span data-ttu-id="1a00c-549">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-549">no</span></span>           |
| <span data-ttu-id="1a00c-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="1a00c-550">msdyn_duration</span></span>                         | <span data-ttu-id="1a00c-551">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-551">no</span></span>             | <span data-ttu-id="1a00c-552">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-552">no</span></span>           |
| <span data-ttu-id="1a00c-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="1a00c-553">msdyn_effort</span></span>                           | <span data-ttu-id="1a00c-554">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-554">no</span></span>             | <span data-ttu-id="1a00c-555">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-555">no</span></span>           |
| <span data-ttu-id="1a00c-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="1a00c-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="1a00c-557">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-557">no</span></span>             | <span data-ttu-id="1a00c-558">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-558">no</span></span>           |
| <span data-ttu-id="1a00c-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="1a00c-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="1a00c-560">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-560">no</span></span>             | <span data-ttu-id="1a00c-561">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-561">no</span></span>           |
| <span data-ttu-id="1a00c-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="1a00c-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="1a00c-563">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-563">no</span></span>             | <span data-ttu-id="1a00c-564">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-564">no</span></span>           |
| <span data-ttu-id="1a00c-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="1a00c-565">msdyn_finish</span></span>                           | <span data-ttu-id="1a00c-566">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-566">yes</span></span>            | <span data-ttu-id="1a00c-567">sí</span><span class="sxs-lookup"><span data-stu-id="1a00c-567">yes</span></span>          |
| <span data-ttu-id="1a00c-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="1a00c-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="1a00c-569">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-569">no</span></span>             | <span data-ttu-id="1a00c-570">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-570">no</span></span>           |
| <span data-ttu-id="1a00c-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="1a00c-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="1a00c-572">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-572">no</span></span>             | <span data-ttu-id="1a00c-573">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-573">no</span></span>           |
| <span data-ttu-id="1a00c-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="1a00c-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="1a00c-575">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-575">no</span></span>             | <span data-ttu-id="1a00c-576">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-576">no</span></span>           |
| <span data-ttu-id="1a00c-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="1a00c-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="1a00c-578">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-578">no</span></span>             | <span data-ttu-id="1a00c-579">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-579">no</span></span>           |
| <span data-ttu-id="1a00c-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="1a00c-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="1a00c-581">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-581">no</span></span>             | <span data-ttu-id="1a00c-582">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-582">no</span></span>           |
| <span data-ttu-id="1a00c-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="1a00c-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="1a00c-584">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-584">no</span></span>             | <span data-ttu-id="1a00c-585">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-585">no</span></span>           |
| <span data-ttu-id="1a00c-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="1a00c-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="1a00c-587">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-587">no</span></span>             | <span data-ttu-id="1a00c-588">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-588">no</span></span>           |
| <span data-ttu-id="1a00c-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="1a00c-590">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-590">no</span></span>             | <span data-ttu-id="1a00c-591">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-591">no</span></span>           |
| <span data-ttu-id="1a00c-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="1a00c-593">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-593">no</span></span>             | <span data-ttu-id="1a00c-594">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-594">no</span></span>           |
| <span data-ttu-id="1a00c-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="1a00c-596">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-596">no</span></span>             | <span data-ttu-id="1a00c-597">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-597">no</span></span>           |
| <span data-ttu-id="1a00c-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="1a00c-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="1a00c-599">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-599">no</span></span>             | <span data-ttu-id="1a00c-600">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-600">no</span></span>           |
| <span data-ttu-id="1a00c-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="1a00c-602">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-602">no</span></span>             | <span data-ttu-id="1a00c-603">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-603">no</span></span>           |
| <span data-ttu-id="1a00c-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="1a00c-604">msdyn_progress</span></span>                         | <span data-ttu-id="1a00c-605">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-605">no</span></span>             | <span data-ttu-id="1a00c-606">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-606">no</span></span>           |
| <span data-ttu-id="1a00c-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="1a00c-608">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-608">no</span></span>             | <span data-ttu-id="1a00c-609">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-609">no</span></span>           |
| <span data-ttu-id="1a00c-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="1a00c-611">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-611">no</span></span>             | <span data-ttu-id="1a00c-612">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-612">no</span></span>           |
| <span data-ttu-id="1a00c-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="1a00c-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="1a00c-614">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-614">no</span></span>             | <span data-ttu-id="1a00c-615">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-615">no</span></span>           |
| <span data-ttu-id="1a00c-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="1a00c-617">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-617">no</span></span>             | <span data-ttu-id="1a00c-618">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-618">no</span></span>           |
| <span data-ttu-id="1a00c-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="1a00c-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="1a00c-620">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-620">no</span></span>             | <span data-ttu-id="1a00c-621">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-621">no</span></span>           |
| <span data-ttu-id="1a00c-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="1a00c-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="1a00c-623">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-623">no</span></span>             | <span data-ttu-id="1a00c-624">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-624">no</span></span>           |
| <span data-ttu-id="1a00c-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="1a00c-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="1a00c-626">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-626">no</span></span>             | <span data-ttu-id="1a00c-627">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-627">no</span></span>           |
| <span data-ttu-id="1a00c-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="1a00c-629">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-629">no</span></span>             | <span data-ttu-id="1a00c-630">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-630">no</span></span>           |
| <span data-ttu-id="1a00c-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="1a00c-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="1a00c-632">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-632">no</span></span>             | <span data-ttu-id="1a00c-633">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-633">no</span></span>           |
| <span data-ttu-id="1a00c-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="1a00c-635">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-635">no</span></span>             | <span data-ttu-id="1a00c-636">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-636">no</span></span>           |
| <span data-ttu-id="1a00c-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="1a00c-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="1a00c-638">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-638">no</span></span>             | <span data-ttu-id="1a00c-639">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-639">no</span></span>           |
| <span data-ttu-id="1a00c-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="1a00c-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="1a00c-641">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-641">no</span></span>             | <span data-ttu-id="1a00c-642">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-642">no</span></span>           |
| <span data-ttu-id="1a00c-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="1a00c-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="1a00c-644">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-644">no</span></span>             | <span data-ttu-id="1a00c-645">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-645">no</span></span>           |
| <span data-ttu-id="1a00c-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="1a00c-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="1a00c-647">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-647">no</span></span>             | <span data-ttu-id="1a00c-648">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-648">no</span></span>           |
| <span data-ttu-id="1a00c-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="1a00c-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="1a00c-650">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-650">no</span></span>             | <span data-ttu-id="1a00c-651">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-651">no</span></span>           |
| <span data-ttu-id="1a00c-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="1a00c-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="1a00c-653">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-653">no</span></span>             | <span data-ttu-id="1a00c-654">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-654">no</span></span>           |
| <span data-ttu-id="1a00c-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="1a00c-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="1a00c-656">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-656">no</span></span>             | <span data-ttu-id="1a00c-657">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-657">no</span></span>           |
| <span data-ttu-id="1a00c-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="1a00c-659">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-659">no</span></span>             | <span data-ttu-id="1a00c-660">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-660">no</span></span>           |
| <span data-ttu-id="1a00c-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="1a00c-662">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-662">no</span></span>             | <span data-ttu-id="1a00c-663">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-663">no</span></span>           |
| <span data-ttu-id="1a00c-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="1a00c-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="1a00c-665">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-665">no</span></span>             | <span data-ttu-id="1a00c-666">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-666">no</span></span>           |
| <span data-ttu-id="1a00c-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="1a00c-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="1a00c-668">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-668">no</span></span>             | <span data-ttu-id="1a00c-669">no</span><span class="sxs-lookup"><span data-stu-id="1a00c-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="1a00c-670">Limitaciones y problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="1a00c-670">Limitations and known issues</span></span>
<span data-ttu-id="1a00c-671">La siguiente es una lista de limitaciones y problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="1a00c-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="1a00c-672">Las API de programación solo pueden ser utilizadas por los **Usuarios con licencia de Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="1a00c-673">No pueden ser utilizadas por:</span><span class="sxs-lookup"><span data-stu-id="1a00c-673">They can't be used by:</span></span>
    - <span data-ttu-id="1a00c-674">Usuarios de la aplicación</span><span class="sxs-lookup"><span data-stu-id="1a00c-674">Application users</span></span>
    - <span data-ttu-id="1a00c-675">Usuarios de sistema</span><span class="sxs-lookup"><span data-stu-id="1a00c-675">System users</span></span>
    - <span data-ttu-id="1a00c-676">Usuarios de integración</span><span class="sxs-lookup"><span data-stu-id="1a00c-676">Integration users</span></span>
    - <span data-ttu-id="1a00c-677">Otros usuarios que no tienen la licencia requerida</span><span class="sxs-lookup"><span data-stu-id="1a00c-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="1a00c-678">Cada **OperationSet** solo puede tener un máximo de 100 operaciones.</span><span class="sxs-lookup"><span data-stu-id="1a00c-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="1a00c-679">Cada usuario solo puede tener un máximo de 10 operaciones **OperationSet** abiertas.</span><span class="sxs-lookup"><span data-stu-id="1a00c-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="1a00c-680">Project Operations actualmente admiten un máximo de 500 tareas en total en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="1a00c-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="1a00c-681">El estado de error y los registros de error de **OperationSet** no están disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="1a00c-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="1a00c-682">Límites y límites en proyectos y tareas</span><span class="sxs-lookup"><span data-stu-id="1a00c-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="1a00c-683">Control de errores</span><span class="sxs-lookup"><span data-stu-id="1a00c-683">Error handling</span></span>

   - <span data-ttu-id="1a00c-684">Para revisar los errores generados por los conjuntos de operaciones, vaya a **Configuración** \> **Integración de programación** \> **Conjuntos de operaciones**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="1a00c-685">Para revisar los errores generados por el servicio de programación de proyectos, vaya a **Configuración** \> **Integración de programación** \> **Registros de errores de PSS**.</span><span class="sxs-lookup"><span data-stu-id="1a00c-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="1a00c-686">Escenario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a00c-686">Sample scenario</span></span>

<span data-ttu-id="1a00c-687">En este escenario, creará un proyecto, un miembro del equipo, cuatro tareas y dos asignaciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="1a00c-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="1a00c-688">A continuación, actualizará una tarea, actualizará el proyecto, eliminará una tarea, eliminará una asignación de recursos y creará una dependencia de tareas.</span><span class="sxs-lookup"><span data-stu-id="1a00c-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="1a00c-689">Ejemplos adicionales</span><span class="sxs-lookup"><span data-stu-id="1a00c-689">Additional samples</span></span>

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
