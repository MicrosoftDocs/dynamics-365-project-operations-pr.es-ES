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
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085078"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="eebba-104">Líneas de ofertas basadas en proyectos (Pro)</span><span class="sxs-lookup"><span data-stu-id="eebba-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="eebba-105">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="eebba-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eebba-106">Las líneas de oferta basadas en proyectos están diseñadas para ayudar a estimar el trabajo del proyecto en un compromiso.</span><span class="sxs-lookup"><span data-stu-id="eebba-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="eebba-107">La estructura de una línea de oferta basada en proyectos se amplía para las estimaciones de proyectos con los siguientes conceptos:</span><span class="sxs-lookup"><span data-stu-id="eebba-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="eebba-108">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="eebba-108">Billing Method</span></span>
- <span data-ttu-id="eebba-109">Asignación de proyectos y tareas</span><span class="sxs-lookup"><span data-stu-id="eebba-109">Project and Task Mapping</span></span>
- <span data-ttu-id="eebba-110">Clases de transacciones incluidas</span><span class="sxs-lookup"><span data-stu-id="eebba-110">Included Transaction classes</span></span>
- <span data-ttu-id="eebba-111">Límite a no exceder</span><span class="sxs-lookup"><span data-stu-id="eebba-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="eebba-112">Configuración de imputabilidad</span><span class="sxs-lookup"><span data-stu-id="eebba-112">Chargeability setup</span></span>
- <span data-ttu-id="eebba-113">Estimación utilizando los detalles de la línea de oferta</span><span class="sxs-lookup"><span data-stu-id="eebba-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="eebba-114">Clientes de línea de oferta</span><span class="sxs-lookup"><span data-stu-id="eebba-114">Quote line Customers</span></span>

<span data-ttu-id="eebba-115">La siguiente tabla proporciona información sobre los campos de la pestaña **General** de la línea de oferta basada en proyecto.</span><span class="sxs-lookup"><span data-stu-id="eebba-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="eebba-116">Estos campos ayudan a establecer la base para una estimación detallada y desde cero para el trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="eebba-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="eebba-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="eebba-117">**Field**</span></span> | <span data-ttu-id="eebba-118">**Relevancia, propósito y orientación**</span><span class="sxs-lookup"><span data-stu-id="eebba-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="eebba-119">**Impacto posterior**</span><span class="sxs-lookup"><span data-stu-id="eebba-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="eebba-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="eebba-120">Name</span></span> | <span data-ttu-id="eebba-121">El nombre de la línea de oferta que debería ayudarle a identificar el componente discreto de la oferta que se está estimando.</span><span class="sxs-lookup"><span data-stu-id="eebba-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="eebba-122">Se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-123">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="eebba-123">Billing Method</span></span> | <span data-ttu-id="eebba-124">En una oferta creada a partir de una oportunidad, este valor se copia del campo correspondiente en la línea de oportunidad.</span><span class="sxs-lookup"><span data-stu-id="eebba-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="eebba-125">Este campo incluye los dos modelos de contratación principales admitidos por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="eebba-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="eebba-126">- Precio fijo</span><span class="sxs-lookup"><span data-stu-id="eebba-126">- Fixed price</span></span></br><span data-ttu-id="eebba-127">- Tiempo y material.</span><span class="sxs-lookup"><span data-stu-id="eebba-127">- Time and material.</span></span>| <span data-ttu-id="eebba-128">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-129">Project</span><span class="sxs-lookup"><span data-stu-id="eebba-129">Project</span></span> | <span data-ttu-id="eebba-130">Utilice este campo opcional para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso.</span><span class="sxs-lookup"><span data-stu-id="eebba-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="eebba-131">Cuando un proyecto se asigna a una línea de oferta, ayuda a configurar las tareas facturables y también a traer una estimación basada en el proyecto a la línea de oferta como detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="eebba-132">Cuando un proyecto no está asignado a una línea de oferta basada en proyecto, la estimación debe crearse manualmente creando cada detalle de línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="eebba-133">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="eebba-134">Tareas incluidas</span><span class="sxs-lookup"><span data-stu-id="eebba-134">Included Tasks</span></span> | <span data-ttu-id="eebba-135">Indica si esta línea de oferta se utiliza para todas o algunas de las tareas del proyecto para el proyecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="eebba-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="eebba-136">Este campo tiene los siguientes posibles valores:</span><span class="sxs-lookup"><span data-stu-id="eebba-136">This field has the following possible values:</span></span></br><span data-ttu-id="eebba-137">- Todas las tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="eebba-137">- All project tasks</span></span></br><span data-ttu-id="eebba-138">- Solo tareas de proyecto seleccionadas</span><span class="sxs-lookup"><span data-stu-id="eebba-138">- Selected project tasks only</span></span></br><span data-ttu-id="eebba-139">Un valor en blanco en este campo es equivalente a la opción **Todas las tareas del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="eebba-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="eebba-140">Cuando se selecciona **Solo tareas de proyecto seleccionadas** en la página del proyecto, la pestaña **Configuración de facturación de tareas** le permite seleccionar tareas específicas para asociarlas a esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="eebba-141">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-142">Incluir tiempo</span><span class="sxs-lookup"><span data-stu-id="eebba-142">Include Time</span></span> | <span data-ttu-id="eebba-143">Un indicador **Sí**/**No** indica si las transacciones de tiempo o los costes laborales del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="eebba-144">Un valor **No** indica que las transacciones de tiempo o los costes laborales no se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="eebba-145">Un valor **Sí** indica que las transacciones de tiempo o los costes laborales se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="eebba-146">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-147">Incluir gasto</span><span class="sxs-lookup"><span data-stu-id="eebba-147">Include Expense</span></span> | <span data-ttu-id="eebba-148">Un indicador **Sí**/**No** indica si los costes de gastos del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="eebba-149">Un valor **No** indica que el coste de gastos no se incluirá en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="eebba-150">Un valor **Sí** indica que el coste de gastos se incluirá en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="eebba-151">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-152">Incluir tarifa</span><span class="sxs-lookup"><span data-stu-id="eebba-152">Include Fee</span></span> | <span data-ttu-id="eebba-153">Un indicador **Sí**/**No** indica si las tarifas del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="eebba-154">Un valor **No** indica que las tarifas no se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="eebba-155">Un valor **No** indica que las tarifas se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="eebba-156">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-157">Importe de la oferta</span><span class="sxs-lookup"><span data-stu-id="eebba-157">Quoted Amount</span></span> | <span data-ttu-id="eebba-158">Esta es la cantidad que se ofertará al cliente por todo el trabajo previsto en esta línea de oferta basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="eebba-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="eebba-159">En una oferta creada a partir de una oportunidad, este valor se copia del campo **Presupuesto del cliente** correspondiente en la línea de oportunidad.</span><span class="sxs-lookup"><span data-stu-id="eebba-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="eebba-160">Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="eebba-161">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-162">Impuesto estimado</span><span class="sxs-lookup"><span data-stu-id="eebba-162">Estimated Tax</span></span> | <span data-ttu-id="eebba-163">Este es un campo editable para que el usuario agregue el importe del impuesto estimado en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="eebba-164">Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los impuestos de los detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="eebba-165">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-166">Importe ofertado después de impuestos</span><span class="sxs-lookup"><span data-stu-id="eebba-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="eebba-167">Este campo es el importe de la línea de oferta después de impuestos y es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eebba-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="eebba-168">La cantidad de este campo se calcula como *Importe ofertado + Impuestos*.</span><span class="sxs-lookup"><span data-stu-id="eebba-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="eebba-169">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-170">Límite de No exceder</span><span class="sxs-lookup"><span data-stu-id="eebba-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="eebba-171">Este campo es editable y solo está disponible en líneas de oferta basadas en proyectos que tienen un método de facturación **Tiempo y material**.</span><span class="sxs-lookup"><span data-stu-id="eebba-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="eebba-172">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="eebba-173">Presupuesto del cliente</span><span class="sxs-lookup"><span data-stu-id="eebba-173">Customer Budget</span></span> | <span data-ttu-id="eebba-174">Este campo es editable y se copia a partir del campo correspondiente de la línea de oportunidad si la oferta se creo a partir de una oportunidad.</span><span class="sxs-lookup"><span data-stu-id="eebba-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="eebba-175">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="eebba-176">Reglas de validación para campos en la pestaña General de líneas de oferta basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="eebba-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="eebba-177">**Regla 1** : si el campo **Tareas incluidas** está en blanco, o si está configurado en **Todas las tareas del proyecto** , se incluye un proyecto en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="eebba-178">**Regla 2** : si el campo **Tareas incluidas** está en blanco, o si está configurado en **Todas las tareas del proyecto** , un proyecto y una determinada clase de transacción solo se pueden incluir en una línea de oferta basada en proyectos de una oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="eebba-179">**Regla 3** : si el campo **Tareas incluidas** está configurado en **Solo tareas del proyecto seleccionadas** , un proyecto y una determinada clase de transacción se pueden incluir en varias líneas de oferta basadas en proyectos de una oferta.</span><span class="sxs-lookup"><span data-stu-id="eebba-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="eebba-180">**Regla 4** : si una oportunidad tiene varias ofertas, puede haber líneas de oferta de ofertas diferentes que hagan referencia al mismo proyecto e incluyan la misma clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="eebba-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="eebba-181">**Regla 5** : si las ofertas no pertenecen a la misma oportunidad, no pueden incluir el mismo proyecto y clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="eebba-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="eebba-182">
                    <strong>Oportunidad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="eebba-183">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="eebba-184">
                    <strong>Línea de oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="eebba-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="eebba-186">
                    <strong>Tareas incluidas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="eebba-187">
                    <strong>Incluir tiempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="eebba-188">
                    <strong>Incluir gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="eebba-189">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="eebba-190">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="eebba-191">
                    <strong>Válido/no válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="eebba-192">
                    <strong>Razón</strong>
                </span><span class="sxs-lookup"><span data-stu-id="eebba-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="eebba-193">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-194">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-195">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-196">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-197">Blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-198">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-199">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-200">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-201">No válido</span><span class="sxs-lookup"><span data-stu-id="eebba-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-202">Infracción de la regla n.º 2.</span><span class="sxs-lookup"><span data-stu-id="eebba-202">Violation of Rule #2.</span></span> <span data-ttu-id="eebba-203">El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en las líneas de oferta QL1 y QL2.</span><span class="sxs-lookup"><span data-stu-id="eebba-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="eebba-204">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-205">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-206">QL2</span><span class="sxs-lookup"><span data-stu-id="eebba-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-207">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-208">Blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-209">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-210">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-211">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-211">Yes</span></span> </p>
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
<span data-ttu-id="eebba-212">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-213">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-214">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-215">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-216">Blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-217">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-218">No</span><span class="sxs-lookup"><span data-stu-id="eebba-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-219">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-220">No válido</span><span class="sxs-lookup"><span data-stu-id="eebba-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-221">Infracción de la regla n.º 2.</span><span class="sxs-lookup"><span data-stu-id="eebba-221">Violation of Rule #2.</span></span> <span data-ttu-id="eebba-222">El tiempo y las tarifas del proyecto P1 se incluyen en las líneas de oferta QL1 y QL2.</span><span class="sxs-lookup"><span data-stu-id="eebba-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="eebba-223">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-224">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-225">QL2</span><span class="sxs-lookup"><span data-stu-id="eebba-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-226">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-227">Blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-228">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-229">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-230">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-230">Yes</span></span> </p>
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
<span data-ttu-id="eebba-231">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-232">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-233">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-234">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-235">Blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-236">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-237">No</span><span class="sxs-lookup"><span data-stu-id="eebba-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-238">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-239">Válido</span><span class="sxs-lookup"><span data-stu-id="eebba-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="eebba-240">El tiempo y las tarifas del proyecto P1 se incluyen en QL1.</span><span class="sxs-lookup"><span data-stu-id="eebba-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="eebba-241">El gasto del proyecto P1 se incluyen en QL2.</span><span class="sxs-lookup"><span data-stu-id="eebba-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="eebba-242">No hay superposición en lo que se incluye en cada línea de oferta y es válido.</span><span class="sxs-lookup"><span data-stu-id="eebba-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="eebba-243">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-244">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-245">QL2</span><span class="sxs-lookup"><span data-stu-id="eebba-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-246">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-247">Blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-248">No</span><span class="sxs-lookup"><span data-stu-id="eebba-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-249">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-250">No</span><span class="sxs-lookup"><span data-stu-id="eebba-250">No</span></span> </p>
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
<span data-ttu-id="eebba-251">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-252">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-253">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-254">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-255">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="eebba-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-256">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-257">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-258">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-259">No válido</span><span class="sxs-lookup"><span data-stu-id="eebba-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-260">Infracción de la regla n.º 2 anterior</span><span class="sxs-lookup"><span data-stu-id="eebba-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="eebba-261">Q1 incluye tiempo, gastos y tarifas en un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="eebba-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="eebba-262">QL2 incluye tiempo, gastos y tarifas para todo el proyecto P1 y se superpone con lo que se incluye en Q1.</span><span class="sxs-lookup"><span data-stu-id="eebba-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="eebba-263">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-264">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-265">QL2</span><span class="sxs-lookup"><span data-stu-id="eebba-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-266">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-267">Blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-268">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-269">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-270">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-270">Yes</span></span> </p>
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
<span data-ttu-id="eebba-271">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-272">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-273">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-274">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-275">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="eebba-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-276">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-277">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-278">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-279">Válido</span><span class="sxs-lookup"><span data-stu-id="eebba-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-280">Según la regla n.° 3 anterior,</span><span class="sxs-lookup"><span data-stu-id="eebba-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="eebba-281">Q1 incluye tiempo, gastos y tarifas en un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="eebba-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="eebba-282">QL2 incluye tiempo, gastos y tarifas para un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="eebba-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="eebba-283">La única validación adicional es alrededor del subconjunto de tareas de QL1 que son diferentes del subconjunto de tareas de QL2.</span><span class="sxs-lookup"><span data-stu-id="eebba-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="eebba-284">Esto asegura que no haya superposiciones.</span><span class="sxs-lookup"><span data-stu-id="eebba-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="eebba-285">Esto lo hace el sistema cuando se asocian tareas.</span><span class="sxs-lookup"><span data-stu-id="eebba-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="eebba-286">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-287">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-288">QL2</span><span class="sxs-lookup"><span data-stu-id="eebba-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-289">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-290">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="eebba-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-291">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-292">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-293">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-293">Yes</span></span> </p>
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
<span data-ttu-id="eebba-294">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-295">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-296">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-297">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-298">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-299">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-300">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-301">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="eebba-302">Válido</span><span class="sxs-lookup"><span data-stu-id="eebba-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-303">Según la Regla n.° 5, Q1 y Q2 son dos ofertas de la misma oportunidad, por lo que ambas pueden estimar los mismos componentes de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="eebba-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="eebba-304">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-305">T2</span><span class="sxs-lookup"><span data-stu-id="eebba-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-306">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-307">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-308">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-309">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-310">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-311">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-311">Yes</span></span> </p>
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
<span data-ttu-id="eebba-312">O1</span><span class="sxs-lookup"><span data-stu-id="eebba-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-313">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-314">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-315">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-316">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-317">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-318">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-319">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="eebba-320">Válido</span><span class="sxs-lookup"><span data-stu-id="eebba-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="eebba-321">Según la Regla n.° 4, Q1 y Q2 son dos ofertas de diferentes oportunidades, por lo que no pueden estimar los mismos componentes del mismo proyecto.</span><span class="sxs-lookup"><span data-stu-id="eebba-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="eebba-322">O2</span><span class="sxs-lookup"><span data-stu-id="eebba-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="eebba-323">T1</span><span class="sxs-lookup"><span data-stu-id="eebba-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-324">QL1</span><span class="sxs-lookup"><span data-stu-id="eebba-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-325">P1</span><span class="sxs-lookup"><span data-stu-id="eebba-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="eebba-326">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="eebba-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-327">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="eebba-328">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="eebba-329">Sí</span><span class="sxs-lookup"><span data-stu-id="eebba-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="eebba-330">No válido</span><span class="sxs-lookup"><span data-stu-id="eebba-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

