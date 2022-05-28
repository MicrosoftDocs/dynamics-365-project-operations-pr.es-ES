---
title: Administrar varios clientes en contratos de proyectos
description: Este tema proporciona información sobre cómo administrar varios clientes en un contrato de proyecto.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bf8b0d313b2b07924d730fe8923b05559bbcc244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591333"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Administrar varios clientes en contratos de proyectos

Este tema proporciona información sobre cómo administrar varios clientes en un contrato de proyecto. Puede utilizar un contrato de proyecto cuando se necesita un acuerdo contractual para varios clientes para financiar un trato. En la página **Contrato de proyecto**, la pestaña **Resumen** incluye información sobre el cliente principal para una oferta. Otros clientes que participan en la oferta se pueden agregar a la pestaña **Clientes**.

Todos los clientes contratados en la pestaña **Clientes** del contrato de proyecto predeterminado como clientes de línea de contrato en cualquier nueva línea de contrato basada en proyecto creada para el contrato de proyecto. Las líneas de contrato basadas en proyectos existentes no heredan nuevos registros de clientes de contrato que se crean posteriormente.

Puede agregar, actualizar o eliminar clientes de línea de contrato y contrato en cualquier momento antes de que se gane el contrato. Un cliente del contrato del proyecto debe configurarse como cliente en la empresa propietaria o entidad jurídica de la página **Clientes**. Las entidades jurídicas están configuradas en el módulo **Gestión de proyectos y contabilidad** de Dynamics 365 Project Operations y están disponibles como empresas en los módulos **Ventas de proyectos** y **Entrega** de Project Operations.

## <a name="primary-customers"></a>Clientes principales

El cliente potencial de la pestaña **Resumen** del contrato del proyecto es el cliente principal del contrato. No puede actualizar el cliente principal desde la lista de clientes del contrato. Si intenta eliminar el cliente principal de una lista de clientes del contrato, recibirá un mensaje de error que indica que no se puede eliminar el registro del cliente principal en un contrato. En lugar, cambie el cliente del campo **Cliente potencial** de la pestaña **Resumen** del contrato del proyecto. Cuando se actualiza este campo, el cliente recién seleccionado se agrega como un nuevo cliente de contrato con la marca **Primario** establecida en **Sí**. El cliente principal anterior sigue siendo un cliente en el contrato. Sin embargo, ya no es el cliente principal.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Crear, actualizar o eliminar un registro de cliente de contrato

Puede crear, actualizar o eliminar un cliente de contrato desde la pestaña **Clientes de contrato** en la página **Contrato**. Los siguientes campos se incluyen en el registro de cliente de contrato de un contrato de proyecto.

| **Campo** | **Ubicación** | **Descripción** | 
| --- | --- | --- | 
| Cuenta | Cuadrícula editable en la pestaña **Clientes de contrato** las páginas principal y de creación rápida para un cliente de contrato. | Enumera todas las cuentas activas. Este campo se bloquea después de que se crea el registro. Para actualizar el registro, tiene que eliminarlo y, a continuación, volverlo a crear. Si ha registrado datos reales o si el registro del cliente del contrato es un cliente principal, no puede eliminar el registro. Cuando se crea una línea de contrato, los clientes de contrato se copian como clientes de línea de contrato. |
| Porcentaje dividido de facturación | Cuadrícula editable en la pestaña **Clientes de contrato** las páginas principal y de creación rápida para un cliente de contrato. | Representa el porcentaje de cada transacción de venta no facturada que se atribuye al cliente de contrato. Cuando se crean nuevas líneas de contrato de proyecto, el porcentaje de división de facturación se copia en las nuevas líneas de contrato creadas y en los clientes de la línea de contrato de proyecto. |
| Facturar a nombre de contacto | Cuadrícula editable en la pestaña **Clientes de contrato** las páginas principal y de creación rápida para un cliente de contrato. | Este campo de texto debe usarse para identificar a la persona de contacto de la factura para el cliente. El valor predeterminado toma como predeterminado el registro de la cuenta relacionada. El nombre de contacto se copia en **Facturar al nombre del contrato** en la factura que se genera para el cliente. |
| Nombre de facturación | Cuadrícula editable en la pestaña **Clientes de contrato** las páginas principal y de creación rápida para un cliente de contrato. | Use este campo para identificar a la persona de contacto de la factura para el cliente. El valor predeterminado toma como predeterminado el registro de la cuenta relacionada. El nombre se copia en el campo **Facturar al nombre del contrato** en la factura que se genera para el cliente. |
| Condiciones de pago | Cuadrícula editable en la pestaña **Clientes de contrato** y las páginas principal y creación rápida para un cliente de contrato. | El valor predeterminado toma como predeterminado el registro de la cuenta relacionada. Los términos se copian a **Facturar al nombre del contrato** en la factura generada para el cliente. |
| Empresa propietaria | Cuadrícula editable en la pestaña **Clientes de contrato de proyecto** y las páginas principal y de creación rápida para un cliente de contrato de proyecto. | La entidad jurídica en la que está configurado el cliente en el módulo **Gestión de proyectos y contabilidad**. Este campo es de solo lectura y está configurado para la empresa propietaria del contrato de proyecto.</br>La lista de clientes para agregar en el campo **Cuenta** ya está filtrada a la lista de la empresa propietaria en el módulo **Gestión de proyectos y contabilidad** de Project Operations. La empresa propietaria es igual a la entidad jurídica en el módulo **Gestión de proyectos y contabilidad** de Project Operations. Todos los costes e ingresos derivados del proyecto se contabilizan en la contabilidad general de la empresa propietaria. |
| Es redondeo | Cuadrícula editable en la pestaña **Clientes de contrato** las páginas principal y de creación rápida para un cliente de contrato. | Indica si el cliente es un cliente de redondeo predeterminado para la oferta. Solo puede haber un cliente de redondeo en un contrato de proyecto. Cuando el coste y las ventas sin facturar se dividen en la cantidad y dan lugar a una diferencia de redondeo, esa diferencia se aplica al valor real que se asigna al cliente. |
| Límite de No exceder | Cuadrícula editable en la pestaña **Clientes de contrato** las páginas principal y de creación rápida para un cliente de contrato. | Indica si hay un límite negociado o un tope para el importe total que se facturará al cliente para el contrato. La configuración de Límite de no exceder establecida a nivel de cliente del contrato se evalúa en función de los datos reales de ventas no facturadas que hacen referencia al cliente de contrato. |

## <a name="edit-billing-split-percentages"></a>Editar porcentajes de división de facturación

Puede editar los porcentajes de división de facturación editando en la cuadrícula. Cuando los porcentajes de división de facturación no suman el 100 por ciento, se produce un error. Después de editar un porcentaje de división de facturación, actualice la página **Contrato de proyecto** para eliminar el error.

También puede seleccionar **Distribuir uniformemente** en la subcuadrícula de los clientes del contrato de proyecto. Las divisiones de facturación se asignan equitativamente a todos los clientes del contrato de proyecto. Si hay algún factor de redondeo, se agregará el factor al cliente de redondeo. Uno de los clientes del contrato siempre tiene la marca **Redondeo** establecida en **Sí**. Ese cliente es el cliente de redondeo. Normalmente, el cliente de redondeo también es el cliente principal del contrato, pero eso no es obligatorio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]