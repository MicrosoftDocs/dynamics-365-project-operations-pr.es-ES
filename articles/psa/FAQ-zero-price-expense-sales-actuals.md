---
title: ¿Por qué el precio se establece de forma predeterminada en cero en ventas de gastos reales?
description: Las tres comprobaciones siguientes le ayudarán a resolver el problema de que el precio se establezca de forma predeterminada en 0 en ventas de gastos reales.
author: rumant
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: bd474d7c0cd64262fdb21d6269efa781b6dc31f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285909"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>¿Por qué el precio se establece de forma predeterminada en cero en ventas de gastos reales?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas preguntas más frecuentes se aplican a gastos reales donde la clase de transacción se establece en Gasto y el tipo de transacción es Ventas sin facturar. Las tres comprobaciones siguientes le ayudarán a resolver el problema de que el precio (tasa de facturación) se establezca de forma predeterminada en 0 en ventas de gastos reales.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Comprobación 1: Identificar la lista de precios de ventas para el proyecto

Busque el proyecto en el campo de proyecto de los datos reales y vaya a la página de proyecto. A continuación vaya a la pestaña Ventas. En la cuadrícula Líneas de contrato de proyecto, haga clic en el vínculo del campo de Contrato de proyecto. La página Contrato de proyecto se abrirá. En la página Contrato de proyecto, vaya a la pestaña Listas de precios de proyecto. Compruebe si hay al menos una lista de precios adjuntada aquí.

Si no hay ninguna lista de precios adjunta en la cuadrícula Listas de precios de proyecto del Contrato de proyecto:

- Adjunte una lista de precios a la cuadrícula Listas de precios de proyecto. Las listas de precios que pueden adjuntarse aquí deben tener el campo de contexto establecido en Ventas y el campo de divisa en la lista de precios debe coincidir con el campo de divisa en el Contrato de proyecto. Cuando haya creado las correcciones necesarias, vuelva a crear una entrada de gasto, apruébela, y compruebe que las ventas reales no facturadas muestran un precio válido.
- Si tiene una o más listas de precios adjuntas en la cuadrícula Listas de precios de proyecto del Contrato de proyecto, vaya a la Comprobación 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Comprobación 2: ¿Alguna de las listas de precios identificadas anteriormente son válidas para la fecha específica de gastos reales?

Para que Project Service considere una lista de precios para precio predeterminado, esa lista de precios debe ser aplicable a la fecha en las ventas de gastos reales. Compruebe lo siguiente para ver si es aplicable la lista o listas de precios identificadas antes:

- Inicie comprobando si no están vacías las fechas de inicio y finalización de la pestaña general para listas de precios adjuntas. Si las fechas de inicio y finalización de las listas de precios identificadas anteriormente están vacías, ha aislado el problema. 
- Anote el campo de fecha de inicio en los gastos de ventas reales y compruebe si alguna de las listas de precios identificadas es aplicable para esa fecha. Por ejemplo, la fecha de gastos reales debe estar dentro de la fecha de inicio y la fecha de finalización de la lista de precios. 
    - Si no hay ninguna lista de precios que cubra esa fecha en las ventas de gastos reales, ha aislado el problema. Modifique las fechas de inicio y finalización de la lista de precios para asegurarse de que la lista de precios cubre la fecha de los gastos reales. 
    - Si hay varias listas de precios que cubren la fecha en las ventas de gastos reales, ha aislado el problema. Edite las fechas de inicio y finalización de las listas de precios de modo que haya sólo una lista de precios que cubra la fecha de los gastos reales. 
    - Si solo hay una lista de precios que cubre esa fecha de los gastos reales, pase a la Comprobación 3.
Cuando termine de crear las correcciones necesarias, vuelva a crear una entrada de gasto, apruébela, y compruebe que las ventas reales no facturadas muestran un precio válido.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Comprobación 3: ¿Hay un precio válido para la categoría de gasto en la lista de precios del proyecto aplicable? 

Si ha completado correctamente la Comprobación 1 y la Comprobación 2, ahora debe tener únicamente una lista de precios de proyecto que es aplicable a la fecha de las ventas de gastos reales. Abra la lista de precios de proyecto y vaya a la pestaña Precios de categorías. Asegúrese de que hay una fila en la cuadrícula para la categoría de gastos específica en el Gasto real.
 
- Si no hay ninguna fila, ha aislado el problema. Cree una fila en la cuadrícula Precio de categoría para la categoría en su coste real. A continuación, vuelva a crear una entrada de gasto, apruébela y compruebe que los datos de las ventas reales sin facturar muestran un precio válido. 
- Si existe una fila de la categoría de gastos en la cuadrícula de precios de categorías, compruebe si tiene un precio válido.

Para comprender qué es un precio válido, use estos métodos:

- Si el campo Método de cálculo de precios en la línea de precios de categoría se establece en De coste, la tarifa unitaria en las ventas de gastos reales se establecerá de forma predeterminada con el valor de la entrada Gasto.
- Si el campo Método de cálculo de precios en la línea de precios de categoría se establece en Porcentaje de incremento, compruebe si el campo Porcentaje se establece en un valor válido. La tarifa unitaria en las ventas de gastos reales se establece de forma predeterminada aplicando este un porcentaje de incremento en la entrada Gasto.
- Si el campo Método de cálculo de precios en la línea de precios de categoría se establece en Precio unitario, compruebe si el campo Precio se establece en un valor válido. La tarifa unitaria en las ventas de gastos reales se establecerá de forma predeterminada con la cantidad de divisa especificada en el campo Precio.

Si la configuración de precio para la categoría de gastos no es válida, ha aislado el problema. La solución es editar la línea de precio de categoría con un precio válido para la categoría de gastos de acuerdo con las reglas anteriores. Cuando termine, vuelva a crear una entrada de gasto, apruébela, y luego compruebe que las ventas reales no facturas obtienen un precio válido.

Si aún no ve un precio válido en las ventas de gastos reales después de realizar las tres comprobaciones anteriores, registre un vale de soporte.




[!INCLUDE[footer-include](../includes/footer-banner.md)]