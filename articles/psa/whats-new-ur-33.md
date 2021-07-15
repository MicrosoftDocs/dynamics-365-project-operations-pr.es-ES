---
title: Novedades o cambios en la versión de actualización 33, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 33, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334605"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novedades o cambios en la versión de actualización 33, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 33. Esta versión tiene un número de compilación de V3.10.54.98 y generalmente está disponible a través de una actualización automática en julio de 2021.

## <a name="update-release-33"></a>Versión de actualización 33

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- Dos campos cerrados, **msdyn_description** y **msdyn_externaldescription**, son editables después del envío.
- Aparece un mensaje de error si se crea un gasto que no está relacionado con un proyecto.
- Cuando se crea una entrada de tiempo, el rol de recurso se establece de forma predeterminada a un rol inactivo.
- Las líneas del diario asociadas con un gasto retirado y eliminado no se eliminan.
- En el **Formulario de creación rápida de entrada de tiempo**, actualice la vista **Lista de tareas del proyecto** para cambiar la fecha que se muestra de forma predeterminada a la fecha de inicio de la tarea.
- Cuando crea una entrada de tiempo desde la pestaña **Relacionados** del recurso que se puede reservar, la entrada de tiempo se crea incorrectamente para el usuario que inició sesión en lugar del recurso que se puede reservar principal.
- Se agregan nuevos campos al cuadro de diálogo **MDD de aprobación en masa**.

**Planificación del proyecto**

Se han solucionado los siguientes problemas:
- Rendimiento lento en la creación de proyectos cuando se aplican plantillas de horas de trabajo del proyecto con calendarios complejos.
- Cuando la fecha de inicio es mayor que la fecha final, se muestra un error en la plantilla del proyecto de texto debido a diferencias en el componente de tiempo de cada campo.

**Administración de recursos**

Se han solucionado los siguientes problemas:
- Se utiliza un parámetro incorrecto en la consulta de uso de recursos y el XML lleva a resultados de filtro incorrectos en la cuadrícula **Utilización de recursos**.
- La confirmación **Ampliar reservas** muestra una fecha final incorrecta para las reservas.

**Ventas**

Se han solucionado los siguientes problemas:
- Se produce un mensaje de error si se crea un precio de categoría al que le falten valores.
- Se produce un mensaje de error si se crea un hito de línea de contrato sin una línea de pedido.
