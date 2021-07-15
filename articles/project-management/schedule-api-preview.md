---
title: Usar las API de programación de proyectos para realizar operaciones con entidades de programación
description: Este tema proporciona información y ejemplos para usar las API de programación de proyectos.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293248"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="96450-103">Usar las API de programación de proyectos para realizar operaciones con entidades de programación</span><span class="sxs-lookup"><span data-stu-id="96450-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="96450-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="96450-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="96450-105">Parte o toda la funcionalidad que se menciona en este tema está disponible como parte de una versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="96450-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="96450-106">El contenido y la funcionalidad están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="96450-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="96450-107">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="96450-107">Scheduling entities</span></span>

<span data-ttu-id="96450-108">Las API de programación de proyectos ofrecen la capacidad de realizar operaciones de creación, actualización y eliminación con **Entidades de programación**.</span><span class="sxs-lookup"><span data-stu-id="96450-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="96450-109">Estas entidades se administran a través del motor de programación en Project para la web.</span><span class="sxs-lookup"><span data-stu-id="96450-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="96450-110">Crear, actualizar y eliminar operaciones con **Entidades de programación** estaba restringido en versiones anteriores de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="96450-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="96450-111">La siguiente tabla proporciona una lista completa de las entidades del programación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="96450-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="96450-112">Nombre de entidad</span><span class="sxs-lookup"><span data-stu-id="96450-112">Entity name</span></span>  | <span data-ttu-id="96450-113">Nombre lógico de la entidad</span><span class="sxs-lookup"><span data-stu-id="96450-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="96450-114">Project</span><span class="sxs-lookup"><span data-stu-id="96450-114">Project</span></span> | <span data-ttu-id="96450-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="96450-115">msdyn_project</span></span> |
| <span data-ttu-id="96450-116">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-116">Project Task</span></span>  | <span data-ttu-id="96450-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="96450-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="96450-118">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-118">Project Task Dependency</span></span>  | <span data-ttu-id="96450-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="96450-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="96450-120">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="96450-120">Resource Assignment</span></span> | <span data-ttu-id="96450-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="96450-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="96450-122">Cubo de proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-122">Project Bucket</span></span>  | <span data-ttu-id="96450-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="96450-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="96450-124">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-124">Project Team Member</span></span> | <span data-ttu-id="96450-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="96450-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="96450-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="96450-126">OperationSet</span></span>

<span data-ttu-id="96450-127">OperationSet es un patrón de unidad de trabajo que se puede usar cuando se deben procesar varias solicitudes que afectan la programación dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="96450-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="96450-128">API de programación del proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-128">Project schedule APIs</span></span>

<span data-ttu-id="96450-129">La siguiente es una lista de las API de programación de proyectos actuales.</span><span class="sxs-lookup"><span data-stu-id="96450-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="96450-130">**msdyn_CreateProjectV1**: esta API se puede utilizar para crear un proyecto.</span><span class="sxs-lookup"><span data-stu-id="96450-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="96450-131">El proyecto y el cubo del proyecto predeterminado se crean inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="96450-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="96450-132">**msdyn_CreateTeamMemberV1**: esta API se puede utilizar para crear un miembro de equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="96450-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="96450-133">El registro de miembro del equipo se crea inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="96450-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="96450-134">**msdyn_CreateOperationSetV1**: esta API se puede utilizar para programar varias solicitudes que deben realizarse dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="96450-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="96450-135">**msdyn_PSSCreateV1**: esta API se puede utilizar para crear una entidad.</span><span class="sxs-lookup"><span data-stu-id="96450-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="96450-136">La entidad puede ser cualquiera de las entidades de programación del proyecto que respaldan la operación de creación.</span><span class="sxs-lookup"><span data-stu-id="96450-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="96450-137">**msdyn_PSSUpdateV1**: esta API se puede utilizar para actualizar una entidad.</span><span class="sxs-lookup"><span data-stu-id="96450-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="96450-138">La entidad puede ser cualquiera de las entidades de programación del proyecto que respaldan la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="96450-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="96450-139">**msdyn_PSSDeleteV1**: esta API se puede utilizar para eliminar una entidad.</span><span class="sxs-lookup"><span data-stu-id="96450-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="96450-140">La entidad puede ser cualquiera de las entidades de programación del proyecto que respaldan la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="96450-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="96450-141">**msdyn_ExecuteOperationSetV1**: esta API se utiliza para ejecutar todas las operaciones dentro del conjunto de operaciones establecido.</span><span class="sxs-lookup"><span data-stu-id="96450-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="96450-142">Usar las API de programación de proyectos con OperationSet</span><span class="sxs-lookup"><span data-stu-id="96450-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="96450-143">Porque los registros con ambos **CreateProjectV1** y **CreateTeamMemberV1** se crean inmediatamente, estas API no se pueden utilizar en **OperationSet** directamente.</span><span class="sxs-lookup"><span data-stu-id="96450-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="96450-144">Sin embargo, puede utilizar la API para crear los registros necesarios, crear un **OperationSet** y, a continuación, utilizar estos registros creados previamente en **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="96450-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="96450-145">Operaciones admitidas</span><span class="sxs-lookup"><span data-stu-id="96450-145">Supported operations</span></span>

| <span data-ttu-id="96450-146">Entidades de programación</span><span class="sxs-lookup"><span data-stu-id="96450-146">Scheduling entity</span></span> | <span data-ttu-id="96450-147">Crear</span><span class="sxs-lookup"><span data-stu-id="96450-147">Create</span></span> | <span data-ttu-id="96450-148">Actualización</span><span class="sxs-lookup"><span data-stu-id="96450-148">Update</span></span> | <span data-ttu-id="96450-149">Delete</span><span class="sxs-lookup"><span data-stu-id="96450-149">Delete</span></span> | <span data-ttu-id="96450-150">Consideraciones importantes</span><span class="sxs-lookup"><span data-stu-id="96450-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="96450-151">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-151">Project task</span></span> | <span data-ttu-id="96450-152">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-152">Yes</span></span> | <span data-ttu-id="96450-153">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-153">Yes</span></span> | <span data-ttu-id="96450-154">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-154">Yes</span></span> | <span data-ttu-id="96450-155">Nada</span><span class="sxs-lookup"><span data-stu-id="96450-155">None</span></span> |
| <span data-ttu-id="96450-156">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-156">Project task dependency</span></span> | <span data-ttu-id="96450-157">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-157">Yes</span></span> | <span data-ttu-id="96450-158">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-158">Yes</span></span> | | <span data-ttu-id="96450-159">Los registros de dependencia de tareas del proyecto no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="96450-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="96450-160">En su lugar, se puede eliminar un registro antiguo y se puede crear un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="96450-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="96450-161">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="96450-161">Resource assignment</span></span> | <span data-ttu-id="96450-162">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-162">Yes</span></span> | <span data-ttu-id="96450-163">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-163">Yes</span></span> | | <span data-ttu-id="96450-164">No se admiten las operaciones con los siguientes campos: **BookableResourceID**, **Esfuerzo**, **EffortCompleted**, **EffortCompleted** y **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="96450-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="96450-165">Los registros de asignación de recursos no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="96450-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="96450-166">En su lugar, se puede eliminar el registro antiguo y se puede crear un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="96450-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="96450-167">Cubo de proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-167">Project bucket</span></span> | <span data-ttu-id="96450-168">N/D</span><span class="sxs-lookup"><span data-stu-id="96450-168">N/A</span></span> | <span data-ttu-id="96450-169">N/D</span><span class="sxs-lookup"><span data-stu-id="96450-169">N/A</span></span> | <span data-ttu-id="96450-170">N/D</span><span class="sxs-lookup"><span data-stu-id="96450-170">N/A</span></span> | <span data-ttu-id="96450-171">El cubo predeterminado se crea utilizando la API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="96450-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="96450-172">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-172">Project team member</span></span> | <span data-ttu-id="96450-173">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-173">Yes</span></span> | <span data-ttu-id="96450-174">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-174">Yes</span></span> | <span data-ttu-id="96450-175">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-175">Yes</span></span> | <span data-ttu-id="96450-176">Para la operación de creación, use la API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="96450-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="96450-177">Project</span><span class="sxs-lookup"><span data-stu-id="96450-177">Project</span></span> | <span data-ttu-id="96450-178">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-178">Yes</span></span> | <span data-ttu-id="96450-179">Sí</span><span class="sxs-lookup"><span data-stu-id="96450-179">Yes</span></span> | <span data-ttu-id="96450-180">N/D</span><span class="sxs-lookup"><span data-stu-id="96450-180">N/A</span></span> | <span data-ttu-id="96450-181">No se admiten operaciones con los siguientes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esfuerzo**, **EffortCompleted**, **EffortRemaining**, **Progreso**, **Terminar**, **TaskEarliestStart**, y **Duración**.</span><span class="sxs-lookup"><span data-stu-id="96450-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="96450-182">Estas API se pueden llamar con objetos de entidad que incluyen campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="96450-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="96450-183">La propiedad del identificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="96450-183">The ID property is optional.</span></span> <span data-ttu-id="96450-184">Si se proporciona, el sistema intenta usarlo y lanza una excepción si no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="96450-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="96450-185">Si no se proporciona, el sistema lo generará.</span><span class="sxs-lookup"><span data-stu-id="96450-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="96450-186">Campos restringidos</span><span class="sxs-lookup"><span data-stu-id="96450-186">Restricted fields</span></span>

<span data-ttu-id="96450-187">Las siguientes tablas definen los campos que están restringidos para **Crear** y **Editar.**</span><span class="sxs-lookup"><span data-stu-id="96450-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="96450-188">Tarea de proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-188">Project task</span></span>

| <span data-ttu-id="96450-189">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="96450-189">**Logical name**</span></span>                       | <span data-ttu-id="96450-190">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="96450-190">**Can create**</span></span> | <span data-ttu-id="96450-191">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="96450-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="96450-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="96450-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="96450-193">no</span><span class="sxs-lookup"><span data-stu-id="96450-193">no</span></span>             | <span data-ttu-id="96450-194">no</span><span class="sxs-lookup"><span data-stu-id="96450-194">no</span></span>               |
| <span data-ttu-id="96450-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="96450-196">no</span><span class="sxs-lookup"><span data-stu-id="96450-196">no</span></span>             | <span data-ttu-id="96450-197">no</span><span class="sxs-lookup"><span data-stu-id="96450-197">no</span></span>               |
| <span data-ttu-id="96450-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="96450-198">msdyn_actualend</span></span>                        | <span data-ttu-id="96450-199">no</span><span class="sxs-lookup"><span data-stu-id="96450-199">no</span></span>             | <span data-ttu-id="96450-200">no</span><span class="sxs-lookup"><span data-stu-id="96450-200">no</span></span>               |
| <span data-ttu-id="96450-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="96450-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="96450-202">no</span><span class="sxs-lookup"><span data-stu-id="96450-202">no</span></span>             | <span data-ttu-id="96450-203">no</span><span class="sxs-lookup"><span data-stu-id="96450-203">no</span></span>               |
| <span data-ttu-id="96450-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="96450-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="96450-205">no</span><span class="sxs-lookup"><span data-stu-id="96450-205">no</span></span>             | <span data-ttu-id="96450-206">no</span><span class="sxs-lookup"><span data-stu-id="96450-206">no</span></span>               |
| <span data-ttu-id="96450-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="96450-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="96450-208">no</span><span class="sxs-lookup"><span data-stu-id="96450-208">no</span></span>             | <span data-ttu-id="96450-209">no</span><span class="sxs-lookup"><span data-stu-id="96450-209">no</span></span>               |
| <span data-ttu-id="96450-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="96450-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="96450-211">no</span><span class="sxs-lookup"><span data-stu-id="96450-211">no</span></span>             | <span data-ttu-id="96450-212">no</span><span class="sxs-lookup"><span data-stu-id="96450-212">no</span></span>               |
| <span data-ttu-id="96450-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="96450-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="96450-214">no</span><span class="sxs-lookup"><span data-stu-id="96450-214">no</span></span>             | <span data-ttu-id="96450-215">no</span><span class="sxs-lookup"><span data-stu-id="96450-215">no</span></span>               |
| <span data-ttu-id="96450-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="96450-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="96450-217">no</span><span class="sxs-lookup"><span data-stu-id="96450-217">no</span></span>             | <span data-ttu-id="96450-218">no</span><span class="sxs-lookup"><span data-stu-id="96450-218">no</span></span>               |
| <span data-ttu-id="96450-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="96450-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="96450-220">no</span><span class="sxs-lookup"><span data-stu-id="96450-220">no</span></span>             | <span data-ttu-id="96450-221">no</span><span class="sxs-lookup"><span data-stu-id="96450-221">no</span></span>               |
| <span data-ttu-id="96450-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="96450-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="96450-223">no</span><span class="sxs-lookup"><span data-stu-id="96450-223">no</span></span>             | <span data-ttu-id="96450-224">no</span><span class="sxs-lookup"><span data-stu-id="96450-224">no</span></span>               |
| <span data-ttu-id="96450-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="96450-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="96450-226">no</span><span class="sxs-lookup"><span data-stu-id="96450-226">no</span></span>             | <span data-ttu-id="96450-227">no</span><span class="sxs-lookup"><span data-stu-id="96450-227">no</span></span>               |
| <span data-ttu-id="96450-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="96450-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="96450-229">no</span><span class="sxs-lookup"><span data-stu-id="96450-229">no</span></span>             | <span data-ttu-id="96450-230">no</span><span class="sxs-lookup"><span data-stu-id="96450-230">no</span></span>               |
| <span data-ttu-id="96450-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="96450-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="96450-232">no</span><span class="sxs-lookup"><span data-stu-id="96450-232">no</span></span>             | <span data-ttu-id="96450-233">no</span><span class="sxs-lookup"><span data-stu-id="96450-233">no</span></span>               |
| <span data-ttu-id="96450-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="96450-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="96450-235">no</span><span class="sxs-lookup"><span data-stu-id="96450-235">no</span></span>             | <span data-ttu-id="96450-236">no</span><span class="sxs-lookup"><span data-stu-id="96450-236">no</span></span>               |
| <span data-ttu-id="96450-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="96450-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="96450-238">no</span><span class="sxs-lookup"><span data-stu-id="96450-238">no</span></span>             | <span data-ttu-id="96450-239">no</span><span class="sxs-lookup"><span data-stu-id="96450-239">no</span></span>               |
| <span data-ttu-id="96450-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="96450-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="96450-241">no</span><span class="sxs-lookup"><span data-stu-id="96450-241">no</span></span>             | <span data-ttu-id="96450-242">no</span><span class="sxs-lookup"><span data-stu-id="96450-242">no</span></span>               |
| <span data-ttu-id="96450-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="96450-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="96450-244">no</span><span class="sxs-lookup"><span data-stu-id="96450-244">no</span></span>             | <span data-ttu-id="96450-245">no</span><span class="sxs-lookup"><span data-stu-id="96450-245">no</span></span>               |
| <span data-ttu-id="96450-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="96450-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="96450-247">no</span><span class="sxs-lookup"><span data-stu-id="96450-247">no</span></span>             | <span data-ttu-id="96450-248">no</span><span class="sxs-lookup"><span data-stu-id="96450-248">no</span></span>               |
| <span data-ttu-id="96450-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="96450-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="96450-250">no</span><span class="sxs-lookup"><span data-stu-id="96450-250">no</span></span>             | <span data-ttu-id="96450-251">no</span><span class="sxs-lookup"><span data-stu-id="96450-251">no</span></span>               |
| <span data-ttu-id="96450-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="96450-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="96450-253">no</span><span class="sxs-lookup"><span data-stu-id="96450-253">no</span></span>             | <span data-ttu-id="96450-254">no</span><span class="sxs-lookup"><span data-stu-id="96450-254">no</span></span>               |
| <span data-ttu-id="96450-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="96450-256">no</span><span class="sxs-lookup"><span data-stu-id="96450-256">no</span></span>             | <span data-ttu-id="96450-257">no</span><span class="sxs-lookup"><span data-stu-id="96450-257">no</span></span>               |
| <span data-ttu-id="96450-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="96450-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="96450-259">no</span><span class="sxs-lookup"><span data-stu-id="96450-259">no</span></span>             | <span data-ttu-id="96450-260">no</span><span class="sxs-lookup"><span data-stu-id="96450-260">no</span></span>               |
| <span data-ttu-id="96450-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="96450-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="96450-262">no</span><span class="sxs-lookup"><span data-stu-id="96450-262">no</span></span>             | <span data-ttu-id="96450-263">no</span><span class="sxs-lookup"><span data-stu-id="96450-263">no</span></span>               |
| <span data-ttu-id="96450-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="96450-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="96450-265">no</span><span class="sxs-lookup"><span data-stu-id="96450-265">no</span></span>             | <span data-ttu-id="96450-266">no</span><span class="sxs-lookup"><span data-stu-id="96450-266">no</span></span>               |
| <span data-ttu-id="96450-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="96450-267">msdyn_progress</span></span>                         | <span data-ttu-id="96450-268">no</span><span class="sxs-lookup"><span data-stu-id="96450-268">no</span></span>             | <span data-ttu-id="96450-269">no (sí para P4W)</span><span class="sxs-lookup"><span data-stu-id="96450-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="96450-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="96450-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="96450-271">no</span><span class="sxs-lookup"><span data-stu-id="96450-271">no</span></span>             | <span data-ttu-id="96450-272">no</span><span class="sxs-lookup"><span data-stu-id="96450-272">no</span></span>               |
| <span data-ttu-id="96450-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="96450-274">no</span><span class="sxs-lookup"><span data-stu-id="96450-274">no</span></span>             | <span data-ttu-id="96450-275">no</span><span class="sxs-lookup"><span data-stu-id="96450-275">no</span></span>               |
| <span data-ttu-id="96450-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="96450-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="96450-277">no</span><span class="sxs-lookup"><span data-stu-id="96450-277">no</span></span>             | <span data-ttu-id="96450-278">no</span><span class="sxs-lookup"><span data-stu-id="96450-278">no</span></span>               |
| <span data-ttu-id="96450-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="96450-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="96450-280">no</span><span class="sxs-lookup"><span data-stu-id="96450-280">no</span></span>             | <span data-ttu-id="96450-281">no</span><span class="sxs-lookup"><span data-stu-id="96450-281">no</span></span>               |
| <span data-ttu-id="96450-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="96450-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="96450-283">no</span><span class="sxs-lookup"><span data-stu-id="96450-283">no</span></span>             | <span data-ttu-id="96450-284">no</span><span class="sxs-lookup"><span data-stu-id="96450-284">no</span></span>               |
| <span data-ttu-id="96450-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="96450-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="96450-286">no</span><span class="sxs-lookup"><span data-stu-id="96450-286">no</span></span>             | <span data-ttu-id="96450-287">no</span><span class="sxs-lookup"><span data-stu-id="96450-287">no</span></span>               |
| <span data-ttu-id="96450-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="96450-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="96450-289">no</span><span class="sxs-lookup"><span data-stu-id="96450-289">no</span></span>             | <span data-ttu-id="96450-290">no</span><span class="sxs-lookup"><span data-stu-id="96450-290">no</span></span>               |
| <span data-ttu-id="96450-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="96450-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="96450-292">no</span><span class="sxs-lookup"><span data-stu-id="96450-292">no</span></span>             | <span data-ttu-id="96450-293">no</span><span class="sxs-lookup"><span data-stu-id="96450-293">no</span></span>               |
| <span data-ttu-id="96450-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="96450-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="96450-295">no</span><span class="sxs-lookup"><span data-stu-id="96450-295">no</span></span>             | <span data-ttu-id="96450-296">no</span><span class="sxs-lookup"><span data-stu-id="96450-296">no</span></span>               |
| <span data-ttu-id="96450-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="96450-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="96450-298">no</span><span class="sxs-lookup"><span data-stu-id="96450-298">no</span></span>             | <span data-ttu-id="96450-299">no</span><span class="sxs-lookup"><span data-stu-id="96450-299">no</span></span>               |
| <span data-ttu-id="96450-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="96450-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="96450-301">no</span><span class="sxs-lookup"><span data-stu-id="96450-301">no</span></span>             | <span data-ttu-id="96450-302">no</span><span class="sxs-lookup"><span data-stu-id="96450-302">no</span></span>               |
| <span data-ttu-id="96450-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="96450-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="96450-304">no</span><span class="sxs-lookup"><span data-stu-id="96450-304">no</span></span>             | <span data-ttu-id="96450-305">no</span><span class="sxs-lookup"><span data-stu-id="96450-305">no</span></span>               |
| <span data-ttu-id="96450-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="96450-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="96450-307">no</span><span class="sxs-lookup"><span data-stu-id="96450-307">no</span></span>             | <span data-ttu-id="96450-308">no</span><span class="sxs-lookup"><span data-stu-id="96450-308">no</span></span>               |
| <span data-ttu-id="96450-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="96450-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="96450-310">no</span><span class="sxs-lookup"><span data-stu-id="96450-310">no</span></span>             | <span data-ttu-id="96450-311">no</span><span class="sxs-lookup"><span data-stu-id="96450-311">no</span></span>               |
| <span data-ttu-id="96450-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="96450-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="96450-313">no</span><span class="sxs-lookup"><span data-stu-id="96450-313">no</span></span>             | <span data-ttu-id="96450-314">no</span><span class="sxs-lookup"><span data-stu-id="96450-314">no</span></span>               |
| <span data-ttu-id="96450-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="96450-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="96450-316">no</span><span class="sxs-lookup"><span data-stu-id="96450-316">no</span></span>             | <span data-ttu-id="96450-317">no</span><span class="sxs-lookup"><span data-stu-id="96450-317">no</span></span>               |
| <span data-ttu-id="96450-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="96450-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="96450-319">no</span><span class="sxs-lookup"><span data-stu-id="96450-319">no</span></span>             | <span data-ttu-id="96450-320">no</span><span class="sxs-lookup"><span data-stu-id="96450-320">no</span></span>               |
| <span data-ttu-id="96450-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="96450-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="96450-322">no</span><span class="sxs-lookup"><span data-stu-id="96450-322">no</span></span>             | <span data-ttu-id="96450-323">no</span><span class="sxs-lookup"><span data-stu-id="96450-323">no</span></span>               |
| <span data-ttu-id="96450-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="96450-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="96450-325">no</span><span class="sxs-lookup"><span data-stu-id="96450-325">no</span></span>             | <span data-ttu-id="96450-326">no</span><span class="sxs-lookup"><span data-stu-id="96450-326">no</span></span>               |
| <span data-ttu-id="96450-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="96450-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="96450-328">no</span><span class="sxs-lookup"><span data-stu-id="96450-328">no</span></span>             | <span data-ttu-id="96450-329">no</span><span class="sxs-lookup"><span data-stu-id="96450-329">no</span></span>               |
| <span data-ttu-id="96450-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="96450-330">msdyn_summary</span></span>                          | <span data-ttu-id="96450-331">no</span><span class="sxs-lookup"><span data-stu-id="96450-331">no</span></span>             | <span data-ttu-id="96450-332">no</span><span class="sxs-lookup"><span data-stu-id="96450-332">no</span></span>               |
| <span data-ttu-id="96450-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="96450-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="96450-334">no</span><span class="sxs-lookup"><span data-stu-id="96450-334">no</span></span>             | <span data-ttu-id="96450-335">no</span><span class="sxs-lookup"><span data-stu-id="96450-335">no</span></span>               |
| <span data-ttu-id="96450-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="96450-337">no</span><span class="sxs-lookup"><span data-stu-id="96450-337">no</span></span>             | <span data-ttu-id="96450-338">no</span><span class="sxs-lookup"><span data-stu-id="96450-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="96450-339">Dependencia de tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-339">Project task dependency</span></span>

| <span data-ttu-id="96450-340">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="96450-340">**Logical name**</span></span>              | <span data-ttu-id="96450-341">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="96450-341">**Can create**</span></span> | <span data-ttu-id="96450-342">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="96450-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="96450-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="96450-343">msdyn_linktype</span></span>                | <span data-ttu-id="96450-344">no</span><span class="sxs-lookup"><span data-stu-id="96450-344">no</span></span>             | <span data-ttu-id="96450-345">no</span><span class="sxs-lookup"><span data-stu-id="96450-345">no</span></span>           |
| <span data-ttu-id="96450-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="96450-346">msdyn_linktypename</span></span>            | <span data-ttu-id="96450-347">no</span><span class="sxs-lookup"><span data-stu-id="96450-347">no</span></span>             | <span data-ttu-id="96450-348">no</span><span class="sxs-lookup"><span data-stu-id="96450-348">no</span></span>           |
| <span data-ttu-id="96450-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="96450-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="96450-350">sí</span><span class="sxs-lookup"><span data-stu-id="96450-350">yes</span></span>            | <span data-ttu-id="96450-351">no</span><span class="sxs-lookup"><span data-stu-id="96450-351">no</span></span>           |
| <span data-ttu-id="96450-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="96450-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="96450-353">sí</span><span class="sxs-lookup"><span data-stu-id="96450-353">yes</span></span>            | <span data-ttu-id="96450-354">no</span><span class="sxs-lookup"><span data-stu-id="96450-354">no</span></span>           |
| <span data-ttu-id="96450-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="96450-355">msdyn_project</span></span>                 | <span data-ttu-id="96450-356">sí</span><span class="sxs-lookup"><span data-stu-id="96450-356">yes</span></span>            | <span data-ttu-id="96450-357">no</span><span class="sxs-lookup"><span data-stu-id="96450-357">no</span></span>           |
| <span data-ttu-id="96450-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="96450-358">msdyn_projectname</span></span>             | <span data-ttu-id="96450-359">sí</span><span class="sxs-lookup"><span data-stu-id="96450-359">yes</span></span>            | <span data-ttu-id="96450-360">no</span><span class="sxs-lookup"><span data-stu-id="96450-360">no</span></span>           |
| <span data-ttu-id="96450-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="96450-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="96450-362">sí</span><span class="sxs-lookup"><span data-stu-id="96450-362">yes</span></span>            | <span data-ttu-id="96450-363">no</span><span class="sxs-lookup"><span data-stu-id="96450-363">no</span></span>           |
| <span data-ttu-id="96450-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="96450-364">msdyn_successortask</span></span>           | <span data-ttu-id="96450-365">sí</span><span class="sxs-lookup"><span data-stu-id="96450-365">yes</span></span>            | <span data-ttu-id="96450-366">no</span><span class="sxs-lookup"><span data-stu-id="96450-366">no</span></span>           |
| <span data-ttu-id="96450-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="96450-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="96450-368">sí</span><span class="sxs-lookup"><span data-stu-id="96450-368">yes</span></span>            | <span data-ttu-id="96450-369">no</span><span class="sxs-lookup"><span data-stu-id="96450-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="96450-370">Asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="96450-370">Resource assignment</span></span>

| <span data-ttu-id="96450-371">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="96450-371">**Logical name**</span></span>             | <span data-ttu-id="96450-372">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="96450-372">**Can create**</span></span> | <span data-ttu-id="96450-373">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="96450-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="96450-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="96450-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="96450-375">sí</span><span class="sxs-lookup"><span data-stu-id="96450-375">yes</span></span>            | <span data-ttu-id="96450-376">no</span><span class="sxs-lookup"><span data-stu-id="96450-376">no</span></span>           |
| <span data-ttu-id="96450-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="96450-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="96450-378">sí</span><span class="sxs-lookup"><span data-stu-id="96450-378">yes</span></span>            | <span data-ttu-id="96450-379">no</span><span class="sxs-lookup"><span data-stu-id="96450-379">no</span></span>           |
| <span data-ttu-id="96450-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="96450-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="96450-381">no</span><span class="sxs-lookup"><span data-stu-id="96450-381">no</span></span>             | <span data-ttu-id="96450-382">no</span><span class="sxs-lookup"><span data-stu-id="96450-382">no</span></span>           |
| <span data-ttu-id="96450-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="96450-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="96450-384">no</span><span class="sxs-lookup"><span data-stu-id="96450-384">no</span></span>             | <span data-ttu-id="96450-385">no</span><span class="sxs-lookup"><span data-stu-id="96450-385">no</span></span>           |
| <span data-ttu-id="96450-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="96450-386">msdyn_committype</span></span>             | <span data-ttu-id="96450-387">no</span><span class="sxs-lookup"><span data-stu-id="96450-387">no</span></span>             | <span data-ttu-id="96450-388">no</span><span class="sxs-lookup"><span data-stu-id="96450-388">no</span></span>           |
| <span data-ttu-id="96450-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="96450-389">msdyn_committypename</span></span>         | <span data-ttu-id="96450-390">no</span><span class="sxs-lookup"><span data-stu-id="96450-390">no</span></span>             | <span data-ttu-id="96450-391">no</span><span class="sxs-lookup"><span data-stu-id="96450-391">no</span></span>           |
| <span data-ttu-id="96450-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="96450-392">msdyn_effort</span></span>                 | <span data-ttu-id="96450-393">no</span><span class="sxs-lookup"><span data-stu-id="96450-393">no</span></span>             | <span data-ttu-id="96450-394">no</span><span class="sxs-lookup"><span data-stu-id="96450-394">no</span></span>           |
| <span data-ttu-id="96450-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="96450-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="96450-396">no</span><span class="sxs-lookup"><span data-stu-id="96450-396">no</span></span>             | <span data-ttu-id="96450-397">no</span><span class="sxs-lookup"><span data-stu-id="96450-397">no</span></span>           |
| <span data-ttu-id="96450-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="96450-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="96450-399">no</span><span class="sxs-lookup"><span data-stu-id="96450-399">no</span></span>             | <span data-ttu-id="96450-400">no</span><span class="sxs-lookup"><span data-stu-id="96450-400">no</span></span>           |
| <span data-ttu-id="96450-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="96450-401">msdyn_finish</span></span>                 | <span data-ttu-id="96450-402">no</span><span class="sxs-lookup"><span data-stu-id="96450-402">no</span></span>             | <span data-ttu-id="96450-403">no</span><span class="sxs-lookup"><span data-stu-id="96450-403">no</span></span>           |
| <span data-ttu-id="96450-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="96450-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="96450-405">no</span><span class="sxs-lookup"><span data-stu-id="96450-405">no</span></span>             | <span data-ttu-id="96450-406">no</span><span class="sxs-lookup"><span data-stu-id="96450-406">no</span></span>           |
| <span data-ttu-id="96450-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="96450-408">no</span><span class="sxs-lookup"><span data-stu-id="96450-408">no</span></span>             | <span data-ttu-id="96450-409">no</span><span class="sxs-lookup"><span data-stu-id="96450-409">no</span></span>           |
| <span data-ttu-id="96450-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="96450-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="96450-411">no</span><span class="sxs-lookup"><span data-stu-id="96450-411">no</span></span>             | <span data-ttu-id="96450-412">no</span><span class="sxs-lookup"><span data-stu-id="96450-412">no</span></span>           |
| <span data-ttu-id="96450-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="96450-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="96450-414">no</span><span class="sxs-lookup"><span data-stu-id="96450-414">no</span></span>             | <span data-ttu-id="96450-415">no</span><span class="sxs-lookup"><span data-stu-id="96450-415">no</span></span>           |
| <span data-ttu-id="96450-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="96450-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="96450-417">no</span><span class="sxs-lookup"><span data-stu-id="96450-417">no</span></span>             | <span data-ttu-id="96450-418">no</span><span class="sxs-lookup"><span data-stu-id="96450-418">no</span></span>           |
| <span data-ttu-id="96450-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="96450-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="96450-420">no</span><span class="sxs-lookup"><span data-stu-id="96450-420">no</span></span>             | <span data-ttu-id="96450-421">no</span><span class="sxs-lookup"><span data-stu-id="96450-421">no</span></span>           |
| <span data-ttu-id="96450-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="96450-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="96450-423">no</span><span class="sxs-lookup"><span data-stu-id="96450-423">no</span></span>             | <span data-ttu-id="96450-424">no</span><span class="sxs-lookup"><span data-stu-id="96450-424">no</span></span>           |
| <span data-ttu-id="96450-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="96450-425">msdyn_projectid</span></span>              | <span data-ttu-id="96450-426">sí</span><span class="sxs-lookup"><span data-stu-id="96450-426">yes</span></span>            | <span data-ttu-id="96450-427">no</span><span class="sxs-lookup"><span data-stu-id="96450-427">no</span></span>           |
| <span data-ttu-id="96450-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="96450-428">msdyn_projectidname</span></span>          | <span data-ttu-id="96450-429">no</span><span class="sxs-lookup"><span data-stu-id="96450-429">no</span></span>             | <span data-ttu-id="96450-430">no</span><span class="sxs-lookup"><span data-stu-id="96450-430">no</span></span>           |
| <span data-ttu-id="96450-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="96450-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="96450-432">no</span><span class="sxs-lookup"><span data-stu-id="96450-432">no</span></span>             | <span data-ttu-id="96450-433">no</span><span class="sxs-lookup"><span data-stu-id="96450-433">no</span></span>           |
| <span data-ttu-id="96450-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="96450-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="96450-435">no</span><span class="sxs-lookup"><span data-stu-id="96450-435">no</span></span>             | <span data-ttu-id="96450-436">no</span><span class="sxs-lookup"><span data-stu-id="96450-436">no</span></span>           |
| <span data-ttu-id="96450-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="96450-437">msdyn_start</span></span>                  | <span data-ttu-id="96450-438">no</span><span class="sxs-lookup"><span data-stu-id="96450-438">no</span></span>             | <span data-ttu-id="96450-439">no</span><span class="sxs-lookup"><span data-stu-id="96450-439">no</span></span>           |
| <span data-ttu-id="96450-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="96450-440">msdyn_taskid</span></span>                 | <span data-ttu-id="96450-441">no</span><span class="sxs-lookup"><span data-stu-id="96450-441">no</span></span>             | <span data-ttu-id="96450-442">no</span><span class="sxs-lookup"><span data-stu-id="96450-442">no</span></span>           |
| <span data-ttu-id="96450-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="96450-443">msdyn_taskidname</span></span>             | <span data-ttu-id="96450-444">no</span><span class="sxs-lookup"><span data-stu-id="96450-444">no</span></span>             | <span data-ttu-id="96450-445">no</span><span class="sxs-lookup"><span data-stu-id="96450-445">no</span></span>           |
| <span data-ttu-id="96450-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="96450-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="96450-447">no</span><span class="sxs-lookup"><span data-stu-id="96450-447">no</span></span>             | <span data-ttu-id="96450-448">no</span><span class="sxs-lookup"><span data-stu-id="96450-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="96450-449">Miembro del equipo del proyecto</span><span class="sxs-lookup"><span data-stu-id="96450-449">Project team member</span></span>

| <span data-ttu-id="96450-450">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="96450-450">**Logical name**</span></span>                                 | <span data-ttu-id="96450-451">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="96450-451">**Can create**</span></span> | <span data-ttu-id="96450-452">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="96450-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="96450-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="96450-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="96450-454">no</span><span class="sxs-lookup"><span data-stu-id="96450-454">no</span></span>             | <span data-ttu-id="96450-455">no</span><span class="sxs-lookup"><span data-stu-id="96450-455">no</span></span>           |
| <span data-ttu-id="96450-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="96450-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="96450-457">no</span><span class="sxs-lookup"><span data-stu-id="96450-457">no</span></span>             | <span data-ttu-id="96450-458">no</span><span class="sxs-lookup"><span data-stu-id="96450-458">no</span></span>           |
| <span data-ttu-id="96450-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="96450-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="96450-460">no</span><span class="sxs-lookup"><span data-stu-id="96450-460">no</span></span>             | <span data-ttu-id="96450-461">no</span><span class="sxs-lookup"><span data-stu-id="96450-461">no</span></span>           |
| <span data-ttu-id="96450-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="96450-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="96450-463">no</span><span class="sxs-lookup"><span data-stu-id="96450-463">no</span></span>             | <span data-ttu-id="96450-464">no</span><span class="sxs-lookup"><span data-stu-id="96450-464">no</span></span>           |
| <span data-ttu-id="96450-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="96450-465">msdyn_effort</span></span>                                     | <span data-ttu-id="96450-466">no</span><span class="sxs-lookup"><span data-stu-id="96450-466">no</span></span>             | <span data-ttu-id="96450-467">no</span><span class="sxs-lookup"><span data-stu-id="96450-467">no</span></span>           |
| <span data-ttu-id="96450-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="96450-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="96450-469">no</span><span class="sxs-lookup"><span data-stu-id="96450-469">no</span></span>             | <span data-ttu-id="96450-470">no</span><span class="sxs-lookup"><span data-stu-id="96450-470">no</span></span>           |
| <span data-ttu-id="96450-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="96450-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="96450-472">no</span><span class="sxs-lookup"><span data-stu-id="96450-472">no</span></span>             | <span data-ttu-id="96450-473">no</span><span class="sxs-lookup"><span data-stu-id="96450-473">no</span></span>           |
| <span data-ttu-id="96450-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="96450-474">msdyn_finish</span></span>                                     | <span data-ttu-id="96450-475">no</span><span class="sxs-lookup"><span data-stu-id="96450-475">no</span></span>             | <span data-ttu-id="96450-476">no</span><span class="sxs-lookup"><span data-stu-id="96450-476">no</span></span>           |
| <span data-ttu-id="96450-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="96450-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="96450-478">no</span><span class="sxs-lookup"><span data-stu-id="96450-478">no</span></span>             | <span data-ttu-id="96450-479">no</span><span class="sxs-lookup"><span data-stu-id="96450-479">no</span></span>           |
| <span data-ttu-id="96450-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="96450-480">msdyn_hours</span></span>                                      | <span data-ttu-id="96450-481">no</span><span class="sxs-lookup"><span data-stu-id="96450-481">no</span></span>             | <span data-ttu-id="96450-482">no</span><span class="sxs-lookup"><span data-stu-id="96450-482">no</span></span>           |
| <span data-ttu-id="96450-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="96450-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="96450-484">no</span><span class="sxs-lookup"><span data-stu-id="96450-484">no</span></span>             | <span data-ttu-id="96450-485">no</span><span class="sxs-lookup"><span data-stu-id="96450-485">no</span></span>           |
| <span data-ttu-id="96450-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="96450-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="96450-487">no</span><span class="sxs-lookup"><span data-stu-id="96450-487">no</span></span>             | <span data-ttu-id="96450-488">no</span><span class="sxs-lookup"><span data-stu-id="96450-488">no</span></span>           |
| <span data-ttu-id="96450-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="96450-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="96450-490">no</span><span class="sxs-lookup"><span data-stu-id="96450-490">no</span></span>             | <span data-ttu-id="96450-491">no</span><span class="sxs-lookup"><span data-stu-id="96450-491">no</span></span>           |
| <span data-ttu-id="96450-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="96450-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="96450-493">no</span><span class="sxs-lookup"><span data-stu-id="96450-493">no</span></span>             | <span data-ttu-id="96450-494">no</span><span class="sxs-lookup"><span data-stu-id="96450-494">no</span></span>           |
| <span data-ttu-id="96450-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="96450-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="96450-496">no</span><span class="sxs-lookup"><span data-stu-id="96450-496">no</span></span>             | <span data-ttu-id="96450-497">no</span><span class="sxs-lookup"><span data-stu-id="96450-497">no</span></span>           |
| <span data-ttu-id="96450-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="96450-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="96450-499">no</span><span class="sxs-lookup"><span data-stu-id="96450-499">no</span></span>             | <span data-ttu-id="96450-500">no</span><span class="sxs-lookup"><span data-stu-id="96450-500">no</span></span>           |
| <span data-ttu-id="96450-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="96450-501">msdyn_start</span></span>                                      | <span data-ttu-id="96450-502">no</span><span class="sxs-lookup"><span data-stu-id="96450-502">no</span></span>             | <span data-ttu-id="96450-503">no</span><span class="sxs-lookup"><span data-stu-id="96450-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="96450-504">Project</span><span class="sxs-lookup"><span data-stu-id="96450-504">Project</span></span>

| <span data-ttu-id="96450-505">**Nombre lógico**</span><span class="sxs-lookup"><span data-stu-id="96450-505">**Logical name**</span></span>                       | <span data-ttu-id="96450-506">**Puede crear**</span><span class="sxs-lookup"><span data-stu-id="96450-506">**Can create**</span></span> | <span data-ttu-id="96450-507">**Puede editar**</span><span class="sxs-lookup"><span data-stu-id="96450-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="96450-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="96450-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="96450-509">no</span><span class="sxs-lookup"><span data-stu-id="96450-509">no</span></span>             | <span data-ttu-id="96450-510">no</span><span class="sxs-lookup"><span data-stu-id="96450-510">no</span></span>           |
| <span data-ttu-id="96450-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="96450-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="96450-512">no</span><span class="sxs-lookup"><span data-stu-id="96450-512">no</span></span>             | <span data-ttu-id="96450-513">no</span><span class="sxs-lookup"><span data-stu-id="96450-513">no</span></span>           |
| <span data-ttu-id="96450-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="96450-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="96450-515">no</span><span class="sxs-lookup"><span data-stu-id="96450-515">no</span></span>             | <span data-ttu-id="96450-516">no</span><span class="sxs-lookup"><span data-stu-id="96450-516">no</span></span>           |
| <span data-ttu-id="96450-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="96450-518">no</span><span class="sxs-lookup"><span data-stu-id="96450-518">no</span></span>             | <span data-ttu-id="96450-519">no</span><span class="sxs-lookup"><span data-stu-id="96450-519">no</span></span>           |
| <span data-ttu-id="96450-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="96450-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="96450-521">no</span><span class="sxs-lookup"><span data-stu-id="96450-521">no</span></span>             | <span data-ttu-id="96450-522">no</span><span class="sxs-lookup"><span data-stu-id="96450-522">no</span></span>           |
| <span data-ttu-id="96450-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="96450-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="96450-524">no</span><span class="sxs-lookup"><span data-stu-id="96450-524">no</span></span>             | <span data-ttu-id="96450-525">no</span><span class="sxs-lookup"><span data-stu-id="96450-525">no</span></span>           |
| <span data-ttu-id="96450-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="96450-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="96450-527">sí</span><span class="sxs-lookup"><span data-stu-id="96450-527">yes</span></span>            | <span data-ttu-id="96450-528">no</span><span class="sxs-lookup"><span data-stu-id="96450-528">no</span></span>           |
| <span data-ttu-id="96450-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="96450-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="96450-530">sí</span><span class="sxs-lookup"><span data-stu-id="96450-530">yes</span></span>            | <span data-ttu-id="96450-531">no</span><span class="sxs-lookup"><span data-stu-id="96450-531">no</span></span>           |
| <span data-ttu-id="96450-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="96450-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="96450-533">sí</span><span class="sxs-lookup"><span data-stu-id="96450-533">yes</span></span>            | <span data-ttu-id="96450-534">no</span><span class="sxs-lookup"><span data-stu-id="96450-534">no</span></span>           |
| <span data-ttu-id="96450-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="96450-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="96450-536">no</span><span class="sxs-lookup"><span data-stu-id="96450-536">no</span></span>             | <span data-ttu-id="96450-537">no</span><span class="sxs-lookup"><span data-stu-id="96450-537">no</span></span>           |
| <span data-ttu-id="96450-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="96450-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="96450-539">no</span><span class="sxs-lookup"><span data-stu-id="96450-539">no</span></span>             | <span data-ttu-id="96450-540">no</span><span class="sxs-lookup"><span data-stu-id="96450-540">no</span></span>           |
| <span data-ttu-id="96450-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="96450-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="96450-542">no</span><span class="sxs-lookup"><span data-stu-id="96450-542">no</span></span>             | <span data-ttu-id="96450-543">no</span><span class="sxs-lookup"><span data-stu-id="96450-543">no</span></span>           |
| <span data-ttu-id="96450-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="96450-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="96450-545">no</span><span class="sxs-lookup"><span data-stu-id="96450-545">no</span></span>             | <span data-ttu-id="96450-546">no</span><span class="sxs-lookup"><span data-stu-id="96450-546">no</span></span>           |
| <span data-ttu-id="96450-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="96450-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="96450-548">no</span><span class="sxs-lookup"><span data-stu-id="96450-548">no</span></span>             | <span data-ttu-id="96450-549">no</span><span class="sxs-lookup"><span data-stu-id="96450-549">no</span></span>           |
| <span data-ttu-id="96450-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="96450-550">msdyn_duration</span></span>                         | <span data-ttu-id="96450-551">no</span><span class="sxs-lookup"><span data-stu-id="96450-551">no</span></span>             | <span data-ttu-id="96450-552">no</span><span class="sxs-lookup"><span data-stu-id="96450-552">no</span></span>           |
| <span data-ttu-id="96450-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="96450-553">msdyn_effort</span></span>                           | <span data-ttu-id="96450-554">no</span><span class="sxs-lookup"><span data-stu-id="96450-554">no</span></span>             | <span data-ttu-id="96450-555">no</span><span class="sxs-lookup"><span data-stu-id="96450-555">no</span></span>           |
| <span data-ttu-id="96450-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="96450-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="96450-557">no</span><span class="sxs-lookup"><span data-stu-id="96450-557">no</span></span>             | <span data-ttu-id="96450-558">no</span><span class="sxs-lookup"><span data-stu-id="96450-558">no</span></span>           |
| <span data-ttu-id="96450-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="96450-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="96450-560">no</span><span class="sxs-lookup"><span data-stu-id="96450-560">no</span></span>             | <span data-ttu-id="96450-561">no</span><span class="sxs-lookup"><span data-stu-id="96450-561">no</span></span>           |
| <span data-ttu-id="96450-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="96450-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="96450-563">no</span><span class="sxs-lookup"><span data-stu-id="96450-563">no</span></span>             | <span data-ttu-id="96450-564">no</span><span class="sxs-lookup"><span data-stu-id="96450-564">no</span></span>           |
| <span data-ttu-id="96450-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="96450-565">msdyn_finish</span></span>                           | <span data-ttu-id="96450-566">sí</span><span class="sxs-lookup"><span data-stu-id="96450-566">yes</span></span>            | <span data-ttu-id="96450-567">sí</span><span class="sxs-lookup"><span data-stu-id="96450-567">yes</span></span>          |
| <span data-ttu-id="96450-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="96450-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="96450-569">no</span><span class="sxs-lookup"><span data-stu-id="96450-569">no</span></span>             | <span data-ttu-id="96450-570">no</span><span class="sxs-lookup"><span data-stu-id="96450-570">no</span></span>           |
| <span data-ttu-id="96450-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="96450-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="96450-572">no</span><span class="sxs-lookup"><span data-stu-id="96450-572">no</span></span>             | <span data-ttu-id="96450-573">no</span><span class="sxs-lookup"><span data-stu-id="96450-573">no</span></span>           |
| <span data-ttu-id="96450-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="96450-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="96450-575">no</span><span class="sxs-lookup"><span data-stu-id="96450-575">no</span></span>             | <span data-ttu-id="96450-576">no</span><span class="sxs-lookup"><span data-stu-id="96450-576">no</span></span>           |
| <span data-ttu-id="96450-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="96450-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="96450-578">no</span><span class="sxs-lookup"><span data-stu-id="96450-578">no</span></span>             | <span data-ttu-id="96450-579">no</span><span class="sxs-lookup"><span data-stu-id="96450-579">no</span></span>           |
| <span data-ttu-id="96450-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="96450-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="96450-581">no</span><span class="sxs-lookup"><span data-stu-id="96450-581">no</span></span>             | <span data-ttu-id="96450-582">no</span><span class="sxs-lookup"><span data-stu-id="96450-582">no</span></span>           |
| <span data-ttu-id="96450-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="96450-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="96450-584">no</span><span class="sxs-lookup"><span data-stu-id="96450-584">no</span></span>             | <span data-ttu-id="96450-585">no</span><span class="sxs-lookup"><span data-stu-id="96450-585">no</span></span>           |
| <span data-ttu-id="96450-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="96450-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="96450-587">no</span><span class="sxs-lookup"><span data-stu-id="96450-587">no</span></span>             | <span data-ttu-id="96450-588">no</span><span class="sxs-lookup"><span data-stu-id="96450-588">no</span></span>           |
| <span data-ttu-id="96450-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="96450-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="96450-590">no</span><span class="sxs-lookup"><span data-stu-id="96450-590">no</span></span>             | <span data-ttu-id="96450-591">no</span><span class="sxs-lookup"><span data-stu-id="96450-591">no</span></span>           |
| <span data-ttu-id="96450-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="96450-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="96450-593">no</span><span class="sxs-lookup"><span data-stu-id="96450-593">no</span></span>             | <span data-ttu-id="96450-594">no</span><span class="sxs-lookup"><span data-stu-id="96450-594">no</span></span>           |
| <span data-ttu-id="96450-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="96450-596">no</span><span class="sxs-lookup"><span data-stu-id="96450-596">no</span></span>             | <span data-ttu-id="96450-597">no</span><span class="sxs-lookup"><span data-stu-id="96450-597">no</span></span>           |
| <span data-ttu-id="96450-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="96450-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="96450-599">no</span><span class="sxs-lookup"><span data-stu-id="96450-599">no</span></span>             | <span data-ttu-id="96450-600">no</span><span class="sxs-lookup"><span data-stu-id="96450-600">no</span></span>           |
| <span data-ttu-id="96450-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="96450-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="96450-602">no</span><span class="sxs-lookup"><span data-stu-id="96450-602">no</span></span>             | <span data-ttu-id="96450-603">no</span><span class="sxs-lookup"><span data-stu-id="96450-603">no</span></span>           |
| <span data-ttu-id="96450-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="96450-604">msdyn_progress</span></span>                         | <span data-ttu-id="96450-605">no</span><span class="sxs-lookup"><span data-stu-id="96450-605">no</span></span>             | <span data-ttu-id="96450-606">no</span><span class="sxs-lookup"><span data-stu-id="96450-606">no</span></span>           |
| <span data-ttu-id="96450-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="96450-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="96450-608">no</span><span class="sxs-lookup"><span data-stu-id="96450-608">no</span></span>             | <span data-ttu-id="96450-609">no</span><span class="sxs-lookup"><span data-stu-id="96450-609">no</span></span>           |
| <span data-ttu-id="96450-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="96450-611">no</span><span class="sxs-lookup"><span data-stu-id="96450-611">no</span></span>             | <span data-ttu-id="96450-612">no</span><span class="sxs-lookup"><span data-stu-id="96450-612">no</span></span>           |
| <span data-ttu-id="96450-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="96450-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="96450-614">no</span><span class="sxs-lookup"><span data-stu-id="96450-614">no</span></span>             | <span data-ttu-id="96450-615">no</span><span class="sxs-lookup"><span data-stu-id="96450-615">no</span></span>           |
| <span data-ttu-id="96450-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="96450-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="96450-617">no</span><span class="sxs-lookup"><span data-stu-id="96450-617">no</span></span>             | <span data-ttu-id="96450-618">no</span><span class="sxs-lookup"><span data-stu-id="96450-618">no</span></span>           |
| <span data-ttu-id="96450-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="96450-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="96450-620">no</span><span class="sxs-lookup"><span data-stu-id="96450-620">no</span></span>             | <span data-ttu-id="96450-621">no</span><span class="sxs-lookup"><span data-stu-id="96450-621">no</span></span>           |
| <span data-ttu-id="96450-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="96450-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="96450-623">no</span><span class="sxs-lookup"><span data-stu-id="96450-623">no</span></span>             | <span data-ttu-id="96450-624">no</span><span class="sxs-lookup"><span data-stu-id="96450-624">no</span></span>           |
| <span data-ttu-id="96450-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="96450-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="96450-626">no</span><span class="sxs-lookup"><span data-stu-id="96450-626">no</span></span>             | <span data-ttu-id="96450-627">no</span><span class="sxs-lookup"><span data-stu-id="96450-627">no</span></span>           |
| <span data-ttu-id="96450-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="96450-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="96450-629">no</span><span class="sxs-lookup"><span data-stu-id="96450-629">no</span></span>             | <span data-ttu-id="96450-630">no</span><span class="sxs-lookup"><span data-stu-id="96450-630">no</span></span>           |
| <span data-ttu-id="96450-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="96450-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="96450-632">no</span><span class="sxs-lookup"><span data-stu-id="96450-632">no</span></span>             | <span data-ttu-id="96450-633">no</span><span class="sxs-lookup"><span data-stu-id="96450-633">no</span></span>           |
| <span data-ttu-id="96450-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="96450-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="96450-635">no</span><span class="sxs-lookup"><span data-stu-id="96450-635">no</span></span>             | <span data-ttu-id="96450-636">no</span><span class="sxs-lookup"><span data-stu-id="96450-636">no</span></span>           |
| <span data-ttu-id="96450-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="96450-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="96450-638">no</span><span class="sxs-lookup"><span data-stu-id="96450-638">no</span></span>             | <span data-ttu-id="96450-639">no</span><span class="sxs-lookup"><span data-stu-id="96450-639">no</span></span>           |
| <span data-ttu-id="96450-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="96450-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="96450-641">no</span><span class="sxs-lookup"><span data-stu-id="96450-641">no</span></span>             | <span data-ttu-id="96450-642">no</span><span class="sxs-lookup"><span data-stu-id="96450-642">no</span></span>           |
| <span data-ttu-id="96450-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="96450-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="96450-644">no</span><span class="sxs-lookup"><span data-stu-id="96450-644">no</span></span>             | <span data-ttu-id="96450-645">no</span><span class="sxs-lookup"><span data-stu-id="96450-645">no</span></span>           |
| <span data-ttu-id="96450-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="96450-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="96450-647">no</span><span class="sxs-lookup"><span data-stu-id="96450-647">no</span></span>             | <span data-ttu-id="96450-648">no</span><span class="sxs-lookup"><span data-stu-id="96450-648">no</span></span>           |
| <span data-ttu-id="96450-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="96450-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="96450-650">no</span><span class="sxs-lookup"><span data-stu-id="96450-650">no</span></span>             | <span data-ttu-id="96450-651">no</span><span class="sxs-lookup"><span data-stu-id="96450-651">no</span></span>           |
| <span data-ttu-id="96450-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="96450-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="96450-653">no</span><span class="sxs-lookup"><span data-stu-id="96450-653">no</span></span>             | <span data-ttu-id="96450-654">no</span><span class="sxs-lookup"><span data-stu-id="96450-654">no</span></span>           |
| <span data-ttu-id="96450-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="96450-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="96450-656">no</span><span class="sxs-lookup"><span data-stu-id="96450-656">no</span></span>             | <span data-ttu-id="96450-657">no</span><span class="sxs-lookup"><span data-stu-id="96450-657">no</span></span>           |
| <span data-ttu-id="96450-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="96450-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="96450-659">no</span><span class="sxs-lookup"><span data-stu-id="96450-659">no</span></span>             | <span data-ttu-id="96450-660">no</span><span class="sxs-lookup"><span data-stu-id="96450-660">no</span></span>           |
| <span data-ttu-id="96450-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="96450-662">no</span><span class="sxs-lookup"><span data-stu-id="96450-662">no</span></span>             | <span data-ttu-id="96450-663">no</span><span class="sxs-lookup"><span data-stu-id="96450-663">no</span></span>           |
| <span data-ttu-id="96450-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="96450-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="96450-665">no</span><span class="sxs-lookup"><span data-stu-id="96450-665">no</span></span>             | <span data-ttu-id="96450-666">no</span><span class="sxs-lookup"><span data-stu-id="96450-666">no</span></span>           |
| <span data-ttu-id="96450-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="96450-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="96450-668">no</span><span class="sxs-lookup"><span data-stu-id="96450-668">no</span></span>             | <span data-ttu-id="96450-669">no</span><span class="sxs-lookup"><span data-stu-id="96450-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="96450-670">Limitaciones y problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="96450-670">Limitations and known issues</span></span>
<span data-ttu-id="96450-671">La siguiente es una lista de limitaciones y problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="96450-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="96450-672">Las API de programación del proyecto solo pueden ser utilizadas por **Usuarios con licencia de Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="96450-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="96450-673">No pueden ser utilizadas por:</span><span class="sxs-lookup"><span data-stu-id="96450-673">They can't be used by:</span></span>
    - <span data-ttu-id="96450-674">Usuarios de la aplicación</span><span class="sxs-lookup"><span data-stu-id="96450-674">Application users</span></span>
    - <span data-ttu-id="96450-675">Usuarios de sistema</span><span class="sxs-lookup"><span data-stu-id="96450-675">System users</span></span>
    - <span data-ttu-id="96450-676">Usuarios de integración</span><span class="sxs-lookup"><span data-stu-id="96450-676">Integration users</span></span>
    - <span data-ttu-id="96450-677">Otros usuarios que no tienen la licencia requerida</span><span class="sxs-lookup"><span data-stu-id="96450-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="96450-678">Cada **OperationSet** solo puede tener un máximo de 100 operaciones.</span><span class="sxs-lookup"><span data-stu-id="96450-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="96450-679">Cada usuario solo puede tener un máximo de 10 operaciones **OperationSet** abiertas.</span><span class="sxs-lookup"><span data-stu-id="96450-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="96450-680">Project Operations actualmente admiten un máximo de 500 tareas en total en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="96450-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="96450-681">El estado de error y los registros de error de **OperationSet** no están disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="96450-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="96450-682">Límites y límites en proyectos y tareas</span><span class="sxs-lookup"><span data-stu-id="96450-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="96450-683">Control de errores</span><span class="sxs-lookup"><span data-stu-id="96450-683">Error handling</span></span>

   - <span data-ttu-id="96450-684">Para revisar los errores generados por los conjuntos de operaciones, vaya a **Configuración** \> **Integración de programación** \> **Conjuntos de operaciones**.</span><span class="sxs-lookup"><span data-stu-id="96450-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="96450-685">Para revisar los errores generados por el servicio de programación de proyectos, vaya a **Ajustes** \> **Integración de programación** \> **Registros de errores de PSS**.</span><span class="sxs-lookup"><span data-stu-id="96450-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="96450-686">Escenario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="96450-686">Sample scenario</span></span>

<span data-ttu-id="96450-687">En este escenario, creará un proyecto, un miembro del equipo, cuatro tareas y dos asignaciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="96450-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="96450-688">A continuación, actualizará una tarea, actualizará el proyecto, eliminará una tarea, eliminará una asignación de recursos y creará una dependencia de tareas.</span><span class="sxs-lookup"><span data-stu-id="96450-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="96450-689">Ejemplos adicionales</span><span class="sxs-lookup"><span data-stu-id="96450-689">Additional samples</span></span>

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
