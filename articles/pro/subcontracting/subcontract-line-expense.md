---
title: Líneas de subcontrato para categorías de gastos
description: Este tema explica cómo registrar líneas de subcontratos para gastos y usar los campos para registrar la compra de tiempo de los proveedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323842"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Líneas de subcontrato para categorías de gastos

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Un subcontrato en Dynamics 365 Project Operations puede tener una línea para categorías de gastos. Las líneas de subcontrato para categorías de gastos permiten a un administrador del proyecto comprar categorías de servicios o productos de proveedores que pueden cargar a un proyecto.

Para crear una línea de subcontrato para categorías de gastos en Project Operations, complete los siguientes pasos.

1. En el panel de navegación, seleccione **Subcontratos** y abra el subcontrato con el que quiere trabajar.
2. En la pestaña **Líneas de subcontratación**, seleccione **Nueva** para crear una nueva línea.
3. En la página **Creación rápida**, en el campo **Clase de transacción**, seleccione **Gastos** e introduzca o seleccione cualquier otra información de campo requerida.

La siguiente tabla proporciona información sobre los campos de la página de detalles de **Línea de subcontrato** y la página **Creación rápida**.

| **Campo** |  **Descripción** |
| ----------| ---------------- |
| Asignar nombre | El nombre de la línea de subcontratación. |
| Descripción | Una breve descripción de las categorías de servicios y productos que se compran en la línea de subcontrato. |
| Tipo de línea | Este campo tiene un valor predeterminado de **Basado en cantidad**.  |
| Método de facturación | El método de facturación de la línea de subcontratación. Según el método de facturación de la línea, se dispone de un programa de facturación basado en hitos para el método de facturación de precio fijo.  |
| Clase de transacción | Este campo tiene un valor predeterminado de **Tiempo**. Para crear líneas de subcontrato para la compra de productos, establezca el campo **Clase de transacción** en **Gasto**. Este valor del campo indica que la línea de subcontrato se utiliza para registrar una compra de una categoría de productos o servicios que se utilizarán en proyectos. |
| Categoría de transacción | Seleccione la categoría de transacción. |
| Inicio solicitado | La fecha en la que las categorías de compra deben estar disponibles desde el proveedor. El inicio solicitado se utiliza para elegir una lista de precios del proyecto de las listas de precios del proyecto adjuntas al subcontrato. El coste de la categoría en la línea de subcontrato se predetermina a partir de esa lista de precios. |
| Finalización solicitada | La fecha en la que las categorías de compra ya no son necesarias. Esta fecha llama a una advertencia cuando un administrador del proyecto asocia esta línea de subcontrato con estimaciones de gastos específicos en los proyectos que tienen una fecha posterior a esta fecha. |
| Cantidad pedida | La cantidad de la categoría que se compra al proveedor. Cuando un administrador del proyecto supera la cantidad comprada, se producirá una advertencia.  |
| Unidad de venta | El valor predeterminado de este campo se basa en el grupo de unidades predeterminado que se configura para la categoría seleccionada. |
| Unidad | El valor predeterminado de este campo se basa en la unidad predeterminada para la categoría seleccionada. La combinación de categoría y unidad se utiliza para predeterminar el precio unitario de la línea de subcontrato. |
| Precio por unidad | El valor del campo de precio unitario se predetermina a partir de la combinación de categoría y unidad, a partir de los precios de categorías relacionados con la lista de precios del proyecto que es aplicable para el inicio solicitado de la línea de subcontrato.  |
| Subtotal | Este campo de solo lectura se calcula automáticamente como el precio unitario por la cantidad si se ingresan los valores de cantidad y precio unitario. Si uno o ambos campos están vacíos, puede ingresar un valor en este campo manualmente.  |
| Impuesto sobre las ventas | Especifique el importe del impuesto sobre las ventas.  |
| Importe total | El importe total de la línea de subcontrato, impuestos incluidos. Este valor se calcula como subtotal + impuestos sobre ventas.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
