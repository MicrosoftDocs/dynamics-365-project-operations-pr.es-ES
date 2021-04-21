---
title: Administrar el trabajo pendiente de facturación de proyectos
description: Este tema proporciona información sobre las diversas vistas disponibles para usar cuando se administra el trabajo pendiente de facturación de proyectos.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25dc9cff6aeb6daed9a27ba843a74b892ca4751c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867017"
---
# <a name="manage-project-billing-backlog"></a>Administrar el trabajo pendiente de facturación de proyectos 

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Dynamics 365 Project Operations tiene vistas dedicadas para ayudar a administrar el trabajo pendiente de facturación. Para gestionar el retraso de facturación, seleccione los enlaces en el área **Ventas**, debajo de **Facturación**. 

Están disponibles las siguientes vistas:

- Anticipos y pagos a cuenta
- Anticipos y pagos a cuenta disponibles
- Hitos de precio fijo
- Trabajo pendiente de facturación de productos
- Trabajo pendiente de facturación de tiempo y material

## <a name="retainers-and-advances"></a>Anticipos y pagos a cuenta

La vista **Anticipos y pagos a cuenta** enumera todos los anticipos y avances en todos los contratos de proyectos del sistema. Después de facturar un anticipo o anticipo, el monto del anticipo está disponible para su uso.

## <a name="available-retainers-and-advances"></a>Anticipos y pagos a cuenta disponibles

La vista **Anticipos y pagos a cuenta disponibles** enumera todos los anticipos y avances disponibles en todos los contratos de proyectos del sistema. Después de facturar un anticipo o anticipo, el monto del anticipo está disponible para su uso y se agrega a la lista. Después de que la cantidad del anticipo o anticipo se haya usado por completo, se elimina de la lista.

## <a name="fixed-price-milestones"></a>Hitos de precio fijo

La vista **Hitos de precio fijo** enumera todos los hitos de precio fijo en todas las líneas de contrato del proyecto en el sistema. Los hitos únicos o múltiples se pueden marcar como **Listo para facturar** o **No está listo para facturar** en esta vista. Marcar un hito como **Listo para facturar** lo pone a disposición para incluirlo en un borrador de factura.

Cuando las líneas de contrato de varios clientes tienen un método de facturación de precio fijo, se crea un hito para cada cliente en la línea de contrato. Se puede crear un hito y luego dividirlo en registros de hitos individuales específicos del cliente. Esta división es interna y de acuerdo con la división porcentual de facturación definida para cada cliente en la línea de contrato. En la vista **Hitos de precio fijo**, verá los registros de hitos individuales específicos del cliente. Cada uno de estos registros de hitos se puede marcar como **Listo para facturar** por separado de esta vista. Cuando una o más de las divisiones de hitos relacionados se marcan como **Listo para facturar**, el estado del encabezado se actualiza a **En progreso** desde **No empezado**. Cuando se facturan todas las divisiones de hitos, el estado del hito del encabezado se actualiza a **Terminado**.

En esta vista se muestra un hito en un borrador de factura con un estado de facturación de **Factura de cliente creada**. Cuando se confirma el borrador de la factura, el estado de facturación en el registro se actualiza a **Factura de cliente registrada**. No actualice este valor de estado utilizando código personalizado. Project Operations no funciona correctamente cuando estos valores de estado se actualizan con código personalizado.

## <a name="product-billing-backlog"></a>Trabajo pendiente de facturación de productos

La vista **Backlog de facturación del producto** enumera todas las líneas de contrato basadas en productos en todos los contratos de proyecto en el sistema. Las líneas de contrato basadas en el producto únicas o múltiples se pueden marcar como **Listo para facturar** o **No está listo para facturar** en esta vista. Marcar una línea de contrato basada en el producto como **Listo para facturar** permite que pueda incluirse en un borrador de factura.

En esta vista se muestra una línea de contrato basada en el producto que está en un borrador de factura con un estado de facturación **Factura del cliente creada**. Cuando se confirma el borrador de la factura, el estado de facturación en este registro se actualiza a **Factura de cliente contabilizada**. No actualice este valor de estado utilizando código personalizado. Project Operations no funciona correctamente cuando estos valores de estado se actualizan con código personalizado.

## <a name="time-and-material-billing-backlog"></a>Trabajo pendiente de facturación de tiempo y material

La vista **Backlog de facturación de tiempo y material** enumera todos los datos reales de ventas no facturados en todos los contratos de proyecto en el sistema que no se han facturado. Las ventas reales no facturadas únicas o múltiples se pueden marcar como **Lista para facturar** o **No está lista para facturar** desde esta vista. Marcar una venta real no facturada como **Lista para facturar** la pone a disposición para incluirla en un borrador de factura.

Los datos reales de ventas no facturadas con un estado **No exceder** de **Error** no se pueden marcar como **Listo para facturar**. Si los datos reales deben marcarse como **Listo para facturar**, restablezca el estado de otros datos reales en la línea de contrato que están comprometidos. y luego vuelva a evaluar el estado de **No exceder**.

Si las líneas de contrato de varios clientes tienen un método de facturación de tiempo y material, cuando se aprueban el tiempo y los gastos, se crea un real de ventas no facturadas para cada cliente en la línea de contrato de acuerdo con la división porcentual de facturación definida para cada uno de los clientes. En la vista **Backlog de facturación de tiempo y material**, verá estos datos reales de ventas no facturadas específicos del cliente. Cada uno de estos registros de ventas reales sin facturar se puede marcar como **Listo para facturar** por separado de esta vista.

Un valor real de ventas no facturado que está en un borrador de factura con un estado de facturación de **Factura de cliente creada**. Cuando se confirma el borrador de la factura, el estado de facturación en este registro se actualiza a **Factura de cliente contabilizada**. No actualice este valor de estado utilizando código personalizado. Project Operations no funciona correctamente cuando estos valores de estado se actualizan con código personalizado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
