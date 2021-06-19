---
title: Estimaciones financieras del tiempo de los recursos en proyectos
description: Este tema proporciona información sobre cómo se calculan las estimaciones financieras para el tiempo.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010807"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Estimaciones financieras del tiempo de los recursos en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las estimaciones financieras para el tiempo se calculan en función de tres factores: 

- El tipo de miembro de equipo genérico o con nombre asignado a cada tarea de nodo hoja en el plan del proyecto. 
- El tipo o complejidad del trabajo.
- La extensión del esfuerzo para la asignación del recurso en la tarea. 

Los dos primeros factores influyen en el costo unitario o la tarifa de facturación de la asignación de un recurso. El coste unitario o la tarifa de facturación de una asignación de recursos está determinado por los atributos del recurso asignado. Estos atributos incluyen la unidad organizativa a la que pertenece el recurso y la función estándar del recurso. También puede agregar atributos personalizados relevantes para su negocio para el recurso, como título estándar o nivel de experiencia, y hacer que influyan en el coste unitario o la tarifa de facturación de la asignación.
Además de los atributos del recurso, los atributos del trabajo, como la tarea, también pueden influir en la tasa de facturación unitaria o la tasa de coste de la asignación. Por ejemplo, cuando ciertas tareas son más complejas, la asignación del recurso a esas tareas específicas da como resultado un coste unitario o una tasa de facturación más alta que las tareas que son menos complejas.   

El tercer factor proporciona la cantidad de horas con esa tarifa. En los casos en que una tarea cubra dos períodos de precio, es probable que la primera parte de la asignación de recursos para esa tarea tenga un coste y un precio diferente al de la segunda parte de la tarea. La estimación del esfuerzo en cada asignación de recursos es un valor complejo almacenado con la distribución diaria del esfuerzo por día.

Para obtener instrucciones detalladas sobre cómo configurar atributos personalizados de trabajo y recursos como dimensiones de precios y costes, consulte [Descripción general de las dimensiones de precios](../pricing-costing/pricing-dimensions-overview.md).

La estimación financiera de cada asignación de recursos se calcula como **tasa/hora para la tarea multiplicada por el número de horas**.  De forma similar a la estimación del esfuerzo, la estimación financiera de costes e ingresos para cada asignación de recursos es un valor complejo almacenado con la distribución diaria del importe en divisa por día. 

## <a name="summarizing-financial-estimates-for-time"></a>Resumir la estimaciones financieras por tiempo
Una estimación financiera del tiempo en una tarea de nodo hoja es la suma de las estimaciones financieras de todas las asignaciones de recursos para esa tarea.

Una estimación financiera del tiempo en una tarea de resumen o principal es la suma de las estimaciones financieras de todas sus tareas secundarias. Este es el coste laboral estimado en el proyecto. 

![Estimaciones de recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Valores predeterminados de precio y divisa de coste

El precio de coste predeterminado proviene de las listas de precios adjuntas a la unidad de contratación del proyecto. La divisa de coste de proyecto es siempre la divisa de la unidad contratante del proyecto. En una asignación de recursos, la estimación financiera del coste se almacena en la moneda de coste del proyecto. A veces, la divisa en la que se configura la tasa de coste en la lista de precios es diferente de la divisa de coste del proyecto. En estos casos, la aplicación convierte la divisa en la que se configura el precio de coste para la divisa del proyecto. En la cuadrícula **Estimaciones**, todas las estimaciones de costes se muestran y resumen en la divisa de coste del proyecto. 

## <a name="default-bill-rate-and-sales-currency"></a>Tarifa de facturación y divisa de ventas predeterminadas

El precio de venta predeterminado proviene de las listas de precios del proyecto adjuntas al contrato del proyecto relacionado si se cierra la operación comercial, o de la cotización del proyecto relacionado si la operación aún se encuentra en la etapa de preventa. La divisa de venta del proyecto es siempre la divisa de la cotización del proyecto o el contrato del proyecto. En una asignación de recursos, la estimación financiera de la venta se almacena en la divisa de venta del proyecto. A diferencia del coste, el precio de venta que se establece en la lista de precios nunca puede ser diferente de la divisa de venta del proyecto. No hay ningún escenario en el que sea necesario convertir la divisa. En la cuadrícula **Estimaciones**, todas las estimaciones de ventas se muestran y resumen en la divisa de venta del proyecto. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
