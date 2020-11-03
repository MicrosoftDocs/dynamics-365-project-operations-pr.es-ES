---
title: Flujo de trabajo de gestión de gastos
description: Este tema explica cómo puede usar el sistema de flujo de trabajo en Microsoft Dynamics 365 Finance para configurar un proceso de revisión para los informes de gastos en la Gestión de gastos.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085303"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="b621e-103">Flujo de trabajo de gestión de gastos</span><span class="sxs-lookup"><span data-stu-id="b621e-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b621e-104">Puede usar el sistema de flujo de trabajo en para configurar un proceso de revisión para los informes de gastos en la Gestión de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="b621e-105">Puede configurar un flujo de trabajo que utilice los siguientes criterios para determinar quién aprueba los informes de gastos:</span><span class="sxs-lookup"><span data-stu-id="b621e-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="b621e-106">La jerarquía de informes de los empleados y los límites de aprobación predefinidos</span><span class="sxs-lookup"><span data-stu-id="b621e-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="b621e-107">Aprobación de varios niveles que admite aprobadores interinos y un aprobador final</span><span class="sxs-lookup"><span data-stu-id="b621e-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="b621e-108">Dimensiones financieras y responsabilidad del proyecto</span><span class="sxs-lookup"><span data-stu-id="b621e-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="b621e-109">Asignación a usuarios o grupos de usuarios específicos</span><span class="sxs-lookup"><span data-stu-id="b621e-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="b621e-110">Se pueden crear aprobaciones de flujo de trabajo para informes de gastos, solicitudes de viaje, adelantos en efectivo y recuperación del impuesto al valor agregado (IVA).</span><span class="sxs-lookup"><span data-stu-id="b621e-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="b621e-111">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b621e-111">**Example**</span></span>

<span data-ttu-id="b621e-112">El siguiente proceso es un ejemplo del flujo de trabajo de gestión de gastos para un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="b621e-113">Un empleado crea y guarda un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="b621e-114">El empleado envía el informe de gastos para su aprobación.</span><span class="sxs-lookup"><span data-stu-id="b621e-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="b621e-115">El aprobador se identifica según las reglas que se definieron cuando se configuró el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b621e-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="b621e-116">El aprobador recibe una notificación de que un informe de gastos está listo para su aprobación.</span><span class="sxs-lookup"><span data-stu-id="b621e-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="b621e-117">El aprobador revisa el informe de gastos y verifica que se cumplan las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="b621e-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="b621e-118">Los gastos no violan ninguna política de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="b621e-119">Si un gasto viola una directiva, el aprobador verifica que el informe de gastos incluya una justificación comercial válida.</span><span class="sxs-lookup"><span data-stu-id="b621e-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="b621e-120">Los recibos electrónicos se adjuntan al informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="b621e-121">El aprobador aprueba el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="b621e-122">El informe de gastos se asigna al coordinador de proveedores para su contabilización.</span><span class="sxs-lookup"><span data-stu-id="b621e-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="b621e-123">Se produce uno de los siguientes pasos, dependiendo de si la publicación automática está configurada:</span><span class="sxs-lookup"><span data-stu-id="b621e-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="b621e-124">Si se configura la contabilización automática, el informe de gastos se procesa para el pago y se actualiza el estado del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="b621e-125">Si la contabilización automática no está configurada, el coordinador de proveedores verifica que se hayan enviado todos los recibos originales y que los recibos estén alineados con los gastos del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="b621e-126">Todos los códigos de impuestos que se introducen en el informe de gastos también deben verificarse como correctos.</span><span class="sxs-lookup"><span data-stu-id="b621e-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="b621e-127">Una vez verificados estos requisitos, se contabiliza el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="b621e-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="b621e-128">Una vez que se contabiliza el informe de gastos, se autoriza el pago del informe de gastos y se reembolsa al empleado.</span><span class="sxs-lookup"><span data-stu-id="b621e-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
