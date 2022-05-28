---
title: Listas de precios de productos
description: En este tema se proporciona información sobre las listas de precios en los precios del catálogo que se utilizan para ofertas y contratos de proyectos.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4feb7638dd7b6826e575d83457ae7f74ef6793bf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593265"
---
# <a name="product-price-lists"></a>Listas de precios de productos

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

 En Project Operations, las entidades **Listas de precios de productos** y entidades de elementos de lista de precios relacionadas admiten la funcionalidad para fijar precios de productos en líneas de cotización y contrato basadas en productos. Para los productos utilizados en proyectos, se utilizan los registros de elementos de la lista de precios para las listas de precios del proyecto. 

Los productos deben configurarse de modo que tengan listas de precios y costes predeterminados en el catálogo de productos. Use el precio de lista, el coste estándar y el coste actual para configurar el coste predeterminado y los precios de lista. Los precios de lista predeterminados se usan en una línea de cotización o en una línea de contrato de proyecto solo cuando el sistema no puede encontrar una línea de lista de precios para ese producto en la lista de precios del producto para la oferta o el contrato del proyecto.

El precio de coste de las líneas del catálogo de productos puede cambiar entre ofertas. Esta capacidad es importante, porque si no realiza un seguimiento preciso de los costes, no puede determinar las ganancias operativas en la involucración del proyecto. De forma predeterminada, el coste estándar del producto se utiliza como precio de coste. Sin embargo, el precio de coste predeterminado se puede actualizar en la línea de oferta si hay un precio de coste diferente para esa oferta.

## <a name="price-list-items"></a>Elementos de lista de precios

Puede agregar productos de un catálogo de productos a diferentes listas de precios. Las líneas de la lista de precios para productos siempre hacen referencia a una unidad específica. El precio de un producto en los elementos de lista de precios se puede configurar como un importe en divisa. Alternativamente, se puede configurar en función del precio de lista, el coste actual o el coste estándar.

La funcionalidad de precios admite varias opciones de redondeo cuando los precios del producto se configuran en función del precio de lista, el coste estándar o el coste actual. Además de aprovechar los múltiples métodos de precios y las opciones de redondeo, puede asociar las listas de descuentos con los elementos de la lista de precios. 

 
## <a name="default-product-price-list"></a>Lista de precios de productos predeterminada
Cada registro de cliente tiene un campo **Lista de precios predeterminada** donde puede especificar una lista de precios que coincida con la divisa del cliente. No se introduce un valor predeterminado automáticamente en ese campo. Cuando existe un acuerdo de precios personalizado con un cliente específico, puede usar dicho campo para asociar una lista de precios con ese cliente.

Las entidades de Oportunidad, Oferta y Contrato de proyecto utilizan el siguiente orden para introducir las listas de precios de productos predeterminadas. Se utiliza el mismo orden para las listas de precios del proyecto.

1.  Oferta
2.  Oportunidad
3.  Cliente
4.  Configuración global 

De manera predeterminada, el campo **Producto** en la línea de oferta enumera todos los productos activos en la lista de precios de productos de la oferta. Si un producto se ha desactivado, o si es un borrador de un producto, no está en la lista, incluso si está en la lista de precios. 

Las líneas del catálogo de productos se agregan como líneas de factura en la primera factura que se crea para un contrato de proyecto. En un borrador de factura, esas líneas de factura se pueden eliminar. En ese caso, las líneas aparecerán en una factura posterior hasta que se facturen o hasta que la factura se envíe al cliente. No puede facturar una cantidad parcial de una línea de factura de producto. Cuando se facturan las líneas de producto del contrato del proyecto, se crean los datos reales. Sin embargo, esos datos reales no están vinculados a la entidad del proyecto relacionada. Es decir, las líneas de contrato de proyecto basadas en productos son independientes de cualquier uso basado en proyectos. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
