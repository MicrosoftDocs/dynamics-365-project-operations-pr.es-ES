---
title: Novedades o cambios en la versión de actualización 12, V3, de Project Service Automation
description: Este tema proporciona información sobre las novedades de la versión de actualización 12 de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 5f05488a652f7a699aaa5d8e644eae38d7083f404d3c461cdaabd1915b1a710a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004512"
---
# <a name="project-service-automation-update-release-12-v3"></a>Versión de actualización de Project Service Automation 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA). Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 12. Esta versión tiene un número de compilación de V3.10.2.34 y está disponible con carácter general a través de una actualización automática en octubre de 2019.

## <a name="update-release-12"></a>Versión de actualización 12

### <a name="bug-fixes"></a>Solución de errores

- Tiempo y gasto

    - Corregido: Los mensajes de error de entrada de tiempo se han actualizado con un contexto más relevante.
    - Corregido: La programación y cuadrícula de entrada de tiempo muestra correctamente la barra de desplazamiento vertical cuando es necesario.
    - Corregido: Se pueden aprobar las entradas de tiempo y gasto enviadas.
    - Corregido: Se ha corregido el mensaje de diálogo de confirmación de cancelación de aprobación para reflejar el estado de la aprobación cuando se cambia de **Aprobado** a **Enviado**.
    - Corregido: Los campos **Precio**, **Unidad** y **Cantidad** están ahora bloqueados en el registro Gasto después de que se haya aprobado.

- Administración del proyecto

    - Fijo: Se ha eliminado la acción **Nuevo** del formulario principal **Miembro del equipo**.
    - Corregido: Se han actualizado las asignaciones de recursos para explicar errores de redondeo impreciso, que conducen a un cambio en la fecha de finalización de una tarea.
    - Corregido: En la cuadrícula de tareas, los errores del lado del servidor relevantes aparecerán al usuario.
    - Corregido: El nombre del miembro del equipo ahora se muestra en el selector de usuarios de la tarea en lugar del nombre del puesto.

- Administración de recursos

    - Corregido: Los detalles de los requisitos de recursos para los proyectos creados a partir de una plantilla ahora usan el calendario del proyecto.
    - Corregido: Las habilidades y competencias ahora pasan de manera predeterminada de los datos maestros de rol al requisito de recurso creado para ese rol.

- Sales

    - Corregido: ID de objetos duplicados encontrados en el formulario **principal de contrato**.
    - Corregido: La lógica se ha actualizado para hacer que la pestaña **Análisis de la oferta** esté visible para que muestre la configuración de metadatos de la pestaña.
    - Corregido: La Fecha contable del registro actual ahora proviene de la fecha de entrada de tiempo/gasto y no de la fecha de la aprobación.


[!INCLUDE[footer-include](../includes/footer-banner.md)]