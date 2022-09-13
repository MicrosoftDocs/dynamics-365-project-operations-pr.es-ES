---
title: 'Novedades de agosto de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de agosto de 2022 de Microsoft Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403878"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de agosto de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.45.0.53
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de escritura dual de Project Operations en esta versión. Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Administración de oportunidades | 2762089 | Gestión de errores al cerrar el contrato como perdido si el guardado automático está deshabilitado en la organización.|
|Planificación y seguimiento de proyectos | 2767841 | Actualizaciones de telemetría en escenarios de crear o actualizar una entidad de proyecto.|
|Facturación y precios | 2771072 | Gestión de excepciones de referencia nula mientras se gana la oferta.|
|Facturación y precios | 2844181 |Error al obtener una identificación de correlación y bloquear la creación de una factura.|
|Facturación y precios | 2852836 | Faltan datos reales de empresas vinculadas para Gastos de empresas vinculadas creados y aprobados en CE.|


### <a name="project-management-and-accounting-in-finance"></a>Administración de proyectos y contabilidad en Finance

Para obtener información sobre las correcciones de errores incluidas en esta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) y consulte el [artículo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
