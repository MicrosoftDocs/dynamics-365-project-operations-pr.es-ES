---
title: 'Novedades de marzo de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de marzo de 2022 de la implementación de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910927"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de marzo de 2022: Project Operations para escenarios basados en recursos/no mantenidos en existencias

*Se aplica a: Project Operations para escenarios basados en recursos/no mantenidos en existencias*

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.30.0.99
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.25

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

Las dietas ahora se admiten en el nuevo y renovado espacio de trabajo de gastos moderno. Las empresas que usan dietas pueden habilitar esta función para ofrecer a los usuarios una manera fácil de enviar y sus gastos de dietas y recibir un reembolso por ellos. Para obtener más información, consulte [Gastos por dietas](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

La siguiente lista muestra los mapas de doble escritura se modificaron o agregaron en la versión de marzo de 2022 de Project Operations.

| **Asignación de entidad** | **Versión actualizada** | **Comentarios** |
| --- | --- | --- |
| Entidad de exportación de línea de facturas de proveedores de proyectos de integración de Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Asignaciones actualizadas para alinearse con la entidad de línea de factura de proveedor en Dataverse. <br>No activar la versión de asignación 1.0.0.4. Estará lista para usarse en combinación con el entorno de finanzas, versión 10.0.26, en la próxima actualización mensual. |

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si no está activada la última versión del mapa. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado una asignación de tabla lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Tiempo y gastos | 2388011 | Mostrar comentarios de rechazo a los remitentes de entradas de tiempo durante la aprobación masiva. |
| Planificación y seguimiento del proyecto | 2495294 | Los detalles del proyecto no deben ser editables en la página **Detalles de la tarea**. |
| Facturación y precios | 2499605 | Los hitos de contrato que se crean a partir de hitos de cotización se marcan incorrectamente como de solo lectura. |
| Planificación y seguimiento del proyecto | 2506050 | El conjunto de operaciones permanece pendiente durante una hora si no hay ningún cambio que guardar. A continuación, el conjunto se marca falsamente como **Fallido**, mientras que debe completarse inmediatamente. |
| Facturación y precios | 2507401 | Las unidades de contratación predeterminadas se ingresan incorrectamente en los proyectos debido a un almacenamiento en caché incorrecto. |
| Facturación y precios | 2541660 | **Validación de creación de pedidos de venta** en doble escritura debe ser solo para pedidos basados en proyectos. |
| Facturación y precios | 2552745 | Los impuestos no se dividen entre los clientes que han configurado reglas de facturación dividida. |
| Facturación y precios | 2558859 | Mensajes de error mejorados cuando se configuran las dimensiones de precios. |
| Facturación y precios | 2558933 | **Importar desde estimaciones del proyecto** falla cuando **msdyn\_project** se agrega como una dimensión de precios. |
| Facturación y precios | 2559101 | La eliminación de parámetros del proyecto no está bloqueada y causa problemas. |
| Administración de oportunidades | 2570390 | El complemento de doble escritura obliga a que el tipo de cuenta en cotizaciones, pedidos y oportunidades sea **Cliente**, incluso cuando ese tipo de cuenta no sea correcto. |
| Facturación y precios | 2586097 | Los datos reales de costos facturados divididos no se revierten cuando se elimina un proyecto de una línea de contrato de proyecto. |
| Facturación y precios | 2589619 | El impuesto sobre el material fuera de catálogo se propaga a los datos reales de ventas no facturados y a la factura. |
| Administración de oportunidades | 2594015 | Un presupuesto no se puede cerrar como ganado para clientes que tienen términos de pago **Net60**. |
| Planificación y seguimiento del proyecto | 2595841 | En Project for the Web, los usuarios reciben un mensaje de error acerca de un **msdyn\_actualstart** que falta cuando crean una nueva solicitud de recursos. |
| Tiempo y gasto | 2602511 | El campo **Rechazado por** para las entradas de tiempo muestra **Sistema** en lugar de un usuario designado como rechazador. |
| Tiempo y gasto | 2602528 | Un aprobador de proyectos puede aprobar el tiempo en proyectos en los que no figura como aprobador. |
| Facturación y precios | 2608550 | Una factura de corrección se puede confirmar incluso si no hay cambios en el original. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Administración y contabilidad de proyectos de Dynamics 365 Finance

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Gestión de proyectos y contabilidad | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Hay una discrepancia entre Finance y Project Operations en la longitud permitida del campo **Id. de categoria**. |
| Gestión de proyectos y contabilidad | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Los proyectos de precio fijo no pueden eliminarse cuando el campo **Facturación en cuenta** se establece en **Ganancia y perdida** y se usa el principio de **Porcentaje completado**. |
| Gestión de proyectos y contabilidad | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Se ingresó un grupo de impuestos sobre las ventas predeterminado incorrecto desde la configuración del proyecto en las líneas de gastos en el diario de integración de Project Operations. |
| Gestión de proyectos y contabilidad | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | No puede editar las dimensiones del encabezado de la propuesta de factura del proyecto en una implementación integrada con Project Operations. |
| Gestión de proyectos y contabilidad | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Las facturas de proveedores de empresas vinculadas no deben integrarse con Dataverse. |
| Gestión de proyectos y contabilidad | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Hay una discrepancia en la moneda de los saldos de los clientes y la moneda del informe. |
| Gestión de proyectos y contabilidad | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Puede registrar una factura de proyecto incluso si el cliente está en retención para todas las facturas. |
| Gestión de proyectos y contabilidad | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | El botón **Eliminar todas las líneas** falta en las propuestas de factura de proyecto que tienen las vistas **Encabezamiento** y **Líneas**. |
| Gestión de proyectos y contabilidad | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Cuando registra una factura de proveedor, se produce el siguiente error: "La fecha contable de la factura debe estar en el mismo año contable que el pedido de compra relacionado. Ejecute el proceso de fin de año del pedido de compra o cambie la fecha al año contable actual". |
| Viajes y gastos | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | El costo comprometido de un proyecto no se libera después de liberado el costo comprometido de la solicitud de viaje. |
| Viajes y gastos | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | El siguiente error ocurre cuando envía un informe de gastos: "Stack Trace: la empresa no existe". |
| Viajes y gastos | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | El valor predeterminado **Id. de projecto ID** no se ingresa en los informes de gastos cuando se selecciona el parámetro **Requerir actividad para el diario** en el proyecto. |
| Viajes y gastos | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | El botón **Gastos de registro** no funciona correctamente en Project Operations para escenarios de recursos/no almacenados. |
| Viajes y gastos | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Hay un problema con **Tarifa por kilómetro** para un informe de gastos de kilometraje que incluye pasajeros. |
| Viajes y gastos | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Las tasas de gastos por kilometraje para los empleados no se suman correctamente cuando se utilizan dos tipos de vehículos diferentes en la categoría de gastos **Niveles de tarifa de kilometraje**. |
| Viajes y gastos | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | La búsqueda del campo **Proyecto** en una línea de solicitud de viaje no devuelve la lista correcta de proyectos. |
| Viajes y gastos | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometraje en revisión** muestra una advertencia en los informes de gastos. |
| Viajes y gastos | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | El servicio de reconocimiento óptico de caracteres (OCR) de recibos no funciona debido a un problema con la URL del servicio de OCR de gastos. |
| Viajes y gastos | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Cuando está habilitada la característica **Capacidad para detallar gastos periódicos rápidamente**, los importes de las líneas de desglose en los informes de gastos cambian los importes cada vez que se abre la página **Detalles**. |
| Viajes y gastos | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | No puede eliminar un informe de gastos cuando la lista provisional tiene más de un aprobador. |

## <a name="removed-and-deprecated-features"></a>Características quitadas y en desuso

El artículo [Funciones quitadas o en desuso en Project Operations](removed-depreciated-features-project.md) describe funciones que se eliminaron o dejaron en desuso para Dynamics 365 Project Operations.

- Una característica quitada ya no está disponible en el producto.
- Una función en desuso no está en desarrollo activo y se podría quitar en una actualización futura.

Antes de eliminar una característica del producto, aparecerá un aviso de desuso en el artículo [Características quitadas o en desuso en Project Operations](removed-depreciated-features-project.md), 12 meses antes de su eliminación.

Para los cambios importantes que solo afectan al tiempo de compilación y tienen códigos binarios compatibles con entornos de espacio aislado y de producción, el tiempo de puesta en desuso será inferior a 12 meses. Por lo general, estos cambios son actualizaciones funcionales que deben hacerse en el compilador.
