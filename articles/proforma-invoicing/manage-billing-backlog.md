---
title: Administrar el trabajo pendiente de facturación
description: Este artículo proporciona información sobre cómo ver y trabajar con el trabajo pendiente de facturación en Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929399"
---
# <a name="manage-billing-backlog"></a>Administrar el trabajo pendiente de facturación

**Se aplica a**: Project Operations para escenarios basados en recursos/no mantenidos en existencias

Dynamics 365 Project Operations tiene vistas dedicadas para ayudar a administrar el trabajo pendiente de facturación. Para gestionar el retraso de facturación, seleccione los enlaces en el área **Ventas**, debajo de **Facturación**. 

Están disponibles las siguientes vistas:

- Anticipos y pagos a cuenta
- Anticipos y pagos a cuenta disponibles
- Hitos de precio fijo
- Trabajo pendiente de facturación de tiempo y material

## <a name="retainers-and-advances"></a>Anticipos y pagos a cuenta

La vista **Anticipos y pagos a cuenta** enumera todos los anticipos y pagos a cuenta de todos los contratos del proyecto. Después de facturar un anticipo o anticipo, el monto del anticipo está disponible para su uso.

## <a name="available-retainers-and-advances"></a>Anticipos y pagos a cuenta disponibles

La vista **Anticipos y pagos a cuenta disponibles** enumera todos los anticipos y pagos a cuenta disponibles de todos los contratos del proyecto del sistema. Después de facturar un anticipo o anticipo, el monto del anticipo está disponible para su uso y se agrega a la lista. Después de que el importe del anticipo o pago a cuenta se haya usado por completo, se eliminará de la lista.

## <a name="fixed-price-milestones"></a>Hitos de precio fijo

La vista **Hitos de precio fijo** enumera todos los hitos de precio fijo de todas las líneas de contrato del proyecto. Desde esta vista, los hitos únicos o múltiples se pueden marcar como **Listo para facturar** o **No está listo para facturar** en esta vista. Marcar un hito como **Listo para facturar** permite que pueda incluirse en un borrador de factura.

Cuando las líneas de contrato de varios clientes tienen un método de facturación de precio fijo, se crea un hito para cada cliente en la línea de contrato. Se puede crear un hito y luego dividirlo en registros de hitos individuales específicos del cliente. Esta división es interna y de acuerdo con la división porcentual de facturación definida para cada cliente en la línea de contrato. En la vista **Hitos de precio fijo**, verá los registros de hitos individuales específicos del cliente. Cada uno de estos registros de hitos se puede marcar como **Listo para facturar** por separado de esta vista. Cuando una o más de las divisiones de hitos relacionados se marcan como **Listo para facturar**, el estado del encabezado se actualiza a **En curso** desde **No iniciado**. Cuando se facturan todas las divisiones de hitos, el estado del hito del encabezado se actualiza a **Terminado**.

En esta vista se muestra un hito en un borrador de factura con un estado de facturación de **Factura de cliente creada**. Cuando se confirma el borrador de la factura, el estado de facturación en el registro se actualiza a **Factura de cliente registrada**. 

> [!NOTE] 
> No actualice este valor de estado mediante código personalizado. Project Operations no funciona correctamente cuando estos valores de estado se actualizan con código personalizado.

## <a name="time-and-material-billing-backlog"></a>Trabajo pendiente de facturación de tiempo y material

La vista **Backlog de facturación de tiempo y material** enumera todos los datos reales de ventas no facturados en todos los contratos de proyecto en el sistema que no se han facturado. Las ventas reales no facturadas únicas o múltiples se pueden marcar como **Lista para facturar** o **No está lista para facturar** desde esta vista. Marcar una venta real no facturada como **Lista para facturar** la pone a disposición para incluirla en un borrador de factura.

Los datos reales de ventas no facturadas con un estado **No exceder** de **Error** no se pueden marcar como **Listo para facturar**. Si los datos reales deben marcarse como **Listo para facturar**, restablezca el estado en otros datos reales en la línea de contrato que estén confirmados y luego vuelva a evaluar el estado **No exceder**.

Si las líneas de contrato de varios clientes tienen un método de facturación de tiempo y material, cuando se aprueban el tiempo y los gastos, se crea un real de ventas no facturadas para cada cliente en la línea de contrato de acuerdo con la división porcentual de facturación definida para cada uno de los clientes. En la vista **Backlog de facturación de tiempo y material**, verá estos datos reales de ventas no facturadas específicos del cliente. Cada uno de estos registros de ventas reales sin facturar se puede marcar como **Listo para facturar** por separado de esta vista.

En esta vista se muestra un dato real de ventas sin facturar que está en un borrador de factura con un estado de facturación **Factura del cliente creada**. Al confirmar el borrador de factura, el estado de facturación de este registro se actualiza a **Factura del cliente registrada**. 

> [!NOTE] 
> No actualice este valor de estado mediante código personalizado. Project Operations no funciona correctamente cuando estos valores de estado se actualizan con código personalizado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
