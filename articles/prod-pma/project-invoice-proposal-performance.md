---
title: Rendimiento de propuesta de factura de proyecto
description: Este tema proporciona información sobre las mejoras de rendimiento de las propuestas de factura del proyecto.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573580"
---
# <a name="project-invoice-proposal-performance"></a>Rendimiento de propuesta de factura de proyecto

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Cuando crea una nueva propuesta de factura, puede encontrar problemas de rendimiento a medida que aumenta el número de proyectos y subproyectos. Para mejorar el rendimiento, se encuentra disponible una característica que reduce el tiempo necesario para crear una nueva propuesta de factura para las transacciones de proyecto registradas.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Habilitar la mejora del rendimiento de propuesta de factura de proyecto
Para habilitar la característica de mejora del rendimiento de la propuesta de factura del proyecto, complete los siguientes pasos.

1.  Vaya a **Administración de características** > **Todas**. En la lista de características, ubique la **Mejora del rendimiento de la propuesta de factura del proyecto**.
2.  Seleccione **Habilitar ahora**.
3.  Actualice su navegador y luego cree una nueva propuesta de factura.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Deshabilitar la mejora del rendimiento de propuesta de factura de proyecto
Complete los siguientes pasos para deshabilitar la característica de mejora del rendimiento de la propuesta de factura del proyecto.

1.  Vaya a **Administración de características** > **Todas**. En la lista de características, ubique la **Mejora del rendimiento de la propuesta de factura del proyecto**.
2.  Seleccione **Deshabilitar**.
3.  Actualice el explorador.

> [!NOTE]
> El rendimiento de la propuesta de factura no se puede aplicar cuando las reglas de facturación están habilitadas o los procesos por lotes se están ejecutando.
