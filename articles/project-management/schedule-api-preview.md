---
title: Utilizar las API de programación para realizar operaciones con entidades de programación
description: Este tema proporciona información y ejemplos para usar las API de programación.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868150"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="0ac4c-103">Utilizar las API de programación para realizar operaciones con entidades de programación</span><span class="sxs-lookup"><span data-stu-id="0ac4c-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="0ac4c-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="0ac4c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="0ac4c-105">Parte o toda la funcionalidad que se menciona en este tema está disponible como parte de una versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="0ac4c-106">El contenido y la funcionalidad están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="0ac4c-107">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="0ac4c-107">Scheduling entities</span></span>

<span data-ttu-id="0ac4c-108">Las API de programación brindan la capacidad de realizar operaciones de creación, actualización y eliminación con **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="0ac4c-109">Estas entidades se administran a través del motor de programación en Project para la web.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="0ac4c-110">Crear, actualizar y eliminar operaciones con **Entidades de programación** estaba restringido en versiones anteriores de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="0ac4c-111">La siguiente tabla proporciona una lista completa de las **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="0ac4c-112">Nombre de entidad</span><span class="sxs-lookup"><span data-stu-id="0ac4c-112">Entity name</span></span>  | <span data-ttu-id="0ac4c-113">Nombre lógico de la entidad</span><span class="sxs-lookup"><span data-stu-id="0ac4c-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="0ac4c-114">Project</span><span class="sxs-lookup"><span data-stu-id="0ac4c-114">Project</span></span> | <span data-ttu-id="0ac4c-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="0ac4c-115">msdyn_project</span></span> |
| <span data-ttu-id="0ac4c-116">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="0ac4c-116">Project Task</span></span>  | <span data-ttu-id="0ac4c-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="0ac4c-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="0ac4c-118">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="0ac4c-118">Project Task Dependency</span></span>  | <span data-ttu-id="0ac4c-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="0ac4c-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="0ac4c-120">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="0ac4c-120">Resource Assignment</span></span> | <span data-ttu-id="0ac4c-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="0ac4c-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="0ac4c-122">Cubo de proyecto</span><span class="sxs-lookup"><span data-stu-id="0ac4c-122">Project Bucket</span></span>  | <span data-ttu-id="0ac4c-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="0ac4c-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="0ac4c-124">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="0ac4c-124">Project Team Member</span></span> | <span data-ttu-id="0ac4c-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="0ac4c-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="0ac4c-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="0ac4c-126">OperationSet</span></span>

<span data-ttu-id="0ac4c-127">OperationSet es un patrón de unidad de trabajo que se puede usar cuando se deben procesar varias solicitudes que afectan la programación dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="0ac4c-128">Programar las API</span><span class="sxs-lookup"><span data-stu-id="0ac4c-128">Schedule APIs</span></span>

<span data-ttu-id="0ac4c-129">La siguiente es una lista de las API de programación actuales.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="0ac4c-130">**msdyn_CreateProjectV1**: esta API se puede utilizar para crear un proyecto.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="0ac4c-131">El proyecto y el cubo del proyecto predeterminado se crean inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="0ac4c-132">**msdyn_CreateTeamMemberV1**: esta API se puede utilizar para crear un miembro de equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="0ac4c-133">El registro de miembro del equipo se crea inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="0ac4c-134">**msdyn_CreateOperationSetV1**: esta API se puede utilizar para programar varias solicitudes que deben realizarse dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="0ac4c-135">**msdyn_PSSCreateV1**: esta API se puede utilizar para crear una entidad.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="0ac4c-136">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de creación.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="0ac4c-137">**msdyn_PSSUpdateV1**: esta API se puede utilizar para actualizar una entidad.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="0ac4c-138">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="0ac4c-139">**msdyn_PSSDeleteV1**: esta API se puede utilizar para eliminar una entidad.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="0ac4c-140">La entidad puede ser cualquiera de las entidades de programación que admiten la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="0ac4c-141">**msdyn_ExecuteOperationSetV1**: esta API se utiliza para ejecutar todas las operaciones dentro del conjunto de operaciones establecido.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="0ac4c-142">Utilizar las API de programación con OperationSet</span><span class="sxs-lookup"><span data-stu-id="0ac4c-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="0ac4c-143">Porque los registros con ambos **CreateProjectV1** y **CreateTeamMemberV1** se crean inmediatamente, estas API no se pueden utilizar en **OperationSet** directamente.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="0ac4c-144">Sin embargo, puede utilizar la API para crear los registros necesarios, crear un **OperationSet** y, a continuación, utilizar estos registros creados previamente en **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="0ac4c-145">Operaciones admitidas</span><span class="sxs-lookup"><span data-stu-id="0ac4c-145">Supported operations</span></span>

| <span data-ttu-id="0ac4c-146">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="0ac4c-146">Scheduling entity</span></span> | <span data-ttu-id="0ac4c-147">Crear</span><span class="sxs-lookup"><span data-stu-id="0ac4c-147">Create</span></span> | <span data-ttu-id="0ac4c-148">Actualización</span><span class="sxs-lookup"><span data-stu-id="0ac4c-148">Update</span></span> | <span data-ttu-id="0ac4c-149">Delete</span><span class="sxs-lookup"><span data-stu-id="0ac4c-149">Delete</span></span> | <span data-ttu-id="0ac4c-150">Consideraciones importantes</span><span class="sxs-lookup"><span data-stu-id="0ac4c-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="0ac4c-151">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="0ac4c-151">Project task</span></span> | <span data-ttu-id="0ac4c-152">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-152">Yes</span></span> | <span data-ttu-id="0ac4c-153">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-153">Yes</span></span> | <span data-ttu-id="0ac4c-154">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-154">Yes</span></span> | <span data-ttu-id="0ac4c-155">Nada</span><span class="sxs-lookup"><span data-stu-id="0ac4c-155">None</span></span> |
| <span data-ttu-id="0ac4c-156">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="0ac4c-156">Project task dependency</span></span> | <span data-ttu-id="0ac4c-157">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-157">Yes</span></span> | <span data-ttu-id="0ac4c-158">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-158">Yes</span></span> | | <span data-ttu-id="0ac4c-159">Los registros de dependencia de tareas del proyecto no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="0ac4c-160">En su lugar, se puede eliminar un registro antiguo y se puede crear un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="0ac4c-161">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="0ac4c-161">Resource assignment</span></span> | <span data-ttu-id="0ac4c-162">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-162">Yes</span></span> | <span data-ttu-id="0ac4c-163">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-163">Yes</span></span> | | <span data-ttu-id="0ac4c-164">No se admiten las operaciones con los siguientes campos: **BookableResourceID**, **Esfuerzo**, **EffortCompleted**, **EffortCompleted** y **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="0ac4c-165">Los registros de asignación de recursos no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="0ac4c-166">En su lugar, se puede eliminar el registro antiguo y se puede crear un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="0ac4c-167">Cubo de proyecto</span><span class="sxs-lookup"><span data-stu-id="0ac4c-167">Project bucket</span></span> | <span data-ttu-id="0ac4c-168">N/D</span><span class="sxs-lookup"><span data-stu-id="0ac4c-168">N/A</span></span> | <span data-ttu-id="0ac4c-169">N/D</span><span class="sxs-lookup"><span data-stu-id="0ac4c-169">N/A</span></span> | <span data-ttu-id="0ac4c-170">N/D</span><span class="sxs-lookup"><span data-stu-id="0ac4c-170">N/A</span></span> | <span data-ttu-id="0ac4c-171">El cubo predeterminado se crea utilizando la API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="0ac4c-172">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="0ac4c-172">Project team member</span></span> | <span data-ttu-id="0ac4c-173">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-173">Yes</span></span> | <span data-ttu-id="0ac4c-174">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-174">Yes</span></span> | <span data-ttu-id="0ac4c-175">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-175">Yes</span></span> | <span data-ttu-id="0ac4c-176">Para la operación de creación, use la API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="0ac4c-177">Project</span><span class="sxs-lookup"><span data-stu-id="0ac4c-177">Project</span></span> | <span data-ttu-id="0ac4c-178">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-178">Yes</span></span> | <span data-ttu-id="0ac4c-179">Sí</span><span class="sxs-lookup"><span data-stu-id="0ac4c-179">Yes</span></span> | <span data-ttu-id="0ac4c-180">N/D</span><span class="sxs-lookup"><span data-stu-id="0ac4c-180">N/A</span></span> | <span data-ttu-id="0ac4c-181">No se admiten operaciones con los siguientes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esfuerzo**, **EffortCompleted**, **EffortRemaining**, **Progreso**, **Terminar**, **TaskEarliestStart**, y **Duración**.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="0ac4c-182">Estas API se pueden llamar con objetos de entidad que incluyen campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="0ac4c-183">La propiedad del identificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-183">The ID property is optional.</span></span> <span data-ttu-id="0ac4c-184">Si se proporciona, el sistema intenta usarlo y lanza una excepción si no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="0ac4c-185">Si no se proporciona, el sistema lo generará.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="0ac4c-186">Limitaciones y problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="0ac4c-186">Limitations and known issues</span></span>
<span data-ttu-id="0ac4c-187">La siguiente es una lista de limitaciones y problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="0ac4c-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="0ac4c-188">Las API de programación solo pueden ser utilizadas por los **Usuarios con licencia de Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="0ac4c-189">No pueden ser utilizadas por:</span><span class="sxs-lookup"><span data-stu-id="0ac4c-189">They can't be used by:</span></span>
    - <span data-ttu-id="0ac4c-190">Usuarios de la aplicación</span><span class="sxs-lookup"><span data-stu-id="0ac4c-190">Application users</span></span>
    - <span data-ttu-id="0ac4c-191">Usuarios de sistema</span><span class="sxs-lookup"><span data-stu-id="0ac4c-191">System users</span></span>
    - <span data-ttu-id="0ac4c-192">Usuarios de integración</span><span class="sxs-lookup"><span data-stu-id="0ac4c-192">Integration users</span></span>
    - <span data-ttu-id="0ac4c-193">Otros usuarios que no tienen la licencia requerida</span><span class="sxs-lookup"><span data-stu-id="0ac4c-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="0ac4c-194">Cada **OperationSet** solo puede tener un máximo de 100 operaciones.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="0ac4c-195">Cada usuario solo puede tener un máximo de 10 operaciones **OperationSet** abiertas.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="0ac4c-196">Project Operations actualmente admiten un máximo de 500 tareas en total en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="0ac4c-197">El estado de error y los registros de error de **OperationSet** no están disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="0ac4c-198">Las API de programación se ofrecen en versión preliminar pública.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="0ac4c-199">Microsoft no admite el uso de estas API en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="0ac4c-200">Escenario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0ac4c-200">Sample scenario</span></span>

<span data-ttu-id="0ac4c-201">En este escenario, creará un proyecto, un miembro del equipo, cuatro tareas y dos asignaciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="0ac4c-202">A continuación, actualizará una tarea, actualizará el proyecto, eliminará una tarea, eliminará una asignación de recursos y creará una dependencia de tareas.</span><span class="sxs-lookup"><span data-stu-id="0ac4c-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="0ac4c-203">Ejemplos adicionales</span><span class="sxs-lookup"><span data-stu-id="0ac4c-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
