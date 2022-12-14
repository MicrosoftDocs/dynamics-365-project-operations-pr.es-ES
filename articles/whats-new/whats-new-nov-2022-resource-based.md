---
title: 'Novedades de noviembre de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de noviembre de 2022 de Microsoft Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831102"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de noviembre de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.58.0.119
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de escritura dual de Project Operations en esta versión. Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2781818 | Error de clave no encontrada al establecer el precio predeterminado para el registro de uso de material. |
| Facturación y precios | 2922373 | No se puede vincular la línea de presupuesto al proyecto que se ha cerrado como presupuesto perdido. |
| Facturación y precios | 2943206 | El campo **Línea de contrato** en la entidad del proyecto debe ser opcional. |
| Facturación y precios | 2953182 | Mejorar el mensaje de error para las facturas de corrección.|
| Facturación y precios | 2959500 | No se puede vincular la línea de presupuesto a una tarea de proyecto que ya está asociada con un presupuesto perdido.|
| Facturación y precios | 2959560 | Se recibió el mensaje "Este cliente ya está en el contrato del proyecto" al cerrar la cotización como ganada en ciertos lugares. |
| Facturación y precios | 3031727 | Las asignaciones de recursos fallan con el error Falta el campo obligatorio 'msdyn_Company'. |
| Facturación y precios | 3036905 | La empresa propietaria nunca se inicializa en ProjectTeamMember. |
| Administración de oportunidades | 2763519 | Error de referencia nula en EnsureProjectContractAllowsUpdates. |
| Administración de oportunidades | 2783798 | Al importar estimaciones de proyectos en la línea de cotización, faltan descripciones de tareas para estimaciones de gastos y materiales.|
| Administración de oportunidades | 2988635 | Mejore la descripción del mensaje de error al eliminar el cliente en la cotización. |
| Administración de oportunidades | 3001191 | No se puede crear una cotización de Oportunidad donde el método de facturación se especifica como nulo. |
| Actualizado | 3012324 | La conversión del proyecto falló en un proyecto con caracteres de control como Tabulador en su nombre. || Planificación y seguimiento de proyectos | 2790384 | El tiempo de espera de OperationSet pendiente es demasiado corto. |
| Planificación y seguimiento de proyectos | 3044275 | Falta la localización para: missingProjectSchedulerErrorMessage. |
| Planificación y seguimiento de proyectos | 3044277 | La cuadrícula de Project Recon no se carga cuando el programador no está configurado.|
| Administración de recursos | 2943153 | Actualice la pestaña Seguimiento para mostrar dos lugares decimales para la Duración.|
| Subcontratación | 2932774 | Línea de factura del proveedor Solo lectura arrojando error incorrectamente. |
| Subcontratación | 2939556 | El estado del encabezado de la factura del proveedor no debe configurarse como Borrador para eliminar en línea si no está activo. |
| Tiempo y gasto | 2939998 | Adopción de la nueva versión de TESA en ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Administración de proyectos y contabilidad en Finance

Para obtener información sobre las correcciones de errores incluidas en esta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services y consulte el [artículo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
