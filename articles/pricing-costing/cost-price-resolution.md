---
title: Resolución de precios de coste para estimaciones y datos reales
description: Este tema proporciona información sobre cómo se resuelven los precios de venta en estimaciones y reales.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d81b521acbfd97127cf056bd41a3249c01108374
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001402"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Resolución de precios de coste para estimaciones y datos reales

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Para resolver los precios de coste y la lista de precios de coste para estimaciones y reales, el sistema utiliza la información en los campos **Fecha**, **Moneda** y **Unidad de contratación** del proyecto relacionado. Una vez resuelta la lista de precios de coste, la aplicación resuelve la tasa de coste.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resuelva las tasas de coste en líneas reales y estimadas por tiempo

Las líneas de estimación de tiempo se refieren a los detalles de la línea de cotización y contrato para las asignaciones de tiempo y recursos en un proyecto.

Después de que la lista de precios de coste se resuelva, el sistema utiliza los campos **Rol**, **Compañía de recursos** y **Unidad de recursos** en la línea de estimación para el tiempo, para que coincida con las líneas de precio de función en la lista de precios resuelta. Esta coincidencia supone que está utilizando dimensiones de precios listas para usar de los costes laborales. Si ha configurado el sistema para hacer coincidir campos en lugar de, o además de **Rol**, **Compañía de recursos** y **Unidad de recursos**, entonces se utilizará una combinación distinta para recuperar una línea de precio de función coincidente. Si la aplicación encuentra una línea de precio de rol que tiene una tarifa de coste para la combinación de campos **Rol**, **Compañía de recursos** y **Unidad de recursos**, entonces esa tarifa de factura se establece por defecto. Si la aplicación no puede coincidir exactamente con la combinación de valores **Rol**, **Empresa de dotación de recursos**, y **Unidad de dotación de recursos**, recuperará líneas de precio de rol con un valor de rol coincidente, pero tendrá valores nulos para **Unidad de dotación de recursos** y **Empresa de dotación de recursos**. Una vez que se encuentra un registro de precio de rol coincidente con un valor de precio de rol coincidente, la tasa de coste toma los valores predeterminados de ese registro. 

> [!NOTE]
> Si configura una priorización diferente de **Rol**, **Compañía de recursos** y **Unidad de recursos**, o si tiene otras dimensiones que tienen mayor prioridad, este comportamiento cambiará en consecuencia. El sistema recupera registros de precios de rol con valores que coinciden con cada uno de los valores de dimensión de precios en orden de prioridad con filas que tienen valores nulos para aquellas dimensiones que ocupan las últimas posiciones en el orden de prioridad.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resuelva las tasas de coste en líneas reales y estimadas por gasto

Las líneas de estimación para gasto se refieren a los detalles de la línea de cotización y contrato para gastos y las líneas de estimación de gastos de un proyecto.

Después de que la lista de precios de coste se resuelva, el sistema usa una combinación de los campos los campos **Categoría** y **Unidad** en la línea de estimación para el gasto, para que coincida con las líneas de **Categoría de precio** en la lista de precios resuelta. Si el sistema encuentra una línea de precio de categoría que tiene una tarifa de coste para la combinación de campos **Categoría** y **Unidad**, entonces esa tarifa de coste se establece por defecto. Si el sistema no puede hacer coincidir los valores **Categoría** y **Unidad**, o si puede encontrar una línea de precio de categoría coincidente pero el método de fijación de precios no es **Precio por unidad**, la tasa de costo se establece por defecto en cero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolución de tasas de coste en líneas de datos reales y estimados para materiales

Las líneas de estimación de material se refieren a los detalles de la línea de cotización y contrato para materiales y las líneas de estimación de material en un proyecto.

Una vez resuelta una lista de precios de coste, el sistema utiliza una combinación de los campos **Producto** y **Unidad** en la línea de estimación para que una estimación de material coincida con las líneas **Elementos de lista de precios** en la lista de precios resuelta. Si el sistema encuentra una línea de precio de producto que tiene una tasa de coste para la combinación de los campos **Producto** y **Unidad**, la tasa de coste es toma los valores predeterminados. Si el sistema no puede coincidir con los valores **Producto** y **Unidad**, el coste unitario pasa al valor predeterminado de cero. Este valor predeterminado también se tomará si hay un elemento de lista de precios coincidente, pero el método de fijación de precios se basa en un coste estándar o coste actual que no está definido en el producto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
