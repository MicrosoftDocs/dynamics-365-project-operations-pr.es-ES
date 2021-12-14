---
title: 'Novedades de noviembre de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de noviembre de 2021 de la implementación de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827347"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de noviembre de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

*Se aplica a: Project Operations para escenarios basados en recursos/no mantenidos en existencias*

Este tema se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en la versión del entorno de Dataverse 4.26.0.145, 4.26.0.148, o 4.26.0.150
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance versión 10.0.22

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- Las interfaces de programación de aplicaciones (API) de programación de proyectos ahora admiten la capacidad de crear y eliminar depósitos de proyectos.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de escritura dual de Project Operations en esta versión. Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-in-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2240080 | El campo **Términos de pago** no debe estar duplicado en la factura proforma. |
| Facturación y precios | 2358236 | La corrección de facturas debe permitir correcciones que tengan líneas de precio cero. |
| Administración de recursos | 2410072 | Permite la configuración de un recurso que está asignado a la tarea como un administrador de proyecto. |
| Facturación y precios | 2430234 | Solucione un problema de cálculo de rendimiento de costos. |
| Tiempo y gasto | 2436978 | Permita que se ingrese el tiempo en formato hh:mm. |
| Facturación y precios | 2448623 | Permitir que las listas de precios se actualicen después de que estén asociadas a una unidad organizativa. |
| Tiempo y gasto | 2460396 | Permita que se elimine una entrada de tiempo borrando la celda. |
| Facturación y precios | 2467386 | Permita que se elimine un proyecto que tiene una tarea, incluso cuando la tarea esté asociada con una cotización ganada. |
| Tiempo y gasto | 2461744 | La vista **Mi aprobación fallida** solo contiene aprobaciones de proyectos con un estado de **Enviado**. |
| Tiempo y gasto | 2464082 | Elimine el enlace de aprobaciones de proyectos al conjunto de aprobaciones cuando se coincida con un estado de destino. |
| Tiempo y gasto | 2468108 | El trabajo de programación no debe establecer un estado **Procesando** del conjunto de aprobaciones. |
| Tiempo y gasto | 2471503 | Elimine los conjuntos de aprobación que tengan siete días de antigüedad. |
| Facturación y precios | 2480687 | La referencia de la línea de cotización no debe eliminarse cuando se crea un hito de la línea de cotización. |

### <a name="project-management-and-accounting-in-finance"></a>Administración de proyectos y contabilidad en Finance

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Gestión de proyectos y contabilidad | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Los importes retenidos por el proveedor en las transacciones de gastos del proyecto no se muestran en la lista de transacciones. |
| Gestión de proyectos y contabilidad | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La factura del proveedor de empresas vinculadas se rompe cuando se activa la integración de la factura del proveedor. |
| Gestión de proyectos y contabilidad | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Las condiciones de pago de las facturas del proyecto no funcionan como se esperaba. |
| Gestión de proyectos y contabilidad | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Cuando se libera la retención del proveedor, la contabilización del comprobante tiene líneas adicionales incorrectas. |
| Gestión de proyectos y contabilidad | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Cuando el diario de integración de Project Operations se publica, falla a causa de las dimensiones que faltan para una cuenta que no está siendo publicada. |
| Gestión de proyectos y contabilidad | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La pestaña **Proyecto** no se puede editar en una factura de proveedor pendiente cuando la categoría de compras está asignada al artículo. |
| Gestión de proyectos y contabilidad | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta el panel de navegación si no ha iniciado sesión en Project Operations Dataverse. |
| Gestión de proyectos y contabilidad | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Cuando publica ingresos de una factura de proyecto en un caso de anticipo aplicado, se da un problema porque las transacciones del asiento no se equilibran. |
| Gestión de proyectos y contabilidad | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creación de un presupuesto después de registrar una propuesta de factura bloquea las líneas de corrección de la importación. |
| Gestión de proyectos y contabilidad | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | No debería ser posible la modificación de un registro de hitos totalmente facturado. |
| Viajes y gastos | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Todos los informes de gastos se pueden ver cuando busca una categoría en la aplicación móvil Expense. |
| Viajes y gastos | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Importes incorrectos de las transacciones de impuestos sobre ventas y con proveedores que se registran a partir de un gasto que se creó a partir de una transacción con tarjeta de crédito. |
| Viajes y gastos | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Aparece un mensaje de advertencia irrelevante cuando actualiza las páginas del **Informe de gastos**. |
| Viajes y gastos | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Se utiliza el aprobador interino incorrecto cuando se elimina un aprobador interino y luego se vuelve a enviar un informe de gastos a través del flujo de trabajo. |
| Viajes y gastos | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Se produce un error de publicación relacionado con la configuración del kilometraje. |
