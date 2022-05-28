---
title: Novedades o cambios en la versión de actualización 42, V3, de Project Service Automation
description: Este tema enumera las características y correcciones que están disponibles en Microsoft Dynamics 365 Project Service Automation, versión de actualización 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589217"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novedades o cambios en la versión de actualización 42, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation, versión de actualización 42, V3. Esta versión tiene un número de compilación de V3.10.73.61 y generalmente está disponible a través de una actualización automática en abril de 2022.

## <a name="update-release-42"></a>Versión de actualización 42

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Tiempo y gasto**

- Cuando se rechaza una hoja de horas, el usuario que la rechazó se identifica incorrectamente como **Sistema**.
- Cuando se importan entradas de tiempo, falta el valor **Categoría de recursos**.
- Los aprobadores de proyectos pueden aprobar proyectos enviados cuando sus permisos no están configurados específicamente para **Puede aprobar**.

**Ventas**

- Cuando los valores reales se registran en tareas de nivel no raíz, los costos reales se agregan incorrectamente.
