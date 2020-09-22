---
title: Contratos de proyecto
description: Este tema proporciona ejemplos de los contratos de proyecto que puede crear para varios tipos de proyectos y fuentes de financiación, y cómo puede administrar contratos y facturar a los clientes del proyecto.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756036"
---
# <a name="project-contracts"></a><span data-ttu-id="b4aa9-103">Contratos de proyecto</span><span class="sxs-lookup"><span data-stu-id="b4aa9-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4aa9-104">Este artículo proporciona ejemplos de los contratos de proyecto que puede crear para varios tipos de proyectos y fuentes de financiación, y cómo puede administrar contratos y facturar a los clientes del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="b4aa9-105">El tipo de proyecto que crea para un contrato de proyecto determina el método que se utiliza para facturar a los clientes del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="b4aa9-106">Puede modificar un contrato de proyecto y el proyecto relacionado, pero no puede cambiar el tipo de proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="b4aa9-107">Al usar un contrato de proyecto, puede facturar uno o varios proyectos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="b4aa9-108">El contrato del proyecto también ayuda a garantizar un procedimiento de facturación consistente para cada subproyecto en una estructura de proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="b4aa9-109">Cada proyecto que se facturará debe estar asociado con un contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="b4aa9-110">La configuración para un contrato de proyecto se aplica a todos los proyectos y subproyectos asociados con ese contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="b4aa9-111">Un contrato de proyecto puede especificar una o más fuentes de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="b4aa9-112">Por lo tanto, puede dividir la facturación entre varias entidades financieras, establecer límites de financiación para que no se facture a las fuentes de financiación más de un importe específico y configurar reglas de financiación para cobrar gastos.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="b4aa9-113">Financiación para contratos de proyecto</span><span class="sxs-lookup"><span data-stu-id="b4aa9-113">Funding for project contracts</span></span>
<span data-ttu-id="b4aa9-114">Algunos contratos de proyecto especifican que múltiples partes comparten la responsabilidad de financiar los costes del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="b4aa9-115">Estos son algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-115">Here are some examples:</span></span>

-   <span data-ttu-id="b4aa9-116">Un cliente grande que tiene varias divisiones solicita que la financiación de un proyecto se divida por división.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="b4aa9-117">Su empresa comparte los costos de un gran proyecto con una organización externa.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="b4aa9-118">Un proyecto de carretera está cofinanciado por dos municipios.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="b4aa9-119">Un proyecto para un puente está financiado por una subvención del gobierno y una corporación privada.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="b4aa9-120">En Dynamics 365 Finance, puede dividir la facturación de una sola transacción o un proyecto completo entre varios clientes, subvenciones u organizaciones.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="b4aa9-121">En proyectos que tienen múltiples entidades de financiación, todas las partes que contribuyen a la financiación de un proyecto de financiación avanzado se denominan fuentes de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="b4aa9-122">Una vez que un cliente, una organización o una subvención se define como fuente de financiación, se puede asignar a una o más reglas de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="b4aa9-123">Las reglas de financiación contienen los criterios que determinan cómo se asignan los cargos a las diversas fuentes de financiación de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="b4aa9-124">Debido a que los artículos almacenados, como los que aparecen en las solicitudes de compra y las órdenes de compra, no se pueden dividir, el importe del coste no se puede dividir entre varias fuentes de financiación en el momento de la distribución.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="b4aa9-125">Por lo tanto, el valor de la fuente de financiación sigue siendo 0 (cero) hasta que se registre la emisión de inventario.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="b4aa9-126">Cuando se registra la emisión de inventario, el importe del coste se distribuye de acuerdo con las reglas de distribución de cuentas para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="b4aa9-127">A continuación, se muestran algunos pasos que puede seguir para facilitar la división de la facturación entre varias fuentes de financiación:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="b4aa9-128">Especifique que todas las transacciones que se especifican para un proyecto utilizan la misma moneda de venta que el contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="b4aa9-129">Establezca límites de financiación, de modo que no se facture a una fuente de financiación más de un importe específico para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="b4aa9-130">Configure las reglas de financiación y los límites de financiación para cada trabajador, artículo, categoría, grupo de categoría y tipo de transacción (o para todos los tipos de transacción).</span><span class="sxs-lookup"><span data-stu-id="b4aa9-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="b4aa9-131">Seleccione fechas de inicio y finalización opcionales para definir el período en el que cada regla de financiación es válida.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="b4aa9-132">Especifique el porcentaje del que es responsable cada fuente de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="b4aa9-133">Especifique qué fuente de financiamiento es responsable de redondear las diferencias causadas por los cálculos de asignación de fondos.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="b4aa9-134">Configure reglas que determinen cómo los costes del proyecto se facturan a los clientes externos y se cargan a las organizaciones internas.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="b4aa9-135">Registre las transacciones en una cuenta de fondos retenidos hasta que pueda obtener fondos adicionales, o hasta que decida asumir los costes internamente.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="b4aa9-136">Para determinar qué grupo de impuestos asociar con una transacción, se busca en el proyecto una asignación de grupo de impuestos.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="b4aa9-137">Si no se ha realizado ninguna asignación de grupo de impuestos a nivel de proyecto, se busca el contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="b4aa9-138">Ejemplo: Múltiples fuentes de financiación (simple)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="b4aa9-139">La siguiente tabla proporciona escenarios para administrar la asignación de fondos entre múltiples fuentes de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="b4aa9-140">Estos escenarios se basan en los supuestos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="b4aa9-141">La configuración de prioridades se tiene en cuenta en la asignación de fondos antes de que se apliquen otros criterios de reglas de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="b4aa9-142">No se ha especificado ningún intervalo de fechas para definir el período d, cuando la regla de financiación es válida.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4aa9-143"><strong>Escenario</strong></span><span class="sxs-lookup"><span data-stu-id="b4aa9-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="b4aa9-144"><strong>Fuente de financiación</strong></span><span class="sxs-lookup"><span data-stu-id="b4aa9-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="b4aa9-145"><strong>Porcentaje de asignación</strong></span><span class="sxs-lookup"><span data-stu-id="b4aa9-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="b4aa9-146"><strong>Prioridad de asignación</strong></span><span class="sxs-lookup"><span data-stu-id="b4aa9-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4aa9-147">Desea asignar costes a una fuente de financiamiento hasta que se agoten sus fondos, asignar costos a una segunda fuente de financiación hasta que se agoten sus fondos y, finalmente, asignar los costes restantes a una tercera fuente de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4aa9-148">Fuente de financiación 1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="b4aa9-149">Fuente de financiación 2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="b4aa9-150">Fuente de financiación 3</span><span class="sxs-lookup"><span data-stu-id="b4aa9-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4aa9-151">100%</span><span class="sxs-lookup"><span data-stu-id="b4aa9-151">100%</span></span></li>
<li><span data-ttu-id="b4aa9-152">100%</span><span class="sxs-lookup"><span data-stu-id="b4aa9-152">100%</span></span></li>
<li><span data-ttu-id="b4aa9-153">100%</span><span class="sxs-lookup"><span data-stu-id="b4aa9-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4aa9-154">1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-154">1</span></span></li>
<li><span data-ttu-id="b4aa9-155">2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-155">2</span></span></li>
<li><span data-ttu-id="b4aa9-156">3</span><span class="sxs-lookup"><span data-stu-id="b4aa9-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4aa9-157">Desea asignar el 75 por ciento de los costes a una fuente de financiación y el 25 por ciento a una segunda fuente de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="b4aa9-158">Cuando se agote cualquiera de esas fuentes de financiación, querrá pagar los costes restantes de una tercera fuente de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4aa9-159">Fuente de financiación 1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="b4aa9-160">Fuente de financiación 2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="b4aa9-161">Fuente de financiación 3</span><span class="sxs-lookup"><span data-stu-id="b4aa9-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4aa9-162">75 %</span><span class="sxs-lookup"><span data-stu-id="b4aa9-162">75%</span></span></li>
<li><span data-ttu-id="b4aa9-163">25 %</span><span class="sxs-lookup"><span data-stu-id="b4aa9-163">25%</span></span></li>
<li><span data-ttu-id="b4aa9-164">100%</span><span class="sxs-lookup"><span data-stu-id="b4aa9-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4aa9-165">1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-165">1</span></span></li>
<li><span data-ttu-id="b4aa9-166">1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-166">1</span></span></li>
<li><span data-ttu-id="b4aa9-167">2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4aa9-168">Desea asignar el 75 por ciento de los costes a una fuente de financiación y el 25 por ciento a una segunda fuente de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="b4aa9-169">Cuando se agote cualquiera de esas fuentes de financiación, querrá dividir los costes restantes entre una tercera fuente de financiación y una cuarta.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4aa9-170">Fuente de financiación 1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="b4aa9-171">Fuente de financiación 2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="b4aa9-172">Fuente de financiación 3</span><span class="sxs-lookup"><span data-stu-id="b4aa9-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="b4aa9-173">Fuente de financiación 4</span><span class="sxs-lookup"><span data-stu-id="b4aa9-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4aa9-174">75 %</span><span class="sxs-lookup"><span data-stu-id="b4aa9-174">75%</span></span></li>
<li><span data-ttu-id="b4aa9-175">25 %</span><span class="sxs-lookup"><span data-stu-id="b4aa9-175">25%</span></span></li>
<li><span data-ttu-id="b4aa9-176">50 %</span><span class="sxs-lookup"><span data-stu-id="b4aa9-176">50%</span></span></li>
<li><span data-ttu-id="b4aa9-177">50 %</span><span class="sxs-lookup"><span data-stu-id="b4aa9-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4aa9-178">1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-178">1</span></span></li>
<li><span data-ttu-id="b4aa9-179">1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-179">1</span></span></li>
<li><span data-ttu-id="b4aa9-180">2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-180">2</span></span></li>
<li><span data-ttu-id="b4aa9-181">2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4aa9-182">Desea asignar el primer 25 por ciento de los costes a una fuente de financiación y el resto a una segunda fuente de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4aa9-183">Fuente de financiación 1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="b4aa9-184">Fuente de financiación 2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4aa9-185">25 %</span><span class="sxs-lookup"><span data-stu-id="b4aa9-185">25%</span></span></li>
<li><span data-ttu-id="b4aa9-186">100%</span><span class="sxs-lookup"><span data-stu-id="b4aa9-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4aa9-187">1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-187">1</span></span></li>
<li><span data-ttu-id="b4aa9-188">2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="b4aa9-189">Ejemplo: Múltiples fuentes de financiación (complejo)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="b4aa9-190">Tiene tres fuentes de financiación que desea utilizar en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="b4aa9-191">Utilice la fuente de financiación 2 y la fuente de financiación 3 por igual hasta que se agote la fuente de financiación 2.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="b4aa9-192">Continúe utilizando la fuente de financiación 3 hasta que se agote.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="b4aa9-193">Utilice la fuente de financiación 1 después de que se agote la fuente de financiación 3.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="b4aa9-194">Para lograr este objetivo, en primer lugar debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="b4aa9-195">Establezca límites de financiación para la fuente de financiación 2 y la fuente de financiación 3, para sus respectivos importes.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="b4aa9-196">Cree las siguientes reglas de financiación:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="b4aa9-197">Regla 1 (Prioridad 1): asignar el 50 por ciento de las transacciones a la fuente de financiamiento 2 y el 50 por ciento a la fuente de financiamiento 3.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="b4aa9-198">Regla 2 (Prioridad 2): asignar el 100 por ciento de las transacciones a la fuente de financiación 3.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="b4aa9-199">Regla 3 (Prioridad 3): asignar el 100 por ciento de las transacciones a la fuente de financiación 1.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="b4aa9-200">Esta configuración funciona porque las transacciones se comparan con reglas y límites para determinar si alguna de ellas se aplica a la transacción.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="b4aa9-201">Si no se aplican reglas o límites específicos a la transacción, se aplica la regla Todas las transacciones.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="b4aa9-202">La regla Todas las transacciones coincide con todas las transacciones.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="b4aa9-203">Si se encuentra una regla que coincide con una transacción, el porcentaje que se ha asignado en esa regla se aplica primero, pero solo después de que las coincidencias se verifiquen con arreglo a los límites que se hayan establecido.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="b4aa9-204">Si se ha alcanzado un límite y se agotan los fondos de una fuente de financiación, se ignora la regla de financiación asociada con el límite de financiación y el programa verifica la siguiente regla que se aplica.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="b4aa9-205">En algunos casos, solo se puede asignar una parte de una transacción según una regla.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="b4aa9-206">Esto puede suceder porque se alcanza un límite cuando se asigna la transacción.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="b4aa9-207">En este caso, solo se asigna una cierta cantidad de acuerdo con esa regla, como el 50 por ciento a cada fuente de financiación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="b4aa9-208">Este es el caso de la regla 1, que se describe anteriormente en esta sección.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="b4aa9-209">El resto se asigna de acuerdo con la siguiente regla en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="b4aa9-210">En la siguiente tabla se examina esta escenario con más detalle.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4aa9-211"><strong>Foco</strong></span><span class="sxs-lookup"><span data-stu-id="b4aa9-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="b4aa9-212"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="b4aa9-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4aa9-213">Reglas de financiación</span><span class="sxs-lookup"><span data-stu-id="b4aa9-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="b4aa9-214">Regla 1 (Prioridad 1): todas las transacciones.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="b4aa9-215">Asigne la fuente de financiación 2 al 50 % y la fuente de financiación 3 al 50 %.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="b4aa9-216">Regla 2 (Prioridad 2): todas las transacciones.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="b4aa9-217">Asigne la fuente de financiación 3 al 100 %.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="b4aa9-218">Regla 3 (Prioridad 2): todas las transacciones.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="b4aa9-219">Asigne la fuente de financiación 1 al 100 %.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4aa9-220">Límites de financiación</span><span class="sxs-lookup"><span data-stu-id="b4aa9-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="b4aa9-221">Límite de la fuente de financiación 1 = 10 000</span><span class="sxs-lookup"><span data-stu-id="b4aa9-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="b4aa9-222">Límite de la fuente de financiación 2 = 500</span><span class="sxs-lookup"><span data-stu-id="b4aa9-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="b4aa9-223">Límite de la fuente de financiación 3 = 750</span><span class="sxs-lookup"><span data-stu-id="b4aa9-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4aa9-224">Transacción 1</span><span class="sxs-lookup"><span data-stu-id="b4aa9-224">Transaction 1</span></span></td>
<td><span data-ttu-id="b4aa9-225"><strong>Importe de la transacción</strong>: 100 <strong>Financiación</strong>: la transacción se paga de acuerdo con la regla 1 únicamente, porque la transacción se paga en su totalidad después de que se aplica la regla 1.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="b4aa9-226">La transacción se financia a partes iguales entre la fuente de financiación 2 y la fuente de financiación 3.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="b4aa9-227">Fuente de financiación 2: 50</span><span class="sxs-lookup"><span data-stu-id="b4aa9-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="b4aa9-228">Fuente de financiación 3: 50</span><span class="sxs-lookup"><span data-stu-id="b4aa9-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4aa9-229">Transacción 2</span><span class="sxs-lookup"><span data-stu-id="b4aa9-229">Transaction 2</span></span></td>
<td><span data-ttu-id="b4aa9-230"><strong>Importe de la transacción</strong>: 5000 <strong>Financiación</strong>: la transacción se paga de acuerdo con la totalidad de las tres reglas.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="b4aa9-231"><strong>Regla 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="b4aa9-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="b4aa9-232">Fuente de financiación 2: 450</span><span class="sxs-lookup"><span data-stu-id="b4aa9-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="b4aa9-233">Fuente de financiación 3: 450</span><span class="sxs-lookup"><span data-stu-id="b4aa9-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="b4aa9-234">
<strong>Regla 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="b4aa9-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="b4aa9-235">Fuente de financiación 3: 250 (= 750 – 50 – 450)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="b4aa9-236">
<strong>Regla 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="b4aa9-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="b4aa9-237">Fuente de financiación 1: 3850 (= 5000 – 450 – 450 – 250)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4aa9-238">Fondos totales que se distribuyen para cada fuente de financiación</span><span class="sxs-lookup"><span data-stu-id="b4aa9-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="b4aa9-239">Fuente de financiación 1: 3850</span><span class="sxs-lookup"><span data-stu-id="b4aa9-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="b4aa9-240">Fuente de financiación 2: 500</span><span class="sxs-lookup"><span data-stu-id="b4aa9-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="b4aa9-241">Fuente de financiación 3: 750</span><span class="sxs-lookup"><span data-stu-id="b4aa9-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="b4aa9-242">Reglas de facturación</span><span class="sxs-lookup"><span data-stu-id="b4aa9-242">Billing rules</span></span>
<span data-ttu-id="b4aa9-243">Cuando negocia un contrato de proyecto con un cliente, define cómo y cuándo puede facturar al cliente por el trabajo en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="b4aa9-244">Después de configurar el contrato de proyecto y el proyecto, puede configurar las reglas de facturación para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="b4aa9-245">Las reglas de facturación se basan en los términos del proyecto que se especifican en el contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="b4aa9-246">Las reglas de facturación que puede crear dependen de los términos del contrato del proyecto y del tipo de proyecto, como tiempo y material o precio fijo, que asocie con la regla de facturación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="b4aa9-247">Puede crear más de una regla de facturación para un contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="b4aa9-248">También puede asignar una regla de facturación a varios proyectos que están asociados con el mismo contrato de proyecto y tienen condiciones de facturación similares.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="b4aa9-249">Puede configurar los siguientes tipos de reglas de facturación:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="b4aa9-250">**Unidad de entrega**: facturar a un cliente cuando complete una unidad de entrega.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="b4aa9-251">Defina las unidades de entrega en el contrato.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="b4aa9-252">**Progreso**: facturar a un cliente cuando complete un porcentaje específico del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="b4aa9-253">Puede configurar una regla de facturación para calcular automáticamente el porcentaje de trabajo completado, o puede calcular manualmente el porcentaje de trabajo completado y la cantidad a facturar al cliente.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="b4aa9-254">**Hito**: facturar a un cliente por el importe total de un hito de proyecto cuando se alcance el hito.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="b4aa9-255">**Tarifa**: facturar a un cliente por sus servicios más una tarifa de administración, que generalmente es un porcentaje del coste de los servicios.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="b4aa9-256">**Tiempo y material**: facturar a un cliente por el valor del tiempo y los materiales que se utilizan en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="b4aa9-257">Para todos los tipos de reglas de facturación, puede especificar un porcentaje de retención que se deduce de las facturas de los clientes hasta que un proyecto alcance una fase acordada.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="b4aa9-258">El porcentaje de retención del pago se especifica en el contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="b4aa9-259">El importe se calcula y se resta del valor total de las líneas en una factura de cliente.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="b4aa9-260">Para las reglas de facturación **Tiempo y material** y **Progreso**, puede asignar categorías imputables.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="b4aa9-261">Las categorías imputables indican las transacciones que deben incluirse en las facturas de los clientes.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="b4aa9-262">Cuando esté listo para facturar al cliente, el importe a facturar por el proyecto se calcula según las reglas de facturación y se genera una propuesta de factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="b4aa9-263">Las siguientes secciones proporcionan ejemplos que muestran cómo configurar y administrar reglas de facturación para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="b4aa9-264">Ejemplo: Crear una regla de facturación basada en la cantidad de unidades entregadas</span><span class="sxs-lookup"><span data-stu-id="b4aa9-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="b4aa9-265">Su organización formaliza un acuerdo para proporcionar un total de cinco sesiones de formación a los empleados de un cliente a un coste de 10 000 por sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="b4aa9-266">Factura al cliente después de cada sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="b4aa9-267">Cuando configura las reglas de facturación para el contrato, usa los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="b4aa9-268">La unidad de entrega es una sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="b4aa9-269">El precio unitario es de 10 000 por sesión de formación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="b4aa9-270">El número total de unidades es de cinco sesiones de formación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="b4aa9-271">Cuando haya completado una sesión de formación, puede crear una factura por 10 000, por la primera unidad que se entregó, y enviar la factura al cliente.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="b4aa9-272">Ejemplo: Crear una regla de facturación basada en un porcentaje específico de finalización del proyecto (cálculo manual)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="b4aa9-273">Su organización, una empresa de consultoría de software, formaliza un acuerdo con un cliente para desarrollar parte de un producto que el cliente está desarrollando.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="b4aa9-274">Su organización acepta entregar el código de software a lo largo de un periodo de seis meses.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="b4aa9-275">El cliente acepta pagar a su organización un total de 100 000 por el trabajo.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="b4aa9-276">Crea una regla de facturación para facturar al cliente en función del porcentaje de trabajo que se completa en el proyecto, como se especifica en el contrato.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="b4aa9-277">Al final del primer mes, se reúne con el cliente para determinar el porcentaje de trabajo completado.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="b4aa9-278">Después de que usted y el cliente revisen el proyecto, decide que el proyecto está completado en un 15 por ciento.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="b4aa9-279">Crea una factura para 15 000 (15 por ciento de 100 000) y se la envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="b4aa9-280">Ejemplo: Crear una regla de facturación basada en un porcentaje específico de finalización del proyecto (cálculo automático)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="b4aa9-281">Su organización, una empresa de desarrollo de software, acepta desarrollar un paquete de gestión de nóminas para un cliente por 30 000.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="b4aa9-282">El cliente acepta pagar a su organización en función del porcentaje de trabajo terminado.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="b4aa9-283">Calcula que los costes del proyecto son 20 000.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="b4aa9-284">El contrato del proyecto especifica las categorías de trabajo que utiliza en el proceso de facturación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="b4aa9-285">Configura reglas de facturación que calculan automáticamente los importes de la factura para el porcentaje de trabajo completado para cada categoría.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="b4aa9-286">Establece un presupuesto para cada categoría:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="b4aa9-287">**Desarrollo**: coste de 15 000 e ingresos de 20 000</span><span class="sxs-lookup"><span data-stu-id="b4aa9-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="b4aa9-288">**Instalación**: coste de 5000 e ingresos de 10 000</span><span class="sxs-lookup"><span data-stu-id="b4aa9-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="b4aa9-289">Cuando crea una factura de cliente por primera vez, el importe de la factura se calcula automáticamente en función de la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="b4aa9-290">Después de un mes, el trabajador del proyecto envía una hoja de horas para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="b4aa9-291">El coste de las horas del trabajador es de 5000 para el desarrollo y 1000 para la instalación.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="b4aa9-292">El trabajo de desarrollo está completado en un 33 % (coste real de 5000/coste presupuestado de 15 000) y el trabajo de instalación está completado en un 20 % (coste real de 1000/coste presupuestado de 5000).</span><span class="sxs-lookup"><span data-stu-id="b4aa9-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="b4aa9-293">El importe de la factura de 8667 se calcula automáticamente (33 por ciento de 20 000 + 20 por ciento de 10 000).</span><span class="sxs-lookup"><span data-stu-id="b4aa9-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="b4aa9-294">Crea una factura por 8667 y se la envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="b4aa9-295">Ejemplo: Crear una regla de facturación basada en hitos acordados</span><span class="sxs-lookup"><span data-stu-id="b4aa9-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="b4aa9-296">Su organización, una empresa de consultoría de gestión, acepta realizar una investigación de mercado para un producto de consumo que el cliente planea vender.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="b4aa9-297">El cliente acepta utilizar sus servicios por un período de tres meses, a partir de marzo, y acepta pagar a su organización 50 000.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="b4aa9-298">El proyecto tiene tres hitos:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-298">The project has three milestones:</span></span>

-   <span data-ttu-id="b4aa9-299">Hito 1: Recopilar datos del consumidor (31 de marzo)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="b4aa9-300">Hito 2: Analizar datos de consumidores (30 de abril)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="b4aa9-301">Hito 3: Presentar una propuesta de viabilidad del producto (31 de mayo)</span><span class="sxs-lookup"><span data-stu-id="b4aa9-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="b4aa9-302">El cliente acepta pagar a su organización 10 000 por el primer hito, 20 000 por el segundo y 20 000 por el tercer hito.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="b4aa9-303">Cuando configura el contrato del proyecto, acepta facturar al cliente según el hito que se haya completado.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="b4aa9-304">La configuración de la regla de facturación incluye los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="b4aa9-305">Definir la categoría del hito.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-305">Define the project milestones.</span></span>
-   <span data-ttu-id="b4aa9-306">Defina el importe a facturar al cliente cuando se complete cada hito.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="b4aa9-307">Cuando se completa el primer hito el 31 de marzo, marca el hito como completado y luego crea una factura por 10 000 y se la envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="b4aa9-308">No puede crear una factura para un hito hasta que haya marcado el hito como completado.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="b4aa9-309">Ejemplo: Crear una regla de facturación basada en los servicios más una tarifa de gestión</span><span class="sxs-lookup"><span data-stu-id="b4aa9-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="b4aa9-310">Su organización, una empresa de consultoría de gestión, acepta realizar una investigación de mercado para evaluar la viabilidad de un producto que el cliente, una empresa minorista, está desarrollando.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="b4aa9-311">Los términos del acuerdo especifican que proporcionará los servicios de sus tres principales consultores de gestión, quienes realizarán la investigación en función del tiempo y los materiales.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="b4aa9-312">El cliente acepta pagar 100 por hora, más una tarifa de gestión del 10 por ciento por las horas de consultoría que se cargan al proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="b4aa9-313">Cuando configure el contrato del proyecto, cree una regla de facturación para agregar una tarifa de gestión del 10 por ciento a las horas de consultoría que se cargan al proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="b4aa9-314">Cuando crea una factura para el cliente, al cliente se le factura una tarifa de gestión del 10 por ciento más el coste de las horas de consultoría.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="b4aa9-315">Por ejemplo, si los tres consultores trabajaron un total de 200 horas en el proyecto, se crea una factura por 22 000 según el siguiente cálculo:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="b4aa9-316">200 horas a 100 por hora = 20 000</span><span class="sxs-lookup"><span data-stu-id="b4aa9-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="b4aa9-317">Comisión de gestión del 10 por ciento = 2000</span><span class="sxs-lookup"><span data-stu-id="b4aa9-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="b4aa9-318">Importe total de la factura = 22 000</span><span class="sxs-lookup"><span data-stu-id="b4aa9-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="b4aa9-319">Si las tarifas están sujetas a impuestos para un cliente y selecciona un grupo de impuestos en el contrato del proyecto, el grupo de impuestos se especifica automáticamente en una regla de facturación para las tarifas.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="b4aa9-320">Ejemplo: Crear una regla de facturación para el valor del tiempo y los materiales</span><span class="sxs-lookup"><span data-stu-id="b4aa9-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="b4aa9-321">Su organización, una empresa de consultoría de software, acepta proporcionar cinco consultores técnicos para trabajar en un proyecto de desarrollo de software para un cliente durante los próximos seis meses.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="b4aa9-322">El cliente se compromete a pagar 150 por cada hora de consultoría, más el coste de los suministros de oficina.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="b4aa9-323">Su organización envía una factura al cliente al final de cada mes.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="b4aa9-324">Cuando configura el contrato del proyecto, acepta facturar al cliente cada mes por el tiempo y los materiales del proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="b4aa9-325">Crea una regla de facturación que incluye la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="b4aa9-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="b4aa9-326">La duración del contrato es de seis meses.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-326">The contract period is six months.</span></span>
-   <span data-ttu-id="b4aa9-327">El tiempo de consulta se calcula a razón de 150 por hora.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="b4aa9-328">Los suministros de oficina se facturan al coste y el coste total del proyecto no debe exceder los 10 000.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="b4aa9-329">Crea una factura de cliente al final de cada mes natural durante el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="b4aa9-330">Durante el primer mes, los consultores del proyecto registran un total de 800 horas.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="b4aa9-331">El coste de los suministros de oficina que se cargan al proyecto es de 2000.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="b4aa9-332">Por lo tanto, al final del mes, crea una factura por 122 000, que se calcula como 800 horas a 150 por hora, más 2000 para suministros de oficina.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



