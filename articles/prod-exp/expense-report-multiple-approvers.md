---
title: Múltiples aprobadores en un informe de gastos
description: En este tema se proporciona información sobre los informes de gastos que requieren la aprobación de varias personas.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271734"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="16a5b-103">Múltiples aprobadores en un informe de gastos</span><span class="sxs-lookup"><span data-stu-id="16a5b-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="16a5b-104">Según las directivas de aprobación de gastos de su organización, es posible que más de una persona tenga que aprobar un informe de gastos enviado por un empleado.</span><span class="sxs-lookup"><span data-stu-id="16a5b-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="16a5b-105">Cuando configura el proceso de flujo de trabajo para la aprobación del informe de gastos, puede agregar elementos del flujo de trabajo que incluyen tareas o pasos para uno o más aprobadores de informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="16a5b-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="16a5b-106">Por ejemplo, es posible que requiera que todos los informes de gastos sean aprobados primero por el gerente del empleado que envió el informe y después el coordinador de proveedores.</span><span class="sxs-lookup"><span data-stu-id="16a5b-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="16a5b-107">Si decide requerir varios aprobadores de informes de gastos, puede agregar los elementos del flujo de trabajo de cualquiera de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="16a5b-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="16a5b-108">Agregue un elemento de aprobación que tenga un paso.</span><span class="sxs-lookup"><span data-stu-id="16a5b-108">Add one approval element that has one step.</span></span> <span data-ttu-id="16a5b-109">Por ejemplo, es posible que el paso requiera que se asigne un informe de gastos a un grupo de usuarios y que sea aprobado por el 50 por ciento de los miembros del grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="16a5b-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="16a5b-110">Agregue un elemento de aprobación que tenga varios pasos.</span><span class="sxs-lookup"><span data-stu-id="16a5b-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="16a5b-111">Por ejemplo, el elemento de aprobación puede tener los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="16a5b-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="16a5b-112">El gerente del empleado que envió el informe de gastos lo aprueba.</span><span class="sxs-lookup"><span data-stu-id="16a5b-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="16a5b-113">El empleado del departamento de proveedores verifica los recibos y los elementos del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="16a5b-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="16a5b-114">El propietario del presupuesto aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="16a5b-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="16a5b-115">Agregue varios elementos de aprobación, cada uno de los cuales tiene un paso.</span><span class="sxs-lookup"><span data-stu-id="16a5b-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="16a5b-116">Por ejemplo, puede agregar un elemento de aprobación independiente para cada uno de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="16a5b-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="16a5b-117">El gerente del empleado aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="16a5b-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="16a5b-118">El propietario del presupuesto aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="16a5b-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]