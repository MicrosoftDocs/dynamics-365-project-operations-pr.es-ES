---
title: Informes de gastos y múltiples aprobadores
description: En este tema se proporciona información sobre los informes de gastos que requieren la aprobación de más de una persona.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276549"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="0d69f-103">Informes de gastos y múltiples aprobadores</span><span class="sxs-lookup"><span data-stu-id="0d69f-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="0d69f-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="0d69f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d69f-105">Según las directivas de aprobación de gastos de su organización, es posible que más de una persona tenga que aprobar un informe de gastos enviado.</span><span class="sxs-lookup"><span data-stu-id="0d69f-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="0d69f-106">Cuando configura el proceso de flujo de trabajo para la aprobación del informe de gastos, puede agregar elementos del flujo de trabajo que incluyen tareas o pasos para uno o más aprobadores de informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="0d69f-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="0d69f-107">Por ejemplo, es posible que requiera que todos los informes de gastos sean aprobados por dos personas distintas, el gerente del empleado que envió el informe y el coordinador de proveedores.</span><span class="sxs-lookup"><span data-stu-id="0d69f-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="0d69f-108">Si decide requerir varios aprobadores de informes de gastos, puede agregar los elementos del flujo de trabajo de cualquiera de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="0d69f-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="0d69f-109">Agregue un elemento de aprobación que tenga un paso.</span><span class="sxs-lookup"><span data-stu-id="0d69f-109">Add one approval element that has one step.</span></span> <span data-ttu-id="0d69f-110">Por ejemplo, es posible que el paso requiera que se asigne un informe de gastos a un grupo de usuarios y que sea aprobado por el 50 por ciento de los miembros del grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="0d69f-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="0d69f-111">Agregue un elemento de aprobación que tenga varios pasos.</span><span class="sxs-lookup"><span data-stu-id="0d69f-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="0d69f-112">Por ejemplo, el elemento de aprobación puede tener los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="0d69f-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="0d69f-113">El gerente del empleado que envió el informe de gastos lo aprueba.</span><span class="sxs-lookup"><span data-stu-id="0d69f-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="0d69f-114">El empleado del departamento de proveedores verifica los recibos y los elementos del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="0d69f-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="0d69f-115">El propietario del presupuesto aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="0d69f-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="0d69f-116">Agregue varios elementos de aprobación, cada uno de los cuales tiene un paso.</span><span class="sxs-lookup"><span data-stu-id="0d69f-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="0d69f-117">Por ejemplo, puede agregar un elemento de aprobación independiente para cada uno de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="0d69f-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="0d69f-118">El gerente del empleado aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="0d69f-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="0d69f-119">El propietario del presupuesto aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="0d69f-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]