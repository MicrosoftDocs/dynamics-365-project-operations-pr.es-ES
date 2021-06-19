---
title: Informes de gastos y múltiples aprobadores
description: En este tema se proporciona información sobre los informes de gastos que requieren la aprobación de más de una persona.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002077"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="ff467-103">Informes de gastos y múltiples aprobadores</span><span class="sxs-lookup"><span data-stu-id="ff467-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="ff467-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="ff467-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ff467-105">Según las directivas de aprobación de gastos de su organización, es posible que más de una persona tenga que aprobar un informe de gastos enviado.</span><span class="sxs-lookup"><span data-stu-id="ff467-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="ff467-106">Cuando configure el proceso de flujo de trabajo para aprobar un informe de gastos, puede agregar elementos del flujo de trabajo que incluyan tareas o pasos para uno o varios aprobadores de informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="ff467-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="ff467-107">Por ejemplo, puede exigir que todos los informes de gastos sean aprobados por dos personas independientes, el jefe del empleado que envió el informe y el coordinador de proveedores.</span><span class="sxs-lookup"><span data-stu-id="ff467-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="ff467-108">Si decide exigir varios aprobadores de informes de gastos, puede agregar los elementos del flujo de trabajo según una de las formas que indicamos a continuación:</span><span class="sxs-lookup"><span data-stu-id="ff467-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="ff467-109">Agregar un elemento de aprobación que tenga un paso.</span><span class="sxs-lookup"><span data-stu-id="ff467-109">Add one approval element that has one step.</span></span> <span data-ttu-id="ff467-110">Por ejemplo, el paso puede requerir que se asigne un informe de gastos a un grupo de usuarios y que se exija la aprobación del 50 por ciento de los miembros del grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="ff467-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="ff467-111">Agregar un elemento de aprobación con varios pasos.</span><span class="sxs-lookup"><span data-stu-id="ff467-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="ff467-112">Por ejemplo, el elemento de aprobación puede tener los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="ff467-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="ff467-113">El gerente del empleado que envió el informe de gastos lo aprueba.</span><span class="sxs-lookup"><span data-stu-id="ff467-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="ff467-114">El empleado de Proveedores verifica los recibos y los elementos del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="ff467-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="ff467-115">El propietario del presupuesto aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="ff467-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="ff467-116">Agregar varios elementos de aprobación que tengan, cada uno de ellos, un paso.</span><span class="sxs-lookup"><span data-stu-id="ff467-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="ff467-117">Por ejemplo, puede agregar un elemento de aprobación independiente para cada uno de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="ff467-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="ff467-118">El gerente del empleado aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="ff467-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="ff467-119">El propietario del presupuesto aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="ff467-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]