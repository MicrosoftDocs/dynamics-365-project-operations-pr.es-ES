---
title: ¿Por qué el precio se establece de forma predeterminada en cero en costes reales del tiempo?
description: Solución de problemas de por qué un precio se establece de forma predeterminada en cero en costes reales del tiempo.
author: rumant
manager: kfend
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
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131405"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>¿Por qué el precio se establece de forma predeterminada en cero en costes reales del tiempo?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas preguntas más frecuentes se aplican a datos reales donde la clase de transacción se establece en Tiempo y el tipo de transacción es Coste. Las tres comprobaciones siguientes le ayudarán a resolver el problema de que el precio se establezca de forma predeterminada en 0 en costes reales de tiempo.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Comprobación 1: Identificar la lista de precios de costes para el proyecto

Busque el proyecto en el campo de proyecto de los datos reales y vaya a la página de proyecto. Haga clic en el vínculo de unidad de contratación en el campo. En la página Unidad de contratación, compruebe si la unidad de contratación tiene una lista de precios en la cuadrícula Listas de precios de coste.

Si hay más de una lista de precios, ha aislado el problema. Project Service sólo admite una lista de precios por unidad organizativa. Quite todas las listas de precios de esta entidad hasta que quede sólo una lista de precios adjunta en la cuadrícula de Listas de precios de coste de la unidad organizativa.

Si no hay listas de precios adjuntadas a la unidad organizativa, anote la divisa de la unidad organizativa. Vaya a Project Service y luego a Parámetros y abra la pestaña Listas de precios. Compruebe si existen listas de precios con contexto establecido para coste y divisa que coincida con la divisa de la unidad organizativa.
 
Si no hay listas de precios que coincidan con ese criterio, ha aislado el problema. Asegúrese de tener al menos una lista de precios cuyo contexto esté establecido como Coste y cuya divisa coincida con la divisa de la unidad organizativa.

Si hay más de una lista de precios que coincida con ese criterio, continúe leyendo este documento para hacer más comprobaciones.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Comprobación 2: ¿Alguna de las listas de precios identificadas anteriormente son válidas para el coste real del tiempo?

Para que Project Service considere una lista de precios para precio predeterminado, esa lista de precios debe ser aplicable a la fecha en el coste real del tiempo. Compruebe lo siguiente para ver si es aplicable la lista o listas de precios identificadas antes:

- Compruebe si no están vacías las fechas de inicio y finalización de la pestaña general para listas de precios adjuntas. Si las fechas de inicio y finalización de las listas de precios identificadas anteriormente están vacías, ha aislado el problema. 
- Anote el campo de fecha de inicio en el coste real del tiempo y compruebe si alguna de las listas de precios identificadas es aplicable para esa fecha. Por ejemplo, la fecha de costes reales del tiempo debe estar dentro de la fecha de inicio y la fecha de finalización de la lista de precios. 
    - Si no hay ninguna lista de precios que cubra esa fecha en el coste real del tiempo, ha aislado el problema. Modifique las fechas de inicio y finalización de la lista de precios para asegurarse de que la lista de precios cubre la fecha del coste real del tiempo. 
    - Si hay varias listas de precios que cubren la fecha en el coste real del tiempo, ha aislado el problema. Puede solucionarlo editando las fechas de inicio y finalización de la lista o listas de precios de modo que haya sólo una lista de precios que cubra la fecha del coste real del tiempo. 
    - Si solo hay una lista de precios que cubre esa fecha del coste real del tiempo, pase a la siguiente comprobación del documento.
Cuando termine de hacer las correcciones necesarias, vuelva a crear una entrada de tiempo, apruébela, y compruebe que el coste real del tiempo muestra un precio válido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Comprobación 3: ¿Existe un precio en la lista de precios para las dimensiones de precios en el coste real del tiempo?

Si ha completado correctamente la Comprobación 1 y la Comprobación 2, ahora debe tener únicamente una lista de precios que es aplicable al coste real del tiempo. Abra esta Lista de precios y vaya a la pestaña Precios de rol. Asegúrese de que hay una fila en la cuadrícula para las dimensiones de precios en el coste real del tiempo.

Si no hay ninguna fila en la cuadrícula de precios de rol para las dimensiones de precios en el coste real del tiempo, ha aislado el problema. Cree una fila en la cuadrícula Precios de rol para las dimensiones de precios en el coste real del tiempo. Cuando termine, vuelva a crear una entrada de tiempo, apruébela, y compruebe que el coste real del tiempo muestra un precio válido.
 
Si aún no ve un precio válido en el coste real del tiempo después de realizar las tres comprobaciones anteriores, registre un vale de soporte.



