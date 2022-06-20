---
title: Novedades o cambios en la versión de actualización 32, V3, de Project Service Automation
description: En este artículo se enumeran las funciones y correcciones disponibles en Project Service Automation Update Release 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 5124137c24da9b579ee1365524d66d9135b2d420
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912905"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novedades o cambios en la versión de actualización 32, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation V3, Update Release 32. Esta versión tiene un número de compilación de V3.10.53.108 y estará disponible de manera general a través de una actualización automática en junio de 2021.

## <a name="update-release-32"></a>Versión de actualización 32

### <a name="bug-fixes"></a>Correcciones de errores

#### <a name="general"></a>General

- Cuando falla una actualización importante, solo se deben bloquear los puntos de entrada de la aplicación principal para garantizar que las entidades compartidas sigan siendo accesibles.

#### <a name="time-and-expense"></a>Tiempo y gasto

Se han solucionado los siguientes problemas:

- **TimeEntriesImportFromResourceAssignment** no mantiene las horas de inicio y finalización del segmento de perfil de asignación de recursos.
- Si selecciona **Entrada abierta** en la cuadrícula **Entrada de tiempo**, es posible que no pueda seleccionar otros formularios.
- Mientras importa asignaciones en entradas de tiempo, la consulta del código del cliente podría generar una URL larga que falle en la consulta.
- En la cuadrícula **Entrada de tiempo**, después de eliminar un valor de una celda, el foco no permanece en la cuadrícula.
- El botón **Rechazar** ha sido eliminado de la vista **Aprobaciones de procesamiento** de las aprobaciones modernas.
- La estabilidad y el rendimiento de la aprobación masiva de entrada de tiempo se ven afectados por interbloqueos y por un fallo en el manejo adecuado de las personalizaciones relacionadas con la entidad **Entrada de tiempo**.

#### <a name="project-planning"></a>Planificación de proyectos

- Se genera una excepción de referencia nula cuando actualiza un proyecto que tiene un valor nulo en el campo **Unidad de contratación**.
- **Actualizar totales del proyecto** calcula incorrectamente el coste restante y las ventas restantes en un proyecto.
- Los cálculos de precios redundantes afectan al rendimiento relacionado con las actualizaciones en los contornos de asignación de recursos.

#### <a name="resource-management"></a>Administración de recursos

Se ha resuelto el siguiente problema:

- Cuando la capacidad de calendario de un recurso que se puede reservar es superior a 1, Project Service Automation reconoce incorrectamente la capacidad como 0 (cero). Por lo tanto, se produce un bucle infinito en la vista de programación.

#### <a name="sales"></a>Ventas

Se han solucionado los siguientes problemas:

- Cuando se crea una línea de diario que tiene un tipo de transacción personalizado, se produce la siguiente excepción de referencia nula: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Los roles y categorías que se desactivan antes de copiar un presupuesto no deben agregarse a los roles y categorías imputables del presupuesto recién copiado.
- La fecha del documento y la fecha contable no están alineadas con la fecha de inicio que se proporciona en un detalle de línea de factura que se crea directamente en un borrador de factura.
- Las excepciones de referencias nulas se generan en escenarios relacionados con la inactivación de roles y categorías antes de que se copie un presupuesto.
- La acción **Actualizar precios** de la página **Proyectos** no actualiza las estimaciones de gastos ni las estimaciones de materiales.
