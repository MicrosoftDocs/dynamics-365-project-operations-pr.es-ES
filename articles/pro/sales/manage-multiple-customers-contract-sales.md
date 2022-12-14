---
title: Administrar varios clientes en contratos de proyectos
description: Este artículo proporciona información sobre cómo gestionar varios clientes en contratos de proyecto.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 001c3c822a5d1cef6bd85164ef5e63e81719dafb
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824554"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Administrar varios clientes en contratos de proyectos

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Los contratos de proyecto en Dynamics 365 Project Operations admiten el escenario en el que un acuerdo contractual involucra a varios clientes que están financiando un trato. La pestaña **Resumen** en la página **Contrato de proyecto** incluye el campo **Cliente**. Este campo identifica al cliente principal de la oferta. Otros clientes para el trato se pueden configurar en la pestaña **Clientes** de la página **Contrato de proyecto**.

Todos los clientes contratados en la pestaña Clientes del contrato de proyecto predeterminado como clientes de líneas de contrato en cualquier nueva línea de contrato basada en proyecto creada para el contrato de proyecto. Las líneas de contrato existentes basadas en proyectos no heredan nuevos clientes de contrato a medida que se crean nuevos registros.

Las líneas de contrato basadas en productos se asocian automáticamente al cliente principal.

Los clientes de contrato y los clientes de línea de contrato se pueden agregar, actualizar o eliminar en cualquier momento antes de que se gane el contrato.

## <a name="primary-customer"></a>Cliente principal

El cliente que figura en la pestaña **Resumen** del contrato del proyecto, ya que el cliente potencial es el cliente principal del contrato. Cuando intente eliminar el cliente principal de la lista de clientes en el contrato, recibirá un mensaje de error que indica que el registro de un cliente principal en un contrato no se puede eliminar.

El cliente principal no se puede actualizar desde la lista de clientes del contrato. En cambio, cambie el cliente potencial en la pestaña **Resumen** del contrato. Cuando este campo se actualiza en la página **Resumen del contrato**, el nuevo cliente se agrega como un nuevo cliente de contrato con el conjunto de indicadores **Primario**. El cliente principal anterior seguirá siendo un cliente del contrato.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Crear, actualizar o eliminar un registro de cliente de contrato

Un cliente por contrato puede crearse, actualizarse o eliminarse de la pestaña **Clientes** en la página **Contrato de proyecto**. Los campos de la siguiente tabla están en el registro del cliente del contrato de un contrato de proyecto y deben tenerse en cuenta mientras trabaja con el contrato.

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| **Cuenta** | La cuadrícula se puede editar en la pestaña **Clientes de contrato** y los formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Enumera todas las cuentas activas. Este campo se bloquea después de que se crea el registro. Para actualizar la cuenta, elimine el registro y cree uno nuevo. Si ha registrado datos reales o si el registro del cliente del contrato es un cliente principal, no puede eliminar el registro. | Los clientes de contrato se copian como clientes de línea de contrato cuando se crea una línea de contrato. |
| **Porcentaje dividido de facturación** | La cuadrícula se puede editar en la pestaña **Clientes de contrato** y los formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Representa el porcentaje de cada transacción de venta no facturada que se atribuirá a este cliente de línea de contrato. | Copiado en nuevas líneas de contrato y para proyectos de clientes de línea de contrato en nuevas líneas de contrato de proyecto. |
| **Facturar a nombre de contacto** | La cuadrícula se puede editar en la pestaña **Clientes de contrato** y los formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Este campo de texto debe usarse para identificar a la persona de contacto de la factura para este cliente. Este campo toma como valor predeterminado el registro de la cuenta relacionada. | Copiado al campo **Facturar al nombre del contrato** en la factura que se genera para este cliente. |
| **Nombre de facturación** | La cuadrícula se puede editar en la pestaña **Clientes de contrato** y los formularios **Principal** y **Creación rápida** para un cliente de contrato | Este campo de texto debe usarse para identificar a la persona de contacto de la factura para este cliente. Este campo toma como valor predeterminado el registro de la cuenta relacionada. | Copiado al campo **Facturar al nombre del contrato** en la factura que se genera para este cliente. |
| **Condiciones de pago** | La cuadrícula se puede editar en la pestaña **Clientes de contrato** y los formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Los valores se toman como predeterminados del registro de la cuenta relacionada. | Copiado al campo **Facturar al nombre del contrato** en la factura que se genera para este cliente. |
| **Es redondeo** | La cuadrícula se puede editar en la pestaña **Clientes de contrato** y los formularios **Principal** y **Creación rápida** para un cliente de línea de contrato. | Indica si este cliente es un cliente de redondeo predeterminado para esta oferta. Solo puede haber un cliente de redondeo en un contrato de proyecto. | Cuando el costo y las ventas no facturadas se dividen en la cantidad dan lugar a una diferencia de redondeo, esa diferencia se aplica al valor real que se asigna a este cliente. |
| **Límite a no exceder** | La cuadrícula se puede editar en la pestaña **Clientes de contrato** y los formularios **Principal** y **Creación rápida** para un cliente de contrato | Indica si hay un límite negociado o un tope para el monto total que se facturará al cliente para este contrato. | La configuración de **Límite de no exceder** establecida a nivel de cliente del contrato se evaluará en **Datos reales de ventas no facturadas** que hacen referencia a este cliente contratado. |

## <a name="edit-billing-split-percentages"></a>Editar porcentajes de división de facturación

Los porcentajes de división de facturación se pueden editar con la experiencia de edición de cuadrícula en línea. Cuando los porcentajes de división de facturación no suman el 100 por ciento, recibirá un error. Después de editar los porcentajes de división de facturación, actualice la página para omitir el error.

También puede seleccionar **Distribuir uniformemente** sobre la subcuadrícula **Clientes contractuales** para asignar las divisiones de facturación de manera uniforme a todos los clientes del contrato. Si hay un factor de redondeo, se agregará al cliente de redondeo. Uno de los clientes del contrato siempre se etiqueta como el cliente de **redondeo**, lo que significa que el registro del cliente del contrato tiene el indicador de redondeo establecido en **Sí**. Normalmente, este es el cliente principal del contrato, pero también se puede cambiar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
