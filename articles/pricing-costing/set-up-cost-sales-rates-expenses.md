---
title: Configurar tarifas de costes y ventas para gastos
description: Este artículo proporciona información sobre cómo configurar costos y tarifas de ventas para categorías de transacciones y gastos.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c503230348750af246f6ee7a4af1176d7bf22ba4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911893"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Configurar tarifas de costes y ventas para gastos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede configurar el costo y los precios de venta para las categorías de transacciones en Dynamics 365 Project Operations. Debido a que los precios de coste y venta están diseñados para Gastos, cada categoría de transacción que los incluya también debe configurarse como una categoría de gastos. Esta configuración garantiza la precisión en la funcionalidad posterior. Los precios de coste y venta para las categorías de transacciones solo se pueden enumerar en una moneda, que debe ser la moneda en el encabezado de la lista de precios.

Para configurar las tarifas de costes y ventas para las categorías de transacciones, complete los siguientes pasos. 

1. Vaya a **Ventas** > **Clientes** > **Lista de precios**.
2. Seleccione **Nuevo** para crear una nueva lista de precios. 
3. En **Precios de categoría**, en el menú de la subcuadrícula, seleccione **Precio de nueva categoría**. 
4. En la página **Creación rápida**, ingrese la categoría de transacción y la unidad para la que está creando el nuevo precio.

La siguiente tabla muestra los campos en la pestaña **General** y la página **Creación rápida** de una categoría de línea de precio que debería recordar a medida que crea categorías de precios en una lista de precios de ventas o costes.

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| Categoría de transacción | Pestaña **General** y páginas **Creación rápida** | Seleccione la categoría de transacción para la que está creando un precio de venta o de costo. | La categoría de transacción en la estimación entrante o real para Gastos se comparará con esta línea para predeterminar la tarifa de coste o ventas de la categoría de transacción. |
| Programación de unidad | Pestaña **General** y páginas **Creación rápida** | La programación unitaria se predetermina a la programación unitaria de la categoría de transacción. | No hay impacto posterior a partir de este campo. |
| Unidad | Pestaña **General** y páginas **Creación rápida** | Seleccione la unidad para la que se están configurando las tarifas. | La unidad en la estimación entrante o real se compara con la unidad en esta línea para establecer la tasa predeterminada en la estimación de gastos o real. |
| Método de cálculo de precios | Pestaña **General** y páginas **Creación rápida** | Posibles valores del campo **Método de cálculo de precios** son, **Precio por unidad**, **A un coste** y **Margen de beneficio sobre el coste**. | Durante la configuración del precio, seleccionando **Precio por unidad** bloquea el campo **Porcentaje** en la línea de precio de categoría. Si **A un coste** está seleccionado, los campos **Precio** y **Porcentaje** están bloqueados en la lista de precios de venta. Seleccionar **Margen de beneficio sobre el coste** bloquea el campo **Precio** en la lista de precios de venta. En una línea real entrante para gastos, el método de cálculo de precios **A un coste** o **Margen de beneficio sobre el coste** da como resultado que a la línea de ventas no facturada correspondiente se le asigne un precio que sea igual al precio sobre el costo real o se calcule como un margen de beneficio sobre el precio. |
| Precio | Pestaña **General** y páginas **Creación rápida** | Configure una tasa por unidad para la categoría de transacción y la combinación de unidades. Por ejemplo, la tasa de kilometraje es 10 USD por milla y 8 USD por kilómetro. | La tasa de kilometraje será la tasa que se establece por defecto en el precio por unidad o coste del estimado entrante o línea actual de una clase de transacción de gastos.|
| Porcentaje | Pestaña **General** y páginas **Creación rápida** | Configure un porcentaje sobre coste para la categoría de transacción y la combinación de unidades. Por ejemplo, la tarifa de venta de pasajes aéreos debe marcarse un 10 por ciento sobre el costo del gasto del pasaje aéreo incurrido. | Este porcentaje de incremento por encima del coste solo es aplicable en una lista de precios de ventas cuando el método de cálculo de precios seleccionado es **Margen de beneficio sobre coste**. |
| Divisa | Pestaña **General** y páginas **Creación rápida** | De forma predeterminada, este valor proviene de la moneda en el encabezado de la lista de precios. Para los precios de la categoría de transacción, la moneda no se puede anular. | Esta moneda es la predeterminada en el precio por unidad de la línea actual de la clase de transacción de gastos para costes y ventas. |

## <a name="pricing-methods-for-expenses"></a>Métodos de cálculos de precios de gastos

Cuando configura precios de categoría que solo son relevantes en el contexto de precios de gastos, puede utilizar uno de los siguientes tres métodos de precios:

- **Precio unitario**
- **De coste**
- **Margen de beneficio sobre el coste**

### <a name="price-per-unit"></a>Precio unitario
Cuando se selecciona este método de precios en una línea de precios de categoría que está vinculada a una lista de precios de venta, el precio predeterminado para la combinación de categoría y unidad tanto en la estimación como en el real. La estimación se refiere a las líneas de estimación del proyecto para los gastos, el detalle de la línea de cotización y el detalle de la línea del contrato para los gastos.

### <a name="at-cost"></a>De coste
Cuando se selecciona este método de precios en la línea de precios de categoría que está vinculada a una lista de precios de venta, el precio predeterminado para la combinación de categoría y unidad es solo para los gastos reales. Por ejemplo, datos reales de ventas no facturadas para la clase de transacción de gastos. El precio unitario se establece sobre las ventas reales no facturadas del precio unitario sobre el coste real de dicho gasto. El precio predeterminado basado en el costo no se realiza en las estimaciones del proyecto para los gastos o en los detalles de la línea de cotización y del contrato para los gastos.

### <a name="markup-over-cost"></a>Margen de beneficio sobre el coste
Cuando se selecciona este método de precios en la línea de precios de categoría que está vinculada a una lista de precios de venta, el precio predeterminado para la combinación de categoría y unidad es solo para un gasto real. Por ejemplo, datos reales de ventas no facturadas para la clase de transacción de gastos. Este precio unitario se establece sobre las ventas no facturadas reales a un valor calculado a partir del precio unitario sobre el costo real de ese gasto después de que se aplica el porcentaje de margen definido. El precio predeterminado basado en el costo no se realiza en las estimaciones del proyecto para los gastos o en los detalles de la línea de cotización y del contrato para los gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
