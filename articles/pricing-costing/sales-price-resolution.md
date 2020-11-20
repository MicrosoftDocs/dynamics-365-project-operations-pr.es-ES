---
title: Resolver precios de venta para estimaciones y datos reales
description: Este tema proporciona información sobre cómo se resuelven las tarifas de ventas en estimaciones y reales.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119574"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Resolver precios de venta para estimaciones y datos reales

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Cuando los precios de venta en estimaciones y reales se resuelven en Dynamics 365 Project Operations, el sistema primero usa la fecha y moneda de la cotización o contrato del proyecto relacionado para resolver la lista de precios de venta. Una vez resuelta la lista de precios de venta, el sistema resuelve la tarifa de venta o factura.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Resuelva las tasas de ventas en líneas reales y estimadas por tiempo

En Project Operations, las líneas de estimación de tiempo se utilizan para indicar la línea de cotización y los detalles de la línea de contrato para el tiempo y las asignaciones de recursos en el proyecto.

Después de que se resuelve una lista de precios para las ventas, el sistema completa los siguientes pasos para establecer la tarifa de facturación predeterminada.

1. El sistema utiliza los campos **Rol** y **Compañía de recursos** y **Unidad de recursos** en la línea de estimación para el tiempo, para que coincida con las líneas de precio de función en la lista de precios resuelta. Esta coincidencia supone que se están utilizando dimensiones de precios listas para usar para las tarifas de facturación. Si ha configurado precios basados en cualquier otro campo en lugar de, o además de **Rol**, **Compañía de recursos** y **Unidad de recursos**, esa es la combinación que se utilizará para recuperar una línea de precio de función coincidente.
2. Si el sistema encuentra una línea de precio de rol que tiene una tarifa de factura para la combinación de campos **Rol** y **Compañía de recursos** y **Unidad de recursos**, entonces esa tarifa de factura se establece por defecto.
3. Si el sistema no puede igualar los valores de campo **Rol**, **Compañía de recursos** y **Unidad de recursos**, entonces recupera líneas de precio de función con una función coincidente pero valores nulos de **Unidad de recursos**. Una vez que el sistema encuentra un registro de precio de función coincidente, establecerá la tarifa de facturación predeterminada de ese registro. Esta coincidencia asume una configuración lista para usar para la prioridad relativa de **Rol** vs **Unidad de recursos** como una dimensión de precios de venta.

> [!NOTE]
> Si configuró una priorización diferente de **Rol**, **Compañía de recursos** y **Unidad de recursos**, o si tiene otras dimensiones que tienen mayor prioridad, este comportamiento cambiará en consecuencia. El sistema recupera los registros de precio de función con valores coincidentes de cada uno de los valores de dimensión de precios en el orden de prioridad con filas que tienen valores nulos para esas dimensiones en último lugar.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Resuelva las tasas de ventas en líneas reales y estimadas por gasto

En Project Operations, las líneas de estimación de gasto se utilizan para indicar la línea de cotización y los detalles de la línea de contrato para los gastos y las líneas de estimaciones de gastos en el proyecto.

Después de que se resuelve una lista de precios para las ventas, el sistema completa los siguientes pasos para establecer el precio de venta por unidad.

1. El sistema utiliza la combinación de los campos **Categoría** y **Unidad de recursos** en la línea de estimación para el gasto, contra las líneas de precio de categoría en la lista de precios que se ha resuelto.
2. Si el sistema encuentra una línea de precio de categoría que tiene una tarifa de ventas para la combinación de campos **Categoría** y **Unidad**, entonces esa tarifa de ventas se establece por defecto.
3. Si el sistema encuentra una línea de precio de categoría coincidente, el método de fijación de precios se puede utilizar para predeterminar el precio de venta. La tabla siguiente muestra el comportamiento de incumplimiento del precio de gasto en Project Operations.

    | Contexto | Método de cálculo de precios | Precio predeterminado |
    | --- | --- | --- |
    | Estimación | Precio unitario | Según la línea de precio de la categoría |
    | &nbsp; | De coste | 0.00 |
    | &nbsp; | Margen de beneficio sobre el coste | 0.00 |
    | Real | Precio unitario | Según la línea de precio de la categoría |
    | &nbsp; | De coste | Basado en el coste real relacionado |
    | &nbsp; | Margen de beneficio sobre el coste | Al aplicar un margen según lo definido por la línea de precio de categoría en la tasa de coste unitario del costo real relacionado |

4. Si el sistema no puede emparejar los valores de los campos **Categoría** y **Unidad**, la tasa de ventas predeterminada es cero (0).