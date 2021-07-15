---
title: 'Novedades de junio de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de junio de 2021 de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 28890238f9debb96786a31f66dd9a219f88a5338
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293158"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de junio de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

- Project Operations en la versión del entorno 4.11.0.156 o 4.11.0.164 de Dynamics 365 Dataverse.
- Gestión de proyectos y contabilidad en la versión de entornos de aplicaciones de Finance and Operations 10.0.19.

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- Capacidad de eliminar [Proyecto de líneas de propuesta de factura para escenarios de ajuste](../invoicing/correct-project-invoice-proposals.md).
- Las líneas de gastos detalladas reflejan los nombres de las subcategorías en el informe de gastos [Informes de gastos reinventados: nuevas funciones](../expense/expense-reports-reimagined.md#new-features).
- El método de pago está disponible en el panel de nuevos gastos al crear un nuevo gasto.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de escritura dual de Project Operations en esta versión. 

Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Siempre ejecute la última versión de la asignación en su entorno y habilitar todas las asignaciones de tabla relacionados a medida que actualiza la solución Dataverse de Project Operations y la versión de la solución de aplicaciones de Finance and Operations. Es posible que algunas funciones y capacidades no funcionen correctamente si la última versión de la asignación no está activada. Puede ver la versión activa de la asignación en la página **Escritura dual** en la columna **Versión**. Active una nueva versión de la asignación seleccionando **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado un mapa de asignación lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2281417 | Se solucionó el problema relacionado con el fallo de la acción de creación automática de facturas a través del programa de facturas. |
| Facturación y precios | 2287835 | Rendimiento mejorado de la confirmación de facturas. |
| Administración de oportunidades | 2222555 | La imputabilidad estimada del material debe copiarse correctamente en los detalles de la línea de oferta cuando se utiliza **Importar desde estimación del proyecto**. |
| Administración de oportunidades | 2223427 | Ahora se permiten personalizaciones para la acción **GenerateRetainersFromRetainerScheduleOptions**. |
| Administración de oportunidades | 2277528 | Cálculo de valor de hito de facturación fijo para líneas de contrato de proyecto con múltiples clientes. |
| Planificación y seguimiento de proyectos | 2226110 | Se solucionó el problema intermitente con la función **Generar requisito** en la cuadrícula **Equipo del proyecto**. |
| Planificación y seguimiento de proyectos | 2208109 | Los usuarios no pueden crear un proyecto que use una moneda con tareas relacionadas con otra moneda. |
| Planificación y seguimiento de proyectos | 2258228 | La lista de campos permitidos para modificar con entidades de **Programación** que utilizan la API de programación se han actualizado. |
| Planificación y seguimiento de proyectos | 2293989 | El idioma y la configuración regional correctos deben pasarse a la cuadrícula **Tareas de proyecto**. |
| Administración de recursos | 2220493 | Se ha corregido la experiencia del usuario en la cuadrícula **Tarea** al marcar rápidamente una solicitud de recurso como completa. |
| Administración de recursos | 2330496 | Se ha corregido el problema de carga del **Tablero de programación**. (La actualización de calidad está disponible en la versión 4.11.0.164) |
| Tiempo y gasto | 2194431 | La cuadrícula **Entrada de tiempo** debe respetar el comienzo de la semana según lo establecido en la **Configuración del sistema**. |
| Tiempo y gasto | 2277311 | Después de eliminar el valor en una celda en la cuadrícula **Entrada de tiempo**, el cursor permanece en la cuadrícula. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestión de proyectos y contabilidad en Dynamics 365 Finance

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Gestión de proyectos y contabilidad | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notas de formulario** y **Configuración de formulario** no se ven en **Configuración de gestión de proyectos** en las entidades jurídicas de Finance que se integran con Project Operations. |
| Gestión de proyectos y contabilidad | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | La descripción predeterminada del IVA está en blanco cuando **Tipo de registro** = **Impuesto sobre las ventas** para comprobantes de facturas de proyectos. |
| Gestión de proyectos y contabilidad | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Las transacciones dobles se registran cuando se utiliza la facturación basada en tareas en Dataverse con integración de Project Operations. |
| Gestión de proyectos y contabilidad | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | El porcentaje completado en el reconocimiento de ingresos es incorrecto al utilizar la integración de Project Operations. |
| Gestión de proyectos y contabilidad | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | La acumulación de ingresos se duplica en una factura de proveedor pendiente en un escenario integrado de Project Operations. |
| Gestión de proyectos y contabilidad | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | No se puede publicar el diario de integración cuando la regla del perfil de ingresos se establece en la configuración **Grupo**. |
| Gestión de proyectos y contabilidad | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | No se puede registrar una factura de compra para pedidos de compra de proyectos que tienen líneas con varias unidades de medida. |
| Gestión de proyectos y contabilidad | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | La dimensión financiera predeterminada de un proyecto no se puede actualizar mediante la entidad de datos **V2** del proyecto. |
| Gestión de proyectos y contabilidad | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | El proceso por lotes para crear estimaciones de proyectos tarda demasiado en completarse. |
| Gestión de proyectos y contabilidad | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | La eliminación de un contrato también elimina la dirección asociada con el cliente. |
| Viajes y gastos | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | La condición de flujo de trabajo de aprobación del informe de gastos no se evalúa correctamente. |
| Viajes y gastos | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | La directiva del informe de gastos no evalúa correctamente el id. del proyecto. |
| Viajes y gastos | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | La acción **Dividir en personal para transacciones de gastos de empresas vinculadas** no funciona correctamente. |
| Viajes y gastos | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Las justificaciones de línea del informe de gastos se eliminan accidentalmente cuando se eliminan determinadas solicitudes de viaje. Esto ocurre cuando el recID del informe de gastos y la solicitud de viaje son los mismos. |
| Viajes y gastos | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Hay un problema en la aplicación móvil Expense cuando el campo **Id. de proyecto** es obligatorio en las directivas de informes de gastos. |
| Viajes y gastos | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Los gastos de empresas vinculadas que están asociados con un proyecto no se pueden editar. En su lugar, se muestra el siguiente mensaje de error, "Referencia de objeto no establecida en una instancia de un objeto". |
| Viajes y gastos | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Después de que se publique el informe de gastos, la moneda y el importe incorrectos se enumeran en la contabilidad auxiliar del banco. |
| Viajes y gastos | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Se han realizado mejoras en la característica *Eliminar transacciones con tarjeta de crédito*.  |
| Viajes y gastos | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | El impuesto sobre las ventas incluido en un informe de gastos no se calcula de manera uniforme cuando se especifica una moneda de informe diferente en una entidad jurídica. |
| Viajes y gastos | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | El rendimiento se ve afectado al agregar un nuevo gasto de viaje en efectivo. |
| Viajes y gastos | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Las reglas de la directiva de gastos no se activan en un informe de gastos. |
| Viajes y gastos | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Al cargar una nueva categoría compartida mediante el Marco de administración de datos, se eliminan todas las subcategorías de todas las categorías compartidas. |
| Viajes y gastos | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Cuando crea una línea de gastos y luego selecciona una categoría, aparece el siguiente mensaje de error, "La combinación de DOM del grupo de impuestos sobre las ventas y del grupo de impuestos sobre las ventas de artículos STD no es válida". |
| Viajes y gastos | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Hay problemas de sincronización en la aplicación móvil Expense. |
