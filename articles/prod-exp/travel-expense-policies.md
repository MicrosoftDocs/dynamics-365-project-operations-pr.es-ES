---
title: Configurar directivas de gasto
description: Puede configurar directivas de gastos que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje en Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085295"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="bee25-103">Configurar directivas de gasto</span><span class="sxs-lookup"><span data-stu-id="bee25-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bee25-104">Puede definir directivas que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje.</span><span class="sxs-lookup"><span data-stu-id="bee25-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="bee25-105">La implementación de directivas de gastos puede ayudarle a administrar los gastos de manera eficaz.</span><span class="sxs-lookup"><span data-stu-id="bee25-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="bee25-106">Por ejemplo, puede establecer una directiva para los gastos de hotel en la ciudad de Nueva York, que establece que el gasto por noche no puede exceder los 250 USD.</span><span class="sxs-lookup"><span data-stu-id="bee25-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="bee25-107">Si un trabajador presenta un informe de gastos o una solicitud de viaje donde la tarifa por habitación excede esta cantidad, el sistema notificará al</span><span class="sxs-lookup"><span data-stu-id="bee25-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="bee25-108">trabajador que se ha excedido el importe de la directiva de gastos.</span><span class="sxs-lookup"><span data-stu-id="bee25-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="bee25-109">Puede configurar el mensaje que recibirá el trabajador cuando</span><span class="sxs-lookup"><span data-stu-id="bee25-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="bee25-110">defina la directiva.</span><span class="sxs-lookup"><span data-stu-id="bee25-110">define the policy.</span></span>      
        
<span data-ttu-id="bee25-111">Puede definir tres tipos de directivas:</span><span class="sxs-lookup"><span data-stu-id="bee25-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="bee25-112">Advertencia: permite al trabajador enviar un informe de gastos o una solicitud de viaje, pero el gasto se marcará para todos los aprobadores y</span><span class="sxs-lookup"><span data-stu-id="bee25-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="bee25-113">para informes posteriores.</span><span class="sxs-lookup"><span data-stu-id="bee25-113">for later reporting.</span></span>        

- <span data-ttu-id="bee25-114">Error: requiere que el trabajador revise el gasto para cumplir con la directiva antes de enviar el informe de gastos o la solicitud de viaje.</span><span class="sxs-lookup"><span data-stu-id="bee25-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="bee25-115">Justificación: requiere que el trabajador o un gerente introduzca una justificación por exceder el importe de la directiva antes de enviar el informe de gastos o la solicitud de viaje.</span><span class="sxs-lookup"><span data-stu-id="bee25-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="bee25-116">Sugerencias de directiva</span><span class="sxs-lookup"><span data-stu-id="bee25-116">Policy tips</span></span>
<span data-ttu-id="bee25-117">A continuación, se incluyen algunas sugerencias que pueden ayudarle a crear nuevas directivas para la administración de gastos.</span><span class="sxs-lookup"><span data-stu-id="bee25-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="bee25-118">Las directivas tienen fecha de vigencia, lo que significa que una directiva no surtirá efecto si se crea con una fecha posterior a la fecha en que se produjo el gasto.</span><span class="sxs-lookup"><span data-stu-id="bee25-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="bee25-119">Por ejemplo, si está creando una nueva política hoy para imponer un gasto máximo de comida de $50, los gastos existentes ingresados a partir de ayer no se compararán con esta política.</span><span class="sxs-lookup"><span data-stu-id="bee25-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="bee25-120">Al crear una directiva para una categoría de gastos que se puede desglosar, considere la posibilidad de agregar una condición para el tipo de línea de gastos.</span><span class="sxs-lookup"><span data-stu-id="bee25-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="bee25-121">Algunas políticas, como exigir un recibo, pueden no tener sentido para las líneas detalladas y solo deben aplicarse a la línea del encabezado o a una línea no detallada.</span><span class="sxs-lookup"><span data-stu-id="bee25-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="bee25-122">Las directivas de administración de gastos se evalúan respecto a la entidad de origen de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bee25-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="bee25-123">Para los escenarios de empresas vinculadas, en su lugar puede establecer que la directiva se evalúe con respecto a la entidad de destino (entidad prestataria).</span><span class="sxs-lookup"><span data-stu-id="bee25-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="bee25-124">Para ejecutar las directivas en la entidad de destino, active la característica "Evaluar la directiva con respecto a la entidad jurídica prestataria" en el área de trabajo **Administración de característica**.</span><span class="sxs-lookup"><span data-stu-id="bee25-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="bee25-125">Cuándo evaluar las directivas</span><span class="sxs-lookup"><span data-stu-id="bee25-125">When to evaluate policies</span></span>

<span data-ttu-id="bee25-126">En los parámetros de administración de gastos, hay una opción para evaluar las directivas de administración de gastos cuando se guarda una línea o cuando se envía un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="bee25-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="bee25-127">Si opta por evaluar cuándo se guarda una línea esto aseguro que los usuarios tendrán una visibilidad más temprana de lo que deben hacer para completar su informe de gastos de una vez.</span><span class="sxs-lookup"><span data-stu-id="bee25-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="bee25-128">De lo contrario, puede retrasar la evaluación de la directiva y tiene una validación al final, durante el envío al flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="bee25-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
