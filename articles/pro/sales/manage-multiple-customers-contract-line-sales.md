---
title: Administrar varios clientes en líneas de contratos basadas en proyectos (lite)
description: Este tema proporciona información sobre cómo administrar varios clientes en líneas de contrato basadas en proyectos.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f28e7d1363647621f7bd23504aa6d4ea3fc95fc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181675"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Administrar varios clientes en líneas de contratos basadas en proyectos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las líneas de contrato basadas en proyectos pueden incluir una lista de clientes responsables del pago. Esta lista de clientes en la línea de contrato basada en proyectos puede ser la misma que la lista de clientes en el contrato, pero no es obligatorio. Cuando se gana una cotización de proyecto y se crea un contrato de proyecto, la lista de clientes en la línea de cotización se copia en la línea de contrato correspondiente. Los clientes de la cotización se copian en el contrato.

Cuando se factura el contrato del proyecto, la lista de clientes en la línea de contrato basada en el proyecto tiene prioridad sobre la lista de clientes en el contrato. La lista de clientes en el contrato del proyecto solo se utiliza para predeterminar nuevas líneas de contrato.

Todos los clientes contratados en la pestaña **Clientes** del contrato de proyecto predeterminado como clientes de línea de contrato en cualquier nueva línea de contrato creada para el contrato de proyecto. Cualquier línea de contrato existente no heredará los nuevos registros de cliente de contrato creados después de ellos.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Crear, actualizar o eliminar un registro de cliente de línea de contrato

Puede crear, actualizar o eliminar un cliente de línea de contrato de la pestaña Clientes de la línea de contrato en la página Línea de contrato basada en proyectos. Cuando se agrega un nuevo cliente en la línea de contrato basada en el proyecto, también se agrega en el contrato general como un cliente de contrato con un porcentaje de división de facturación predeterminado del cero por ciento. El porcentaje de división de facturación del contrato general se copia en las nuevas líneas de contrato y en el contrato de proyecto eventual. Sin embargo, cuando se factura desde el contrato, lo que se utiliza es el porcentaje de división de facturación a nivel de línea de contrato y no el porcentaje de división de facturación a nivel de contrato general.

A continuación, se muestran los campos del registro de cliente de la línea de **Contrato** de una línea de contrato basada en un proyecto para tener en cuenta mientras trabaja con ella:

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| **Cuenta** | Cuadrícula editable en la pestaña **Clientes de contrato** y formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Todas las cuentas activas. Este campo se bloquea después de que se crea el registro. Para actualizar el campo, elimine el registro y cree uno nuevo. Si ha registrado datos reales, no puede eliminar el registro. Sin embargo, puede marcar el porcentaje de división de facturación como cero para esa cuenta. Cuando el registro se marca como cero, los costos e ingresos reales futuros que se atribuyen o dividen a este cliente se ven afectados. | Cuando elige una cuenta de la lista maestra de cuentas para agregarlas y guardarlas, el cliente de la línea de contrato también se agrega como cliente de contrato. Los clientes de la línea de contrato se utilizan cuando se generan las facturas. |
| **Porcentaje dividido de facturación** | Cuadrícula editable en la pestaña **Clientes de contrato** y formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Este campo representa el porcentaje de cada transacción de venta no facturada que se atribuirá a este cliente de línea de contrato. | Los clientes de línea de contrato y los porcentajes de división de facturación se utilizan cuando se crean datos reales después de la aprobación y cuando se genera la factura. |
| **Límite a no exceder** | Cuadrícula editable en la pestaña **Clientes de contrato** y formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Indica si hay un límite negociado o un tope para el monto total que se facturará a este cliente por la línea del contrato. | El límite de no exceder para el cliente de la línea de contrato se usa cuando se crean los datos reales y se generan las facturas. |
| **Es redondeo** | Cuadrícula editable en la pestaña **Clientes de contrato** y formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Este campo indica si este cliente es un cliente de redondeo predeterminado para esta línea de contrato basada en proyecto. | Cuando genera un real según el porcentaje de división de facturación, puede haber algunas diferencias de redondeo. A este cliente se le atribuyen las diferencias de redondeo en este caso. |

## <a name="edit-billing-split-percentages"></a>Editar porcentajes de división de facturación

Los porcentajes de división de facturación se pueden editar en la cuadrícula. Cuando los porcentajes de división de facturación no suman el 100 por ciento, se producirá un error. Después de editar los porcentajes de división de facturación, actualice la página para eliminar el error.

También puede seleccionar **Distribuir uniformemente** en la subcuadrícula del cliente de la línea de contrato. Esta acción asigna de manera uniforme las divisiones de facturación a todos los clientes de la línea de contrato. Si hay algún factor de redondeo, se agregará al cliente de redondeo. Un cliente de línea de contrato siempre se etiqueta como el cliente de **Redondeo** con la marca **Redondeo** establecida en **Sí**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]