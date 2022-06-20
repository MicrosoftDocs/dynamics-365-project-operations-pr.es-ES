---
title: Novedades o cambios en la versión de actualización 33, V3, de Project Service Automation
description: En este artículo se enumeran las funciones y correcciones disponibles en Project Service Automation Update Release 33, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915437"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novedades o cambios en la versión de actualización 33, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation V3, Update Release 33. Esta versión tiene un número de compilación de V3.10.54.98 y generalmente está disponible a través de una actualización automática en julio de 2021.

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
