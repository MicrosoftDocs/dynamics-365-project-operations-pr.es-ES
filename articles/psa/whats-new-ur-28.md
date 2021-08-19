---
title: Novedades o cambios en la versión de actualización 28, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 28, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: fed18ba292943f53965ee518afb5cbb13427ca60f32451edb49f67e6f10d24fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994972"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novedades o cambios en la versión de actualización 28, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

Este tema enumera las características y correcciones nuevas o modificadas para Project Service Automation V3, Update Release 28. Esta versión tiene un número de compilación de V3.10.46.32 y generalmente está disponible a través de una actualización automática en enero de 2021.

## <a name="update-release-28"></a>Versión de actualización 28

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- Los usuarios disponen de la opción **Edición masiva** para actualizar las entradas de tiempo aprobadas y enviadas.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- En aquellos casos en los que el GUID de la tarea se interprete como un número, las tareas no se podrán abrir para edición mediante **Editar tarea** en la cinta de la página **Estructura de descomposición del trabajo**.

**Sales**

Se han solucionado los siguientes problemas:

- Se genera una excepción de referencia nula cuando se invoca el complemento **GetEstimatesForProject**.
- La opción **Marcar como listo para facturar** de la cuadrícula de hitos solo actualiza parcialmente los atributos, con la excepción del atributo **InvoiceStatus**, que se actualiza.



[!INCLUDE[footer-include](../includes/footer-banner.md)]