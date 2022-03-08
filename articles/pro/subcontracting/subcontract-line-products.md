---
title: Líneas de subcontrato para productos
description: Este tema explica cómo registrar líneas de subcontratos para productos y usar los diversos campos para registrar la compra de productos a los proveedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323707"
---
# <a name="subcontract-lines-for-products"></a>Líneas de subcontrato para productos

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Un subcontrato en Dynamics 365 Project Operations puede tener una línea de subcontrato para productos. Estas líneas permiten a un administrador del proyecto comprar productos de proveedores que luego pueden usar en las tareas del proyecto.

Complete los siguientes pasos para crear una línea de subcontrato para productos en Project Operations.

1. En la página de navegación, seleccione **Subcontratos** y abra el subcontrato con el que quiere trabajar. 
2. En la pestaña **Líneas de subcontratación**, seleccione **+ Nueva** para crear una nueva línea de subcontrato.
3. En la página **Creación rápida**, en el campo **Clase de transacción**, seleccione **Material** e introduzca o seleccione cualquier la información de campo requerida. 
4. Seleccione **Guardar**.

La siguiente tabla proporciona información sobre los campos de la página **Detalles de línea de subcontrato** y la página **Creación rápida**, en tanto que son relevantes para la compra de productos.

| Campo | Descripción |
| ----- | ----------- |
| Asignar nombre | El nombre de la línea de subcontratación. |
| Descripción | Una breve descripción de los productos que se compran en la línea del subcontrato. |
| Tipo de línea | El valor predeterminado es **Basado en cantidad**. |
| Método de facturación |  El método de facturación de la línea de subcontratación. Para los métodos de facturación de precio fijo, se configura un programa de facturación basado en hitos. |
| Clase de transacción | El valor predeterminado es **Tiempo**. Para crear líneas de subcontrato para la compra de productos, en el campo **Clase de transacción**, seleccione **Material**. Esta selección indica que la línea de subcontrato se utiliza para registrar una compra de productos que se utilizarán en proyectos. |
| Seleccionar producto | Seleccione si el producto que se está comprando se mantiene en el catálogo de productos o es un producto fuera de catálogo. |
| Producto | Seleccione un producto activo del catálogo. Este campo está disponible solo cuando **Seleccionar producto** se establece en **Existente**. |
| Producto fuera de catálogo | Introduzca el nombre del producto fuera de catálogo. Este campo está disponible solo cuando **Seleccionar producto** se establece en **Fuera de catálogo**.  |
| Fecha de entrega solicitada | Seleccione la fecha de entrega requerida para los productos. Esta fecha también se utiliza para elegir una lista de precios del proyecto en las listas de precios del proyecto adjuntas al subcontrato. El coste del producto en la línea de subcontrato luego se establece de forma predeterminada conforme a esa lista de precios. |
| Fecha de entrega contratada | Seleccione la fecha en la que se acuerda contractualmente la entrega de los productos.  |
| Cantidad pedida | Introduzca la cantidad del producto que se compra al proveedor. Si un administrador del proyecto supera esta cantidad, se producirá una advertencia. |
| Unidad de venta | Este valor es predeterminado solo para productos de catálogo. Cuando se seleccionan tanto **Producto** como **Fecha de entrega requerida**, el sistema selecciona la lista de precios aplicable en función de la fecha de entrega. Los artículos de la lista de precios relacionados se consultan para el producto correspondiente. Los valores de unidad y grupo de unidades predeterminados de la configuración en el registro del artículo de la lista de precios. |
| Unidad | Este valor se predetermina a la configuración de la unidad en el registro del artículo de la lista de precios. Puede cambiar esto a otra unidad, según sea necesario. La combinación de producto y unidad se utiliza para calcular el valor predeterminado del precio unitario de la línea de subcontrato para productos de catálogo existentes. |
| Precio por unidad | El precio unitario se predetermina con la combinación de producto y unidad, a partir de la lista de los artículos de la lista de precios relacionada con el proyecto que es aplicable para la fecha de entrega solicitada de la línea de subcontrato.  |
| Subtotal | Este campo de solo lectura se calcula como Cantidad x Precio unitario, si ambos campos tienen valores introducidos. Si el campo **Cantidad**, el campo **Precio unitario**, o ambos, están vacíos, puede ingresar un valor manualmente.  |
| Impuesto sobre las ventas | introduzca el valor del impuesto sobre las ventas. |
| Importe total | Este campo calculado muestra el importe total de la línea de subcontrato después de incluir los impuestos. El valor de este campo se calcula como subtotal + impuestos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
