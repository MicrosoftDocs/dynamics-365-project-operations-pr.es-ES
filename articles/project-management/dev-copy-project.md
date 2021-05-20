---
title: Desarrollar plantillas de proyectos con Copiar proyecto
description: Este tema proporciona información sobre cómo crear plantillas de proyecto mediante la acción personalizada Copiar proyecto.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949835"
---
# <a name="develop-project-templates-with-copy-project"></a>Desarrollar plantillas de proyectos con Copiar proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations admite la capacidad de copiar un proyecto y de revertir cualquier asignación a los recursos genéricos que representan el rol. Los clientes pueden utilizar esta funcionalidad para crear plantillas de proyectos básicas.

Cuando selecciona **Copiar proyecto**, se actualiza el estado del proyecto de destino. Use **Razón para el estado** para determinar cuándo se completa la acción de copia. Seleccionar **Copiar proyecto** también actualiza la fecha de inicio del proyecto a la fecha de inicio actual si no se detecta una fecha objetivo en la entidad del proyecto objetivo.

## <a name="copy-project-custom-action"></a>Acción personalizada Copiar proyecto 

### <a name="name"></a>Nombre 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parámetros de entrada
Hay tres parámetros de entrada:

| Parámetro          | Escribir   | Valores                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referencia de entidad | Proyecto de origen |
| Destino             | Referencia de entidad | Proyecto de destino |


- **{"clearTeamsAndAssignments":true}**: el comportamiento predeterminado de Project for the Web y eliminará todas las asignaciones y miembros del equipo.
- **{"removeNamedResources":true}** El comportamiento predeterminado de Project Operations y revertirá las asignaciones a recursos genéricos.

Para obtener más información sobre las acciones predeterminadas, consulte [Usar acciones de la API web](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Especifique los campos para copiar 
Cuando se llama a la acción, **Copiar proyecto** mirará la vista del proyecto **Copiar columnas de proyecto** para determinar qué campos copiar cuando se copia el proyecto.


### <a name="example"></a>Ejemplo
El ejemplo siguiente muestra cómo se llama a la acción personalizada **CopyProject** con el conjunto de parámetros **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]