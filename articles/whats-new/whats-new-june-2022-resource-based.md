---
title: 'Novedades de junio de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de junio de 2022 de Microsoft Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031352"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de junio de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en la versión del entorno de Dataverse 4.43.0.77 o 4.43.0.119
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

La siguiente tabla muestra los mapas de escritura dual que se modificaron o agregaron en la versión de junio de 2022 de Project Operations.

| Asignación de entidad | Versión actualizada | Comments |
| --- | --- | --- |
| Entidad de exportación de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | El campo heredado quedó en desuso y se asignó al nuevo campo para el seguimiento del estado de la factura del proveedor. |

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Subcontratación | 2708885 | Se corrigió el mensaje de error que aparece cuando un usuario crea un registro de encabezado de reserva de recursos reservables donde no se completa ningún recurso reservable. |
| Planificación y seguimiento del proyecto | 2629441 | Se corrigió la lógica de activación del flujo de trabajo para ayudar a evitar un bucle infinito cuando se actualizan las tareas del proyecto. |
| Tiempo y gastos | 2641209 | Las importaciones de entradas de tiempo de asignaciones/reservas deben conservar una referencia de recurso reservable. |
| Planificación y seguimiento del proyecto | 2651148 | El encabezado del documento del proyecto debe estar protegido.|
| Planificación y seguimiento del proyecto | 2653145 | Se agregaron validaciones para garantizar que no se pueda crear un registro de proyecto que tenga caracteres no válidos en su nombre. |
| Tiempo y gastos | 2654710 | Corregido el filtrado en la página **Aprobaciones**. |
| Facturación y precios | 2667805 | Se agregaron validaciones para ayudar a evitar que se creen datos reales de ventas facturados si no existen respaldos de datos reales de ventas no facturados. |
| Facturación y precios | 2668378 | Se agregaron validaciones para ayudar a evitar que se agregue una dimensión de precios personalizada a menos que se complete un nombre lógico y un nombre de campo. |
| Subcontratación | 2677485 | Se actualizó la versión de destino del mapa de doble escritura de las líneas de factura del proveedor. |
| Tiempo y gastos | 2700428 | Se mejoró la lógica de aprobaciones para garantizar que se puedan procesar otros conjuntos de aprobación para el proyecto incluso si uno de los conjuntos de aprobación está atascado en los trabajos del sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Administración de proyectos y contabilidad en Finance

Para obtener información sobre las correcciones de errores incluidas en esta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) y consulte el [artículo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
