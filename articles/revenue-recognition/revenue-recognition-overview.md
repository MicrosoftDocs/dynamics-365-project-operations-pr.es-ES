---
title: Introducción al reconocimiento de ingresos
description: En este tema se proporciona información acerca de reconocimiento de ingresos en Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368047"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="9feca-103">Introducción al reconocimiento de ingresos</span><span class="sxs-lookup"><span data-stu-id="9feca-103">Revenue recognition overview</span></span>

<span data-ttu-id="9feca-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="9feca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9feca-105">En Dynamics 365 Project Operations, los principios de reconocimiento de ingresos varían según el método de facturación seleccionado para un proyecto o parte del proyecto.</span><span class="sxs-lookup"><span data-stu-id="9feca-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="9feca-106">En este tema se proporciona información acerca de reconocimiento de ingresos en Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9feca-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="9feca-107">Transacciones contabilizadas usando el método de facturación de tiempo y material</span><span class="sxs-lookup"><span data-stu-id="9feca-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="9feca-108">El reconocimiento de costes e ingresos están conectados.</span><span class="sxs-lookup"><span data-stu-id="9feca-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="9feca-109">El coste de transacción y las ventas no facturadas se registran utilizando el [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="9feca-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="9feca-110">El perfil de costes e ingresos del proyecto determina si las transacciones de ventas no facturadas se registran en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="9feca-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="9feca-111">Si se ha seleccionado **Ingresos acumulados**, el sistema utiliza las cuentas de **Trabajo en proceso - Valor de ventas** y **Ingresos acumulados - Valor de ventas** durante el registro.</span><span class="sxs-lookup"><span data-stu-id="9feca-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="9feca-112">A continuación, se muestra ejemplo de este método.</span><span class="sxs-lookup"><span data-stu-id="9feca-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="9feca-113">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="9feca-113">Transaction type</span></span> | <span data-ttu-id="9feca-114">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="9feca-114">Debit/Credit</span></span> | <span data-ttu-id="9feca-115">Importe</span><span class="sxs-lookup"><span data-stu-id="9feca-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="9feca-116">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="9feca-116">WIP Sales value</span></span> | <span data-ttu-id="9feca-117">Debe</span><span class="sxs-lookup"><span data-stu-id="9feca-117">Debit</span></span> | <span data-ttu-id="9feca-118">100</span><span class="sxs-lookup"><span data-stu-id="9feca-118">100</span></span> |
  | <span data-ttu-id="9feca-119">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="9feca-119">Accrued revenue sales value</span></span> | <span data-ttu-id="9feca-120">Haber</span><span class="sxs-lookup"><span data-stu-id="9feca-120">Credit</span></span> | <span data-ttu-id="9feca-121">100</span><span class="sxs-lookup"><span data-stu-id="9feca-121">100</span></span> |

- <span data-ttu-id="9feca-122">Los ingresos se reconocen durante la facturación.</span><span class="sxs-lookup"><span data-stu-id="9feca-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="9feca-123">El sistema utiliza la cuenta de **Ingresos facturados** durante el registro.</span><span class="sxs-lookup"><span data-stu-id="9feca-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="9feca-124">A continuación, se muestra ejemplo de este método.</span><span class="sxs-lookup"><span data-stu-id="9feca-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="9feca-125">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="9feca-125">Transaction type</span></span> | <span data-ttu-id="9feca-126">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="9feca-126">Debit/Credit</span></span> | <span data-ttu-id="9feca-127">Importe</span><span class="sxs-lookup"><span data-stu-id="9feca-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="9feca-128">Saldo del cliente</span><span class="sxs-lookup"><span data-stu-id="9feca-128">Customer balance</span></span> | <span data-ttu-id="9feca-129">Débito</span><span class="sxs-lookup"><span data-stu-id="9feca-129">Debit</span></span> | <span data-ttu-id="9feca-130">120</span><span class="sxs-lookup"><span data-stu-id="9feca-130">120</span></span> |
  | <span data-ttu-id="9feca-131">Impuestos repercutidos</span><span class="sxs-lookup"><span data-stu-id="9feca-131">Sales tax payable</span></span> | <span data-ttu-id="9feca-132">Crédito</span><span class="sxs-lookup"><span data-stu-id="9feca-132">Credit</span></span> | <span data-ttu-id="9feca-133">20</span><span class="sxs-lookup"><span data-stu-id="9feca-133">20</span></span> |
  | <span data-ttu-id="9feca-134">Ingresos facturados</span><span class="sxs-lookup"><span data-stu-id="9feca-134">Invoiced Revenue</span></span> | <span data-ttu-id="9feca-135">Crédito</span><span class="sxs-lookup"><span data-stu-id="9feca-135">Credit</span></span> | <span data-ttu-id="9feca-136">100</span><span class="sxs-lookup"><span data-stu-id="9feca-136">100</span></span> |

- <span data-ttu-id="9feca-137">Si se acumularon ingresos cuando se registraron las ventas sin facturar, el sistema revertirá los ingresos acumulados al momento de la facturación.</span><span class="sxs-lookup"><span data-stu-id="9feca-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="9feca-138">Tipo de transacción</span><span class="sxs-lookup"><span data-stu-id="9feca-138">Transaction type</span></span> | <span data-ttu-id="9feca-139">Debe/Haber</span><span class="sxs-lookup"><span data-stu-id="9feca-139">Debit/Credit</span></span> | <span data-ttu-id="9feca-140">Importe</span><span class="sxs-lookup"><span data-stu-id="9feca-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="9feca-141">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="9feca-141">WIP Sales value</span></span> | <span data-ttu-id="9feca-142">Crédito</span><span class="sxs-lookup"><span data-stu-id="9feca-142">Credit</span></span> | <span data-ttu-id="9feca-143">100</span><span class="sxs-lookup"><span data-stu-id="9feca-143">100</span></span> |
  | <span data-ttu-id="9feca-144">Trabajo en proceso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="9feca-144">Accrued revenue sales value</span></span> | <span data-ttu-id="9feca-145">Débito</span><span class="sxs-lookup"><span data-stu-id="9feca-145">Debit</span></span> | <span data-ttu-id="9feca-146">100</span><span class="sxs-lookup"><span data-stu-id="9feca-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="9feca-147">Transacciones contabilizadas usando el método de facturación de precio fijo</span><span class="sxs-lookup"><span data-stu-id="9feca-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="9feca-148">El reconocimiento de costes e ingresos son independientes.</span><span class="sxs-lookup"><span data-stu-id="9feca-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="9feca-149">El coste de transacción se registra utilizando el [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="9feca-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="9feca-150">No se crean transacciones de ventas sin facturar.</span><span class="sxs-lookup"><span data-stu-id="9feca-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="9feca-151">Los ingresos se pueden reconocer durante la facturación si el perfil de costes e ingresos del proyecto tiene el **Principio utilizado para los cálculos de finalización de proyectos** establecido en **Sin trabajo en curso**.</span><span class="sxs-lookup"><span data-stu-id="9feca-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="9feca-152">Utilice este método solo para proyectos sencillos a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="9feca-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="9feca-153">Los ingresos se pueden reconocer utilizando estimaciones de ingresos a precio fijo, con el método **Contrato completado** o **Reconocimiento de ingresos de porcentaje de finalización**.</span><span class="sxs-lookup"><span data-stu-id="9feca-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9feca-154">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9feca-154">Additional resources</span></span>
[<span data-ttu-id="9feca-155">Artículo Configurar la contabilidad para proyectos facturables</span><span class="sxs-lookup"><span data-stu-id="9feca-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="9feca-156">Proyectos de estimación de ingresos a precio fijo</span><span class="sxs-lookup"><span data-stu-id="9feca-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="9feca-157">Administrar estimaciones de ingresos</span><span class="sxs-lookup"><span data-stu-id="9feca-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="9feca-158">Coste para completar métodos</span><span class="sxs-lookup"><span data-stu-id="9feca-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]