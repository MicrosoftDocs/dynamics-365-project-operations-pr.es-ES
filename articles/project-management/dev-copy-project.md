---
title: Desarrollar plantillas de proyectos con Copiar proyecto
description: Este artículo proporciona información sobre cómo crear plantillas de proyecto mediante la acción personalizada Copiar proyecto.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923853"
---
# <a name="develop-project-templates-with-copy-project"></a>Desarrollar plantillas de proyectos con Copiar proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations admite la capacidad de copiar un proyecto y de revertir cualquier asignación a los recursos genéricos que representan el rol. Los clientes pueden utilizar esta funcionalidad para crear plantillas de proyectos básicas.

Cuando selecciona **Copiar proyecto**, se actualiza el estado del proyecto de destino. Use **Razón para el estado** para determinar cuándo se completa la acción de copia. Seleccionar **Copiar proyecto** también actualiza la fecha de inicio del proyecto a la fecha de inicio actual si no se detecta una fecha objetivo en la entidad del proyecto objetivo.

## <a name="copy-project-custom-action"></a>Acción personalizada Copiar proyecto

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Parámetros de entrada

Hay tres parámetros de entrada:

- **ReplaceNamedResources** o **ClearTeamsAndAssignments**: configure solo una de las opciones. No configure ninguna.

    - **\{"ReplaceNamedResources":true\}**: el comportamiento predeterminado para Project Operations. Todos los recursos con nombre se sustituyen por recursos genéricos.
    - **\{"ClearTeamsAndAssignments":true\}**: el comportamiento predeterminado de Project for the Web. Se eliminan todas las asignaciones y los miembros del equipo.

- **SourceProject**: la referencia de entidad del proyecto de origen desde el que copiar. Este parámetro de proveedor no puede ser NULL.
- **Destino**: la referencia de entidad del proyecto de destino al que copiar. Este parámetro de proveedor no puede ser NULL.

La siguiente tabla proporciona un resumen de los tres parámetros.

| Parámetro                | Type             | valor                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Booleana          | **True** o **False** |
| ClearTeamsAndAssignments | Booleana          | **True** o **False** |
| SourceProject            | Referencia de entidad | El proyecto de origen    |
| Target                   | Referencia de entidad | El proyecto de destino    |

Para obtener más información sobre las acciones predeterminadas, consulte [Usar acciones de la API web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validaciones

Se realizan las siguientes validaciones.

1. NULL comprueba y recupera los proyectos de origen y de destino para confirmar la existencia de ambos proyectos en la organización.
2. El sistema valida que el proyecto de destino sea válido para copiar verificando las siguientes condiciones:

    - No hay actividad previa en el proyecto (incluida la selección de la pestaña **Tareas**), y el proyecto se crea por primera vez.
    - No hay una copia anterior, no se ha solicitado ninguna importación en este proyecto y el proyecto no tiene un estado **Fallido**.

3. La operación no se llama mediante HTTP.

## <a name="specify-fields-to-copy"></a>Especifique los campos para copiar

Cuando se llama a la acción, **Copiar proyecto** mirará la vista del proyecto **Copiar columnas de proyecto** para determinar qué campos copiar cuando se copia el proyecto.

### <a name="example"></a>Ejemplo

El siguiente ejemplo muestra cómo llamar a la acción personalizada **CopyProjectV3** con el conjunto de parámetros **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
