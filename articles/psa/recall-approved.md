---
title: Recuperación de las entradas de tiempo o gastos aprobados
description: En este tema se proporciona información sobre cómo recuperar una transacción de tiempo o gasto aprobada previamente.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 71f75c1c516ca6e652baf311aa14e0c3fd4ba81e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998207"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="1dc2c-103">Recuperación de las entradas de tiempo o gastos aprobados</span><span class="sxs-lookup"><span data-stu-id="1dc2c-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1dc2c-104">Un miembro del equipo del proyecto u otra persona que presente una entrada de tiempo o gasto puede recuperar esa entrada de tiempo o gasto después de que se haya aprobado.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="1dc2c-105">El proceso para recuperar una entrada de tiempo o gasto aprobado consta de dos pasos:</span><span class="sxs-lookup"><span data-stu-id="1dc2c-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="1dc2c-106">Un remitente solicita una recuperación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="1dc2c-107">Un aprobador aprueba la recuperación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="1dc2c-108">Solicitud de una recuperación</span><span class="sxs-lookup"><span data-stu-id="1dc2c-108">Request a recall</span></span>

<span data-ttu-id="1dc2c-109">Siga estos pasos para solicitar una recuperación de un tiempo aprobado o entrada de gastos.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="1dc2c-110">Para entradas de tiempo, vaya a **Proyectos** \> **Mi trabajo** \> **Entrada de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="1dc2c-111">–o bien–</span><span class="sxs-lookup"><span data-stu-id="1dc2c-111">–or–</span></span>

    <span data-ttu-id="1dc2c-112">Para entradas de gastos, vaya a **Proyectos** \> **Mi trabajo** \> **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="1dc2c-113">Para entradas de tiempo, seleccione todas las entradas de tiempo para una combinación específica de un proyecto y una tarea.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="1dc2c-114">Alternativamente, en la cuadrícula, seleccione las celdas individuales por tiempo en una fecha específica para un proyecto específico.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="1dc2c-115">–o bien–</span><span class="sxs-lookup"><span data-stu-id="1dc2c-115">–or–</span></span>

    <span data-ttu-id="1dc2c-116">Para las entradas de gastos, seleccione la fila para la entrada de gastos que recuperar.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="1dc2c-117">Seleccione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-117">Select **Recall**.</span></span> <span data-ttu-id="1dc2c-118">Aparece un cuadro de diálogo de confirmación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="1dc2c-119">Si las entradas de tiempo y gastos seleccionadas ya están aprobadas, se le solicitará que introduzca un motivo para la recuperación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="1dc2c-120">Escriba un motivo para la recuperación y, a continuación, seleccione **Aceptar** para confirmar la operación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="1dc2c-121">El sistema envía a la persona que aprobó las entradas una solicitud para aprobar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="1dc2c-122">Aunque las entradas de tiempo y gastos aprobadas se pueden recuperar, si ya se ha facturado al cliente un tiempo o gasto aprobado, no se puede crear una solicitud de recuperación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="1dc2c-123">Los usuarios que intenten crear una solicitud de recuperación recibirán un mensaje que indicará que el tiempo o el gasto no se pueden recuperar porque ya se han facturado.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="1dc2c-124">Aprobación o rechazo de una solicitud de recuperación</span><span class="sxs-lookup"><span data-stu-id="1dc2c-124">Approve or reject a recall request</span></span>

<span data-ttu-id="1dc2c-125">Siga estos pasos para aprobar o rechazar una solicitud de recuperación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="1dc2c-126">Vaya a **Proyectos** \> **Mi trabajo** \> **Aprobaciones**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="1dc2c-127">En la página de lista **Aprobaciones**, cambie la vista a **Solicitudes de recuperación pendientes de aprobación**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="1dc2c-128">Se mostrará una lista de solicitudes de recuperación enviadas.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="1dc2c-129">Seleccione una o más entradas y, a continuación, seleccione **Aprobar** o **Rechazar**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="1dc2c-130">Si seleccionó **Aprobar**, recibirá un mensaje de advertencia en el que se explicará el impacto de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="1dc2c-131">Seleccione **Aceptar** para confirmar la operación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="1dc2c-132">Se aprobará la solicitud de recuperación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-132">The recall request is approved.</span></span>

    <span data-ttu-id="1dc2c-133">–o bien–</span><span class="sxs-lookup"><span data-stu-id="1dc2c-133">–or–</span></span>

    <span data-ttu-id="1dc2c-134">Si seleccionó **Rechazar**, se rechazará la solicitud de recuperación.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="1dc2c-135">Como cuando se solicita una recuperación, cuando se aprueba una recuperación, el sistema verifica cualquier actividad de facturación en las entradas de tiempo o gastos.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="1dc2c-136">Si ya se ha facturado una entrada, o si está en un borrador de factura, el aprobador recibirá un mensaje de error que indicará que no se puede aprobar la recuperación del tiempo o el gasto, porque ya se ha facturado.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="1dc2c-137">Impacto de una solicitud de recuperación</span><span class="sxs-lookup"><span data-stu-id="1dc2c-137">Impact of a recall request</span></span>

<span data-ttu-id="1dc2c-138">Cuando se recupera una aprobación, hay un impacto tanto operativo como financiero.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="1dc2c-139">Impacto operativo</span><span class="sxs-lookup"><span data-stu-id="1dc2c-139">Operational impact</span></span>

<span data-ttu-id="1dc2c-140">Si se aprueba una solicitud de recuperación, el registro de aprobación se marca como **Rechazado**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="1dc2c-141">El estado de la entrada se cambia a **Devuelto** o **Rechazado** según sea una entrada de tiempo o una entrada de gastos.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="1dc2c-142">El miembro del equipo del proyecto puede ver entradas, editar y, a continuación, volver a enviar entradas o eliminar entradas por completo.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="1dc2c-143">Si se rechaza una solicitud de recuperación, el estado de la entrada permanece **Aprobado** y el miembro del equipo del proyecto o el aprobador del proyecto no pueden editar la entrada.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="1dc2c-144">Impacto financiero</span><span class="sxs-lookup"><span data-stu-id="1dc2c-144">Financial impact</span></span>

<span data-ttu-id="1dc2c-145">Si se aprueba una solicitud de recuperación, los datos reales correspondientes de costes y ventas se actualizan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1dc2c-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="1dc2c-146">El campo **Estado del ajuste** se actualiza a **Ajustado**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="1dc2c-147">El campo **Estado de facturación** se actualiza a **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="1dc2c-148">A continuación, se crean movimientos de retrocesión en la tabla Datos reales.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="1dc2c-149">Para crear entradas de retrocesión, el sistema copia los valores de campo desde los datos reales originales.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="1dc2c-150">Los únicos valores que no se copian son los valores de cantidad.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="1dc2c-151">En su lugar, estos valores se revierten.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-151">These values are reversed instead.</span></span> <span data-ttu-id="1dc2c-152">A continuación, se crean datos reales revertidos para los datos reales **Coste** y **Ventas sin facturar**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="1dc2c-153">El campo **Estado del ajuste** en los datos reales invertidos se establece en **No ajustable**, y el campo **Estado de facturación** se establece en **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="1dc2c-154">Debido a estos cambios, el gasto registrado y la acumulación de ingresos en el proyecto ya no representarán los importes que representan esos datos reales.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="1dc2c-155">Si se rechaza una solicitud de recuperación, no habrá impacto financiero en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="1dc2c-156">Cambios en los registros de entrada de tiempo</span><span class="sxs-lookup"><span data-stu-id="1dc2c-156">Changes to time entry records</span></span>

<span data-ttu-id="1dc2c-157">La siguiente ilustración muestra los cambios que se producen para las entradas de tiempo aprobadas cuando se recuperan.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Transiciones de estado de entrada de tiempo](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="1dc2c-159">Cambios en los registros de entrada de gastos</span><span class="sxs-lookup"><span data-stu-id="1dc2c-159">Changes to expense entry records</span></span>

<span data-ttu-id="1dc2c-160">La siguiente ilustración muestra los cambios que se producen para las entradas de gastos aprobadas cuando se recuperan.</span><span class="sxs-lookup"><span data-stu-id="1dc2c-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Transiciones de estado de entrada de gastos](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]