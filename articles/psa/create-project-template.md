---
title: Crear una plantilla de proyecto
description: Cómo crear una plantilla de proyecto en Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085161"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="7d885-103">Crear una plantilla de proyecto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="7d885-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7d885-104">Las plantillas de proyecto ahorran tiempo si su empresa presenta ofertas regularmente para tipos similares de proyectos.</span><span class="sxs-lookup"><span data-stu-id="7d885-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="7d885-105">Ofrecen un conjunto de roles estándar y de horas estimadas para un tipo de proyecto.</span><span class="sxs-lookup"><span data-stu-id="7d885-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="7d885-106">Los administradores de cuentas y los jefes de proyecto pueden crear los proyectos basados en una plantilla de proyectos, o pueden copiar la plantilla y crear la suya propia.</span><span class="sxs-lookup"><span data-stu-id="7d885-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="7d885-107">Componentes de la plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="7d885-107">Components of project template</span></span>
 <span data-ttu-id="7d885-108">Una plantilla de proyecto consta de tres componentes:</span><span class="sxs-lookup"><span data-stu-id="7d885-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="7d885-109">**Estructura de descomposición del trabajo** : Una estructura de descomposición del trabajo en una plantilla de proyecto tiene el mismo conjunto de elementos que en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="7d885-109">**Work breakdown structure** : A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="7d885-110">Puede crear una jerarquía de tareas, asociar roles a tarea, definir atributos de programación, establecer dependencias y ver todos los datos del diagrama de Gantt.</span><span class="sxs-lookup"><span data-stu-id="7d885-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="7d885-111">La estructura de descomposición del trabajo en plantillas de proyecto también es compatible con los modos de tarea para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="7d885-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="7d885-112">No hay diferencia entre una plantilla de proyecto y un proyecto al crear un programa de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7d885-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="7d885-113">**Estimaciones de proyecto** : Las estimaciones de proyecto en plantillas funcionan igual que en proyectos, excepto las listas de precios para establecer valores predeterminados de coste y precios de ventas siempre son las listas de precios de coste y precios de ventas predeterminadas definidas en parámetros de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7d885-113">**Project estimates** : Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="7d885-114">El resto de la funcionalidad es igual que en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="7d885-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="7d885-115">**Formación del equipo de proyecto** : Cuando se forma un equipo de proyecto para una plantilla de proyectos, no puede reservar un recurso con nombre en una plantilla.</span><span class="sxs-lookup"><span data-stu-id="7d885-115">**Project team formation** : When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="7d885-116">Puede usar **Generar equipo de proyecto** en la estructura de descomposición del trabajo para generar un conjunto de recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="7d885-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="7d885-117">También puede especificar conocimientos y habilidades necesarios para recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="7d885-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="7d885-118">No puede sustituir un recurso genérico con un recurso reservable en plantillas de proyecto.</span><span class="sxs-lookup"><span data-stu-id="7d885-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="7d885-119">Crear un proyecto a partir de una plantilla</span><span class="sxs-lookup"><span data-stu-id="7d885-119">Create a project from a template</span></span>  
 <span data-ttu-id="7d885-120">Puede crear un proyecto a partir de una plantilla de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="7d885-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="7d885-121">Cuando cree un proyecto de la oferta, puede seleccionar una plantilla de proyecto en el formulario de creación rápida de proyecto.</span><span class="sxs-lookup"><span data-stu-id="7d885-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="7d885-122">Cuando cree un proyecto haciendo clic en **Nuevo proyecto** , el formulario de proyecto se muestra antes de guardar el registro.</span><span class="sxs-lookup"><span data-stu-id="7d885-122">When creating a project by clicking **New Project** , the project form displays before you save the record.</span></span> <span data-ttu-id="7d885-123">Desde ahí, puede hacer clic en el campo **Elegir una plantilla** para elegir de la lista de plantillas de proyecto predefinidas en su organización.</span><span class="sxs-lookup"><span data-stu-id="7d885-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="7d885-124">Haga clic en **Crear un proyecto a partir de una plantilla** en la página **Plantilla del proyecto** para crear un proyecto desde la plantilla.</span><span class="sxs-lookup"><span data-stu-id="7d885-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="7d885-125">Copiar componentes de una plantilla a un proyecto</span><span class="sxs-lookup"><span data-stu-id="7d885-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="7d885-126">Al copiar los componentes de una plantilla en un proyecto, hay algunas cosas que debería saber.</span><span class="sxs-lookup"><span data-stu-id="7d885-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="7d885-127">**Copiar una estructura de descomposición del trabajo** : Al copiar la estructura de descomposición del trabajo de una plantilla de proyecto, si el proyecto tiene otro calendario del proyecto que la plantilla, las horas laborables del calendario del proyecto se aplicarán a la programación de tareas.</span><span class="sxs-lookup"><span data-stu-id="7d885-127">**Copying a work breakdown structure** : When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="7d885-128">Esto ajusta la programación al calendario del proyecto de apoyo.</span><span class="sxs-lookup"><span data-stu-id="7d885-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="7d885-129">De forma similar, la primera tarea en la estructura de descomposición del trabajo toma la fecha de inicio del proyecto, por lo que el resto de la programación de la jerarquía de tareas se actualiza en función de la duración y las dependencias especificadas en la estructura de descomposición del trabajo de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="7d885-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="7d885-130">**Copiar estimaciones del proyecto** : Al copiar a través de las líneas de estimación de proyectos, se actualizarán las listas de precios basándose en la unidad propietaria del proyecto para la lista de precios de coste y el cliente para la lista de precios de ventas.</span><span class="sxs-lookup"><span data-stu-id="7d885-130">**Copying project estimates** : When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="7d885-131">El coste unitario y los precios de venta se determinan a partir de estas listas de precios en los proyectos asociados a una entidad de ventas.</span><span class="sxs-lookup"><span data-stu-id="7d885-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="7d885-132">**Copiar un equipo del proyecto** : Al copiar el equipo del proyecto desde la plantilla hasta un proyecto, los recursos genéricos se copian, junto con las cualificaciones y las habilidades definidas en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="7d885-132">**Copying a project team** : When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="7d885-133">Las asignaciones de recursos genéricos también se mantienen como en la plantilla del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7d885-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7d885-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d885-134">See Also</span></span>  
 [<span data-ttu-id="7d885-135">Guía del jefe de proyecto</span><span class="sxs-lookup"><span data-stu-id="7d885-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
