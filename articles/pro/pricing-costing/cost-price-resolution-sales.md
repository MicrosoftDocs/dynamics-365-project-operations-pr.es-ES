---
title: Resolver precios de coste en estimaciones y datos reales de proyectos
description: Este tema proporciona información sobre cómo se resuelven los precios de coste en las estimaciones y los datos reales del proyecto.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 94aa1a62ad17fdeb3da8499585ac704b5db75701
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586503"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Resolver precios de coste en estimaciones y datos reales de proyectos 

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Para resolver los precios de coste y la lista de precios de coste para estimaciones y reales, el sistema utiliza la información en los campos **Fecha**, **Moneda** y **Unidad de contratación** del proyecto relacionado. Una vez resuelta la lista de precios de coste, la aplicación resuelve la tasa de coste.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resuelva las tasas de coste en líneas reales y estimadas por tiempo

Las líneas de estimación de tiempo se refieren a los detalles de la línea de cotización y contrato para las asignaciones de tiempo y recursos en un proyecto.

Una vez resuelta una lista de precios de coste, los campos **Rol** y **Unidad de dotación de recursos** de la línea de estimación de Tiempo se comparan con las líneas de precios de rol en la lista de precios. Para esta coincidencia se supone que utiliza las dimensiones de precios estándar para el coste de mano de obra. Si ha configurado el sistema para hacer coincidir campos en lugar de, o además de **Rol** y **Unidad de recursos**, entonces se utilizará una combinación distinta para recuperar una línea de precio de función coincidente. Si la aplicación encuentra una línea de precio de rol que tiene una tarifa de coste para la combinación de campos **Rol** y **Unidad de recursos**, entonces esa tarifa de factura se establece por defecto. Si la aplicación no puede hacer coincidir los valores de **Rol** y **Unidad de recursos**, entonces recupera líneas de precio de función con una función coincidente pero valores nulos de **Unidad de recursos**. Una vez que tiene un registro de precio de función coincidente, la tasa de coste se establece por defecto en ese registro. 

> [!NOTE]
> Si configuró una priorización diferente de **Rol** y **Unidad de recursos**, o si tiene otras dimensiones que tienen mayor prioridad, este comportamiento cambiará en consecuencia. El sistema recupera los registros de precio de función con valores coincidentes de cada uno de los valores de dimensión de precios en el orden de prioridad con filas que tienen valores nulos para esas dimensiones en último lugar.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resuelva las tasas de coste en líneas reales y estimadas por gasto

Las líneas de estimación para gasto se refieren a los detalles de la línea de cotización y contrato para gastos y las líneas de estimación de gastos de un proyecto.

Una vez resuelta una lista de precios de coste, el sistema utiliza una combinación de los campos **Categoría** y **Unidad** en la línea de estimación de gasto para buscar una coincidencia en las líneas de **Precio de categoría** de la lista de precios resuelta. Si el sistema encuentra una línea de precio de categoría que tiene una tarifa de coste para la combinación de campos **Categoría** y **Unidad**, entonces esa tarifa de coste se establece por defecto. Si el sistema no encuentra coincidencias de los valores de **Categoría** y **Unidad**, o si encuentra una línea de precio de categoría coincidente pero el método de cálculo de precios no es **Precio unitario**, la tasa de coste predeterminada es cero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolución de tasas de coste en líneas de datos reales y estimados para materiales

Las líneas de estimación de material se refieren a los detalles de la línea de cotización y contrato para materiales y las líneas de estimación de material en un proyecto.

Una vez resuelta una lista de precios de coste, el sistema utiliza una combinación de los campos **Producto** y **Unidad** en la línea de estimación para que una estimación de material coincida con las líneas **Elementos de lista de precios** en la lista de precios resuelta. Si el sistema encuentra una línea de precio de producto que tiene una tasa de coste para la combinación de los campos **Producto** y **Unidad**, la tasa de coste es toma los valores predeterminados. Si el sistema no puede hacer coincidir los valores **Producto** y **Unidad** o si puede encontrar una un elemento de lista de precios coincidente pero el método de fijación de precios se basa en el coste estándar o el coste actual y ninguno está definido en el producto, el coste unitario tomar el valor predeterminado de cero.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
