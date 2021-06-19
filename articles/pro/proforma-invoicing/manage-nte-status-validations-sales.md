---
title: Administrar los estados y validaciones que no se deben superar
description: Este tema proporciona información sobre las comprobaciones de límite que no deben superarse realizadas en Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d51a61e441b004ae836037aefa172fdd20ac83ed
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003922"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Administrar los estados y validaciones que no se deben superar 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

## <a name="not-to-exceed-on-approvals"></a>No exceder en aprobaciones

Cuando se envía una entrada de tiempo, gasto o uso de material, se crea un registro de aprobación. Si la aprobación es imputable y se asigna a una línea de contrato de tiempo y material, el sistema completa una verificación de validación de no exceder en los siguientes niveles:

  - Verifique el límite establecido para el cliente en la línea del contrato del proyecto
  - Verifique el límite establecido en la línea del contrato
  - Verifique el límite establecido para el cliente
  - Verifique el límite establecido en el contrato

Las verificaciones en cada nivel implican garantizar que el monto del valor de las ventas en esta aprobación no violará el límite de no exceder en ese nivel después de contabilizar el monto del atraso de facturación ya registrado y el monto facturado hasta la fecha en ese nivel.

Si la verificación pasa, la aprobación recibe un estado de validación de **Éxito**.

Si la verificación falla, la aprobación recibe un estado de validación de **Error**. El detalle de la validación de no exceder informará al usuario en qué nivel falló la validación.

Cuando la entrada de tiempo, gasto o uso de material enviada se considera no imputable, el estado de validación de no exceder se establece en **No aplicable** con el detalle de validación igual a **No aplicable**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>No exceder los datos reales de ventas no facturadas

Cuando se aprueba una entrada de tiempo, gasto o uso de material, se crean registros de datos reales de costes y ventas no facturadas. Si el valor de venta real no facturado es imputable y se asigna a una línea de contrato de tiempo y material, la aplicación realiza una verificación de validación de no exceder en los siguientes niveles:

  - Verifique el límite establecido para el cliente en la línea del contrato del proyecto
  - Verifique el límite establecido en la línea del contrato
  - Verifique el límite establecido para el cliente
  - Verifique el límite establecido en el contrato

Las verificaciones en cada nivel garantizan que el monto del valor de las ventas en el valor real no violará el límite de no exceder en ese nivel después de contabilizar el monto del atraso de facturación ya registrado y el monto facturado hasta la fecha en ese nivel.

Si el cheque pasa, las ventas reales no facturadas reciben un estado de no exceder de **Comprometido**.

Si la comprobación falla, las ventas reales no facturadas reciben un estado de no exceder de **Error**. El detalle de la validación informa al usuario en qué nivel falló la validación.

Cuando las ventas reales no facturadas se consideran gratuitas o complementarias, si no hay una configuración de límite que no se exceda en ninguno de los cuatro niveles, o si el valor real que se crea es el costo, la retención, la unidad de recursos o las ventas entre organizaciones, los campos **Estado de no exceder** y **Detalle de validación que no debe exceder** deben establecerse en **No aplica**.

## <a name="reset-the-not-to-exceed-status"></a>Restablecer del estado de no exceder

Puede realizar un restablecimiento masivo del estado de no exceder. Los directores de proyecto pueden ajustar la validación de no exceder para priorizar la facturación de un trabajo en particular, tiempo, gasto o uso de material sobre otros que ya están comprometidos a partir de la cantidad de no exceder disponible.

Una vez que se restablece el estado de no exceder en los datos reales de ventas no facturadas, se reduce el monto comprometido. El director de proyectos puede seleccionar otra entrada de trabajo, tiempo, gasto o uso de material que no haya superado previamente la validación de no exceder y volver a evaluar. Con la reducción en la cantidad comprometida, estos datos reales ahora pasan la validación, lo que ayuda al director de proyectos a ejercer una mayor influencia y control sobre las transacciones facturables para ese período.

Para restablecer el estado de no exceder, seleccione uno o más datos reales de la vista **Backlog de facturación de tiempo y material** o **Reales** y luego seleccione **Restablecer estado de no exceder**.

El estado de no exceder se restablece a **no evaluado** en todos los datos reales seleccionados relevantes. Los datos reales que tienen su estado de no exceder restablecido son los datos reales de ventas no facturados que aún no se han facturado, no están en un borrador de factura y están marcados como cargables. Cualquier otro valor real seleccionado se ignora.

## <a name="reevaluate-not-to-exceed-status"></a>Volver a evaluar el estado de no exceder

Puede realizar una reevaluación masiva del estado de no exceder. La reevaluación del estado de no exceder es útil cuando:

  - Hubo una renegociación de los límites de no exceder con el cliente y será necesario reevaluar los datos reales.
  - El gerente de proyecto desea ajustar la facturación de la acumulación de ventas no facturadas priorizando un cuerpo de trabajo sobre otro.

Para reevaluar el estado de no exceder, seleccione uno o más datos reales de la vista **Backlog de facturación de tiempo y material** o **Reales** y luego seleccione **Reevaluar estado de no exceder**.

Todos los datos reales seleccionados relevantes con un límite que no debe excederse se evaluarán contra la configuración del límite que no debe exceder. Los datos reales que son relevantes para la reevaluación del estado de no exceder son los datos reales de ventas no facturados que aún no se han facturado, no están en un borrador de factura y están marcados como cargables. Cualquier otro valor real seleccionado seleccionado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
