---
title: Cancelar entradas de gastos y tiempo aprobadas anteriormente
description: En este tema se proporciona información sobre cómo cancelar una transacción de gastos y tiempo de proyecto aprobada.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150599"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="64524-103">Cancelar entradas de gastos o tiempo aprobadas anteriormente</span><span class="sxs-lookup"><span data-stu-id="64524-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="64524-104">En la versión más reciente de Dynamics 365 Project Service Automation, los aprobadores pueden cancelar las entradas de gasto o tiempo que aprobaron anteriormente.</span><span class="sxs-lookup"><span data-stu-id="64524-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="64524-105">Cancelar una entrada de gastos o tiempo aprobada anteriormente</span><span class="sxs-lookup"><span data-stu-id="64524-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="64524-106">Siga estos pasos para cancelar una entrada de gastos o tiempo aprobada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="64524-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="64524-107">Vaya a **Proyectos** \> **Mi trabajo** \> **Aprobaciones**.</span><span class="sxs-lookup"><span data-stu-id="64524-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="64524-108">En la página de lista **Aprobaciones**, cambie la vista a **Mis aprobaciones anteriores**.</span><span class="sxs-lookup"><span data-stu-id="64524-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="64524-109">Se mostrará una lista de las entradas de gastos y tiempo aprobadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="64524-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="64524-110">Seleccione una o varias entradas y después seleccione **Cancelar aprobación**.</span><span class="sxs-lookup"><span data-stu-id="64524-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="64524-111">Recibirá un mensaje de advertencia.</span><span class="sxs-lookup"><span data-stu-id="64524-111">You receive a warning message.</span></span>
4. <span data-ttu-id="64524-112">Seleccione **Aceptar** para cancelar la aprobación.</span><span class="sxs-lookup"><span data-stu-id="64524-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="64524-113">Comprender el impacto de cancelar una aprobación de una entrada de gastos o tiempo</span><span class="sxs-lookup"><span data-stu-id="64524-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="64524-114">Cuando se cancela una aprobación, hay un impacto tanto operativo como financiero.</span><span class="sxs-lookup"><span data-stu-id="64524-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="64524-115">Impacto operativo</span><span class="sxs-lookup"><span data-stu-id="64524-115">Operational impact</span></span>

<span data-ttu-id="64524-116">En lo que respecta a las operaciones, cuando se cancela una aprobación, el estado del registro se restablece a **Borrador** y la aprobación deja de aparecer en la vista **Mis aprobaciones anteriores**.</span><span class="sxs-lookup"><span data-stu-id="64524-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="64524-117">En su lugar, la aprobación cancelada aparece en la vista **Entradas de horas para aprobación** o la vista **Entradas de gastos para aprobación**, dependiendo de si se trataba de una entrada de tiempo o de gastos.</span><span class="sxs-lookup"><span data-stu-id="64524-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="64524-118">Además, el estado de la entrada de gastos o de tiempo relacionado se cambia a **Enviado** para que la entrada relacionada sea homogénea con las aprobaciones que tienen un estado de **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="64524-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="64524-119">Como aprobador, podrá editar algunos de los campos de las aprobaciones que tengan el estado de **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="64524-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="64524-120">Entre estos campos se incluyen los campos **Tipo de facturación** y **Horas facturables para entradas de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="64524-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="64524-121">Tras realizar los cambios, podrá volver a aprobar el registro.</span><span class="sxs-lookup"><span data-stu-id="64524-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="64524-122">De manera alternativa, puede rechazar la entrada.</span><span class="sxs-lookup"><span data-stu-id="64524-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="64524-123">Si rechaza la aprobación de una entrada de tiempo, el estado de la entrada cambiará a **Devuelto**.</span><span class="sxs-lookup"><span data-stu-id="64524-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="64524-124">Si rechaza la aprobación de una entrada de gastos, el estado cambiará a **Rechazado**.</span><span class="sxs-lookup"><span data-stu-id="64524-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="64524-125">Funcionalmente, tanto las entradas devueltas como las rechazadas se comportan igual que una entrada con el estado de **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="64524-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="64524-126">Un miembro del equipo del proyecto puede realizar cualquier cambio necesario en la entrada y después volver a enviarla para su aprobación, o bien puede eliminar la entrada por completo.</span><span class="sxs-lookup"><span data-stu-id="64524-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="64524-127">Impacto financiero</span><span class="sxs-lookup"><span data-stu-id="64524-127">Financial impact</span></span>

<span data-ttu-id="64524-128">El proyecto también se ve afectado desde el punto de vista financiero cuando se cancela una aprobación.</span><span class="sxs-lookup"><span data-stu-id="64524-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="64524-129">En primer lugar, los datos reales correspondientes de costes y ventas se actualizan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="64524-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="64524-130">El estado de ajuste se establece en **Ajustado**.</span><span class="sxs-lookup"><span data-stu-id="64524-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="64524-131">El estado de la facturación se establece en **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="64524-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="64524-132">A continuación, se crean movimientos de retrocesión en la tabla Datos reales.</span><span class="sxs-lookup"><span data-stu-id="64524-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="64524-133">Para crear entradas de retrocesión, el sistema copia los valores de campo desde los datos reales originales.</span><span class="sxs-lookup"><span data-stu-id="64524-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="64524-134">Los únicos valores que no se copian son los valores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="64524-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="64524-135">En su lugar, estos valores se revierten.</span><span class="sxs-lookup"><span data-stu-id="64524-135">These values are reversed instead.</span></span> <span data-ttu-id="64524-136">A continuación, se crean datos reales revertidos para los datos reales **Coste** y **Ventas sin facturar**.</span><span class="sxs-lookup"><span data-stu-id="64524-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="64524-137">El campo **Estado del ajuste** de los datos reales revertidos se establece en **No ajustable** y el estado de facturación se establece en **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="64524-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="64524-138">Tras realizar estos cambios, el importe que se registra como gasto en el proyecto y la acumulación de ingresos del proyecto dejarán de representar los importes que representan esos datos reales.</span><span class="sxs-lookup"><span data-stu-id="64524-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
