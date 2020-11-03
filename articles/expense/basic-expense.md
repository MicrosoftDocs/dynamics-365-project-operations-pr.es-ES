---
title: Entrada de gastos (simplificados)
description: Este tema proporciona información sobre cómo trabajar con la entrada de gastos en una implementación simplificada.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085032"
---
# <a name="expense-entry-lite"></a>Entrada de gastos (simplificados)

_**Se aplica a:** Implementación simplificada: del acuerdo a la facturación proforma_

La gestión de gastos básica o simplificada es la capacidad de registrar gastos simples. Puede registrar gastos contra un proyecto y luego el aprobador del proyecto los revisará y aprobará.

Para obtener más información sobre las capacidades de gastos en Dynamics 365 Project Operations, consulte [Resumen de gastos](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Capturar un gasto básico

Puede capturar sus gastos para enviarlos al aprobador.

1. Vaya a **Gastos** y seleccione **Nuevo**.
2. En la página **Nuevo gasto** , especifique la información de gasto requerida y, a continuación, seleccione **Guardar**.

## <a name="submit-a-basic-expense"></a>Enviar un gasto básico

Una vez que haya terminado de capturar todos sus gastos y esté listo para que se aprueben, debe enviarlos.

1. Vaya a **Gastos** y seleccione un gasto. O bien, seleccione todos los gastos usando la casilla de verificación del encabezado.
2. Seleccione **Enviar**. El sistema procesa las entradas seleccionadas y luego crea solicitudes de aprobación de gastos.

## <a name="recall-a-basic-expense"></a>Recuperar un gasto básico

Cuando envía un gasto por error, puede recuperarlo. El tiempo necesario para recuperar una entrada de gastos depende de su etapa de aprobación.  Si el aprobador aún no ha aprobado la entrada, la recuperación puede ocurrir de inmediato. Sin embargo, si la entrada ya se ha aprobado, se le pide al aprobador que apruebe la recuperación y revierta las transacciones.

1. Vaya a **Gastos** y luego, en la lista de gastos, seleccione el gasto que desea recuperar.
2. Seleccione **Recuperar**. Si la entrada de gastos aún no se ha aprobado, el sistema la recupera inmediatamente. Si la entrada de gastos ya se aprobó, se crea una solicitud de recuperación para notificar al aprobador que desea revertir el gasto. El aprobador luego confirmará que se puede realizar la reversión y se devolverá la entrada.

## <a name="delete-a-basic-expense"></a>Eliminar un gasto básico

Los gastos que aún no se han enviado se pueden eliminar. Para eliminar un gasto que ya se ha enviado, primero debe recuperarlo.

## <a name="see-also"></a>Consultar también

- [Información general de aprobaciones](../approvals/approvals-overview.md)
