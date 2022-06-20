---
title: Novedades o cambios de octubre de 2021 en Project Operations para escenarios basados en existencias/producción
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de octubre de 2021 de la implementación de Project Operations para escenarios basados en existencias/producción.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933697"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novedades o cambios de octubre de 2021 en Project Operations para escenarios basados en existencias/producción

_**Se aplica a:** Project Operations para escenarios basados en existencias/producción_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.22
 
## <a name="quality-updates"></a>Actualizaciones de calidad

| Área de características | Número de referencia | Actualización de calidad |
|--------------|------------------|----------------|
| Gestión de proyectos y contabilidad | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | El trabajo del proyecto en proceso (WIP) y los importes de ingresos acumulados no se revierten correctamente cuando se registra una factura de cliente de empresas vinculadas. |
| Gestión de proyectos y contabilidad | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | La función **Evitar el cierre del proyecto si existen transacciones abiertas** no funciona. |
| Gestión de proyectos y contabilidad | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | La clasificación de facturación en una factura de servicios no completa automáticamente las dimensiones de los proyectos cuando esa funcionalidad está habilitada. |
| Gestión de proyectos y contabilidad | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | En escenarios no de empresas vinculadas, WIP y los importes de ingresos acumulados no se revierten correctamente cuando se registra la factura del proyecto. |
| Gestión de proyectos y contabilidad | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Los valores de débito y crédito se cambian cuando el complemento de Microsoft Excel se utiliza con el diario de gastos del proyecto y el campo **Tipo de cuenta de compensación** está configurado en **Proyecto**. |
| Gestión de proyectos y contabilidad | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | El monto que se contabiliza en las transacciones del proyecto está sobrevalorado en una orden de compra del proyecto que incluye artículos en stock y que tiene montos de impuestos no deducibles cuando **UseTax** está marcado. |
| Gestión de proyectos y contabilidad | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | El sistema divide la cantidad entre los informes de pérdidas y ganancias del proyecto y los informes WIP del proyecto. |
| Gestión de proyectos y contabilidad | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | El inventario disponible es incorrecto después de que se ajusta un requisito de artículo parcialmente devuelto. |
| Gestión de proyectos y contabilidad | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Los nombres de los recursos se duplican en Project Operations cuando se editan en Microsoft Project. |
| Gestión de proyectos y contabilidad | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Los informes de gastos de empresas vinculadas que tienen cuentas por pagar costos de facturas de proveedor pendientes de empresas vinculadas se registran primero en el tipo de publicación **Costo del proyecto WIP**. Sin embargo, durante el procesamiento, los costos relacionados con la estimación se contabilizan en el tipo de publicación **Costo del proyecto** en lugar del tipo de publicación esperado **Costo de empresas vinculadas**. |
| Gestión de proyectos y contabilidad | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | No se muestran los resultados de retención de proveedores en las transacciones de gastos del proyecto. |
| Gestión de proyectos y contabilidad | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | La hoja de tiempo debe redondear el monto de la transacción en la moneda de la transacción a un número específico de decimales en todas las distribuciones contables y asientos de asignación de diario general. |
| Gestión de proyectos y contabilidad | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Las cantidades de necesidades de artículos del proyecto se actualizan automáticamente cuando se firman las órdenes previsionales. |
| Gestión de proyectos y contabilidad | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | El número de comprobante, el saldo del proveedor del tipo de transacción y el número de cuenta no se pueden revertir en la factura de prepago de una orden de compra. |
| Gestión de proyectos y contabilidad | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La factura del proveedor de empresas vinculadas se rompe cuando se activa la integración de la factura del proveedor. |
| Gestión de proyectos y contabilidad | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Cuando crea un diario de gastos del proyecto, el monto del costo se muestra en el campo **Crédito**. |
| Gestión de proyectos y contabilidad | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Las condiciones de pago de las facturas del proyecto no funcionan como se esperaba. |
| Gestión de proyectos y contabilidad | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Los comprobantes de la hoja de horas trabajadas se pueden reutilizar cuando la secuencia numérica está configurada como continua. |
| Gestión de proyectos y contabilidad | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIA: la lógica **Cantidad de retención manual** no coincide con la lógica **Cantidad de retención automática** en la propuesta de factura de contrato de proyecto. |
| Gestión de proyectos y contabilidad | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Cuando se libera la retención del proveedor, la contabilización del comprobante tiene líneas adicionales incorrectas. |
| Gestión de proyectos y contabilidad | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Cuando el campo **Fecha de la factura** en la página **Crear propuesta de factura** se cambia, puede ocurrir el siguiente error: "Referencia de objeto no establecida en una instancia de un objeto". |
| Gestión de proyectos y contabilidad | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Se produce un error cuando intenta aprobar una hoja de horas desde el flujo de trabajo **TSLine** y hay una política de parte de horas para los sábados y domingos. |
| Gestión de proyectos y contabilidad | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | El tipo de elemento de proyecto de saldo inicial se excluye de **Resúmenes de transacciones de propuestas de facturas** cuando se calcula el total de la factura de la propuesta de factura. |
| Gestión de proyectos y contabilidad | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Si el costo de consumo en una orden de producción del proyecto es 0 (cero), se produce el siguiente error cuando intenta estimar: "Intentó dividir por cero". |
| Gestión de proyectos y contabilidad | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | La aplicación Project Timesheet Mobile para Android deja de responder. El problema está relacionado con **TimeEntryDataManager ArgumentNullException**. |
| Gestión de proyectos y contabilidad | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | El diario de integración de Project Operations falla cuando lo publica, porque a una cuenta le faltan dimensiones. Sin embargo, la cuenta a la que le faltan las dimensiones no es la cuenta en la que está publicando. |
| Gestión de proyectos y contabilidad | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | El filtro **ToDate** en las búsquedas no se borra cuando se quita del cuadro de diálogo **Seleccione** la página **Costo de publicación**. |
| Gestión de proyectos y contabilidad | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Restablecer toda la distribución** falla y muestra un error para las hojas de tiempo que se crean para un proyecto del tipo **Solo tiempo**. |
| Gestión de proyectos y contabilidad | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La pestaña **Proyecto** no se puede editar en una factura de proveedor pendiente cuando la categoría de compras está asignada al artículo. |
| Gestión de proyectos y contabilidad | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta el panel de navegación si no ha iniciado sesión en Project Operations Dataverse. |
| Gestión de proyectos y contabilidad | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Para las transacciones de ajuste de proyectos de empresas vinculadas, existen problemas en la empresa de destino. |
| Gestión de proyectos y contabilidad | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Los costos comprometidos para un proyecto calculan la cantidad y el precio de costo incorrectos si la orden de compra fue procesada por **Proceso de fin de año de la orden de compra** en el libro mayor. |
| Gestión de proyectos y contabilidad | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Cuando un pedido de producción de proyecto que tiene pedidos de calidad se informa como terminado, se produce el siguiente error: "No hay transacción virtual marcada con transacción de inventario". |
| Gestión de proyectos y contabilidad | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Cuando se registra una factura de Cuentas por pagar relacionada con el proyecto, se produce el siguiente error: "Proyecto de texto enumerado - costo - artículo no existe". |
| Gestión de proyectos y contabilidad | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Los costos indirectos se duplican cuando acumula ingresos manualmente. |
| Gestión de proyectos y contabilidad | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Acumule ingresos y la publicación WIP no produce transacciones. |
| Gestión de proyectos y contabilidad | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | La activación del precio pendiente falla para un artículo de coste estándar cuando existe una orden de compra de proyecto recibida. |
| Gestión de proyectos y contabilidad | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | El valor invertido de WIP del registro de facturas es diferente al valor de WIP registrado original de una entrada de tiempo. |
| Gestión de proyectos y contabilidad | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Hay un problema de publicación para el ingreso facturado del proyecto en casos de anticipos aplicados cuando las transacciones de un asiento no se equilibran. |
| Gestión de proyectos y contabilidad | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creación de un presupuesto después de que se contabiliza una propuesta de factura bloquea la importación de líneas de corrección en Project Operations. |
| Gestión de proyectos y contabilidad | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | No debería ser posible la modificación de un registro de hitos totalmente facturado. |
| Gestión de proyectos y contabilidad | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Cuando se utilizan cargos automáticos, la factura del cliente de empresas vinculadas para una hoja de horas no se puede registrar y se muestra un mensaje de error. |
| Gestión de proyectos y contabilidad | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | La dirección de un subproyecto no se actualizó correctamente. |
| Gestión de proyectos y contabilidad | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | El precio de costo de los requisitos del artículo se actualiza con el precio de compra de las órdenes de compra consolidadas. |
| Gestión de proyectos y contabilidad | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | El costo publicado no es correcto después de que se actualiza el precio de compra y el parámetro **Activar la gestión de cambios** está habilitado. |
| Viajes y gastos | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Todos los gastos del usuario se pueden ver cuando busca una categoría en la aplicación móvil Expense. |
| Viajes y gastos | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Importes incorrectos de las transacciones de impuestos sobre ventas y con proveedores que se registran a partir de un gasto que se creó a partir de una transacción con tarjeta de crédito. |
| Viajes y gastos | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Se muestra un mensaje de advertencia irrelevante cuando actualiza las páginas del informe de gastos. |
| Viajes y gastos | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Se utiliza el aprobador interino incorrecto cuando se elimina un aprobador interino y luego se vuelve a enviar a través del flujo de trabajo. |
| Viajes y gastos | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Se produce un error de publicación relacionado con la configuración del kilometraje. |
| Viajes y gastos | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | La distribución no actualiza la entidad jurídica cuando se vuelve a agregar una transacción no adjunta al informe de gastos de un gasto de empresas vinculadas. |

### <a name="regulatory-updates"></a>Actualizaciones regulatorias

Para obtener información sobre actualizaciones normativas para aplicaciones de finanzas y operaciones, consulte [Actualizaciones normativas](/dynamics365/finance/localizations/regulatory-updates). También puede iniciar sesión en Microsoft Dynamics Lifecycle Services (LCS) y usar la herramienta de búsqueda de problemas para ver las actualizaciones normativas planificadas. La búsqueda de problemas le permite buscar por país o región, tipo de función y lanzamiento.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
