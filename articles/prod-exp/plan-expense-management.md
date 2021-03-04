---
title: Configurar la gestión de gastos
description: Este artículo describe las consideraciones y las decisiones que debe tomar durante el proceso de planificación antes de configurar la administración de gastos en Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960358"
---
# <a name="configure-expense-management"></a><span data-ttu-id="3f29b-103">Configurar la gestión de gastos</span><span class="sxs-lookup"><span data-stu-id="3f29b-103">Configure expense management</span></span>

<span data-ttu-id="3f29b-104">Este tema describe las consideraciones y las decisiones que debe tomar durante el proceso de planificación antes de configurar la administración de gastos.</span><span class="sxs-lookup"><span data-stu-id="3f29b-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="3f29b-105">En la Gestión de gastos, puede almacenar información sobre métodos de pago, solicitudes de viaje, informes de gastos, políticas, etc.</span><span class="sxs-lookup"><span data-stu-id="3f29b-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="3f29b-106">Debido a que muchas de las decisiones que toma cuando planifica su configuración para la gestión de gastos se basan en la jerarquía y la estructura financiera de su organización, debe consultar los documentos de planificación para esas áreas.</span><span class="sxs-lookup"><span data-stu-id="3f29b-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="3f29b-107">Gastos de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="3f29b-107">Intercompany expenses</span></span>

<span data-ttu-id="3f29b-108">Cuando habilita los gastos de empresas vinculadas, permite que las entidades legales y los empleados incurran en gastos en nombre de otra entidad legal y cobren el pago de la entidad legal de empleo dentro de su organización.</span><span class="sxs-lookup"><span data-stu-id="3f29b-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="3f29b-109">Por ejemplo, un empleado de la entidad legal A completa un proyecto para la entidad legal B y el proyecto incurre en gastos relacionados con viajes.</span><span class="sxs-lookup"><span data-stu-id="3f29b-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="3f29b-110">Si los gastos de empresas vinculadas están habilitados, el empleado puede presentar un informe de gastos que contabilizará el gasto en la entidad jurídica B, y el gasto deberá pagarlo la entidad jurídica A. Si su organización no tiene varias entidades jurídicas, no t tiene que habilitar los gastos de empresas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="3f29b-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="3f29b-111">**Decisión:** ¿Quiere habilitar los gastos de empresas vinculadas?</span><span class="sxs-lookup"><span data-stu-id="3f29b-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="3f29b-112">Administración financiera</span><span class="sxs-lookup"><span data-stu-id="3f29b-112">Financial management</span></span>

<span data-ttu-id="3f29b-113">La gestión de gastos está estrechamente integrada con la gestión financiera de su organización.</span><span class="sxs-lookup"><span data-stu-id="3f29b-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="3f29b-114">Gran parte de su configuración para la gestión de gastos se basará en las decisiones que haya tomado sobre las finanzas de su organización.</span><span class="sxs-lookup"><span data-stu-id="3f29b-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="3f29b-115">Las siguientes secciones describen las diversas áreas que requieren planificación y decisiones, según las decisiones financieras de su organización y la orientación de su equipo de liderazgo.</span><span class="sxs-lookup"><span data-stu-id="3f29b-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="3f29b-116">Dietas</span><span class="sxs-lookup"><span data-stu-id="3f29b-116">Per diems</span></span>

<span data-ttu-id="3f29b-117">Debe definir las dietas de los empleados que proporciona su organización.</span><span class="sxs-lookup"><span data-stu-id="3f29b-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="3f29b-118">Debido a que las dietas se utilizan normalmente para cubrir gastos como comidas, alojamiento y otros gastos incidentales, puede crear reglas para las dietas que ofrece su organización.</span><span class="sxs-lookup"><span data-stu-id="3f29b-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="3f29b-119">las tarifas de dietas pueden basarse en la época del año, el lugar de viaje o ambos.</span><span class="sxs-lookup"><span data-stu-id="3f29b-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="3f29b-120">Cuando define una regla de dietas, puede especificar que se retendrá un porcentaje de la tarifa de dieta si un trabajador recibe comidas o servicios gratuitos.</span><span class="sxs-lookup"><span data-stu-id="3f29b-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="3f29b-121">También puede definir niveles de tarifas de dietas para establecer el mínimo y máximo de horas que la tarifa de dieta puede aplicarse al viaje de un trabajador.</span><span class="sxs-lookup"><span data-stu-id="3f29b-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="3f29b-122">**Decisiones:**</span><span class="sxs-lookup"><span data-stu-id="3f29b-122">**Decisions:**</span></span>

- <span data-ttu-id="3f29b-123">Reglas predeterminadas de dietas para el primer y último día:</span><span class="sxs-lookup"><span data-stu-id="3f29b-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="3f29b-124">¿Cuál es la cantidad mínima de horas que un empleado puede reclamar por día y aún recibir dietas?</span><span class="sxs-lookup"><span data-stu-id="3f29b-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="3f29b-125">¿Hay una reducción en la cantidad que se ofrece por las comidas del primer y último día?</span><span class="sxs-lookup"><span data-stu-id="3f29b-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="3f29b-126">Si hay una reducción, ¿cuál es el porcentaje de la reducción?</span><span class="sxs-lookup"><span data-stu-id="3f29b-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3f29b-127">¿Hay una reducción en la cantidad que se ofrece por un hotel del primer y último día?</span><span class="sxs-lookup"><span data-stu-id="3f29b-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="3f29b-128">Si hay una reducción, ¿cuál es el porcentaje de la reducción?</span><span class="sxs-lookup"><span data-stu-id="3f29b-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3f29b-129">¿Hay una reducción en la cantidad que se ofrece por un otros gastos del primer y último día?</span><span class="sxs-lookup"><span data-stu-id="3f29b-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="3f29b-130">Si hay una reducción, ¿cuál es el porcentaje de la reducción?</span><span class="sxs-lookup"><span data-stu-id="3f29b-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="3f29b-131">Reglas de dietas predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="3f29b-131">Default per diem rules:</span></span>

    - <span data-ttu-id="3f29b-132">¿Existe una reducción porcentual en la asignación de dietas para cada comida si, por ejemplo, la comida es gratuita?</span><span class="sxs-lookup"><span data-stu-id="3f29b-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="3f29b-133">Si hay una reducción, ¿cuál es el porcentaje de la reducción para cada comida?</span><span class="sxs-lookup"><span data-stu-id="3f29b-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="3f29b-134">¿Se calcula la reducción de comida por día, por viaje o por el número de comidas por día?</span><span class="sxs-lookup"><span data-stu-id="3f29b-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="3f29b-135">¿Deben redondearse las cantidades de las dietas de la manera habitual o redondearlas hacia arriba?</span><span class="sxs-lookup"><span data-stu-id="3f29b-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="3f29b-136">¿Se calculan las dietas en un período de 24 horas o en un día calendario?</span><span class="sxs-lookup"><span data-stu-id="3f29b-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="3f29b-137">Reglas de dietas que se basan en la ubicación:</span><span class="sxs-lookup"><span data-stu-id="3f29b-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="3f29b-138">¿Varían las tarifas de dietas según la ubicación?</span><span class="sxs-lookup"><span data-stu-id="3f29b-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="3f29b-139">¿Qué ubicaciones están incluidas?</span><span class="sxs-lookup"><span data-stu-id="3f29b-139">What locations are included?</span></span>
    - <span data-ttu-id="3f29b-140">Si las tarifas de dietas varían según la ubicación, para cada ubicación, qué porcentaje se proporciona para los siguientes tipos de gastos:</span><span class="sxs-lookup"><span data-stu-id="3f29b-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="3f29b-141">Comidas</span><span class="sxs-lookup"><span data-stu-id="3f29b-141">Meals</span></span>
        - <span data-ttu-id="3f29b-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="3f29b-142">Hotel</span></span>
        - <span data-ttu-id="3f29b-143">Otros gastos</span><span class="sxs-lookup"><span data-stu-id="3f29b-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="3f29b-144">Diarios y cuentas de gestión de gastos</span><span class="sxs-lookup"><span data-stu-id="3f29b-144">Expense management journals and accounts</span></span>

<span data-ttu-id="3f29b-145">La gestión de gastos requiere que utilice varios diarios y cuentas.</span><span class="sxs-lookup"><span data-stu-id="3f29b-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="3f29b-146">Debe decidir, por ejemplo, si se utiliza la misma cuenta para adelantos en efectivo y disputas de tarjetas de crédito.</span><span class="sxs-lookup"><span data-stu-id="3f29b-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="3f29b-147">**Decisiones:**</span><span class="sxs-lookup"><span data-stu-id="3f29b-147">**Decisions:**</span></span>

- <span data-ttu-id="3f29b-148">¿En qué diario del libro mayor se registran los informes de gastos aprobados?</span><span class="sxs-lookup"><span data-stu-id="3f29b-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="3f29b-149">¿Qué cuenta se utiliza para adelantos en efectivo?</span><span class="sxs-lookup"><span data-stu-id="3f29b-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="3f29b-150">¿Deben contabilizarse los anticipos en efectivo inmediatamente?</span><span class="sxs-lookup"><span data-stu-id="3f29b-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="3f29b-151">Métodos de pago</span><span class="sxs-lookup"><span data-stu-id="3f29b-151">Payment methods</span></span>

<span data-ttu-id="3f29b-152">Cuando permite que los empleados incurran en gastos en nombre de su empresa, debe definir los métodos de pago que los empleados pueden utilizar.</span><span class="sxs-lookup"><span data-stu-id="3f29b-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="3f29b-153">Por ejemplo, puede permitir que los empleados usen efectivo o una tarjeta de crédito corporativa.</span><span class="sxs-lookup"><span data-stu-id="3f29b-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="3f29b-154">También puede permitir que los empleados usen tarjetas de crédito personales y luego reembolsar a los empleados.</span><span class="sxs-lookup"><span data-stu-id="3f29b-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="3f29b-155">Debe tomar las siguientes decisiones para cada método de pago que permita.</span><span class="sxs-lookup"><span data-stu-id="3f29b-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="3f29b-156">**Decisiones:**</span><span class="sxs-lookup"><span data-stu-id="3f29b-156">**Decisions:**</span></span>

- <span data-ttu-id="3f29b-157">¿Qué métodos de pago están permitidos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="3f29b-158">¿A quién pertenecen los gastos del método de pago?</span><span class="sxs-lookup"><span data-stu-id="3f29b-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="3f29b-159">¿Existe un tipo de cuenta de compensación?</span><span class="sxs-lookup"><span data-stu-id="3f29b-159">Is there an offset account type?</span></span> <span data-ttu-id="3f29b-160">Si hay un tipo de cuenta de compensación, ¿cuál es?</span><span class="sxs-lookup"><span data-stu-id="3f29b-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="3f29b-161">Si hay una cuenta de compensación, ¿cuál es?</span><span class="sxs-lookup"><span data-stu-id="3f29b-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="3f29b-162">Si el método de pago es una tarjeta de crédito, ¿debe utilizarse el método de pago solo con transacciones importadas?</span><span class="sxs-lookup"><span data-stu-id="3f29b-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="3f29b-163">Categorías de gasto y categorías compartidas</span><span class="sxs-lookup"><span data-stu-id="3f29b-163">Expense categories and shared categories</span></span>

<span data-ttu-id="3f29b-164">Cuando los empleados crean un informe de gastos, cada gasto que registran debe asociarse con una categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="3f29b-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="3f29b-165">Las categorías de gastos se derivan de categorías compartidas que se pueden compartir entre las entidades legales de su organización.</span><span class="sxs-lookup"><span data-stu-id="3f29b-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="3f29b-166">Estas categorías también se pueden compartir en Gestión de proyectos y contabilidad, según la forma en que se defina su organización.</span><span class="sxs-lookup"><span data-stu-id="3f29b-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="3f29b-167">Según la definición de su organización y la orientación del equipo de implementación, debe determinar si las categorías que se utilizan en la gestión de gastos se utilizarán solo en la gestión de gastos o si deberían compartirse entre gestión de proyectos y contabilidad y gestión de gastos.</span><span class="sxs-lookup"><span data-stu-id="3f29b-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="3f29b-168">Tenga en cuetna que estas categorías se pueden compartir entre proyecto y gastos o proyecto y producción, pero no entre gastos y producción.</span><span class="sxs-lookup"><span data-stu-id="3f29b-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="3f29b-169">Debe tomar las siguientes decisiones para cada categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="3f29b-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="3f29b-170">**Decisiones:**</span><span class="sxs-lookup"><span data-stu-id="3f29b-170">**Decisions:**</span></span>

- <span data-ttu-id="3f29b-171">¿Cuál es la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-171">What is the expense category?</span></span> <span data-ttu-id="3f29b-172">Los ejemplos incluyen categorías de vuelos, hotel o kilometraje.</span><span class="sxs-lookup"><span data-stu-id="3f29b-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="3f29b-173">¿Se puede utilizar también la categoría de gastos en la gestión y contabilidad de proyectos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="3f29b-174">¿Cuál es el tipo de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-174">What is the expense type?</span></span>
- <span data-ttu-id="3f29b-175">¿Cuál es el método de pago predeterminado para la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="3f29b-176">¿Deben desglosarse los gastos de la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="3f29b-177">¿Cuál es la cuenta principal predeterminada para la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="3f29b-178">¿Cuál es el grupo de impuestos sobre ventas de artículos predeterminado para la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="3f29b-179">¿Se permiten métodos de pago adicionales para la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="3f29b-180">Si se permiten métodos de pago adicionales, ¿cuáles son?</span><span class="sxs-lookup"><span data-stu-id="3f29b-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="3f29b-181">¿Hay subcategorías en esta categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="3f29b-182">Si hay subcategorías, deberá tomar también las siguientes decisiones:</span><span class="sxs-lookup"><span data-stu-id="3f29b-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="3f29b-183">¿Alguna de las subcategorías está excluida de la recuperación de impuestos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="3f29b-184">¿Cuál es el grupo de impuestos sobre ventas de artículos de las subcategorías?</span><span class="sxs-lookup"><span data-stu-id="3f29b-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="3f29b-185">Si la categoría de gastos también se utiliza en la gestión y contabilidad de proyectos, responda las preguntas restantes.</span><span class="sxs-lookup"><span data-stu-id="3f29b-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="3f29b-186">De lo contrario, vaya a la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="3f29b-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="3f29b-187">¿Qué cuentas de costes se utilizarán para los siguientes gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="3f29b-188">Coste</span><span class="sxs-lookup"><span data-stu-id="3f29b-188">Cost</span></span>
    - <span data-ttu-id="3f29b-189">Asignación de nómina</span><span class="sxs-lookup"><span data-stu-id="3f29b-189">Payroll allocation</span></span>
    - <span data-ttu-id="3f29b-190">Valor de coste WIP</span><span class="sxs-lookup"><span data-stu-id="3f29b-190">WIP-cost value</span></span>
    - <span data-ttu-id="3f29b-191">Elemento de coste</span><span class="sxs-lookup"><span data-stu-id="3f29b-191">Cost-item</span></span>
    - <span data-ttu-id="3f29b-192">Elemento de valor de coste WIP</span><span class="sxs-lookup"><span data-stu-id="3f29b-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="3f29b-193">Pérdida acumulada</span><span class="sxs-lookup"><span data-stu-id="3f29b-193">Accrued loss</span></span>
    - <span data-ttu-id="3f29b-194">Pérdida acumulada WIP</span><span class="sxs-lookup"><span data-stu-id="3f29b-194">WIP-accrued loss</span></span>

- <span data-ttu-id="3f29b-195">¿Qué cuentas de ingresos se utilizarán para los siguientes?</span><span class="sxs-lookup"><span data-stu-id="3f29b-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="3f29b-196">Ingresos facturados</span><span class="sxs-lookup"><span data-stu-id="3f29b-196">Invoiced revenue</span></span>
    - <span data-ttu-id="3f29b-197">Valor acumulado de ingresos de ventas</span><span class="sxs-lookup"><span data-stu-id="3f29b-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="3f29b-198">Trabajo en curso - Valor de ventas</span><span class="sxs-lookup"><span data-stu-id="3f29b-198">WIP-sales value</span></span>
    - <span data-ttu-id="3f29b-199">Ingresos acumulados - Producción</span><span class="sxs-lookup"><span data-stu-id="3f29b-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="3f29b-200">Trabajo en curso - Producción</span><span class="sxs-lookup"><span data-stu-id="3f29b-200">WIP-production</span></span>
    - <span data-ttu-id="3f29b-201">Ingresos acumulados - Ganancias</span><span class="sxs-lookup"><span data-stu-id="3f29b-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="3f29b-202">Beneficio WIP</span><span class="sxs-lookup"><span data-stu-id="3f29b-202">WIP-profit</span></span>
    - <span data-ttu-id="3f29b-203">Suscripción de ingresos acumulados</span><span class="sxs-lookup"><span data-stu-id="3f29b-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="3f29b-204">Suscripción WIP</span><span class="sxs-lookup"><span data-stu-id="3f29b-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="3f29b-205">Impuestos</span><span class="sxs-lookup"><span data-stu-id="3f29b-205">Taxes</span></span>

<span data-ttu-id="3f29b-206">Para los impuestos relacionados con los gastos, debe determinar qué se incluye o habilita en los informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="3f29b-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="3f29b-207">**Decisiones:**</span><span class="sxs-lookup"><span data-stu-id="3f29b-207">**Decisions:**</span></span>

- <span data-ttu-id="3f29b-208">¿El impuesto sobre las ventas está incluido en los montos de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="3f29b-209">¿Debe habilitarse la recuperación de impuestos sobre los gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="3f29b-210">Cuando estaba planificando el libro mayor, si decidió aplicar las reglas del impuesto sobre las ventas y el impuesto sobre el uso de EE.</span><span class="sxs-lookup"><span data-stu-id="3f29b-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="3f29b-211">(Para aplicar las reglas de impuestos sobre las ventas y sobre el uso de EE. UU., establezca la opción **Aplicar reglas de impuestos sobre las ventas** opción a **Sí**).</span><span class="sxs-lookup"><span data-stu-id="3f29b-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="3f29b-212">Directivas</span><span class="sxs-lookup"><span data-stu-id="3f29b-212">Policies</span></span>

<span data-ttu-id="3f29b-213">Al crear directivas de informes de gastos, puede ayudar a su organización a ahorrar tiempo y dinero cuando los empleados incurren en gastos en su nombre.</span><span class="sxs-lookup"><span data-stu-id="3f29b-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="3f29b-214">Las directivas ayudan a garantizar que los empleados se mantengan dentro del presupuesto, proporcionen toda la información requerida y gasten el dinero solo cuando lo requieran.</span><span class="sxs-lookup"><span data-stu-id="3f29b-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="3f29b-215">Debe tomar las siguientes decisiones para cada política de informe de gastos y cada política de aprobación de informe de gastos que cree.</span><span class="sxs-lookup"><span data-stu-id="3f29b-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="3f29b-216">**Decisiones:**</span><span class="sxs-lookup"><span data-stu-id="3f29b-216">**Decisions:**</span></span>

- <span data-ttu-id="3f29b-217">¿Cuál es el nombre de la directiva?</span><span class="sxs-lookup"><span data-stu-id="3f29b-217">What is the name of the policy?</span></span>
- <span data-ttu-id="3f29b-218">¿Para qué es la directiva de gastos?</span><span class="sxs-lookup"><span data-stu-id="3f29b-218">What is the expense policy for?</span></span>
- <span data-ttu-id="3f29b-219">Si anteriormente decidió habilitar los gastos de empresas vinculadas, ¿a qué empresas de su organización se aplicará esta directiva?</span><span class="sxs-lookup"><span data-stu-id="3f29b-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="3f29b-220">¿Cuándo entra en vigencia la directiva?</span><span class="sxs-lookup"><span data-stu-id="3f29b-220">When does the policy become effective?</span></span>
- <span data-ttu-id="3f29b-221">¿Cuándo vence la directiva?</span><span class="sxs-lookup"><span data-stu-id="3f29b-221">When does the policy expire?</span></span>
- <span data-ttu-id="3f29b-222">¿Qué es la regla de la directiva?</span><span class="sxs-lookup"><span data-stu-id="3f29b-222">What is the policy rule?</span></span>
- <span data-ttu-id="3f29b-223">¿Cuál es el resultado de la regla de la directiva?</span><span class="sxs-lookup"><span data-stu-id="3f29b-223">What is the outcome of the policy rule?</span></span>
