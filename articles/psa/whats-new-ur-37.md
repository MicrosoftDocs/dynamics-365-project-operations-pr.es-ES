---
title: Novedades o cambios en la versión de actualización 37, V3, de Project Service Automation
description: Este artículo enumera las funciones y correcciones que están disponibles en la actualización de la versión 37, V3 de Microsoft Dynamics 365 Project Service Automation.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922519"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novedades o cambios en la versión de actualización 37, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation Update Release 37, V3. Esta versión tiene un número de compilación de V3.10.58.120 y generalmente está disponible a través de una actualización automática en noviembre de 2021.

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
