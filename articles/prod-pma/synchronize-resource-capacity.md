---
title: Sincronizar la capacidad de los recursos
description: Este tema proporciona información sobre cómo sincronizar la capacidad de un recurso entre calendarios y proyectos.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085126"
---
# <a name="synchronize-resource-capacity"></a>Sincronizar la capacidad de los recursos

[!include [banner](../includes/banner.md)]

Los procesos para la sincronización de recursos ayudan a garantizar que la información para el calendario y el calendario base se incorpore a la programación de recursos del proyecto. Si se cambia el calendario, los procesos realizan las actualizaciones necesarias en la programación de los recursos del proyecto. Los procesos también ayudan a mejorar el rendimiento, porque la información de recursos del calendario se sincroniza de antemano. Por lo tanto, las actualizaciones de la información de programación de recursos se producen más rápidamente. Le recomendamos que programe los procesos por lotes en lugar de uno a la vez. De lo contrario, existe el riesgo de que alguien olvide las fechas inclusivas cuando se sincronizó la información por última vez. Si no se utilizan fechas inclusivas, pueden producirse vacíos durante la sincronización de fechas.

![Sincronización de calendario](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizar acumulaciones de capacidad de los recursos

El proceso de sincronización está diseñado para sincronizar toda la información del calendario de recursos. Esta información incluye información del calendario base sobre cualquier cambio en la tabla de capacidad del calendario de recursos del proyecto. Si se agregan nuevos recursos al proyecto, la sincronización ayuda a garantizar que la información actualizada del calendario esté disponible. Esta sincronización se puede realizar en cualquier momento.

Se recomienda usar un lote. Las opciones están disponibles durante la sincronización de las reservas de capacidad.

1. Seleccione **Gestión de proyectos y contabilidad** &gt; **Periódico** &gt; **Sincronización de capacidad** &gt; **Sincronizar acumulaciones de capacidad de recursos**.
2. Configure las opciones en la tabla siguiente.

    | Opción      | Descripción |
    |-------------|-------------|
    | Código de período | Opcionalmente, seleccione el código de intervalo de fechas del Libro de contabilidad para establecer las fechas de inicio y finalización del proceso de sincronización para acumulaciones de capacidad de recursos. |
    | Fecha de inicio  | Especifique la fecha de inicio del proceso de sincronización para las acumulaciones de capacidad de recursos. |
    | Fecha de finalización    | Especifique la fecha de finalización para el proceso de sincronización para las acumulaciones de capacidad de recursos. |

[![Procreso de sincronización](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)