---
title: Novedades o cambios en la versión de actualización 19, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 19, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143672"
---
# <a name="project-service-automation-update-release-19-v3"></a>Versión de actualización de Project Service Automation 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 19. Esta versión tiene un número de compilación V3.10.30.41 y generalmente está disponible a través de una actualización automática de mayo de 2020.

## <a name="update-release-19"></a>Versión de actualización 19

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas: 

- Errores derivados de que las importaciones de entrada de tiempo no se muestran correctamente.
- Cuadrícula de entrada de tiempo no admite el comportamiento de campo **Solo fecha**.
- Los recursos del proyecto no pueden crear un gasto con un proyecto.

**Administración del proyecto**

Se han solucionado los siguientes problemas: 

-  La tarea descendiente de la secundaria provoca una estimación de esfuerzo incorrecta durante el Cálculo de finalización (EAF).

**Sales**

Se han solucionado los siguientes problemas: 

- La acción **Recalcular** no funciona con detalles de línea de contrato de gastos o detalles de línea de presupuesto.
- **Actualizar precios** falta para las estimaciones de gastos.
-  Los clientes no pueden seleccionar los motivos del estado del contrato personalizados desde la página **Contrato del proyecto**.
- Los clientes experimentan un rendimiento degradado al crear una lista de precios personalizada a partir de un presupuesto.
- Los clientes experimentan incoherencias con las **unidades** predeterminadas en **Detalles de línea de presupuesto** y las páginas **Detalles de línea de contrato**.
- La adición de elementos de categoría de transacción imputable a una línea de contrato imputable no respetará el tipo de facturación **No cargable** de la categoría de transacción.
- Los clientes no pueden usar los roles y la categoría recién agregados en los contratos creados anteriormente.
- Los clientes experimentan un rendimiento degradado por recuperación innecesaria en PreValidateProjectTeamMemberUpdate.cs
- Los roles configurados como no cargables en la lista **Categorías de recursos** deberían agregarse a la pestaña **Roles cargables** como **No cargable** en la línea del contrato para un proyecto.
- Los clientes pueden experimentar un rendimiento degradado al crear un proyecto porque **GetBookableResourceIdFromUser** recupera todas las columnas de recursos reservables en lugar de solo el identificador principal.
- La entidad **Tipo de transacción** carece del complemento de actualización de prevalidación para evitar que los usuarios ingresen **Unidades** y **Grupos de unidades** no válidos para los tipos de transacción.
- El paso **Eliminar** no funciona para la importación de entrada de tiempo.
