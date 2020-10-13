---
title: Líneas de ofertas basadas en proyectos (Pro)
description: Este tema proporciona información sobre el uso de líneas de oferta basadas en proyectos para trabajo de proyecto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908629"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="fce89-104">Líneas de ofertas basadas en proyectos (Pro)</span><span class="sxs-lookup"><span data-stu-id="fce89-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="fce89-105">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="fce89-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fce89-106">Las líneas de oferta basadas en proyectos están diseñadas para ayudar a estimar el trabajo del proyecto en un compromiso.</span><span class="sxs-lookup"><span data-stu-id="fce89-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="fce89-107">La estructura de una línea de oferta basada en proyectos se amplía para las estimaciones de proyectos con los siguientes conceptos:</span><span class="sxs-lookup"><span data-stu-id="fce89-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="fce89-108">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="fce89-108">Billing Method</span></span>
- <span data-ttu-id="fce89-109">Asignación de proyectos y tareas</span><span class="sxs-lookup"><span data-stu-id="fce89-109">Project and Task Mapping</span></span>
- <span data-ttu-id="fce89-110">Clases de transacciones incluidas</span><span class="sxs-lookup"><span data-stu-id="fce89-110">Included Transaction classes</span></span>
- <span data-ttu-id="fce89-111">Límite a no exceder</span><span class="sxs-lookup"><span data-stu-id="fce89-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="fce89-112">Configuración de imputabilidad</span><span class="sxs-lookup"><span data-stu-id="fce89-112">Chargeability setup</span></span>
- <span data-ttu-id="fce89-113">Estimación utilizando los detalles de la línea de oferta</span><span class="sxs-lookup"><span data-stu-id="fce89-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="fce89-114">Clientes de línea de oferta</span><span class="sxs-lookup"><span data-stu-id="fce89-114">Quote line Customers</span></span>

<span data-ttu-id="fce89-115">La siguiente tabla proporciona información sobre los campos de la pestaña **General** de la línea de oferta basada en proyecto.</span><span class="sxs-lookup"><span data-stu-id="fce89-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="fce89-116">Estos campos ayudan a establecer la base para una estimación detallada y desde cero para el trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="fce89-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="fce89-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="fce89-117">**Field**</span></span> | <span data-ttu-id="fce89-118">**Relevancia, propósito y orientación**</span><span class="sxs-lookup"><span data-stu-id="fce89-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="fce89-119">**Impacto posterior**</span><span class="sxs-lookup"><span data-stu-id="fce89-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fce89-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fce89-120">Name</span></span> | <span data-ttu-id="fce89-121">El nombre de la línea de oferta que debería ayudarle a identificar el componente discreto de la oferta que se está estimando.</span><span class="sxs-lookup"><span data-stu-id="fce89-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="fce89-122">Se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-123">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="fce89-123">Billing Method</span></span> | <span data-ttu-id="fce89-124">En una oferta creada a partir de una oportunidad, este valor se copia del campo correspondiente en la línea de oportunidad.</span><span class="sxs-lookup"><span data-stu-id="fce89-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="fce89-125">Este campo incluye los dos modelos de contratación principales admitidos por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="fce89-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="fce89-126">- Precio fijo</span><span class="sxs-lookup"><span data-stu-id="fce89-126">- Fixed price</span></span></br><span data-ttu-id="fce89-127">- Tiempo y material.</span><span class="sxs-lookup"><span data-stu-id="fce89-127">- Time and material.</span></span>| <span data-ttu-id="fce89-128">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-129">Project</span><span class="sxs-lookup"><span data-stu-id="fce89-129">Project</span></span> | <span data-ttu-id="fce89-130">Utilice este campo opcional para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso.</span><span class="sxs-lookup"><span data-stu-id="fce89-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="fce89-131">Cuando un proyecto se asigna a una línea de oferta, ayuda a configurar las tareas facturables y también a traer una estimación basada en el proyecto a la línea de oferta como detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="fce89-132">Cuando un proyecto no está asignado a una línea de oferta basada en proyecto, la estimación debe crearse manualmente creando cada detalle de línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="fce89-133">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="fce89-134">Tareas incluidas</span><span class="sxs-lookup"><span data-stu-id="fce89-134">Included Tasks</span></span> | <span data-ttu-id="fce89-135">Indica si esta línea de oferta se utiliza para todas o algunas de las tareas del proyecto para el proyecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fce89-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="fce89-136">Este campo tiene los siguientes posibles valores:</span><span class="sxs-lookup"><span data-stu-id="fce89-136">This field has the following possible values:</span></span></br><span data-ttu-id="fce89-137">- Todas las tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="fce89-137">- All project tasks</span></span></br><span data-ttu-id="fce89-138">- Solo tareas de proyecto seleccionadas</span><span class="sxs-lookup"><span data-stu-id="fce89-138">- Selected project tasks only</span></span></br><span data-ttu-id="fce89-139">Un valor en blanco en este campo es equivalente a la opción **Todas las tareas del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="fce89-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="fce89-140">Cuando se selecciona **Solo tareas de proyecto seleccionadas** en la página del proyecto, la pestaña **Configuración de facturación de tareas** le permite seleccionar tareas específicas para asociarlas a esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="fce89-141">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-142">Incluir tiempo</span><span class="sxs-lookup"><span data-stu-id="fce89-142">Include Time</span></span> | <span data-ttu-id="fce89-143">Un indicador **Sí**/**No** indica si las transacciones de tiempo o los costes laborales del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fce89-144">Un valor **No** indica que las transacciones de tiempo o los costes laborales no se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fce89-145">Un valor **Sí** indica que las transacciones de tiempo o los costes laborales se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fce89-146">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-147">Incluir gasto</span><span class="sxs-lookup"><span data-stu-id="fce89-147">Include Expense</span></span> | <span data-ttu-id="fce89-148">Un indicador **Sí**/**No** indica si los costes de gastos del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fce89-149">Un valor **No** indica que el coste de gastos no se incluirá en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fce89-150">Un valor **Sí** indica que el coste de gastos se incluirá en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fce89-151">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-152">Incluir tarifa</span><span class="sxs-lookup"><span data-stu-id="fce89-152">Include Fee</span></span> | <span data-ttu-id="fce89-153">Un indicador **Sí**/**No** indica si las tarifas del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fce89-154">Un valor **No** indica que las tarifas no se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fce89-155">Un valor **No** indica que las tarifas se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fce89-156">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-157">Importe de la oferta</span><span class="sxs-lookup"><span data-stu-id="fce89-157">Quoted Amount</span></span> | <span data-ttu-id="fce89-158">Esta es la cantidad que se ofertará al cliente por todo el trabajo previsto en esta línea de oferta basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="fce89-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="fce89-159">En una oferta creada a partir de una oportunidad, este valor se copia del campo **Presupuesto del cliente** correspondiente en la línea de oportunidad.</span><span class="sxs-lookup"><span data-stu-id="fce89-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="fce89-160">Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="fce89-161">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-162">Impuesto estimado</span><span class="sxs-lookup"><span data-stu-id="fce89-162">Estimated Tax</span></span> | <span data-ttu-id="fce89-163">Este es un campo editable para que el usuario agregue el importe del impuesto estimado en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="fce89-164">Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los impuestos de los detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="fce89-165">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-166">Importe ofertado después de impuestos</span><span class="sxs-lookup"><span data-stu-id="fce89-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="fce89-167">Este campo es el importe de la línea de oferta después de impuestos y es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fce89-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="fce89-168">La cantidad de este campo se calcula como *Importe ofertado + Impuestos*.</span><span class="sxs-lookup"><span data-stu-id="fce89-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="fce89-169">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-170">Límite de No exceder</span><span class="sxs-lookup"><span data-stu-id="fce89-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="fce89-171">Este campo es editable y solo está disponible en líneas de oferta basadas en proyectos que tienen un método de facturación **Tiempo y material**.</span><span class="sxs-lookup"><span data-stu-id="fce89-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="fce89-172">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fce89-173">Presupuesto del cliente</span><span class="sxs-lookup"><span data-stu-id="fce89-173">Customer Budget</span></span> | <span data-ttu-id="fce89-174">Este campo es editable y se copia a partir del campo correspondiente de la línea de oportunidad si la oferta se creo a partir de una oportunidad.</span><span class="sxs-lookup"><span data-stu-id="fce89-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="fce89-175">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="fce89-176">Reglas de validación para campos en la pestaña General de líneas de oferta basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="fce89-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="fce89-177">**Regla 1**: si el campo **Tareas incluidas** está en blanco, o si está configurado en **Todas las tareas del proyecto**, se incluye un proyecto en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="fce89-178">**Regla 2**: si el campo **Tareas incluidas** está en blanco, o si está configurado en **Todas las tareas del proyecto**, un proyecto y una determinada clase de transacción solo se pueden incluir en una línea de oferta basada en proyectos de una oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="fce89-179">**Regla 3**: si el campo **Tareas incluidas** está configurado en **Solo tareas del proyecto seleccionadas**, un proyecto y una determinada clase de transacción se pueden incluir en varias líneas de oferta basadas en proyectos de una oferta.</span><span class="sxs-lookup"><span data-stu-id="fce89-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="fce89-180">**Regla 4**: si una oportunidad tiene varias ofertas, puede haber líneas de oferta de ofertas diferentes que hagan referencia al mismo proyecto e incluyan la misma clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="fce89-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="fce89-181">**Regla 5**: si las ofertas no pertenecen a la misma oportunidad, no pueden incluir el mismo proyecto y clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="fce89-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="fce89-182">
                    <strong>Oportunidad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="fce89-183">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fce89-184">
                    <strong>Línea de oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fce89-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="fce89-186">
                    <strong>Tareas incluidas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fce89-187">
                    <strong>Incluir tiempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fce89-188">
                    <strong>Incluir gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fce89-189">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="fce89-190">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="fce89-191">
                    <strong>Válido/no válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="fce89-192">
                    <strong>Razón</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fce89-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-193">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-194">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-195">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-196">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-197">Blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-198">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-199">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-200">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-201">No válido</span><span class="sxs-lookup"><span data-stu-id="fce89-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-202">Infracción de la regla n.º 2.</span><span class="sxs-lookup"><span data-stu-id="fce89-202">Violation of Rule #2.</span></span> <span data-ttu-id="fce89-203">El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en las líneas de oferta QL1 y QL2.</span><span class="sxs-lookup"><span data-stu-id="fce89-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-204">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-205">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-206">QL2</span><span class="sxs-lookup"><span data-stu-id="fce89-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-207">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-208">Blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-209">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-210">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-211">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-212">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-213">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-214">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-215">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-216">Blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-217">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-218">No</span><span class="sxs-lookup"><span data-stu-id="fce89-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-219">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-220">No válido</span><span class="sxs-lookup"><span data-stu-id="fce89-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-221">Infracción de la regla n.º 2.</span><span class="sxs-lookup"><span data-stu-id="fce89-221">Violation of Rule #2.</span></span> <span data-ttu-id="fce89-222">El tiempo y las tarifas del proyecto P1 se incluyen en las líneas de oferta QL1 y QL2.</span><span class="sxs-lookup"><span data-stu-id="fce89-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-223">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-224">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-225">QL2</span><span class="sxs-lookup"><span data-stu-id="fce89-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-226">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-227">Blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-228">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-229">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-230">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-231">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-232">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-233">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-234">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-235">Blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-236">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-237">No</span><span class="sxs-lookup"><span data-stu-id="fce89-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-238">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-239">Válido</span><span class="sxs-lookup"><span data-stu-id="fce89-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="fce89-240">El tiempo y las tarifas del proyecto P1 se incluyen en QL1.</span><span class="sxs-lookup"><span data-stu-id="fce89-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="fce89-241">El gasto del proyecto P1 se incluyen en QL2.</span><span class="sxs-lookup"><span data-stu-id="fce89-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="fce89-242">No hay superposición en lo que se incluye en cada línea de oferta y es válido.</span><span class="sxs-lookup"><span data-stu-id="fce89-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-243">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-244">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-245">QL2</span><span class="sxs-lookup"><span data-stu-id="fce89-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-246">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-247">Blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-248">No</span><span class="sxs-lookup"><span data-stu-id="fce89-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-249">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-250">No</span><span class="sxs-lookup"><span data-stu-id="fce89-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-251">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-252">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-253">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-254">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-255">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="fce89-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-256">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-257">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-258">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-259">No válido</span><span class="sxs-lookup"><span data-stu-id="fce89-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-260">Infracción de la regla n.º 2 anterior</span><span class="sxs-lookup"><span data-stu-id="fce89-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="fce89-261">Q1 incluye tiempo, gastos y tarifas en un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="fce89-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fce89-262">QL2 incluye tiempo, gastos y tarifas para todo el proyecto P1 y se superpone con lo que se incluye en Q1.</span><span class="sxs-lookup"><span data-stu-id="fce89-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-263">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-264">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-265">QL2</span><span class="sxs-lookup"><span data-stu-id="fce89-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-266">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-267">Blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-268">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-269">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-270">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-271">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-272">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-273">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-274">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-275">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="fce89-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-276">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-277">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-278">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-279">Válido</span><span class="sxs-lookup"><span data-stu-id="fce89-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-280">Según la regla n.° 3 anterior,</span><span class="sxs-lookup"><span data-stu-id="fce89-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="fce89-281">Q1 incluye tiempo, gastos y tarifas en un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="fce89-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fce89-282">QL2 incluye tiempo, gastos y tarifas para un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="fce89-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fce89-283">La única validación adicional es alrededor del subconjunto de tareas de QL1 que son diferentes del subconjunto de tareas de QL2.</span><span class="sxs-lookup"><span data-stu-id="fce89-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="fce89-284">Esto asegura que no haya superposiciones.</span><span class="sxs-lookup"><span data-stu-id="fce89-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="fce89-285">Esto lo hace el sistema cuando se asocian tareas.</span><span class="sxs-lookup"><span data-stu-id="fce89-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-286">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-287">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-288">QL2</span><span class="sxs-lookup"><span data-stu-id="fce89-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-289">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-290">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="fce89-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-291">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-292">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-293">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-294">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-295">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-296">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-297">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-298">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-299">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-300">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-301">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fce89-302">Válido</span><span class="sxs-lookup"><span data-stu-id="fce89-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-303">Según la Regla n.° 5, Q1 y Q2 son dos ofertas de la misma oportunidad, por lo que ambas pueden estimar los mismos componentes de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="fce89-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-304">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-305">T2</span><span class="sxs-lookup"><span data-stu-id="fce89-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-306">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-307">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-308">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-309">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-310">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-311">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-312">O1</span><span class="sxs-lookup"><span data-stu-id="fce89-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-313">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-314">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-315">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-316">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-317">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-318">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-319">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fce89-320">Válido</span><span class="sxs-lookup"><span data-stu-id="fce89-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fce89-321">Según la Regla n.° 4, Q1 y Q2 son dos ofertas de diferentes oportunidades, por lo que no pueden estimar los mismos componentes del mismo proyecto.</span><span class="sxs-lookup"><span data-stu-id="fce89-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fce89-322">O2</span><span class="sxs-lookup"><span data-stu-id="fce89-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fce89-323">T1</span><span class="sxs-lookup"><span data-stu-id="fce89-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-324">QL1</span><span class="sxs-lookup"><span data-stu-id="fce89-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-325">P1</span><span class="sxs-lookup"><span data-stu-id="fce89-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fce89-326">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="fce89-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-327">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fce89-328">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fce89-329">Sí</span><span class="sxs-lookup"><span data-stu-id="fce89-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fce89-330">No válido</span><span class="sxs-lookup"><span data-stu-id="fce89-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

