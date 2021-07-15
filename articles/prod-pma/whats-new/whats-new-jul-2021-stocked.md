---
title: Novedades y cambios en Project Operations de julio de 2021 para escenarios basados en existencias/producción
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de julio de 2021 de Project Operations para escenarios basados en existencias/producción.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: fb1814330b5e474ccbda0ab85dd67758a6f270a9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334606"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Novedades y cambios en Project Operations de julio de 2021 para escenarios basados en existencias/producción

_**Se aplica a:** Project Operations para escenarios basados en existencias/producción_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

- Gestión de proyectos y contabilidad en el entorno de Dynamics 365 Finance versión 10.0.20
 
### <a name="quality-updates"></a>Actualizaciones de calidad
                                                                                                                                                                                  
| Área de características                      | Número de referencia| Actualización de calidad                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestión de proyectos y contabilidad | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Los registros de compromiso de costes de una solicitud de compra se borran en cuanto el pedido de compra se libera de la incidencia de la solicitud de compra.                                                                           |
| Gestión de proyectos y contabilidad | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | La validación del presupuesto ocurre dos veces en una solicitud de compra. Esta duplicación significa que la solicitud no se puede cerrar y no se crea el pedido de compra correspondiente.                                                                                                                        |
| Gestión de proyectos y contabilidad | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | La regla de facturación **Porcentaje sobre el que facturar** no se ha podido completar por una incidencia de redondeo.                                                                              |
| Gestión de proyectos y contabilidad | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Cuando ajusta la transacción y el porcentaje tiene decimales, el coste y el precio de venta no se ajustan correctamente.                                      |
| Gestión de proyectos y contabilidad | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | El explorador de origen de contabilidad muestra las horas para una sola línea de la hoja de horas para varias líneas de la hoja de horas con diferentes actividades.                                      |
| Gestión de proyectos y contabilidad | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Las vistas guardadas y la personalización de los detalles de la línea de la hoja de horas hacen que el sistema siempre abra los detalles de la primera hoja de horas de la lista al intentar abrir una hoja de horas.  |
| Gestión de proyectos y contabilidad | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | El nodo raíz del proyecto desaparece y los registros de estructura de descomposición de trabajo se eliminan después de la importación.                                                                                             |
| Gestión de proyectos y contabilidad | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Cuando los artículos se reciben y emiten parcialmente a partir de la necesidad de artículos, el sistema actualiza el saldo de consumo de presupuesto incorrecto. |
| Gestión de proyectos y contabilidad | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Los pedidos de compra de retención del proyecto no muestran los totales correctamente en el panel **Totales** o en la cuadrícula **Factura pendiente**.                                                                  |
| Gestión de proyectos y contabilidad | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Al cerrar el inventario, los ajustes de coste de los artículos del proyecto se registran en la cuenta de saldo en lugar de la cuenta de pérdidas y ganancias.                                                            |
| Gestión de proyectos y contabilidad | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Un comprobante de transacción registrado en el proyecto y un comprobante de estimación utilizan USD como divisa de contabilidad, pero la cantidad muestra cuál sería el equivalente en CAD.              |
| Gestión de proyectos y contabilidad | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Los costes comprometidos con un requisito de artículo y un pedido de compra son incorrectos en el proceso de facturación del pedido de compra con la recepción del producto parcial y la facturación parcial.       |
| Gestión de proyectos y contabilidad | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | El ajuste del proyecto no actualiza correctamente el importe de las ventas con costes indirectos.                                                                                    |
| Gestión de proyectos y contabilidad | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | A la tabla **Hoja de horas** le falta una relación definida con la vista **Trabajador/Recurso**.                                                                                   |
| Gestión de proyectos y contabilidad | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | No se puede rellenar el campo **Número de actividad** cuando lo seleccione en el menú desplegable de una hoja de horas de empresas vinculadas.                                                                 |
| Gestión de proyectos y contabilidad | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | No puede agregar un campo personalizado **Finalidad** o **Descripción de la actividad** a las siguientes páginas: **Transacción registrada del proyecto**, **Creación de propuesta de factura** o **Propuesta de factura**.  |
| Gestión de proyectos y contabilidad | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Se proporciona un control de fecha de entrega incorrecto cuando crea requisitos de artículo mediante la administración de datos (**ProjSalesItemRequirementEntity**).                                              |
| Gestión de proyectos y contabilidad | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Cuando selecciona un Id. de contrato de proyecto en Finance, el entorno integrado de Project Operations abre la página para crear un nuevo registro en lugar de abrir el contrato de proyecto existente.                                                                                                                 |
| Gestión de proyectos y contabilidad | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  La etiqueta "@SYS4083080" ("No se puede encontrar un registro de trabajador único que corresponda a los valores introducidos") no se ha traducido al danés.                                |
| Gestión de proyectos y contabilidad | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | El campo **Grupo de impuestos de artículos** no se puede editar en una propuesta de factura.                                                                               |
| Gestión de proyectos y contabilidad | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | El coste comprometido está sobrevalorado con importes de impuestos no deducibles.                                                                                                    |
| Gestión de proyectos y contabilidad | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | La publicación de una hoja de horas de empresas vinculadas con varios proyectos y diferentes dimensiones financieras genera valores inesperados en la contabilidad general.                             |
| Gestión de proyectos y contabilidad | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Las líneas de propuesta de factura se duplican debido a múltiples instancias del proceso periódico **Importar desde almacenamiento provisional** que se ejecutan al mismo tiempo.                                      |
| Gestión de proyectos y contabilidad | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Hay un error en la publicación de la propuesta de factura de nota de crédito, por lo que las transacciones en el comprobante no se equilibran.    |
| Gestión de proyectos y contabilidad | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Los costes comprometidos del proyecto se vuelven incorrectos después de que se liberen las facturas pendientes en espera.                                                                             |
| Gestión de proyectos y contabilidad | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | No puede crear una nota de crédito para un pedido de venta de proyecto cuando el impuesto está en una moneda diferente a la moneda de la empresa.                                      |
| Gestión de proyectos y contabilidad | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | La eliminación de un contrato también elimina la dirección asociada con el cliente.                                                                                     |
| Gestión de proyectos y contabilidad | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | No se puede publicar una propuesta de factura que sea resultado de una corrección de transacción de tiempo negativa.                                                                    |
| Viajes y gastos                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Los impuestos se calculan de manera diferente en los informes de gastos.                                                                                                                  |
| Viajes y gastos                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | La actualización de la versión **DB72_Expense.updateTrvExpTransProjTransId()** no permite que **trvExpTrans.ReferenceDataAreaId** cree la nueva secuencia numérica.                    |
| Viajes y gastos                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | El importe presentado no se muestra con el campo obligatorio.                                                                                                             |
| Viajes y gastos                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Mejoras en el rendimiento a la hora de adjuntar un gasto al informe de gastos mediante la interfaz de usuario de gastos rediseñados.                                                            |
| Viajes y gastos                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Puede eliminar los informes de gastos registrados.                                                                                           |
| Viajes y gastos                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | El mensaje de política de gastos se muestra varias veces.                                                                                                       |
| Viajes y gastos                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | El campo **Método de pago** está incluido en el panel **Gasto nuevo**.                                                                                                      |
| Viajes y gastos                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | La herramienta **Restablecer el estado del documento de gastos** debería restablecer el estado del informe de gastos a **Borrador** si no se encontró el flujo de trabajo. 

### <a name="regulatory-updates"></a>Actualizaciones regulatorias
Para obtener información sobre actualizaciones normativas para aplicaciones de Finance and Operations, vea [Actualizaciones regulatorias](/dynamics365/finance/localizations/regulatory-updates). También puede iniciar sesión en Lifecycle Services (LCS) y ver las actualizaciones normativas planificadas mediante la herramienta de búsqueda de problemas. La búsqueda de problemas le permite buscar por país, tipo de función y lanzamiento.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
