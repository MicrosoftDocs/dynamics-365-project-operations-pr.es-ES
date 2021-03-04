---
title: Gastos de empresas vinculadas
description: Este tema proporciona información sobre cómo se usan los gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960853"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="9c730-103">Gastos de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="9c730-103">Intercompany expenses</span></span>

<span data-ttu-id="9c730-104">Un trabajador contratado por una entidad jurídica de una organización puede trabajar para otra entidad jurídica de la misma organización.</span><span class="sxs-lookup"><span data-stu-id="9c730-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="9c730-105">Puede utilizar los gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="9c730-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="9c730-106">La entidad jurídica que emplea al trabajador se denomina entidad jurídica prestamista.</span><span class="sxs-lookup"><span data-stu-id="9c730-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="9c730-107">La entidad jurídica por la que el trabajador incurre en gastos se denomina entidad jurídica prestataria.</span><span class="sxs-lookup"><span data-stu-id="9c730-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="9c730-108">Para que un trabajador pueda crear y enviar gastos de empresas vinculadas, hay que habilitar las líneas de gastos de empresas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="9c730-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="9c730-109">En la entidad jurídica prestamista, en la página **Parámetros de gestión de gastos**, seleccione **Permitir líneas de gastos de empresas vinculadas**.</span><span class="sxs-lookup"><span data-stu-id="9c730-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="9c730-110">Contabilización de impuestos para gastos de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="9c730-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c730-111">Para poder utilizar grupos de impuestos asociados con la entidad jurídica prestamista (origen) en lugar de la entidad jurídica prestataria (destino) en un informe de gastos, hay que habilitar la funcionalidad en la configuración de impuestos sobre las ventas de la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="9c730-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="9c730-112">Si el parámetro **Entidad jurídica para registrar impuestos de empresas vinculadas** está establecido en **Origen** y el campo **Aplicar reglas de tributación de impuestos** está establecido en **No**, se utilizará la combinación de impuestos para la entidad jurídica prestamista.</span><span class="sxs-lookup"><span data-stu-id="9c730-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="9c730-113">Cuando el mismo parámetro se establece en **Destino**, se utilizará la combinación de impuestos para la entidad jurídica prestataria.</span><span class="sxs-lookup"><span data-stu-id="9c730-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="9c730-114">Para las entidades legales en los Estados Unidos, cuando el parámetro se establece en **Origen**, el campo **Impuesto sobre las ventas por cobrar** también debe configurarse en la nueva página **Grupos de contabilización del libro mayor**.</span><span class="sxs-lookup"><span data-stu-id="9c730-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="9c730-115">El motor de contabilidad utilizará la información de este campo para la entrada contable relacionada con los impuestos.</span><span class="sxs-lookup"><span data-stu-id="9c730-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="9c730-116">El comportamiento es consistente para las líneas de gastos contabilizadas con o sin un proyecto.</span><span class="sxs-lookup"><span data-stu-id="9c730-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
