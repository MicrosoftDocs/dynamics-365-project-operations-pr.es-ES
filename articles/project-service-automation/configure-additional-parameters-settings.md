---
title: Configurar opciones de parámetros adicionales
description: Cómo configurar las opciones de parámetros adicionales en Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756099"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="8c193-103">Configurar opciones de parámetros adicionales (Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="8c193-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8c193-104">Una vez que ha configurado los elementos de los temas anteriores, debe configurar parámetros de proyecto adicionales para usar con sus proyectos.</span><span class="sxs-lookup"><span data-stu-id="8c193-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="8c193-105">La primera vez que instaló [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], creó una configuración de parámetros para crear primero todos los registros necesarios para que funcione [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="8c193-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="8c193-106">Ahora es el momento de volver y configurar campos adicionales para estas configuraciones de parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c193-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="8c193-107">Deberá haber configurado los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8c193-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="8c193-108">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="8c193-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="8c193-109">Frecuencia de factura</span><span class="sxs-lookup"><span data-stu-id="8c193-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="8c193-110">Plantilla de horas laborables</span><span class="sxs-lookup"><span data-stu-id="8c193-110">Work hours template</span></span>  
  
-   <span data-ttu-id="8c193-111">Lista de precios</span><span class="sxs-lookup"><span data-stu-id="8c193-111">Price list</span></span>  
 
<span data-ttu-id="8c193-112">En este paso, también indicará el tipo de asignación de recursos que desee:</span><span class="sxs-lookup"><span data-stu-id="8c193-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="8c193-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="8c193-113">**Central**.</span></span> <span data-ttu-id="8c193-114">Sólo los administradores de recursos pueden asignar recursos a proyectos.</span><span class="sxs-lookup"><span data-stu-id="8c193-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="8c193-115">**Híbrido**.</span><span class="sxs-lookup"><span data-stu-id="8c193-115">**Hybrid**.</span></span> <span data-ttu-id="8c193-116">Los administradores de recursos, jefes de proyecto, y los directores de cuentas pueden asignar recursos a proyectos.</span><span class="sxs-lookup"><span data-stu-id="8c193-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="8c193-117">Para establecer parámetros de proyecto:</span><span class="sxs-lookup"><span data-stu-id="8c193-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="8c193-118">Vaya a **Project Service > Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="8c193-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="8c193-119">Haga clic en las opciones de parámetros que desea configurar (los que creó la primera vez que instaló el [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), o haga clic en **Nuevo** para crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="8c193-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="8c193-120">En el área **General**, defina todas las opciones para los parámetros del proyecto.</span><span class="sxs-lookup"><span data-stu-id="8c193-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="8c193-121">En el área **Lista de precios**, haga clic en **+** para agregar una lista de precios, seleccione una lista de precios en la lista desplegable **Lista de precios de parámetros de proyecto** y después haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="8c193-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="8c193-122">Haga clic en el botón **Guardar** en la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="8c193-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="8c193-123">El registro de parámetros del proyecto debe mantenerse para que Project Service funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="8c193-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="8c193-124">No se debe eliminar este registro.</span><span class="sxs-lookup"><span data-stu-id="8c193-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="8c193-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c193-125">See Also</span></span>  
 [<span data-ttu-id="8c193-126">Configuración de recursos</span><span class="sxs-lookup"><span data-stu-id="8c193-126">Set up resources</span></span>](../project-service/set-up-resources.md)
