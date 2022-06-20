---
title: 'Novedades de diciembre de 2021: implementación de Project Operations Lite'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de diciembre de 2021 de la implementación simplificada de Project Operations.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914101"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novedades de diciembre de 2021: implementación de Project Operations Lite

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en la versión del entorno de Dataverse 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

### <a name="subcontract-management"></a>Administración de subcontrataciones 

- [Subcontratación de miembros del equipo del proyecto](../subcontracting/subcontracting-project-team-members.md): un gerente de proyecto puede crear miembros del equipo con nombre o genéricos con subcontratos y líneas de subcontratos para impactar la dotación de personal y la estimación.
- [Opciones de subcontratación para los miembros del equipo del proyecto](../subcontracting/subcon-options.md): al hacer elecciones de personal para los miembros del equipo del proyecto con nombre o genéricos, el director del proyecto puede revisar los subcontratos existentes o crear nuevos subcontratos para uno o más miembros del equipo del proyecto. 
- [Estimación de costos de asignaciones de recursos subcontratados](../subcontracting/costing-subcon-ra.md): la estimación de costos del proyecto tomará en cuenta las asignaciones de recursos subcontratados y los costará utilizando las listas de precios de compra asociadas con los subcontratos. 
- [Configure el tablero de programación para mostrar a los trabajadores contratados y la capacidad subcontratada](../subcontracting/configure-sb-subcon.md): el tablero de programación en Project Operations ahora se puede configurar para buscar y sugerir el tipo de trabajador contratado de recursos reservables y capacidad subcontratada junto con los empleados. Esta configuración se puede aplicar cuando se buscan recursos dentro del contexto de la dotación de personal para un requisito de proyecto específico o cuando se busca fuera del contexto de un requisito de proyecto.
- [Dotar de personal a un proyecto con trabajadores contratados y capacidad subcontratada](../subcontracting/staffing-cw.md): los trabajadores contratados ahora se pueden contratar en proyectos que aprovechan las experiencias del tablero de programación.
- [Registro de tiempo, gastos y uso de material en proyectos para componentes subcontratados](../subcontracting/recording-subcon-actuals.md): los trabajadores contratados pueden registrar el tiempo y los gastos, y los miembros del equipo del proyecto también pueden registrar el uso de los materiales comprados mediante un subcontrato en un proyecto. Esto dará como resultado el registro de costos precisos en proyectos que utilizan la capacidad o los materiales adquiridos.
- [Transiciones de estado en un subcontrato](../subcontracting/subcon-states.md): los subcontratos pueden confirmarse para completar la negociación con el proveedor, cerrarse para indicar la finalización de la entrega o cancelarse para indicar la terminación del contrato con el proveedor antes de la finalización de la entrega.

### <a name="task-planning"></a>Planificación de tareas
- Solución de problemas mejorada para administradores del sistema. Cuando un usuario no puede abrir un proyecto, el Administrador puede revisar los errores no relacionados con la licencia generados desde Project for the Web en los [Registros de programación de proyectos](../../project-management/schedule-api-logs.md).
- [Usar listas de verificación de tareas en Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). En Microsoft Project for the Web, puede agregar una lista de verificación a una tarea para realizar un seguimiento de elementos específicos.

## <a name="quality-updates"></a>Actualizaciones de calidad

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Planificación y seguimiento | 2392596 | Las API de programación ahora permiten actualizaciones en los campos **Esfuerzo restante**, **Esfuerzo completado** y **% completado**. |
| Planificación y seguimiento | 2478497 | Los campos **Número de actividad** e **ID de tarea** para las API de programación pueden estar en blanco al ingresar porque el sistema los completará mediante la numeración automática.|
| Tiempo y gasto | 2468135 | El número de reintentos de aprobación se reduce de cinco a tres. |
| Tiempo y gasto | 2468188 | Se solucionó el problema con el texto del registro que excedía la longitud máxima en el atributo **notetext** de la entidad **anotación**. |
