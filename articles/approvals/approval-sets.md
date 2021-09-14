---
title: Conjuntos de aprobaciones
description: Este tema explica cómo trabajar con conjuntos de aprobaciones, solicitudes y los subconjuntos de esas operaciones.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323257"
---
# <a name="approval-sets"></a>Conjuntos de aprobaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Aprobación agrupa las solicitudes de aprobación de grupo en subconjuntos más pequeños de operaciones. Esta agrupación permite que las aprobaciones se procesen por proyecto, en un orden específico y permite reintentar y secuenciar. La agrupación de las solicitudes de aprobación mejora la confiabilidad y la trazabilidad del proceso de aprobación para grandes volúmenes de aprobaciones.

Los conjuntos de aprobaciones indican el estado general de procesamiento de sus registros relacionados. Cuando se procesa un registro de aprobación utilizando un conjunto de aprobación, el registro se mueve de **Enviado** a **Aprobado** y ya no está vinculado al conjunto de aprobación. Si un registro falla cuando se envía para su aprobación, el registro permanece en un estado de **Enviado** y el conjunto de aprobación se marca como fallido. El conjunto de aprobación registra el mensaje de error del error.

## <a name="processing-approvals-and-approval-sets"></a>Procesamiento de aprobaciones y conjuntos de aprobaciones
Las aprobaciones que están en cola para su procesamiento se pueen ver en la vista **Aprobaciones de procesamiento**. El sistema procesa todas las entradas varias veces de forma asincrónica, incluido el reintento de una aprobación si los intentos anteriores fallaron.

El campo **Duración del conjunto de aprobaciones** registra el número de intentos que quedan para procesar el conjunto antes de que se marque como fallido.

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
