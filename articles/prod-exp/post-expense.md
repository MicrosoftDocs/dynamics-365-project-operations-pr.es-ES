---
title: Registrar un informe de gastos
description: Este tema explica cómo registrar un informe de gastos en el libro mayor.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085294"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="04e4d-103">Registrar un informe de gastos</span><span class="sxs-lookup"><span data-stu-id="04e4d-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04e4d-104">Una vez que se ha aprobado y transferido un informe de gastos al diario general, se puede registrar al libro de contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="04e4d-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="04e4d-105">Cuando publica un informe de gastos, se identifican los gastos que son idóneos para la recuperación del impuesto sobre el valor añadido (IVA).</span><span class="sxs-lookup"><span data-stu-id="04e4d-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="04e4d-106">La tarea de verificar y recuperar los pagos del IVA se asigna al empleado que es responsable de verificar el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="04e4d-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="04e4d-107">Si los gastos de un informe de gastos se cargan a una empresa que no sea la empresa que emplea al empleado, debe verificar tanto la empresa a la que se le deben esos gastos como la empresa que los adeuda.</span><span class="sxs-lookup"><span data-stu-id="04e4d-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="04e4d-108">Por ejemplo, el empleado que presentó un informe de gastos trabaja para la empresa DAT pero le cobró un gasto a la empresa DIR.</span><span class="sxs-lookup"><span data-stu-id="04e4d-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="04e4d-109">En este caso, DAT es la empresa a la que se debe el gasto y DIR es la empresa que debe el gasto.</span><span class="sxs-lookup"><span data-stu-id="04e4d-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="04e4d-110">Después de verificar estas líneas de diario, puede registrar las líneas de gastos en el libro mayor.</span><span class="sxs-lookup"><span data-stu-id="04e4d-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="04e4d-111">Para registrar un informe de gastos, en la página **Informes de gastos aprobados** , seleccione el informe de gastos y, a continuación, en el Panel de acciones, seleccione **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="04e4d-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="04e4d-112">También puede registrar todos los informes de gastos de la lista al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="04e4d-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="04e4d-113">Seleccione todos los informes de gastos y luego seleccione **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="04e4d-113">Select all the expense reports, and then select **Post**.</span></span>
