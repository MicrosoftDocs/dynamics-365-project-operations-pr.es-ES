---
title: Información general de utilización de recursos
description: En este tema se proporciona información acerca de la vista de uso de recursos en Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000817"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="30c4c-103">Información general de utilización de recursos</span><span class="sxs-lookup"><span data-stu-id="30c4c-103">Resource utilization overview</span></span>

<span data-ttu-id="30c4c-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="30c4c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="30c4c-105">Los recursos pueden tener un uso facturable objetivo.</span><span class="sxs-lookup"><span data-stu-id="30c4c-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="30c4c-106">Este uso objetivo se define como un atributo en el rol predeterminado de un recurso o se establece en el registro del recurso individual que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="30c4c-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="30c4c-107">Los cálculos de uso se basan en las horas reales que los recursos han notificado mediante entradas de tiempo aprobadas.</span><span class="sxs-lookup"><span data-stu-id="30c4c-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="30c4c-108">Se utilizan las siguientes fórmulas para calcular el uso:</span><span class="sxs-lookup"><span data-stu-id="30c4c-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="30c4c-109">Uso facturable = Horas reales facturables ÷ Capacidad del recurso</span><span class="sxs-lookup"><span data-stu-id="30c4c-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="30c4c-110">Uso no facturable = Tiempo real con id. de tipo de facturación = No imputable, complementario o no disponible ÷ Capacidad del recurso</span><span class="sxs-lookup"><span data-stu-id="30c4c-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="30c4c-111">Interno = Tiempo real sin contrato de venta ÷ Capacidad del recurso</span><span class="sxs-lookup"><span data-stu-id="30c4c-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="30c4c-112">Capacidad del recurso = Horas de trabajo del recurso – Fuera de la oficina – Días festivos</span><span class="sxs-lookup"><span data-stu-id="30c4c-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="30c4c-113">Puede encontrar la vista **Uso de recursos** en el panel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="30c4c-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="30c4c-114">Cada celda de la cuadrícula representa el porcentaje de uso facturable del recurso en un período, como un día, una semana o un mes.</span><span class="sxs-lookup"><span data-stu-id="30c4c-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="30c4c-115">Se usan las siguientes fórmulas para colorear las celdas:</span><span class="sxs-lookup"><span data-stu-id="30c4c-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="30c4c-116">**Verde**: uso facturable >= uso de destino del recurso.</span><span class="sxs-lookup"><span data-stu-id="30c4c-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="30c4c-117">**Amarillo**: uso de destino – 20 <= uso facturable < uso de destino.</span><span class="sxs-lookup"><span data-stu-id="30c4c-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="30c4c-118">**Rojo**: uso facturable < uso de destino – 20.</span><span class="sxs-lookup"><span data-stu-id="30c4c-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="30c4c-119">Puesto que la vista **Uso de recursos** se basa en el tablero de programación, puede usar las capacidades de filtrado del tablero de programación para filtrar sus resultados.</span><span class="sxs-lookup"><span data-stu-id="30c4c-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="30c4c-120">La cuadrícula requiere que establezca un uso objetivo en el rol o en el recurso individual.</span><span class="sxs-lookup"><span data-stu-id="30c4c-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="30c4c-121">Para realizar esta configuración, vaya a **Recursos** > **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="30c4c-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="30c4c-122">Además, se debe asignar un rol predeterminado a cada recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="30c4c-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="30c4c-123">Vaya a **Recursos** > **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="30c4c-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="30c4c-124">En la pestaña **Project Service**, verifique que se haya definido un rol de recurso y que el campo **Es predeterminado** esté establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="30c4c-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="30c4c-125">Puede agregar roles adicionales en los que **Es predeterminado** = **No**.</span><span class="sxs-lookup"><span data-stu-id="30c4c-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="30c4c-126">El rol en el que **Es predeterminado** = **Sí** se usa para evaluar el uso del recurso en relación el objetivo para ese rol.</span><span class="sxs-lookup"><span data-stu-id="30c4c-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="30c4c-127">En la pestaña **Project Service** también puede establecer un uso objetivo individual para el recurso.</span><span class="sxs-lookup"><span data-stu-id="30c4c-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="30c4c-128">El cálculo de uso utiliza después ese uso objetivo para evaluar el objetivo del recurso en lugar del objetivo del rol predeterminado del recurso.</span><span class="sxs-lookup"><span data-stu-id="30c4c-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="30c4c-129">El uso solo se muestra para un recurso solo si ese recurso ha aprobado el tiempo imputable durante el período que se muestra en la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="30c4c-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]