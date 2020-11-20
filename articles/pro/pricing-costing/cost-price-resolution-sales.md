---
title: Resolver precios de coste en estimaciones y datos reales (lite)
description: Este tema proporciona información sobre cómo se resuelven los precios de venta en estimaciones y reales.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176812"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Resolver precios de coste en estimaciones y datos reales (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Para resolver los precios de coste y la lista de precios de coste para estimaciones y reales, el sistema utiliza la información en los campos **Fecha**, **Moneda** y **Unidad de contratación** del proyecto relacionado. Una vez resuelta la lista de precios de coste, la aplicación resuelve la tasa de coste.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resuelva las tasas de coste en líneas reales y estimadas por tiempo

Las líneas de estimación de tiempo se refieren a los detalles de la línea de cotización y contrato para las asignaciones de tiempo y recursos en un proyecto.

Después de que la lista de precios de coste se resuelva, el sistema utiliza los campos **Rol** y **Unidad de recursos** en la línea de estimación para el tiempo, para que coincida con las líneas de precio de función en la lista de precios resuelta. Esta coincidencia supone que está utilizando dimensiones de precios listas para usar de los costes laborales. Si ha configurado el sistema para hacer coincidir campos en lugar de, o además de **Rol** y **Unidad de recursos**, entonces se utilizará una combinación distinta para recuperar una línea de precio de función coincidente. Si la aplicación encuentra una línea de precio de rol que tiene una tarifa de coste para la combinación de campos **Rol** y **Unidad de recursos**, entonces esa tarifa de factura se establece por defecto. Si la aplicación no puede hacer coincidir los valores de **Rol** y **Unidad de recursos**, entonces recupera líneas de precio de función con una función coincidente pero valores nulos de **Unidad de recursos**. Una vez que tiene un registro de precio de función coincidente, la tasa de coste se establece por defecto en ese registro. 

> [!NOTE]
> Si configuró una priorización diferente de **Rol** y **Unidad de recursos**, o si tiene otras dimensiones que tienen mayor prioridad, este comportamiento cambiará en consecuencia. El sistema recupera los registros de precio de función con valores coincidentes de cada uno de los valores de dimensión de precios en el orden de prioridad con filas que tienen valores nulos para esas dimensiones en último lugar.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resuelva las tasas de coste en líneas reales y estimadas por gasto

Las líneas de estimación para gasto se refieren a los detalles de la línea de cotización y contrato para gastos y las líneas de estimación de gastos de un proyecto.

Después de que la lista de precios de coste se resuelva, el sistema usa una combinación de los campos los campos **Categoría** y **Unidad** en la línea de estimación para el gasto, para que coincida con las líneas de **Categoría de precio** en la lista de precios resuelta. Si el sistema encuentra una línea de precio de categoría que tiene una tarifa de coste para la combinación de campos **Categoría** y **Unidad**, entonces esa tarifa de coste se establece por defecto. Si el sistema no puede hacer coincidir los valores **Categoría** y **Unidad**, o si puede encontrar una línea de precio de categoría coincidente pero el método de fijación de precios no es **Precio por unidad**, la tasa de costo se establece por defecto en cero (0).
