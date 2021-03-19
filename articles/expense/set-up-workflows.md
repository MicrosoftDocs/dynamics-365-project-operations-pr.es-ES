---
title: Configurar flujos de trabajo para la administración de gastos
description: Puede configurar un proceso de flujo de trabajo que se utiliza para revisar y aprobar documentos de viaje y gastos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276054"
---
# <a name="set-up-workflows-for-expense-management"></a>Configurar flujos de trabajo para la administración de gastos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede configurar un proceso de flujo de trabajo para revisar y aprobar documentos de viaje y gastos. Puede definir flujos de trabajo para informes de gastos, solicitudes de viaje y solicitudes de anticipos.

Un flujo de trabajo representa un proceso de negocio y define cómo fluye un documento a través del sistema. El flujo de trabajo también indica quién debe completar una tarea o aprobar un documento. El uso del sistema de flujo de trabajo en su organización tiene varios beneficios:

- **Procesos coherentes**: Puede definir el proceso de aprobación para documentos específicos, como solicitudes de compra e informes de gastos. El uso del sistema de flujo de trabajo contribuye a garantizar que los documentos se procesan y aprueban de forma coherente y eficaz.
- **Visibilidad de los procesos**: puede realizar un seguimiento del estado, el historial y las métricas de rendimiento de una instancia de flujo de trabajo específica. Esto ayuda a determinar si se deben realizar cambios en el flujo de trabajo para mejorar su eficacia.
- **Lista de trabajo centralizada**: los usuarios pueden consultar una lista de trabajo centralizada para ver las tareas y las aprobaciones de flujo de trabajo que se les han asignado. 

## <a name="workflow-types"></a>Tipos de flujo de trabajo

En la siguiente tabla se muestran los tipos de flujos de trabajo que puede crear en **Administración de gastos**.


|              <strong>Tipo</strong>              |                   <strong>Utilice este tipo para</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Aprobación automática de informes de gastos</strong> |            Cree flujos de trabajo de aprobación para informes de gastos.             |
|  <strong>Registro automático de informes de gastos</strong>   |        Cree flujos de trabajo de registro automático para informes de gastos.        |
|       <strong>Elemento de línea de gastos</strong>        |     Cree flujos de trabajo de aprobación para elementos de línea en informes de gastos.      |
| <strong>Registro automático de elemento de línea de gastos</strong> | Cree flujos de trabajo de registro automático para elementos de línea en informes de gastos. |
|       <strong>Solicitud de viaje</strong>       |          Cree flujos de trabajo de aprobación para solicitudes de viaje.           |
|      <strong>Solicitud de anticipo</strong>      |         Cree flujos de trabajo de aprobación para solicitudes de anticipo.          |
|        <strong>Devolución de impuestos de IVA</strong>        | Cree flujos de trabajo de aprobación para la devolución del impuesto sobre el valor añadido (IVA).  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]