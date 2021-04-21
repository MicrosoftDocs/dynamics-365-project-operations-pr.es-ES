---
title: Información general de líneas de contrato basadas en proyectos
description: En este tema se proporciona información sobre el trabajo con líneas de contrato basadas en proyecto.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858179"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="bba35-103">Información general de líneas de contrato basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="bba35-103">Project-based contract lines overview</span></span>

<span data-ttu-id="bba35-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="bba35-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bba35-105">Las líneas de contrato basadas en proyectos en Dynamics 365 Project Operations están diseñadas para contener los acuerdos de estimación y facturación para componentes específicos del trabajo del proyecto en un compromiso.</span><span class="sxs-lookup"><span data-stu-id="bba35-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="bba35-106">La estructura de una línea de contrato basada en proyectos se amplía para estimaciones de proyectos y escenarios de facturación con los siguientes conceptos:</span><span class="sxs-lookup"><span data-stu-id="bba35-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="bba35-107">Método de facturación</span><span class="sxs-lookup"><span data-stu-id="bba35-107">Billing method</span></span>
- <span data-ttu-id="bba35-108">Asignación de proyectos y tareas</span><span class="sxs-lookup"><span data-stu-id="bba35-108">Project and task mapping</span></span>
- <span data-ttu-id="bba35-109">Clases de transacciones incluidas</span><span class="sxs-lookup"><span data-stu-id="bba35-109">Included transaction classes</span></span>
- <span data-ttu-id="bba35-110">Límite a no exceder</span><span class="sxs-lookup"><span data-stu-id="bba35-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="bba35-111">Configuración de imputabilidad</span><span class="sxs-lookup"><span data-stu-id="bba35-111">Chargeability setup</span></span>
- <span data-ttu-id="bba35-112">Estimaciones utilizando detalles de línea de contrato</span><span class="sxs-lookup"><span data-stu-id="bba35-112">Estimates using contract line details</span></span>
- <span data-ttu-id="bba35-113">Clientes de líneas de contrato</span><span class="sxs-lookup"><span data-stu-id="bba35-113">Contract line customers</span></span>

<span data-ttu-id="bba35-114">La siguiente tabla incluye los campos en la pestaña **General** de líneas de contrato basadas en proyectos que ayudan a establecer la base para un presupuesto detallado y desde cero y arreglos de facturación para el trabajo basado en proyectos.</span><span class="sxs-lookup"><span data-stu-id="bba35-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="bba35-115">Campo</span><span class="sxs-lookup"><span data-stu-id="bba35-115">Field</span></span> | <span data-ttu-id="bba35-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bba35-116">Description</span></span> | <span data-ttu-id="bba35-117">Impacto posterior</span><span class="sxs-lookup"><span data-stu-id="bba35-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bba35-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="bba35-118">**Name**</span></span> | <span data-ttu-id="bba35-119">Nombre de la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-119">Name of the contract line.</span></span> <span data-ttu-id="bba35-120">Esto identifica el componente discreto del contrato que se está estimando.</span><span class="sxs-lookup"><span data-stu-id="bba35-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="bba35-121">Para un contrato de proyecto creado a partir de una cotización, este valor se copia de un valor correspondiente de la línea de cotización basada en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="bba35-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="bba35-122">El nombre que se copia en la línea de factura del proyecto que se crea a partir de esta línea de contrato cuando se crea la factura.</span><span class="sxs-lookup"><span data-stu-id="bba35-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="bba35-123">**Método de facturación**</span><span class="sxs-lookup"><span data-stu-id="bba35-123">**Billing Method**</span></span> | <span data-ttu-id="bba35-124">En un contrato de proyecto creado a partir de una cotización, este valor se copia de un campo correspondiente de la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="bba35-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="bba35-125">Este es un conjunto de opciones que representa los dos principales modelos de contratación soportados por Project Operations:</span><span class="sxs-lookup"><span data-stu-id="bba35-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="bba35-126">- **Precio fijo**</span><span class="sxs-lookup"><span data-stu-id="bba35-126">- **Fixed Price**</span></span></br><span data-ttu-id="bba35-127">- **Tiempo y material**</span><span class="sxs-lookup"><span data-stu-id="bba35-127">- **Time and Material**</span></span> | <span data-ttu-id="bba35-128">Según el método de facturación de la línea de contrato referenciada, se procesará la transacción real.</span><span class="sxs-lookup"><span data-stu-id="bba35-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="bba35-129">Si la línea de contrato a la que hace referencia el real tiene un método de facturación de tiempo y material, se crean un costo y registros reales de ventas no facturadas.</span><span class="sxs-lookup"><span data-stu-id="bba35-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="bba35-130">Si la línea de contrato a la que hace referencia el real tiene un método de facturación de precio fijo, solo se crea un costo real.</span><span class="sxs-lookup"><span data-stu-id="bba35-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="bba35-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="bba35-131">**Project**</span></span> | <span data-ttu-id="bba35-132">Utilice este campo para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso.</span><span class="sxs-lookup"><span data-stu-id="bba35-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="bba35-133">Este valor se utilizará junto con **Tareas incluidas** y **Clases de transacciones incluidas** para resolver la referencia de la línea del contrato en un registro de línea valor real o estimado.</span><span class="sxs-lookup"><span data-stu-id="bba35-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="bba35-134">**Tareas incluidas**</span><span class="sxs-lookup"><span data-stu-id="bba35-134">**Included Tasks**</span></span> | <span data-ttu-id="bba35-135">Indica si esta línea de contrato incluye todas las tareas del proyecto para el proyecto seleccionado o solo un subconjunto de las tareas.</span><span class="sxs-lookup"><span data-stu-id="bba35-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="bba35-136">Es un conjunto de opciones que puede tener los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="bba35-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="bba35-137">- **Todas las tareas de proyecto**</span><span class="sxs-lookup"><span data-stu-id="bba35-137">- **All Project Tasks**</span></span></br><span data-ttu-id="bba35-138">- **Solo tareas de proyecto seleccionadas**.</span><span class="sxs-lookup"><span data-stu-id="bba35-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="bba35-139">Un valor en blanco en este campo equivale a seleccionar **Todas las tareas del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="bba35-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="bba35-140">Si **Solo tareas seleccionadas** está seleccionado, puede seleccionar tareas específicas y asociarlas a esta línea de contrato en la pestaña **Configuración de facturación de tareas** en la página **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="bba35-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="bba35-141">El valor se utiliza junto con las clases **Proyecto** y **Transacción incluida** para resolver la referencia de línea de contrato en un registro de línea real o estimado.</span><span class="sxs-lookup"><span data-stu-id="bba35-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="bba35-142">**Incluir tiempo**</span><span class="sxs-lookup"><span data-stu-id="bba35-142">**Include Time**</span></span> | <span data-ttu-id="bba35-143">Un valor **Sí**/**No** indica si las transacciones de tiempo o los costes de mano de obra en el proyecto seleccionado se incluirán en esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="bba35-144">El valor **No** indica que las transacciones de tiempo o el coste de mano de obra no se incluirán en esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="bba35-145">El valor **Sí** indica que lo harán.</span><span class="sxs-lookup"><span data-stu-id="bba35-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="bba35-146">Este valor se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado.</span><span class="sxs-lookup"><span data-stu-id="bba35-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="bba35-147">**Incluir gasto**</span><span class="sxs-lookup"><span data-stu-id="bba35-147">**Include Expense**</span></span> | <span data-ttu-id="bba35-148">Un valor **Sí**/**No** indica si los costes por gastos en el proyecto seleccionado se incluirán en esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="bba35-149">El valor **No** indica que el coste de gastos no se incluirá en esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="bba35-150">El valor **Sí** indica que lo hará.</span><span class="sxs-lookup"><span data-stu-id="bba35-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="bba35-151">Este valor se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado.</span><span class="sxs-lookup"><span data-stu-id="bba35-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="bba35-152">**Incluir materiales**</span><span class="sxs-lookup"><span data-stu-id="bba35-152">**Include Materials**</span></span> | <span data-ttu-id="bba35-153">Un valor **Sí**/**No** indica si los costes por material en el proyecto seleccionado se incluirán en esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="bba35-154">Un valor **No** indica que los costes por material no se incluirán en esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="bba35-155">El valor **Sí** indica que lo hará.</span><span class="sxs-lookup"><span data-stu-id="bba35-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="bba35-156">Este valor se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado.</span><span class="sxs-lookup"><span data-stu-id="bba35-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="bba35-157">**Incluir tarifa**</span><span class="sxs-lookup"><span data-stu-id="bba35-157">**Include Fee**</span></span> | <span data-ttu-id="bba35-158">Un valor **Sí**/**No** indica si las tarifas en el proyecto seleccionado se incluirán en esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="bba35-159">El valor **No** indica que los honorarios no se incluirán en esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="bba35-160">El valor **Sí** indica que lo harán.</span><span class="sxs-lookup"><span data-stu-id="bba35-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="bba35-161">Este valor se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado.</span><span class="sxs-lookup"><span data-stu-id="bba35-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="bba35-162">**Importe contratado**</span><span class="sxs-lookup"><span data-stu-id="bba35-162">**Contracted Amount**</span></span> | <span data-ttu-id="bba35-163">En una línea de contrato de precio fijo, este importe es el valor acordado que se facturará al cliente por todos los componentes de trabajo asociados con esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="bba35-164">En una línea de contrato de tiempo y material, este importe es un valor estimado de lo que se facturará al cliente por todos los componentes de trabajo asociados con esta línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="bba35-165">En un contrato de proyecto que se crea a partir de una cotización, este valor se copia de un campo correspondiente de la línea de cotización.</span><span class="sxs-lookup"><span data-stu-id="bba35-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="bba35-166">Cuando una línea de contrato basada en proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del monto en los detalles de la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="bba35-167">Cuando la línea del contrato tiene detalles de línea, este valor se puede modificar cambiando los importes en los detalles de la línea.</span><span class="sxs-lookup"><span data-stu-id="bba35-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="bba35-168">En una línea de contrato de precio fijo, este valor se utiliza para generar el monto antes de impuestos sobre los hitos de facturación periódica.</span><span class="sxs-lookup"><span data-stu-id="bba35-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="bba35-169">**Impuesto estimado**</span><span class="sxs-lookup"><span data-stu-id="bba35-169">**Estimated Tax**</span></span> | <span data-ttu-id="bba35-170">El usuario puede editar este campo para ingresar el monto del impuesto estimado en la línea del contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="bba35-171">Cuando una línea de contrato basada en proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del monto de impuestos en los detalles de la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="bba35-172">Cuando la línea del contrato tiene detalles de línea, este valor se puede modificar cambiando los importes de impuestos en los detalles de la línea.</span><span class="sxs-lookup"><span data-stu-id="bba35-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="bba35-173">En una línea de contrato de precio fijo, este valor se utiliza para generar impuestos sobre los hitos de facturación periódica.</span><span class="sxs-lookup"><span data-stu-id="bba35-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="bba35-174">**Importe contratado después de impuestos**</span><span class="sxs-lookup"><span data-stu-id="bba35-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="bba35-175">Importe de la línea de contrato después de impuestos.</span><span class="sxs-lookup"><span data-stu-id="bba35-175">The contract line amount after tax.</span></span> <span data-ttu-id="bba35-176">Este campo es de solo lectura y se calcula como **Importe contratado + Impuestos**.</span><span class="sxs-lookup"><span data-stu-id="bba35-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="bba35-177">En una línea de contrato de precio fijo, este valor se utiliza para generar hitos de facturación periódica.</span><span class="sxs-lookup"><span data-stu-id="bba35-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="bba35-178">**Límite a no exceder**</span><span class="sxs-lookup"><span data-stu-id="bba35-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="bba35-179">El usuario puede editar este campo y solo está disponible en líneas de contrato basadas en proyectos que tienen el método de facturación establecido como tiempo y material.</span><span class="sxs-lookup"><span data-stu-id="bba35-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="bba35-180">El usuario puede editar este campo.</span><span class="sxs-lookup"><span data-stu-id="bba35-180">The user can edit this field.</span></span> <span data-ttu-id="bba35-181">Cuando un valor real de tiempo y material hace referencia a esta línea de contrato por tiempo y material, la cantidad en el real se evalúa contra el límite que no debe excederse en esta línea de contrato después de contabilizar los montos ya gastados y comprometidos.</span><span class="sxs-lookup"><span data-stu-id="bba35-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="bba35-182">Esta evaluación se completa después de contabilizar los montos ya gastados y comprometidos.</span><span class="sxs-lookup"><span data-stu-id="bba35-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="bba35-183">**Presupuesto del cliente**</span><span class="sxs-lookup"><span data-stu-id="bba35-183">**Customer Budget**</span></span> | <span data-ttu-id="bba35-184">Este campo es editable y se copia de un campo correspondiente de la línea de cotización si el contrato se creó a partir de una oferta.</span><span class="sxs-lookup"><span data-stu-id="bba35-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="bba35-185">Este campo solo se utiliza para información y no tiene ningún significado posterior.</span><span class="sxs-lookup"><span data-stu-id="bba35-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="bba35-186">Reglas de validación para las opciones de la pestaña General de las líneas de contrato basadas en proyectos</span><span class="sxs-lookup"><span data-stu-id="bba35-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="bba35-187">Regla 1: si el campo **Tareas incluidas** está en blanco o establecido en **Todas las tareas del proyecto**, todas las tareas del proyecto están incluidas en la línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="bba35-188">Regla 2: cuando el campo **Tareas incluidas** está en blanco o se establece explícitamente en **Todas las tareas del proyecto**, un proyecto y una determinada clase de transacción solo se pueden incluir en una línea de contrato basada en proyecto de un contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="bba35-189">Regla 3: cuando el campo **Tareas incluidas** está en blanco o se establece explícitamente en **Solo las tareas del proyecto seleccionadas**, un proyecto y una determinada clase de transacción se pueden incluir en varias líneas de contrato basadas en proyecto de un contrato.</span><span class="sxs-lookup"><span data-stu-id="bba35-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="bba35-190">
                    <strong>Contrato</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bba35-191">
                    <strong>Línea de contrato</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="bba35-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="bba35-193">
                    <strong>Tareas incluidas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="bba35-194">
                    <strong>Incluir tiempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="bba35-195">
                    <strong>Incluir gasto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="bba35-196">
                    <strong>Incluir materiales</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="bba35-197">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="bba35-198">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="bba35-199">
                    <strong>Válido/no válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="bba35-200">
                    <strong>Razón</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bba35-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-201">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-202">CL1</span><span class="sxs-lookup"><span data-stu-id="bba35-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-203">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-204">En blanco</span><span class="sxs-lookup"><span data-stu-id="bba35-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-205">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-206">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-207">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-208">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-209">No válido</span><span class="sxs-lookup"><span data-stu-id="bba35-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-210">Infracción de la regla n.º 2.</span><span class="sxs-lookup"><span data-stu-id="bba35-210">Violation of Rule #2.</span></span> <span data-ttu-id="bba35-211">El tiempo, los gastos, los materiales y las tarifas del proyecto P1 se incluyen en las líneas de contrato CL1 y CL2.</span><span class="sxs-lookup"><span data-stu-id="bba35-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-212">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-213">CL2</span><span class="sxs-lookup"><span data-stu-id="bba35-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-214">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-215">En blanco</span><span class="sxs-lookup"><span data-stu-id="bba35-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-216">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-217">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-218">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-219">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-220">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-221">CL1</span><span class="sxs-lookup"><span data-stu-id="bba35-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-222">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-223">En blanco</span><span class="sxs-lookup"><span data-stu-id="bba35-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-224">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-225">No</span><span class="sxs-lookup"><span data-stu-id="bba35-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-226">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-227">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-228">No válido</span><span class="sxs-lookup"><span data-stu-id="bba35-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-229">Infracción de la regla n.º 2.</span><span class="sxs-lookup"><span data-stu-id="bba35-229">Violation of Rule #2.</span></span> <span data-ttu-id="bba35-230">El tiempo, los materiales y las tarifas del proyecto P1 se incluyen en las líneas de contrato CL1 y CL2.</span><span class="sxs-lookup"><span data-stu-id="bba35-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-231">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-232">CL2</span><span class="sxs-lookup"><span data-stu-id="bba35-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-233">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-234">En blanco</span><span class="sxs-lookup"><span data-stu-id="bba35-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-235">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-236">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-237">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-238">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-239">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-240">CL1</span><span class="sxs-lookup"><span data-stu-id="bba35-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-241">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-242">En blanco</span><span class="sxs-lookup"><span data-stu-id="bba35-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-243">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-244">No</span><span class="sxs-lookup"><span data-stu-id="bba35-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-245">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-246">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-247">Válido</span><span class="sxs-lookup"><span data-stu-id="bba35-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-248">El tiempo, los materiales y las tarifas del proyecto P1 se incluyen en CL1.</span><span class="sxs-lookup"><span data-stu-id="bba35-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="bba35-249">El gasto del proyecto P1 se incluyen en CL2.</span><span class="sxs-lookup"><span data-stu-id="bba35-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="bba35-250">No hay superposición en lo que se incluye en cada línea del contrato y, por lo tanto, es válido.</span><span class="sxs-lookup"><span data-stu-id="bba35-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-251">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-252">CL2</span><span class="sxs-lookup"><span data-stu-id="bba35-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-253">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-254">En blanco</span><span class="sxs-lookup"><span data-stu-id="bba35-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-255">No</span><span class="sxs-lookup"><span data-stu-id="bba35-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-256">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-257">No</span><span class="sxs-lookup"><span data-stu-id="bba35-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-258">No</span><span class="sxs-lookup"><span data-stu-id="bba35-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-259">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-260">CL1</span><span class="sxs-lookup"><span data-stu-id="bba35-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-261">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-262">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="bba35-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-263">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-264">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-265">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-266">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-267">No válido</span><span class="sxs-lookup"><span data-stu-id="bba35-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-268">Infracción de la regla n.º 2</span><span class="sxs-lookup"><span data-stu-id="bba35-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="bba35-269">C1 incluye tiempo, materiales, gastos y tarifas en un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="bba35-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="bba35-270">CL2 incluye tiempo, materiales, gastos y tarifas para todo el proyecto P1 y, por lo tanto, se superpone con lo que se incluye en C1.</span><span class="sxs-lookup"><span data-stu-id="bba35-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-271">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-272">CL2</span><span class="sxs-lookup"><span data-stu-id="bba35-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-273">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-274">En blanco</span><span class="sxs-lookup"><span data-stu-id="bba35-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-275">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-276">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-277">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-278">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-279">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-280">CL1</span><span class="sxs-lookup"><span data-stu-id="bba35-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-281">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-282">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="bba35-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-283">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-284">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-285">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-286">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-287">Válido</span><span class="sxs-lookup"><span data-stu-id="bba35-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bba35-288">Según la regla n.° 3</span><span class="sxs-lookup"><span data-stu-id="bba35-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="bba35-289">C1 incluye tiempo, gastos, materiales y tarifas en un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="bba35-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="bba35-290">CL2 incluye tiempo, gastos, materiales y tarifas para un subconjunto de tareas en el proyecto P1.</span><span class="sxs-lookup"><span data-stu-id="bba35-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="bba35-291">La única validación adicional se refiere al subconjunto de tareas en CL1 y es diferente del subconjunto de tareas en CL2 para garantizar que no haya superposiciones.</span><span class="sxs-lookup"><span data-stu-id="bba35-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="bba35-292">Esto lo hace el sistema cuando se asocian tareas.</span><span class="sxs-lookup"><span data-stu-id="bba35-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="bba35-293">C1</span><span class="sxs-lookup"><span data-stu-id="bba35-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bba35-294">CL2</span><span class="sxs-lookup"><span data-stu-id="bba35-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-295">P1</span><span class="sxs-lookup"><span data-stu-id="bba35-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="bba35-296">Solo tareas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="bba35-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-297">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bba35-298">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-299">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bba35-300">Sí</span><span class="sxs-lookup"><span data-stu-id="bba35-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
