---
title: Novedades o cambios en la versión de actualización 35, V3, de Project Service Automation
description: Este artículo enumera las funciones y correcciones que están disponibles en la actualización de la versión 35, V3 de Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912859"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novedades o cambios en la versión de actualización 35, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation Update Release 35, V3. Esta versión tiene un número de compilación V3.10.56.110 y generalmente está disponible a través de una actualización automática en septiembre de 2021.

## <a name="update-release-35"></a>Versión de actualización 35

### <a name="bug-fixes"></a>Correcciones de errores

Se han solucionado los siguientes problemas.

**Tiempo y gasto**

- El aprobador del proyecto recibe un error de privilegio de lectura cuando aprueba entradas de gastos con un rol de **Aprobador de proyectos**.
- El aprobador del proyecto recibe un error de privilegio de escritura en **msdyn_projectapproval** cuando cancelan una entrada de tiempo aprobada con un rol de **Aprobador de proyectos**.
- Al seleccionar **Copiar semana** en una entrada de tiempo en el módulo de la aplicación Dynamics 365 para teléfonos, módulo de la aplicación de Project Resource Hub, se produce el siguiente error: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE".
- La política **Reintentar** aprueba automáticamente las entradas que se rechazaron previamente.
- La subcuadrícula **Conjuntos de aprobación** muestra acciones de cinta no aplicables.
- Faltan iconos para **Tarea de proyecto** y **Rol de recurso** en la entidad **Entrada de tiempo**.
- Cuando importa asignaciones de recursos, las entradas de tiempo importadas no tienen la duración correcta para las asignaciones que se crearon mediante tareas en modo manual.
- Falta **Eliminar** en la página **Búsqueda avanzada de registros de entrada de tiempo**.
- Falta **Guardar** en la página **Información de entrada de tiempo**. Este problema evita que los cambios se guarden al cerrar la página.

**Planificación del proyecto**

- Las cuadrículas **Asignación de recursos** y **Conciliación de recursos** no ordenan los atributos agrupados alfabéticamente.
- No se pueden crear tareas si el comportamiento de la fecha está personalizado para **Solo fecha**.

**Administración de recursos**

- Si tanto Dynamics 365 Field Service como Project Service Automation están instalados, se producen problemas de superposición cuando **Vista asociada de requisitos de recursos** se asocia con una página principal.
- Hacer doble clic en **Guardar**, en el cuadro de diálogo **Creación rápida de miembros del equipo**, evita que se cree el requisito de recursos.

**Ventas**

- Se lanza una excepción si se elimina una tarea que está asociada con un presupesto que tiene estado **Ganado**.
