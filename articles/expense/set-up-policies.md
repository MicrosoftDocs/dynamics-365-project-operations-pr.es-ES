---
title: Definir directivas de gastos
description: Puede definir directivas de gastos que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje.
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
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 863d1e44dad9fa0d2174cf77582a1d820988e92d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276099"
---
# <a name="define-expense-policies"></a><span data-ttu-id="94a0a-103">Definir directivas de gastos</span><span class="sxs-lookup"><span data-stu-id="94a0a-103">Define expense policies</span></span>

<span data-ttu-id="94a0a-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="94a0a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94a0a-105">Puede definir directivas que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje.</span><span class="sxs-lookup"><span data-stu-id="94a0a-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="94a0a-106">La implementación de directivas de gastos puede ayudarle a administrar los gastos de manera eficaz.</span><span class="sxs-lookup"><span data-stu-id="94a0a-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="94a0a-107">Por ejemplo, puede establecer una directiva para los gastos de hotel en la ciudad de Nueva York, que establece que el gasto por noche no puede exceder los 250 USD.</span><span class="sxs-lookup"><span data-stu-id="94a0a-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="94a0a-108">Si un trabajador presenta un informe de gastos o una solicitud de viaje donde la tarifa por habitación excede esta cantidad, el sistema notificará al</span><span class="sxs-lookup"><span data-stu-id="94a0a-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="94a0a-109">trabajador que se ha excedido el importe de la directiva de gastos.</span><span class="sxs-lookup"><span data-stu-id="94a0a-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="94a0a-110">Puede configurar el mensaje que recibirá el trabajador cuando</span><span class="sxs-lookup"><span data-stu-id="94a0a-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="94a0a-111">defina la directiva.</span><span class="sxs-lookup"><span data-stu-id="94a0a-111">define the policy.</span></span>      
        
<span data-ttu-id="94a0a-112">Puede definir tres tipos de directivas:</span><span class="sxs-lookup"><span data-stu-id="94a0a-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="94a0a-113">**Advertencia**: Permite al trabajador enviar un informe de gastos o una solicitud de viaje, pero el gasto se marcará para todos los aprobadores y</span><span class="sxs-lookup"><span data-stu-id="94a0a-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="94a0a-114">para informes posteriores.</span><span class="sxs-lookup"><span data-stu-id="94a0a-114">for later reporting.</span></span>        

- <span data-ttu-id="94a0a-115">**Error**: Requiere que el trabajador revise el gasto para cumplir con la directiva antes de enviar el informe de gastos o la solicitud de viaje.</span><span class="sxs-lookup"><span data-stu-id="94a0a-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="94a0a-116">**Justificación**: Requiere que el trabajador o un gerente introduzca una justificación por exceder el importe de la directiva antes de enviar el informe de gastos o la solicitud de viaje.</span><span class="sxs-lookup"><span data-stu-id="94a0a-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="94a0a-117">Sugerencias de directiva</span><span class="sxs-lookup"><span data-stu-id="94a0a-117">Policy tips</span></span>
<span data-ttu-id="94a0a-118">A continuación, se incluyen algunas sugerencias que pueden ayudarle a crear nuevas directivas para la administración de gastos:</span><span class="sxs-lookup"><span data-stu-id="94a0a-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="94a0a-119">Las directivas tienen fecha de vigencia, lo que significa que una directiva no surtirá efecto si se crea con una fecha posterior a la fecha en que se produjo el gasto.</span><span class="sxs-lookup"><span data-stu-id="94a0a-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="94a0a-120">Por ejemplo, hoy crea una nueva directiva para establecer un gasto máximo de comida de 50 USD.</span><span class="sxs-lookup"><span data-stu-id="94a0a-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="94a0a-121">Cualquier gasto existente introducido a partir de ayer no se comprobará con esta directiva.</span><span class="sxs-lookup"><span data-stu-id="94a0a-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="94a0a-122">Al crear una directiva para una categoría de gastos que se puede desglosar, considere la posibilidad de agregar una condición para el tipo de línea de gastos.</span><span class="sxs-lookup"><span data-stu-id="94a0a-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="94a0a-123">Puede que algunas directivas, como exigir un recibo, no tengan sentido para las líneas desglosadas.</span><span class="sxs-lookup"><span data-stu-id="94a0a-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="94a0a-124">En esta situación, la directiva solo se aplica a la línea de encabezado o a una línea no desglosada.</span><span class="sxs-lookup"><span data-stu-id="94a0a-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="94a0a-125">Las directivas de administración de gastos se evalúan respecto a la entidad de origen de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="94a0a-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="94a0a-126">Para los escenarios de empresas vinculadas, en su lugar puede establecer que la directiva se evalúe con respecto a la entidad de destino (entidad prestataria).</span><span class="sxs-lookup"><span data-stu-id="94a0a-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="94a0a-127">Para ejecutar las directivas en la entidad de destino, active la característica **Evaluar la directiva con respecto a la entidad jurídica prestataria** en el área de trabajo **Administración de característica**.</span><span class="sxs-lookup"><span data-stu-id="94a0a-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="94a0a-128">Cuándo evaluar las directivas</span><span class="sxs-lookup"><span data-stu-id="94a0a-128">When to evaluate policies</span></span>

<span data-ttu-id="94a0a-129">En los parámetros de administración de gastos, puede seleccionar la opción de evaluar las directivas de administración de gastos cuando se guarda una línea o cuando se envía un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="94a0a-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="94a0a-130">Si opta por evaluar cuándo se guarda una línea, los usuarios tendrán una visibilidad más temprana de lo que deben hacer para completar su informe de gastos de una vez.</span><span class="sxs-lookup"><span data-stu-id="94a0a-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="94a0a-131">De lo contrario, puede retrasar la evaluación de la directiva y ahorrar tiempo validando al final, durante el envío al flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="94a0a-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]