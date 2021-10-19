---
title: Líneas de subcontrato para categorías de gastos
description: Este tema explica cómo registrar líneas de subcontratos para gastos y usar los campos para registrar la compra de tiempo de los proveedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c32bf2ac54de98a921d338e436ecd089e68a759
ms.sourcegitcommit: cd4e81f129681a12f2efe63ec2bb14e611cf88ba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/20/2021
ms.locfileid: "7506120"
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

| **Campo** | **Descripción** | **Impacto funcional** |
| --- | --- | --- |
| Asignar nombre | Nombre de la línea de subcontratación para ayudar con la identificación. | Esto se mostrará como la primera columna en todas las búsquedas basadas en líneas de subcontratación. |
| Descripción | Una breve descripción de las categorías de gastos que se compran en la línea de subcontratación. | Nada |
|Tipo de línea | Este campo tiene un valor predeterminado de **Basado en cantidad**. |Nada |
| Método de facturación | Este es un conjunto de opciones que representa los dos principales modelos de contratación que admite Project Operations: **Precio fijo** y **Tiempo y material**. | Se dispone de una programación de facturas basada en hitos para líneas de subcontratación si se selecciona el método de facturación Precio fijo. |
| Clase de transacción | Este campo tiene un valor predeterminado de **Tiempo**. Para crear líneas de subcontratación para la compra de productos, establezca el campo **Clase de transacción** en **Gasto**.  | Esto indica que la línea de subcontratación se está utilizando para registrar la compra de una categoría de gastos que se utilizará en proyectos. |
| Categoría de transacción | Muestra una lista de categorías de transacciones activas en el sistema. |Nada |
| Inicio solicitado | Ingrese la fecha en la que las categorías de compra deben estar disponibles del proveedor. | El inicio solicitado se utiliza para elegir una de las listas de precios del proyecto adjuntas al subcontrato. El costo de la categoría en la línea de subcontratación proviene de esa lista de precios. |
| Finalización solicitada | Ingrese la fecha en la que las categorías de compra ya no serían necesarias. | Esto se usará para mostrar advertencias cuando un gerente de proyecto esté asociando esta línea de subcontratación a estimaciones de gastos específicas en el proyecto que se requieren después de esta fecha. |
| Cantidad pedida | Cantidad de la categoría que se compra al proveedor. | Esto se usará para mostrar advertencias cuando un jefe de proyecto esté extrayendo de esta cantidad.|
| Unidad de venta | El valor predeterminado se basa en el grupo de unidades predeterminado que está configurado para la categoría seleccionada. |Nada |
| Unidad | El valor predeterminado se basa en la unidad predeterminada configurada para la categoría seleccionada.  | La combinación de **Categoría** y **Unidad** se utilizará como valor predeterminado o se calculará para el precio unitario de la línea de subcontratación.  |
| Precio por unidad | El valor predeterminado utiliza la combinación de **Categoría** y **Unidad** de los precios de categorías relacionados con la lista de precios del proyecto, que es aplicable para el inicio solicitado de la línea de subcontratación. |Nada |
| Subtotal | Este es un campo de solo lectura que se calcula como Cantidad X Precio unitario, si se ingresan los valores de cantidad y precio unitario. Si uno o ambos campos están en blanco, puede ingresar un valor en este campo. |Nada |
| Impuesto sobre las ventas | Especifique el importe del impuesto sobre las ventas. |Nada |
| Importe total | El importe total de la línea de subcontrato, impuestos incluidos. Este valor se calcula como Subtotal + Impuestos sobre ventas. |Nada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
