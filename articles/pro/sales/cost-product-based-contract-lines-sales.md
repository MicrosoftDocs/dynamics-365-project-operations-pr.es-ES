---
title: Líneas de contrato basadas en productos de coste (lite)
description: En este tema se proporciona información sobre la creación
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003562"
---
# <a name="cost-product-based-contract-lines---lite"></a>Líneas de contrato basadas en productos de coste (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_


Las líneas de contrato basadas en producto de Dynamics 365 Project Operations incluyen el campo **Precio de coste**, que almacena el precio de coste del producto para los cálculos de rentabilidad posteriores.

Cuando se crea una línea de contrato basada en producto para un producto del catálogo, el coste predeterminado de la línea es **Coste estándar** en el catálogo de productos. El campo **Coste estándar** del catálogo de productos se configura en la divisa base de la organización. Cuando el coste unitario está por defecto en la línea del contrato, se convierte a la moneda de venta en el contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Coste unitario de línea de contrato basada en producto

Tener un coste unitario en una línea de contrato basada en productos permite distintos costes de producto por cada venta de una unidad. Si bien no siempre es necesario, existen ciertos escenarios en los que el proveedor puede descontar el costo del producto para el cliente. Tenga en cuenta el escenario siguiente:

Fabrikam Robotics está instalando brazos robóticos en las líneas de montaje de Adatum Corporation. Fabrikam proporciona servicios de instalación, pero los brazos robóticos son de Trey Research. Si la instalación de brazos robóticos en Adatum Corporation abre una nueva industria vertical para los brazos robóticos de Trey Research, estos podrían ofrecer un descuento especial para esta oferta a Fabrikam. En este caso, Fabrikam crea una línea de contrato basada en producto para Robotic Arms. Se especifica un coste unitario para este contrato. El coste es diferente al de los brazos robóticos de Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]