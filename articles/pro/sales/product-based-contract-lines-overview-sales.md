---
title: Información general de líneas de contrato basadas en productos (lite)
description: En este tema se proporciona información sobre líneas de contrato basadas en productos.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369757"
---
# <a name="product-based-contract-lines-overview---lite"></a>Información general de líneas de contrato basadas en productos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Puede crear líneas de contrato basadas en productos en Dynamics 365 Project Operations. Las líneas de contrato basadas en productos pueden ser líneas creadas manualmente o artículos del catálogo de productos.

## <a name="product-catalog"></a>Catálogo de productos

Los productos de un catálogo de productos tienen una unidad de venta y una unidad predeterminada. Si varios productos comparten el mismo conjunto de atributos, puede crear una familia de productos que también tenga esos atributos. Todos los productos de una familia de productos heredan el mismo conjunto de atributos.

Por ejemplo, una empresa vende licencias de suscripción para distintas clases de software. Por lo tanto, todo el software de suscripción tendrá los siguientes dos atributos:

- Número de usuarios
- Duración de la suscripción (en meses)

Para mantener este tipo de catálogo, cree una familia de productos que se denomine **Software de suscripción**. Agregue los atributos, **Número de usuarios** y **Duración de la suscripción** a la familia de productos. Luego, agregue productos individuales a la familia de productos **Software de suscripción**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Agregar artículos del catálogo de productos a un contrato de proyecto

Los contratos de proyecto tienen secciones para dos clases de líneas, basadas en proyecto y basadas en productos. Las líneas basadas en productos incluyen todos los productos y unidades en la lista de precios de productos en el contrato. Los productos que no forman parte de la lista de productos del contrato pueden agregarse.

Puede seleccionar productos de otras listas de precios o directamente del catálogo de productos. Cuando seleccione productos directamente de un catálogo de productos, la lista de precios predeterminada de ese producto se utilizará para el precio de venta del producto. Si no se establece una lista de precios predeterminada, el precio se establece en 0 (cero).

Si una línea de contrato se basa en un catálogo de productos, puede reemplazar el precio de venta directamente en la línea. Una línea de contrato tiene el campo **Precios** con los dos valores:

- **Reemplazar precio**
- **Usar valor predeterminado**

Si establece el campo **Precios** a **Reemplazar precio**, no se establece el precio predeterminado. Especifique el precio para el producto de línea de contrato. Si configura el campo en **Usar predeterminado**, se utiliza el precio de venta predeterminado y el campo no se puede editar.

Después de instalar Project Operations, los precios de venta predeterminados se introducen en las líneas basadas en productos en un contrato. El campo **Precios** se establece en **Reemplazar precio** para que pueda editar el precio predeterminado en las líneas de contrato. Se trata de una invalidación específica de Project Operations para el comportamiento de las líneas basadas en productos en Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]