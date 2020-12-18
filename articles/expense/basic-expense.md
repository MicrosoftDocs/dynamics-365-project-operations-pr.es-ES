---
title: Entrada de gastos (simplificados)
description: Este tema proporciona información sobre cómo trabajar con la entrada de gastos en una implementación simplificada.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590967"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="6c98b-103">Entrada de gastos (simplificados)</span><span class="sxs-lookup"><span data-stu-id="6c98b-103">Expense entry (lite)</span></span>

<span data-ttu-id="6c98b-104">_**Se aplica a:** Implementación simplificada: del acuerdo a la facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="6c98b-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c98b-105">La gestión de gastos básica o simplificada es la capacidad de registrar gastos simples.</span><span class="sxs-lookup"><span data-stu-id="6c98b-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="6c98b-106">Puede registrar gastos contra un proyecto y luego el aprobador del proyecto los revisará y aprobará.</span><span class="sxs-lookup"><span data-stu-id="6c98b-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="6c98b-107">Para obtener más información acerca de las capacidades de gastos en Dynamics 365 Project Operations, consulte [Información general de gastos](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6c98b-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="6c98b-108">Capturar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="6c98b-108">Capture a basic expense</span></span>

<span data-ttu-id="6c98b-109">Puede capturar sus gastos para enviarlos al aprobador.</span><span class="sxs-lookup"><span data-stu-id="6c98b-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="6c98b-110">Vaya a **Gastos** y seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="6c98b-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="6c98b-111">En la página **Nuevo gasto**, especifique la información de gasto requerida y, a continuación, seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="6c98b-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="6c98b-112">Enviar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="6c98b-112">Submit a basic expense</span></span>

<span data-ttu-id="6c98b-113">Una vez que haya terminado de capturar todos sus gastos y esté listo para que se aprueben, debe enviarlos.</span><span class="sxs-lookup"><span data-stu-id="6c98b-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="6c98b-114">Vaya a **Gastos** y seleccione un gasto.</span><span class="sxs-lookup"><span data-stu-id="6c98b-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="6c98b-115">O bien, seleccione todos los gastos usando la casilla de verificación del encabezado.</span><span class="sxs-lookup"><span data-stu-id="6c98b-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="6c98b-116">Seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="6c98b-116">Select **Submit**.</span></span> <span data-ttu-id="6c98b-117">El sistema procesa las entradas seleccionadas y luego crea solicitudes de aprobación de gastos.</span><span class="sxs-lookup"><span data-stu-id="6c98b-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="6c98b-118">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="6c98b-118">Add an attachment</span></span>

<span data-ttu-id="6c98b-119">Es posible que deba proporcionar al aprobador documentación adicional acerca de su gasto.</span><span class="sxs-lookup"><span data-stu-id="6c98b-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="6c98b-120">Puede adjuntar un recibo en la escala de tiempo de la entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="6c98b-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="6c98b-121">Seleccione **Editar** y en la sección **Escala de tiempo**, y luego seleccione el icono del clip de papel para adjuntar el recibo.</span><span class="sxs-lookup"><span data-stu-id="6c98b-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="6c98b-122">Recuperar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="6c98b-122">Recall a basic expense</span></span>

<span data-ttu-id="6c98b-123">Cuando envía un gasto por error, puede recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="6c98b-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="6c98b-124">El tiempo necesario para recuperar una entrada de gastos depende de su etapa de aprobación.</span><span class="sxs-lookup"><span data-stu-id="6c98b-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="6c98b-125">Si el aprobador aún no ha aprobado la entrada, la recuperación puede ocurrir de inmediato.</span><span class="sxs-lookup"><span data-stu-id="6c98b-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="6c98b-126">Sin embargo, si la entrada ya se ha aprobado, se le pide al aprobador que apruebe la recuperación y revierta las transacciones.</span><span class="sxs-lookup"><span data-stu-id="6c98b-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="6c98b-127">Vaya a **Gastos** y luego, en la lista de gastos, seleccione el gasto que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="6c98b-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="6c98b-128">Seleccione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="6c98b-128">Select **Recall**.</span></span> <span data-ttu-id="6c98b-129">Si la entrada de gastos aún no se ha aprobado, el sistema la recupera inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6c98b-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="6c98b-130">Si la entrada de gastos ya se aprobó, se crea una solicitud de recuperación para notificar al aprobador que desea revertir el gasto.</span><span class="sxs-lookup"><span data-stu-id="6c98b-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="6c98b-131">El aprobador luego confirmará que se puede realizar la reversión y se devolverá la entrada.</span><span class="sxs-lookup"><span data-stu-id="6c98b-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="6c98b-132">Eliminar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="6c98b-132">Delete a basic expense</span></span>

<span data-ttu-id="6c98b-133">Los gastos que aún no se han enviado se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="6c98b-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="6c98b-134">Para eliminar un gasto que ya se ha enviado, primero debe recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="6c98b-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c98b-135">Consultar también</span><span class="sxs-lookup"><span data-stu-id="6c98b-135">See also</span></span>

- [<span data-ttu-id="6c98b-136">Información general de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="6c98b-136">Approvals overview</span></span>](../approvals/approvals-overview.md)
