---
title: Novedades o cambios en la versión de actualización 37, V3, de Project Service Automation
description: Este tema enumera las características y correcciones que están disponibles en Microsoft Dynamics 365 Project Service Automation, versión de actualización 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727626"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novedades o cambios en la versión de actualización 37, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation, versión de actualización 37, V3. Esta versión tiene un número de compilación de V3.10.58.120 y generalmente está disponible a través de una actualización automática en noviembre de 2021.

## <a name="update-release-37"></a>Versión de actualización 37

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Tiempo y gasto**
- Los usuarios no pueden eliminar una entrada de tiempo borrando la celda.
- La vista **Mi aprobación fallida** solo contiene aprobaciones de proyectos con un estado de **Enviado**.

**Administración de proyectos**
- Los usuarios reciben un error de excepción de referencia nula al abrir un proyecto en el complemento de escritorio de Microsoft si el nombre del puesto del miembro del equipo del proyecto está vacío.
- No hay botón **Guardar** en la página **Tarea de proyecto** para que los usuarios no puedan guardar los cambios en los registros de tareas.
- Los usuarios no pueden eliminar un proyecto que tiene una tarea asociada a una cotización con un estado de **Ganado**.

**Ventas**
- El campo **Divisa** en la página **Proyecto** se actualiza para que coincida con la moneda de la plantilla aplicada.
- El costo se calcula incorrectamente en tareas que tienen varias monedas.
