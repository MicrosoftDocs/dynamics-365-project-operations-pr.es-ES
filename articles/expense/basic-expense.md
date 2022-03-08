---
title: Entrada de gastos (simplificados)
description: Este tema proporciona información sobre cómo trabajar con la entrada de gastos en una implementación simplificada.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 48bf86a5cee475708f93462dc154e21b36240023f0a94cf31c49e9a096951736
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007842"
---
# <a name="expense-entry-lite"></a>Entrada de gastos (simplificados)

_**Se aplica a:** Implementación simplificada: del acuerdo a la facturación proforma_

La gestión de gastos básica o simplificada es la capacidad de registrar gastos simples. Puede registrar los gastos de un proyecto y luego el aprobador del proyecto los revisará y aprobará.

Para obtener más información acerca de las capacidades de gastos en Dynamics 365 Project Operations, consulte [Información general de gastos](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Capturar un gasto básico

Puede capturar sus gastos para enviarlos al aprobador.

1. Vaya a **Gastos** y seleccione **Nuevo**.
2. En la página **Nuevo gasto**, especifique la información de gasto requerida y, a continuación, seleccione **Guardar**.

## <a name="submit-a-basic-expense"></a>Enviar un gasto básico

Una vez que haya terminado de capturar todos sus gastos y esté listo para que se aprueben, debe enviarlos.

1. Vaya a **Gastos** y seleccione un gasto. O bien, seleccione todos los gastos usando la casilla del encabezado.
2. Seleccione **Enviar**. El sistema procesa las entradas seleccionadas y luego crea solicitudes de aprobación de gastos.

## <a name="add-an-attachment"></a>Agregar datos adjuntos

Es posible que deba proporcionar al aprobador documentación adicional acerca de su gasto. Puede adjuntar un recibo en la escala de tiempo de la entrada de gasto. Seleccione **Editar** y en la sección **Escala de tiempo**, y luego seleccione el icono del clip de papel para adjuntar el recibo.

## <a name="recall-a-basic-expense"></a>Recuperar un gasto básico

Cuando envía un gasto por error, puede recuperarlo. El tiempo necesario para recuperar una entrada de gasto depende de la fase de aprobación en que se encuentre.  Si el aprobador todavía no ha aprobado la entrada, la recuperación puede ser inmediata. Sin embargo, si ya se ha aprobado la entrada, hay que pedir al aprobador que apruebe la recuperación y revierta las transacciones.

1. Vaya a **Gastos** y, en la lista de gastos, seleccione el gasto que quiera recuperar.
2. Seleccione **Recuperar**. Si todavía no se ha aprobado la entrada de gasto, el sistema la recuperará de inmediato. Si, por el contrario, la entrada de gasto ya se ha aprobado, se crea una solicitud de recuperación para notificar al aprobador que usted quiere revertir el gasto. El aprobador luego confirmará que se puede realizar la reversión y se devolverá la entrada.

## <a name="delete-a-basic-expense"></a>Eliminar un gasto básico

Los gastos que aún no se han enviado se pueden eliminar. Para eliminar un gasto que ya se ha enviado, primero debe recuperarlo.

## <a name="see-also"></a>Consultar también

- [Información general de aprobaciones](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]