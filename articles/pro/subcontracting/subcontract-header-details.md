---
title: Detalles del encabezado para subcontratos
description: Este tema explica la funcionalidad proporcionada en el encabezado del subcontrato en Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323662"
---
# <a name="header-details-for-subcontracts"></a>Detalles del encabezado para subcontratos

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este tema explica la funcionalidad proporcionada en el encabezado del subcontrato en Dynamics 365 Project Operations.

Conforme un administrador de proyecto planifica y ejecuta proyectos, puede emplear subcontratistas y comprar productos y servicios de proveedores. Cuando un administrador de proyecto necesita comprar productos o servicios, puede crear un subcontrato en Project Operations.

Siga estos pasos para crear un subcontrato.

1. En el panel de navegación, seleccione **Subcontratos**, y en la página **Subcontratar**, seleccione **Nuevo**.
2. Especifique la información necesaria y después seleccione **Guardar**.

    La siguiente tabla proporciona información sobre los campos de la página de encabezado del subcontrato.

    | **Campo** | **Descripción** |
    | --- | --- | 
    | Asignar nombre | El nombre del subcontrato. |
    | Descripción | Una breve descripción de los servicios y productos que se compran en el subcontrato. |
    | Proveedor | El nombre de la empresa a la que se compran los productos y servicios. Este registro de cuenta tiene un tipo de relación de **Proveedor** o **Distribuidor**. |
    | Fecha de subcontrato | La fecha en que se crea el subcontrato. |
    | Razón para el estado | El estado del subcontrato. |
    | Divisa | La divisa en la que se compran los productos y servicios. El valor en este campo es el predeterminado de la cuenta del proveedor, pero se puede cambiar. Las listas de precios del proyecto que se utilizan para fijar el precio de productos y servicios en el subcontrato deben estar en esta divisa. Las listas de precios en cualquier otra divisa no se pueden asociar al subcontrato. El coste de los productos y servicios incurridos en este subcontrato se registrará en el proyecto en esta divisa. |
    | Unidad de contratación | La división de la empresa que está suscribiendo un contrato de compra o subcontrato con el proveedor. |
    | Condiciones de pago | Las condiciones de pago de las facturas de proveedor que se emiten en este subcontrato. El valor en este campo es el predeterminado del registro de cuenta del proveedor. |
    | Dirección de pago | La dirección a la que se envía el pago de las facturas de proveedor. El valor en este campo es el predeterminado del registro de cuenta del proveedor. |
    | Nombre de facturación | El nombre de la persona o división de la empresa del proveedor que enviará la factura. El valor en este campo es el predeterminado del registro de la cuenta del proveedor y se utilizará como el nombre del contacto principal en las facturas del proveedor creadas para este subcontrato. |
    | Dirección de facturación | La dirección utilizada en las facturas de este proveedor. El valor en este campo es el predeterminado del registro de cuenta del proveedor. Esta dirección también se utiliza como la dirección de la factura en las facturas de proveedor creadas para este subcontrato. |
    | Subtotal | Si un subcontrato no tiene líneas, introduzca un valor en este campo que denote el subtotal del pedido antes de impuestos. Si el subcontrato tiene líneas, este campo es de solo lectura. La cantidad que se muestra es la cantidad subtotal de todas las líneas del subcontrato. |
    | Impuesto total | Si un subcontrato no tiene líneas, introduzca un valor en este campo que denote los impuestos de este subcontrato. Si el subcontrato tiene líneas, este campo es de solo lectura. La cantidad que se muestra es la suma del importe de los impuestos de todas las líneas del subcontrato. |
    | Importe total |  Este campo calculado muestra el importe total del subcontrato después de incluir los impuestos.  |
    | Fecha confirmada | La fecha de confirmación del subcontrato.  |
    | Solicitado por | El valor de este campo toma como valor predeterminado el nombre del usuario que crea el subcontrato. El creador del subcontrato puede cambiar este valor para indicar la persona en nombre de la cual se está creando el subcontrato.  |
    | Administrador de cuentas de proveedores | El nombre del contacto principal de la cuenta del proveedor. El valor en este campo es el predeterminado del registro de cuenta del proveedor. El usuario puede cambiar este valor de campo para seleccionar un contacto diferente como el administrador de la cuenta del proveedor del subcontrato. Este contacto puede configurar y enviar alertas por correo electrónico y negociaciones de precios. |


