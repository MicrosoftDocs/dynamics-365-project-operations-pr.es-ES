---
title: 'Novedades de octubre de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de octubre de 2022 de Microsoft Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806626"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de octubre de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.57.0.176
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.30

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

| Área de características | Nombre de característica | Más información |
| --- | --- | --- |
| Planificación y seguimiento de proyectos | **Programación externa de Project Operations**<br>El modo de programación externa permite a los clientes crear, actualizar y eliminar de forma nativa entidades relacionadas con estructuras de descomposición del trabajo (WBS) usando API de Dataverse nativas sin los límites actuales que impone Microsoft Project for the Web. | [Programación externa](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementación y configuración | <p>**Permitir que los clientes elijan el tipo de implementación**<br>Las actualizaciones impulsadas por productos (PDU) de Project Operations se utilizan para instalar automáticamente la solución de escritura dual de Project Operations cuando las soluciones centrales y de orquestación de escritura dual están instaladas en el entorno.</p><p>Esta función introduce un nuevo parámetro **Comportamiento de actualización de la solución** en los parámetros del proyecto. Cuando este parámetro se establece en **Solo Lite**, las PUD ya no instalarán automáticamente la solución de escritura dual de Project Operations aun cuando las soluciones centrales y de orquestación de escritura dual están instaladas en el entorno. Este comportamiento beneficiará a los clientes que planean usar soluciones de escritura dual para integrar pedidos de ventas en aplicaciones de finanzas y operaciones, pero desean usar Project Operations en modo Lite (es decir, sin integración en aplicaciones de finanzas y operaciones).</p> | |
| Facturación y precios | <p>**Conversión de moneda para transacciones de venta no facturadas de gastos en entornos integrados**<br>Para los clientes que usan Project Operations integrado con aplicaciones de finanzas y operaciones (es decir, en el tipo de implementación de recursos/sin existencias), los tipos de cambio generalmente se controlan en las aplicaciones de finanzas y operaciones. Sin embargo, si se debe fijar el precio de una categoría de gastos utilizando el método de cálculo de precio "al costo" o "recargo sobre el costo" cuando se factura al cliente, el tipo de cambio que se usa para calcular el monto de las ventas usa los tipos de cambio en Dataverse, no los tipos de cambio de las aplicaciones de finanzas y operaciones.</p><p>Esta función introduce un nuevo parámetro **Comportamiento de conversión de divisa** en los parámetros del proyecto. Cuando este parámetro se establece en **Extendido con respaldo**, los importes de ventas no facturados en transacciones de gastos se calculan utilizando los tipos de cambio de las aplicaciones de finanzas y operaciones.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de escritura dual de Project Operations en esta versión. Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2316317 | El sistema permite crear facturas que no tengan transacciones imputables. |
| Facturación y precios | 2737300 | Valide la disponibilidad del campo **Cliente** antes de acceder al formulario. |
| Facturación y precios | 2744948 | Agregue una verificación nula para el método de facturación. |
| Facturación y precios | 2763515 | Manejador de error de referencia nula cuando falta el contrato de venta de la factura. |
| Facturación y precios | 2844301 | La creación de facturas por lotes falla debido a un error. |
| Facturación y precios | 2845869 | Almacenamiento incorrecto del servicio de organización. |
| Facturación y precios | 2853729 | Los detalles de la función y el precio se actualizan cuando se modifica el tipo de facturación. |
| Facturación y precios | 2940350 | Cuando se determina el precio de los datos reales, solo se deben ingresar automáticamente las listas de precios activas. |
| Implementación y configuración | 3001206 | La entidad msdyn\_replaylogheader impide las actualizaciones de las organizaciones de clientes. |
| Administración de oportunidades | 2755582 | Control de excepciones de referencia nula en el asistente de regla de facturación dividida. |
| Administración de oportunidades | 2761477 | Cuando se utiliza la facturación dividida, la eliminación de un hito (encabezado) deja hitos huérfanos. |
| Administración de oportunidades | 2767595 | Cuando se abre un registro de uso de material en el formulario principal, el recurso que se puede reservar para el registro cambia al usuario que ha iniciado sesión actualmente. |
| Planificación y seguimiento de proyectos | 2790384 | El tiempo de espera de OperationSet pendiente es demasiado corto. |
| Planificación y seguimiento de proyectos | 2957840 | Las tareas no se pueden guardar y las columnas no se pueden agregar a la página **Tareas** en Integrated Project Operations. |
| Administración de recursos | 2751560 | Unidades organizativas preferidas incoherentes en los requisitos de recursos. |
| Subcontratación | 2853245 | La coincidencia de los datos reales de la línea de factura del proveedor no actualiza el estado de verificación si una línea de contrato ya está vinculada a la línea de factura del proveedor. |
| Subcontratación | 2907231 | La etapa de proceso de las facturas de proveedores no puede avanzar. |
| Tiempo y gasto | 2867363 | Los registros no quedan fuera de la vista Ausencias/Vacaciones para aprobación cuando están en cola para aprobación. |
| Tiempo y gasto | 2894405 | TESA: El directorio POC no utilizado está causando problemas de cumplimiento. |

### <a name="project-management-and-accounting-in-finance"></a>Administración de proyectos y contabilidad en Finance

Para obtener información sobre las correcciones de errores incluidas en esta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services y consulte el [artículo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
