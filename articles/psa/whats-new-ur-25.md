---
title: Novedades o cambios en la versión de actualización 25, V3, de Project Service Automation
description: En este artículo se enumeran las funciones y correcciones disponibles en Project Service Automation Update Release 25, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922565"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novedades o cambios en la versión de actualización 25, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo, se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation V3, versión de actualización 25. Esta versión tiene un número de compilación V 3.10.43.76 y generalmente está disponible a través de una actualización automática en octubre de 2020.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
