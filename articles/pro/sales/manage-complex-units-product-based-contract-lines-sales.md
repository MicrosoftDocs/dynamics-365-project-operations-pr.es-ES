---
title: Administrar unidades complejas para líneas de contratos basadas en productos (lite)
description: Este tema proporciona información sobre cómo respaldar la venta de productos basados en suscripción.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273354"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Administrar unidades complejas para líneas de contratos basadas en productos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Dynamics 365 Project Operations utiliza factores de cantidad para respaldar la venta de productos basados ​​en suscripción. Para productos basados ​​en suscripción, la cantidad en la línea de contrato o de contrato del proyecto se expresa como el número de meses de usuario.

El precio del software de suscripción se almacena en el catálogo como el precio por usuario, por mes. Durante el proceso de venta, el precio en la línea de contrato suele ser el precio por usuario, por mes que negoció y descontó el agente de ventas. Cada operación tiene un número diferente de usuarios y un número diferente de meses de suscripción. La cantidad que se utiliza para calcular la cantidad de la línea de contrato es un producto de la cantidad de usuarios y la cantidad de meses de suscripción.

Para respaldar este tipo de venta, Project Operations admite el concepto de *factores de cantidad*. Los factores de cantidad dependen de los atributos del producto. Cuando configura propiedades específicas para un producto, puede marcar un subconjunto de esas propiedades, o todas las propiedades, como factores de cantidad.

Project Operations valida que solo las propiedades numéricas o las propiedades del producto que tienen un tipo de datos numéricos se marcan como factores de cantidad. Cuando un producto con factores de cantidad configurados se agrega a una línea de contrato, el campo **Cantidad** pasa a ser de solo lectura. Después de introducir valores para las propiedades del producto que son factores de cantidad, Project Operations calcula la cantidad de la línea de contrato.

Por ejemplo, Dynamics 365 Sales podría tener las siguientes propiedades:

- **Número de usuarios**: el número de usuarios.
- **Número de meses**: el número de meses de suscripción.
- **SKU del producto**: la unidad de mantenimiento de existencias (SKU) del producto.

Las propiedades **Número de usuarios** y **Número de meses** se pueden marcar como factores de cantidad editando las propiedades de la línea de productos.

Para crear factores de cantidad a partir de las propiedades del producto, complete los siguientes pasos.

1. Sobre **Project Operations**, seleccione **Ventas-Productos**.
2. Abra el producto para el que necesita configurar factores de cantidad. Asegúrese de que el producto ya tenga las propiedades configuradas.
3. Sobre la página **Información del proyecto**, seleccione la pestaña **Factores de cantidad**.
4. En la subcuadrícula, seleccione **+ Cálculo de nuevo campo**.
5. Introduzca el nombre del **factor de cantidad** y seleccione el valor de propiedad que se asigna al cálculo del campo.
6. Guardar y cerrar el formulario.
7. Repita los pasos 2 a 6 para todas las propiedades que juntas compondrán la cantidad para la línea de contrato basada en productos.

Con los factores de cantidad configurados, cuando el usuario crea una línea de contrato para este producto, la cantidad de la línea de contrato se bloquea. Luego, la cantidad se calcula como un producto de los valores de propiedad para esa línea de contrato.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]