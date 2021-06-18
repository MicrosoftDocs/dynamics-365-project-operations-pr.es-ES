---
title: Configurar opciones de parámetros adicionales
description: Cómo configurar las opciones de parámetros adicionales en Project Service
author: JohnPBurrows
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
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001132"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="43f58-103">Configurar opciones de parámetros adicionales (Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="43f58-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="43f58-104">Una vez que ha configurado los elementos de los temas anteriores, debe configurar parámetros de proyecto adicionales para usar con sus proyectos.</span><span class="sxs-lookup"><span data-stu-id="43f58-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="43f58-105">La primera vez que instaló [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], creó una configuración de parámetros para crear primero todos los registros necesarios para que funcione [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="43f58-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="43f58-106">Ahora es el momento de volver y configurar campos adicionales para estas configuraciones de parámetros.</span><span class="sxs-lookup"><span data-stu-id="43f58-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="43f58-107">Deberá haber configurado los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="43f58-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="43f58-108">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="43f58-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="43f58-109">Frecuencia de factura</span><span class="sxs-lookup"><span data-stu-id="43f58-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="43f58-110">Plantilla de horas laborables</span><span class="sxs-lookup"><span data-stu-id="43f58-110">Work hours template</span></span>  
  
-   <span data-ttu-id="43f58-111">Lista de precios</span><span class="sxs-lookup"><span data-stu-id="43f58-111">Price list</span></span>  
 
<span data-ttu-id="43f58-112">En este paso, también indicará el tipo de asignación de recursos que desee:</span><span class="sxs-lookup"><span data-stu-id="43f58-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="43f58-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="43f58-113">**Central**.</span></span> <span data-ttu-id="43f58-114">Sólo los administradores de recursos pueden asignar recursos a proyectos.</span><span class="sxs-lookup"><span data-stu-id="43f58-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="43f58-115">**Híbrido**.</span><span class="sxs-lookup"><span data-stu-id="43f58-115">**Hybrid**.</span></span> <span data-ttu-id="43f58-116">Los administradores de recursos, jefes de proyecto, y los directores de cuentas pueden asignar recursos a proyectos.</span><span class="sxs-lookup"><span data-stu-id="43f58-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="43f58-117">Para establecer parámetros de proyecto:</span><span class="sxs-lookup"><span data-stu-id="43f58-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="43f58-118">Vaya a **Project Service > Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="43f58-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="43f58-119">Haga clic en las opciones de parámetros que desea configurar (los que creó la primera vez que instaló el [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), o haga clic en **Nuevo** para crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="43f58-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="43f58-120">En el área **General**, defina todas las opciones para los parámetros del proyecto.</span><span class="sxs-lookup"><span data-stu-id="43f58-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="43f58-121">En el área **Lista de precios**, haga clic en **+** para agregar una lista de precios, seleccione una lista de precios en la lista desplegable **Lista de precios de parámetros de proyecto** y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="43f58-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="43f58-122">Haga clic en el botón **Guardar** en la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="43f58-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="43f58-123">El registro de parámetros del proyecto debe mantenerse para que Project Service funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="43f58-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="43f58-124">No se debe eliminar este registro.</span><span class="sxs-lookup"><span data-stu-id="43f58-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="43f58-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="43f58-125">See Also</span></span>  
 [<span data-ttu-id="43f58-126">Configuración de recursos</span><span class="sxs-lookup"><span data-stu-id="43f58-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]