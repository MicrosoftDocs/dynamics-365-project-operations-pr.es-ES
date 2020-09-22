---
title: ¿Por qué el precio se establece de forma predeterminada en cero en ventas reales del tiempo?
description: Solución de problemas de por qué un precio se establece de forma predeterminada en cero en ventas reales del tiempo.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 202ee371-2863-4bcf-918c-212d7293faa8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 04ab519955b55088d85bdf36c3a90835f70ea501
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756027"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>¿Por qué el precio se establece de forma predeterminada en cero en ventas reales del tiempo?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas preguntas más frecuentes se aplican a datos reales donde la clase de transacción se establece en Tiempo y el tipo de transacción es Ventas sin facturar. Las tres comprobaciones siguientes le ayudarán a resolver el problema de que el precio (tasa de facturación) se establezca de forma predeterminada en 0 en ventas reales del tiempo.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Comprobación 1: Identificar la lista de precios de ventas para el proyecto

Busque el proyecto en el campo de proyecto de los datos reales y vaya a la página de proyecto. A continuación vaya a la pestaña Ventas y en la cuadrícula Líneas de contrato de proyecto, haga clic en el vínculo del campo de Contrato de proyecto. La página Contrato de proyecto se abrirá. En la página Contrato de proyecto, vaya a la pestaña Listas de precios de proyecto. Compruebe si hay al menos una lista de precios adjuntada aquí. Si no hay ninguna lista de precios adjunta en la cuadrícula Listas de precios de proyecto del Contrato de proyecto ha aislado el problema. Adjunte una lista de precios a la cuadrícula Listas de precios de proyecto. Las listas de precios que pueden adjuntarse aquí deben tener el campo de contexto establecido en Ventas y el campo de divisa en la lista de precios debe coincidir con el campo de divisa en el Contrato de proyecto. Cuando termine de crear las correcciones necesarias, vuelva a crear una entrada de tiempo, apruébela, y compruebe que las ventas reales no facturadas muestran un precio válido. 

Si tiene una o más listas de precios adjuntas en la cuadrícula Listas de precios de proyecto del Contrato de proyecto, continúe con la siguiente comprobación del documento.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Comprobación 2: ¿Alguna de las listas de precios identificadas anteriormente son válidas para el tiempo real de ventas?

Para que Project Service considere una lista de precios para precio predeterminado, esa lista de precios debe ser aplicable a la fecha en el tiempo real de ventas. Compruebe lo siguiente para ver si es aplicable la lista o listas de precios identificadas antes:
- Compruebe si no están vacías las fechas de inicio y finalización de la pestaña general para listas de precios adjuntas. Si las fechas de inicio y finalización de las listas de precios identificadas anteriormente están vacías, ha aislado el problema. 
- Anote el campo de fecha de inicio en el tiempo real de ventas y compruebe si alguna de las listas de precios identificadas es aplicable para esa fecha. Por ejemplo, la fecha de tiempo real de ventas debe estar dentro de la fecha de inicio y la fecha de finalización de la lista de precios. 
    - Si no hay ninguna lista de precios que cubra esa fecha en el tiempo real de ventas, ha aislado el problema. Modifique las fechas de inicio y finalización de la lista de precios para asegurarse de que la lista de precios cubre la fecha del tiempo real de ventas. 
    - Si hay varias listas de precios que cubren la fecha en el tiempo real de ventas, ha aislado el problema. Puede solucionarlo editando las fechas de inicio y finalización de la lista o listas de precios de modo que haya sólo una lista de precios que cubra la fecha del tiempo real de ventas. 
    - Si solo hay una lista de precios que cubre esa fecha del tiempo real de ventas, pase a la Comprobación 3.
Cuando termine de hacer las correcciones necesarias, vuelva a crear una entrada de tiempo, apruébela, y compruebe que el tiempo real de ventas muestra un precio válido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Comprobación 3: ¿Existe un precio en la lista de precios para las dimensiones de precios en el tiempo real de ventas?

Si ha completado correctamente la Comprobación 1 y la Comprobación 2, ahora debe tener únicamente una lista de precios que es aplicable al tiempo real de ventas. Abra esta Lista de precios y vaya a la pestaña Precios de rol. Asegúrese de que hay una fila en la cuadrícula para las dimensiones de precios en el tiempo real de ventas.

Si no hay ninguna fila en la cuadrícula de precios de rol para las dimensiones de precios en el tiempo real de ventas, ha aislado el problema. Cree una fila en la cuadrícula Precios de rol para las dimensiones de precios en el tiempo real de ventas. Cuando termine, vuelva a crear una entrada de tiempo, apruébela, y compruebe que el tiempo real de ventas muestra un precio válido.

Si aún no ve un precio válido en tiempo real de ventas después de seguir las tres comprobaciones anteriores, registre un vale de soporte. 

