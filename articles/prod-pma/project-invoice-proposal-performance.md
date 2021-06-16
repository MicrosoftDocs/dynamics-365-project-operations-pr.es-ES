---
title: Rendimiento de propuesta de factura de proyecto
description: Este tema proporciona información sobre las mejoras de rendimiento de las propuestas de factura del proyecto.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920323"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="fc29c-103">Rendimiento de propuesta de factura de proyecto</span><span class="sxs-lookup"><span data-stu-id="fc29c-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc29c-104">Cuando crea una nueva propuesta de factura, puede encontrar problemas de rendimiento a medida que aumenta el número de proyectos y subproyectos.</span><span class="sxs-lookup"><span data-stu-id="fc29c-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="fc29c-105">Para mejorar el rendimiento, se encuentra disponible una característica que reduce el tiempo necesario para crear una nueva propuesta de factura para las transacciones de proyecto registradas.</span><span class="sxs-lookup"><span data-stu-id="fc29c-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="fc29c-106">Habilitar la mejora del rendimiento de propuesta de factura de proyecto</span><span class="sxs-lookup"><span data-stu-id="fc29c-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="fc29c-107">Para habilitar la característica de mejora del rendimiento de la propuesta de factura del proyecto, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="fc29c-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="fc29c-108">Vaya a **Administración de características** > **Todas**.</span><span class="sxs-lookup"><span data-stu-id="fc29c-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="fc29c-109">En la lista de características, ubique la **Mejora del rendimiento de la propuesta de factura del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="fc29c-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="fc29c-110">Seleccione **Habilitar ahora**.</span><span class="sxs-lookup"><span data-stu-id="fc29c-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="fc29c-111">Actualice su navegador y luego cree una nueva propuesta de factura.</span><span class="sxs-lookup"><span data-stu-id="fc29c-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="fc29c-112">Deshabilitar la mejora del rendimiento de propuesta de factura de proyecto</span><span class="sxs-lookup"><span data-stu-id="fc29c-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="fc29c-113">Complete los siguientes pasos para deshabilitar la característica de mejora del rendimiento de la propuesta de factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="fc29c-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="fc29c-114">Vaya a **Administración de características** > **Todas**.</span><span class="sxs-lookup"><span data-stu-id="fc29c-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="fc29c-115">En la lista de características, ubique la **Mejora del rendimiento de la propuesta de factura del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="fc29c-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="fc29c-116">Seleccione **Deshabilitar**.</span><span class="sxs-lookup"><span data-stu-id="fc29c-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="fc29c-117">Actualice el explorador.</span><span class="sxs-lookup"><span data-stu-id="fc29c-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="fc29c-118">El rendimiento de la propuesta de factura no se puede aplicar cuando las reglas de facturación están habilitadas o los procesos por lotes se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="fc29c-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>