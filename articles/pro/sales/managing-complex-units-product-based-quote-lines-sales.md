---
title: Administración de unidades complejas, como por usuario, por mes para líneas de ofertas basadas en productos (lite)
description: Este tema proporciona información sobre la administración de unidades complejas para líneas de oferta basadas en productos.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78bdb64d901cf68ce02c168987c2386e1416f6ee
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994787"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Administración de unidades complejas, como por usuario, por mes para líneas de ofertas basadas en productos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Dynamics 365 Project Operations utiliza factores de cantidad para respaldar la venta de productos basados ​​en suscripción. Para productos basados ​​en suscripción, la cantidad en la línea de oferta o contrato del proyecto se expresa como el número de meses de usuario.

Por lo general, el precio del software de suscripción se almacena en el catálogo como el precio por usuario por mes. Durante el proceso de venta, el precio en la línea de oferta suele ser el precio por usuario, por mes que negoció y descontó el agente de ventas de TI. Cada operación tiene un número diferente de usuarios y un número diferente de meses de suscripción. La cantidad que se utiliza para calcular la línea de oferta es un producto de la cantidad de usuarios y la cantidad de meses de suscripción.

Para respaldar este tipo de venta, Project Operations introdujo el concepto de factores de cantidad. Los factores de cantidad dependen de los atributos del producto en Dynamics 365. Cuando configura propiedades específicas para un producto, Project Operations le permite marcar un subconjunto de esas propiedades, o todas ellas, como factores de cantidad.

Project Operations valida que solo las propiedades numéricas o las propiedades del producto que tienen un tipo de datos numéricos se marcan como factores de cantidad. Cuando agrega un producto con factores de cantidad a una línea de oferta, el campo **Cantidad** pasa a ser de solo lectura. Después de introducir valores para las propiedades del producto que son factores de cantidad, Project Operations calcula la cantidad de la línea de oferta.

Por ejemplo, Dynamics 365 Sales podría tener las siguientes propiedades:

- **Número de usuarios**: el número de usuarios
- **Número de meses**: el número de meses de suscripción
- **SKU de producto**

Puede marcar las propiedades **Número de usuarios** y **Número de meses** como factores de cantidad editando las propiedades de la línea de productos.

Para crear factores de cantidad a partir de las propiedades del producto, siga estos pasos:

1. En el panel de navegación izquierdo Operaciones del proyecto, vaya a **Ventas** > **Productos**.
2. Abra el producto para el que necesita configurar factores de cantidad. Asegúrese de que el producto ya tenga las propiedades configuradas.
3. En la página **Información del proyecto** del producto, seleccione la pestaña **Factores de cantidad**.
4. En la subcuadrícula, seleccione **+ Cálculo de nuevo campo**.
5. Introduzca el nombre del factor de cantidad y seleccione el valor de propiedad que se asigna al cálculo del campo.
6. Guardar y cerrar el formulario. Repita estos pasos para todas las propiedades que se utilizarán para calcular la cantidad de la línea de oferta basada en el producto.

Cuando crea una línea de oferta basada en productos para un producto, la cantidad de la línea de oferta se bloqueará. La cantidad se calculará como un producto de los valores de propiedad que introduzca para esa línea de oferta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]