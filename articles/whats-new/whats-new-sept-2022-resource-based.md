---
title: 'Novedades de septiembre de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de septiembre de 2022 de Microsoft Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634827"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de septiembre de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.46.0.60
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.29

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

| Área de características | Nombre de característica | Más información |
| --- | --- | --- |
| Administración de oportunidades | **Revisión y activación de ofertas**<br>Project Operations brinda el soporte completo del proceso de ventas. Las cotizaciones de proyectos se pueden activar para representar un estado en el que la cotización es de solo lectura y se está revisando. Las cotizaciones activadas se pueden revisar para crear nuevas cotizaciones que tengan un número de revisión incrementado. Las cotizaciones de proyectos activadas o las revisiones de cotizaciones se pueden cerrar como ganadas o perdidas. | [Activar y revisar una oferta de proyecto](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturación y precios | **Incumplimiento de precio agnóstico de zona horaria**<br>Project Operations ha introducido el concepto de una fecha agnóstica de zona horaria en todos los datos reales del proyecto. Un campo nuevo, **Fecha de transacción**, ahora está disponible en líneas de diario y datos reales, y se usará para almacenar la fecha en que ocurrió la transacción, pero sin convertir esa fecha a la hora universal coordinada. Esta fecha se utilizará para procesos posteriores, como el incumplimiento de precios y la creación de facturas. | <p>[Determinar tasas de costes para estimaciones y datos reales que se basan en proyectos](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determinar precios de venta para estimaciones y datos reales de proyectos](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturación y precios | **Sustituciones de precios con fecha de vigencia en Project Operations**<br>Reemplazos de precios de la fecha de vigencia proporciona una forma de anular o cambiar precios específicos en la lista de precios. | [Reemplazos de precios de la fecha de vigencia](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontratación | **Subcontratación y reconciliación de facturas de proveedores**<br>Esta función permite a los clientes crear subcontratos para comprar tiempo de recursos, categorías de gastos y materiales que se utilizan para el trabajo del proyecto. También permite a los clientes registrar, en aplicaciones de finanzas y operaciones, facturas de proveedores que estarán disponibles para los gerentes de proyectos en Dataverse para verificar. | <p>[Administración de subcontrataciones](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Crear facturas de proveedor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tiempo y gasto | **Aprobador global**<br>Esta función permite la aprobación centralizada de proveedores de software independientes (ISV), independientemente del estado del proyecto o del miembro del equipo en el proyecto. | [Seguridad y aprobaciones](/dynamics365/project-operations/approvals/approvals-security) |
| Gestión de gastos | **Capacidad para contabilizar el pasivo de gastos en la moneda del proveedor**<br>Esta función permite que los informes de gastos se registren en una moneda del proveedor para el método de pago en efectivo. | [Capacidad para contabilizar el pasivo de gastos en la moneda del proveedor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Adquisición de proceso | **Pagos de proveedores de pago cuando se pagan**<br>Esta función permite que la función Pagar cuando se pague (PWP) se use con entornos sin existencias de Project Operations. Permite bloquear/retener los pagos del proveedor, según los términos de retención, hasta que se reciba el pago del cliente. | [Pagos de proveedores de pago cuando se pagan](/dynamics365/project-operations/procurement/pay-when-paid) |
| Adquisición de proceso | **Solicitudes de compra de proyecto**<br>Esta función permite a los usuarios crear pedidos de compra relacionados con proyectos en entidades jurídicas donde está habilitada la integración de Project Operations on Dynamics 365 Customer Engagement. Las órdenes de compra del proyecto se pueden usar para registrar la adquisición de material no almacenado en el proyecto por persona del departamento de Adquisiciones. Los pedidos de compra del proyecto no se sincronizarán con Dataverse. Sin embargo, puede utilizar una entidad virtual para mostrar las líneas de pedido de compra del proyecto en Dataverse para obtener información sobre el administrador del proyecto. El costo de la factura del proveedor relacionado con el proyecto se integra con la entidad Datos reales del proyecto en Dataverse. El coste del proyecto se registra en la subcontabilidad del proyecto usando el diario de integración de Project Operations. | |
|Planificación y seguimiento de proyectos|**Usar las API de programación de proyectos para realizar operaciones con entidades de programación** </br> </br>La API de edición de contorno de asignación de recursos permite a los desarrolladores especificar mediante programación el esfuerzo de un asignado a la tarea en cualquier intervalo de fechas compatible para una planificación de esfuerzo por fases más granular.|[Usar las API de programación de proyectos para realizar operaciones con entidades de programación](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

La siguiente tabla muestra los mapas de escritura dual que se modificaron o agregaron en la versión de septiembre de 2022 de Project Operations.

| Asignación de entidad | Versión actualizada | Comments |
| -------------- | ------------------- | ------------|
| Datos reales de integración de Project Operations (msdyn_actuals) | 1.0.0.15 | Este mapa admite el procesamiento de datos reales de subcontratos con Project Operations para escenarios basados en recursos. |
| Entidad de exportación de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Este mapa admite el procesamiento de datos reales de subcontratos con Project Operations para escenarios basados en recursos. |
| Entidad de exportación de línea de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Este mapa admite el procesamiento de datos reales de subcontratos con Project Operations para escenarios basados en recursos. |

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2754422 | Las estimaciones de gastos y materiales no fluyen a Finance cuando los proyectos se copian en Dataverse. |
| Tiempo y gasto | 2787409 | Un aprobador no válido puede aprobar una entrada de tiempo que no sea de proyecto. |
| Administración de oportunidades | 2788907 | Mensaje de error actualizado sobre la validación de exclusividad para líneas de pedido que incluyen marcas. |
| Tiempo y gasto | 2842253 | Manejo de excepciones nulas para aprobación de tiempo. |
| Facturación y precios | 2844181 | Si no se obtiene el ID de correlación, se bloquea la creación de facturas. |
| Facturación y precios | 2876628 | QLD, CLD: la resolución estimada de la lista de precios debe usar campos de rango de fechas heredados de la lista de precios. |
| Subcontratación | 2893222 | Si no se especifica un rol para una línea de subcontrato, debería ser posible seleccionar esa línea en un miembro del equipo para cualquier rol. |

### <a name="project-management-and-accounting-in-finance"></a>Administración de proyectos y contabilidad en Finance

Para obtener información sobre las correcciones de errores incluidas en esta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services y consulte el [artículo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Características desactivadas de manera determinada en próxima versión

La tabla siguiente enumera las características que se han activado de forma predeterminada en la versión 10.0.30. La mayoría de las características que se han activado de forma automática se pueden desactivar en [Administración de características](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). En el futuro, es posible que algunas características que se han activado automáticamente se eliminen de la Administración de características y se vuelvan obligatorias. Este cambio garantiza que los clientes utilicen la funcionalidad actual, de modo que las mejoras puedan basarse en la funcionalidad actual a medida que se agregan. Las características nunca se habilitarán automáticamente en menos de un año, a menos que se determine que son esenciales.

| Nombre de característica | Habilitar fecha | Fecha de adición de característica | Estado de la característica | Módulo |
| --- | --- | --- |--- |--- |
| Habilite la operación asíncrona cuando el usuario necesite cambiar entre operaciones sincronizadas y asíncronas | 21 de octubre de 2022 | 9 de abril de 2021 | Activada de forma predeterminada | Gestión de gastos |
| Se requiere evaluación de política de gastos para recibos | 21 de octubre de 2022 | 20 de diciembre de 2021 | Activada de forma predeterminada | Gestión de gastos |
| Vista de lista de informes de gastos creados por trabajadores delegados | 21 de octubre de 2022 | 19 de febrero de 2020 | Activada de forma predeterminada | Gestión de gastos |
| Cálculo del total de millas por año fiscal | 21 de octubre de 2022 | 10 de mayo de 2022 | Activada de forma predeterminada | Gestión de gastos |
