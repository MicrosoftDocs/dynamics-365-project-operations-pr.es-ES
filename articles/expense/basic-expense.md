---
title: Entrada de gastos (simplificados)
description: Este tema proporciona información sobre cómo trabajar con la entrada de gastos en una implementación simplificada.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085032"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="a8d98-103">Entrada de gastos (simplificados)</span><span class="sxs-lookup"><span data-stu-id="a8d98-103">Expense entry (lite)</span></span>

<span data-ttu-id="a8d98-104">_**Se aplica a:** Implementación simplificada: del acuerdo a la facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="a8d98-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a8d98-105">La gestión de gastos básica o simplificada es la capacidad de registrar gastos simples.</span><span class="sxs-lookup"><span data-stu-id="a8d98-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="a8d98-106">Puede registrar gastos contra un proyecto y luego el aprobador del proyecto los revisará y aprobará.</span><span class="sxs-lookup"><span data-stu-id="a8d98-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="a8d98-107">Para obtener más información sobre las capacidades de gastos en Dynamics 365 Project Operations, consulte [Resumen de gastos](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a8d98-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="a8d98-108">Capturar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="a8d98-108">Capture a basic expense</span></span>

<span data-ttu-id="a8d98-109">Puede capturar sus gastos para enviarlos al aprobador.</span><span class="sxs-lookup"><span data-stu-id="a8d98-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="a8d98-110">Vaya a **Gastos** y seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="a8d98-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="a8d98-111">En la página **Nuevo gasto** , especifique la información de gasto requerida y, a continuación, seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="a8d98-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="a8d98-112">Enviar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="a8d98-112">Submit a basic expense</span></span>

<span data-ttu-id="a8d98-113">Una vez que haya terminado de capturar todos sus gastos y esté listo para que se aprueben, debe enviarlos.</span><span class="sxs-lookup"><span data-stu-id="a8d98-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="a8d98-114">Vaya a **Gastos** y seleccione un gasto.</span><span class="sxs-lookup"><span data-stu-id="a8d98-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="a8d98-115">O bien, seleccione todos los gastos usando la casilla de verificación del encabezado.</span><span class="sxs-lookup"><span data-stu-id="a8d98-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="a8d98-116">Seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="a8d98-116">Select **Submit**.</span></span> <span data-ttu-id="a8d98-117">El sistema procesa las entradas seleccionadas y luego crea solicitudes de aprobación de gastos.</span><span class="sxs-lookup"><span data-stu-id="a8d98-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="a8d98-118">Recuperar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="a8d98-118">Recall a basic expense</span></span>

<span data-ttu-id="a8d98-119">Cuando envía un gasto por error, puede recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="a8d98-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="a8d98-120">El tiempo necesario para recuperar una entrada de gastos depende de su etapa de aprobación.</span><span class="sxs-lookup"><span data-stu-id="a8d98-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="a8d98-121">Si el aprobador aún no ha aprobado la entrada, la recuperación puede ocurrir de inmediato.</span><span class="sxs-lookup"><span data-stu-id="a8d98-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="a8d98-122">Sin embargo, si la entrada ya se ha aprobado, se le pide al aprobador que apruebe la recuperación y revierta las transacciones.</span><span class="sxs-lookup"><span data-stu-id="a8d98-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="a8d98-123">Vaya a **Gastos** y luego, en la lista de gastos, seleccione el gasto que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="a8d98-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="a8d98-124">Seleccione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="a8d98-124">Select **Recall**.</span></span> <span data-ttu-id="a8d98-125">Si la entrada de gastos aún no se ha aprobado, el sistema la recupera inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a8d98-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="a8d98-126">Si la entrada de gastos ya se aprobó, se crea una solicitud de recuperación para notificar al aprobador que desea revertir el gasto.</span><span class="sxs-lookup"><span data-stu-id="a8d98-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="a8d98-127">El aprobador luego confirmará que se puede realizar la reversión y se devolverá la entrada.</span><span class="sxs-lookup"><span data-stu-id="a8d98-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="a8d98-128">Eliminar un gasto básico</span><span class="sxs-lookup"><span data-stu-id="a8d98-128">Delete a basic expense</span></span>

<span data-ttu-id="a8d98-129">Los gastos que aún no se han enviado se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="a8d98-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="a8d98-130">Para eliminar un gasto que ya se ha enviado, primero debe recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="a8d98-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8d98-131">Consultar también</span><span class="sxs-lookup"><span data-stu-id="a8d98-131">See also</span></span>

- [<span data-ttu-id="a8d98-132">Información general de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="a8d98-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
