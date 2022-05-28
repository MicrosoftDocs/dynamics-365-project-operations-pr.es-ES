---
title: 'Novedades en mayo de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de mayo de 2021 de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d0af6d99a24619b3613a3aaa027404556b1b81c4
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723789"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades en mayo de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

- Project Operations en la versión de entorno de Dynamics 365 Dataverse 4.10.0.186
- Gestión de proyectos y contabilidad en entornos de aplicaciones de finanzas y operaciones, versión 10.0.18

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- [Modos de programación](../project-management/scheduling-modes.md): los directores de proyecto pueden definir si un proyecto debe administrarse utilizando un modo de programación de duración fija, trabajo fijo o unidades fijas.
- [Configurar el kilometraje utilizando niveles de tarifas por kilometraje](../expense/set-up-mileage.md): cctualice los niveles de tarifa de kilometraje para los informes de gastos de los empleados.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

La siguiente lista muestra las asignaciones de doble escritura que se han modificado o agregado en la versión de mayo de 2021 de Project Operations.

| Asignación de entidad | Versión actualizada | Comentarios |
| --- | --- | --- |
| Origen de financiación del proyecto (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sincronización de las condiciones de pago del cliente del contrato del proyecto. |
| Propuesta de factura de proyecto V2 (facturas) | 1.0.0.3 | Sincronización de las condiciones de pago de la factura proforma. |
| Entidad de exportación de línea de facturas de proveedores de proyectos de integración de Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Actualizaciones de calidad |
| Proyectos V2 (msdyn\_projects) | 1.0.0.2 | Actualizaciones de calidad |

Siempre debe ejecutar la última versión de la asignación en su entorno y habilitar todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de aplicaciones de finanzas y operaciones. Es posible que algunas funciones y capacidades no funcionen correctamente si la última versión de la asignación no está activada. Puede ver la versión activa de la asignación en la columna **Versión** en la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado un mapa de asignación lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla faltantes en asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2227635 | Los valores en los campos **Unidad de venta** y **Unidad** predeterminados del producto en la cuadrícula **Estimaciones de materiales**. |
| Facturación y precios | 2234127 | El campo **Id. de tarea** ahora se integra correctamente en los datos reales del proyecto de Dataverse cuando se contabiliza una factura de proveedor. |
| Facturación y precios | 2235564 | Guardar la línea del diario garantiza que la divisa que se muestra en la entrada de la línea del diario coincida con la predeterminada en la línea después de guardar. |
| Facturación y precios | 2246671 | Hacer una transacción no imputable durante la facturación revierte el registro de ventas no facturadas original y crea un nuevo registro de ventas no facturadas como no imputable. |
| Facturación y precios | 2264042 | La corrección de factura válida no debe bloquearse si hay un detalle de corrección de factura que no es válido en el entorno. |
| Facturación y precios | 2146367 | La asignación de doble escritura del encabezado de la factura del proyecto se amplía para incluir las condiciones de pago. |
| Administración de oportunidades | 2086888 | No agregue roles ni categorías que estén desactivados antes de copiar un presupuesto a los roles y categorías imputables del presupuesto recién copiado. |
| Administración de oportunidades | 2234376 | Los campos de solo lectura están atenuados en la cuadrícula **Estimaciones de materiales**. |
| Administración de oportunidades | 2238337 | Se puede guardar una presupuesto basado en un contacto incluso si no está asociado con una lista de precios de proyecto. |
| Administración de oportunidades | 2239810 | Cerrar un presupuesto como perdido también cierra el proyecto asociado y cancela cualquier reserva. |
| Planificación y seguimiento de proyectos | 2099559 | Validaciones adicionales agregadas para el estado del sistema antes de que se abra la cuadrícula **Tareas del proyecto**. |
| Planificación y seguimiento de proyectos | 2178987 | Se corrigió un error transitorio producido al seleccionar **Fase siguiente** en la página **Proyecto**. |
| Administración de recursos | 2224817 | La funcionalidad para extender las reservas se establece de forma predeterminada en el estado de reserva correcto. |
| Entrada de tiempo | 2202476 | La página **Entrada de tiempo** ahora usa el control de cuadrícula de reacción y corrige problemas como la desalineación de la cuadrícula. |
| Entrada de tiempo | 2223377 | La entrada de tiempo se oculta en la sección **Relacionados** de la página **Recurso que se puede reservar** para evitar confusiones con la usabilidad. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administración y contabilidad de proyectos de Dynamics 365 Finance

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Gestión de proyectos y contabilidad | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | En Project Operations para escenarios basados en recursos, no puede convertir una oferta a cerrada por un error de integración. |
| Gestión de proyectos y contabilidad | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | En Project Operations: se produce un error cuando intenta asociar una línea de contrato a un identificador de proyecto debido a la verificación de líneas de contrato y tipos de transacción superpuestos. |
| Gestión de proyectos y contabilidad | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** establece la dirección de la factura del origen de financiación de un cliente diferente. |
| Viajes y gastos | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Puede producirse un error de registro relacionado con la configuración del kilometraje. |
| Viajes y gastos | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | La funcionalidad **Dividir a personal** no funciona para transacciones de gastos en moneda extranjera. |
| Viajes y gastos | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Los valores desplegables de categorías de gastos muestran categorías incorrectas para delegados independientemente de si son un recurso. |
| Viajes y gastos | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | No puede guardar un informe de gastos de empresas vinculadas debido a un error de **validación de recurso/categoría**. |
| Viajes y gastos | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | El cálculo incorrecto de la tarifa de kilometraje en el registro del informe de gastos tiene líneas divididas. |
| Viajes y gastos | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | No puede publicar un informe de gastos de empresas vinculadas cuando se incluye el impuesto sobre las ventas y el tipo de cuenta de compensación del método de pago es **Trabajador**. |
| Viajes y gastos | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | La reversión de la entidad de datos **TrvRequisitionLine** y el índice exclusivo están asociados. |
| Viajes y gastos | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | El informe de gastos admite la creación y actualización de líneas de documentos de origen. |
| Viajes y gastos | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Un diario de subcontabilidad erróneo aparece en un escenario de empresas vinculadas si el impuesto sobre las ventas se contabiliza en la entidad jurídica de destino. |
| Viajes y gastos | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | En Project Operations, la estimación de gastos no se elimina de Finance cuando se elimina de Dataverse. |
| Viajes y gastos | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Cuando la categoría de gastos no es una categoría de proyecto, las dimensiones financieras seleccionadas en la página **Gastos** no se copian en el informe de gastos. |
