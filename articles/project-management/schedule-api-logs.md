---
title: Registros de programación de proyectos
description: Este tema proporciona información y ejemplos que lo ayudarán a usar los registros de programación de proyectos para rastrear errores relacionados con el servicio de programación de proyectos y las API de programación de proyectos.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589539"
---
# <a name="project-scheduling-logs"></a>Registros de programación de proyectos

_**Se aplica a**: Project Operations para escenarios basados en recursos/no mantenidos en existencias, implementación simplificada: de la oferta a la facturación proforma_, _Project for the Web_

Microsoft Dynamics 365 Project Operations usa [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) como su motor de programación principal. En lugar de usar Interfaces de programación de aplicaciones web (API) de Microsoft Dataverse estándar, Project Operations utiliza las nuevas API de programación de proyectos para crear, actualizar y eliminar tareas de proyectos, asignaciones de recursos, dependencias de tareas, depósitos de proyectos y miembros de equipos de proyectos. Sin embargo, cuando las operaciones de creación, actualización o eliminación se ejecutan mediante programación en entidades de estructura de descomposición del trabajo (WBS), pueden producirse errores. Para rastrear estos errores y el historial de operaciones, se han implementado dos nuevos registros administrativos: **Conjunto de operación** y **Servicio de programación de proyectos (PSS)**. Para acceder a estos registros, vaya a **Configuración** \> **Programación de integración**.

La ilustración siguiente muestra el modelo de datos para los registros de programación de proyecto.

![Modelo de datos para los registros de programación de proyecto.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Registro de conjunto de operación

El registro del conjunto de operaciones realiza un seguimiento de la ejecución de un conjunto de operaciones que se utiliza para ejecutar una o varias operaciones de creación, actualización o eliminación en un lote en proyectos, tareas de proyectos, asignaciones de recursos, dependencias de tareas, depósitos de proyectos o miembros del equipo del proyecto. El campo **Operación en estado** muestra el estado general del conjunto de operaciones. Los detalles de la carga útil del conjunto de operaciones se capturan en los registros de Detalle del conjunto de operaciones relacionados.

### <a name="operation-set"></a>Conjunto de operaciones

La tabla siguiente muestra los campos que relacionados con la entidad **Conjunto de operaciones**.

| SchemaName            | Description                                                                                                  | Nombre para mostrar            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | La fecha y hora en que se el conjunto de operaciones se completó o falló.                                                | CompletedOn            |
| msdyn_correlationid   | El valor de **correlationId** de la solicitud.                                                                  | CorrelationId          |
| msdyn_description     | Descripción del conjunto de operaciones.                                                                        | Description            |
| msdyn_executedon      | La fecha y hora en que se ejecutó el registro.                                                                       | Ejecutado el            |
| msdyn_operationsetId  | El identificador único de las instancias de la entidad.                                                                   | OperationSet           |
| msdyn_Project         | El proyecto relacionado con el conjunto de operaciones.                                                            | Project                |
| msdyn_projectid       | El valor de **projectId** de la solicitud.                                                                      | ProjectId (en desuso) |
| msdyn_projectName     | No aplicable.                                                                                              | No aplicable         |
| msdyn_PSSErrorLog     | El identificador único del registro de errores del servicio de programación de proyectos asociado con el conjunto de operaciones. | Registro de errores de PSS          |
| msdyn_PSSErrorLogName | No aplicable.                                                                                              | No aplicable         |
| msdyn_status          | El estado del conjunto de operaciones.                                                                             | Status                 |
| msdyn_statusName      | No aplicable.                                                                                              | No aplicable         |
| msdyn_useraadid       | El identificador del objeto Azure Active Directory (Azure AD) del usuario al que pertenece la solicitud.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalles de conjunto de operaciones

La tabla siguiente muestra los campos que relacionados con la entidad **Detalles del conjunto de operaciones**.

| SchemaName                 | Description                                                                                 | Nombre para mostrar           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Los campos Dataverse serializados para la solicitud.                                            | CdsPayload            |
| msdyn_entityname           | Nombre de la entidad para la solicitud.                                                     | EntityName            |
| msdyn_httpverb             | Método de solicitud.                                                                         | Verbo HTTP (en desuso) |
| msdyn_httpverbName         | No aplicable.                                                                             | No aplicable        |
| msdyn_operationset         | El identificador único del conjunto de operaciones al que pertenece este registro.                      | OperationSet          |
| msdyn_operationsetdetailId | El identificador único de las instancias de la entidad.                                                  | Detalle de OperationSet   |
| msdyn_operationsetName     | No aplicable.                                                                             | No aplicable        |
| msdyn_operationtype        | El tipo de operación del detalle del conjunto de operaciones.                                             | OperationType         |
| msdyn_operationtypeName    | No aplicable.                                                                             | No aplicable        |
| msdyn_psspayload           | Los campos serializados del Servicio de programación de proyectos para la solicitud.                           | PssPayload            |
| msdyn_recordid             | El identificador único del registro de solicitud.                                                       | Identificador de registro             |
| msdyn_requestnumber        | Un número generado automáticamente que se usa para identificar el pedido en que se reciben las solicitudes. | Número de solicitud        |

## <a name="project-scheduling-service-error-logs"></a>Registros de error del servicio de programación de proyectos

Los registros de errores del Servicio de programación de proyectos capturan los errores que ocurren cuando el Servicio de programación de proyectos intenta una operación **Guardar** o **Abrir**. Hay tres escenarios admitidos donde se generan estos registros:

- Las acciones iniciadas por el usuario fallan críticamente (por ejemplo, no se puede crear una asignación porque faltan privilegios).
- El servicio de programación de proyectos no puede crear, actualizar, eliminar ni realizar ninguna otra operación en cascada en una entidad mediante programación.
- El usuario experimenta errores cuando un registro no se abre (por ejemplo, cuando se abre un proyecto o se actualiza la información de un miembro del equipo).

### <a name="project-scheduling-service-log"></a>Registro del servicio de programación de proyectos

La tabla siguiente muestra los campos que se incluyen en el registro del Servicio de programación de proyectos.

| SchemaName          | Description                                                                    | Nombre para mostrar    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | La pila de llamadas de la excepción.                                               | Pila de llamadas     |
| msdyn_correlationid | Id. de correlación del error.                                               | CorrelationId  |
| msdyn_errorcode     | Un campo que se utiliza para almacenar el código de error Dataverse o el código de error HTTP. | Código de error     |
| msdyn_HelpLink      | Un vínculo de la documentación de ayuda pública.                                       | Vínculo de ayuda      |
| msdyn_log           | El registro del servicio de programación de proyectos.                                   | Registro            |
| msdyn_project       | El proyecto con el que está asociado el registro del error.                             | Project        |
| msdyn_projectName   | El nombre del proyecto si se conservará la carga útil del conjunto de operaciones. | No aplicable |
| msdyn_psserrorlogId | El identificador único de las instancias de la entidad.                                     | Registro de errores de PSS  |
| msdyn_SessionId     | Id. de sesión del proyecto.                                                        | Identificador de sesión     |

## <a name="error-log-cleanup"></a>Limpieza del registro de errores

De forma predeterminada, tanto los registros de errores del servicio de programación de proyectos como el registro del conjunto de operaciones se pueden limpiar cada 90 días. Se eliminan todos los registros con más de 90 días. Sin embargo, al cambiar el valor del campo **msdyn_StateOperationSetAge** en la página **Parámetros del proyecto**, los administradores pueden ajustar el rango de limpieza para que sea entre 1 y 120 días. Hay varios métodos disponibles para cambiar este valor:

- Personaliza la entidad **Parámetro del proyecto** creando una página personalizada y agregando el campo **Antigüedad del conjunto de operaciones obsoletas**.
- Utilice el código de cliente que utiliza el [Kit de desarrollo de software WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Use el código del SDK de servicio que usa el método SDK de Xrm **updateRecord** (referencia de API de cliente) en aplicaciones basadas en modelos. Power Apps incluye una descripción y parámetros admitidos para el método **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
