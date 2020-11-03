---
title: Informes de gastos y múltiples aprobadores
description: En este tema se proporciona información sobre los informes de gastos que requieren la aprobación de más de una persona.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085151"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="5e636-103">Informes de gastos y múltiples aprobadores</span><span class="sxs-lookup"><span data-stu-id="5e636-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="5e636-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="5e636-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5e636-105">Según las directivas de aprobación de gastos de su organización, es posible que más de una persona tenga que aprobar un informe de gastos enviado.</span><span class="sxs-lookup"><span data-stu-id="5e636-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="5e636-106">Cuando configura el proceso de flujo de trabajo para la aprobación del informe de gastos, puede agregar elementos del flujo de trabajo que incluyen tareas o pasos para uno o más aprobadores de informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="5e636-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="5e636-107">Por ejemplo, es posible que requiera que todos los informes de gastos sean aprobados por dos personas distintas, el gerente del empleado que envió el informe y el coordinador de proveedores.</span><span class="sxs-lookup"><span data-stu-id="5e636-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="5e636-108">Si decide requerir varios aprobadores de informes de gastos, puede agregar los elementos del flujo de trabajo de cualquiera de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="5e636-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="5e636-109">Agregue un elemento de aprobación que tenga un paso.</span><span class="sxs-lookup"><span data-stu-id="5e636-109">Add one approval element that has one step.</span></span> <span data-ttu-id="5e636-110">Por ejemplo, es posible que el paso requiera que se asigne un informe de gastos a un grupo de usuarios y que sea aprobado por el 50 por ciento de los miembros del grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="5e636-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="5e636-111">Agregue un elemento de aprobación que tenga varios pasos.</span><span class="sxs-lookup"><span data-stu-id="5e636-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="5e636-112">Por ejemplo, el elemento de aprobación puede tener los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="5e636-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="5e636-113">El gerente del empleado que envió el informe de gastos lo aprueba.</span><span class="sxs-lookup"><span data-stu-id="5e636-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="5e636-114">El empleado del departamento de proveedores verifica los recibos y los elementos del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="5e636-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="5e636-115">El propietario del presupuesto aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="5e636-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="5e636-116">Agregue varios elementos de aprobación, cada uno de los cuales tiene un paso.</span><span class="sxs-lookup"><span data-stu-id="5e636-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="5e636-117">Por ejemplo, puede agregar un elemento de aprobación independiente para cada uno de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="5e636-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="5e636-118">El gerente del empleado aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="5e636-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="5e636-119">El propietario del presupuesto aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="5e636-119">The budget owner approves the expense report.</span></span>
