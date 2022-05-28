---
title: Líneas de factura de proveedor de tiempo
description: Este tema explica cómo registrar las líneas de factura del proveedor para los costos de tiempo que incluyen los subcontratistas.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ac598dff7b0b4a29ac0397a31130ada3b197fe44
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597221"
---
# <a name="vendor-invoice-lines-for-time"></a>Líneas de factura de proveedor de tiempo

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Una factura de proveedor en Microsoft Dynamics 365 Project Operations puede tener líneas de factura de proveedor por tiempo. Los administradores de proyecto pueden usar líneas de factura de proveedor por tiempo para registrar los costos del tiempo del subcontratista en los proyectos.

Las líneas de factura de proveedor por tiempo pueden o no hacer referencia a una línea de subcontrato por tiempo. Si una línea de factura de proveedor por tiempo hace referencia a un subcontrato, los administradores de proyectos podrán comparar y verificar el tiempo que factura la línea de factura del proveedor con el tiempo registrado por los subcontratistas y aprobado por los administradores de proyectos en el proyecto.

La siguiente tabla proporciona información sobre los campos de las líneas de factura de proveedor para el tiempo.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | El nombre de la línea de factura de proveedor, para ayudar con la identificación. | Este nombre se mostrará como la primera columna en todas las búsquedas basadas en líneas de factura de proveedor. |
| Description | Una breve descripción de los servicios que factura el proveedor en la línea de factura del proveedor. | None |
| Subcontrato | El subcontrato en el que se pidieron originalmente los servicios. | Cuando se selecciona un subcontrato para la factura del proveedor, todas las líneas de la factura del proveedor heredarán esa selección. Una factura de proveedor no puede tener líneas de factura de proveedor que hagan referencia a diferentes subcontratos. |
| Línea de subcontrato | La línea de subcontrato en la que se pidieron los servicios. La lista de líneas de subcontrato que se pueden seleccionar se limita a las líneas del subcontrato seleccionado. | Cuando se selecciona una línea de subcontrato en una línea de factura de proveedor por tiempo, los valores predeterminados para los campos **Proyecto**, **Rol** y **Recurso reservable** se ingresan desde los campos correspondientes de la línea de subcontrato. Si la línea de subcontrato seleccionada tiene valores en los campos **Proyecto**, **Rol** y **Reservable**, los valores de los campos correspondientes de la línea de factura del proveedor no pueden diferir de esos valores. |
| Fecha de la transacción | La fecha en que se registrará en el proyecto el costo real de la línea de factura del proveedor. | None |
| Clase de transacción | El valor predeterminado es **Tiempo**. | El valor **Tiempo** indica que la línea de factura del proveedor se está utilizando para registrar el importe de la factura del tiempo del subcontratista. |
| Project | El nombre del proyecto en el que se utilizaron los servicios que se están facturando. | Este campo es obligatorio y no se puede dejar en blanco. |
| Task | El nombre de la tarea del proyecto en la que se utilizaron los servicios que se están facturando. Este campo está disponible solo si se selecciona un proyecto. La selección de una tarea de proyecto es opcional. | Si este campo se deja en blanco, el director del proyecto puede hacer coincidir la línea de la factura del proveedor con el tiempo registrado por los recursos del subcontratista en cualquier tarea del proyecto. Si la línea de factura del proveedor no hace referencia a una línea de subcontrato y este campo se deja en blanco, el costo real creado por la línea de factura del proveedor no se vinculará a ningún dato real de ventas no facturado. En este caso, si se configura la facturación basada en tareas, es posible que los costos no se puedan facturar al cliente final. |
| Role | El rol de los recursos de subcontratista cuyo tiempo se está facturando. | Este campo especifica el rol que desempeñan los recursos de subcontratista cuyo tiempo se factura en la factura del proveedor. |
| Recurso que se puede reservar | El nombre del subcontratista cuyo tiempo se está facturando. La selección de los recursos reservables es opcional. | Si este campo se deja en blanco, el director del proyecto puede hacer coincidir la línea de la factura del proveedor con el tiempo registrado por cualquier recurso que pertenezca al proveedor en la línea de factura del proveedor. |
| Cantidad | Introduzca el número de horas de tiempo que factura el proveedor en la línea de factura. |None |
| Unidad de venta | El valor predeterminado es **Unidad de venta de tiempo** y no se puede cambiar. | None |
| Unidad | El valor predeterminado para esta unidad base de horas de la unidad de venta de tiempo. Puede cambiar este valor para comprar en cualquier unidad de la unidad de venta de tiempo, como día o semana. | La combinación de valores de **Rol** y **Unidad** se utilizará como valor predeterminado o calculado para el campo **Precio unitario** de la línea de factura de proveedor. |
| Precio unitario | El precio unitario predeterminado utiliza la combinación de los valores **Rol** y **Unidad** de la lista de precios del proyecto aplicable para la fecha de transacción de la línea de factura de proveedor. | Si el precio de la lista de precios del proyecto aplicable se configura en una unidad que difiere de la unidad en la línea de la factura del proveedor, el sistema usa la conversión de unidades para calcular el precio por unidad. |
| Subtotal | Este es un campo de solo lectura que se calcula como *Cantidad* &times; *Precio unitario*, si se ingresan los valores yanto en el campo **Cantidad** como en el campo **Precio unitario**. Si uno o estos dos campos están en blanco, puede ingresar un valor en este campo. | None |
| Impuesto sobre las ventas | Especifique el importe del impuesto sobre las ventas. | None |
| Importe total | El importe total de la línea de factura del proveedor, incluidos los impuestos. Este valor se calcula como *Subtotal* + *Impuestos*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
