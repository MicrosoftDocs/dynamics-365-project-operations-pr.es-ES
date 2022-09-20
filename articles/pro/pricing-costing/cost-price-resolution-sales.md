---
title: Determinar tasas de costes para estimaciones y datos reales de proyectos
description: Este artículo proporciona información sobre cómo se determinan los precios de tasas de costes en las estimaciones y los datos reales del proyecto.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475257"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Determinar tasas de costes para estimaciones y datos reales de proyectos

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Para determinar las tarifas de coste en estimaciones y datos reales se resuelven en Microsoft Dynamics 365 Project Operations, el sistema utiliza primero la fecha y la moneda en el contexto estimado o real entrante para determinar la lista de precios de coste. Específicamente en el contexto actual, el sistema utiliza el campo **Fecha de transacción** para determinar qué lista de precios es aplicable. El valor de **Fecha de la transacción** de la estimación entrante o real se compara con los valores de **Fecha de inicio efectiva (independiente de la zona horaria)** y **Fecha de finalización efectiva (independiente de la zona horaria)** de la lista de precios. Una vez determinada la lista de precios de coste, el sistema determina la tasa de coste. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinar las tasas de coste en contextos estimados y reales por tiempo

Estimar contexto por **tiempo** se refiere a:

- Detalles de línea de oferta por **tiempo**.
- Detalles de línea de contrato por **tiempo**.
- Asignaciones de recursos en un proyecto.

Contexto real por **tiempo** se refiere a:

- Líneas de diario de entrada y corrección para **tiempo**.
- Líneas de diario que se crean cuando se envía una entrada de tiempo.

Después de que se determine una lista de precio de coste, el sistema completa los siguientes pasos para introducir una tasa de coste predeterminada.

1. El sistema hace coincidir la combinación de los campos **Rol** y **Unidad de dotación de recursos** en el contexto estimado o real por **tiempo** frente a las líneas de precio del rol en la lista de precios. Para esta coincidencia se supone que utiliza las dimensiones de precios estándar para el coste de mano de obra. Si ha configurado el sistema para hacer coincidir campos en lugar de, o además de **Rol** y **Unidad de recursos**, se utilizará una combinación distinta para recuperar una línea de precio de función coincidente.
1. Si el sistema encuentra una línea de precio de rol que tiene una tarifa de coste para la combinación de campos **Rol** y **Unidad de dotación de recursos**, esa tasa de coste se usa como predeterminada.
1. Si el sistema no puede igualar los valores de campo **Rol** y **Unidad de dotación de recursos**, entonces recupera líneas de precio con valores coincidentes para el campo **Rol**, pero valores nulos para el campo **Unidad de dotación de recursos**. Una vez que el sistema ha encontrado un registro de precio de función coincidente, la tasa de coste de ese registro se usará como predeterminada.

> [!NOTE]
> Si configuró una priorización diferente de los campos **Rol** y **Unidad de recursos**, o si tiene otras dimensiones que tienen mayor prioridad, este comportamiento precedente cambiará en consecuencia. El sistema recupera registros de precios de roles que tienen valores que coinciden con cada valor de dimensión de precios en orden de prioridad. Las filas que tienen valores nulos para esas dimensiones van en último lugar.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinar las tasas de coste en líneas reales y estimadas por gasto

Estimar contexto por **gasto** se refiere a:

- Detalles de línea de oferta por **gasto**.
- Detalles de línea de contrato por **gasto**.
- Estimaciones de gastos en un proyecto.

Contexto real por **gasto** se refiere a:

- Líneas de diario de entrada y corrección para **gasto**.
- Líneas de diario que se crean cuando se envía una entrada de gasto.

Después de que se determine una lista de precio de coste, el sistema completa los siguientes pasos para introducir una tasa de coste predeterminada.

1. El sistema hace coincidir la combinación de los campos **Categoría** y **Unidad** en el contexto estimado o real por **gasto** frente a las líneas de precio de la categoría en la lista de precios.
1. Si el sistema encuentra una línea de precio de categoría que tiene una tarifa de coste para la combinación de **Categoría** y **Unidad**, esa tasa de coste se usa como predeterminada.
1. Si el sistema no puede coincidir con los valores **Categoría** y **Unidad**, el precio se establece en **0** (cero) de forma predeterminada.
1. En el contexto de estimación, si el sistema no encuentra una línea de precios de categoría coincidente, pero el método de cálculo de precios es otro que no sea **Precio por unidad**, la tasa de coste se establece en **0** (cero) de forma predeterminada.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinar tasas de coste en líneas de datos reales y estimados para materiales

Estimar contexto por **material** se refiere a:

- Detalles de línea de oferta por **material**.
- Detalles de línea de contrato por **material**.
- Estimaciones de materiales en un proyecto.

Contexto real por **material** se refiere a:

- Líneas de diario de entrada y corrección para **material**.
- Líneas de diario que se crean cuando se envía un registro de uso de materiales.

Después de que se determine una lista de precio de coste, el sistema completa los siguientes pasos para introducir una tasa de coste predeterminada.

1. El sistema usa la combinación de los campos **Producto** y **Unidad** en el contexto estimado o real por **material** frente a los elementos de lista de precios en la lista de precios.
1. Si el sistema encuentra un elemento de lista de precios que tiene una tarifa de coste para la combinación de **Producto** y **Unidad**, esa tasa de coste se usa como predeterminada.
1. Si el sistema no puede coincidir con los valores **Producto** y **Unidad**, el coste unitario se establece en **0** (cero) de forma predeterminada.
1. En el contexto de estimación o real, si el sistema no encuentra un elemento de lista de precios coincidente, pero el método de cálculo de precios es otro que no sea **Importe de divisa**, el coste unitario se establece en **0** de forma predeterminada. Este comportamiento se produce porque Project Operations solo admite el método de cálculo de precios **Importe de divisa** para los materiales que se utilizan en un proyecto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
