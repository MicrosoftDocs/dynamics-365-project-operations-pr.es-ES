---
title: Cancelar la aprobación de entradas aprobadas anteriormente
description: Este tema explica cómo un director de proyecto puede cancelar la aprobación de entradas de tiempo, gastos o uso de material previamente aprobadas.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584801"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Cancelar la aprobación de entradas aprobadas anteriormente

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Un director de proyecto o aprobador que haya aprobado previamente entradas de tiempo, gastos o uso de material, puede cancelar la aprobación de esas entradas. 

Siga estos pasos para cancelar la aprobación de una entrada de tiempo, gastos o uso de materiales aprobada anteriormente.

1. Vaya a **Proyectos** \> **Mi trabajo** \> **Aprobaciones**.
2. La lista **Aprobaciones** muestra todas las entradas de tiempo que están esperando aprobación. Cambie la vista a **Mis aprobaciones anteriores**.
3. Seleccione las aprobaciones de tiempo, gasto o materiales a cancelar. A continuación, en el Panel de acciones, seleccione **Cancelar aprobación**.
4. En el cuadro de mensaje de confirmación que aparece, seleccione **ACEPTAR** para confirmar la operación.

> [!IMPORTANT]
> No puede cancelar la aprobación de una entrada de tiempo, gasto y uso de material previamente aprobada que ya se ha facturado al cliente. Si lo intenta, recibirá un mensaje que indica que la aprobación no se puede cancelar porque ya se facturó. En este caso, puede cancelar la aprobación solo si se utiliza una factura correctiva para emitir un crédito completo o un reembolso al cliente en la factura original.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impacto de cancelar la aprobación de entradas aprobadas anteriormente

Cuando se cancela una aprobación, hay un impacto tanto operativo como financiero.

### <a name="operational-impact"></a>Impacto operativo

Si se cancela la aprobación de una entrada, el registro de aprobación se marca como **Enviado**. El estado de la entrada se cambia a **Enviado**. En esta etapa, un miembro del equipo del proyecto puede recuperar la entrada sin enviar una solicitud de recuperación.

El aprobador puede cambiar los valores de **Cantidad facturable** y **Tipo de facturación** y luego aprobar de nuevo la entrada.

### <a name="financial-impact"></a>Impacto financiero

Si se cancela la aprobación de una entrada, los datos reales correspondientes de costes y ventas se actualizan de la siguiente manera:

- El campo **Estado del ajuste** se actualiza a **Ajustado**.
- El campo **Estado de facturación** se actualiza a **Cancelado**.

A continuación, se crean movimientos de retrocesión en la tabla Datos reales. Para crear entradas de retrocesión, el sistema copia los valores de campo desde los datos reales originales. Los únicos valores que no se copian son los valores de cantidad. En su lugar, estos valores se revierten. A continuación, se crean datos reales revertidos para los datos reales **Coste** y **Ventas sin facturar**. El campo **Estado del ajuste** en los datos reales invertidos se establece en **No ajustable**, y el campo **Estado de facturación** se establece en **Cancelado**. Debido a estos cambios, el gasto registrado y la acumulación de ingresos en el proyecto ya no representarán los importes que representan esos datos reales.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
