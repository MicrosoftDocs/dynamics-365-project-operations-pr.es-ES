---
title: Cancelar entradas de gastos y tiempo aprobadas anteriormente
description: En este artículo se proporciona información sobre cómo cancelar una transacción de gastos y tiempo de proyecto aprobada.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 840f163ee9bf1fc98f140efdcc0d37a5424ddb8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933329"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Cancelar entradas de gastos o tiempo aprobadas anteriormente

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En la versión más reciente de Dynamics 365 Project Service Automation, los aprobadores pueden cancelar las entradas de gasto o tiempo que aprobaron anteriormente.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Cancelar una entrada de gastos o tiempo aprobada anteriormente

Siga estos pasos para cancelar una entrada de gastos o tiempo aprobada anteriormente.

1. Vaya a **Proyectos** \> **Mi trabajo** \> **Aprobaciones**.
2. En la página de lista **Aprobaciones**, cambie la vista a **Mis aprobaciones anteriores**. Se mostrará una lista de las entradas de gastos y tiempo aprobadas anteriormente.
3. Seleccione una o varias entradas y después seleccione **Cancelar aprobación**. Recibirá un mensaje de advertencia.
4. Seleccione **Aceptar** para cancelar la aprobación.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Comprender el impacto de cancelar una aprobación de una entrada de gastos o tiempo

Cuando se cancela una aprobación, hay un impacto tanto operativo como financiero.

### <a name="operational-impact"></a>Impacto operativo

En lo que respecta a las operaciones, cuando se cancela una aprobación, el estado del registro se restablece a **Borrador** y la aprobación deja de aparecer en la vista **Mis aprobaciones anteriores**. En su lugar, la aprobación cancelada aparece en la vista **Entradas de horas para aprobación** o la vista **Entradas de gastos para aprobación**, dependiendo de si se trataba de una entrada de tiempo o de gastos. Además, el estado de la entrada de gastos o de tiempo relacionado se cambia a **Enviado** para que la entrada relacionada sea homogénea con las aprobaciones que tienen un estado de **Borrador**.

Como aprobador, podrá editar algunos de los campos de las aprobaciones que tengan el estado de **Borrador**. Entre estos campos se incluyen los campos **Tipo de facturación** y **Horas facturables para entradas de tiempo**. Tras realizar los cambios, podrá volver a aprobar el registro. De manera alternativa, puede rechazar la entrada. Si rechaza la aprobación de una entrada de tiempo, el estado de la entrada cambiará a **Devuelto**. Si rechaza la aprobación de una entrada de gastos, el estado cambiará a **Rechazado**. Funcionalmente, tanto las entradas devueltas como las rechazadas se comportan igual que una entrada con el estado de **Borrador**. Un miembro del equipo del proyecto puede realizar cualquier cambio necesario en la entrada y después volver a enviarla para su aprobación, o bien puede eliminar la entrada por completo.

### <a name="financial-impact"></a>Impacto financiero

El proyecto también se ve afectado desde el punto de vista financiero cuando se cancela una aprobación. En primer lugar, los datos reales correspondientes de costes y ventas se actualizan de la siguiente manera:

- El estado de ajuste se establece en **Ajustado**.
- El estado de la facturación se establece en **Cancelado**.

A continuación, se crean movimientos de retrocesión en la tabla Datos reales. Para crear entradas de retrocesión, el sistema copia los valores de campo desde los datos reales originales. Los únicos valores que no se copian son los valores de cantidad. En su lugar, estos valores se revierten. A continuación, se crean datos reales revertidos para los datos reales **Coste** y **Ventas sin facturar**. El campo **Estado del ajuste** de los datos reales revertidos se establece en **No ajustable** y el estado de facturación se establece en **Cancelado**.

Tras realizar estos cambios, el importe que se registra como gasto en el proyecto y la acumulación de ingresos del proyecto dejarán de representar los importes que representan esos datos reales.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
