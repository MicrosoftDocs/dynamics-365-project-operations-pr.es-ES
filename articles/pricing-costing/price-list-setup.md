---
title: Configurar listas de precios
description: En este tema se proporciona información sobre cómo configurar las listas de precios de costes y ventas.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 227e9a6f0ce6fd3fa1c2b0bd9afa014a3ec4f9758ead0dfb408156535692575c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009507"
---
# <a name="set-up-price-lists"></a>Configurar listas de precios

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Listas de precios en Dynamics 365 Project Operations representan un catálogo de tarifas. Las tarifas expresan costos, ventas y tarifas de facturación. Dependiendo de si la lista de precios expresa tarifas de costo o tarifas de ventas y facturación, el contexto de la lista de precios es **Ventas** o **Coste**.

Las siguientes extensiones son específicas de Project Operations y se aplican a las listas de precios de Dynamics 365 Sales.

- **Contexto**: este campo tiene los valores admitidos, **Costo** y **Ventas**. El valor **Compra** no se admite. Establezca el contexto a **Costo** para hacer una lista de precios de costo o establecer el contexto para **Ventas** para una lista de precios de venta. Las listas de precios de coste resuelven el precio del tipo de coste en los registros de estimaciones y de datos reales. Las listas de precios de venta resuelven el precio en registros estimados y reales de tipos de ventas facturadas y no facturadas.
- **Unidad de tiempo**: esta es la unidad de tiempo predeterminada para la que se configura el precio en la tabla **Precio del rol** para esta lista de precios.
- **Entidad de lista de precios** : este campo oculto es para que Project Operations pueda diferenciar las listas de precios que son cotizadas o específicas del contrato de aquellas que son estándar y aplicables globalmente.

## <a name="price-list-header"></a>Encabezado de lista de precios

La siguiente tabla incluye los campos en la pestaña **General** de una lista de precios que son exclusivos de Project Operations o que tienen cambios significativos en el comportamiento de las listas de precios en Sales.

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| Nombre | Pestaña **General** y formularios **Creación rápida** | La identidad de la lista de precios. | La lista de precios se muestra con este valor en todas las páginas de lista y opciones desplegables.|
| Contexto | Pestaña **General** y formularios **Creación rápida** | Este campo se puede establecer en **Coste** o **Ventas**. | Una lista de precios establecida en **Coste** se utiliza para buscar el precio de las estimaciones de costes y los costes reales. Una lista de precios establecida en **Ventas** se utiliza para buscar el precio de las estimaciones de ventas y las ventas reales. Solo las listas de precios que tienen el contexto establecido en **Ventas** se puede adjuntar a listas de precios de proyectos para clientes, cotizaciones de proyectos y contratos de proyectos. |
| Fecha de inicio | Pestaña **General** y formularios **Creación rápida** | La fecha de inicio del período en el que entra en vigor la lista de precios. | Con el campo **Fecha final**, este campo se utiliza para determinar qué lista de precios es aplicable para una determinada estimación o línea real. |
| Fecha de finalización | Pestaña **General** y formularios **Creación rápida** | La fecha de finalización del período en el que entra en vigor la lista de precios. | Con el campo **Fecha de inicio**, este campo se utiliza para determinar qué lista de precios es aplicable para una determinada estimación o línea real. |
| Divisa | Pestaña **General** y formularios **Creación rápida** | Este campo se utiliza para predeterminar la moneda en cada rol, categoría o línea de artículo de lista de precios relacionada con esta lista de precios. | En las listas de precios de **Ventas**, los roles, las categorías o las líneas de artículos de la lista de precios no se pueden crear en ninguna moneda que no sea esta. En la lista de precios de **Coste** puede crear una línea de precios de rol en cualquier moneda. La moneda definida aquí se utiliza por defecto. La configuración del usuario que está relacionada con los precios de los roles puede anular este valor para permitir la configuración de la tasa de coste de mano de obra en cualquier moneda. Las tasas de coste de la categoría y los costes de los artículos de la lista de precios se pueden configurar solo en la moneda definida aquí. |
| Unidad de tiempo | Pestaña **General** y formularios **Creación rápida** | Este campo se utiliza para predeterminar la unidad de tiempo en cada línea de rol relacionada con esta lista de precios. | Este valor de campo solo se utiliza en la configuración de precio de función relacionada. En la lista de precios de **Coste** y **Ventas** puede crear una línea de precios de rol en cualquier unidad de tiempo. La unidad de tiempo definida aquí se utiliza por defecto. La configuración del usuario que está relacionada con los precios de los roles puede anular este valor para permitir la configuración de costes laborales y tasa de facturación en cualquier unidad de tiempo. |
| Descripción | Pestaña **General** y formularios **Creación rápida** | Este campo de texto le permite proporcionar una descripción de varias líneas de la lista de precios. | Este campo se muestra en las vistas **Asociado** sobre la lista de precios en varias entidades que tienen listas de precios relacionadas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]