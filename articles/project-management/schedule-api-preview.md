---
title: Usar las API de programación de proyectos para realizar operaciones con entidades de programación
description: Este artículo proporciona información y ejemplos para usar las API de programación de proyectos.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541146"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Usar las API de programación de proyectos para realizar operaciones con entidades de programación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


**Entidades de programación**

Las API de programación de proyectos ofrecen la capacidad de realizar operaciones de creación, actualización y eliminación con **Entidades de programación**. Estas entidades se administran a través del motor de programación en Project para la web. Crear, actualizar y eliminar operaciones con **Entidades de programación** estaba restringido en versiones anteriores de Dynamics 365 Project Operations.

La siguiente tabla proporciona una lista completa de las entidades del programación del proyecto.

| **Nombre de entidad**         | **Nombre lógico de la entidad**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tarea de proyecto            | msdyn_projecttask           |
| Dependencia de tareas de proyecto | msdyn_projecttaskdependency |
| Asignación de recursos     | msdyn_resourceassignment    |
| Cubo de proyecto          | msdyn_projectbucket         |
| Miembro del equipo del proyecto     | msdyn_projectteam           |
| Listas de comprobación del proyecto      | msdyn_projectchecklist      |
| Etiqueta de proyecto           | msdyn_projectlabel          |
| Relación de tarea con etiqueta de proyecto   | msdyn_projecttasktolabel    |
| Sprint del proyecto          | msdyn_projectsprint         |

**OperationSet**

OperationSet es un patrón de unidad de trabajo que se puede usar cuando se deben procesar varias solicitudes que afectan la programación dentro de una transacción.

**API de programación del proyecto**

La siguiente es una lista de las API de programación de proyectos actuales.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Esta API se utiliza para crear un proyecto. El cubo del proyecto y el proyecto predeterminado se crean inmediatamente.                         |
| **msdyn_CreateTeamMemberV1**            | Esta API se utiliza para crear un miembro de equipo de proyecto. El registro de miembro del equipo se crea inmediatamente.                                  |
| **msdyn_CreateOperationSetV1**          | Esta API se puede utilizar para programar varias solicitudes que deben realizarse dentro de una transacción.                                        |
| **msdyn_PssCreateV1**                   | Esta API se utiliza para crear una entidad. La entidad puede ser cualquiera de las entidades de programación del proyecto que respaldan la operación de creación. |
| **msdyn_PssUpdateV1**                   | Esta API se utiliza para actualizar una entidad. La entidad puede ser cualquiera de las entidades de programación de proyectos que admitan la operación de actualización  |
| **msdyn_PssDeleteV1**                   | Esta API se utiliza para eliminar una entidad. La entidad puede ser cualquiera de las entidades de programación del proyecto que respaldan la operación de eliminación. |
| **msdyn_ExecuteOperationSetV1**         | Esta API se utiliza para ejecutar todas las operaciones dentro del conjunto de operaciones establecido.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Esta API se utiliza para actualizar un contorno de trabajo planificado de asignación de recursos.                                                        |



**Usar las API de programación de proyectos con OperationSet**

Porque los registros con ambos **CreateProjectV1** y **CreateTeamMemberV1** se crean inmediatamente, estas API no se pueden utilizar en **OperationSet** directamente. Sin embargo, puede utilizar la API para crear los registros necesarios, crear un **OperationSet** y, a continuación, utilizar estos registros creados previamente en **OperationSet**.

**Operaciones admitidas**

| **Entidades de programación**   | **Crear** | **Actualización** | **Delete** | **Consideraciones importantes**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tarea de proyecto            | Sí        | Sí        | Sí        | Los campos **Progreso**, **EffortCompleted** y **EffortRemaining** los campos se pueden editar en Project for the Web, pero no se pueden editar en Project Operations.                                                                                                                                                                                             |
| Dependencia de tareas de proyecto | Sí        | No         | Sí        | Los registros de dependencia de tareas del proyecto no se actualizan. En su lugar, se puede eliminar un registro antiguo y se puede crear un registro nuevo.                                                                                                                                                                                                                                 |
| Asignación de recursos     | Sí        | Sí\*      | Sí        | No se admiten las operaciones con los siguientes campos: **BookableResourceID**, **Esfuerzo**, **EffortCompleted**, **EffortCompleted** y **PlannedWork**. Los registros de asignación de recursos no se actualizan. En su lugar, se puede eliminar el registro antiguo y se puede crear un registro nuevo. Se ha proporcionado una API independiente para actualizar los contornos de asignación de recursos. |
| Cubo de proyecto          | Sí        | Sí        | Sí        | El cubo predeterminado se crea utilizando la API **CreateProjectV1**. Se agregó soporte para crear y eliminar cubos de proyectos en la versión de actualización 16.                                                                                                                                                                                                   |
| Miembro del equipo del proyecto     | Sí        | Sí        | Sí        | Para la operación de creación, use la API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Sí        | Sí        |            | No se admiten operaciones con los siguientes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esfuerzo**, **EffortCompleted**, **EffortRemaining**, **Progreso**, **Terminar**, **TaskEarliestStart**, y **Duración**.                                                                                       |
| Listas de comprobación del proyecto      | Sí        | Sí        | Sí        |                                                                                                                                                                                                                                                                                                                                                         |
| Etiqueta de proyecto           | No         | Sí        | No         | Los nombres de las etiquetas se pueden cambiar. Esta función solo está disponible para Project for the Web                                                                                                                                                                                                                                                                      |
| Relación de tarea con etiqueta de proyecto   | Sí        | No         | Sí        | Esta función solo está disponible para Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint del proyecto          | Sí        | Sí        | Sí        | El campo **Inicio** debe tener una fecha anterior al campo **Fin**. Los sprints para el mismo proyecto no pueden superponerse entre sí. Esta función solo está disponible para Project for the Web                                                                                                                                                                    |




La propiedad del identificador es opcional. Si se proporciona, el sistema intenta usarlo y lanza una excepción si no se puede usar. Si no se proporciona, el sistema lo generará.

**Limitaciones y problemas conocidos**

La siguiente es una lista de limitaciones y problemas conocidos:

-   Las API de programación del proyecto solo pueden utilizarlas los **Usuarios con licencia de Microsoft Project**. No pueden ser utilizadas por:
    -   Usuarios de la aplicación
    -   Usuarios de sistema
    -   Usuarios de integración
    -   Otros usuarios que no tienen la licencia requerida
-   Cada **OperationSet** solo puede tener un máximo de 100 operaciones.
-   Cada usuario solo puede tener un máximo de 10 operaciones **OperationSet** abiertas.
-   Project Operations actualmente admiten un máximo de 500 tareas en total en un proyecto.
-   Cada operación Actualizar contorno de asignación de recursos cuenta como una sola operación.
-   Cada lista de contornos actualizados puede contener un máximo de 100 intervalos de tiempo.
-   El estado de error y los registros de error de **OperationSet** no están disponibles actualmente.
-   Hay un máximo de 400 sprints por proyecto.
-   [Límites y límites en proyectos y tareas](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Actualmente, las etiquetas solo están disponibles para Project for the Web.

**Control de errores**

-   Para revisar los errores generados por los conjuntos de operaciones, vaya a **Configuración** \> **Integración de programación** \> **Conjuntos de operaciones**.
-   Para revisar los errores generados por el servicio de programación de proyectos, vaya a **Ajustes** \> **Integración de programación** \> **Registros de errores de PSS**.

**Edición de contornos de asignación de recursos**

A diferencia de todas las demás API de programación de proyectos que actualizan una entidad, la API de contorno de asignación de recursos es la única responsable de las actualizaciones de un solo campo, msdyn_plannedwork, en una sola entidad, msydn_resourceassignment.

El modo de programación dado es:

-   **Unidades fijas**
-   el calendario del proyecto es de 9:00 p. m. a 5:00 p. m. es de 9:00 p. m. a 5:00 p. m., lunes, martes, jueves y viernes (NO SE TRABAJAN LOS MIÉRCOLES)
-   y el calendario de recursos es de lunes a viernes de 9:00 p. m. a 1:00 p. m. PST

Esta asignación es por una semana, cuatro horas al día. Esto se debe a que el calendario de recursos es de 9 a 1 PST, o cuatro horas al día.

| &nbsp;     | Task | Fecha de inicio | Fecha de finalización  | Cantidad | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 trabajador |  T1  | 13/6/2022  | 17/6/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Por ejemplo, si desea que el trabajador solo trabaje tres horas cada día esta semana y permita una hora para otras tareas.

#### <a name="updatedcontours-sample-payload"></a>Carga útil de ejemplo UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Esta es la asignación después de ejecutar la API de programación de contorno de actualización.

| &nbsp;     | Task | Fecha de inicio | Fecha de finalización  | Cantidad | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 trabajador | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Escenario de ejemplo**

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

** Ejemplos adicionales

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
