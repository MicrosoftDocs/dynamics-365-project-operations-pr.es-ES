---
title: Copiar listas de precios
description: Este tema proporciona información sobre cómo copiar las listas de precios de productos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67a69d521ac0a5632371138bd4fbb9dd00fe34ee
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181518"
---
# <a name="copy-price-lists"></a>Copiar listas de precios

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede crear copias de listas de precios en Dynamics 365 Project Operations. Por ejemplo, puede crear listas de precios para el próximo año utilizando una lista de precios del año actual.  O puede copiar una lista de precios para las tarifas de facturación y los precios de venta de las listas de precios para el costo. 

Para hacer una copia de la lista de precios, complete los siguientes pasos.

1. Abra la lista de precios de la que desea hacer una copia y seleccione **Copiar**.
2. Ingrese la información necesaria para copiar la lista de precios. La siguiente tabla muestra las consideraciones que se deben tener en cuenta al ingresar información.

| Campo | Descripción | Impacto posterior |
| --- | --- | --- |
| Nombre | El nombre de la lista de precios de origen con el **-copia** adjunto. | La lista de precios incluye este valor en todas las páginas de lista y opciones desplegables. |
| Contexto | Introduzca el contexto que desea para la lista de precios objetivo. | Una lista de precios que tenga el contexto establecido en **Coste** se utiliza para buscar el precio de las estimaciones de costes y los costes reales. Una lista de precios que tiene el contexto establecido en **Ventas** se utiliza para buscar el precio de las estimaciones de ventas y las ventas reales. Solo las listas de precios que tienen el contexto establecido en **Ventas** se puede adjuntar a listas de precios de un proyecto para un cliente, cotizaciones o contrato. |
| Fecha de inicio | La fecha de inicio del período en el que entra en vigor la lista de precios. | Junto con **Fecha final**, este campo se utiliza para determinar qué lista de precios es aplicable para una determinada estimación o línea real. |
| Fecha de finalización | La fecha de finalización del período en el que entra en vigor la lista de precios. | Junto con **Fecha inicial**, este campo se utiliza para determinar qué lista de precios es aplicable para una determinada estimación o línea real. |
| Divisa | La moneda de la lista de precios de origen. Esto se puede cambiar. | Cuando se cambia, todas las líneas de precios resultantes para mano de obra, gastos y artículos del catálogo de productos se convierten a la moneda de la lista de precios objetivo durante la copia. |
| Unidad de tiempo | La moneda de la lista de precios de origen. Esto se puede cambiar. | Cuando se cambia, todas las líneas de precios resultantes para mano de obra, se convierten a la unidad de la lista de precios objetivo durante la copia. Se utiliza la conversión de la configuración de unidades para la unidad de tiempo de la lista de precios de origen y la unidad de tiempo de la lista de precios objetivo. |
| Descripción | Una descripción de la lista de precios de origen con el **-copia** adjunto. Este es un campo de texto que le permite tener una descripción de varias líneas de la lista de precios. | Este campo se muestra en las vistas **Asociado** sobre la lista de precios en varias entidades que tienen listas de precios relacionadas. |

3. Guarda la lista de precios. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Actualice una lista de precios aplicando un margen de beneficio a todos los precios

1. En las pestañas **Rol**, **Categoría** y **Artículo de lista de precios** de una lista de precios, puede seleccionar **Actualizar precios** para aplicar un margen de beneficio a todos los precios de la subcuadrícula. 
2. En la página de diálogo que se abre, introduzca un margen de beneficios. También puede ingresar un porcentaje de margen negativo para disminuir los precios en un cierto porcentaje. 
3. Seleccione **Aceptar** en la página de diálogo y luego verifique que los precios en la subcuadrícula reflejen los cambios que realizó.
