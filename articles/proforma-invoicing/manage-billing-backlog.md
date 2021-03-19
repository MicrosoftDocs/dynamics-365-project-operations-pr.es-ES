---
title: Administrar el trabajo pendiente de facturación
description: Este tema proporciona información sobre cómo ver y trabajar con el trabajo pendiente de facturación en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c3752abd26e760d27320d2b86079d84a967d53cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287754"
---
# <a name="manage-the-billing-backlog"></a>Administrar el trabajo pendiente de facturación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations tiene dos vistas dedicadas para ayudarle a trabajar y a administrar la acumulación de facturación. Son **Hitos de precio fijo** y **Trabajo pendiente de facturación de tiempo y material** Para seleccionar una vista, en el área **Ventas** de Project Operations, en la página de navegación izquierda, seleccione **Facturación**. Los enlaces del trabajo pendiente de facturación se almacenan allí.

## <a name="fixed-price-milestones"></a>Hitos de precio fijo

Esta vista enumera todos los hitos de precio fijo en todas las líneas de contrato del proyecto en el sistema. Los hitos únicos o múltiples se pueden marcar como **Listo para facturar** o **No está listo para facturar** desde esta vista. Cuando marca un hito como **Listo para facturar**, el hito está disponible para un borrador de factura.

Cuando las líneas de contrato de varios clientes tienen un método de facturación de precio fijo, se crea un hito para cada cliente en la línea de contrato. El usuario crea un hito y ese hito se divide en registros de hitos específicos de cliente = internamente, de acuerdo con el porcentaje de facturación definido para cada cliente en la línea de contrato. En la vista **Hitos de precio fijo**, verá registros de hitos individuales específicos del cliente. Cada uno de estos registros de hitos se puede marcar como **Listo para facturar** por separado de esta vista. Cuando una o más de las divisiones de hitos relacionados se marcan como **Listo para facturar**, el encabezado pasa a un estado de **En progreso** desde **No empezado**. Cuando se hayan facturado todas las divisiones de hitos, el estado de hitos del encabezado pasa a ser **Terminado**.

En esta vista se muestra un hito en un borrador de factura con un estado de facturación de **Factura de cliente creada**. Cuando se confirma el borrador de la factura, el estado de facturación en este registro se actualiza a **Factura contabilizada**. No se recomienda actualizar este valor de estado mediante código personalizado. Project Operations no funcionará correctamente si estos valores de estado se actualizan con código personalizado.

## <a name="time-and-material-billing-backlog"></a>Trabajo pendiente de facturación de tiempo y material

Esta vista enumera todos los datos reales de ventas no facturados que no se han facturado en todos los contratos de proyecto en el sistema. Las ventas reales no facturadas únicas o múltiples se pueden marcar como **Lista para facturar** o **No está lista para facturar** desde esta vista. Marcar una venta real no facturada como **Lista para facturar** la pone a disposición para incluirla en un borrador de factura.

Datos reales de ventas no facturados que tienen un estado **Sin exceder** de **Ha fallado** no se pueden marcar como **Listo para facturar**. Si estos datos reales deben marcarse como tales, restablezca el estado en otros datos reales en la línea de contrato que están comprometidos y luego evalúe el estado **Sin exceder**.

En el caso de líneas de contrato de varios clientes que tienen un método de facturación de tiempo y material, cuando se aprueban el tiempo y los gastos, se crea una venta real no facturada para cada cliente en la línea de contrato de acuerdo con la división porcentual de facturación definida para cada cliente en el línea de contrato. En la vista **Trabajos pendientes de facturación de tiempo y material**, verá estos datos reales de ventas no facturados específicos del cliente. Cada uno de estos registros de ventas reales sin facturar se puede marcar como **Listo para facturar** por separado de esta vista.

Una venta real sin facturar en un borrador de factura aparece en esta vista con un **Estado de facturación** de **Factura de cliente creada**. Cuando se confirma el borrador de la factura, el estado de facturación en este registro se actualiza a **Factura de cliente contabilizada**. No se recomienda actualizar este valor usando un código personalizado cuando está en este estado. Project Operations no funcionará correctamente cuando estos valores de estado se actualizan con código personalizado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]