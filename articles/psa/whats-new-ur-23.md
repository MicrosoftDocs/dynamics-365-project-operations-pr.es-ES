---
title: Novedades o cambios en la versión de actualización 23, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 23, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006487"
---
# <a name="project-service-automation-update-release-23-v3"></a>Versión de actualización de Project Service Automation 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 23. Esta versión tiene un número de compilación de V 3.10.34.30 y está disponible con carácter general a través de una actualización automática en agosto de 2020.

## <a name="update-release-23"></a>Versión de actualización 23

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas:
- Gestione un caso perimetral en **Eliminación de miembro del equipo del proyecto** para proporcionar una excepción significativa.
- La importación de asignaciones da como resultado una pantalla de eliminación en blanco.

**Administración de recursos**

Se han solucionado los siguientes problemas:

- La **Tarjeta de recursos de la cuadrícula de utilización de recursos** muestra datos incorrectos cuando la escala de tiempo es superior a cinco días.
- Cuando los clientes crean un recurso que se puede reservar, el complemento genera un error intermitentemente al agregar automáticamente el recurso a un grupo de Microsoft Office 365.
- La vista **Conciliación** muestra los contornos manuales incorrectamente en la vista **Semana** o **Mes**.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- Un número excesivo de entidades **RetrieveMultiple para usersettings** están causando un rendimiento degradado para aprobaciones de proyectos y otras operaciones.
- La búsqueda de recursos de la cuadrícula **Planificación de tareas** se limita a mostrar solo hasta cinco miembros del equipo del proyecto. 
- La búsqueda de recursos de la cuadrícula **Planificación de tareas** no filtra los recursos inactivos.
- El modo manual no funciona como se esperaba en la estructura de descomposición del trabajo de planificación del proyecto.
- La cuadrícula **Planificación de tareas** muestra **Categorías de transacciones inactivas**.
- La cuadrícula **Asignación de recursos** se redondea incorrectamente cuando una tarea tiene varias asignaciones.
- Los valores de redondeo son diferentes entre el coste planificado y el coste real para una única tarea.

**Sales**

Se han solucionado los siguientes problemas:

- Hacer doble clic en **Capturar todas las categorías de transacciones** crea varias líneas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]