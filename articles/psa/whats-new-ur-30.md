---
title: Novedades o cambios en la versión de actualización 30, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 30, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010447"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novedades o cambios en la versión de actualización 30, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution.md).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 30. Esta versión tiene un número de compilación de V3.10.51.61 y generalmente está disponible a través de una actualización automática en abril de 2021.

## <a name="update-release-30"></a>Versión de actualización 30

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- Se produce un error cuando crea y guarda una entrada de tiempo en la página **Creación rápida** si campo **Rol** se elimina.
- El filtro de entrada de tiempo aplica el operador de filtro incorrecto.
- Los partes de horas copiados no se muestran automáticamente cuando selecciona **Copiar semana** en el control de entrada de tiempo.

**Administración de recursos**

Se han solucionado los siguientes problemas:

- Cuando amplía una reserva, el estado de reserva asignado a la reserva física es incorrecto. La ampliación de una reserva respeta el estado de la reserva definido como **Comprometido** en los metadatos de configuración de la reserva.
- Cuando no se especifica un estado de reserva válido, el mensaje de error no se localiza correctamente.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- Los proyectos no se pueden crear en una divisa e incluir tareas relacionadas en otra divisa.

**Ventas**

Se han solucionado los siguientes problemas:

- Cuando se copia una lista de precios, los precios no se actualizan.
- El cierre de una cotización como obtenida produce errores cuando el detalle del coste tiene un valor para el origen.
- En la entidad **Tarea de proyecto**, **Coste estimado** ha sido renombrado a **Coste planificado (base)**.
- Se genera una excepción de referencia nula cuando se crean o eliminan facturas.
