---
title: Líneas de ofertas basadas en proyectos
description: Este tema proporciona información sobre el uso de líneas de oferta basadas en proyectos para trabajo de proyecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085015"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="45deb-103">Líneas de ofertas basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="45deb-103">Project-based quote lines</span></span>

<span data-ttu-id="45deb-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="45deb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="45deb-105">Las líneas de oferta basadas en proyectos están diseñadas para ayudar a estimar el trabajo del proyecto en un compromiso.</span><span class="sxs-lookup"><span data-stu-id="45deb-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="45deb-106">La estructura de una línea de oferta basada en proyectos se amplía para las estimaciones de proyectos con los siguientes conceptos:</span><span class="sxs-lookup"><span data-stu-id="45deb-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="45deb-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="45deb-107">Billing Method</span></span>
- <span data-ttu-id="45deb-108">Asignación de proyectos</span><span class="sxs-lookup"><span data-stu-id="45deb-108">Project Mapping</span></span>
- <span data-ttu-id="45deb-109">Clases de transacciones incluidas</span><span class="sxs-lookup"><span data-stu-id="45deb-109">Included Transaction classes</span></span>
- <span data-ttu-id="45deb-110">Límite a no exceder</span><span class="sxs-lookup"><span data-stu-id="45deb-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="45deb-111">Configuración de imputabilidad</span><span class="sxs-lookup"><span data-stu-id="45deb-111">Chargeability setup</span></span>
- <span data-ttu-id="45deb-112">Estimación utilizando los detalles de la línea de oferta</span><span class="sxs-lookup"><span data-stu-id="45deb-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="45deb-113">Clientes de línea de oferta</span><span class="sxs-lookup"><span data-stu-id="45deb-113">Quote line Customers</span></span>

<span data-ttu-id="45deb-114">La siguiente tabla proporciona información sobre los campos de la pestaña **General** de la línea de oferta basada en proyecto.</span><span class="sxs-lookup"><span data-stu-id="45deb-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="45deb-115">Estos campos ayudan a establecer la base para una estimación detallada y desde cero para el trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="45deb-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="45deb-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="45deb-116">**Field**</span></span> | <span data-ttu-id="45deb-117">**Relevancia, propósito y orientación**</span><span class="sxs-lookup"><span data-stu-id="45deb-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="45deb-118">**Impacto posterior**</span><span class="sxs-lookup"><span data-stu-id="45deb-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="45deb-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="45deb-119">Name</span></span> | <span data-ttu-id="45deb-120">El nombre de la línea de oferta que debería ayudarle a identificar el componente discreto de la oferta que se está estimando.</span><span class="sxs-lookup"><span data-stu-id="45deb-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="45deb-121">Se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-122">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="45deb-122">Billing Method</span></span> | <span data-ttu-id="45deb-123">En una oferta creada a partir de una oportunidad, este valor se copia del campo correspondiente en la línea de oportunidad.</span><span class="sxs-lookup"><span data-stu-id="45deb-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="45deb-124">Este campo incluye los dos modelos de contratación principales admitidos por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="45deb-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="45deb-125">- Precio fijo</span><span class="sxs-lookup"><span data-stu-id="45deb-125">- Fixed price</span></span></br><span data-ttu-id="45deb-126">- Tiempo y material.</span><span class="sxs-lookup"><span data-stu-id="45deb-126">- Time and material.</span></span>| <span data-ttu-id="45deb-127">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-128">Project</span><span class="sxs-lookup"><span data-stu-id="45deb-128">Project</span></span> | <span data-ttu-id="45deb-129">Utilice este campo opcional para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso.</span><span class="sxs-lookup"><span data-stu-id="45deb-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="45deb-130">Cuando un proyecto se asigna a una línea de oferta, ayuda a configurar las tareas facturables y también a traer una estimación basada en el proyecto a la línea de oferta como detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="45deb-131">Cuando un proyecto no está asignado a una línea de oferta basada en proyecto, la estimación debe crearse manualmente creando cada detalle de línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="45deb-132">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-133">Incluir tiempo</span><span class="sxs-lookup"><span data-stu-id="45deb-133">Include Time</span></span> | <span data-ttu-id="45deb-134">Un indicador **Sí**/**No** indica si las transacciones de tiempo o los costes laborales del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="45deb-135">Un valor **No** indica que las transacciones de tiempo o los costes laborales no se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="45deb-136">Un valor **Sí** indica que las transacciones de tiempo o los costes laborales se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="45deb-137">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-138">Incluir gasto</span><span class="sxs-lookup"><span data-stu-id="45deb-138">Include Expense</span></span> | <span data-ttu-id="45deb-139">Un indicador **Sí**/**No** indica si los costes de gastos del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="45deb-140">Un valor **No** indica que el coste de gastos no se incluirá en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="45deb-141">Un valor **Sí** indica que el coste de gastos se incluirá en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="45deb-142">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-143">Incluir tarifa</span><span class="sxs-lookup"><span data-stu-id="45deb-143">Include Fee</span></span> | <span data-ttu-id="45deb-144">Un indicador **Sí**/**No** indica si las tarifas del proyecto seleccionado se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="45deb-145">Un valor **No** indica que las tarifas no se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="45deb-146">Un valor **No** indica que las tarifas se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="45deb-147">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-148">Importe de la oferta</span><span class="sxs-lookup"><span data-stu-id="45deb-148">Quoted Amount</span></span> | <span data-ttu-id="45deb-149">Esta es la cantidad que se ofertará al cliente por todo el trabajo previsto en esta línea de oferta basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="45deb-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="45deb-150">En una oferta creada a partir de una oportunidad, este valor se copia del campo **Presupuesto del cliente** correspondiente en la línea de oportunidad.</span><span class="sxs-lookup"><span data-stu-id="45deb-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="45deb-151">Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="45deb-152">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-153">Impuesto estimado</span><span class="sxs-lookup"><span data-stu-id="45deb-153">Estimated Tax</span></span> | <span data-ttu-id="45deb-154">Este es un campo editable para que el usuario agregue el importe del impuesto estimado en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="45deb-155">Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los impuestos de los detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="45deb-156">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-157">Importe ofertado después de impuestos</span><span class="sxs-lookup"><span data-stu-id="45deb-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="45deb-158">Este campo es el importe de la línea de oferta después de impuestos y es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="45deb-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="45deb-159">La cantidad de este campo se calcula como *Importe ofertado + Impuestos*.</span><span class="sxs-lookup"><span data-stu-id="45deb-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="45deb-160">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-161">Límite de No exceder</span><span class="sxs-lookup"><span data-stu-id="45deb-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="45deb-162">Este campo es editable y solo está disponible en líneas de oferta basadas en proyectos que tienen un método de facturación **Tiempo y material**.</span><span class="sxs-lookup"><span data-stu-id="45deb-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="45deb-163">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="45deb-164">Presupuesto del cliente</span><span class="sxs-lookup"><span data-stu-id="45deb-164">Customer Budget</span></span> | <span data-ttu-id="45deb-165">Este campo es editable y se copia a partir del campo correspondiente de la línea de oportunidad si la oferta se creo a partir de una oportunidad.</span><span class="sxs-lookup"><span data-stu-id="45deb-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="45deb-166">Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="45deb-167">Reglas de validación para campos en la pestaña General de líneas de oferta basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="45deb-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="45deb-168">**Regla 1** : una determinada clase de transacción en el proyecto seleccionado solo se puede incluir en una línea de oferta basada en el proyecto de una oferta.</span><span class="sxs-lookup"><span data-stu-id="45deb-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="45deb-169">**Regla 2** : si una oportunidad tiene varias ofertas, puede haber líneas de oferta de ofertas diferentes que hagan referencia al mismo proyecto e incluyan la misma clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="45deb-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="45deb-170">**Regla 3** : si las ofertas no pertenecen a la misma oportunidad, no pueden incluir el mismo proyecto y clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="45deb-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="45deb-171">
                    <strong>Oportunidad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="45deb-172">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="45deb-173">
                    <strong>Línea de oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="45deb-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="45deb-175">
                    <strong>Incluir tiempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="45deb-176">
                    <strong>Incluir gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="45deb-177">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="45deb-178">
                    <strong>tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="45deb-179">
                    <strong>Válido/no válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="45deb-180">
                    <strong>Razón</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45deb-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="45deb-181">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-182">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-183">QL1</span><span class="sxs-lookup"><span data-stu-id="45deb-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-184">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-185">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-186">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-187">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-188">No válido</span><span class="sxs-lookup"><span data-stu-id="45deb-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-189">Infracción de la regla n.º 1.</span><span class="sxs-lookup"><span data-stu-id="45deb-189">Violation of Rule #1.</span></span> <span data-ttu-id="45deb-190">El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en ambas líneas de oferta, QL1 y QL2.</span><span class="sxs-lookup"><span data-stu-id="45deb-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="45deb-191">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-192">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-193">QL2</span><span class="sxs-lookup"><span data-stu-id="45deb-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-194">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-195">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-196">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-197">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-197">Yes</span></span> </p>
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
<span data-ttu-id="45deb-198">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-199">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-200">QL1</span><span class="sxs-lookup"><span data-stu-id="45deb-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-201">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-202">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-203">No</span><span class="sxs-lookup"><span data-stu-id="45deb-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-204">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-205">No válido</span><span class="sxs-lookup"><span data-stu-id="45deb-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-206">Infracción de la regla n.º 1.</span><span class="sxs-lookup"><span data-stu-id="45deb-206">Violation of Rule #1.</span></span> <span data-ttu-id="45deb-207">El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en ambas líneas de oferta, QL1 y QL2.</span><span class="sxs-lookup"><span data-stu-id="45deb-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="45deb-208">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-209">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-210">QL2</span><span class="sxs-lookup"><span data-stu-id="45deb-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-211">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-212">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-213">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-214">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-214">Yes</span></span> </p>
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
<span data-ttu-id="45deb-215">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-216">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-217">QL1</span><span class="sxs-lookup"><span data-stu-id="45deb-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-218">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-219">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-220">No</span><span class="sxs-lookup"><span data-stu-id="45deb-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-221">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-222">Válido</span><span class="sxs-lookup"><span data-stu-id="45deb-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="45deb-223">El tiempo y las tarifas del proyecto P1 se incluyen en QL1.</span><span class="sxs-lookup"><span data-stu-id="45deb-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="45deb-224">El gasto del proyecto P1 se incluyen en QL2.</span><span class="sxs-lookup"><span data-stu-id="45deb-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="45deb-225">No hay superposición en lo que se incluye en cada línea de oferta, por lo que es válido.</span><span class="sxs-lookup"><span data-stu-id="45deb-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="45deb-226">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-227">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-228">QL2</span><span class="sxs-lookup"><span data-stu-id="45deb-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-229">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-230">No</span><span class="sxs-lookup"><span data-stu-id="45deb-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-231">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-232">No</span><span class="sxs-lookup"><span data-stu-id="45deb-232">No</span></span> </p>
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
<span data-ttu-id="45deb-233">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-234">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-235">QL1</span><span class="sxs-lookup"><span data-stu-id="45deb-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-236">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-237">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-238">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-239">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-240">No válido</span><span class="sxs-lookup"><span data-stu-id="45deb-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-241">Infracción de la regla n.º 1 anterior</span><span class="sxs-lookup"><span data-stu-id="45deb-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="45deb-242">Q1 incluye tiempo, gastos y tarifas para todo el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="45deb-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="45deb-243">QL2 incluye tiempo, gastos y tarifas para todo el proyecto P1 y se superpone con lo que se incluye en Q1.</span><span class="sxs-lookup"><span data-stu-id="45deb-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="45deb-244">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-245">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-246">QL2</span><span class="sxs-lookup"><span data-stu-id="45deb-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-247">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-248">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-249">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-250">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-250">Yes</span></span> </p>
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
<span data-ttu-id="45deb-251">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-252">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-253">QL1</span><span class="sxs-lookup"><span data-stu-id="45deb-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-254">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-255">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-256">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-257">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="45deb-258">Válido</span><span class="sxs-lookup"><span data-stu-id="45deb-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-259">Según la Regla n.° 2, Q1 y Q2 son dos ofertas de la misma oportunidad, por lo que ambas pueden estimar los mismos componentes de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="45deb-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="45deb-260">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-261">T2</span><span class="sxs-lookup"><span data-stu-id="45deb-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-262">QL1 en Q2</span><span class="sxs-lookup"><span data-stu-id="45deb-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-263">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-264">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-265">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-266">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-266">Yes</span></span> </p>
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
<span data-ttu-id="45deb-267">O1</span><span class="sxs-lookup"><span data-stu-id="45deb-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-268">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-269">QL1</span><span class="sxs-lookup"><span data-stu-id="45deb-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-270">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-271">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-272">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-273">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="45deb-274">Válido</span><span class="sxs-lookup"><span data-stu-id="45deb-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45deb-275">Según la Regla n.° 3, Q1 y Q2 son dos ofertas de diferentes oportunidades, por lo que no pueden estimar los mismos componentes del mismo proyecto.</span><span class="sxs-lookup"><span data-stu-id="45deb-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="45deb-276">O2</span><span class="sxs-lookup"><span data-stu-id="45deb-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="45deb-277">T1</span><span class="sxs-lookup"><span data-stu-id="45deb-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-278">QL1</span><span class="sxs-lookup"><span data-stu-id="45deb-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-279">P1</span><span class="sxs-lookup"><span data-stu-id="45deb-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-280">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="45deb-281">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="45deb-282">Sí</span><span class="sxs-lookup"><span data-stu-id="45deb-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="45deb-283">No válido</span><span class="sxs-lookup"><span data-stu-id="45deb-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

