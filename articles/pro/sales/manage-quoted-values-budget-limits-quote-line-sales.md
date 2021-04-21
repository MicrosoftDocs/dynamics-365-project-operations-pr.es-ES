---
title: Información general sobre líneas de ofertas basadas en proyectos
description: Este tema proporciona información sobre el uso de líneas de oferta basadas en proyectos para trabajo de proyecto.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858719"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="2d92b-103">Información general sobre líneas de ofertas basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="2d92b-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="2d92b-104">_**Se aplica a:** Implementación lite: acuerdo para factura proforma, Project Operations para escenarios basados en recursos/no mantenidos_</span><span class="sxs-lookup"><span data-stu-id="2d92b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2d92b-105">Las líneas de oferta basadas en proyectos están diseñadas para ayudar a estimar el trabajo del proyecto en un compromiso.</span><span class="sxs-lookup"><span data-stu-id="2d92b-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="2d92b-106">La estructura de una línea de oferta basada en proyectos se amplía para las estimaciones de proyectos con los siguientes conceptos:</span><span class="sxs-lookup"><span data-stu-id="2d92b-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="2d92b-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="2d92b-107">Billing Method</span></span>
- <span data-ttu-id="2d92b-108">Asignación de proyectos y tareas</span><span class="sxs-lookup"><span data-stu-id="2d92b-108">Project and Task Mapping</span></span>
- <span data-ttu-id="2d92b-109">Clases de transacciones incluidas</span><span class="sxs-lookup"><span data-stu-id="2d92b-109">Included Transaction classes</span></span>
- <span data-ttu-id="2d92b-110">Límite a no exceder</span><span class="sxs-lookup"><span data-stu-id="2d92b-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="2d92b-111">Configuración de imputabilidad</span><span class="sxs-lookup"><span data-stu-id="2d92b-111">Chargeability setup</span></span>
- <span data-ttu-id="2d92b-112">Estimación utilizando los detalles de la línea de oferta</span><span class="sxs-lookup"><span data-stu-id="2d92b-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="2d92b-113">Clientes de línea de oferta</span><span class="sxs-lookup"><span data-stu-id="2d92b-113">Quote line Customers</span></span>

<span data-ttu-id="2d92b-114">La siguiente tabla proporciona información sobre los campos de la pestaña **General** de la línea de oferta basada en proyecto.</span><span class="sxs-lookup"><span data-stu-id="2d92b-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="2d92b-115">Estos campos ayudan a establecer la base para una estimación detallada y desde cero para el trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="2d92b-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="2d92b-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="2d92b-116">**Field**</span></span> | <span data-ttu-id="2d92b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d92b-117">**Description**</span></span> | <span data-ttu-id="2d92b-118">**Impacto posterior**</span><span class="sxs-lookup"><span data-stu-id="2d92b-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2d92b-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="2d92b-119">Name</span></span> | <span data-ttu-id="2d92b-120">El nombre de la línea de cotización que le ayuda a identificar el componente discreto de la cotización que se está estimando.</span><span class="sxs-lookup"><span data-stu-id="2d92b-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="2d92b-121">Se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-122">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="2d92b-122">Billing Method</span></span> | <span data-ttu-id="2d92b-123">En una oferta creada a partir de una oportunidad, este valor se copia del campo correspondiente en la línea de oportunidad.</span><span class="sxs-lookup"><span data-stu-id="2d92b-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="2d92b-124">Este campo incluye los dos principales modelos de contratación soportados por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="2d92b-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="2d92b-125">- Precio fijo</span><span class="sxs-lookup"><span data-stu-id="2d92b-125">- Fixed price</span></span></br><span data-ttu-id="2d92b-126">- Tiempo y material.</span><span class="sxs-lookup"><span data-stu-id="2d92b-126">- Time and material.</span></span>| <span data-ttu-id="2d92b-127">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-128">Project</span><span class="sxs-lookup"><span data-stu-id="2d92b-128">Project</span></span> | <span data-ttu-id="2d92b-129">Utilice este campo opcional para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso.</span><span class="sxs-lookup"><span data-stu-id="2d92b-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="2d92b-130">Cuando un proyecto se asigna a una línea de oferta, ayuda a configurar las tareas facturables y también a traer una estimación basada en el proyecto a la línea de oferta como detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="2d92b-131">Cuando un proyecto no está asignado a una línea de oferta basada en proyecto, la estimación debe crearse manualmente creando cada detalle de línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="2d92b-132">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="2d92b-133">Tareas incluidas</span><span class="sxs-lookup"><span data-stu-id="2d92b-133">Included Tasks</span></span> | <span data-ttu-id="2d92b-134">Indica si esta línea de oferta se utiliza para todas o algunas de las tareas del proyecto para el proyecto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2d92b-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="2d92b-135">Este campo tiene los siguientes posibles valores:</span><span class="sxs-lookup"><span data-stu-id="2d92b-135">This field has the following possible values:</span></span></br><span data-ttu-id="2d92b-136">- Todas las tareas de proyecto</span><span class="sxs-lookup"><span data-stu-id="2d92b-136">- All project tasks</span></span></br><span data-ttu-id="2d92b-137">- Solo tareas de proyecto seleccionadas</span><span class="sxs-lookup"><span data-stu-id="2d92b-137">- Selected project tasks only</span></span></br><span data-ttu-id="2d92b-138">Un valor en blanco en este campo es equivalente a la opción **Todas las tareas del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="2d92b-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="2d92b-139">Cuando se selecciona **Solo tareas de proyecto seleccionadas** en la página del proyecto, la pestaña **Configuración de facturación de tareas** le permite seleccionar tareas específicas para asociarlas a esta línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="2d92b-140">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-141">Incluir tiempo</span><span class="sxs-lookup"><span data-stu-id="2d92b-141">Include Time</span></span> | <span data-ttu-id="2d92b-142">Un valor **Sí**/**No** indica si las transacciones de tiempo o los costes de mano de obra en el proyecto seleccionado se incluirán en la estimación de esta línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2d92b-143">Un valor **No** indica que las transacciones de tiempo o los costes laborales no se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2d92b-144">Un valor **Sí** indica que las transacciones de tiempo o los costes laborales se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2d92b-145">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-146">Incluir gasto</span><span class="sxs-lookup"><span data-stu-id="2d92b-146">Include Expense</span></span> | <span data-ttu-id="2d92b-147">Un valor **Sí**/**No** indica si los costes de gastos en el proyecto seleccionado se incluirán en la estimación de esta línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2d92b-148">Un valor **No** indica que el coste de gastos no se incluirá en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2d92b-149">Un valor **Sí** indica que el coste de gastos se incluirá en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2d92b-150">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-151">Incluir material</span><span class="sxs-lookup"><span data-stu-id="2d92b-151">Include Material</span></span> | <span data-ttu-id="2d92b-152">Un valor **Sí**/**No** indica si los costes de material en el proyecto seleccionado se incluirán en la estimación de esta línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2d92b-153">Un valor **No** indica que los costes por material no se incluirán en la estimación de esta línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2d92b-154">Un valor **Sí** indica que los costes por material se incluirán en la estimación de esta línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2d92b-155">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-156">Incluir tarifa</span><span class="sxs-lookup"><span data-stu-id="2d92b-156">Include Fee</span></span> | <span data-ttu-id="2d92b-157">Un valor **Sí**/**No** indica si las tarifas en el proyecto seleccionado se incluirán en la estimación de esta línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2d92b-158">Un valor **No** indica que las tarifas no se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2d92b-159">Un valor **No** indica que las tarifas se incluirán en la estimación de esta línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2d92b-160">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-161">Importe de la oferta</span><span class="sxs-lookup"><span data-stu-id="2d92b-161">Quoted Amount</span></span> | <span data-ttu-id="2d92b-162">Esta es la cantidad que se cotizará al cliente por todo el trabajo previsto en esta línea de cotización basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="2d92b-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="2d92b-163">En una oferta creada a partir de una oportunidad, este valor se copia del campo **Presupuesto del cliente** correspondiente en la línea de oportunidad.</span><span class="sxs-lookup"><span data-stu-id="2d92b-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="2d92b-164">Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="2d92b-165">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-166">Impuesto estimado</span><span class="sxs-lookup"><span data-stu-id="2d92b-166">Estimated Tax</span></span> | <span data-ttu-id="2d92b-167">Este es un campo editable para que el usuario agregue el importe del impuesto estimado en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="2d92b-168">Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los impuestos de los detalles de la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="2d92b-169">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-170">Importe ofertado después de impuestos</span><span class="sxs-lookup"><span data-stu-id="2d92b-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="2d92b-171">Este campo es el importe de la línea de oferta después de impuestos y es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2d92b-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="2d92b-172">La cantidad de este campo se calcula como *Importe ofertado + Impuestos*.</span><span class="sxs-lookup"><span data-stu-id="2d92b-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="2d92b-173">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-174">Límite de No exceder</span><span class="sxs-lookup"><span data-stu-id="2d92b-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="2d92b-175">Este campo es editable y solo está disponible en líneas de oferta basadas en proyectos que tienen un método de facturación **Tiempo y material**.</span><span class="sxs-lookup"><span data-stu-id="2d92b-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="2d92b-176">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2d92b-177">Presupuesto del cliente</span><span class="sxs-lookup"><span data-stu-id="2d92b-177">Customer Budget</span></span> | <span data-ttu-id="2d92b-178">Este campo es editable y se copia a partir del campo correspondiente de la línea de oportunidad si la oferta se creo a partir de una oportunidad.</span><span class="sxs-lookup"><span data-stu-id="2d92b-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="2d92b-179">Este valor se copia en la línea de contrato del proyecto que se crea a partir de esta línea de cotización cuando aceptan la cotización.</span><span class="sxs-lookup"><span data-stu-id="2d92b-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="2d92b-180">Reglas de validación para campos en la pestaña General de líneas de oferta basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="2d92b-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="2d92b-181">**Regla 1**: si el campo **Tareas incluidas** está en blanco, o si está configurado en **Todas las tareas del proyecto**, se incluye un proyecto en la línea de oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="2d92b-182">**Regla 2**: si el campo **Tareas incluidas** está en blanco, o si está configurado en **Todas las tareas del proyecto**, un proyecto y una determinada clase de transacción solo se pueden incluir en una línea de oferta basada en proyectos de una oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="2d92b-183">**Regla 3**: si el campo **Tareas incluidas** está configurado en **Solo tareas del proyecto seleccionadas**, un proyecto y una determinada clase de transacción se pueden incluir en varias líneas de oferta basadas en proyectos de una oferta.</span><span class="sxs-lookup"><span data-stu-id="2d92b-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="2d92b-184">**Regla 4**: si una oportunidad tiene varias ofertas, puede haber líneas de oferta de ofertas diferentes que hagan referencia al mismo proyecto e incluyan la misma clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="2d92b-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="2d92b-185">**Regla 5**: si las ofertas no pertenecen a la misma oportunidad, no pueden incluir el mismo proyecto y clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="2d92b-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="2d92b-186">
                    <strong>Oportunidad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="2d92b-187">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="2d92b-188">
                    <strong>Línea de oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="2d92b-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="2d92b-190">
                    <strong>Tareas incluidas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="2d92b-191">
                    <strong>Incluir tiempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="2d92b-192">
                    <strong>Incluir gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="2d92b-193">
                    <strong>Incluir material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="2d92b-194">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="2d92b-195">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="2d92b-196">
                    <strong>Válido/no válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="2d92b-197">
                    <strong>Razón</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d92b-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-198">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-199">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-200">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-201">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-202">En blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-203">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-204">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-205">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-206">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-207">No válido</span><span class="sxs-lookup"><span data-stu-id="2d92b-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-208">Infracción de la regla n.º 2.</span><span class="sxs-lookup"><span data-stu-id="2d92b-208">Violation of Rule #2.</span></span> <span data-ttu-id="2d92b-209">El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en las líneas de oferta QL1 y QL2</span><span class="sxs-lookup"><span data-stu-id="2d92b-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-210">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-211">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-212">QL2</span><span class="sxs-lookup"><span data-stu-id="2d92b-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-213">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-214">En blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-215">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-216">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-217">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-218">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-219">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-220">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-221">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-222">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-223">En blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-224">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-225">No</span><span class="sxs-lookup"><span data-stu-id="2d92b-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-226">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-227">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-228">No válido</span><span class="sxs-lookup"><span data-stu-id="2d92b-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-229">Infracción de la regla n.º 2.</span><span class="sxs-lookup"><span data-stu-id="2d92b-229">Violation of Rule #2.</span></span> <span data-ttu-id="2d92b-230">El tiempo, el material y las tarifas del proyecto P1 se incluyen en las líneas de oferta QL1 y QL2</span><span class="sxs-lookup"><span data-stu-id="2d92b-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-231">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-232">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-233">QL2</span><span class="sxs-lookup"><span data-stu-id="2d92b-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-234">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-235">En blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-236">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-237">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-238">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-239">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-240">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-241">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-242">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-243">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-244">En blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-245">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-246">No</span><span class="sxs-lookup"><span data-stu-id="2d92b-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-247">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-248">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-249">Válido</span><span class="sxs-lookup"><span data-stu-id="2d92b-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-250">El tiempo, el material y las tarifas del proyecto P1 se incluyen en QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="2d92b-251">El gasto del proyecto P1 se incluyen en QL2</span><span class="sxs-lookup"><span data-stu-id="2d92b-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="2d92b-252">No hay superposición en lo que se incluye en cada línea de cotización y, por lo tanto, es válido.</span><span class="sxs-lookup"><span data-stu-id="2d92b-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-253">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-254">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-255">QL2</span><span class="sxs-lookup"><span data-stu-id="2d92b-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-256">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-257">En blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-258">No</span><span class="sxs-lookup"><span data-stu-id="2d92b-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-259">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-260">No</span><span class="sxs-lookup"><span data-stu-id="2d92b-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-261">No</span><span class="sxs-lookup"><span data-stu-id="2d92b-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-262">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-263">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-264">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-265">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-266">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="2d92b-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-267">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-268">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-269">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-270">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-271">No válido</span><span class="sxs-lookup"><span data-stu-id="2d92b-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-272">Infracción de la regla n.º 2</span><span class="sxs-lookup"><span data-stu-id="2d92b-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="2d92b-273">Q1 incluye tiempo, material, gastos y tarifas en un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="2d92b-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="2d92b-274">QL2 incluye tiempo, gastos y tarifas para todo el proyecto P1 y, por lo tanto, se superpone con lo que se incluye en Q1.</span><span class="sxs-lookup"><span data-stu-id="2d92b-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-275">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-276">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-277">QL2</span><span class="sxs-lookup"><span data-stu-id="2d92b-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-278">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-279">En blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-280">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-281">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-282">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-283">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-284">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-285">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-286">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-287">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-288">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="2d92b-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-289">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-290">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-291">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-292">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-293">Válido</span><span class="sxs-lookup"><span data-stu-id="2d92b-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-294">Según la regla n.° 3</span><span class="sxs-lookup"><span data-stu-id="2d92b-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="2d92b-295">Q1 incluye tiempo, material, gastos y tarifas en un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="2d92b-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2d92b-296">QL2 incluye tiempo, material, gastos y tarifas para un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="2d92b-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2d92b-297">La única validación adicional se refiere al subconjunto de tareas en QL1 que es diferente del subconjunto de tareas en QL2 para garantizar que no haya superposiciones.</span><span class="sxs-lookup"><span data-stu-id="2d92b-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="2d92b-298">Esto lo hace el sistema cuando se asocian tareas.</span><span class="sxs-lookup"><span data-stu-id="2d92b-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-299">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-300">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-301">QL2</span><span class="sxs-lookup"><span data-stu-id="2d92b-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-302">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-303">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="2d92b-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-304">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-305">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-306">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-307">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-308">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-309">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-310">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-311">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-312">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-313">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-314">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-315">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-316">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-317">Válido</span><span class="sxs-lookup"><span data-stu-id="2d92b-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-318">Según la Regla n.° 5, Q1 y Q2 son dos cotizaciones en la misma oportunidad, por lo que ambas pueden estimar los mismos componentes de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="2d92b-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-319">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-320">T2</span><span class="sxs-lookup"><span data-stu-id="2d92b-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-321">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-322">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-323">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-324">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-325">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-326">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-327">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-328">O1</span><span class="sxs-lookup"><span data-stu-id="2d92b-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-329">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-330">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-331">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-332">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-333">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-334">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-335">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-336">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-337">No válido</span><span class="sxs-lookup"><span data-stu-id="2d92b-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d92b-338">Según la Regla n.° 4, Q1 y Q2 son dos cotizaciones en diferentes oportunidades, por lo que ambas pueden estimar los mismos componentes de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="2d92b-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2d92b-339">O2</span><span class="sxs-lookup"><span data-stu-id="2d92b-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2d92b-340">T1</span><span class="sxs-lookup"><span data-stu-id="2d92b-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2d92b-341">QL1</span><span class="sxs-lookup"><span data-stu-id="2d92b-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-342">P1</span><span class="sxs-lookup"><span data-stu-id="2d92b-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2d92b-343">Todas las tareas del proyecto o en blanco</span><span class="sxs-lookup"><span data-stu-id="2d92b-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2d92b-344">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2d92b-345">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2d92b-346">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2d92b-347">Sí</span><span class="sxs-lookup"><span data-stu-id="2d92b-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
