---
title: Novedades o cambios en la versión de actualización 18, V3, de Project Service Automation
description: En este artículo se enumeran las funciones y correcciones disponibles en Project Service Automation Update Release 18, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918885"
---
# <a name="project-service-automation-update-release-18-v3"></a>Versión de actualización de Project Service Automation 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea, página de soluciones para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation V3, Update Release 18. Esta versión tiene un número de compilación de V3.10.8.12 y generalmente está disponible a través de una actualización automática en abril de 2020.

## <a name="update-release-18"></a>Versión de actualización 18

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

- Corregido: los flujos **Recordar**, **Solicitud** y **Cancelar aprobación** arrojan excepciones con mensajes de error poco claros.
- Corregido: cuando **Cancelar aprobación** falla por un gasto, no se produce un error de excepción relevante.
- Corregido: la cuadrícula de entrada de tiempo gestiona incorrectamente los días no laborables en Australia después del cambio de horario de verano (DST) en octubre.
- Corregido: la lógica de incumplimiento incorrecta impide el envío de gastos.
- Corregido: cuando falla la aprobación de entrada de tiempo, la aprobación permanece en un estado de **Pendiente**.
- Corregido: errores de SQL en aprobaciones masivas (interbloqueo/tiempo de espera).
- Corregido: problemas de rendimiento significativos en la experiencia del usuario causados por la actualización de los miembros del equipo al aprobar las entradas de tiempo.

**Administración del proyecto**

- Corregido: notificación de zona horaria movida desde la vista **Reconciliación** al formulario principal de **Proyecto**.
- Corregido: la plantilla del calendario no se configura en sus valores predeterminados de manera correcta cuando se abre un nuevo formulario de proyecto.
- Corregido: para los navegadores basados en cromo, los usuarios no pueden seleccionar fácilmente las tareas predecesoras para eliminar.
- Corregido: crear o copiar **Proyecto desde una plantilla vacía** captura asignaciones no relacionadas.
- Corregido: en casos extremos específicos, la creación de una nueva asignación a partir de la cuadrícula de tareas produce una creación de registros duplicados.
- Corregido: en modo manual, los usuarios no pueden actualizar las fechas de inicio de las tareas para que sean posteriores a la fecha actual guardada.

**Administración de recursos**

- Corregido: la fila del subtotal de la vista **Reconciliación** calcula incorrectamente la varianza de las reservas después de extender las reservas.
- Corregido: la vista **Reconciliación** muestra incorrectamente las asignaciones de recursos cuando el recurso que se puede reservar tiene un calendario que no coincide con el calendario del proyecto.

**Sales**

- Corregido: cuando las entradas de tiempo se vuelven a aprobar (**Aprobar > Cancelar >**, aprobar nuevamente), se crea un duplicado real no imputable.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
