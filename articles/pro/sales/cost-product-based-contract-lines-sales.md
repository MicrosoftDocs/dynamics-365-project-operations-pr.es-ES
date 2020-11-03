---
title: Líneas de contrato basadas en productos de gestión de costes
description: En este tema se proporciona información sobre la creación
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "4085379"
---
# <a name="costing-product-based-contract-lines"></a>Líneas de contrato basadas en productos de gestión de costes

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_


Las líneas de contrato basadas en productos en Dynamics 365 Project Operations incluyen **Precio de coste** campo, que almacena el precio de costo del producto para los cálculos de rentabilidad posteriores.

Cuando se crea una línea de contrato basada en productos para un producto de catálogo, el costo de la línea de contrato basada en producto se toma de forma predeterminada del campo **Coste estándar** del catálogo de productos. El campo **Coste estándar** del catálogo de productos se configura en la divisa base de la organización. Cuando el coste unitario está por defecto en la línea del contrato, se convierte a la moneda de venta en el contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Coste unitario de línea de contrato basada en producto

Tener un coste unitario en una línea de contrato basada en productos permite distintos costes de producto por cada venta de una unidad. Si bien no siempre es necesario, existen ciertos escenarios en los que el proveedor puede descontar el costo del producto para el cliente. Tenga en cuenta el escenario siguiente:

Fabrikam Robotics está instalando brazos robóticos en las líneas de montaje de Adatum Corporation. Fabrikam proporciona servicios de instalación, pero los brazos robóticos se obtienen de Trey Research. Si la instalación de brazos robóticos en Adatum Corporation abre una nueva industria vertical para los brazos robóticos de Trey Research, estos podrían ofrecer un descuento especial para esta oferta a Fabrikam. En este caso, Fabrikam crea una línea de contrato basada en productos para Robotic Arms e ingresa un costo por unidad para este contrato que es diferente del costo estándar de los brazos robóticos de Trey Research.
