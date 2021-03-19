---
title: Novedades o cambios en la versión de actualización 29, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 29, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499692"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novedades o cambios en la versión de actualización 29, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 29. Esta versión tiene el número de compilación V3.10.45.98 y está disponible de forma generalizada mediante una actualización automática desde febrero de 2021.

## <a name="update-release-29"></a>Versión de actualización 29

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- Los usuarios no pueden ver las horas de trabajo registradas en días no laborables en la cuadrícula de entrada de tiempo.
- Las entradas de gastos aprobadas se pueden editar en la cuadrícula.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- Falta la lógica de validación para garantizar que las horas de esfuerzo de asignación de recursos no pueden ser negativas.
- La acción personalizada, **AssignResourcesForTask** actualiza todos los campos en lugar de solo los campos modificados.
- Al copiar un proyecto en un entorno con complementos o flujos de trabajo que están registrados en el evento **CreateProject**, el atributo **msdyn_bulkgenerationstatus** no se actualiza si el **CopyWBSToProject** falla.
- Cuando expande el calendario del proyecto, los días laborables no se ordenan en orden ascendente, lo que provoca que fallen algunas actualizaciones de tareas del proyecto.
- Cambiar el Gerente de Proyecto en un proyecto existente desencadena la lógica predeterminada de la unidad organizativa.

**Ventas**

Se han solucionado los siguientes problemas:

- La pestaña **Ejecución del contrato** en la página **Contrato** falla silenciosamente durante la inicialización cuando no hay líneas de contrato presentes.
