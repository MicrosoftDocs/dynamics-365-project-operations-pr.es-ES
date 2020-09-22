---
title: Información general de Project Service Automation
description: Este tema proporciona información sobre la integración de Dynamics 365 Project Service Automation con la solución de integración de Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756028"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="7ca26-103">Información general de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7ca26-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7ca26-104">La solución de integración de Project Service Automation con Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Dynamics 365 Finance y Dynamics 365 Project Service Automation a través de Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7ca26-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="7ca26-105">Las plantillas de integración que están disponibles con la función de integración de datos permiten el flujo de proyectos, contratos de proyecto, líneas de contrato de proyecto, hitos de línea de contrato de proyecto, tareas de proyecto, categorías de transacción de gastos, cálculos de horas y cálculos de gastos desde Project Service Automation hasta Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="7ca26-106">Si utiliza la versión 7.3.0, debe instalar KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="7ca26-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="7ca26-107">Entonces podrá integrar proyectos de precio fijo.</span><span class="sxs-lookup"><span data-stu-id="7ca26-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="7ca26-108">Si está utilizando la versión 7.3.0 y está transfiriendo transacciones de tarifas desde Project Service Automation, debe instalar KB 4345320 para incluir esas tarifas en la factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7ca26-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="7ca26-109">Si utiliza la versión 8.0, podrá utilizar la integración de tareas, las categorías de transacciones de gastos, las estimaciones de horas, las estimaciones de gastos y el bloqueo de funciones.</span><span class="sxs-lookup"><span data-stu-id="7ca26-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="7ca26-110">Si está utilizando la versión 8.0.1 o posterior, podrá sincronizar los datos reales.</span><span class="sxs-lookup"><span data-stu-id="7ca26-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="7ca26-111">Antes de que pueda integrar Project Service Automation en Finance, debe configurar los parámetros de integración de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7ca26-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="7ca26-112">Para más información, consulte [Parámetros de integración de Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7ca26-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="7ca26-113">Esta solución de integración permite la sincronización directa en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="7ca26-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="7ca26-114">Mantenga los contratos del proyecto en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7ca26-115">Cree proyectos en los contratos en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7ca26-116">Mantenga las líneas de contratos del proyecto en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7ca26-117">Mantenga los hitos de las líneas de contratos del proyecto en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7ca26-118">Mantenga las tareas del proyecto en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7ca26-119">Mantenga los categorías de transacciones de gastos en Finance y sincronícelos directamente desde Finance a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7ca26-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="7ca26-120">Cree cálculos de horas de proyectos en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7ca26-121">Cree cálculos de gastos de proyectos en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7ca26-122">Cree datos reales de tiempo, gastos y tarifas del proyecto en Project Service Automation y cree transacciones del proyecto en el diario de integración de Project Service Automation para que se puedan registrar en Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="7ca26-123">Sincronización de datos</span><span class="sxs-lookup"><span data-stu-id="7ca26-123">Data synchronization</span></span>

<span data-ttu-id="7ca26-124">La siguiente ilustración muestra cómo se sincronizan los datos como parte de la integración entre Project Service Automation y Finance.</span><span class="sxs-lookup"><span data-stu-id="7ca26-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="7ca26-125">No todas las plantillas están disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="7ca26-125">Not all templates are currently available.</span></span> <span data-ttu-id="7ca26-126">Las plantillas se publicarán a medida que se completen.</span><span class="sxs-lookup"><span data-stu-id="7ca26-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="7ca26-127">[![Integración de Project Service Automation con Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="7ca26-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="7ca26-128">Requisitos del sistema para Finance</span><span class="sxs-lookup"><span data-stu-id="7ca26-128">System requirements for Finance</span></span>

<span data-ttu-id="7ca26-129">Para utilizar la solución de integración de Project Service Automation en Finance, debe instalar Enterprise Edition 7.3 con Platform update 12 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7ca26-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="7ca26-130">Requisitos del sistema para Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7ca26-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="7ca26-131">Para utilizar la solución de integración de Project Service Automation en Finance, debe instalar los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="7ca26-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="7ca26-132">Dynamics 365 Project Service Automation versión 9.0.0.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7ca26-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="7ca26-133">Perspectiva de la solución de efectivo para Dynamics 365 Sales, versión 1.14.0.0 (v14) o posterior</span><span class="sxs-lookup"><span data-stu-id="7ca26-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="7ca26-134">Solución de Project Service Automation para Finance para Dynamics 365 Project Service Automation, versión 1.0.0.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7ca26-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="7ca26-135">Instale la solución de integración de Project Service Automation con Finance en su instancia de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7ca26-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="7ca26-136">Descargue la solución de integración de Project Service Automation con Finance de [Centro de descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) y siga las instrucciones que se incluyen con la solución.</span><span class="sxs-lookup"><span data-stu-id="7ca26-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
