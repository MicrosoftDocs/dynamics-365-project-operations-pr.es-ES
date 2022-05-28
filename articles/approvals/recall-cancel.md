---
title: Recuperación de entradas aprobadas anteriormente
description: Este tema explica cómo un miembro del equipo del proyecto puede solicitar la recuperación de registros de tiempo, gastos y uso de materiales previamente enviados y aprobados, y cómo un gerente de proyecto puede aprobar o rechazar solicitudes de recuperación.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586595"
---
# <a name="recall-previously-approved-entries"></a>Recuperación de entradas aprobadas anteriormente

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Un miembro del equipo del proyecto que envía una entrada de tiempo, gasto o material puede recuperar esa entrada después de que se haya aprobado. El proceso de recuperación tiene dos pasos prncipales:

1. Un remitente solicita una recuperación.
2. Un aprobador aprueba la solicitud de recuperación.

## <a name="request-a-recall"></a>Solicitud de una recuperación

Siga estos pasos para solicitar una recuperación de una entrada de tiempo, gastos o material aprobada.

1. Siga uno de estos pasos, según el tipo de entrada que desee recuperar:

    - Para entradas de tiempo, vaya a **Proyectos** \> **Mi trabajo** \> **Entrada de tiempo** y seleccione todas las entradas de tiempo para una combinación específica de un proyecto y una tarea. Alternativamente, en la cuadrícula, seleccione las celdas individuales por tiempo en una fecha específica para un proyecto específico.
    - Para las entradas de gastos, vaya a **Proyectos** \> **Mi trabajo** \> **Gastos** y seleccione la fila para la entrada de gastos que recuperar.
    - Para las entradas de uso de materiales, vaya a **Proyectos** \> **Mi trabajo** \> **Registro de uso de materiales** y seleccione la fila para la entrada de uso de materiales que recuperar.

2. Seleccione **Recuperar**. Aparece un cuadro de diálogo de confirmación. Si las entradas de tiempo, gastos o uso de materiales seleccionadas ya están aprobadas, se le solicitará que introduzca un motivo para la recuperación.
3. Escriba un motivo para la recuperación y, a continuación, seleccione **Aceptar** para confirmar la operación. El sistema envía a la persona que aprobó las entradas una solicitud para aprobar la recuperación.

> [!IMPORTANT]
> No puede crear una solicitud de recuperación para una entrada de tiempo, gasto o uso de material previamente aprobada que ya se ha facturado al cliente. Si lo intenta, recibirá un mensaje que indicará que la entrada de tiempo, gasto o uso de material no se puede recuperar porque ya se han facturado. En este caso, puede solicitar una recuperación de la entrada solo si se utiliza una factura correctiva para emitir un crédito completo o un reembolso al cliente en la factura original.

## <a name="approve-or-reject-a-recall-request"></a>Aprobación o rechazo de una solicitud de recuperación

Siga estos pasos para aprobar o rechazar una solicitud de recuperación.

1. Vaya a **Proyectos** \> **Mi trabajo** \> **Aprobaciones**.
2. En la página de lista **Aprobaciones**, cambie la vista a **Solicitudes de recuperación pendientes de aprobación**. Se mostrará una lista de solicitudes de recuperación enviadas.
3. Seleccione una o más entradas y, a continuación, seleccione **Aprobar** o **Rechazar**.
4. Si seleccionó **Aprobar**, recibirá un mensaje de advertencia en el que se explicará el impacto de la aprobación. Seleccione **Aceptar** para confirmar la operación. Se aprobará la solicitud de recuperación.

    –o bien–

    Si seleccionó **Rechazar**, se rechazará la solicitud de recuperación.

> [!IMPORTANT]
> Cuando se solicita una recuperación, al igual que cuando se solicita, el sistema verifica cualquier actividad de facturación en las entradas de tiempo, gastos o uso de material. Si ya se ha facturado una entrada, o si está en un borrador de factura, el aprobador recibe un mensaje de error que indica que no se puede aprobar la recuperación del tiempo o el gasto, porque ya se ha facturado. En este caso, el aprobador puede aprobar la recuperación solo si se utiliza una factura correctiva para emitir un crédito completo o un reembolso al cliente en la factura original.

## <a name="impact-of-a-recall-request"></a>Impacto de una solicitud de recuperación

Cuando se recupera una aprobación, hay un impacto tanto operativo como financiero.

### <a name="operational-impact"></a>Impacto operativo

Si se aprueba una solicitud de recuperación, el registro de aprobación se marca como **Rechazado**. El estado de la entrada se cambia a **Devuelto** o **Rechazado** según sea una entrada de tiempo, gastos o uso de material.

El miembro del equipo del proyecto puede ver entradas, editarlas y, a continuación, volver a enviarlas, o eliminar entradas por completo.

Si se rechaza una solicitud de recuperación, el estado de la entrada permanece **Aprobado** y el miembro del equipo del proyecto o el aprobador del proyecto no pueden editar la entrada.

### <a name="financial-impact"></a>Impacto financiero

Si se aprueba una solicitud de recuperación, los datos reales correspondientes de costes y ventas se actualizan de la siguiente manera:

- El campo **Estado del ajuste** se actualiza a **Ajustado**.
- El campo **Estado de facturación** se actualiza a **Cancelado**.

A continuación, se crean movimientos de retrocesión en la tabla Datos reales. Para crear entradas de retrocesión, el sistema copia los valores de campo desde los datos reales originales. Los únicos valores que no se copian son los valores de cantidad. En su lugar, estos valores se revierten. A continuación, se crean datos reales revertidos para los datos reales **Coste** y **Ventas sin facturar**. El campo **Estado del ajuste** en los datos reales invertidos se establece en **No ajustable**, y el campo **Estado de facturación** se establece en **Cancelado**. Debido a estos cambios, el gasto registrado y la acumulación de ingresos en el proyecto ya no representarán los importes que representan esos datos reales.

Si se rechaza una solicitud de recuperación, no habrá impacto financiero en el proyecto.

## <a name="changes-to-time-entry-records"></a>Cambios en los registros de entrada de tiempo

La siguiente ilustración muestra los cambios que se producen para las entradas de tiempo aprobadas y los registros de aprobación correspondientes cuando se recuperan.

![Transiciones de estado de entrada de tiempo.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Cambios en los registros de entrada de gastos y uso de material

La siguiente ilustración muestra los cambios que se producen para las entradas de gastos y uso de material, y los registros de aprobación correspondientes cuando se recuperan.

![Transiciones de estado de entrada de gastos.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
