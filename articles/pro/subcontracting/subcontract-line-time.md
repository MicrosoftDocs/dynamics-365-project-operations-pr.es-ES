---
title: Líneas de subcontrato por tiempo
description: Este tema explica cómo registrar líneas de subcontratos para tiempo y registrar la compra de tiempo de los proveedores.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323887"
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

| **Campo** | **Descripción** |
| --- | --- |
| Asignar nombre | El nombre de la línea de subcontratación. |
| Descripción | Una breve descripción de los servicios que se compran en la línea de subcontrato. | 
| Tipo de línea | Este campo es un valor predeterminado.  |
| Método de facturación | Seleccione el método de facturación. Según el método de facturación de la línea de subcontrato referenciada, se pone a disposición un programa de facturación basado en hitos para el método de facturación de precio fijo. |
| Clase de transacción | Este campo es un valor predeterminado que indica si la línea de subcontrato se está utilizando para registrar una compra de tiempo de subcontratista. |
| Rol | El rol de los recursos subcontratados cuyo tiempo se está comprando. El rol asignado a los recursos del subcontrato determina el coste de la compra. |
| Inicio solicitado | La fecha en la que se requieren los recursos del subcontratista para comenzar a trabajar. El inicio solicitado se utiliza para elegir una lista de precios del proyecto de las listas de precios del proyecto adjuntas al subcontrato. El coste del rol en la línea de subcontrato luego se establece por defecto en esa lista de precios. |
| Finalización solicitada | La fecha en la que finaliza la asignación de los recursos del subcontratista. Esta fecha se usa para mostrar advertencias cuando un administrador del proyecto está aprovechando esta capacidad para los requisitos de recursos que se producen después de esta fecha. |
| Cantidad pedida | El número de horas de rol que se compran al proveedor. Este valor se usa para mostrar advertencias cuando un administrador del proyecto está aprovechando en exceso esta capacidad para los requisitos de recursos. |
| Unidad de venta | El valor predeterminado de este campo es el grupo de unidades de tiempo, y no se puede cambiar.  |
| Unidad | Este campo tiene como valor predeterminado la unidad base de horas del grupo de unidades de tiempo. Puede cambiar este valor para comprar cualquier unidad del grupo de unidades de tiempo, como día o semana. La combinación de rol y unidad se utiliza para calcular el precio unitario de la línea de subcontrato. |
| Precio por unidad | El precio unitario se predetermina a partir de la combinación de rol y unidad, a partir de la lista de precios del proyecto que es aplicable para la fecha de inicio solicitada de la línea de subcontrato. Cuando la lista de precios del proyecto aplicable tiene el precio configurado en una unidad diferente a la unidad de la línea de subcontrato, el sistema usa la conversión de unidades para calcular el precio por unidad. |
| Subtotal | Este es un campo de solo lectura que se calcula automáticamente como **Cantidad x Precio unitario** si se ingresan los valores de cantidad y precio unitario. Si la cantidad, el precio unitario, o ambos, están vacíos, puede ingresar un valor en el campo. |
| Impuesto sobre las ventas |  Especifique el importe del impuesto sobre las ventas. |
| Importe total | El importe total de la línea de subcontrato después de incluir los impuestos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
