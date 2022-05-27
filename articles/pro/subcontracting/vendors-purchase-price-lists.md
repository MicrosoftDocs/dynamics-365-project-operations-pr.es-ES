---
title: Administración de lista de precios de compra y proveedores en Project Operations
description: Este tema proporciona información que le ayudará a crear y mantener datos de proveedores y listas de precios de compra para la subcontratación.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576751"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Administración de lista de precios de compra y proveedores en Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

## <a name="vendors-in-project-operations"></a>Proveedores en Project Operations

En Microsoft Dynamics 365 Project Operations, las cuentas de proveedores tienen un tipo de relación de **Proveedor** o **Distribuidor**. Puede seleccionar solo un registro de cuenta que tenga uno de estos tipos de relación como proveedor en un subcontrato.

Puede asociar una o más listas de precios de compra con un registro de proveedor. Sin embargo, cada lista de precios de compra asociada a un registro de proveedor debe tener una fecha de vigencia distinta. En Project Operations no se admite la superposición de validez de fechas en las listas de precios de compra.

De forma predeterminada, los siguientes campos y conceptos en un registro de proveedor se utilizan para cualquier subcontrato que se crea para el proveedor:

- Condiciones de pago
- Contacto de facturación
- Contacto principal

    > [!NOTE]
    > De forma predeterminada, el contacto principal del proveedor se utiliza como administrador de cuentas del proveedor del subcontrato.

- Moneda
- Listas de precios de compra actuales

## <a name="purchase-price-lists-in-project-operations"></a>Listas de precios de compra en Project Operations

Una lista de precios donde el campo **Contexto** esté establecido en **Compra** se considera una lista de precios de compra. Las listas de precios de compra se pueden definir para representar un catálogo de tarifas de compra por tiempo, gastos y materiales. Las listas de precios de compra se asemejan a las listas de precios de costes y ventas en Project Operations. Los siguientes conceptos se aplican a las listas de precios de compras de la misma manera que se aplican a las listas de precios de costes y ventas:

- **Fecha de vigencia** – Las listas de precios de compra tienen fecha de vigencia. La fecha de vigencia está representada por los campos de fecha de inicio y fecha de finalización en cada lista de precios. El tiempo entre la fecha de inicio y la fecha de finalización es el período de vigencia de la fecha.
- **Moneda** – La moneda en el encabezado de la lista de precios se usa como la moneda en la que se expresan los precios de compra para mano de obra, categorías de gastos y productos en el catálogo.
- **Unidad de tiempo predeterminada** – La unidad de tiempo predeterminada expresa los precios laborales para las compras. El campo de unidad de tiempo en una lista de precios se usa solo para proporcionar un valor predeterminado. Ese valor se puede cambiar en filas de precios de roles individuales.

Las listas de precios de compras se pueden adjuntar a los registros de proveedores como asociaciones que se conocen como listas de precios de proyectos. Estas listas de precios se utilizan para introducir precios predeterminados en líneas de subcontratos. De forma predeterminada, cuando se adjuntan varias listas de precios de compra a un registro de proveedor, se utiliza la lista de precios más actual para los subcontratos que se crean para el proveedor. Solo listas de precios donde el campo **Contexto** esté establecido en **Compra** se puede adjuntar a los registros de proveedores.

### <a name="subcontract-specific-purchase-price-lists"></a>Listas de precios de compra específicas de subcontratos

Las listas de precios de compras también se pueden adjuntar a los subcontratos como asociaciones que se conocen como listas de precios de proyectos. Estas listas de precios se utilizan para introducir precios predeterminados en líneas de subcontratos. De forma predeterminada, cuando se adjuntan varias listas de precios de compra a un subcontrato, cada una debe tener una fecha de vigencia distinta. En Project Operations no se admite listas de precios de compra con superposición de validez de fechas. Solo listas de precios donde el campo **Contexto** esté establecido en **Compra** se puede adjuntar a los subcontratos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
