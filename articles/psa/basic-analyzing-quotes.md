---
title: Análisis de ofertas de proyecto
description: En este tema se proporciona información sobre el análisis de ofertas de proyecto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291280"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="10c8b-103">Análisis de ofertas de proyecto</span><span class="sxs-lookup"><span data-stu-id="10c8b-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="10c8b-104">Dynamics 365 Project Service Automation analiza las ofertas de proyecto para estimar la rentabilidad.</span><span class="sxs-lookup"><span data-stu-id="10c8b-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="10c8b-105">También analiza la alineación de la oferta con las expectativas del cliente en cuanto a la fecha de entrega, la fecha de finalización y el presupuesto.</span><span class="sxs-lookup"><span data-stu-id="10c8b-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="10c8b-106">Análisis de rentabilidad</span><span class="sxs-lookup"><span data-stu-id="10c8b-106">Profitability analysis</span></span>

<span data-ttu-id="10c8b-107">Project Service Automation analiza la rentabilidad mediante el margen bruto y el margen bruto ajustado.</span><span class="sxs-lookup"><span data-stu-id="10c8b-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="10c8b-108">Los márgenes brutos se calculan mediante la fórmula siguiente:</span><span class="sxs-lookup"><span data-stu-id="10c8b-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="10c8b-109">El margen bruto ajustado se calcula mediante la fórmula siguiente:</span><span class="sxs-lookup"><span data-stu-id="10c8b-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="10c8b-110">Si los valores de margen bruto y de margen bruto ajustado difieren por un amplio margen, gran parte del trabajo de la oferta se clasificará como no imputable.</span><span class="sxs-lookup"><span data-stu-id="10c8b-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="10c8b-111">Análisis de las expectativas del cliente</span><span class="sxs-lookup"><span data-stu-id="10c8b-111">Analysis of customer expectations</span></span>

<span data-ttu-id="10c8b-112">Puede analizar las ofertas y generar gráficos de expectativas del cliente acerca de la programación y el presupuesto si especifica valores para los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="10c8b-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="10c8b-113">El campo **Fecha de entrega solicitada** en el encabezado de la oferta.</span><span class="sxs-lookup"><span data-stu-id="10c8b-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="10c8b-114">El campo **Presupuesto del cliente** para cada línea de la oferta (para las líneas basadas en proyectos y las líneas basadas en productos).</span><span class="sxs-lookup"><span data-stu-id="10c8b-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="10c8b-115">El análisis de las expectativas del cliente acerca de la programación se realiza comparando la última fecha de finalización del detalle de la línea de la oferta con la fecha de entrega solicitada de todas las líneas de la oferta.</span><span class="sxs-lookup"><span data-stu-id="10c8b-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="10c8b-116">El análisis de las expectativas del cliente acerca del presupuesto se realiza comparando la suma del presupuesto del cliente total con el importe ofertado de todas las líneas de la oferta.</span><span class="sxs-lookup"><span data-stu-id="10c8b-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]