---
title: Introducción al reconocimiento de ingresos
description: En este tema se proporciona información acerca de reconocimiento de ingresos en Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531560"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="d8bff-103">Introducción al reconocimiento de ingresos</span><span class="sxs-lookup"><span data-stu-id="d8bff-103">Revenue recognition overview</span></span>

<span data-ttu-id="d8bff-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="d8bff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d8bff-105">En Dynamics 365 Project Operations, los principios de reconocimiento de ingresos varían según el método de facturación seleccionado para un proyecto o parte del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d8bff-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="d8bff-106">En este tema se proporciona información acerca de reconocimiento de ingresos en Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d8bff-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="d8bff-107">Transacciones contabilizadas usando el método de facturación de tiempo y material</span><span class="sxs-lookup"><span data-stu-id="d8bff-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="d8bff-108">El reconocimiento de costes e ingresos están conectados.</span><span class="sxs-lookup"><span data-stu-id="d8bff-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="d8bff-109">El coste de transacción y las ventas no facturadas se registran utilizando el [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="d8bff-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="d8bff-110">El perfil de costes e ingresos del proyecto determina si las transacciones de ventas no facturadas se registran en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="d8bff-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="d8bff-111">Si se ha seleccionado **Ingresos acumulados**, el sistema utiliza las cuentas de **Trabajo en proceso - Valor de ventas** y **Ingresos acumulados - Valor de ventas** durante el registro.</span><span class="sxs-lookup"><span data-stu-id="d8bff-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="d8bff-112">A continuación se muestra un ejemplo de este método.</span><span class="sxs-lookup"><span data-stu-id="d8bff-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="d8bff-113">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="d8bff-113">Transaction type</span></span> | <span data-ttu-id="d8bff-114">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="d8bff-114">Debit/Credit</span></span> | <span data-ttu-id="d8bff-115">Importe</span><span class="sxs-lookup"><span data-stu-id="d8bff-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d8bff-116">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="d8bff-116">WIP Sales value</span></span> | <span data-ttu-id="d8bff-117">Débito</span><span class="sxs-lookup"><span data-stu-id="d8bff-117">Debit</span></span> | <span data-ttu-id="d8bff-118">100</span><span class="sxs-lookup"><span data-stu-id="d8bff-118">100</span></span> |
  | <span data-ttu-id="d8bff-119">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="d8bff-119">Accrued revenue sales value</span></span> | <span data-ttu-id="d8bff-120">Crédito</span><span class="sxs-lookup"><span data-stu-id="d8bff-120">Credit</span></span> | <span data-ttu-id="d8bff-121">100</span><span class="sxs-lookup"><span data-stu-id="d8bff-121">100</span></span> |

- <span data-ttu-id="d8bff-122">Los ingresos se reconocen durante la facturación.</span><span class="sxs-lookup"><span data-stu-id="d8bff-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="d8bff-123">El sistema utiliza la cuenta de **Ingresos facturados** durante el registro.</span><span class="sxs-lookup"><span data-stu-id="d8bff-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="d8bff-124">A continuación se muestra un ejemplo de este método.</span><span class="sxs-lookup"><span data-stu-id="d8bff-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="d8bff-125">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="d8bff-125">Transaction type</span></span> | <span data-ttu-id="d8bff-126">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="d8bff-126">Debit/Credit</span></span> | <span data-ttu-id="d8bff-127">Importe</span><span class="sxs-lookup"><span data-stu-id="d8bff-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d8bff-128">Saldo del cliente</span><span class="sxs-lookup"><span data-stu-id="d8bff-128">Customer balance</span></span> | <span data-ttu-id="d8bff-129">Débito</span><span class="sxs-lookup"><span data-stu-id="d8bff-129">Debit</span></span> | <span data-ttu-id="d8bff-130">120</span><span class="sxs-lookup"><span data-stu-id="d8bff-130">120</span></span> |
  | <span data-ttu-id="d8bff-131">Impuestos repercutidos</span><span class="sxs-lookup"><span data-stu-id="d8bff-131">Sales tax payable</span></span> | <span data-ttu-id="d8bff-132">Crédito</span><span class="sxs-lookup"><span data-stu-id="d8bff-132">Credit</span></span> | <span data-ttu-id="d8bff-133">20</span><span class="sxs-lookup"><span data-stu-id="d8bff-133">20</span></span> |
  | <span data-ttu-id="d8bff-134">Ingresos facturados</span><span class="sxs-lookup"><span data-stu-id="d8bff-134">Invoiced Revenue</span></span> | <span data-ttu-id="d8bff-135">Crédito</span><span class="sxs-lookup"><span data-stu-id="d8bff-135">Credit</span></span> | <span data-ttu-id="d8bff-136">100</span><span class="sxs-lookup"><span data-stu-id="d8bff-136">100</span></span> |

- <span data-ttu-id="d8bff-137">Si se acumularon ingresos cuando se registraron las ventas sin facturar, el sistema revertirá los ingresos acumulados al momento de la facturación.</span><span class="sxs-lookup"><span data-stu-id="d8bff-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="d8bff-138">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="d8bff-138">Transaction type</span></span> | <span data-ttu-id="d8bff-139">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="d8bff-139">Debit/Credit</span></span> | <span data-ttu-id="d8bff-140">Importe</span><span class="sxs-lookup"><span data-stu-id="d8bff-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d8bff-141">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="d8bff-141">WIP Sales value</span></span> | <span data-ttu-id="d8bff-142">Crédito</span><span class="sxs-lookup"><span data-stu-id="d8bff-142">Credit</span></span> | <span data-ttu-id="d8bff-143">100</span><span class="sxs-lookup"><span data-stu-id="d8bff-143">100</span></span> |
  | <span data-ttu-id="d8bff-144">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="d8bff-144">Accrued revenue sales value</span></span> | <span data-ttu-id="d8bff-145">Débito</span><span class="sxs-lookup"><span data-stu-id="d8bff-145">Debit</span></span> | <span data-ttu-id="d8bff-146">100</span><span class="sxs-lookup"><span data-stu-id="d8bff-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="d8bff-147">Transacciones contabilizadas usando el método de facturación de precio fijo</span><span class="sxs-lookup"><span data-stu-id="d8bff-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="d8bff-148">El reconocimiento de costes e ingresos son independientes.</span><span class="sxs-lookup"><span data-stu-id="d8bff-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="d8bff-149">El coste de transacción se registra utilizando el [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="d8bff-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="d8bff-150">No se crean transacciones de ventas sin facturar.</span><span class="sxs-lookup"><span data-stu-id="d8bff-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="d8bff-151">Los ingresos se pueden reconocer durante la facturación si el perfil de costes e ingresos del proyecto tiene el **Principio utilizado para los cálculos de finalización de proyectos** establecido en **Sin trabajo en curso**.</span><span class="sxs-lookup"><span data-stu-id="d8bff-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="d8bff-152">Utilice este método solo para proyectos sencillos a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="d8bff-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="d8bff-153">Los ingresos se pueden reconocer utilizando estimaciones de ingresos a precio fijo, con el método **Contrato completado** o **Reconocimiento de ingresos de porcentaje de finalización**.</span><span class="sxs-lookup"><span data-stu-id="d8bff-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8bff-154">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d8bff-154">Additional resources</span></span>
[<span data-ttu-id="d8bff-155">Artículo Configurar la contabilidad para proyectos facturables</span><span class="sxs-lookup"><span data-stu-id="d8bff-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="d8bff-156">Proyectos de estimación de ingresos a precio fijo</span><span class="sxs-lookup"><span data-stu-id="d8bff-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="d8bff-157">Administrar estimaciones de ingresos</span><span class="sxs-lookup"><span data-stu-id="d8bff-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="d8bff-158">Coste para completar métodos</span><span class="sxs-lookup"><span data-stu-id="d8bff-158">Cost to complete methods</span></span>](cost-complete-methods.md)
