---
title: 'Novedades de febrero de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de febrero de 2022 de la implementación de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933007"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de febrero de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

*Se aplica a: Project Operations para escenarios basados en recursos/no mantenidos en existencias*

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.28.0.120
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.24

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

- A partir de esta versión, puede agregar hasta 300 miembros del equipo a un solo proyecto. Anteriormente, el límite en el número de miembros del equipo era de 150. Para obtener más información, consulte [Límites de proyecto](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Actualizaciones de mapas de doble escritura de Project Operations

La siguiente lista muestra los mapas de doble escritura se modificaron o agregaron en la versión de febrero de 2022 de Project Operations.

| Asignación de entidad | Versión actualizada | Comments |
| --- | --- | --- |
| Entidad de exportación de gastos de proyecto de integración de Project Operations (msdyn\_expenses) | 1.0.0.3 | Extendido para la sincronización de la actividad del proyecto a Dataverse. |

Para obtener la lista actual y las versiones de los mapas de doble escritura de Project Operations, consulte [Versiones de mapas de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2415109 | El valor predeterminado del campo **Condiciones de pago de operaciones** debe ser el registro del cliente del contrato del proyecto y el registro de la factura proforma. |
| Facturación y precios | 2497369 | La corrección material debe seguir el valor de la fecha de los parámetros **Corrección**. |
| Facturación y precios | 2498697 | Se mejoró la configuración de seguridad para **Recuperación de entrada de tiempo**. |
| Facturación y precios | 2513824 | Para escenarios basados en recursos, el id. de categoría de transacción no debe exceder los 28 caracteres en Project Operations. |
| Facturación y precios | 2517455 | No se debe permitir que la acción **Actualizar transacciones de línea de factura** se desencadene varias veces simultáneamente para la misma factura. |
| Facturación y precios | 2517465 | La acción **Desactivar detalles de línea de factura** está bloqueada porque no es compatible. |
| Facturación y precios | 2556660 | Se corrigió la comprobación de efectividad que se realiza en la lista de precios que se adjunta a un registro de parámetros del proyecto. |
| Administración de oportunidades | 2369202 | Se corrigió la lógica comercial que verifica que las listas de precios que tienen fechas de vigencia superpuestas se pueden adjuntar al mismo contrato de proyecto. |
| Administración de oportunidades | 2385965 | Se corrigió el comportamiento en la pestaña **Clientes** de la página **Contrato de proyecto** cuando seleccione **Guardar y cerrar**. |
| Tiempo y gastos | 2538503 | Una tarea de proyecto debe estar disponible en la entidad **Datos reales del proyecto** después de registrar un informe de gastos. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Administración y contabilidad de proyectos de Dynamics 365 Finance

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Gestión de proyectos y contabilidad | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Durante la importación de notas de crédito de proveedor, se produce un error. El mensaje de error dice: "El importe retenido no puede ser mayor que el importe neto restante". |
| Gestión de proyectos y contabilidad | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Si una propuesta de factura incluye transacciones de tarifa cero que son datos reales de ventas no facturados, no se puede realizar la facturación. |
| Gestión de proyectos y contabilidad | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | El costo publicado no es correcto después de actualizar el precio de compra y el parámetro **Activar la gestión de cambios**.|
| Gestión de proyectos y contabilidad | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | El presupuesto de registro de un proyecto de precio fijo utiliza la moneda y el importe incorrectos en el asiento de estimación, incluso cuando la característica **Habilitar la moneda del contrato del proyecto para el cálculo de la estimación** está habilitada. |
| Gestión de proyectos y contabilidad | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** no debe realizar una llamada para habilitar el seguimiento de cambios sin detectar excepciones para las entidades que tienen claves de configuración que no están habilitadas. |
| Gestión de proyectos y contabilidad | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | El trabajo por lotes se corrige cuando se registran varios diarios avanzados y se produce un error. |
| Viajes y gastos | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Debido a un problema de liquidación relacionado con adelantos en efectivo en los informes de gastos, el importe del impuesto no se cubre como parte del adelanto en efectivo. |
| Viajes y gastos | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | La información del impuesto no está incluida en el informe **Gastos: transacciones registradas**. |
| Viajes y gastos | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | La infracción de la política de gastos **Recibos requeridos** muestra incorrectamente una advertencia en los informes de gastos. |
| Viajes y gastos | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Una transacción de proyecto no incluye el impuesto no recuperable en el importe total de las ventas cuando la transacción es el resultado de un gasto de kilometraje. |
| Viajes y gastos | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Cuando una línea detallada tiene impuestos, no puede cambiar la fecha de la línea detallada y se produce un error de estado del documento de origen. |

## <a name="removed-and-deprecated-features"></a>Características quitadas y en desuso

El artículo [Funciones quitadas o en desuso en Project Operations](removed-depreciated-features-project.md) describe funciones que se eliminaron o dejaron en desuso para Dynamics 365 Project Operations.

- Una característica quitada ya no está disponible en el producto.
- Una función en desuso no está en desarrollo activo y se podría quitar en una actualización futura.

Antes de eliminar una característica del producto, aparecerá un aviso de desuso en el artículo [Características quitadas o en desuso en Project Operations](removed-depreciated-features-project.md), 12 meses antes de su eliminación.

Para los cambios importantes que solo afectan al tiempo de compilación y tienen códigos binarios compatibles con entornos de espacio aislado y de producción, el tiempo de puesta en desuso será inferior a 12 meses. Por lo general, estos cambios son actualizaciones funcionales que deben hacerse en el compilador.
