---
title: ¿Por qué el precio se establece de forma predeterminada en cero en costes reales de los gastos?
description: Solución de problemas de por qué un precio se establece de forma predeterminada en cero en costes reales de los gastos.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085169"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>¿Por qué el precio se establece de forma predeterminada en cero en costes reales de los gastos?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas preguntas más frecuentes se aplican a gastos reales donde la clase de transacción se establece en Gasto y el tipo de transacción es Coste.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Solución de problemas de tasas de costes en costes reales de los gastos

Vaya a la entrada de gasto relacionada y asegúrese de que hay un importe en el campo de entrada de gasto. Si la entrada de gasto de origen no tenía el campo de importe relleno, ha aislado el problema.
 
Para resolver este problema, vuelva a crear la entrada de gasto con un importe válido y apruébela.
