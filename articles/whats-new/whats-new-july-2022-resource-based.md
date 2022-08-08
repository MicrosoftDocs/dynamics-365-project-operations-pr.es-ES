---
title: 'Novedades de julio de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de julio de 2022 de Microsoft Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183940"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de julio de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.44.0.22
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de escritura dual de Project Operations en esta versión. Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Implementación y configuración | 2761472 | Se controla un error de instalación de Project Operations. |
| Facturación y precios | 2746940 | El nombre de la línea del subcontrato debe tener una longitud máxima de 100 caracteres. |
| Facturación y precios | 2739162 | Los clientes deben poder ver los botones de la cinta de enfoques en la vista de cuadrícula de datos reales. |
| Planificación y seguimiento de proyectos | 2730318 | Validación actualizada para caracteres no admitidos en el asunto del proyecto. |
| Facturación y precios | 2705361 | Los datos reales de ventas facturados por hitos deben incluirse en los campos de seguimiento del proyecto. |
| Facturación y precios | 2675880 | Evite que un proyecto se vincule a una línea de contrato que no esté basada en el trabajo. |
| Facturación y precios | 2664396 | Si se guarda una lista de precios de oferta sin una oferta, debe haber un error que indique que la oferta no puede estar vacía. |
| Facturación y precios | 2184019 | La pestaña **Facturación basada en tareas** no debe mostrarse para proyectos que no tienen oferta o contrato de respaldo. |

### <a name="project-management-and-accounting-in-finance"></a>Administración de proyectos y contabilidad en Finance

Para obtener información sobre las correcciones de errores incluidas en esta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) y consulte el [artículo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Características desactivadas de manera determinada en próxima versión

La tabla siguiente enumera las características que se han activado de forma predeterminada en la versión 10.0.29. La mayoría de las características que se han activado de forma automática se pueden desactivar en [Administración de características](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). En el futuro, es posible que algunas características que se han activado automáticamente se eliminen de la Administración de características y se vuelvan obligatorias. Este cambio garantiza que los clientes utilicen la funcionalidad actual, de modo que las mejoras puedan basarse en la funcionalidad actual a medida que se agregan. Las características nunca se habilitarán automáticamente en menos de un año, a menos que se determine que son esenciales.

| Nombre de característica | Habilitar fecha | Fecha de adición de característica | Estado de la característica | Módulo |
| --- | --- | --- |--- |--- |
| Habilitar el ajuste de la transacción de hora según el cambio en la asignación de la regla de financiación | 16 de septiembre de 2022 | 7 de octubre de 2020 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Característica de reversión de factura de pago anticipado de pedido de compra de proyecto | 16 de septiembre de 2022 | 6 de octubre de 2021 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Eliminar líneas de propuesta de factura al usar Project Operations para escenarios basados en recursos/no mantenidos en existencias | 16 de septiembre de 2022 | 6 de octubre de 2021 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Ajustar la contabilidad en una transacción de proyecto registrada | 16 de septiembre de 2022 | 10 de mayo de 2020 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Habilitar la configuración de contabilidad predeterminada para el proyecto | 16 de septiembre de 2022 | 19 de febrero de 2020 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Habilitar varias líneas de contrato para un proyecto | 16 de septiembre de 2022 | 29 de Junio de 2020 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Hacer que los diarios de horas del proyecto sean de solo lectura si el estado de aprobación actual no permite la edición | 16 de septiembre de 2022 | 6 de octubre de 2021 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Habilitar la sincronización de líneas de venta desde las líneas de compra cuando las líneas de compra se actualicen y el parámetro de administración de cambios de pedidos de compra esté activado | 16 de septiembre de 2022 | 7 de octubre de 2020 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Habilitar Project Operations en Dynamics 365 Customer Engagement | 16 de septiembre de 2022 | 29 de Junio de 2020 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |
| Característica de corrección de reversión de transacciones de proyectos | 16 de septiembre de 2022 | 13 de Julio de 2020 | Activada de forma predeterminada | Gestión de proyectos y contabilidad |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Características que serán obligatorias en la próxima versión

La tabla siguiente enumera las características que son obligatorias desde la versión 10.0.29 en adelante.

| Nombre de característica | Habilitar fecha | Fecha de adición de característica | Estado de la característica | Módulo |
| --- | --- | --- | --- | --- |
| Calcular el valor comprometido en la fuente de financiación sin redondear el tipo de cambio | 16 de septiembre de 2022 | 14 de Junio de 2020 | Obligatorio | Gestión de proyectos y contabilidad |
| Habilitar el registro de ajustes del proyecto con la misma cuenta contable que la transacción original | 16 de septiembre de 2022 | 14 de Junio de 2020 | Obligatorio | Gestión de proyectos y contabilidad |
| Detalle del importe comprometido del contrato del proyecto | 16 de septiembre de 2022 | 31 de agosto de 2019 | Obligatorio | Gestión de proyectos y contabilidad |
| Habilitar la clasificación por recurso durante la creación de propuestas de facturas de proyectos | 16 de septiembre de 2022 | 31 de agosto de 2019 | Obligatorio | Gestión de proyectos y contabilidad |
