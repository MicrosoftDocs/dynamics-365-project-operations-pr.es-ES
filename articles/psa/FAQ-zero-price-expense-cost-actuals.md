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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285878"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="46be5-103">Por qué el precio se establece de forma predeterminada en cero en los datos reales de costes de gastos</span><span class="sxs-lookup"><span data-stu-id="46be5-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="46be5-104">Estas preguntas más frecuentes se aplican a gastos reales donde la clase de transacción se establece en Gasto y el tipo de transacción es Coste.</span><span class="sxs-lookup"><span data-stu-id="46be5-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="46be5-105">Solución de problemas de tasas de costes en costes reales de los gastos</span><span class="sxs-lookup"><span data-stu-id="46be5-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="46be5-106">Vaya a la entrada de gasto relacionada y asegúrese de que hay un importe en el campo de entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="46be5-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="46be5-107">Si la entrada de gasto de origen no tenía el campo de importe relleno, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="46be5-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="46be5-108">Para resolver este problema, vuelva a crear la entrada de gasto con un importe válido y apruébela.</span><span class="sxs-lookup"><span data-stu-id="46be5-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]