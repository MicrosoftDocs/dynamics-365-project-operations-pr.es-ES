---
title: Listas de precios de productos
description: En este tema se proporciona información sobre las listas de precios en los precios del catálogo que se utilizan para ofertas y contratos de proyectos.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 504aa90bfb478207059b5e2894a3990f9a4a5e9e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085216"
---
# <a name="product-price-lists"></a>Listas de precios de productos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las listas de precios y las entidades de elemento de lista de precios admiten precios de catálogo de productos. En su mayor parte, esta funcionalidad se utiliza para líneas basadas en catálogos en ofertas y contratos de proyectos.

Para las líneas basadas en proyectos, un contrato representa el acuerdo después de la obtención. Puesto que el proceso de negociación generalmente es anterior a la obtención, el precio que se adjunta a la oferta siempre se copia tal cual a una nueva lista de precios y se adjunta al contrato. Esta nueva lista de precios no se puede cambiar fuera del alcance del contrato. Esta limitación ayuda a proteger la lista de tarifas que se negoció de cualquier cambio de precio que se produzca en la lista maestra de precios.

Los productos deben configurarse de modo que tengan listas de precios y costes predeterminados en el catálogo de productos. Use el precio de lista, el coste estándar y el coste actual para configurar el coste predeterminado y los precios de lista. Los precios de lista predeterminados se usan en una línea de cotización o en una línea de contrato de proyecto solo cuando el sistema no puede encontrar una línea de lista de precios para ese producto en la lista de precios del producto para la oferta o el contrato del proyecto.

El precio de coste de las líneas del catálogo de productos puede cambiar entre ofertas. Esta capacidad es importante, porque si no realiza un seguimiento preciso de los costes, no puede determinar las ganancias operativas en la involucración del proyecto. De forma predeterminada, el coste estándar del producto se utiliza como precio de coste. Sin embargo, el precio de coste predeterminado se puede actualizar en la línea de oferta si hay un precio de coste diferente para esa oferta.

## <a name="price-list-items"></a>Elementos de lista de precios

Puede agregar productos de un catálogo de productos a diferentes listas de precios. Las líneas de la lista de precios para productos siempre hacen referencia a una unidad específica. El precio de un producto en los elementos de lista de precios se puede configurar como un importe en divisa. Alternativamente, se puede configurar en función del precio de lista, el coste actual o el coste estándar.

PSA admite varias opciones de redondeo cuando los precios se configuran en función del precio de lista, el coste estándar o el coste actual. Además de aprovechar los múltiples métodos de precios y las opciones de redondeo, puede asociar las listas de descuentos con los elementos de la lista de precios. 

Cuando crea una nueva lista de precios personalizada para una oferta seleccionando **Crear precios personalizados** en la página **Oferta de proyecto** , se realiza una copia de la lista de precios y el campo **Entidad** en el encabezado de la nueva lista de precios se establece en **Entidad de ventas**. El nombre de la nueva lista de precios se adjunta con el nombre de la oferta y una marca de tiempo. También puede usar el nombre de la nueva lista de precios y el nombre de la oferta en los flujos de trabajo personalizados para activar revisiones y aprobaciones adicionales de ofertas que utilizan precios personalizados.

 
## <a name="default-product-price-list"></a>Lista de precios de productos predeterminada
Cada registro de cliente tiene un campo **Lista de precios predeterminada** donde puede especificar una lista de precios que coincida con la divisa del cliente. No se introduce un valor predeterminado automáticamente en ese campo. Cuando existe un acuerdo de precios personalizado con un cliente específico, puede usar dicho campo para asociar una lista de precios con ese cliente.

Las entidades de Oportunidad, Oferta y Contrato de proyecto utilizan el siguiente orden para introducir las listas de precios de productos predeterminadas. Se utiliza el mismo orden para las listas de precios del proyecto.

1.  Oferta
2.  Oportunidad
3.  Cliente
4.  Configuración global 

De manera predeterminada, el campo **Producto** en la línea de oferta enumera todos los productos activos en la lista de precios de productos de la oferta. Si un producto se ha desactivado, o si es un borrador de un producto, no está en la lista, incluso si está en la lista de precios. 

Las líneas del catálogo de productos se agregan como líneas de factura en la primera factura que se crea para un contrato de proyecto. En un borrador de factura, esas líneas de factura se pueden eliminar. En ese caso, las líneas aparecerán en una factura posterior hasta que se facturen o hasta que la factura se envíe al cliente. No puede facturar una cantidad parcial de una línea de factura de producto. Cuando se facturan las líneas de producto del contrato del proyecto, se crean los datos reales. Sin embargo, esos datos reales no están vinculados a la entidad del proyecto relacionada. Es decir, las líneas de contrato de proyecto basadas en productos son independientes de cualquier uso basado en proyectos. No se realiza un seguimiento del consumo de material en los proyectos.
