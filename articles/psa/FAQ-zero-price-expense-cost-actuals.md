---
title: ¿Por qué el precio se establece de forma predeterminada en cero en costes reales de los gastos?
description: Solución de problemas de por qué un precio se establece de forma predeterminada en cero en costes reales de los gastos.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146369"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="b69e6-103">Por qué el precio se establece de forma predeterminada en cero en los datos reales de costes de gastos</span><span class="sxs-lookup"><span data-stu-id="b69e6-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b69e6-104">Estas preguntas más frecuentes se aplican a gastos reales donde la clase de transacción se establece en Gasto y el tipo de transacción es Coste.</span><span class="sxs-lookup"><span data-stu-id="b69e6-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="b69e6-105">Solución de problemas de tasas de costes en costes reales de los gastos</span><span class="sxs-lookup"><span data-stu-id="b69e6-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="b69e6-106">Vaya a la entrada de gasto relacionada y asegúrese de que hay un importe en el campo de entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="b69e6-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="b69e6-107">Si la entrada de gasto de origen no tenía el campo de importe relleno, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="b69e6-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="b69e6-108">Para resolver este problema, vuelva a crear la entrada de gasto con un importe válido y apruébela.</span><span class="sxs-lookup"><span data-stu-id="b69e6-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
