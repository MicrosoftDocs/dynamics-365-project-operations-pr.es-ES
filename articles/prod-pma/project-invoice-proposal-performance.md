---
title: Rendimiento de propuesta de factura de proyecto
description: Este tema proporciona información sobre las mejoras de rendimiento de las propuestas de factura del proyecto.
author: Yowelle
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999512"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="3fe66-103">Rendimiento de propuesta de factura de proyecto</span><span class="sxs-lookup"><span data-stu-id="3fe66-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fe66-104">Cuando crea una nueva propuesta de factura, puede encontrar problemas de rendimiento a medida que aumenta el número de proyectos y subproyectos.</span><span class="sxs-lookup"><span data-stu-id="3fe66-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="3fe66-105">Para mejorar el rendimiento, se encuentra disponible una característica que reduce el tiempo necesario para crear una nueva propuesta de factura para las transacciones de proyecto registradas.</span><span class="sxs-lookup"><span data-stu-id="3fe66-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="3fe66-106">Habilitar la mejora del rendimiento de propuesta de factura de proyecto</span><span class="sxs-lookup"><span data-stu-id="3fe66-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="3fe66-107">Para habilitar la característica de mejora del rendimiento de la propuesta de factura del proyecto, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="3fe66-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="3fe66-108">Vaya a **Administración de características** > **Todas**.</span><span class="sxs-lookup"><span data-stu-id="3fe66-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="3fe66-109">En la lista de características, ubique la **Mejora del rendimiento de la propuesta de factura del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="3fe66-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="3fe66-110">Seleccione **Habilitar ahora**.</span><span class="sxs-lookup"><span data-stu-id="3fe66-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="3fe66-111">Actualice su navegador y luego cree una nueva propuesta de factura.</span><span class="sxs-lookup"><span data-stu-id="3fe66-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="3fe66-112">Deshabilitar la mejora del rendimiento de propuesta de factura de proyecto</span><span class="sxs-lookup"><span data-stu-id="3fe66-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="3fe66-113">Complete los siguientes pasos para deshabilitar la característica de mejora del rendimiento de la propuesta de factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="3fe66-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="3fe66-114">Vaya a **Administración de características** > **Todas**.</span><span class="sxs-lookup"><span data-stu-id="3fe66-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="3fe66-115">En la lista de características, ubique la **Mejora del rendimiento de la propuesta de factura del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="3fe66-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="3fe66-116">Seleccione **Deshabilitar**.</span><span class="sxs-lookup"><span data-stu-id="3fe66-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="3fe66-117">Actualice el explorador.</span><span class="sxs-lookup"><span data-stu-id="3fe66-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="3fe66-118">El rendimiento de la propuesta de factura no se puede aplicar cuando las reglas de facturación están habilitadas o los procesos por lotes se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="3fe66-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
