---
title: Administrar varios clientes en líneas de ofertas basadas en proyectos
description: En este tema se proporciona información sobre cómo administrar varios clientes en líneas de oferta basadas en proyectos.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea7f0a8207fc78914783f5b9c919b3243a0bb5a4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085024"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Administrar varios clientes en líneas de ofertas basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las líneas de oferta basadas en proyectos admiten escenarios en los que cada línea de oferta tiene una lista de clientes que la pagan. Esta lista de clientes de la línea de oferta basada en proyectos puede ser la misma que la lista de clientes de la oferta. También puede cambiar la lista de clientes para que sea diferente. Para crear el contrato de proyecto eventual cuando se gana una oferta de proyecto, la lista de clientes de la línea de oferta basada en el proyecto se copia en la línea de contrato basada en el proyecto correspondiente. Los clientes de la oferta basada en el proyecto se copian en el contrato del proyecto.

Cuando factura el contrato del proyecto eventual, la lista de clientes de la línea de contrato basada en el proyecto tiene prioridad sobre la lista del contrato del proyecto. La lista de clientes en el contrato del proyecto solo se utiliza para las nuevas líneas de contrato del proyecto predeterminadas.

Todos los clientes de oferta de la pestaña **Clientes** de la oferta del proyecto sirven de forma predeterminada como clientes de línea de oferta en cualquier nueva línea de oferta basada en el proyecto creada para la oferta del proyecto. Las líneas de oferta existentes basadas en proyectos no heredan los nuevos registros de clientes de oferta creados después de ellas.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Crear, actualizar o eliminar un registro de cliente de línea de oferta

Puede crear, actualizar o eliminar un cliente de línea de oferta en la pestaña **Clientes de línea de oferta** de la página **Línea de oferta basada en proyecto**. Cuando agrega un nuevo cliente en la línea de oferta basada en proyecto, el cliente también se agrega a la oferta general como cliente de oferta, con un porcentaje de división de facturación predeterminado sobre la oferta general del 0 %. El porcentaje de división de facturación de la oferta general se copia a las nuevas líneas de oferta y al contrato de proyecto eventual. Sin embargo, cuando factura desde el contrato, se utiliza el porcentaje de división de facturación a nivel de línea de oferta, no el porcentaje de división de facturación a nivel de contrato general. 

La siguiente tabla muestra los campos del registro de cliente de línea de oferta de una línea de oferta basada en proyecto.

| Campo | Ubicación | Descripción y guía | Impacto posterior |
| --- | --- | --- | --- |
| **Cuenta** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta** , el formulario principal y el formulario de creación rápida para un cliente de línea de oferta. | Enumera todas las cuentas activas. Este campo se bloquea después de que se crea el registro. Si necesita actualizar el campo, elimine y vuelva a crear el registro. Si ha registrado datos reales, no puede eliminar el registro. | Cuando elige una cuenta de la lista maestra de cuentas para agregar, el cliente de la línea de oferta también se agrega como cliente de oferta. Los clientes de la línea de oferta se copian a los clientes de la línea de contrato del proyecto cuando se gana una oferta. |
| **Porcentaje de división de facturación** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta** , el formulario principal y el formulario de creación rápida para un cliente de línea de oferta. | Representa el porcentaje de cada transacción de venta no facturada que se atribuirá a este cliente de línea de oferta. | Copiado a los clientes de la línea de contrato del proyecto. |
| **Límite a no exceder** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta** , el formulario principal y el formulario de creación rápida para un cliente de línea de oferta. | Indica si hay un límite negociado o un máximo para el importe total que se facturará a este cliente por esta línea de oferta. | Se copia a los clientes de la línea de contrato del proyecto cuando se gana una oferta. |
| **Empresa propietaria** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta** , el formulario principal y el formulario de creación rápida para un cliente de línea de oferta. | La entidad legal en la que este cliente está configurado en el módulo **Gestión de proyectos y contabilidad**. Este campo es de solo lectura y está configurado para la propia empresa propietaria de la oferta. La lista de clientes para agregar en el campo **Cuenta** ya está filtrada a la lista de la empresa propietaria en el módulo **Gestión de proyectos y contabilidad** de Project Operations. | La empresa propietaria equivale al concepto de entidad jurídica. Todos los costes e ingresos derivados de este proyecto se contabilizan en el libro mayor de la empresa propietaria. |
| **Con redondeo** | Una cuadrícula editable en la pestaña **Clientes de línea de oferta** , el formulario principal y el formulario de creación rápida para un cliente de línea de oferta. | Indica si este cliente es un cliente de redondeo predeterminado para esta línea de oferta basada en proyecto. | Se copia a los clientes de la línea de contrato del proyecto cuando se gana una oferta. |

## <a name="edit-billing-split-percentages"></a>Editar porcentajes de división de facturación

Puede editar los porcentajes de división de facturación en línea. Cuando los porcentajes de división de facturación no suman el 100 %, se produce un error. Después de editar los porcentajes de división de facturación, actualice la página de la línea de oferta para eliminar el error.

Utilice la acción de distribución uniforme en la subcuadrícula de clientes de la línea de oferta para asignar divisiones de facturación a todos los clientes de la línea de oferta. Si hay un factor de redondeo, se agregará al cliente de redondeo. Uno de los clientes de la línea de oferta siempre se etiqueta como el cliente de redondeo, lo que significa que el registro del cliente de la línea de oferta tiene el indicador de redondeo establecido en **Sí**. 
