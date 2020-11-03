---
title: Estimaciones de recursos
description: En este tema se proporciona información sobre cómo se calculan las estimaciones de recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085068"
---
# <a name="resource-estimates"></a>Estimaciones de recursos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las estimaciones de recursos provienen del esfuerzo por fases que se define en la estructura de descomposición del trabajo, junto con las dimensiones de precios aplicables. Normalmente, el cálculo es **tarifa/hora para cada rol x horas.** El esfuerzo por fases de tiempo para cada recurso se almacena en el registro de asignación de recursos. El precio se almacena en una lista de precios predefinida. La conversión de unidades se aplica según la lista de precios aplicable.

![Estimaciones de recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Valores predeterminados de precio y divisa de coste

Los precios de coste se predeterminan desde la unidad organizativa.

## <a name="default-bill-rate-and-sales-currency"></a>Tarifa de facturación y divisa de ventas predeterminadas

Los precios de venta se aplican una vez por oferta. La jerarquía para la lista de precios de venta predeterminada es la siguiente:

1. Organización
2. Cliente
3. Oferta/contrato
