---
title: Detalles del encabezado para subcontratos
description: Este tema explica la funcionalidad proporcionada en el encabezado del subcontrato en Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501347"
---
# <a name="header-details-for-subcontracts"></a>Detalles del encabezado para subcontratos

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este tema explica la funcionalidad proporcionada en el encabezado del subcontrato en Dynamics 365 Project Operations.

Conforme un administrador de proyecto planifica y ejecuta proyectos, puede emplear subcontratistas y comprar productos y servicios de proveedores. Cuando un administrador de proyecto necesita comprar productos o servicios, puede crear un subcontrato en Project Operations.

Siga estos pasos para crear un subcontrato.

1. En el panel de navegación, seleccione **Subcontratos**, y en la página **Subcontratar**, seleccione **Nuevo**.
2. Especifique la información necesaria y después seleccione **Guardar**.

    La siguiente tabla proporciona información sobre los campos de la página **Encabezado del subcontrato**.

    | Campo | Descripción |Impacto funcional |
    |---|------|---| 
    | Asignar nombre | El nombre del subcontrato. | En todas las listas desplegables de subcontratos, el nombre del subcontrato aparece en la primera columna para ayudarlo a identificar el subcontrato. | 
    | Descripción | Una breve descripción de los servicios y productos que se compran en el subcontrato. | Nada |
    | Proveedor | El nombre de la empresa a la que se compran los productos y servicios. Este registro de cuenta tiene un tipo de relación de **Proveedor** o **Distribuidor**. | Según el proveedor seleccionado, los valores predeterminados se ingresan automáticamente para los siguientes campos:<br/> **• Divisa** </br> **• Listas de precios** </br> **• Condiciones de pago**</br> **• Dirección de pago**</br> **• Dirección de facturación**</br> **• Nombre de facturación** </br>**• Administrador de cuentas de proveedores**|
    | Fecha de subcontrato | La fecha de creación del subcontrato. | La fecha de subcontrato se utiliza para seleccionar la lista de precios de compra correcta, ya sea de las listas de precios que se adjuntan al proveedor relacionado o de los parámetros del proyecto. |
    | Razón para el estado | El estado del subcontrato. | El estado determina dónde se encuentra el subcontrato en el proceso empresarial y si se puede editar. <br/>Los valores incluyen:<br>• **Borrador**: el subcontrato se puede editar. Solo puede editar subcontratos con un estado de **Borrador**.<br/>• **Confirmado**: Se completa la negociación con el proveedor y se aprueba la entrega del subcontrato. <br/>• **Cerrado**: La entrega del subcontrato está completa.<br/>• **Cancelado**: El subcontrato fue cancelado y no está prevista la entrega.  | 
    | Moneda | Los divisa en la que se compran los productos y servicios. El valor predeterminado se ingresa automáticamente desde la cuenta del proveedor, pero se puede cambiar. | La divisa del subcontrato se utiliza para seleccionar la lista de precios de compra, ya sea de las listas de precios que se adjuntan al proveedor relacionado o de los parámetros del proyecto. Las listas de precios en otra moneda no se pueden asociar al subcontrato. El costo de tiempo, gastos y materiales que los recursos del proveedor entregan a partir de este subcontrato se registran en esta moneda en el proyecto. Una vez que se guarda el registro del subcontrato, la divisa del subcontrato no se puede cambiar.|
    | Unidad de contratación | La división de la empresa que está suscribiendo un contrato de compra o subcontrato con el proveedor. | Nada |
    | Condiciones de pago | Las condiciones de pago de las facturas de proveedor que se emiten en este subcontrato. El valor predeterminado se ingresa automáticamente desde el registro de la cuenta del proveedor, pero se puede cambiar. | Las condiciones de pago del subcontrato se copian en todas las facturas de proveedor relacionadas con este subcontrato. Las condiciones de pago se pueden actualizar si el subcontrato tiene un estado de **Borrador**. | 
    | Dirección de pago | La dirección del proveedor al que se deben enviar los pagos. El valor predeterminado se ingresa automáticamente desde el registro de la cuenta del proveedor, pero se puede cambiar. | La dirección de pago del subcontrato se copia como dirección de pago a todas las facturas de proveedor que se crean para este subcontrato. La dirección de pago se puede actualizar si el subcontrato tiene un estado de **Borrador**.|
    | Nombre de facturación | El nombre de la persona o división de la empresa del proveedor que enviará la factura. El valor predeterminado se ingresa automáticamente desde el registro de la cuenta del proveedor, pero se puede cambiar. | El valor **Nombre de facturación** del subcontrato se copia en todas las facturas de proveedor relacionadas con este subcontrato. Este campo se puede actualizar si el subcontrato tiene un estado de **Borrador**.|
    | Dirección de facturación | La dirección que se utiliza en las facturas del proveedor. El valor predeterminado se ingresa automáticamente desde el registro de la cuenta del proveedor, pero se puede cambiar. | Esta dirección es la dirección de "factura de" en las facturas de proveedor que se crean para este subcontrato. |
    | Subtotal | Si un subcontrato no tiene líneas, ingrese el subtotal del pedido antes de impuestos. Si el subcontrato tiene líneas, este campo es de solo lectura. El importe que se muestra es el importe del subtotal de todas las líneas del subcontrato. | Nada |
    | Impuesto total | Si un subcontrato no tiene líneas, ingrese los impuestos totales en este subcontrato. Si el subcontrato tiene líneas, este campo es de solo lectura. El importe que se muestra es la suma del importe de impuestos de todas las líneas del subcontrato. | Nada |
    | Importe total | Este campo calculado muestra el importe total del subcontrato después de incluir los impuestos. | Nada |
    | Fecha confirmada | La fecha de confirmación del subcontrato. | Nada |
    | Solicitado por | De forma predeterminada, este campo está configurado con el nombre del usuario que crea el subcontrato. Sin embargo, el creador del subcontrato puede cambiar el valor para indicar la persona en nombre de quien está creando el subcontrato. | Nada |
    | Administrador de cuentas de proveedores | El nombre del contacto principal de la cuenta del proveedor. El valor predeterminado se ingresa automáticamente desde el registro de la cuenta del proveedor, pero se puede cambiar. Puede seleccionar un contacto diferente como administrador de cuentas de proveedor del subcontrato. | Puede configurar alertas por correo electrónico para notificar al contacto cuando se realicen cambios en el subcontrato como resultado de las negociaciones de precios. |
