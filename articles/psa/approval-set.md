---
title: Conjuntos de aprobaciones
description: Este tema proporciona información sobre el conjunto de aprobación, las solicitudes y los subconjuntos de esas operaciones.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116892"
---
# <a name="approval-sets"></a><span data-ttu-id="8335e-103">Conjuntos de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="8335e-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8335e-104">Aprobación agrupa las solicitudes de aprobación de grupo en subconjuntos más pequeños de operaciones.</span><span class="sxs-lookup"><span data-stu-id="8335e-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="8335e-105">Esta agrupación permite que las aprobaciones se procesen en orden por proyecto y permite reintentos y secuencias.</span><span class="sxs-lookup"><span data-stu-id="8335e-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="8335e-106">La agrupación mejora la confiabilidad y la trazabilidad del proceso de aprobación para grandes volúmenes de aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="8335e-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="8335e-107">Los conjuntos de aprobaciones indican el estado general de procesamiento de sus registros relacionados.</span><span class="sxs-lookup"><span data-stu-id="8335e-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="8335e-108">Cuando se procesa un registro de aprobación utilizando un conjunto de aprobación, el registro se mueve de **Enviado** a **Aprobado** y está desvinculado del conjunto de aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="8335e-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="8335e-109">Si un registro falla cuando se envía para su aprobación, el registro permanece en un estado de **Enviado** y el conjunto de aprobación se marca como fallido.</span><span class="sxs-lookup"><span data-stu-id="8335e-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="8335e-110">El conjunto de aprobación registra el mensaje de error del error.</span><span class="sxs-lookup"><span data-stu-id="8335e-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="8335e-111">Procesamiento de aprobaciones y conjuntos de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="8335e-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="8335e-112">Las aprobaciones que están en cola para su procesamiento se pueen ver en la vista **Aprobaciones de procesamiento**.</span><span class="sxs-lookup"><span data-stu-id="8335e-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="8335e-113">El sistema intenta procesar todas las entradas varias veces de forma asincrónica, incluido el reintento de una aprobación si los intentos anteriores fallaron.</span><span class="sxs-lookup"><span data-stu-id="8335e-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="8335e-114">El campo **Duración del conjunto de aprobaciones** registra el número de intentos que quedan para procesar el conjunto antes de que se marque como fallido.</span><span class="sxs-lookup"><span data-stu-id="8335e-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="8335e-115">Aprobaciones y conjuntos de aprobaciones fallidos</span><span class="sxs-lookup"><span data-stu-id="8335e-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="8335e-116">La vista **Aprobaciones fallidas** enumera todas las aprobaciones que requieren la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="8335e-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="8335e-117">Abra los registros del conjunto de aprobaciones asociado para identificar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="8335e-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="8335e-118">Seleccionando **Reintentar** se suma al recuento de duración del conjunto de aprobaciones, se mueve el conjunto de aprobaciones de nuevo a un estado de **Procesando** y se intentan procesar los registros restantes.</span><span class="sxs-lookup"><span data-stu-id="8335e-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="8335e-119">Configurar conjuntos de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="8335e-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="8335e-120">Habilitar la característica de conjuntos de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="8335e-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="8335e-121">Antes de habilitar la característica de conjuntos de aprobaciones, verifique que no se estén procesando aprobaciones actualmente.</span><span class="sxs-lookup"><span data-stu-id="8335e-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="8335e-122">Vaya a la página **Parámetros del proyecto** y seleccione **Control de características** > **Habilitar aprobaciones modernas**.</span><span class="sxs-lookup"><span data-stu-id="8335e-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="8335e-123">Deshabilitar la característica de conjuntos de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="8335e-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="8335e-124">Antes de deshabilitar la característica de conjuntos de aprobaciones, verifique que no se estén procesando aprobaciones actualmente.</span><span class="sxs-lookup"><span data-stu-id="8335e-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="8335e-125">Vaya a la página **Parámetros del proyecto** y seleccione **Control de características** > **Deshabilitar aprobaciones modernas**.</span><span class="sxs-lookup"><span data-stu-id="8335e-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="8335e-126">Configurar el umbral asincrónico</span><span class="sxs-lookup"><span data-stu-id="8335e-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="8335e-127">Cuando se crean conjuntos de aprobaciones, el procesamiento pasa a un segundo plano cuando el número seleccionado de registros para aprobación excede el umbral indicado.</span><span class="sxs-lookup"><span data-stu-id="8335e-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="8335e-128">Utilice el campo **Umbral asincrónico** para configurar cuándo el proceso de aprobación debe ejecutarse de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8335e-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="8335e-129">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="8335e-129">Valid values are:</span></span>

  - <span data-ttu-id="8335e-130">Cero: todas las solicitudes deben procesarse de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8335e-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="8335e-131">Números mayores que cero: las aprobaciones se procesan de forma asincrónica solo cuando el número de aprobaciones enviadas supera este valor.</span><span class="sxs-lookup"><span data-stu-id="8335e-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
