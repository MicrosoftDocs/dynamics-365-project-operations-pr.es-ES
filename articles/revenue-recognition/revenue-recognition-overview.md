---
title: Introducción al reconocimiento de ingresos
description: En este tema se proporciona información acerca de reconocimiento de ingresos en Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013777"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="ab35d-103">Introducción al reconocimiento de ingresos</span><span class="sxs-lookup"><span data-stu-id="ab35d-103">Revenue recognition overview</span></span>

<span data-ttu-id="ab35d-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="ab35d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ab35d-105">En Dynamics 365 Project Operations, los principios de reconocimiento de ingresos varían según el método de facturación seleccionado para un proyecto o parte del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ab35d-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="ab35d-106">En este tema se proporciona información acerca de reconocimiento de ingresos en Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ab35d-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="ab35d-107">Transacciones contabilizadas usando el método de facturación de tiempo y material</span><span class="sxs-lookup"><span data-stu-id="ab35d-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="ab35d-108">El reconocimiento de costes e ingresos están conectados.</span><span class="sxs-lookup"><span data-stu-id="ab35d-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="ab35d-109">El coste de transacción y las ventas no facturadas se registran utilizando el [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="ab35d-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="ab35d-110">El perfil de costes e ingresos del proyecto determina si las transacciones de ventas no facturadas se registran en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="ab35d-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="ab35d-111">Si se ha seleccionado **Ingresos acumulados**, el sistema utiliza las cuentas de **Trabajo en proceso - Valor de ventas** y **Ingresos acumulados - Valor de ventas** durante el registro.</span><span class="sxs-lookup"><span data-stu-id="ab35d-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="ab35d-112">A continuación, se muestra ejemplo de este método.</span><span class="sxs-lookup"><span data-stu-id="ab35d-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="ab35d-113">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="ab35d-113">Transaction type</span></span> | <span data-ttu-id="ab35d-114">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="ab35d-114">Debit/Credit</span></span> | <span data-ttu-id="ab35d-115">Importe</span><span class="sxs-lookup"><span data-stu-id="ab35d-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ab35d-116">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="ab35d-116">WIP Sales value</span></span> | <span data-ttu-id="ab35d-117">Debe</span><span class="sxs-lookup"><span data-stu-id="ab35d-117">Debit</span></span> | <span data-ttu-id="ab35d-118">100</span><span class="sxs-lookup"><span data-stu-id="ab35d-118">100</span></span> |
  | <span data-ttu-id="ab35d-119">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="ab35d-119">Accrued revenue sales value</span></span> | <span data-ttu-id="ab35d-120">Haber</span><span class="sxs-lookup"><span data-stu-id="ab35d-120">Credit</span></span> | <span data-ttu-id="ab35d-121">100</span><span class="sxs-lookup"><span data-stu-id="ab35d-121">100</span></span> |

- <span data-ttu-id="ab35d-122">Los ingresos se reconocen durante la facturación.</span><span class="sxs-lookup"><span data-stu-id="ab35d-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="ab35d-123">El sistema utiliza la cuenta de **Ingresos facturados** durante el registro.</span><span class="sxs-lookup"><span data-stu-id="ab35d-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="ab35d-124">A continuación, se muestra ejemplo de este método.</span><span class="sxs-lookup"><span data-stu-id="ab35d-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="ab35d-125">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="ab35d-125">Transaction type</span></span> | <span data-ttu-id="ab35d-126">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="ab35d-126">Debit/Credit</span></span> | <span data-ttu-id="ab35d-127">Importe</span><span class="sxs-lookup"><span data-stu-id="ab35d-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ab35d-128">Saldo del cliente</span><span class="sxs-lookup"><span data-stu-id="ab35d-128">Customer balance</span></span> | <span data-ttu-id="ab35d-129">Débito</span><span class="sxs-lookup"><span data-stu-id="ab35d-129">Debit</span></span> | <span data-ttu-id="ab35d-130">120</span><span class="sxs-lookup"><span data-stu-id="ab35d-130">120</span></span> |
  | <span data-ttu-id="ab35d-131">Impuestos repercutidos</span><span class="sxs-lookup"><span data-stu-id="ab35d-131">Sales tax payable</span></span> | <span data-ttu-id="ab35d-132">Crédito</span><span class="sxs-lookup"><span data-stu-id="ab35d-132">Credit</span></span> | <span data-ttu-id="ab35d-133">20</span><span class="sxs-lookup"><span data-stu-id="ab35d-133">20</span></span> |
  | <span data-ttu-id="ab35d-134">Ingresos facturados</span><span class="sxs-lookup"><span data-stu-id="ab35d-134">Invoiced Revenue</span></span> | <span data-ttu-id="ab35d-135">Crédito</span><span class="sxs-lookup"><span data-stu-id="ab35d-135">Credit</span></span> | <span data-ttu-id="ab35d-136">100</span><span class="sxs-lookup"><span data-stu-id="ab35d-136">100</span></span> |

- <span data-ttu-id="ab35d-137">Si se acumularon ingresos cuando se registraron las ventas sin facturar, el sistema revertirá los ingresos acumulados al momento de la facturación.</span><span class="sxs-lookup"><span data-stu-id="ab35d-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="ab35d-138">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="ab35d-138">Transaction type</span></span> | <span data-ttu-id="ab35d-139">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="ab35d-139">Debit/Credit</span></span> | <span data-ttu-id="ab35d-140">Importe</span><span class="sxs-lookup"><span data-stu-id="ab35d-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ab35d-141">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="ab35d-141">WIP Sales value</span></span> | <span data-ttu-id="ab35d-142">Crédito</span><span class="sxs-lookup"><span data-stu-id="ab35d-142">Credit</span></span> | <span data-ttu-id="ab35d-143">100</span><span class="sxs-lookup"><span data-stu-id="ab35d-143">100</span></span> |
  | <span data-ttu-id="ab35d-144">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="ab35d-144">Accrued revenue sales value</span></span> | <span data-ttu-id="ab35d-145">Débito</span><span class="sxs-lookup"><span data-stu-id="ab35d-145">Debit</span></span> | <span data-ttu-id="ab35d-146">100</span><span class="sxs-lookup"><span data-stu-id="ab35d-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="ab35d-147">Transacciones contabilizadas usando el método de facturación de precio fijo</span><span class="sxs-lookup"><span data-stu-id="ab35d-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="ab35d-148">El reconocimiento de costes e ingresos son independientes.</span><span class="sxs-lookup"><span data-stu-id="ab35d-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="ab35d-149">El coste de transacción se registra utilizando el [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="ab35d-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="ab35d-150">No se crean transacciones de ventas sin facturar.</span><span class="sxs-lookup"><span data-stu-id="ab35d-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="ab35d-151">Los ingresos se pueden reconocer durante la facturación si el perfil de costes e ingresos del proyecto tiene el **Principio utilizado para los cálculos de finalización de proyectos** establecido en **Sin trabajo en curso**.</span><span class="sxs-lookup"><span data-stu-id="ab35d-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="ab35d-152">Utilice este método solo para proyectos sencillos a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="ab35d-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="ab35d-153">Los ingresos se pueden reconocer utilizando estimaciones de ingresos a precio fijo, con el método **Contrato completado** o **Reconocimiento de ingresos de porcentaje de finalización**.</span><span class="sxs-lookup"><span data-stu-id="ab35d-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab35d-154">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ab35d-154">Additional resources</span></span>
[<span data-ttu-id="ab35d-155">Artículo Configurar la contabilidad para proyectos facturables</span><span class="sxs-lookup"><span data-stu-id="ab35d-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="ab35d-156">Proyectos de estimación de ingresos a precio fijo</span><span class="sxs-lookup"><span data-stu-id="ab35d-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="ab35d-157">Administrar estimaciones de ingresos</span><span class="sxs-lookup"><span data-stu-id="ab35d-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="ab35d-158">Coste para completar métodos</span><span class="sxs-lookup"><span data-stu-id="ab35d-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]