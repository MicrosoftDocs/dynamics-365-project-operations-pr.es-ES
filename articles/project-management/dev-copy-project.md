---
title: Desarrollar plantillas de proyectos con Copiar proyecto
description: Este tema proporciona información sobre cómo crear plantillas de proyecto mediante la acción personalizada Copiar proyecto.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005677"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="14b42-103">Desarrollar plantillas de proyectos con Copiar proyecto</span><span class="sxs-lookup"><span data-stu-id="14b42-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="14b42-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="14b42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="14b42-105">Dynamics 365 Project Operations admite la capacidad de copiar un proyecto y de revertir cualquier asignación a los recursos genéricos que representan el rol.</span><span class="sxs-lookup"><span data-stu-id="14b42-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="14b42-106">Los clientes pueden utilizar esta funcionalidad para crear plantillas de proyectos básicas.</span><span class="sxs-lookup"><span data-stu-id="14b42-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="14b42-107">Cuando selecciona **Copiar proyecto**, se actualiza el estado del proyecto de destino.</span><span class="sxs-lookup"><span data-stu-id="14b42-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="14b42-108">Use **Razón para el estado** para determinar cuándo se completa la acción de copia.</span><span class="sxs-lookup"><span data-stu-id="14b42-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="14b42-109">Seleccionar **Copiar proyecto** también actualiza la fecha de inicio del proyecto a la fecha de inicio actual si no se detecta una fecha objetivo en la entidad del proyecto objetivo.</span><span class="sxs-lookup"><span data-stu-id="14b42-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="14b42-110">Acción personalizada Copiar proyecto</span><span class="sxs-lookup"><span data-stu-id="14b42-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="14b42-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="14b42-111">Name</span></span> 

<span data-ttu-id="14b42-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="14b42-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="14b42-113">Parámetros de entrada</span><span class="sxs-lookup"><span data-stu-id="14b42-113">Input parameters</span></span>
<span data-ttu-id="14b42-114">Hay tres parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="14b42-114">There are three input parameters:</span></span>

| <span data-ttu-id="14b42-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="14b42-115">Parameter</span></span>          | <span data-ttu-id="14b42-116">Escribir</span><span class="sxs-lookup"><span data-stu-id="14b42-116">Type</span></span>   | <span data-ttu-id="14b42-117">Valores</span><span class="sxs-lookup"><span data-stu-id="14b42-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="14b42-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="14b42-118">ProjectCopyOption</span></span>  | <span data-ttu-id="14b42-119">String</span><span class="sxs-lookup"><span data-stu-id="14b42-119">String</span></span> | <span data-ttu-id="14b42-120">**{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="14b42-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="14b42-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="14b42-121">SourceProject</span></span>      | <span data-ttu-id="14b42-122">Referencia de entidad</span><span class="sxs-lookup"><span data-stu-id="14b42-122">Entity Reference</span></span> | <span data-ttu-id="14b42-123">Proyecto de origen</span><span class="sxs-lookup"><span data-stu-id="14b42-123">Source Project</span></span> |
| <span data-ttu-id="14b42-124">Destino</span><span class="sxs-lookup"><span data-stu-id="14b42-124">Target</span></span>             | <span data-ttu-id="14b42-125">Referencia de entidad</span><span class="sxs-lookup"><span data-stu-id="14b42-125">Entity Reference</span></span> | <span data-ttu-id="14b42-126">Proyecto de destino</span><span class="sxs-lookup"><span data-stu-id="14b42-126">Target Project</span></span> |


- <span data-ttu-id="14b42-127">**{"clearTeamsAndAssignments":true}**: el comportamiento predeterminado de Project for the Web y eliminará todas las asignaciones y miembros del equipo.</span><span class="sxs-lookup"><span data-stu-id="14b42-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="14b42-128">**{"removeNamedResources":true}** El comportamiento predeterminado de Project Operations y revertirá las asignaciones a recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="14b42-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="14b42-129">Para obtener más información sobre las acciones predeterminadas, consulte [Usar acciones de la API web](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="14b42-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="14b42-130">Especifique los campos para copiar</span><span class="sxs-lookup"><span data-stu-id="14b42-130">Specify fields to copy</span></span> 
<span data-ttu-id="14b42-131">Cuando se llama a la acción, **Copiar proyecto** mirará la vista del proyecto **Copiar columnas de proyecto** para determinar qué campos copiar cuando se copia el proyecto.</span><span class="sxs-lookup"><span data-stu-id="14b42-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="14b42-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14b42-132">Example</span></span>
<span data-ttu-id="14b42-133">El ejemplo siguiente muestra cómo se llama a la acción personalizada **CopyProject** con el conjunto de parámetros **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="14b42-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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