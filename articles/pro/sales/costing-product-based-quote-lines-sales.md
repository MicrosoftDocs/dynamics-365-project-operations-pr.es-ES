---
title: Líneas de ofertas basadas en productos de gestión de costes
description: En este tema se proporciona información sobre la aplicación de un precio de coste a una línea de oferta basada en producto.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003472"
---
# <a name="costing-product-based-quote-lines"></a>Líneas de ofertas basadas en productos de gestión de costes

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


Líneas de cotización basadas en productos en Dynamics 365 Project Operations también tengo un campo **Precio de coste** campo. Este campo se usa para seguir el precio de coste del producto en la línea de oferta y para los cálculos de rentabilidad posteriores.

Cuando se crea una línea de oferta basada en productos para un producto de catálogo, el coste de la línea de oferta basada en producto se toma de forma predeterminada del campo **Coste estándar** del catálogo de productos. El campo de coste estándar del catálogo de productos se configura en la divisa base de la organización. El coste unitario predeterminado en la línea de oferta basada en producto se convierte a la moneda de venta en la oferta.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Coste unitario de línea de oferta basada en producto

El propósito de tener un coste unitario en una línea de oferta basada en producto es permitir diferentes costes para un producto para cada venta. Este no es un escenario habitual, pero a veces el proveedor puede descontar el coste del producto dependiendo del cliente de la venta final.

Por ejemplo:

Fabrikam Robotics está instalando brazos robóticos en las líneas de montaje de A Datum Corporation. Fabrikam proporciona servicios de instalación, pero los brazos robóticos se obtienen de Trey Robotics. Si la instalación de brazos robóticos en A Datum Corporation abre una nueva industria vertical para los brazos robóticos de Trey, Trey podría ofrecer un descuento especial para esta oferta a Fabrikam.

En este caso, Fabrikam creará una línea de oferta basada en el producto para Robotic Arms e ingresará un coste unitario especial para esta oferta. Este coste es diferente del coste estándar de Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]