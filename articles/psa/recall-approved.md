---
title: Recuperación de las entradas de tiempo o gastos aprobados
description: En este tema se proporciona información sobre cómo recuperar una transacción de tiempo o gasto aprobada previamente.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7bacd70881a6c463cc449a365173da5338a3d3fc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085195"
---
# <a name="recall-approved-time-or-expense-entries"></a>Recuperación de las entradas de tiempo o gastos aprobados

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un miembro del equipo del proyecto u otra persona que presente una entrada de tiempo o gasto puede recuperar esa entrada de tiempo o gasto después de que se haya aprobado. El proceso para recuperar una entrada de tiempo o gasto aprobado consta de dos pasos:

1. Un remitente solicita una recuperación.
2. Un aprobador aprueba la recuperación.

## <a name="request-a-recall"></a>Solicitud de una recuperación

Siga estos pasos para solicitar una recuperación de un tiempo aprobado o entrada de gastos.

1. Para entradas de tiempo, vaya a **Proyectos** \> **Mi trabajo** \> **Entrada de tiempo**.

    –o bien–

    Para entradas de gastos, vaya a **Proyectos** \> **Mi trabajo** \> **Gastos**.

2. Para entradas de tiempo, seleccione todas las entradas de tiempo para una combinación específica de un proyecto y una tarea. Alternativamente, en la cuadrícula, seleccione las celdas individuales por tiempo en una fecha específica para un proyecto específico.

    –o bien–

    Para las entradas de gastos, seleccione la fila para la entrada de gastos que recuperar.

3. Seleccione **Recuperar**. Aparece un cuadro de diálogo de confirmación. Si las entradas de tiempo y gastos seleccionadas ya están aprobadas, se le solicitará que introduzca un motivo para la recuperación.
4. Escriba un motivo para la recuperación y, a continuación, seleccione **Aceptar** para confirmar la operación. El sistema envía a la persona que aprobó las entradas una solicitud para aprobar la recuperación.

> [!NOTE]
> Aunque las entradas de tiempo y gastos aprobadas se pueden recuperar, si ya se ha facturado al cliente un tiempo o gasto aprobado, no se puede crear una solicitud de recuperación. Los usuarios que intenten crear una solicitud de recuperación recibirán un mensaje que indicará que el tiempo o el gasto no se pueden recuperar porque ya se han facturado.

## <a name="approve-or-reject-a-recall-request"></a>Aprobación o rechazo de una solicitud de recuperación

Siga estos pasos para aprobar o rechazar una solicitud de recuperación.

1. Vaya a **Proyectos** \> **Mi trabajo** \> **Aprobaciones**.
2. En la página de lista **Aprobaciones** , cambie la vista a **Solicitudes de recuperación pendientes de aprobación**. Se mostrará una lista de solicitudes de recuperación enviadas.
3. Seleccione una o más entradas y, a continuación, seleccione **Aprobar** o **Rechazar**.
4. Si seleccionó **Aprobar** , recibirá un mensaje de advertencia en el que se explicará el impacto de la aprobación. Seleccione **Aceptar** para confirmar la operación. Se aprobará la solicitud de recuperación.

    –o bien–

    Si seleccionó **Rechazar** , se rechazará la solicitud de recuperación.

> [!NOTE]
> Como cuando se solicita una recuperación, cuando se aprueba una recuperación, el sistema verifica cualquier actividad de facturación en las entradas de tiempo o gastos. Si ya se ha facturado una entrada, o si está en un borrador de factura, el aprobador recibirá un mensaje de error que indicará que no se puede aprobar la recuperación del tiempo o el gasto, porque ya se ha facturado.

## <a name="impact-of-a-recall-request"></a>Impacto de una solicitud de recuperación

Cuando se recupera una aprobación, hay un impacto tanto operativo como financiero.

### <a name="operational-impact"></a>Impacto operativo

Si se aprueba una solicitud de recuperación, el registro de aprobación se marca como **Rechazado**. El estado de la entrada se cambia a **Devuelto** o **Rechazado** según sea una entrada de tiempo o una entrada de gastos.

El miembro del equipo del proyecto puede ver entradas, editar y, a continuación, volver a enviar entradas o eliminar entradas por completo.

Si se rechaza una solicitud de recuperación, el estado de la entrada permanece **Aprobado** y el miembro del equipo del proyecto o el aprobador del proyecto no pueden editar la entrada.

### <a name="financial-impact"></a>Impacto financiero

Si se aprueba una solicitud de recuperación, los datos reales correspondientes de costes y ventas se actualizan de la siguiente manera:

- El campo **Estado del ajuste** se actualiza a **Ajustado**.
- El campo **Estado de facturación** se actualiza a **Cancelado**.

A continuación, se crean movimientos de retrocesión en la tabla Datos reales. Para crear entradas de retrocesión, el sistema copia los valores de campo desde los datos reales originales. Los únicos valores que no se copian son los valores de cantidad. En su lugar, estos valores se revierten. A continuación, se crean datos reales revertidos para los datos reales **Coste** y **Ventas sin facturar**. El campo **Estado del ajuste** en los datos reales invertidos se establece en **No ajustable** , y el campo **Estado de facturación** se establece en **Cancelado**. Debido a estos cambios, el gasto registrado y la acumulación de ingresos en el proyecto ya no representarán los importes que representan esos datos reales.

Si se rechaza una solicitud de recuperación, no habrá impacto financiero en el proyecto.

## <a name="changes-to-time-entry-records"></a>Cambios en los registros de entrada de tiempo

La siguiente ilustración muestra los cambios que se producen para las entradas de tiempo aprobadas cuando se recuperan.

![Transiciones de estado de entrada de tiempo](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Cambios en los registros de entrada de gastos

La siguiente ilustración muestra los cambios que se producen para las entradas de gastos aprobadas cuando se recuperan.

![Transiciones de estado de entrada de gastos](media/ExpenseEntryStateTransitions.png)
