---
title: Proyectos de estimación de ingresos a precio fijo
description: En este tema se proporciona información sobre los ingresos a precio fijo en proyectos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531564"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="0d404-103">Proyectos de estimación de ingresos a precio fijo</span><span class="sxs-lookup"><span data-stu-id="0d404-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="0d404-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="0d404-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0d404-105">Cuando crea una línea de contrato de proyecto con los siguientes atributos en Dynamics 365 Project Operations en Microsoft Dataverse, el sistema crea automáticamente un proyecto de estimación de ingresos a precio fijo.</span><span class="sxs-lookup"><span data-stu-id="0d404-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="0d404-106">La información de este proyecto se basa en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0d404-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="0d404-107">Un método de facturación de precio fijo.</span><span class="sxs-lookup"><span data-stu-id="0d404-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="0d404-108">Un proyecto asociado.</span><span class="sxs-lookup"><span data-stu-id="0d404-108">An associated project.</span></span>
  - <span data-ttu-id="0d404-109">Al menos un hito definido en la pestaña **Programación de facturas** de la página **Línea de contrato de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="0d404-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="0d404-110">Revisar proyectos de estimaciones de ingresos a precio fijo</span><span class="sxs-lookup"><span data-stu-id="0d404-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="0d404-111">Para revisar proyectos de estimaciones de ingresos a precio fijo, complete los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="0d404-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="0d404-112">En el entorno de Dynamics 365 Finance, vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Proyectos de estimación de ingresos a precio fijo**.</span><span class="sxs-lookup"><span data-stu-id="0d404-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="0d404-113">Seleccione el proyecto que desea ver y haga doble clic en el **Id. de proyecto de estimación** para abrir el registro y revisar sus detalles.</span><span class="sxs-lookup"><span data-stu-id="0d404-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="0d404-114">Expanda la pestaña **Proyecto**. Verá un proyecto en la cuadrícula **Proyectos seleccionados**.</span><span class="sxs-lookup"><span data-stu-id="0d404-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="0d404-115">El sistema lo usa como proyecto predeterminado porque es el proyecto asociado a la línea de contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="0d404-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="0d404-116">Para cambiar la asociación, seleccione proyectos adicionales y agréguelos a la cuadrícula **Proyectos seleccionados**.</span><span class="sxs-lookup"><span data-stu-id="0d404-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="0d404-117">Si se seleccionan varios proyectos en esta cuadrícula, el porcentaje de finalización del proyecto y las estimaciones de ingresos se calculan juntos para todos los proyectos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="0d404-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="0d404-118">El coste del proyecto, el perfil de ingresos, la plantilla de costes y el código de período se pueden configurar manualmente.</span><span class="sxs-lookup"><span data-stu-id="0d404-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="0d404-119">Si no se configuran manualmente, los valores predeterminados durante el primer cálculo estimado para el proyecto utilizando las reglas configuradas para los perfiles de costes e ingresos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="0d404-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

