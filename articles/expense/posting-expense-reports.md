---
title: Registrar informes de gastos
description: Este artículo explica cómo publicar informes de gastos.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524891"
---
# <a name="post-expense-reports"></a>Registrar informes de gastos

Una vez que se ha aprobado y transferido un informe de gastos al diario general, se puede registrar. Cuando publica un informe de gastos, se identifican los gastos que son idóneos para la recuperación del impuesto sobre el valor añadido (IVA). La tarea de verificar y recuperar los pagos del IVA se asigna al empleado que es responsable de verificar el informe de gastos.

Si los gastos de un informe de gastos se cargan a una empresa que no sea la empresa que emplea al empleado, debe verificar tanto la empresa a la que se le deben esos gastos como la empresa que los adeuda. Por ejemplo, el empleado que presentó un informe de gastos trabaja para la empresa DAT pero le cobró un gasto a la empresa DIR. En este caso, DAT es la empresa a la que se debe el gasto y DIR es la empresa que debe el gasto. Después de verificar estas líneas de diario, puede registrar las líneas de gastos en el libro mayor.

Para registrar un informe de gastos, en la página **Informes de gastos aprobados**, seleccione el informe de gastos y, a continuación, en el Panel de acciones, seleccione **Registrar**.

También puede registrar todos los informes de gastos de la lista al mismo tiempo. Seleccione todos los informes de gastos y luego seleccione **Registrar**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Habilite la capacidad de contabilizar el pasivo de gastos en la moneda del proveedor para la función de método de pago en efectivo

La característica **Capacidad para contabilizar el pasivo por gastos en la moneda del proveedor para el método de pago en efectivo** permite que los informes de gastos se registren en una moneda de proveedor para el método de pago en efectivo.

Actualmente, cuando envía gastos en efectivo, los informes de gastos se registran en la moneda contable. Debido a la conversión de montos entre la moneda de la transacción, la moneda de contabilidad y la moneda del proveedor, se paga un monto incorrecto a los proveedores si la fecha de transacción del gasto y la fecha de pago real tienen tipos de cambio diferentes.

Esta función garantizará que el saldo del proveedor se registre en la moneda del proveedor cuando se registre el informe de gastos.

1. Vaya a **Áreas de trabajo** \> **Administración de características**.
2. En la lista, busque y seleccione **Capacidad para contabilizar el pasivo por gastos en la moneda del proveedor para el método de pago en efectivo** y luego seleccione **Habilitar ahora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
