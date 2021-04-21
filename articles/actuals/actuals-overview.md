---
title: Datos reales
description: Este tema proporciona información sobre cómo trabajar con datos reales en Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852565"
---
# <a name="actuals"></a><span data-ttu-id="1a1c1-103">Datos reales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-103">Actuals</span></span> 

<span data-ttu-id="1a1c1-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="1a1c1-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a1c1-105">Los datos reales representan el progreso financiero y de la programación revisado y aprobado en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="1a1c1-106">Se crean como resultado de la aprobación del plazo, gastos, movimientos de uso de material y movimientos de diario y facturas.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="1a1c1-107">Envío de líneas de diario y tiempo</span><span class="sxs-lookup"><span data-stu-id="1a1c1-107">Journal lines and time submission</span></span>

<span data-ttu-id="1a1c1-108">Para obtener más información sobre movimientos de tiempo, consulte [Resumen de movimientos de tiempo](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1a1c1-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1a1c1-109">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-109">Time and materials</span></span>

<span data-ttu-id="1a1c1-110">Cuando una entrada de tiempo que se envía está vinculada a un proyecto asignado a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1a1c1-111">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="1a1c1-111">Fixed price</span></span>

<span data-ttu-id="1a1c1-112">Cuando se envía una entrada de tiempo vinculada a un proyecto que está asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1a1c1-113">Precios predeterminados</span><span class="sxs-lookup"><span data-stu-id="1a1c1-113">Default pricing</span></span>

<span data-ttu-id="1a1c1-114">La lógica para crear precios predeterminados se encuentra en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="1a1c1-115">Los valores de campo de la entrada de tiempo se copian a la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="1a1c1-116">Estos valores incluyen la fecha de la transacción, la línea de contrato a la que está asignado el proyecto y el resultado de la divisa en la lista de precios correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="1a1c1-117">Los campos que afectan a los precios predeterminados, como, por ejemplo, **Rol** y **Unidad de dotación de recursos**, se utilizan para determinar el precio adecuado en la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1a1c1-118">Puede agregar un campo personalizado en la entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="1a1c1-119">Si desea que el valor del campo se propague a los valores reales, cree el campo en las tablas **Datos reales** y **Línea de diario**.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1a1c1-120">Utilice código personalizado para propagar el valor del campo seleccionado desde Entrada de tiempo a Datos reales a través de la línea del diario utilizando los orígenes de la transacción.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1a1c1-121">Para obtener más información sobre los orígenes de las transacciones y las conexiones, consulte [Vinculación de datos reales a los registros originales](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1a1c1-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="1a1c1-122">Envío de líneas de diario y gastos básicos</span><span class="sxs-lookup"><span data-stu-id="1a1c1-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="1a1c1-123">Para obtener más información sobre movimientos de gastos, consulte [Resumen de gastos](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1a1c1-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1a1c1-124">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-124">Time and materials</span></span>

<span data-ttu-id="1a1c1-125">Cuando una entrada de gasto básico enviada está vinculada a un proyecto asignado a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1a1c1-126">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="1a1c1-126">Fixed price</span></span>

<span data-ttu-id="1a1c1-127">Cuando una entrada de gastos básicos enviada se vincula a un proyecto que está asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1a1c1-128">Precios predeterminados</span><span class="sxs-lookup"><span data-stu-id="1a1c1-128">Default pricing</span></span>

<span data-ttu-id="1a1c1-129">La lógica para introducir precios predeterminados para gastos se basa en la categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="1a1c1-130">La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1a1c1-131">Los campos que afectan a los precios predeterminados, como, por ejemplo, **Categoría de transacción** y **Unidad**, se utilizan para determinar el precio adecuado en la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1a1c1-132">Sin embargo, esto solo funciona cuando el método de fijación de precios en la lista de precios es **Precio por unidad**.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="1a1c1-133">Si el método de fijación de precios es **De coste** o **Incremento por encima del coste**, el precio indicado cuando se crea la entrada de gastos se usa para el coste y el precio en la línea del diario de ventas se calcula según el método de fijación de precios.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="1a1c1-134">Puede agregar un campo personalizado en la entrada de gastos.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="1a1c1-135">Si desea que el valor del campo se propague a los valores reales, cree el campo en las tablas **Datos reales** y **Línea de diario**.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1a1c1-136">Utilice código personalizado para propagar el valor del campo seleccionado desde Entrada de tiempo a Datos reales a través de la línea del diario utilizando los orígenes de la transacción.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1a1c1-137">Para obtener más información sobre los orígenes de las transacciones y las conexiones, consulte [Vinculación de datos reales a los registros originales](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1a1c1-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="1a1c1-138">Envío de registro de líneas del diario y uso de material</span><span class="sxs-lookup"><span data-stu-id="1a1c1-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="1a1c1-139">Para obtener más información sobre la entrada de gasto, consulte [ Registro de uso de material](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="1a1c1-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1a1c1-140">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-140">Time and materials</span></span>

<span data-ttu-id="1a1c1-141">Cuando una entrada de registro de uso de material enviada se vincula a un proyecto que se asigna a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1a1c1-142">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="1a1c1-142">Fixed price</span></span>

<span data-ttu-id="1a1c1-143">Cuando una entrada de registro de uso de material se vincula a un proyecto que está asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1a1c1-144">Precios predeterminados</span><span class="sxs-lookup"><span data-stu-id="1a1c1-144">Default pricing</span></span>

<span data-ttu-id="1a1c1-145">La lógica para indicar precios predeterminados para el material se basa en la combinación de productos y unidades.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="1a1c1-146">La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1a1c1-147">Los campos que afectan a los precios predeterminados, como, por ejemplo, **Id. del producto** y **Unidad**, se utilizan para determinar el precio adecuado en la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1a1c1-148">Sin embargo, esto solo funciona para productos de catálogo.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-148">However, this only works for catalog products.</span></span> <span data-ttu-id="1a1c1-149">Para los productos de escritura, el precio indicado cuando se crea la entrada del registro de uso de material se usa para el coste y el precio de venta en las líneas del diario.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="1a1c1-150">Puede agregar un campo personalizado en la entrada **Registro de uso de materiales**.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="1a1c1-151">Si desea que el valor del campo se propague a los valores reales, cree el campo en las tablas **Datos reales** y **Línea de diario**.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1a1c1-152">Utilice código personalizado para propagar el valor del campo seleccionado desde Entrada de tiempo a Datos reales a través de la línea del diario utilizando los orígenes de la transacción.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1a1c1-153">Para obtener más información sobre los orígenes de las transacciones y las conexiones, consulte [Vinculación de datos reales a los registros originales](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1a1c1-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="1a1c1-154">Utilizar diarios de movimientos para registrar costes</span><span class="sxs-lookup"><span data-stu-id="1a1c1-154">Use entry journals to record costs</span></span>

<span data-ttu-id="1a1c1-155">Puede usar diarios de movimientos para registrar costes o ingresos en materiales, precios, tiempo, gastos o clases de transacciones de impuestos.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="1a1c1-156">Los diarios se pueden usar para los siguientes propósitos:</span><span class="sxs-lookup"><span data-stu-id="1a1c1-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="1a1c1-157">Mueva datos reales de transacciones de otro sistema a Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="1a1c1-158">Registrar cotes que ocurrieron en otro sistema.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="1a1c1-159">Estos costes pueden incluir costes de adquisición o subcontratación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a1c1-160">La aplicación no valida el tipo de línea del diario ni el precio relacionado que se introduce en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="1a1c1-161">Por lo tanto, solo un usuario que sea plenamente consciente del impacto contable que tienen los datos reales en el proyecto debe utilizar los diarios de movimientos para crear los datos reales.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="1a1c1-162">Debido al impacto de este tipo de diario, debe elegir cuidadosamente quién tiene acceso a crear diarios de movimientos.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="1a1c1-163">Registrar datos reales basados en eventos de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-163">Record actuals based on project events</span></span>

<span data-ttu-id="1a1c1-164">Project Operations registra las transacciones financieras que se producen durante un proyecto.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="1a1c1-165">Estas transacciones se registran como datos reales.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="1a1c1-166">Las siguientes tablas muestran los diferentes tipos de datos reales que se crean dependiendo de si el proyecto es un proyecto de tiempo y materiales o de precio fijo, de si se encuentra en fase de preventas o de si se trata de un proyecto interno.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="1a1c1-167">El recurso pertenece a la misma unidad organizativa que la unidad de contratación del proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1a1c1-168">Evento</span><span class="sxs-lookup"><span data-stu-id="1a1c1-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1a1c1-169">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="1a1c1-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1a1c1-170">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="1a1c1-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1a1c1-171">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="1a1c1-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1a1c1-172">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1a1c1-173">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="1a1c1-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1a1c1-174">Datos reales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-174">Actuals</span></span></th>
<th><span data-ttu-id="1a1c1-175">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="1a1c1-175">Transaction currency</span></span></th>
<th><span data-ttu-id="1a1c1-176">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="1a1c1-176">Fixed price</span></span></th>
<th><span data-ttu-id="1a1c1-177">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="1a1c1-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1a1c1-178">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1a1c1-179">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-180">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1a1c1-181">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1a1c1-182">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1a1c1-183">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-183">Cost actual</span></span></td>
<td><span data-ttu-id="1a1c1-184">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-185">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-186">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="1a1c1-187">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-188">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-189">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="1a1c1-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1a1c1-190">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a1c1-191">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1a1c1-192">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-192">Cost actual</span></span></td>
<td><span data-ttu-id="1a1c1-193">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-194">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-195">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-196">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-197">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-198">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="1a1c1-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1a1c1-199">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-200">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="1a1c1-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1a1c1-201">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1a1c1-202">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1a1c1-203">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="1a1c1-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1a1c1-204">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-205">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="1a1c1-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-206">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-207">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-208">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-209">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="1a1c1-209">Billed sales</span></span></td>
<td><span data-ttu-id="1a1c1-210">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a1c1-211">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1a1c1-212">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="1a1c1-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1a1c1-213">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-214">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-215">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-216">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-217">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-218">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="1a1c1-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1a1c1-219">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-220">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="1a1c1-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1a1c1-221">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1a1c1-222">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1a1c1-223">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="1a1c1-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1a1c1-224">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1a1c1-225">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="1a1c1-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1a1c1-226">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="1a1c1-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1a1c1-227">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1a1c1-228">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1a1c1-229">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-230">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="1a1c1-230">Billed sales</span></span></td>
<td><span data-ttu-id="1a1c1-231">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a1c1-232">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1a1c1-233">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="1a1c1-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1a1c1-234">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-235">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="1a1c1-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1a1c1-236">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-237">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="1a1c1-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1a1c1-238">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="1a1c1-239">El recurso pertenece a una unidad organizativa distinta de la unidad de contratación del proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1a1c1-240">Evento</span><span class="sxs-lookup"><span data-stu-id="1a1c1-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1a1c1-241">Proyecto facturable o vendido</span><span class="sxs-lookup"><span data-stu-id="1a1c1-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1a1c1-242">Proyecto en la fase de preventas</span><span class="sxs-lookup"><span data-stu-id="1a1c1-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1a1c1-243">Proyecto interno</span><span class="sxs-lookup"><span data-stu-id="1a1c1-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1a1c1-244">Tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1a1c1-245">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="1a1c1-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1a1c1-246">Datos reales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-246">Actuals</span></span></th>
<th><span data-ttu-id="1a1c1-247">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="1a1c1-247">Transaction currency</span></span></th>
<th><span data-ttu-id="1a1c1-248">Precio fijo</span><span class="sxs-lookup"><span data-stu-id="1a1c1-248">Fixed price</span></span></th>
<th><span data-ttu-id="1a1c1-249">Divisa de la transacción</span><span class="sxs-lookup"><span data-stu-id="1a1c1-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1a1c1-250">Se crea una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1a1c1-251">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-252">Se envía una entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1a1c1-253">No hay actividad en la entidad Datos reales</span><span class="sxs-lookup"><span data-stu-id="1a1c1-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1a1c1-254">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1a1c1-255">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-255">Cost actual</span></span></td>
<td><span data-ttu-id="1a1c1-256">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1a1c1-257">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1a1c1-258">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1a1c1-259">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1a1c1-260">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-261">Dato real de ventas sin facturar: imputable</span><span class="sxs-lookup"><span data-stu-id="1a1c1-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1a1c1-262">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-263">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="1a1c1-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1a1c1-264">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="1a1c1-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-265">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="1a1c1-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1a1c1-266">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1a1c1-267">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1a1c1-268">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-268">Cost actual</span></span></td>
<td><span data-ttu-id="1a1c1-269">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1a1c1-270">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1a1c1-271">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1a1c1-272">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1a1c1-273">Coste real</span><span class="sxs-lookup"><span data-stu-id="1a1c1-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-274">Coste de unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="1a1c1-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1a1c1-275">Divisa de la unidad de dotación de recursos</span><span class="sxs-lookup"><span data-stu-id="1a1c1-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-276">Ventas entre organizaciones</span><span class="sxs-lookup"><span data-stu-id="1a1c1-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1a1c1-277">Divisa de la unidad de contratación</span><span class="sxs-lookup"><span data-stu-id="1a1c1-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-278">Dato real de ventas sin facturar: imputable por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="1a1c1-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1a1c1-279">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-280">Dato real de ventas sin facturar: no imputable por la diferencia</span><span class="sxs-lookup"><span data-stu-id="1a1c1-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1a1c1-281">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1a1c1-282">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1a1c1-283">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="1a1c1-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1a1c1-284">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-285">Ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="1a1c1-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-286">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-287">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1a1c1-288">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-289">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="1a1c1-289">Billed sales</span></span></td>
<td><span data-ttu-id="1a1c1-290">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a1c1-291">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1a1c1-292">Inversión de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="1a1c1-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1a1c1-293">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-294">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-295">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-296">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1a1c1-297">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-298">Ventas facturadas: imputables por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="1a1c1-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1a1c1-299">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-300">Ventas facturadas: no imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="1a1c1-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1a1c1-301">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1a1c1-302">Se corrige una factura para aumentar la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1a1c1-303">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="1a1c1-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1a1c1-304">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1a1c1-305">Inversión de ventas facturadas para hito</span><span class="sxs-lookup"><span data-stu-id="1a1c1-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1a1c1-306">Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></span><span class="sxs-lookup"><span data-stu-id="1a1c1-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1a1c1-307">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1a1c1-308">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1a1c1-309">No disponible</span><span class="sxs-lookup"><span data-stu-id="1a1c1-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-310">Ventas facturadas</span><span class="sxs-lookup"><span data-stu-id="1a1c1-310">Billed sales</span></span></td>
<td><span data-ttu-id="1a1c1-311">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a1c1-312">Se corrige una factura para disminuir la cantidad imputable.</span><span class="sxs-lookup"><span data-stu-id="1a1c1-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1a1c1-313">Ventas facturadas: inversión</span><span class="sxs-lookup"><span data-stu-id="1a1c1-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1a1c1-314">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-315">Ventas facturadas por la nueva cantidad</span><span class="sxs-lookup"><span data-stu-id="1a1c1-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1a1c1-316">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a1c1-317">Ventas sin facturar: imputables por la diferencia</span><span class="sxs-lookup"><span data-stu-id="1a1c1-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1a1c1-318">Divisa de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="1a1c1-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
