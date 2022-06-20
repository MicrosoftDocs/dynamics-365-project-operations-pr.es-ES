---
title: Novedades o cambios en la versión de actualización 42, V3, de Project Service Automation
description: Este artículo enumera las funciones y correcciones que están disponibles en la actualización de la versión 42, V3 de Microsoft Dynamics 365 Project Service Automation.
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912736"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novedades o cambios en la versión de actualización 42, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation Update Release 42, V3. Esta versión tiene un número de compilación de V3.10.73.61 y generalmente está disponible a través de una actualización automática en abril de 2022.

## <a name="update-release-42"></a>Versión de actualización 42

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Tiempo y gasto**

- Cuando se rechaza una hoja de horas, el usuario que la rechazó se identifica incorrectamente como **Sistema**.
- Cuando se importan entradas de tiempo, falta el valor **Categoría de recursos**.
- Los aprobadores de proyectos pueden aprobar proyectos enviados cuando sus permisos no están configurados específicamente para **Puede aprobar**.

**Ventas**

- Cuando los valores reales se registran en tareas de nivel no raíz, los costos reales se agregan incorrectamente.
