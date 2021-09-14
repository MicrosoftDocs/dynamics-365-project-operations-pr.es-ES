---
title: 'Novedades de agosto de 2021: implementación simplificada de Project Operations'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de agosto de 2021 de la implementación simplificada de Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323527"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Novedades de agosto de 2021: implementación simplificada de Project Operations

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

  - Project Operations en el entorno de Dataverse versión 4.13.0.152

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- **Conjuntos de aprobación**: los conjuntos de aprobación agrupan las solicitudes de aprobación de uso de materiales, gastos o tiempo en subconjuntos más pequeños de operaciones. Esta agrupación permite que las aprobaciones se procesen en un orden específico por proyecto y permite reintentar y secuenciar. La agrupación de las solicitudes de aprobación mejora la confiabilidad y la trazabilidad del proceso de aprobación para grandes volúmenes de aprobaciones. Para obtener más información, consulte [Conjuntos de aprobaciones](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2295625 | El nombre del hito se debe copiar de la programación de la factura al detalle de la línea de la factura. |
| Facturación y precios | 2316323 | El descuento no debe ser editable en una factura proforma en Project Operations para escenarios basados en recursos. |
| Administración de oportunidades | 2338619 | Las reglas comerciales de **Oportunidad** y **Oferta** deben invocarse solo en las páginas. |
| Administración de recursos | 2316523 | El uso de **Enviar petición** desde un requisito de recursos que tiene un rol adjunto no debería mostrar un error. |
| Administración de recursos | 2326885 | La creación de un requisito de recursos a través de un proyecto no debería mostrar un error. |
| Tiempo y gastos | 2335584 | Flujos de tareas en desuso en la entrada de tiempo. |
| Tiempo y gastos | 2336884 | El botón de entrada de tiempo **Copiar semana** debe funcionar para algo más que solo el usuario actual. |
