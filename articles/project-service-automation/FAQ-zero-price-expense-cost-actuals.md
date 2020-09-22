---
title: ¿Por qué el precio se establece de forma predeterminada en cero en costes reales de los gastos?
description: Solución de problemas de por qué un precio se establece de forma predeterminada en cero en costes reales de los gastos.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755998"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="8a0f8-103">¿Por qué el precio se establece de forma predeterminada en cero en costes reales de los gastos?</span><span class="sxs-lookup"><span data-stu-id="8a0f8-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8a0f8-104">Estas preguntas más frecuentes se aplican a gastos reales donde la clase de transacción se establece en Gasto y el tipo de transacción es Coste.</span><span class="sxs-lookup"><span data-stu-id="8a0f8-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="8a0f8-105">Solución de problemas de tasas de costes en costes reales de los gastos</span><span class="sxs-lookup"><span data-stu-id="8a0f8-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="8a0f8-106">Vaya a la entrada de gasto relacionada y asegúrese de que hay un importe en el campo de entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="8a0f8-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="8a0f8-107">Si la entrada de gasto de origen no tenía el campo de importe relleno, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="8a0f8-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="8a0f8-108">Para resolver este problema, vuelva a crear la entrada de gasto con un importe válido y apruébela.</span><span class="sxs-lookup"><span data-stu-id="8a0f8-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
