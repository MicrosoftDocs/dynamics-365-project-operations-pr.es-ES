---
title: Administración de varios clientes en ofertas de proyectos
description: Este tema proporciona información sobre cómo trabajar en ofertas con varios clientes que financiarán el proyecto. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085048"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Administración de varios clientes en ofertas de proyectos (Ventas)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las ofertas del proyecto respaldan el escenario en el que la propuesta involucra a varios clientes que financiarán la oferta. La pestaña **Resumen** de la oferta tiene el campo **Cliente potencial** , que identifica al cliente principal de la oferta. Otros clientes de la oferta se pueden configurar en la pestaña **Clientes** de la oferta del proyecto.

Todos los clientes de oferta de la pestaña **Clientes** de la oferta del proyecto sirven de forma predeterminada como clientes de línea de oferta en cualquier **nueva** línea de oferta basada en el proyecto creada para la oferta. Las líneas de oferta existentes basadas en proyectos no heredarán los nuevos registros de clientes de oferta creados después de ellas.

Las líneas de oferta basadas en productos se asocian automáticamente al cliente principal que también es el cliente del campo **Cliente potencial** de la pestaña **Resumen** de la oferta.

Los clientes de oferta y los clientes de línea de oferta se pueden agregar, actualizar o eliminar en cualquier momento antes de ganar la oferta.

## <a name="concept-of-a-primary-customer"></a>Concepto de cliente principal

El cliente que está en la pestaña de resumen de la oferta del proyecto, ya que el cliente potencial es el cliente principal de la oferta. Al intentar eliminar el cliente principal de la lista de clientes de la oferta, aparecerá un error que indica que el registro de un cliente principal de una oferta no se puede eliminar.

El cliente principal no debe actualizarse de la lista de clientes de la oferta. Sin embargo, puede influir en el cliente principal cambiando al cliente potencial en la pestaña **Resumen** de la oferta. Cuando este campo se actualiza en el **Resumen de oferta** , el cliente potencial recién seleccionado se agrega como un nuevo cliente de oferta con el indicador **Primario** establecido. El antiguo cliente potencial seguirá siendo cliente de la oferta.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Crear, actualizar o eliminar un registro de cliente de oferta

Se puede crear, actualizar o eliminar un cliente de oferta desde la pestaña **Clientes de oferta** de la página **Oferta**. Los campos enumerados en la siguiente tabla están en el registro de cliente de oferta una oferta de proyecto.

| **Campo** | **Ubicación** | **Relevancia, propósito y orientación** | **Impacto posterior** |
| --- | --- | --- | --- |
| Cuenta | Cuadrícula editable de la pestaña **Clientes de oferta** y los formularios **Principal** y **Creación rápida** para un cliente de oferta. | Enumera todas las cuentas activas. Este campo se bloquea después de que se crea el registro. Si desea actualizarlo, elimine el registro y vuelva a crearlo. Si ha registrado datos reales, o si el registro del cliente de oferta es un cliente principal, se le permitirá eliminar el registro. | Los clientes de oferta se copian como clientes de la línea de oferta cuando se crea una línea de oferta. Los clientes de oferta también se copian en los clientes de contrato del proyecto cuando se gana una oferta. |
| Porcentaje de división de facturación | Cuadrícula editable de la pestaña **Clientes de oferta** y los formularios **Principal** y **Creación rápida** para un cliente de oferta. | Representa el porcentaje de cada transacción de venta no facturada que se atribuirá a este cliente de línea de oferta. | Copiado a las nuevas líneas de oferta y a los clientes del contrato del proyecto. |
| Facturar a nombre de contacto | Cuadrícula editable de la pestaña **Clientes de oferta** y los formularios **Principal** y **Creación rápida** para un cliente de oferta. | Este es un campo de texto y debe usarse para identificar a la persona de contacto de la factura para este cliente. Estos están predeterminados a partir del registro de cuenta relacionado | Se copia a los clientes del contrato del proyecto cuando se gana una oferta y, a su vez, al campo de nombre Facturar al contrato de la factura que se genera para este cliente. |
| Facturar a nombre | Cuadrícula editable de la pestaña **Clientes de oferta** y los formularios **Principal** y **Creación rápida** para un cliente de oferta. | Este campo de texto debe usarse para identificar a la persona de contacto de la factura para este cliente. | Se copia a los clientes del contrato del proyecto cuando se gana una oferta y, a su vez, al campo **Facturar al nombre de contrato** de la factura que se genera para este cliente. |
| Condiciones de pago | Cuadrícula editable de la pestaña **Clientes de oferta** y los formularios **Principal** y **Creación rápida** para un cliente de oferta. | Este es un conjunto de opciones con valores predeterminados del registro de la cuenta relacionada. | Se copia a los clientes del contrato del proyecto cuando se gana una oferta y, a su vez, al campo **Facturar al nombre de contrato** de la factura que se genera para este cliente. |
| Es redondeo | Cuadrícula editable de la pestaña **Clientes de oferta** y los formularios **Principal** y **Creación rápida** para un cliente de oferta. | Indica si este cliente es un cliente de redondeo predeterminado para esta oferta. | Se copia a los clientes de la línea de contrato del proyecto cuando se gana una oferta. |
| Límite a no exceder | Cuadrícula editable de la pestaña **Clientes de oferta** y los formularios **Principal** y **Creación rápida** para un cliente de oferta. | Indica si hay un límite negociado o un máximo para el importe total que se facturará a este cliente por este compromiso | Se copia a los clientes de la línea de contrato del proyecto cuando se gana una oferta. |

## <a name="editing-billing-split-percentages"></a>Edición de porcentajes de división de facturación

Puede editar los porcentajes de división de facturación utilizando la experiencia de edición de cuadrícula en línea. Cuando los porcentajes de división de facturación no suman el 100 %, se producirá un error. Después de actualizar los porcentajes de división de facturación, actualice la página para eliminar el error.

También puede intentar seleccionar **Distribuir uniformemente** en la subcuadrícula de los clientes de oferta. Esta acción asigna divisiones de facturación a todos los clientes de oferta. Si hay algún factor de redondeo, se agregará al cliente de redondeo. Uno de los clientes de oferta siempre se etiqueta como cliente de redondeo. Esto significa que el registro del cliente de oferta tiene el indicador **Redondeo** establecido en **Sí**. Por lo general, este es el cliente principal de la oferta, pero eso se puede cambiar.
