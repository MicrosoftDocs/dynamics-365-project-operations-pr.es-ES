---
title: Información general sobre líneas de ofertas basadas en productos (lite)
description: En este tema se proporciona información sobre el trabajo con líneas de oferta basadas en producto.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 871597b38d72d2b670c375d2a1711a6022e3446ba3955a3d2a233a6486d85f5c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003342"
---
# <a name="product-based-quote-lines-overview---lite"></a>Información general sobre líneas de ofertas basadas en productos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Puede crear líneas de oferta basadas en productos en Dynamics 365 Project Operations. Las líneas de oferta basadas en productos pueden agregarse manualmente o ser artículos del catálogo de productos.

## <a name="product-catalog"></a>Catálogo de productos

Cada producto de un catálogo de productos tiene una unidad de venta y una unidad predeterminada. Si varios productos comparten el mismo conjunto de atributos, puede crear una familia de productos que comparta esos atributos. 

Por ejemplo, una empresa vende licencias de suscripción para distintas clases de software. Por lo tanto, todo el software de suscripción tendrá los siguientes dos atributos:

- Número de usuarios
- Una duración de suscripción medida en meses

Para mantener este tipo de catálogo, cree una familia de productos que se denomine **Software de suscripción** y agregue el número de usuarios y la duración de la suscripción como atributos. A continuación, puede agregar productos individuales a la familia de productos **Software de suscripción**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Agregar artículos del catálogo de productos a una oferta de proyecto

Las páginas **Oferta de proyecto** y **Contrato de proyecto** tienen secciones para dos tipos de líneas: líneas basadas en proyectos y líneas basadas en productos. Para las líneas basadas en producto, la lista desplegable en la línea de oferta o en la línea de contrato del proyecto incluye todos los productos y unidades en la lista de precios de productos. También puede agregar productos que no forman parte de la lista de precios de productos.

Además, puede seleccionar productos de otras listas de precios o directamente desde el catálogo de productos. Cuando seleccione productos directamente de un catálogo de productos, la lista de precios predeterminada de ese producto se utilizará para obtener el precio de venta del producto. Si no se establece una lista de precios predeterminada, el precio se establece en cero (0).

Cuando una línea de oferta se basa en un catálogo de productos, puede reemplazar el precio de venta directamente en la línea de oferta. Una línea de oferta del campo **Precios** con dos valores disponibles:

- **Reemplazar precios**
- **Usar valor predeterminado**

Si selecciona **Anular precios**, el precio predeterminado no está establecido. En su lugar, debe escribir un precio para el producto en la línea de oferta. Si selecciona **Uso por defecto**, se utiliza el precio de venta predeterminado y el campo se bloquea para su edición.

Los precios de venta predeterminados se introducen en las líneas basadas en productos de una oferta. El campo **Precios** se establece en **Reemplazar precios** para que pueda editar el precio predeterminado en las líneas de oferta. Se trata de una invalidación específica de Project Operations para el comportamiento de las líneas basadas en productos en Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]