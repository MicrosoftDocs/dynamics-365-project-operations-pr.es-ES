---
title: Líneas de subcontrato para productos
description: Este tema explica cómo registrar líneas de subcontratos para productos y usar los diversos campos para registrar la compra de productos a los proveedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71e4a48c3d29d7ea5b015f6c6797da60001fccff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579094"
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

| Campo | Descripción | Impacto funcional|
| ----- | ----------- | ----------- |
| Asignar nombre | Nombre de la línea de subcontratación para ayudar con la identificación. |Esto se mostrará como la primera columna en todas las búsquedas basadas en líneas de subcontratación.
| Descripción | Una breve descripción de los productos que se compran en la línea del subcontrato. | Nada |
| Tipo de línea | Este campo tiene un valor predeterminado de **Basado en cantidad**. |Nada |
| Método de facturación | Este es un conjunto de opciones que representa los dos principales modelos de contratación que admite Project Operations: **Precio fijo** y **Tiempo y material**. | Según el método de facturación seleccionado, se dispone de una programación de facturas basada en hitos para líneas de subcontratación con el método de facturación Precio fijo. |
| Clase de transacción |Este campo tiene un valor predeterminado de **Tiempo**. Para crear líneas de subcontratación para la compra de productos, establezca el campo **Clase de transacción** en **Material**.  | Esto indica que la línea de subcontratación se está utilizando para registrar la compra de productos que se utilizarán en proyectos. |
| Seleccionar producto | Seleccione si el producto que se está comprando se mantiene en el catálogo de productos o es un producto fuera de catálogo. |Nada |
| Producto | Seleccione un producto activo del catálogo. Este campo está disponible solo cuando **Seleccionar producto** se establece en **Existente**. |La combinación de **Producto** y **Unidad** se utilizará como valor predeterminado o se calculará para el precio unitario de la línea de subcontratación.
| Producto fuera de catálogo | Introduzca el nombre del producto fuera de catálogo. Este campo está disponible solo cuando **Seleccionar producto** se establece en **Fuera de catálogo**.  |El precio de compra no se completará automáticamente para los productos fuera de catálogo.|
| Fecha de entrega solicitada | Ingrese la fecha de entrega requerida para los productos.| Esta fecha también se utiliza para elegir una lista de precios del proyecto en las listas de precios del proyecto adjuntas al subcontrato. El coste del producto en la línea de subcontrato luego se establece de forma predeterminada conforme a esa lista de precios. |
| Fecha de entrega contratada | Introduzca la fecha en la que se acuerda contractualmente la entrega de los productos.  |Nada|
| Cantidad pedida | Introduzca la cantidad del producto que se compra al proveedor.| Esto se usará para mostrar advertencias cuando un jefe de proyecto esté extrayendo de esta cantidad.|
| Unidad de venta | Este valor es predeterminado solo para productos de catálogo. |Cuando se seleccionan tanto **Producto** como **Fecha de entrega requerida**, el sistema selecciona la lista de precios aplicable en función de la fecha de entrega. Los artículos de la lista de precios relacionados se consultan para el producto correspondiente. Los valores de unidad y grupo de unidades predeterminados de la configuración en el registro del artículo de la lista de precios. |
| Unidad | Este valor predeterminado es la unidad configurada en el registro de elemento de lista de precios. Puede cambiar esto a otra unidad, según sea necesario.| La combinación de producto y unidad se utiliza para calcular el valor predeterminado del precio unitario de la línea de subcontrato para productos de catálogo existentes. |
| Precio por unidad | El precio unitario se predetermina con la combinación de producto y unidad, a partir de la lista de los artículos de la lista de precios relacionada con el proyecto que es aplicable para la fecha de entrega solicitada de la línea de subcontrato.  |Nada |
| Subtotal | Este campo de solo lectura se calcula como Cantidad x Precio unitario, si ambos campos tienen valores introducidos. Si el campo **Cantidad**, el campo **Precio unitario**, o ambos, están vacíos, puede ingresar un valor manualmente.  |Nada |
| Impuesto sobre las ventas | introduzca el valor del impuesto sobre las ventas. |Nada |
| Importe total | Este campo calculado muestra el importe total de la línea de subcontrato después de incluir los impuestos. El valor de este campo se calcula como Subtotal + Impuestos. |Nada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
