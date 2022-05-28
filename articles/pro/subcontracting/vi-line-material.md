---
title: Líneas de factura de proveedor de productos
description: Este tema explica cómo registrar líneas de factura de proveedor para productos y usar los diferentes campos para registrar compras de productos de proveedores.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599199"
---
# <a name="vendor-invoice-lines-for-products"></a>Líneas de factura de proveedor de productos

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Una factura de proveedor en Microsoft Dynamics 365 Project Operations puede tener líneas de factura de proveedor para productos (también denominados materiales). Los administradores de proyecto pueden usar líneas de factura de proveedor para productos para registrar los costos de productos comprados en los proyectos.

Las líneas de factura de proveedor por productos pueden o no hacer referencia a una línea de subcontrato por materiales. Si una línea de factura de proveedor por productos hace referencia a un subcontrato, los administradores de proyectos podrán comparar y verificar los productos que factura la línea de factura del proveedor frente al uso de productos comprados que registran y aprueban los administradores de proyectos en el proyecto.

La siguiente tabla proporciona información sobre los campos de las líneas de factura de proveedor para productos.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | El nombre de la línea de factura de proveedor, para ayudar con la identificación. | Este nombre se mostrará como la primera columna en todas las búsquedas basadas en líneas de factura de proveedor. |
| Description | Una breve descripción de los productos que factura el proveedor en la línea de factura del proveedor. | None |
| Subcontrato | El subcontrato en el que se pidieron originalmente los productos. | Cuando se selecciona un subcontrato para la factura del proveedor, todas las líneas de la factura del proveedor heredarán esa selección. Una factura de proveedor no puede tener líneas de factura de proveedor que hagan referencia a diferentes subcontratos. |
| Línea de subcontrato | La línea de subcontrato en la que se pidieron los productos. La lista de líneas de subcontrato que se pueden seleccionar se limita a las líneas del subcontrato seleccionado. | Cuando se selecciona una línea de subcontrato en una línea de factura de proveedor por productos, los valores predeterminados para los campos **Proyecto**, **Tarea** y **Producto** se introducen desde los campos correspondientes de la línea de subcontrato. Si la línea de subcontrato seleccionada tiene valores en los campos **Proyecto**, **Tarea** y **Producto**, los valores de los campos correspondientes de la línea de factura del proveedor no pueden diferir de esos valores. |
| Fecha de la transacción | La fecha en que se registrará en el proyecto el costo real de la línea de factura del proveedor. | None|
| Clase de transacción | Cuando se facturan los productos, este campo debe establecerse en **Material**. | El valor **Material** indica que la línea de factura del proveedor se utiliza para registrar el importe de la factura de los materiales que se adquirieron. |
| Project | El nombre del proyecto en el que se utilizaron los productos que se están facturando. | Este campo es obligatorio y no se puede dejar en blanco. |
| Task | El nombre de la taera de proyecto en la que se utilizaron los productos que se están facturando. Este campo está disponible solo si se selecciona un proyecto. La selección de una tarea de proyecto es opcional. | Si este campo se deja en blanco, el director del proyecto puede hacer coincidir la línea de la factura del proveedor con el producto comprado que se utiliza en cualquier tarea del proyecto. Si la línea de factura del proveedor no hace referencia a una línea de subcontrato y este campo se deja en blanco, el costo real creado por la línea de factura del proveedor no se vinculará a ningún dato real de ventas no facturado. En este caso, si se configura la facturación basada en tareas, los costos no se podrán facturar al cliente final. |
| Seleccionar producto | Seleccione si el producto que se está facturando es un producto existente del catálogo o un producto de fuera de catálogo. | El valor predeterminado se ingresa desde la línea de subcontrato cuando se selecciona una línea de subcontrato. |
| Producto | Seleccione el producto del catálogo. Si el producto es de fuera de catálogo, escriba el nombre del producto. | Este campo se usa para ingresar precios de compra predeterminados para productos existentes. |
| Cantidad | Introduzca la cantidad de material que factura el proveedor en esta línea de factura. | None |
| Unidad de venta | Seleccione la unidad de venta del grupo de unidades de la unidad en la que se expresa la cantidad que se está facturando. | None |
| Unidad | El valor predeterminado para esta unidad base de horas de la unidad de venta seleccionada. Puede cambiar este valor para pagar en cualquier unidad de la unidad de venta seleccionada. | La combinación de valores de **Producto** y **Unidad** se utilizará como valor predeterminado o calculado para el campo **Precio unitario** de la línea de factura de proveedor. |
| Precio unitario | El precio unitario predeterminado utiliza la combinación de los valores **Producto** y **Unidad** de la lista de precios del proyecto aplicable para la fecha de transacción de la línea de factura de proveedor. | None |
| Subtotal | Este es un campo de solo lectura que se calcula como *Cantidad* &times; *Precio unitario*, si se ingresan los valores yanto en el campo **Cantidad** como en el campo **Precio unitario**. Si uno o estos dos campos están en blanco, puede ingresar un valor en este campo. | None |
| Impuesto sobre las ventas | Especifique el importe del impuesto sobre las ventas. | None |
| Importe total | El importe total de la línea de factura del proveedor, incluidos los impuestos. Este valor se calcula como *Subtotal* + *Impuestos*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
