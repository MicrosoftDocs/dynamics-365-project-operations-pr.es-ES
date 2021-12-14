---
title: Novedades o cambios de septiembre de 2021 en Project Operations para escenarios basados en existencias/producción
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de septiembre de 2021 de la implementación de Project Operations para escenarios basados en existencias/producción.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815856"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novedades o cambios de septiembre de 2021 en Project Operations para escenarios basados en existencias/producción

_**Se aplica a:** Project Operations para escenarios basados en existencias/producción_

Este tema se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance versión 10.0.21
 
## <a name="quality-updates"></a>Actualizaciones de calidad

| Área de características | Número de referencia | Actualización de calidad |
|---|---|---|
| Gestión de proyectos y contabilidad | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Si el rol de administrador de compras tiene acceso a una entidad jurídica, también obtiene acceso a todos los proyectos en todas las entidades jurídicas. |
| Gestión de proyectos y contabilidad | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Se produce un problema de redondeo del impuesto al valor añadido (IVA) mientras se liquida una nota de crédito con una factura del proyecto original. |
| Gestión de proyectos y contabilidad | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Utilice un presupuesto de proyecto alternativo para la verificación del presupuesto. |
| Gestión de proyectos y contabilidad | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | El grupo de precios **Precio de venta por hora** no se calcula en la estructura de descomposición del trabajo para las cotizaciones del proyecto. |
| Gestión de proyectos y contabilidad | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Estimar la eliminación falla cuando está habilitada la función **Habilitar moneda del contrato del proyecto para el cálculo de la estimación**. |
| Gestión de proyectos y contabilidad | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | La factorización del impuesto sobre las ventas por cantidad se agrega al importe del precio de venta cuando el impuesto sobre el uso se utiliza en el grupo de impuestos sobre las ventas del diario de gastos del proyecto. |
| Gestión de proyectos y contabilidad | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | El impuesto no realizado no se calcula correctamente para el último pago cuando se aplicó la retención del proveedor y el prepago a facturas de pedido de compras. |
| Gestión de proyectos y contabilidad | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | El seguimiento de ajuste no funciona para los diarios de saldo inicial. |
| Gestión de proyectos y contabilidad | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Asignación de la revisión del presupuesto del proyecto por período** se divide en todos los períodos presupuestarios. Cuando se envía la asignación, el registro no se borra. |
| Gestión de proyectos y contabilidad | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Las contabilizaciones trabajo en curso (WIP) en contabilidad general tienen un importe incorrecto. |
| Gestión de proyectos y contabilidad | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | La aprobación del diario de horas del proyecto no funciona. |
| Gestión de proyectos y contabilidad | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | El precio de venta del ajuste del proyecto no se actualiza con los costos indirectos cuando el límite de financiación no está marcado. |
| Gestión de proyectos y contabilidad | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | No se puede crear un requisito de artículo cuando se factura el encabezado de la tabla de Sales y se finaliza la orden de compra de respaldo para las líneas existentes. |
| Gestión de proyectos y contabilidad | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | El monto de retención para una regla de facturación que tiene un hito para un proyecto diferente no se publica en el ID de proyecto correspondiente que se seleccionó para el hito. En cambio, se publica con el primer proyecto. |
| Gestión de proyectos y contabilidad | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Cuando selecciona **Conjunto de dimensiones financieras** en una propuesta de factura, se produce el siguiente error: "No se puede convertir el objeto de tipo 'Dynamics.AX.Application.FormIntControl' para escribir ' Dynamics.AX.Application.FormStringControl'. " |
| Gestión de proyectos y contabilidad | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | El informe de **Factura del proyecto** omite líneas. |
| Gestión de proyectos y contabilidad | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Se produce un error al calcular el control de costes de un proyecto de inversión. |
| Gestión de proyectos y contabilidad | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | El método **ProjTable::InitFromCustTable - canDeletePostalAddress** causa un problema de rendimiento. |
| Gestión de proyectos y contabilidad | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | El mensaje de error debería ser más claro que "Error inesperado". |
| Gestión de proyectos y contabilidad | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | El trabajo por lote de procesamiento de la factura del proyecto procesa y publica la propuesta de factura incluso si las líneas de la factura no se han generado. |
| Gestión de proyectos y contabilidad | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Se produce un problema de redondeo cuando la clave de configuración de la licencia del sector público está desactivada. Se genera un costo o precio de venta incorrecto en las horas de la hoja de tiempo para contratos que tienen múltiples fuentes de fundación. |
| Gestión de proyectos y contabilidad | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | El precio de venta del proyecto en un pedido de compra del proyecto facturada se calcula incorrectamente cuando el modelo de precio de venta es **Razón de contribución**. |
| Gestión de proyectos y contabilidad | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | El sistema no considera los días activos intermedios cuando calcula la tasa de mano de obra efectiva para un empleado. |
| Gestión de proyectos y contabilidad | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Se produce un error de contabilización en la hoja de horas de empresas vinculadas debido al siguiente error de validación: "No se ha configurado ningún socio comercial para la entidad jurídica". |
| Gestión de proyectos y contabilidad | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | La descripción de un pedido de compra que tiene una categoría de gastos no se recupera en la lista de transacciones del proyecto publicada. |
| Gestión de proyectos y contabilidad | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Hay una conversión incorrecta en los diarios de artículos que se publican en un proyecto. |
| Gestión de proyectos y contabilidad | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Puede confirmar una orden de compra incluso si se ha superado el límite de financiación. |
| Gestión de proyectos y contabilidad | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | La sección **Corrección / cancelación de factura** de una factura de servicios desaparece cuando se selecciona un identificador de proyecto. |
| Gestión de proyectos y contabilidad | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Hay problemas de rendimiento cuando se registra una propuesta de factura de proyecto desde un pedido de venta de proyecto que incluye un artículo en stock. |
| Gestión de proyectos y contabilidad | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Las facturas de compra del proyecto no se pueden registrar porque se produce el siguiente error: "La función AccDistProcessorProjectExtension.createForProjectRevenueLine se ha llamado incorrectamente". |
| Gestión de proyectos y contabilidad | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Actualice la creación de los trabajos por lotes de estimación del proyecto para respaldar la ejecución de múltiples subtareas. |
| Gestión de proyectos y contabilidad | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | El estado de una hoja de horas no se puede actualizar a **Borrador** cuando el flujo de trabajo se atasca en un estado **Cancelado**. |
| Gestión de proyectos y contabilidad | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Los importes retenidos no se calculan en la propuesta de factura de nota de crédito si existen varias líneas. |
| Gestión de proyectos y contabilidad | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Cuando intenta cambiar el monto en una factura generada a partir de una orden de compra, se produce el siguiente error: "Las transacciones en el comprobante no se equilibran según XX / XX / XXXX. (divisa de contabilidad: 0,00, divisa de informe: 0,01)." |
| Gestión de proyectos y contabilidad | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Existe un problema de rendimiento cuando una propuesta de factura de proyecto se publica en modo por lotes, debido a la combinación con **GeneralJournalAccountEntry**. |
| Gestión de proyectos y contabilidad | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Hay problemas de rendimiento cuando se publica una hoja de horas. |
| Gestión de proyectos y contabilidad | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | La jerarquía de estimaciones de costos de la estructura de descomposición del trabajo no está alineada correctamente después de expandir todas las tareas o después de expandir una sola tarea manualmente. |
| Gestión de proyectos y contabilidad | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | La plantilla de Excel de cotización del proyecto no se puede agregar al menú **Abrir en Excel**. |
| Gestión de proyectos y contabilidad | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | El número de exención de impuestos de una entidad legal no se incluye en una factura de proyecto impresa. |
| Gestión de proyectos y contabilidad | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | No se actualizan datos financieros en el error de la unidad de inventario cuando se ajusta un proyecto en relación con las líneas de crédito. |
| Gestión de proyectos y contabilidad | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Después de aplicar KB 461935, no puede publicar estimaciones si cambia a secuencias numéricas continuas. |
| Gestión de proyectos y contabilidad | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** hace que la aplicación móvil de la hoja de horas del proyecto para Android deje de responder. |
| Gestión de proyectos y contabilidad | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | El valor invertido de WIP del registro de facturas es diferente al valor de WIP registrado original de la entrada de tiempo. |
| Gestión de proyectos y contabilidad | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | En los casos de anticipo aplicados, las transacciones en un asiento no se equilibran correctamente cuando los ingresos facturados del proyecto se publican. |
| Gestión de proyectos y contabilidad | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Cuando la función **Mejora del rendimiento de la programación de recursos del proyecto** está habilitada, los valores decimales se redondean incorrectamente para la disponibilidad y la capacidad de los recursos. |
| Gestión de proyectos y contabilidad | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Cuando la función **Cree estimaciones de proyectos utilizando múltiples tareas por lotes** está habilitada, la creación de estimaciones en un lote que tiene varias subtareas funciona solo para el período actual. |
| Viajes y gastos | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Una directiva de solicitud de viaje se ignora y el flujo de trabajo se aprueba sin errores. |
| Viajes y gastos | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>La aplicación Mobile Expense no guarda la siguiente información en la línea de gastos:</p><ul><li>El identificador del proyecto</li><li>Si el gasto es facturable</li><li>El Número de actividad</li></ul> |
| Viajes y gastos | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | El campo **Recibos adjunto** está configurado en **Sí** incluso si la línea de gastos no tiene un recibo adjunto. |
| Viajes y gastos | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Aparece un error cuando cambia la categoría de gastos a **Personal**. |
| Viajes y gastos | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | No puede adjuntar un recibo y editar el gasto principal tras dividir una transacción de tarjeta de crédito a un gasto personal. |
| Viajes y gastos | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | La directiva de gastos para transacciones entre empresas vinculadas con un identificador de proyecto no funciona correctamente. |
| Viajes y gastos | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Falta la información de fecha de registro para los informes de gastos registrados. |
| Viajes y gastos | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Hay problemas con el método de pago en la aplicación móvil de gastos. |
| Viajes y gastos | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Una solicitud de viaje creada para un trabajador se puede usar para el informe de gastos de otro trabajador antes de la fecha de delegación. |
| Viajes y gastos | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Cuando crea un gasto, los cambios en los valores de la dimensión financiera no se actualizan correctamente en el nivel de distribución contable en el área de trabajo **Administración de gastos**. |
| Viajes y gastos | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | El estado de aprobación de la línea de gastos principal no se sincroniza con el estado de aprobación del flujo de trabajo de la línea detallada. |
| Viajes y gastos | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Se produce un error si publica un informe de gastos y la recuperación de impuestos está habilitada. |
| Viajes y gastos | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un delegado no puede eliminar documentos de gastos de un empleado despedido. |
| Viajes y gastos | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | La eliminación de una línea de gastos lleva más tiempo de lo esperado y afecta el rendimiento. |
| Viajes y gastos | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** produce un registro **TaxUncommitted** huérfano porque solo se elimina **SourceDocumentLine**. |
| Viajes y gastos | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** no honra **trvExpTrans.ReferenceDataAreaId** para crear la nueva secuencia numérica. |

## <a name="regulatory-updates"></a>Actualizaciones regulatorias

Para obtener información sobre actualizaciones normativas para aplicaciones de Finance and Operations, vea [Actualizaciones regulatorias](/dynamics365/finance/localizations/regulatory-updates). También puede iniciar sesión en Microsoft Dynamics Lifecycle Services (LCS) y usar la herramienta de búsqueda de problemas para ver las actualizaciones normativas planificadas. La búsqueda de problemas le permite buscar por país o región, tipo de función y lanzamiento.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
