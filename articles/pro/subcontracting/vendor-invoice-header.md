---
title: Detalles de encabezados para facturas de proveedor
description: Este artículo explica la funcionalidad que se ofrece en el encabezado de facturas de proveedores de Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929879"
---
# <a name="header-details-for-vendor-invoices"></a>Detalles de encabezados para facturas de proveedor

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este artículo explica la funcionalidad que se ofrece en el encabezado de facturas de proveedores de Microsoft Dynamics 365 Project Operations.

Conforme los administradores de proyectos planean y ejecutan proyectos, podrían emplear subcontratistas y comprar productos y servicios a los proveedores. Durante la ejecución de un proyecto, se incurre en costes de servicios, materiales y categorías de gastos que se adquieren en subcontratos con proveedores. Los proveedores facturan estos costos a los proyectos mediante la creación de facturas de proveedores.

La siguiente tabla proporciona información sobre los campos en los encabezados de facturas de proveedores en Project Operations.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | Nombre de la factura de proveedor. | En todas las listas desplegables de facturas de proveedor, el nombre de la factura de proveedor aparece en la primera columna para ayudarle a identificar la factura de proveedor. Por defecto, cuando se crea una factura de proveedor a partir de un subcontrato, el campo **Nombre** de la factura de proveedor se establece en un valor que consiste en el nombre del subcontrato más la fecha actual. |
| Description | Una breve descripción de los servicios y productos que se facturan en la factura del proveedor. | None |
| Proveedor | El nombre de la empresa que está facturando los productos y servicios. Esta empresa debe ser un registro de cuenta que tenga un tipo de relación de **Proveedor** o **Suministrador**. | <p>Según el proveedor seleccionado, los valores predeterminados se ingresan automáticamente en los siguientes campos:</p><ul><li>Moneda</li><li>Listas de precios</li><li>Condiciones de pago</li><li>Dirección de pago</li></ul> |
| Subcontrato | Una referencia al subcontrato para la factura del proveedor. | <p>Según el subcontrato seleccionado, los valores predeterminados se ingresan automáticamente en los siguientes campos:</p><ul><li>Moneda</li><li>Listas de precios</li><li>Condiciones de pago</li><li>Dirección de pago</li></ul><p>El subcontrato que se selecciona en el encabezado de la factura del proveedor se ingresa de forma predeterminada en las líneas de la factura del proveedor y no se puede cambiar allí.</p> |
| Fecha de la factura | La fecha de los datos reales de costos que se crearán cuando se confirme la factura del proveedor. | La fecha de subcontrato también se utiliza para seleccionar la lista de precios de compra correcta, ya sea de las listas de precios que se adjuntan al proveedor relacionado o de los parámetros del proyecto. |
| Razón para el estado | El estado de la factura de proveedor. | <p>El estado determina dónde se encuentra la factura de proveedor en el proceso de negocio y si se puede editar. Estos son algunos de los valores disponibles:</p><ul><li>**Borrador**: la factura de proveedor se puede editar.</li><li>**Confirmado**: la factura del proveedor se verificó y confirmó. Las facturas de proveedor en este estado no pueden editarse ni eliminarse.</li><li>**En proceso**: la factura del proveedor está siendo revisada. Las facturas de proveedor en este estado pueden editarse, pero no eliminarse.</li><li>**Cancelado**: la factura del proveedor se canceló. Las facturas de proveedor en este estado no pueden editarse ni eliminarse.</li></ul> |
| Moneda | La moneda en la que el proveedor está facturando los productos y servicios en la factura del proveedor. | En una factura de proveedor que hace referencia a un subcontrato, la moneda del subcontrato se ingresa de manera predeterminada como la moneda de la factura del proveedor. En una factura de proveedor que no hace referencia a un subcontrato, el valor predeterminado se ingresa desde el registro de la cuenta del proveedor y se puede cambiar. Después de guardar una factura de proveedor, la moneda ya no se puede editar. |
| Unidad de contratación | La división de la empresa que es responsable de recibir los servicios y/o productos del proveedor. | None |
| Condiciones de pago | Las condiciones de pago de las facturas de proveedor que se emiten. El valor predeterminado se ingresa automáticamente desde el registro de la cuenta del proveedor, pero se puede cambiar. | Las condiciones de pago de un subcontrato se copian en todas las facturas de proveedor relacionadas con el subcontrato. Las condiciones de pago se pueden actualizar si la factura del proveedor tiene un estado de **Borrador**. |
| Dirección de pago | La dirección del proveedor al que se deben enviar los pagos. El valor predeterminado se ingresa automáticamente desde el registro de la cuenta del proveedor, pero se puede cambiar. | La dirección de pago de un subcontrato se copia como dirección de pago a todas las facturas de proveedor que se crean para este subcontrato. La dirección de pago puede actualizarse si la factura del proveedor tiene un estado de **Borrador**. |
| Subtotal | Si la factura de proveedor no tiene líneas, ingrese el subtotal de la factura antes de impuestos. Si la factura del proveedor tiene líneas, este campo es de solo lectura. En este caso, el importe que se muestra es el importe del subtotal de todas las líneas de la factura del proveedor. | None |
| Impuesto total | Si la factura de proveedor no tiene líneas, ingrese el total de impuestos del subcontrato. Si la factura del proveedor tiene líneas, este campo es de solo lectura. En este caso, el importe que se muestra es la suma de importes de impuestos de todas las líneas de la factura del proveedor. | None |
| Importe total | Este campo calculado muestra el importe total de la factura del proveedor después de incluir los impuestos. | None |

> [!NOTE]
> Los siguientes campos de una factura de proveedor no se pueden cambiar después de guardar la factura de proveedor: **Proveedor**, **Subcontrato**, **Divisa**, **Unidad de contratación** y **Términos de pago**. Si se requieren cambios en estos campos de una factura de proveedor, debe eliminar la factura de proveedor y crear una nueva factura de proveedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
