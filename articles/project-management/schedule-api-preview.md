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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilizar las API de programación para realizar operaciones con entidades de programación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

> [!IMPORTANT] 
> Parte o toda la funcionalidad que se menciona en este tema está disponible como parte de una versión preliminar. El contenido y la funcionalidad están sujetos a cambios. 

## <a name="scheduling-entities"></a>Entidades de programación

Las API de programación brindan la capacidad de realizar operaciones de creación, actualización y eliminación con **Entidades de programación**. Estas entidades se administran a través del motor de programación en Project para la web. Crear, actualizar y eliminar operaciones con **Entidades de programación** estaba restringido en versiones anteriores de Dynamics 365 Project Operations.

La siguiente tabla proporciona una lista completa de las **Entidades de programación**.

| Nombre de entidad  | Nombre lógico de la entidad |
| --- | --- |
| Project | msdyn_project |
| Tarea de proyecto  | msdyn_projecttask  |
| Dependencia de tareas de proyecto  | msdyn_projecttaskdependency  |
| Asignación de recursos | msdyn_resourceassignment |
| Cubo de proyecto  | msdyn_projectbucket |
| Miembro del equipo del proyecto | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet es un patrón de unidad de trabajo que se puede usar cuando se deben procesar varias solicitudes que afectan la programación dentro de una transacción.

## <a name="schedule-apis"></a>Programar las API

La siguiente es una lista de las API de programación actuales.

- **msdyn_CreateProjectV1**: esta API se puede utilizar para crear un proyecto. El proyecto y el cubo del proyecto predeterminado se crean inmediatamente.
- **msdyn_CreateTeamMemberV1**: esta API se puede utilizar para crear un miembro de equipo del proyecto. El registro de miembro del equipo se crea inmediatamente.
- **msdyn_CreateOperationSetV1**: esta API se puede utilizar para programar varias solicitudes que deben realizarse dentro de una transacción.
- **msdyn_PSSCreateV1**: esta API se puede utilizar para crear una entidad. La entidad puede ser cualquiera de las entidades de programación que admiten la operación de creación.
- **msdyn_PSSUpdateV1**: esta API se puede utilizar para actualizar una entidad. La entidad puede ser cualquiera de las entidades de programación que admiten la operación de actualización.
- **msdyn_PSSDeleteV1**: esta API se puede utilizar para eliminar una entidad. La entidad puede ser cualquiera de las entidades de programación que admiten la operación de eliminación.
- **msdyn_ExecuteOperationSetV1**: esta API se utiliza para ejecutar todas las operaciones dentro del conjunto de operaciones establecido.

## <a name="using-schedule-apis-with-operationset"></a>Utilizar las API de programación con OperationSet

Porque los registros con ambos **CreateProjectV1** y **CreateTeamMemberV1** se crean inmediatamente, estas API no se pueden utilizar en **OperationSet** directamente. Sin embargo, puede utilizar la API para crear los registros necesarios, crear un **OperationSet** y, a continuación, utilizar estos registros creados previamente en **OperationSet**.

## <a name="supported-operations"></a>Operaciones admitidas

| Entidades de programación | Crear | Actualización | Delete | Consideraciones importantes |
| --- | --- | --- | --- | --- |
Tarea de proyecto | Sí | Sí | Sí | Nada |
| Dependencia de tareas de proyecto | Sí | Sí | | Los registros de dependencia de tareas del proyecto no se actualizan. En su lugar, se puede eliminar un registro antiguo y se puede crear un registro nuevo. |
| Asignación de recursos | Sí | Sí | | No se admiten las operaciones con los siguientes campos: **BookableResourceID**, **Esfuerzo**, **EffortCompleted**, **EffortCompleted** y **PlannedWork**. Los registros de asignación de recursos no se actualizan. En su lugar, se puede eliminar el registro antiguo y se puede crear un registro nuevo. |
| Cubo de proyecto | N/D | N/D | N/D | El cubo predeterminado se crea utilizando la API **CreateProjectV1**. |
| Miembro del equipo del proyecto | Sí | Sí | Sí | Para la operación de creación, use la API **CreateTeamMemberV1**. |
| Project | Sí | Sí | N/D | No se admiten operaciones con los siguientes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esfuerzo**, **EffortCompleted**, **EffortRemaining**, **Progreso**, **Terminar**, **TaskEarliestStart**, y **Duración**. |

Estas API se pueden llamar con objetos de entidad que incluyen campos personalizados.

La propiedad del identificador es opcional. Si se proporciona, el sistema intenta usarlo y lanza una excepción si no se puede usar. Si no se proporciona, el sistema lo generará.

## <a name="restricted-fields"></a>Campos restringidos

Las siguientes tablas definen los campos que están restringidos para **Crear** y **Editar.**

### <a name="project-task"></a>Tarea de proyecto

| **Nombre lógico**                       | **Puede crear** | **Puede editar**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | no             | no               |
| msdyn_actualcost_base                  | no             | no               |
| msdyn_actualend                        | no             | no               |
| msdyn_actualsales                      | no             | no               |
| msdyn_actualsales_base                 | no             | no               |
| msdyn_actualstart                      | no             | no               |
| msdyn_costatcompleteestimate           | no             | no               |
| msdyn_costatcompleteestimate_base      | no             | no               |
| msdyn_costconsumptionpercentage        | no             | no               |
| msdyn_effortcompleted                  | no             | no               |
| msdyn_effortestimateatcomplete         | no             | no               |
| msdyn_iscritical                       | no             | no               |
| msdyn_iscriticalname                   | no             | no               |
| msdyn_ismanual                         | no             | no               |
| msdyn_ismanualname                     | no             | no               |
| msdyn_ismilestone                      | no             | no               |
| msdyn_ismilestonename                  | no             | no               |
| msdyn_LinkStatus                       | no             | no               |
| msdyn_linkstatusname                   | no             | no               |
| msdyn_msprojectclientid                | no             | no               |
| msdyn_plannedcost                      | no             | no               |
| msdyn_plannedcost_base                 | no             | no               |
| msdyn_plannedsales                     | no             | no               |
| msdyn_plannedsales_base                | no             | no               |
| msdyn_pluginprocessingdata             | no             | no               |
| msdyn_progress                         | no             | no (sí para P4W) |
| msdyn_remainingcost                    | no             | no               |
| msdyn_remainingcost_base               | no             | no               |
| msdyn_remainingsales                   | no             | no               |
| msdyn_remainingsales_base              | no             | no               |
| msdyn_requestedhours                   | no             | no               |
| msdyn_resourcecategory                 | no             | no               |
| msdyn_resourcecategoryname             | no             | no               |
| msdyn_resourceorganizationalunitid     | no             | no               |
| msdyn_resourceorganizationalunitidname | no             | no               |
| msdyn_salesconsumptionpercentage       | no             | no               |
| msdyn_salesestimateatcomplete          | no             | no               |
| msdyn_salesestimateatcomplete_base     | no             | no               |
| msdyn_salesvariance                    | no             | no               |
| msdyn_salesvariance_base               | no             | no               |
| msdyn_scheduleddurationminutes         | no             | no               |
| msdyn_scheduledend                     | no             | no               |
| msdyn_scheduledstart                   | no             | no               |
| msdyn_schedulevariance                 | no             | no               |
| msdyn_skipupdateestimateline           | no             | no               |
| msdyn_skipupdateestimatelinename       | no             | no               |
| msdyn_summary                          | no             | no               |
| msdyn_varianceofcost                   | no             | no               |
| msdyn_varianceofcost_base              | no             | no               |

### <a name="project-task-dependency"></a>Dependencia de tareas de proyecto

| **Nombre lógico**              | **Puede crear** | **Puede editar** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | no             | no           |
| msdyn_linktypename            | no             | no           |
| msdyn_predecessortask         | sí            | no           |
| msdyn_predecessortaskname     | sí            | no           |
| msdyn_project                 | sí            | no           |
| msdyn_projectname             | sí            | no           |
| msdyn_projecttaskdependencyid | sí            | no           |
| msdyn_successortask           | sí            | no           |
| msdyn_successortaskname       | sí            | no           |

### <a name="resource-assignment"></a>Asignación de recursos

| **Nombre lógico**             | **Puede crear** | **Puede editar** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | sí            | no           |
| msdyn_bookableresourceidname | sí            | no           |
| msdyn_bookingstatusid        | no             | no           |
| msdyn_bookingstatusidname    | no             | no           |
| msdyn_committype             | no             | no           |
| msdyn_committypename         | no             | no           |
| msdyn_effort                 | no             | no           |
| msdyn_effortcompleted        | no             | no           |
| msdyn_effortremaining        | no             | no           |
| msdyn_finish                 | no             | no           |
| msdyn_plannedcost            | no             | no           |
| msdyn_plannedcost_base       | no             | no           |
| msdyn_plannedcostcontour     | no             | no           |
| msdyn_plannedsales           | no             | no           |
| msdyn_plannedsales_base      | no             | no           |
| msdyn_plannedsalescontour    | no             | no           |
| msdyn_plannedwork            | no             | no           |
| msdyn_projectid              | sí            | no           |
| msdyn_projectidname          | no             | no           |
| msdyn_projectteamid          | no             | no           |
| msdyn_projectteamidname      | no             | no           |
| msdyn_start                  | no             | no           |
| msdyn_taskid                 | no             | no           |
| msdyn_taskidname             | no             | no           |
| msdyn_userresourceid         | no             | no           |

### <a name="project-team-member"></a>Miembro del equipo del proyecto

| **Nombre lógico**                                 | **Puede crear** | **Puede editar** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | no             | no           |
| msdyn_creategenericteammemberwithrequirementname | no             | no           |
| msdyn_deletestatus                               | no             | no           |
| msdyn_deletestatusname                           | no             | no           |
| msdyn_effort                                     | no             | no           |
| msdyn_effortcompleted                            | no             | no           |
| msdyn_effortremaining                            | no             | no           |
| msdyn_finish                                     | no             | no           |
| msdyn_hardbookedhours                            | no             | no           |
| msdyn_hours                                      | no             | no           |
| msdyn_markedfordeletiontimer                     | no             | no           |
| msdyn_markedfordeletiontimestamp                 | no             | no           |
| msdyn_msprojectclientid                          | no             | no           |
| msdyn_percentage                                 | no             | no           |
| msdyn_requiredhours                              | no             | no           |
| msdyn_softbookedhours                            | no             | no           |
| msdyn_start                                      | no             | no           |

### <a name="project"></a>Project

| **Nombre lógico**                       | **Puede crear** | **Puede editar** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | no             | no           |
| msdyn_actualexpensecost_base           | no             | no           |
| msdyn_actuallaborcost                  | no             | no           |
| msdyn_actuallaborcost_base             | no             | no           |
| msdyn_actualsales                      | no             | no           |
| msdyn_actualsales_base                 | no             | no           |
| msdyn_contractlineproject              | sí            | no           |
| msdyn_contractorganizationalunitid     | sí            | no           |
| msdyn_contractorganizationalunitidname | sí            | no           |
| msdyn_costconsumption                  | no             | no           |
| msdyn_costestimateatcomplete           | no             | no           |
| msdyn_costestimateatcomplete_base      | no             | no           |
| msdyn_costvariance                     | no             | no           |
| msdyn_costvariance_base                | no             | no           |
| msdyn_duration                         | no             | no           |
| msdyn_effort                           | no             | no           |
| msdyn_effortcompleted                  | no             | no           |
| msdyn_effortestimateatcompleteeac      | no             | no           |
| msdyn_effortremaining                  | no             | no           |
| msdyn_finish                           | sí            | sí          |
| msdyn_globalrevisiontoken              | no             | no           |
| msdyn_islinkedtomsprojectclient        | no             | no           |
| msdyn_islinkedtomsprojectclientname    | no             | no           |
| msdyn_linkeddocumenturl                | no             | no           |
| msdyn_msprojectdocument                | no             | no           |
| msdyn_msprojectdocumentname            | no             | no           |
| msdyn_plannedexpensecost               | no             | no           |
| msdyn_plannedexpensecost_base          | no             | no           |
| msdyn_plannedlaborcost                 | no             | no           |
| msdyn_plannedlaborcost_base            | no             | no           |
| msdyn_plannedsales                     | no             | no           |
| msdyn_plannedsales_base                | no             | no           |
| msdyn_progress                         | no             | no           |
| msdyn_remainingcost                    | no             | no           |
| msdyn_remainingcost_base               | no             | no           |
| msdyn_remainingsales                   | no             | no           |
| msdyn_remainingsales_base              | no             | no           |
| msdyn_replaylogheader                  | no             | no           |
| msdyn_salesconsumption                 | no             | no           |
| msdyn_salesestimateatcompleteeac       | no             | no           |
| msdyn_salesestimateatcompleteeac_base  | no             | no           |
| msdyn_salesvariance                    | no             | no           |
| msdyn_salesvariance_base               | no             | no           |
| msdyn_scheduleperformance              | no             | no           |
| msdyn_scheduleperformancename          | no             | no           |
| msdyn_schedulevariance                 | no             | no           |
| msdyn_taskearlieststart                | no             | no           |
| msdyn_teamsize                         | no             | no           |
| msdyn_teamsize_date                    | no             | no           |
| msdyn_teamsize_state                   | no             | no           |
| msdyn_totalactualcost                  | no             | no           |
| msdyn_totalactualcost_base             | no             | no           |
| msdyn_totalplannedcost                 | no             | no           |
| msdyn_totalplannedcost_base            | no             | no           |


## <a name="limitations-and-known-issues"></a>Limitaciones y problemas conocidos
La siguiente es una lista de limitaciones y problemas conocidos:

- Las API de programación solo pueden ser utilizadas por los **Usuarios con licencia de Microsoft Project**. No pueden ser utilizadas por:
    - Usuarios de la aplicación
    - Usuarios de sistema
    - Usuarios de integración
    - Otros usuarios que no tienen la licencia requerida
- Cada **OperationSet** solo puede tener un máximo de 100 operaciones.
- Cada usuario solo puede tener un máximo de 10 operaciones **OperationSet** abiertas.
- Project Operations actualmente admiten un máximo de 500 tareas en total en un proyecto.
- El estado de error y los registros de error de **OperationSet** no están disponibles actualmente.
- Las API de programación se ofrecen en versión preliminar pública. Microsoft no admite el uso de estas API en un entorno de producción.
- [Límites y límites en proyectos y tareas](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Control de errores

   - Para revisar los errores generados por los conjuntos de operaciones, vaya a **Configuración** \> **Integración de programación** \> **Conjuntos de operaciones**.
   - Para revisar los errores generados por el servicio de programación de proyectos, vaya a **Configuración** \> **Integración de programación** \> **Registros de errores de PSS**.

## <a name="sample-scenario"></a>Escenario de ejemplo

En este escenario, creará un proyecto, un miembro del equipo, cuatro tareas y dos asignaciones de recursos. A continuación, actualizará una tarea, actualizará el proyecto, eliminará una tarea, eliminará una asignación de recursos y creará una dependencia de tareas.

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

## <a name="additional-samples"></a>Ejemplos adicionales

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
