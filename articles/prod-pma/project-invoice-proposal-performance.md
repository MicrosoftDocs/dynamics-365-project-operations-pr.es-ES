---
title: Rendimiento de propuesta de factura de proyecto
description: Este tema proporciona información sobre las mejoras de rendimiento de las propuestas de factura del proyecto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e707b0d9b379df59726271b5a0441ac04e269b9a
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683467"
---
# <a name="project-invoice-proposal-performance"></a>Rendimiento de propuesta de factura de proyecto

[!include [banner](../includes/banner.md)]

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
> El rendimiento de la propuesta de factura no se puede aplicar cuando las reglas de facturación están habilitadas.
> 
> Durante el proceso por lotes para crear propuestas de facturas, el número de subtareas dividirá las tareas en un número máximo en función del número de contratos con transacciones facturables, independientemente de lo que haya introducido. Por ejemplo, si introduce **3** para el número de subtareas para la creación de propuestas de factura en lote y solo hay dos contratos con transacciones facturables, solo se crean dos subtareas.
