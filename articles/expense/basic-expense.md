---
title: Entrada de gastos (simplificados)
description: En este artículo se proporciona información sobre cómo trabajar con entradas de gastos en una implementación Lite.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b69cc4ec0a4b51cd1d27f8b8a4a94248ae884797
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917965"
---
# <a name="expense-entry-lite"></a>Entrada de gastos (simplificados)

_**Se aplica a:** Implementación simplificada: del acuerdo a la facturación proforma_

La gestión de gastos básica o simplificada es la capacidad de registrar gastos simples. Puede registrar gastos contra un proyecto y luego el aprobador del proyecto los revisará y aprobará.

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