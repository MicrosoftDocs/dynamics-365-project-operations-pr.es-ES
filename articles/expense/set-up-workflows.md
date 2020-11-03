---
title: Configurar flujos de trabajo para la administración de gastos
description: Puede configurar un proceso de flujo de trabajo que se utiliza para revisar y aprobar documentos de viaje y gastos.
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
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085175"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="af54a-103">Configurar flujos de trabajo para la administración de gastos</span><span class="sxs-lookup"><span data-stu-id="af54a-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="af54a-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="af54a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af54a-105">Puede configurar un proceso de flujo de trabajo para revisar y aprobar documentos de viaje y gastos.</span><span class="sxs-lookup"><span data-stu-id="af54a-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="af54a-106">Puede definir flujos de trabajo para informes de gastos, solicitudes de viaje y solicitudes de anticipos.</span><span class="sxs-lookup"><span data-stu-id="af54a-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="af54a-107">Un flujo de trabajo representa un proceso de negocio y define cómo fluye un documento a través del sistema.</span><span class="sxs-lookup"><span data-stu-id="af54a-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="af54a-108">El flujo de trabajo también indica quién debe completar una tarea o aprobar un documento.</span><span class="sxs-lookup"><span data-stu-id="af54a-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="af54a-109">El uso del sistema de flujo de trabajo en su organización tiene varios beneficios:</span><span class="sxs-lookup"><span data-stu-id="af54a-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="af54a-110">**Procesos coherentes** : Puede definir el proceso de aprobación para documentos específicos, como solicitudes de compra e informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="af54a-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="af54a-111">El uso del sistema de flujo de trabajo contribuye a garantizar que los documentos se procesan y aprueban de forma coherente y eficaz.</span><span class="sxs-lookup"><span data-stu-id="af54a-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="af54a-112">**Visibilidad de los procesos** : puede realizar un seguimiento del estado, el historial y las métricas de rendimiento de una instancia de flujo de trabajo específica.</span><span class="sxs-lookup"><span data-stu-id="af54a-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="af54a-113">Esto ayuda a determinar si se deben realizar cambios en el flujo de trabajo para mejorar su eficacia.</span><span class="sxs-lookup"><span data-stu-id="af54a-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="af54a-114">**Lista de trabajo centralizada** : los usuarios pueden consultar una lista de trabajo centralizada para ver las tareas y las aprobaciones de flujo de trabajo que se les han asignado.</span><span class="sxs-lookup"><span data-stu-id="af54a-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="af54a-115">Tipos de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="af54a-115">Workflow types</span></span>

<span data-ttu-id="af54a-116">En la siguiente tabla se muestran los tipos de flujos de trabajo que puede crear en **Administración de gastos**.</span><span class="sxs-lookup"><span data-stu-id="af54a-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="af54a-117"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="af54a-118"><strong>Utilice este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="af54a-119"><strong>Aprobación automática de informes de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="af54a-120">Cree flujos de trabajo de aprobación para informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="af54a-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="af54a-121"><strong>Registro automático de informes de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="af54a-122">Cree flujos de trabajo de registro automático para informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="af54a-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="af54a-123"><strong>Elemento de línea de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="af54a-124">Cree flujos de trabajo de aprobación para elementos de línea en informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="af54a-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="af54a-125"><strong>Registro automático de elemento de línea de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="af54a-126">Cree flujos de trabajo de registro automático para elementos de línea en informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="af54a-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="af54a-127"><strong>Solicitud de viaje</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="af54a-128">Cree flujos de trabajo de aprobación para solicitudes de viaje.</span><span class="sxs-lookup"><span data-stu-id="af54a-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="af54a-129"><strong>Solicitud de anticipo</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="af54a-130">Cree flujos de trabajo de aprobación para solicitudes de anticipo.</span><span class="sxs-lookup"><span data-stu-id="af54a-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="af54a-131"><strong>Devolución de impuestos de IVA</strong></span><span class="sxs-lookup"><span data-stu-id="af54a-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="af54a-132">Cree flujos de trabajo de aprobación para la devolución del impuesto sobre el valor añadido (IVA).</span><span class="sxs-lookup"><span data-stu-id="af54a-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
