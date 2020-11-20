---
title: Desarrollar plantillas de proyectos con Copiar proyecto
description: Este tema proporciona información sobre cómo crear plantillas de proyecto mediante la acción personalizada Copiar proyecto.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131634"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="a3e92-103">Desarrollar plantillas de proyectos con Copiar proyecto</span><span class="sxs-lookup"><span data-stu-id="a3e92-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="a3e92-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="a3e92-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a3e92-105">Dynamics 365 Project Operations admite la capacidad de copiar un proyecto y revertir cualquier asignación a los recursos genéricos que representan el rol.</span><span class="sxs-lookup"><span data-stu-id="a3e92-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="a3e92-106">Los clientes pueden utilizar esta funcionalidad para crear plantillas de proyectos básicas.</span><span class="sxs-lookup"><span data-stu-id="a3e92-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="a3e92-107">Cuando selecciona **Copiar proyecto**, se actualiza el estado del proyecto de destino.</span><span class="sxs-lookup"><span data-stu-id="a3e92-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="a3e92-108">Use **Razón para el estado** para determinar cuándo se completa la acción de copia.</span><span class="sxs-lookup"><span data-stu-id="a3e92-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="a3e92-109">Seleccionar **Copiar proyecto** también actualiza la fecha de inicio del proyecto a la fecha de inicio actual si no se detecta una fecha objetivo en la entidad del proyecto objetivo.</span><span class="sxs-lookup"><span data-stu-id="a3e92-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="a3e92-110">Acción personalizada Copiar proyecto</span><span class="sxs-lookup"><span data-stu-id="a3e92-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="a3e92-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="a3e92-111">Name</span></span> 

<span data-ttu-id="a3e92-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="a3e92-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="a3e92-113">Parámetros de entrada</span><span class="sxs-lookup"><span data-stu-id="a3e92-113">Input parameters</span></span>
<span data-ttu-id="a3e92-114">Hay tres parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="a3e92-114">There are three input parameters:</span></span>

| <span data-ttu-id="a3e92-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a3e92-115">Parameter</span></span>          | <span data-ttu-id="a3e92-116">Escribir</span><span class="sxs-lookup"><span data-stu-id="a3e92-116">Type</span></span>   | <span data-ttu-id="a3e92-117">Valores</span><span class="sxs-lookup"><span data-stu-id="a3e92-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="a3e92-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="a3e92-118">ProjectCopyOption</span></span>  | <span data-ttu-id="a3e92-119">String</span><span class="sxs-lookup"><span data-stu-id="a3e92-119">String</span></span> | <span data-ttu-id="a3e92-120">**{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="a3e92-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="a3e92-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="a3e92-121">SourceProject</span></span>      | <span data-ttu-id="a3e92-122">Referencia de entidad</span><span class="sxs-lookup"><span data-stu-id="a3e92-122">Entity Reference</span></span> | <span data-ttu-id="a3e92-123">Proyecto de origen</span><span class="sxs-lookup"><span data-stu-id="a3e92-123">Source Project</span></span> |
| <span data-ttu-id="a3e92-124">Destino</span><span class="sxs-lookup"><span data-stu-id="a3e92-124">Target</span></span>             | <span data-ttu-id="a3e92-125">Referencia de entidad</span><span class="sxs-lookup"><span data-stu-id="a3e92-125">Entity Reference</span></span> | <span data-ttu-id="a3e92-126">Proyecto de destino</span><span class="sxs-lookup"><span data-stu-id="a3e92-126">Target Project</span></span> |


- <span data-ttu-id="a3e92-127">**{"clearTeamsAndAssignments":true}**: el comportamiento predeterminado de Project for the Web y eliminará todas las asignaciones y miembros del equipo.</span><span class="sxs-lookup"><span data-stu-id="a3e92-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="a3e92-128">**{"removeNamedResources":true}** El comportamiento predeterminado de Project Operations y revertirá las asignaciones a recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="a3e92-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="a3e92-129">Para obtener más información sobre las acciones predeterminadas, consulte [Usar acciones de la API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="a3e92-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="a3e92-130">Especifique los campos para copiar</span><span class="sxs-lookup"><span data-stu-id="a3e92-130">Specify fields to copy</span></span> 
<span data-ttu-id="a3e92-131">Cuando se llama a la acción, **Copiar proyecto** mirará la vista del proyecto **Copiar columnas de proyecto** para determinar qué campos copiar cuando se copia el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a3e92-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
