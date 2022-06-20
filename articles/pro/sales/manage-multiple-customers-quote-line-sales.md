---
title: Administrar varios clientes en líneas de ofertas basadas en proyectos (lite)
description: Este artículo describe ćomo administrar varios clientes en líneas de ofertas basadas en proyectos.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fbd0c17de3de8dc4cd84860851fb5837b86586cd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927809"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Administrar varios clientes en líneas de ofertas basadas en proyectos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las líneas de oferta basadas en proyectos admiten escenarios en los que cada línea de oferta tiene una lista de clientes que la pagan. Esta lista de clientes de la línea de oferta basada en proyectos puede ser la misma que la lista de clientes de la oferta. También puede cambiar la lista de clientes para que sea diferente. Cuando se gana una oferta de proyecto, la lista de clientes de la línea de oferta basada en el proyecto se copia en la línea de contrato basada en proyecto para crear el contrato de proyecto eventual. Los clientes de la oferta basada en el proyecto se copian en el contrato del proyecto.

Cuando factura el contrato del proyecto eventual, la lista de clientes de la línea de contrato basada en el proyecto tiene prioridad sobre la lista del contrato del proyecto. La lista de clientes del contrato del proyecto solo se utilizan como predeterminadas en las nuevas líneas de contrato del proyecto.

Todos los clientes de oferta de la pestaña **Clientes** de la oferta del proyecto sirven de forma predeterminada como clientes de línea de oferta en cualquier nueva línea de oferta basada en el proyecto creada para la oferta del proyecto. Las líneas de oferta existentes basadas en proyectos no heredan los nuevos registros de clientes de oferta creados después de ellas.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Crear, actualizar o eliminar un registro de cliente de línea de oferta

Puede crear, actualizar o eliminar un cliente de línea de oferta en la pestaña **Clientes de línea de oferta** de la página **Línea de oferta basada en proyecto**. Cuando agrega un nuevo cliente en la línea de oferta basada en proyecto, el cliente también se agrega a la oferta general como cliente de oferta, con un porcentaje de división de facturación predeterminado sobre la oferta general del 0 %. El porcentaje de división de facturación de la oferta general se copia a las nuevas líneas de oferta y al contrato de proyecto eventual. Sin embargo, al facturar desde el contrato, se utiliza el porcentaje de división de facturación a nivel de línea de oferta, no el porcentaje de división de facturación a nivel de contrato general. 

La siguiente tabla muestra los campos del registro de cliente de línea de oferta de una línea de oferta basada en proyecto.

| Campo | Ubicación | Descripción y guía | Impacto posterior |
| --- | --- | --- | --- |
| **Cuenta** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta**, el formulario principal y los formularios de creación rápida para un cliente de línea de oferta. | Enumera todas las cuentas activas. Este campo se bloquea después de que se crea el registro. Si necesita actualizar el campo, elimine y vuelva a crear el registro. Si ha registrado datos reales, no puede eliminar el registro. | Cuando elige una cuenta de la lista maestra de cuentas para agregar, el cliente de la línea de oferta también se agrega como cliente de oferta al guardarlo. Al ganarse una oferta, los clientes de la línea de oferta se copian a los clientes de la línea de contrato del proyecto. |
| **Porcentaje de división de facturación** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta**, el formulario principal y los formularios de creación rápida para un cliente de línea de oferta. | Representa el porcentaje de cada transacción de venta no facturada que se atribuirá a este cliente de línea de oferta. | Copiado a los clientes de la línea de contrato del proyecto. |
| **Límite a no exceder** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta**, el formulario principal y los formularios de creación rápida para un cliente de línea de oferta. | Indica si hay un límite negociado o un máximo para el importe total que se facturará a este cliente por esta línea de oferta. | Se copia a los clientes de la línea de contrato del proyecto cuando se gana una oferta. |
| **Con redondeo** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta**, el formulario principal y los formularios de creación rápida para un cliente de línea de oferta. | Indica si este cliente es un cliente de redondeo predeterminado para esta línea de oferta basada en proyecto. | Se copia a los clientes de la línea de contrato del proyecto cuando se gana una oferta. |

## <a name="edit-billing-split-percentages"></a>Editar porcentajes de división de facturación

Puede editar los porcentajes de división de facturación en línea. Cuando los porcentajes de división de facturación no suman el 100 %, se produce un error. Después de editar los porcentajes de división de facturación, actualice la página de la línea de oferta para eliminar el error.

Utilice la acción de distribución uniforme en la subcuadrícula de clientes de la línea de oferta para asignar divisiones de facturación a todos los clientes de la línea de oferta. Si hay un factor de redondeo, se agregará al cliente de redondeo. Uno de los clientes de la línea de oferta siempre se etiqueta como el cliente de redondeo, lo que significa que el registro del cliente de la línea de oferta tiene el indicador de redondeo establecido en **Sí**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]