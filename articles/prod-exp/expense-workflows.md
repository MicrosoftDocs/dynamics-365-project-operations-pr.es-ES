---
title: Configurar flujos de trabajo para la gestión de gastos
description: Puede configurar un proceso de flujo de trabajo para revisar y aprobar documentos de viaje y gastos.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005137"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="ac430-103">Configurar flujos de trabajo para la gestión de gastos</span><span class="sxs-lookup"><span data-stu-id="ac430-103">Set up Expense management workflows</span></span>

<span data-ttu-id="ac430-104">Puede configurar un proceso de flujo de trabajo que se utiliza para revisar y aprobar documentos de viaje y gastos.</span><span class="sxs-lookup"><span data-stu-id="ac430-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="ac430-105">Los documentos para los que pueden definirse flujos de trabajo incluyen informes de gastos, solicitudes de viaje y solicitudes de anticipos.</span><span class="sxs-lookup"><span data-stu-id="ac430-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="ac430-106">Un flujo de trabajo representa un proceso de negocio.</span><span class="sxs-lookup"><span data-stu-id="ac430-106">A workflow represents a business process.</span></span> <span data-ttu-id="ac430-107">Define cómo un documento fluye a través del sistema e indica quién debe completar una tarea o aprobar un documento.</span><span class="sxs-lookup"><span data-stu-id="ac430-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ac430-108">El uso del sistema de flujo de trabajo en su organización tiene varios beneficios:</span><span class="sxs-lookup"><span data-stu-id="ac430-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="ac430-109">**Procesos coherentes**: puede definir el proceso de aprobación para documentos específicos, como solicitudes de compra e informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="ac430-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ac430-110">El uso del sistema de flujo de trabajo contribuye a garantizar que los documentos se procesan y aprueban de forma coherente y eficaz.</span><span class="sxs-lookup"><span data-stu-id="ac430-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="ac430-111">Visibilidad de los procesos: puede realizar un seguimiento del estado, el historial y las métricas de rendimiento de una instancia de flujo de trabajo específica.</span><span class="sxs-lookup"><span data-stu-id="ac430-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ac430-112">Esto ayuda a determinar si se deben realizar cambios en el flujo de trabajo para mejorar su eficacia.</span><span class="sxs-lookup"><span data-stu-id="ac430-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="ac430-113">Lista de trabajo centralizada: los usuarios pueden consultar una lista de trabajo centralizada para ver las tareas y las aprobaciones de flujo de trabajo que se les han asignado.</span><span class="sxs-lookup"><span data-stu-id="ac430-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="ac430-114">**Los tipos de flujos de trabajo que puede crear**</span><span class="sxs-lookup"><span data-stu-id="ac430-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="ac430-115">En la siguiente tabla se muestran los tipos de flujos de trabajo que puede crear en **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="ac430-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="ac430-116"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="ac430-117"><strong>Utilice este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="ac430-118"><strong>Informe de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="ac430-119">Cree flujos de trabajo de aprobación para informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="ac430-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="ac430-120"><strong>Registro automático de informes de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="ac430-121">Cree flujos de trabajo de registro automático para informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="ac430-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="ac430-122"><strong>Elemento de línea de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="ac430-123">Cree flujos de trabajo de aprobación para elementos de línea en informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="ac430-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="ac430-124"><strong>Registro automático de elemento de línea de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="ac430-125">Cree flujos de trabajo de registro automático para elementos de línea en informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="ac430-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="ac430-126"><strong>Solicitud de viaje</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="ac430-127">Cree flujos de trabajo de aprobación para solicitudes de viaje.</span><span class="sxs-lookup"><span data-stu-id="ac430-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="ac430-128"><strong>Solicitud de anticipo</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="ac430-129">Cree flujos de trabajo de aprobación para solicitudes de anticipo.</span><span class="sxs-lookup"><span data-stu-id="ac430-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="ac430-130"><strong>Devolución de impuestos de IVA</strong></span><span class="sxs-lookup"><span data-stu-id="ac430-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="ac430-131">Cree flujos de trabajo de aprobación para la devolución del impuesto sobre el valor añadido (IVA).</span><span class="sxs-lookup"><span data-stu-id="ac430-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]