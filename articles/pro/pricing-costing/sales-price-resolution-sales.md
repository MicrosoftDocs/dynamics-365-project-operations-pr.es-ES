---
title: Determinar precios de venta para estimaciones y datos reales de proyectos
description: Este artículo proporciona información sobre cómo se determinan los precios de ventas en las estimaciones y los datos reales del proyecto.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475206"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Determinar precios de venta para estimaciones y datos reales de proyectos

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Para determinar los precios de venta en estimaciones y reales se resuelven en Microsoft Dynamics 365 Project Operations, el sistema utiliza primero la fecha y la moneda en el contexto estimado o real entrante para determinar la lista de precios de ventas. Específicamente en el contexto actual, el sistema utiliza el campo **Fecha de transacción** para determinar qué lista de precios es aplicable. El valor de **Fecha de la transacción** de la estimación entrante o real se compara con los valores de **Fecha de inicio efectiva (independiente de la zona horaria)** y **Fecha de finalización efectiva (independiente de la zona horaria)** de la lista de precios. Una vez determinada la lista de precios de venta, el sistema determina la tarifa de venta o factura.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Determinar las tasas de ventas en líneas reales y estimadas por tiempo

Estimar contexto por **tiempo** se refiere a:

- Detalles de línea de oferta por **tiempo**.
- Detalles de línea de contrato por **tiempo**.
- Asignaciones de recursos en un proyecto.

Contexto real por **tiempo** se refiere a:

- Líneas de diario de entrada y corrección para **tiempo**.
- Líneas de diario que se crean cuando se envía una entrada de tiempo.
- Detalles de línea de factura por **tiempo**. 

Después de que se determine una lista de precios para las ventas, el sistema completa los siguientes pasos para introducir la tarifa de factura predeterminada.

1. El sistema hace coincidir la combinación de los campos **Rol** y **Unidad de dotación de recursos** en el contexto estimado o real por **tiempo** frente a las líneas de precio del rol en la lista de precios. Esta coincidencia supone que se están utilizando dimensiones de precios listas para usar para las tarifas de facturación. Si ha configurado precios para que se basen en campos en lugar de, o además de **Rol** y **Unidad de recursos**, esa es la combinación de campos se utilizará para recuperar una línea de precio de función coincidente.
1. Si el sistema encuentra una línea de precio de rol que tiene una tarifa de factura para la combinación de campos **Rol** y **Unidad de recursos**, entonces esa tarifa de factura se establece por defecto.
1. Si el sistema no puede igualar los valores de campo **Rol** y **Unidad de dotación de recursos**, entonces recupera líneas de precio con valores coincidentes para el campo **Rol**, pero valores nulos para el campo **Unidad de recursos**. Una vez que el sistema encuentra un registro de precio de función coincidente, la tasa de facturación de ese registro se usará como predeterminada. Esta coincidencia asume una configuración lista para usar para la prioridad relativa de **Rol** frente a **Unidad de recursos** como una dimensión de precios de venta.

> [!NOTE]
> Si configuró una priorización diferente de los campos **Rol** y **Unidad de recursos**, o si tiene otras dimensiones que tienen mayor prioridad, este comportamiento precedente cambiará en consecuencia. El sistema recupera registros de precios de roles que tienen valores que coinciden con cada valor de dimensión de precios en orden de prioridad. Las filas que tienen valores nulos para esas dimensiones van en último lugar.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Determinar las tasas de ventas en líneas reales y estimadas por gasto

Estimar contexto por **gasto** se refiere a:

- Detalles de línea de oferta por **gasto**.
- Detalles de línea de contrato por **gasto**.
- Líneas de estimación de gastos en un proyecto.

Contexto real por **gasto** se refiere a:

- Líneas de diario de entrada y corrección para **gasto**.
- Líneas de diario que se crean cuando se envía una entrada de gasto.
- Detalles de línea de factura por **gasto**. 

Después de que se determine una lista de precios para las ventas, el sistema completa los siguientes pasos para introducir el precio de venta unitario predeterminado.

1. El sistema utiliza hace coincidir la combinación de los campos **Categoría** y **Unidad** en la línea de estimación para el **gasto**, contra las líneas de precio de categoría en la lista de precios.
1. Si el sistema encuentra una línea de precio de categoría que tiene una tarifa de ventas para la combinación de **Categoría** y **Unidad**, esa tarifa de ventas se establece por defecto.
1. Si el sistema encuentra una línea de precio de categoría coincidente, el método de cálculo de precios se puede utilizar para introducir el precio de venta predeterminado. La tabla siguiente muestra el comportamiento predeterminado de precio de gasto en Project Operations.

    | Context | Método de cálculo de precios | Precio predeterminado |
    | --- | --- | --- |
    | Estimación | Precio por unidad | Según la línea de precio de la categoría. |
    |        | De coste | 0.00 |
    |        | Margen de beneficio sobre el coste | 0.00 |
    | Real | Precio por unidad | Según la línea de precio de la categoría. |
    |        | De coste | Basado en el coste real relacionado. |
    |        | Margen de beneficio sobre el coste | Se aplica un incremento según lo definido por la línea de precio de categoría en la tasa de coste unitario del costo real relacionado. |

1. Si el sistema no puede coincidir con los valores **Categoría** y **Unidad**, la tasa de ventas se establece en **0** (cero) de forma predeterminada.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Determinar las tasas de coste en líneas de datos reales y estimados para materiales

Estimar contexto por **material** se refiere a:

- Detalles de línea de oferta por **material**.
- Detalles de línea de contrato por **material**.
- Líneas de estimación de materiales en un proyecto.

Contexto real por **material** se refiere a:

- Líneas de diario de entrada y corrección para **material**.
- Líneas de diario que se crean cuando se envía un registro de uso de materiales.
- Detalles de línea de factura por **material**. 

Después de que se determine una lista de precios para las ventas, el sistema completa los siguientes pasos para introducir el precio de venta unitario predeterminado.

1. El sistema hace coincidir la combinación de los campos **Producto** y **Unidad** en la línea de estimación por **material** contra las líneas de elemento de lista de precios en la lista de precios.
1. Si el sistema encuentra elemento de lista de precios que tiene una tasa de venta para la combinación de **Producto** y **Unidad** y, si el método de fijación de precios es **Importe de divisa**, se utiliza el precio de venta que se especifica en la línea de lista de precios. 
1. Si los valores de los campos **Producto** y **Unidad** no coinciden, o si el método de cálculo de precios es diferente a **Importe de divisa**, la tasa de venta se establece en **0** (cero) por defecto. Este comportamiento se produce porque Project Operations solo admite el método de cálculo de precios **Importe de divisa** para los materiales que se utilizan en un proyecto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
