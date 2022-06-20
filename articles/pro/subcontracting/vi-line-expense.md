---
title: Líneas de factura de proveedor para categorías de gastos
description: Este artículo explica cómo registrar líneas de factura de proveedor para categorías de gastos.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925923"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Líneas de factura de proveedor para categorías de gastos

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Una factura de proveedor en Microsoft Dynamics 365 Project Operations puede tener líneas de factura de proveedor por categorías de gastos. Los administradores de proyectos pueden usar líneas de factura de proveedor para categorías de gastos, para registrar los costos de los servicios que se adquieren como categorías de gastos.

Las líneas de factura de proveedor por categorías de gastos pueden o no hacer referencia a una línea de subcontrato por categorías de gastos. Si una línea de factura de proveedor por categorías de gastos hace referencia a un subcontrato, los administradores de proyectos podrán comparar y verificar los gastos que factura la línea de factura del proveedor frente a los gastos registrados en esas categorías de gastos y aprobados por los administradores de proyectos en el proyecto.

La siguiente tabla proporciona información sobre los campos de las líneas de factura de proveedor para categorías de gastos.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | El nombre de la línea de factura de proveedor, para ayudar con la identificación. | Este nombre se mostrará como la primera columna en todas las búsquedas basadas en líneas de factura de proveedor. |
| Description | Una breve descripción de los servicios que factura el proveedor en la línea de factura del proveedor. | None |
| Subcontrato | El subcontrato en el que se pidieron originalmente los servicios. | Cuando se selecciona un subcontrato para la factura del proveedor, todas las líneas de la factura del proveedor heredarán esa selección. Una factura de proveedor no puede tener líneas de factura de proveedor que hagan referencia a diferentes subcontratos. |
| Línea de subcontrato | La línea de subcontrato en la que se pidieron los servicios. La lista de líneas de subcontrato que se pueden seleccionar se limita a las líneas del subcontrato seleccionado. | Cuando se selecciona una línea de subcontrato en una línea de factura de proveedor por categorías de gastos, los valores predeterminados para los campos **Proyecto**, **Tarea** y **Categoría de transacción** se ingresan desde los campos correspondientes de la línea de subcontrato. Si la línea de subcontrato seleccionada tiene valores en los campos **Proyecto**, **Tarea de proyecto** y **Categoría de transacción**, los valores de los campos correspondientes de la línea de factura del proveedor no pueden diferir de esos valores. |
| Fecha de la transacción | La fecha en que se registrará en el proyecto el costo real de la línea de factura del proveedor. |None |
| Clase de transacción | Seleccione **Gastos** para registrar una factura de proveedor para una categoría de gastos. | El valor **Gastos** indica que la línea de factura del proveedor se utiliza para registrar el importe de la factura de los servicios adquiridos como categorías de gastos. |
| Project | El nombre del proyecto en el que se utilizaron los servicios que se están facturando. | Este campo es obligatorio y no se puede dejar en blanco. |
| Task | El nombre de la tarea del proyecto en la que se utilizaron los servicios que se están facturando. Este campo está disponible solo si se selecciona un proyecto. La selección de una tarea de proyecto es opcional. | Si este campo se deja en blanco, el director del proyecto puede hacer coincidir la línea de la factura del proveedor con gastos registrados en cualquier tarea del proyecto. Si la línea de factura del proveedor no hace referencia a una línea de subcontrato y este campo se deja en blanco, el costo real creado por la línea de factura del proveedor no se vinculará a ningún dato real de ventas no facturado. En este caso, si se configura la facturación basada en tareas, es posible que los costos no se puedan facturar al cliente final. |
| Categoría de transacción | La categoría de transacción que se está facturando. Se debe crear una categoría de gastos correspondiente para la categoría de transacción seleccionada. | La combinación de valores de **Categoría de transacción** y **Unidad** se utilizará como valor predeterminado o calculado para el campo **Precio unitario** de la línea de factura de proveedor. |
| Cantidad | Introduzca la cantidad que está facturando el proveedor en la línea de factura. |None|
| Unidad de venta | Se ingresa un valor predeterminado basado en la unidad de venta de la categoría de transacción seleccionada. | None |
| Unidad | El valor predeterminado para esta unidad base de horas de la unidad de venta seleccionada. Puede cambiar este valor para comprar en cualquier unidad de la unidad de venta. | La combinación de valores de **Categoría de transacción** y **Unidad** se utilizará como valor predeterminado o calculado para el campo **Precio unitario** de la línea de factura de proveedor. |
| Precio unitario | El precio unitario predeterminado utiliza la combinación de los valores **categoría de transacción** y **Unidad** de la lista de precios del proyecto aplicable para la fecha de transacción de la línea de factura de proveedor. | Si el precio de la lista de precios del proyecto aplicable se configura en una unidad que difiere de la unidad en la línea de la factura del proveedor, el sistema usa la conversión de unidades para calcular el precio por unidad. |
| Subtotal | Este es un campo de solo lectura que se calcula como *Cantidad* &times; *Precio unitario*, si se ingresan los valores yanto en el campo **Cantidad** como en el campo **Precio unitario**. Si uno o estos dos campos están en blanco, puede ingresar un valor en este campo.| None |
| Impuesto sobre las ventas | Especifique el importe del impuesto sobre las ventas. | None |
| Importe total | El importe total de la línea de factura del proveedor, incluidos los impuestos. Este valor se calcula como *Subtotal* + *Impuestos*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
