---
title: Conjuntos de aprobaciones en Project Service Automation
description: Este tema proporciona información sobre el conjunto de aprobación, las solicitudes y los subconjuntos de esas operaciones.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0783441d3bf7ed80192a3890a2e297fea05fe425
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583375"
---
# <a name="approval-sets-in-project-service-automation"></a>Conjuntos de aprobaciones en Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aprobación agrupa las solicitudes de aprobación de grupo en subconjuntos más pequeños de operaciones. Esta agrupación permite que las aprobaciones se procesen en orden por proyecto y permite reintentos y secuencias. La agrupación mejora la confiabilidad y la trazabilidad del proceso de aprobación para grandes volúmenes de aprobaciones.

Los conjuntos de aprobaciones indican el estado general de procesamiento de sus registros relacionados. Cuando se procesa un registro de aprobación utilizando un conjunto de aprobación, el registro se mueve de **Enviado** a **Aprobado** y está desvinculado del conjunto de aprobaciones. Si un registro falla cuando se envía para su aprobación, el registro permanece en un estado de **Enviado** y el conjunto de aprobación se marca como fallido. El conjunto de aprobación registra el mensaje de error del error.

## <a name="processing-approvals-and-approval-sets"></a>Procesamiento de aprobaciones y conjuntos de aprobaciones
Las aprobaciones que están en cola para su procesamiento se pueen ver en la vista **Aprobaciones de procesamiento**. El sistema intenta procesar todas las entradas varias veces de forma asincrónica, incluido el reintento de una aprobación si los intentos anteriores fallaron.

El campo **Duración del conjunto de aprobaciones** registra el número de intentos que quedan para procesar el conjunto antes de que se marque como fallido.

## <a name="failed-approvals-and-approval-sets"></a>Aprobaciones y conjuntos de aprobaciones fallidos
La vista **Aprobaciones fallidas** enumera todas las aprobaciones que requieren la intervención del usuario. Abra los registros del conjunto de aprobaciones asociado para identificar la causa del error.
Seleccionando **Reintentar** se suma al recuento de duración del conjunto de aprobaciones, se mueve el conjunto de aprobaciones de nuevo a un estado de **Procesando** y se intentan procesar los registros restantes.

## <a name="configure-approval-sets"></a>Configurar conjuntos de aprobaciones

###  <a name="enable-the-approval-sets-feature"></a>Habilitar la característica de conjuntos de aprobaciones
Antes de habilitar la característica de conjuntos de aprobaciones, verifique que no se estén procesando aprobaciones actualmente.

- Vaya a la página **Parámetros del proyecto** y seleccione **Control de características** > **Habilitar aprobaciones modernas**.

### <a name="turn-off-the-approval-sets-feature"></a>Deshabilitar la característica de conjuntos de aprobaciones
Antes de deshabilitar la característica de conjuntos de aprobaciones, verifique que no se estén procesando aprobaciones actualmente.

- Vaya a la página **Parámetros del proyecto** y seleccione **Control de características** > **Deshabilitar aprobaciones modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurar el umbral asincrónico 
Cuando se crean conjuntos de aprobaciones, el procesamiento pasa a un segundo plano cuando el número seleccionado de registros para aprobación excede el umbral indicado. Utilice el campo **Umbral asincrónico** para configurar cuándo el proceso de aprobación debe ejecutarse de forma sincrónica o asincrónica.
Los valores válidos son:

  - Cero: todas las solicitudes deben procesarse de forma asincrónica. 
  - Números mayores que cero: las aprobaciones se procesan de forma asincrónica solo cuando el número de aprobaciones enviadas supera este valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
