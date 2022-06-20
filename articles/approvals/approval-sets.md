---
title: Conjuntos de aprobaciones
description: Este artículo explica cómo trabajar con conjuntos de aprobación, solicitudes y los subconjuntos de esas operaciones.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918103"
---
# <a name="approval-sets"></a>Conjuntos de aprobaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Aprobación agrupa las solicitudes de aprobación de grupo en subconjuntos más pequeños de operaciones. Esta agrupación permite que las aprobaciones se procesen por proyecto, en un orden específico y permite reintentar y secuenciar. La agrupación de las solicitudes de aprobación mejora la confiabilidad y la trazabilidad del proceso de aprobación para grandes volúmenes de aprobaciones.

Los conjuntos de aprobaciones indican el estado general de procesamiento de sus registros relacionados. Cuando se procesa un registro de aprobación utilizando un conjunto de aprobación, el registro se mueve de **Enviado** a **Aprobado** y ya no está vinculado al conjunto de aprobación. Si un registro falla cuando se envía para su aprobación, el registro permanece en un estado de **Enviado** y el conjunto de aprobación se marca como fallido. El conjunto de aprobación registra el mensaje de error del error.

## <a name="processing-approvals-and-approval-sets"></a>Procesamiento de aprobaciones y conjuntos de aprobaciones
Las aprobaciones que están en cola para su procesamiento se pueen ver en la vista **Aprobaciones de procesamiento**. El sistema procesa todas las entradas varias veces de forma asincrónica, incluido el reintento de una aprobación si los intentos anteriores fallaron.

El campo **Duración del conjunto de aprobaciones** registra el número de intentos que quedan para procesar el conjunto antes de que se marque como fallido.

Los conjuntos de aprobación se procesan a través de la activación periódica basada en un **Flujo de nube** llamado **Project Service: programar conjuntos de aprobación de proyectos de forma recurrente**. Esto se encuentra en la **Solución** llamada **Project Operations**. 

Asegúrese de que el flujo esté activado completando los siguientes pasos.

1. Como administrador, inicie sesión en [flow.microsoft.com](https://powerautomate.microsoft.com).
2. En la esquina superior derecha, cambia al entorno que use para Dynamics 365 Project Operations.
3. Seleccione **Soluciones** para enumerar las soluciones instaladas en el entorno.
4. En la lista de soluciones, seleccione **Project Operations**.
5. Cambie el filtro de **Todos** a **Flujos de nube**.
6. Verifique que el flujo **Project Service: programación recurrente de conjuntos de aprobación de proyectos** esté establecido en **Activado**. Si no es así, seleccione el flujo y luego seleccione **Activar**.
7. Verifique que el procesamiento ocurra cada cinco minutos revisando la lista **Trabajos del sistema** del área **Ajustes** del entorno de área dentro de Project Operations Dataverse.

## <a name="failed-approvals-and-approval-sets"></a>Aprobaciones y conjuntos de aprobaciones fallidos
La vista **Aprobaciones fallidas** enumera todas las aprobaciones que requieren la intervención del usuario. Abra los registros del conjunto de aprobaciones asociado para identificar la causa del error.
Seleccionando **Reintentar** se suma al recuento de duración del conjunto de aprobaciones, se mueve el conjunto de aprobaciones de nuevo a un estado de **Procesando** y se intentan procesar los registros restantes.

## <a name="configure-approval-sets"></a>Configurar conjuntos de aprobaciones

### <a name="enable-the-approval-sets-feature"></a>Habilitar la característica de conjuntos de aprobaciones
Antes de habilitar la característica de conjuntos de aprobaciones, verifique que no se estén procesando aprobaciones actualmente.

- Vaya a la página **Parámetros del proyecto** y seleccione **Control de características** > **Habilitar aprobaciones modernas**.

### <a name="turn-off-the-approval-sets-feature"></a>Deshabilitar la característica de conjuntos de aprobaciones
Antes de deshabilitar la característica de conjuntos de aprobaciones, verifique que no se estén procesando aprobaciones actualmente.

- Vaya a la página **Parámetros del proyecto** y seleccione **Control de características** > **Deshabilitar aprobaciones modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurar el umbral asincrónico 
Cuando se crean conjuntos de aprobaciones, el procesamiento pasa a un segundo plano cuando el número seleccionado de registros para aprobación excede el umbral indicado. Utilice el campo **Umbral asincrónico** para configurar cuándo el proceso de aprobación debe ejecutarse de forma sincrónica o asincrónica. Seleccione uno de los siguientes valores:

  - Cero: todas las solicitudes deben procesarse de forma asincrónica. 
  - Números mayores que cero: las aprobaciones se procesan de forma asincrónica solo cuando el número de aprobaciones enviadas supera este valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
