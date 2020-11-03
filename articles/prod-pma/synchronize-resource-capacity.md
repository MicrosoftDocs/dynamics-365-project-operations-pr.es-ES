---
title: Sincronizar la capacidad de los recursos
description: Este tema proporciona información sobre cómo sincronizar la capacidad de un recurso entre calendarios y proyectos.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085126"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="69ea2-103">Sincronizar la capacidad de los recursos</span><span class="sxs-lookup"><span data-stu-id="69ea2-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69ea2-104">Los procesos para la sincronización de recursos ayudan a garantizar que la información para el calendario y el calendario base se incorpore a la programación de recursos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="69ea2-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="69ea2-105">Si se cambia el calendario, los procesos realizan las actualizaciones necesarias en la programación de los recursos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="69ea2-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="69ea2-106">Los procesos también ayudan a mejorar el rendimiento, porque la información de recursos del calendario se sincroniza de antemano.</span><span class="sxs-lookup"><span data-stu-id="69ea2-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="69ea2-107">Por lo tanto, las actualizaciones de la información de programación de recursos se producen más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="69ea2-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="69ea2-108">Le recomendamos que programe los procesos por lotes en lugar de uno a la vez.</span><span class="sxs-lookup"><span data-stu-id="69ea2-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="69ea2-109">De lo contrario, existe el riesgo de que alguien olvide las fechas inclusivas cuando se sincronizó la información por última vez.</span><span class="sxs-lookup"><span data-stu-id="69ea2-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="69ea2-110">Si no se utilizan fechas inclusivas, pueden producirse vacíos durante la sincronización de fechas.</span><span class="sxs-lookup"><span data-stu-id="69ea2-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sincronización de calendario](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="69ea2-112">Sincronizar acumulaciones de capacidad de los recursos</span><span class="sxs-lookup"><span data-stu-id="69ea2-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="69ea2-113">El proceso de sincronización está diseñado para sincronizar toda la información del calendario de recursos.</span><span class="sxs-lookup"><span data-stu-id="69ea2-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="69ea2-114">Esta información incluye información del calendario base sobre cualquier cambio en la tabla de capacidad del calendario de recursos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="69ea2-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="69ea2-115">Si se agregan nuevos recursos al proyecto, la sincronización ayuda a garantizar que la información actualizada del calendario esté disponible.</span><span class="sxs-lookup"><span data-stu-id="69ea2-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="69ea2-116">Esta sincronización se puede realizar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="69ea2-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="69ea2-117">Se recomienda usar un lote.</span><span class="sxs-lookup"><span data-stu-id="69ea2-117">We recommend that you use a batch.</span></span> <span data-ttu-id="69ea2-118">Las opciones están disponibles durante la sincronización de las reservas de capacidad.</span><span class="sxs-lookup"><span data-stu-id="69ea2-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="69ea2-119">Seleccione **Gestión de proyectos y contabilidad** &gt; **Periódico** &gt; **Sincronización de capacidad** &gt; **Sincronizar acumulaciones de capacidad de recursos**.</span><span class="sxs-lookup"><span data-stu-id="69ea2-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="69ea2-120">Configure las opciones en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="69ea2-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="69ea2-121">Opción</span><span class="sxs-lookup"><span data-stu-id="69ea2-121">Option</span></span>      | <span data-ttu-id="69ea2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="69ea2-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="69ea2-123">Código de período</span><span class="sxs-lookup"><span data-stu-id="69ea2-123">Period code</span></span> | <span data-ttu-id="69ea2-124">Opcionalmente, seleccione el código de intervalo de fechas del Libro de contabilidad para establecer las fechas de inicio y finalización del proceso de sincronización para acumulaciones de capacidad de recursos.</span><span class="sxs-lookup"><span data-stu-id="69ea2-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="69ea2-125">Fecha de inicio</span><span class="sxs-lookup"><span data-stu-id="69ea2-125">Start date</span></span>  | <span data-ttu-id="69ea2-126">Especifique la fecha de inicio del proceso de sincronización para las acumulaciones de capacidad de recursos.</span><span class="sxs-lookup"><span data-stu-id="69ea2-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="69ea2-127">Fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="69ea2-127">End date</span></span>    | <span data-ttu-id="69ea2-128">Especifique la fecha de finalización para el proceso de sincronización para las acumulaciones de capacidad de recursos.</span><span class="sxs-lookup"><span data-stu-id="69ea2-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="69ea2-129">[![Procreso de sincronización](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="69ea2-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
