---
title: 'Novedades en abril de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de abril de 2022 de Microsoft Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110905"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades en abril de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.41.0.45
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.26

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

Las categorías de adquisiciones pueden usarse en pedidos de compra de proyectos y facturas de proveedores pendientes. para más información, consulte [Usar categorías de compras con pedidos de compra de proyectos y facturas de proveedores pendientes](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

La siguiente tabla muestra los mapas de escritura dual que se modificaron o agregaron en la versión de marzo de 2022 de Project Operations.

| Asignación de entidad | Versión actualizada | Comments |
| -------------- | ------------------- | ------------|
| Entidad de exportación de línea de facturas de proveedores de proyectos de integración de Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Este mapa admite el uso de categorías de compras con pedidos de compra de proyectos y facturas de proveedores pendientes. |

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| ------------ | ---------------- | -------------- |
| Tiempo y gastos | 2573900 | La característica **Aprobación moderna** debe estar habilitada de manera predeterminada. |
| Facturación y precios | 2603313 | Se corrigió un error de registro duplicado que impedía agregar líneas de contrato y oferta que tienen un producto. |
| Implementación y configuración | 2611368 | Los clientes deben poder agregar hasta cinco entidades personalizadas a la solución mediante el diseñador de aplicaciones moderno. |
| Tiempo y gastos | 2628285 | Se solucionó un problema que afectaba la capacidad de establecer la categoría de recursos correcta durante la importación de entradas de tiempo. |
| Administración de oportunidades| 2628815 | Actualice el límite de caracteres de la descripción detallada de la línea de oferta para que coincida con el límite de caracteres del asunto de la tarea, de modo que la importación se realice correctamente para las tareas en las que el asunto tiene más de 100 caracteres. |
| Tiempo y gastos| 2629547 | El campo **Enviado por** de aprobaciones del proyecto debe apuntar al usuario que envió el registro. |
| Tiempo y gastos| 2629865 | El campo **Copiar categoría** en las tareas cuando se copian proyectos. |
| Tiempo y gastos| 2636463 | Se corrigieron los filtros de las aprobaciones en los formularios de aprobaciones modernos. |
| Planificación y seguimiento del proyecto | 2648300 | Se solucionó un problema que impedía cambiar el propietario del proyecto. |
| Facturación y precios | 2563000 | No se deben permitir líneas de diario para una venta no facturada en la que la moneda difiere de la moneda del contrato. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administración y contabilidad de proyectos de Dynamics 365 Finance

Para obtener información sobre las correcciones de errores incluidas en esta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) y consulte el [artículo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
