---
title: Entrada de gastos (simplificados)
description: Este tema proporciona información sobre cómo trabajar con la entrada de gastos en una implementación simplificada.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e75a61c25be06a9db121e8165e8ccd25d4719d08
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002212"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="690fb-103">Entrada de gastos (simplificados)</span><span class="sxs-lookup"><span data-stu-id="690fb-103">Expense entry (lite)</span></span>

<span data-ttu-id="690fb-104">_**Se aplica a:** Implementación simplificada: del acuerdo a la facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="690fb-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="690fb-105">La gestión de gastos básica o simplificada es la capacidad de registrar gastos simples.</span><span class="sxs-lookup"><span data-stu-id="690fb-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="690fb-106">Puede registrar los gastos de un proyecto y luego el aprobador del proyecto los revisará y aprobará.</span><span class="sxs-lookup"><span data-stu-id="690fb-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="690fb-107">Para obtener más información acerca de las capacidades de gastos en Dynamics 365 Project Operations, consulte [Información general de gastos](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="690fb-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="690fb-108">Capturar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="690fb-108">Capture a basic expense</span></span>

<span data-ttu-id="690fb-109">Puede capturar sus gastos para enviarlos al aprobador.</span><span class="sxs-lookup"><span data-stu-id="690fb-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="690fb-110">Vaya a **Gastos** y seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="690fb-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="690fb-111">En la página **Nuevo gasto**, especifique la información de gasto requerida y, a continuación, seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="690fb-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="690fb-112">Enviar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="690fb-112">Submit a basic expense</span></span>

<span data-ttu-id="690fb-113">Una vez que haya terminado de capturar todos sus gastos y esté listo para que se aprueben, debe enviarlos.</span><span class="sxs-lookup"><span data-stu-id="690fb-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="690fb-114">Vaya a **Gastos** y seleccione un gasto.</span><span class="sxs-lookup"><span data-stu-id="690fb-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="690fb-115">O bien, seleccione todos los gastos usando la casilla del encabezado.</span><span class="sxs-lookup"><span data-stu-id="690fb-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="690fb-116">Seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="690fb-116">Select **Submit**.</span></span> <span data-ttu-id="690fb-117">El sistema procesa las entradas seleccionadas y luego crea solicitudes de aprobación de gastos.</span><span class="sxs-lookup"><span data-stu-id="690fb-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="690fb-118">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="690fb-118">Add an attachment</span></span>

<span data-ttu-id="690fb-119">Es posible que deba proporcionar al aprobador documentación adicional acerca de su gasto.</span><span class="sxs-lookup"><span data-stu-id="690fb-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="690fb-120">Puede adjuntar un recibo en la escala de tiempo de la entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="690fb-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="690fb-121">Seleccione **Editar** y en la sección **Escala de tiempo**, y luego seleccione el icono del clip de papel para adjuntar el recibo.</span><span class="sxs-lookup"><span data-stu-id="690fb-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="690fb-122">Recuperar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="690fb-122">Recall a basic expense</span></span>

<span data-ttu-id="690fb-123">Cuando envía un gasto por error, puede recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="690fb-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="690fb-124">El tiempo necesario para recuperar una entrada de gasto depende de la fase de aprobación en que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="690fb-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="690fb-125">Si el aprobador todavía no ha aprobado la entrada, la recuperación puede ser inmediata.</span><span class="sxs-lookup"><span data-stu-id="690fb-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="690fb-126">Sin embargo, si ya se ha aprobado la entrada, hay que pedir al aprobador que apruebe la recuperación y revierta las transacciones.</span><span class="sxs-lookup"><span data-stu-id="690fb-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="690fb-127">Vaya a **Gastos** y, en la lista de gastos, seleccione el gasto que quiera recuperar.</span><span class="sxs-lookup"><span data-stu-id="690fb-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="690fb-128">Seleccione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="690fb-128">Select **Recall**.</span></span> <span data-ttu-id="690fb-129">Si todavía no se ha aprobado la entrada de gasto, el sistema la recuperará de inmediato.</span><span class="sxs-lookup"><span data-stu-id="690fb-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="690fb-130">Si, por el contrario, la entrada de gasto ya se ha aprobado, se crea una solicitud de recuperación para notificar al aprobador que usted quiere revertir el gasto.</span><span class="sxs-lookup"><span data-stu-id="690fb-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="690fb-131">El aprobador luego confirmará que se puede realizar la reversión y se devolverá la entrada.</span><span class="sxs-lookup"><span data-stu-id="690fb-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="690fb-132">Eliminar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="690fb-132">Delete a basic expense</span></span>

<span data-ttu-id="690fb-133">Los gastos que aún no se han enviado se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="690fb-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="690fb-134">Para eliminar un gasto que ya se ha enviado, primero debe recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="690fb-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="690fb-135">Consultar también</span><span class="sxs-lookup"><span data-stu-id="690fb-135">See also</span></span>

- [<span data-ttu-id="690fb-136">Información general de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="690fb-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]