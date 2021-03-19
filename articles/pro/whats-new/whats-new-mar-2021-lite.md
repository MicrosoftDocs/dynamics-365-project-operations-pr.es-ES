---
title: 'Novedades de marzo de 2021: implementación ligera de Project Operations'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de marzo de 2021 de la implementación ligera de Project Operations.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500044"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="7f580-103">Novedades de marzo de 2021: implementación ligera de Project Operations</span><span class="sxs-lookup"><span data-stu-id="7f580-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="7f580-104">_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="7f580-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7f580-105">Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="7f580-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="7f580-106">Project Operations en el entorno de Dataverse versión 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="7f580-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="7f580-107">Actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="7f580-107">Quality updates</span></span>

| <span data-ttu-id="7f580-108">**Área de características**</span><span class="sxs-lookup"><span data-stu-id="7f580-108">**Feature area**</span></span> | <span data-ttu-id="7f580-109">**Número de referencia**</span><span class="sxs-lookup"><span data-stu-id="7f580-109">**Reference number**</span></span> | <span data-ttu-id="7f580-110">**Actualización de calidad**</span><span class="sxs-lookup"><span data-stu-id="7f580-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7f580-111">Facturación y precios</span><span class="sxs-lookup"><span data-stu-id="7f580-111">Billing and pricing</span></span> | <span data-ttu-id="7f580-112">2133873</span><span class="sxs-lookup"><span data-stu-id="7f580-112">2133873</span></span> | <span data-ttu-id="7f580-113">Se corrigió la visualización del símbolo de moneda de **Precio de venta unitario** en la cuadrícula **Estimaciones de gastos**.</span><span class="sxs-lookup"><span data-stu-id="7f580-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="7f580-114">Facturación y precios</span><span class="sxs-lookup"><span data-stu-id="7f580-114">Billing and pricing</span></span> | <span data-ttu-id="7f580-115">2174616</span><span class="sxs-lookup"><span data-stu-id="7f580-115">2174616</span></span> | <span data-ttu-id="7f580-116">Cuando se gana una cotización, se hace referencia a la lista de precios personalizada del contrato en los detalles de la línea del contrato que se copian de la cotización.</span><span class="sxs-lookup"><span data-stu-id="7f580-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="7f580-117">Administración de oportunidades</span><span class="sxs-lookup"><span data-stu-id="7f580-117">Opportunity Management</span></span> | <span data-ttu-id="7f580-118">2167475</span><span class="sxs-lookup"><span data-stu-id="7f580-118">2167475</span></span> | <span data-ttu-id="7f580-119">Importe de impuesto fijo en la factura de corrección que originó una entrada real no facturada.</span><span class="sxs-lookup"><span data-stu-id="7f580-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="7f580-120">Administración de oportunidades</span><span class="sxs-lookup"><span data-stu-id="7f580-120">Opportunity Management</span></span> | <span data-ttu-id="7f580-121">2176285</span><span class="sxs-lookup"><span data-stu-id="7f580-121">2176285</span></span> | <span data-ttu-id="7f580-122">El monto del impuesto no debe copiarse de los detalles del contrato de venta / línea de cotización a los detalles del contrato de costo / línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="7f580-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="7f580-123">Administración de oportunidades</span><span class="sxs-lookup"><span data-stu-id="7f580-123">Opportunity Management</span></span> | <span data-ttu-id="7f580-124">2188079</span><span class="sxs-lookup"><span data-stu-id="7f580-124">2188079</span></span> | <span data-ttu-id="7f580-125">No se debe crear una regla de facturación dividida para contratos que no se basan en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7f580-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="7f580-126">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="7f580-126">Planning and Tracking</span></span> | <span data-ttu-id="7f580-127">2138853</span><span class="sxs-lookup"><span data-stu-id="7f580-127">2138853</span></span> | <span data-ttu-id="7f580-128">Se actualizó la función de copia del proyecto para garantizar que las líneas de estimación de gastos que las tareas de referencia se copien en el proyecto de destino.</span><span class="sxs-lookup"><span data-stu-id="7f580-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="7f580-129">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="7f580-129">Planning and Tracking</span></span> | <span data-ttu-id="7f580-130">2173259</span><span class="sxs-lookup"><span data-stu-id="7f580-130">2173259</span></span> | <span data-ttu-id="7f580-131">Se actualizó la función de copia del proyecto para garantizar que no se muestre el mensaje de error **Copiando WBS** en ciertos escenarios.</span><span class="sxs-lookup"><span data-stu-id="7f580-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="7f580-132">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="7f580-132">Time and Expense</span></span> | <span data-ttu-id="7f580-133">2148910</span><span class="sxs-lookup"><span data-stu-id="7f580-133">2148910</span></span> | <span data-ttu-id="7f580-134">Problema de pantalla solucionado con la página **Editar entrada** en la cuadrícula **Entrada de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="7f580-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="7f580-135">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="7f580-135">Time and Expense</span></span> | <span data-ttu-id="7f580-136">2159798</span><span class="sxs-lookup"><span data-stu-id="7f580-136">2159798</span></span> | <span data-ttu-id="7f580-137">Controles más estrictos para garantizar que las entradas de gastos aprobadas no se puedan editar.</span><span class="sxs-lookup"><span data-stu-id="7f580-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


