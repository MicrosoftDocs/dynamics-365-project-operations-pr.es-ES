---
title: Novedades o cambios en la versión de actualización 25, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 25, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183564"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novedades o cambios en la versión de actualización 25, V3, de Project Service Automation

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tema enumera las características y correcciones nuevas o modificadas para Project Service Automation V3, Update Release 25. Esta versión tiene un número de compilación de V 3.10.43.76 y generalmente está disponible a través de una actualización automática en octubre de 2020.

## <a name="update-release-25"></a>Versión de actualización 25

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se ha resuelto el siguiente problema:

- Gráfico de entrada de tiempo que muestra datos adicionales basados en un intervalo demasiado grande que se está recuperando.

**Administración de recursos**

Se ha resuelto el siguiente problema:

- Se agregó el código de Package Deployer para omitir la importación del parche de Universal Resource Scheduling si ya existe un parche de versión superior.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- Se corrigieron las discrepancias de redondeo y tipo de cambio que dieron como resultado un costo planificado incorrecto en la cuadrícula de seguimiento del proyecto.
- Admite la capacidad de mostrar dos o más cuadrículas de reacción en el formulario del **Proyecto**.
- Se proporcionó validación para abordar la capacidad de asignar una tarea después de la fecha de finalización del calendario, lo que da como resultado una asignación de recursos fallida.
- Manejo de errores mejorado para abordar la excepción de referencia nula generada a partir de lo siguiente:

    - Complemento **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** cuando se crea una tarea de proyecto sin un proyecto asociado
    - Complemento **PreProjectTeamMemberCreate**
    - Complemento **PostProjectTeamMemberDelete**
    - Complemento **PreValidateProjectTaskDelete**

**Sales**

Se han solucionado los siguientes problemas:

- Manejo de errores mejorado para abordar las excepciones de referencia nulas generadas **Copiar proyecto: Asistente de estimaciones Gestión de recursos**.
- **No listo para facturar** en un **Backlog de facturación de tiempo y material** no borra el estado de facturación.
- Corregidos los botones **Precios** mal etiquetados en la pestaña **Precio del rol** y **Artículos del catálogo**.