---
title: Líneas de subcontrato por tiempo
description: Este tema explica cómo registrar líneas de subcontratos para tiempo y registrar la compra de tiempo de los proveedores.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547265"
---
# <a name="subcontract-lines-for-time"></a>Líneas de subcontrato por tiempo

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Un subcontrato en Dynamics 365 Project Operations puede tener una línea de subcontrato para tiempo. Las líneas de subcontrato por tiempo permiten que un administrador del proyecto compre tiempo de recursos del proveedor para dotar de personal a las tareas del proyecto y los requisitos de recursos.

Para crear una línea de subcontrato de tiempo en Project Operations, complete los siguientes pasos.

1. En el panel de navegación, seleccione **Subcontratos** y abra un subcontrato.
2. En la pestaña **Líneas de subcontratación**, seleccione **Nueva** para crear una nueva línea de subcontrato.
3. En la página **Creación rápida**, en el campo **Clase de transacción**, seleccione **Tiempo**.
4. Especifique la información del campo restante y después haga clic en **Guardar**.

  La siguiente tabla proporciona información sobre los campos de la página **Línea de subcontrato** y la página **Creación rápida**.

| **Campo** | **Descripción** | **Impacto funcional** |
| --- | --- | --- |
| Asignar nombre | Nombre de la línea de subcontratación para ayudar con la identificación. | Esto se mostrará como la primera columna en todas las búsquedas basadas en líneas de subcontratación. |
| Descripción | Una breve descripción de los servicios que se compran en la línea de subcontrato. |Nada |
| Tipo de línea |   Este campo tiene un valor predeterminado de **Basado en cantidad**.| Nada |
| Método de facturación | Este es un conjunto de opciones que representa los dos principales modelos de contratación que admite Project Operations: **Precio fijo** y **Tiempo y material**. | Según el método de facturación seleccionado, se dispone de una programación de facturas basada en hitos para líneas de subcontratación con el método de facturación Precio fijo. |
| Clase de transacción | El valor predeterminado es **Tiempo**. | Esto indica que se está utilizando la línea de subcontratación para registrar una compra de tiempo de subcontratista. |
| Rol | Seleccione el rol de los recursos de subcontratación cuyo tiempo se está comprando. | El rol desempeñado por los recursos subcontratados determina el costo de la compra. |
| Inicio solicitado | Ingrese la fecha en la que se requieren los recursos del subcontratista para comenzar a trabajar. | Se utiliza para elegir una de las listas de precios del proyecto adjuntas al subcontrato. El costo del rol en la línea de subcontratación proviene de esa lista de precios. |
| Finalización solicitada | Ingrese la fecha en que finaliza la asignación del recurso del subcontratista. | Esto se usará para mostrar advertencias cuando un jefe de proyecto esté extrayendo capacidad para los requisitos de recursos que ocurren después de esta fecha. |
| Cantidad pedida | Ingrese el número de horas del rol que se compra al proveedor. | Esto se usará para mostrar advertencias cuando un jefe de proyecto esté extrayendo en exceso esta capacidad para los requisitos de recursos. |
| Unidad de venta | El valor predeterminado es **Unidad de venta de tiempo**, que no se puede cambiar. | Nada|
| Unidad | El valor predeterminado para este campo es la unidad base de horas de **Unidad de venta de tiempo**. Puede cambiar este valor para comprar cualquier unidad de **Unidad de venta de tiempo**, como día o semana. | La combinación de **Rol** y **Unidad** se utilizará como valor predeterminado o se calculará para el precio unitario de la línea de subcontratación. |
| Precio por unidad | El precio unitario predeterminado utiliza la combinación de **Rol** y **Unidad** de la lista de precios del proyecto aplicable para la fecha de **Inicio solicitado** de la línea de subcontratación. | Cuando la lista de precios del proyecto aplicable tiene el precio configurado en una unidad diferente a la unidad de la línea de subcontrato, el sistema usa la conversión de unidades para calcular el precio por unidad. |
| Subtotal |    Este es un campo de solo lectura que se calcula como Cantidad x Precio unitario, si se ingresan los valores de cantidad y precio unitario. Si la cantidad, el precio unitario, o ambos, están vacíos, puede ingresar un valor en el campo. | Nada|
| Impuesto sobre las ventas |   Especifique el importe del impuesto sobre las ventas. |Nada |
| Importe total | El importe total de la línea de subcontrato, impuestos incluidos. Este valor se calcula como Subtotal + Impuestos sobre ventas.|Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]