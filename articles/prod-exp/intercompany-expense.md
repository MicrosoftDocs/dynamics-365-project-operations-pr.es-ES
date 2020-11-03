---
title: Gastos de empresas vinculadas
description: Un trabajador contratado por una entidad legal en una organización puede realizar trabajo para otra entidad legal en la misma organización. En esta situación, puede utilizar la función de gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085299"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="2ad7e-104">Gastos de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="2ad7e-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ad7e-105">Un trabajador contratado por una entidad legal en una organización puede realizar trabajo para otra entidad legal en la misma organización.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="2ad7e-106">En esta situación, puede utilizar la función de gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="2ad7e-107">La entidad jurídica que emplea al trabajador se denomina entidad jurídica prestamista.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="2ad7e-108">La entidad jurídica por la que el trabajador incurre en gastos se denomina entidad jurídica prestataria.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="2ad7e-109">Antes de que un trabajador pueda crear y enviar gastos por el trabajo que se realiza para una entidad legal diferente, en la entidad legal prestadora, en la página **Parámetros de gestión de gastos** , seleccione la opción **Permitir líneas de gastos de empresas vinculadas**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="2ad7e-110">Contabilización de impuestos para gastos de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="2ad7e-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ad7e-111">Si desea utilizar grupos de impuestos que están asociados con la entidad jurídica prestamista (fuente) en lugar de la entidad jurídica prestataria (destino) en su informe de gastos, deberá configurar esto en la configuración del impuesto sobre las ventas del Libro mayor.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="2ad7e-112">Cuando el parámetro del libro mayor, **Entidad jurídica para la contabilización de impuestos entre empresas** se establece en **Origen** y **Aplicar reglas de impuestos sobre las ventas** se establece en **No** , se utilizará la combinación de impuestos para la entidad jurídica prestadora.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="2ad7e-113">Cuando el mismo parámetro se establece en **Destino** , se utilizará la combinación de impuestos para la entidad jurídica prestataria.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="2ad7e-114">Para las entidades legales en los Estados Unidos, cuando el parámetro se establece en **Origen** , el campo **Impuesto sobre las ventas por cobrar** también debe configurarse en la nueva página **Grupos de contabilización del libro mayor**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="2ad7e-115">El motor de contabilidad utilizará la información de este campo para la entrada contable relacionada con los impuestos.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="2ad7e-116">El comportamiento es consistente para las líneas de gastos contabilizadas con o sin un proyecto.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
