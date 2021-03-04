---
title: 'Novedades de diciembre de 2020: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de diciembre de 2020 de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3889402ab991e307bc3fe5463098dfab383a53b4
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727901"
---
# <a name="whats-new-december-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de diciembre de 2020: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

- Project Operations en el entorno de Dataverse versión 4.5.0.134
- Gestión de proyectos y contabilidad en el entorno de Dynamics 365 Finance versión 10.0.15

Para obtener información sobre cómo actualizar a esta versión, consulte [Actualizar Project Operations en el entorno de Finance](ur5-nonstocked-installation.md).

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión
En esta versión se incluyen las siguientes características:

  - [Facturación con empresas vinculadas](../project-accounting/intercompany-invoicing-overview.md) 
  - [Anticipos y pagos a cuenta de clientes](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Actualizaciones en Project Operations para escenarios basados en recursos/no mantenidos en existencias

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de características                    | Número de referencia | Actualización de calidad                                                                                                                                               |
|---------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facturación y precios             | 1986009          | Las líneas de diario creadas manualmente tienen un rendimiento incoherente cuando se confirman antes de que el proyecto se vincule o desvincule de una línea de contrato                     |
| Facturación y precios             | 2028174          | Las actualizaciones de los detalles de la línea de factura deben seguir la lógica del diario de correcciones                                                                                  |
| Facturación y precios             | 2028315          | Correcciones editables del comportamiento de cuadrícula anidada                                                                                                                        |
| Facturación y precios             | 2031070          | El ajuste de los detalles de la línea de la factura correctiva debe seguir la lógica del diario de correcciones.                                                                              |
| Facturación y precios             | 2034186          | Debe poder actualizar un proyecto en una línea de contrato.                                                                                                        |
| Facturación y precios             | 2034206          | El estado de ajuste debe establecerse durante la reversión real al desvincular un proyecto de una línea de contrato.                                                        |
| Facturación y precios             | 2040871          | Permitir actualizaciones de celdas de unidades y grupos de unidades en la cuadrícula Estimaciones de gastos                                                                                       |
| Facturación y precios             | 2053754          | Los datos reales creados a partir de ediciones de facturas no se marcan con estado de ajuste y estado de facturación.                                                                |
| Facturación y precios             | 2057874          | Se creó la conexión de transacción correcta durante la edición de detalles de líneas de factura.                                                                                     |
| Facturación y precios             | 2057875          | Se creó los orígenes de transacción correcta durante la edición de detalles de líneas de factura.                                                                                        |
| Facturación y precios           | 2057944          | Estado de No exceder se establece como Confirmado para datos reales que no están listos para facturación a partir de una corrección de factura.                                             |
| Facturación y precios           | 2066169          | Actualice la fecha contable para el registro de ventas negativas sin facturar al integrar mediante escritura dual.                                                            |
| Facturación y precios           | 2067622          | Se debe mostrar el icono de procesamiento al generar hitos.                                                                                                |
| Facturación y precios           | 2067624          | El importe contratado debe marcarse como Recomendado por la empresa al generar hitos.                                                                      |
| Facturación y precios           | 2086880          | Oculte **Sugerencia** en la cinta de opciones para las líneas de ofertas basadas en proyectos.                                                                                                |
| Facturación y precios           | 2098140          | Muestre el botón **Factura correcta** para entornos integrados.                                                                                             |
| Implementación y configuración  | 2101152          | El nuevo entorno creado con la plantilla de Project Operations del Centro de administración de Power Platform debe tener realizadas todas las operaciones posteriores a la instalación.               |
| Administración de oportunidades        | 2086601          | Los roles y categorías que están desactivados no se deben copiar en la lista de Roles imputables y Categorías de gastos imputables de las líneas de oferta y líneas de contrato. |
| Planificación y seguimiento de proyectos | 1949065          | La visibilidad de los datos funciona correctamente con un zoom del 200 %.                                                                                                                   |
| Planificación y seguimiento de proyectos | 2046317          | Posibilidad de cambiar el nombre de la entidad del proyecto en Project Operations                                                                                   |
| Planificación y seguimiento de proyectos | 2057171          | Mensaje de error actualizado cuando el campo **Fecha de inicio del proyecto** está vacío en la página **Proyecto**.                                                           |
| Planificación y seguimiento de proyectos | 2057197          | No se admite la copia de línea de estimación con referencia de tarea.                                                                                                     |
| Planificación y seguimiento de proyectos | 2060687          | La advertencia de zona horaria ahora desaparece después de una duración específica.                                                                                                      |
| Administración de recursos           | 1832887          | El Id. de categoría de recurso predeterminado debe ser estático para garantizar cargas de datos repetibles para entornos de Dataverse y Finance.                                                 |
| Tiempo y gasto              | 2081793          | El **Nombre de categoría de gastos** debe estar asignado al campo **Descripción de la categoría de gastos** en aplicaciones de Finance and Operations.                                                  |
| Tiempo y gasto              | 2034882          | El botón **Nuevo** se muestra dos veces en la barra de comandos para las entradas de tiempo cuando Dynamics 365 Field Service está instalado.                                          |
| Tiempo y gasto              | 2056028          | Actualice la página **Editar entrada de tiempo** para incluir la escala de tiempo.                                                                                                              |
| Tiempo y gasto              | 1983747          | El gráfico de entrada de tiempo muestra datos adicionales.                                                                                                                   |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestión de proyectos y contabilidad en Dynamics 365 Finance

| Área de características                        | Número de referencia | Actualización de calidad                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestión de proyectos y contabilidad | [441680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441680)           | Ajustes bloqueados para devolución de requisitos de artículo                                                                                                                                                                                                        |
| Gestión de proyectos y contabilidad | [446498](https://fix.lcs.dynamics.com/Issue/Details/?bugId=446498)           | Las notas del formulario no aparecen en las facturas del proyecto con formato.                                                                                                                                                                                                          |
| Gestión de proyectos y contabilidad | [453407](https://fix.lcs.dynamics.com/Issue/Details/?bugId=453407)           | No se permite MÉXICO CFDI 33 para facturas de proyectos para actualizar el método de pago desde la propuesta de factura.                                                                                                                                                           |
| Gestión de proyectos y contabilidad | [458149](https://fix.lcs.dynamics.com/Issue/Details/?bugId=458149)           | El parámetro que establece automáticamente la fecha contable en un período abierto no se respeta en el diario **Integración**.                                                                                                                                                             |
| Gestión de proyectos y contabilidad | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Los elementos del menú Pronóstico no son visibles en la página de lista **Proyectos**.                                                                                                                                                                                                      |
| Gestión de proyectos y contabilidad | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | No se puede abrir **Declaración de proyecto** > **Transacciones y previsión**.                                                                                                                                                                                                      |
| Gestión de proyectos y contabilidad | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | La eliminación y lectura de la asignación de recursos duplica las entradas de previsión del proyecto en Finance.                                                                                                                                                                   |
| Gestión de proyectos y contabilidad | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468)           | No se pueden crear estimaciones del proyecto en Dataverse sin tener línea de contrato en el proyecto.                                                                                                                                                                 |
| Gestión de proyectos y contabilidad | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Se produce un error en la eliminación debido a un error de desequilibrio del comprobante cuando la moneda de la empresa y la moneda de la transacción son diferentes.                                                                                                                                            |
| Gestión de proyectos y contabilidad | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382)           | El filtro para el estado de la factura en las transacciones de proyecto registradas para proyectos de precio fijo no funciona                                                                                                                                                            |
| Gestión de proyectos y contabilidad | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | No se puede actualizar la fecha de inicio de una tarea en Dataverse.                                                                                                                                                                                                                    |
| Gestión de proyectos y contabilidad | [507172](https://fix.lcs.dynamics.com/Issue/Details/?bugId=507172)           | Se permite eliminar líneas de propuesta de factura en el escenario integrado de Project Operations.                                                                                                                                                                                    |
| Gestión de proyectos y contabilidad | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989)           | Se permite eliminar líneas de propuesta de factura en el escenario integrado de Project Operations.                                                                                                                                                                                    |
| Gestión de proyectos y contabilidad | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Evitar la habilitación de la característica de varias líneas de contrato sin la integración de Dataverse.                                                                                                                                                                                        |
| Gestión de proyectos y contabilidad | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527)           | Los ingresos facturados de la pantalla de estimación son cero (0) cuando la facturación en cuenta = Pérdidas y ganancias                                                                                                                                                                          |
| Gestión de proyectos y contabilidad | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364)           | Trabajo en curso: la contabilización del valor de ventas en la facturación de proyectos de empresas vinculadas selecciona una cuenta inesperada.                                                                                                                                                                           |
| Gestión de proyectos y contabilidad | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799)           | No se puede realizar el reconocimiento de estimaciones/ingresos con Project Operations habilitada.                                                                                                                                                                         |
| Viajes y gastos                | [378738](https://fix.lcs.dynamics.com/Issue/Details/?bugId=378738)           | El gasto introducido por un delegado se devuelve al usuario del gasto y no al delegado.                                                                                                                                                                                           |
| Viajes y gastos                | [409489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=409489)           | El usuario delegado del flujo de trabajo del informe de gastos que envía el flujo de trabajo no se identifica como originador del flujo de trabajo.                                                                                                                                                             |
| Viajes y gastos                | [464658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=464658)           | Las dimensiones predeterminadas en los reemplazos de entidades jurídicas no funcionan en los informes de gastos de empresas vinculadas.                                                                                                                                                                    |
| Viajes y gastos                | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892)           | Problema con el cálculo de reducción de comida del último día para la categoría de gastos de dieta                                                                                                                                                                                    |
| Viajes y gastos                | [473646](https://fix.lcs.dynamics.com/Issue/Details/?bugId=473646)           | El campo **Importe para conciliar** de la página **Solicitud de viaje** no se actualiza después de que se elimine un elemento de línea de gastos del informe de gastos vinculado a la solicitud de viaje.                                                                                                       |
| Viajes y gastos                | [474396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=474396)           | El informe de gastos validó la directiva después de enviarla al flujo de trabajo.                                                                                                                                                                                           |
| Viajes y gastos                | [475777](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475777)            | Los recibos de gastos de viaje no se muestran correctamente para el delegado de entrada.                                                                                                                                                                                            |
| Viajes y gastos                | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714)            | El tipo de gasto por empleado no muestra los gastos detallados cuando el idioma del usuario está establecido en es-MX.                                                                                                                         |
| Viajes y gastos                | [477831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477831)            | El informe de gastos permite introducir la subcategoría incorrecta para una categoría de gastos.                                                                                                                                                                                       |
| Viajes y gastos                | [478630](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478630)            | La conciliación de anticipos en efectivo con el informe de gastos no funciona como se espera cuando el importe del informe de gastos es mayor que el importe del anticipo en efectivo.                                                                                                           |
| Viajes y gastos                | [486680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486680)            | Problemas de rendimiento con consultas relacionadas con ProjProjectLookup. El cliente está bloqueado porque la consulta está tardando mucho tiempo en ejecutarse.                                                                                                                     |
| Viajes y gastos                | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531)            | Los informes de gastos registrados con **Permitir la agrupación de transacciones según la cuenta de pago de compensación** y **Corrección de la fecha contable al contabilizar** activado muestra que las fechas contables no están agrupadas en la tabla **Distribución contable**, que afecta a los registros de impuestos sobre las ventas. |
| Viajes y gastos                | [491759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491759)            | Las transacciones de tarjetas de crédito importadas con una moneda extranjera crean transacciones de proveedor incorrectas si **IVA de inversión** se usa en las líneas del informe de gastos.                                                                                                                     |
| Viajes y gastos                | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175)            | El informe de gastos de empresas vinculadas no se puede crear si el id. de proyecto se agrega en el nivel del encabezado.                                                                                                                                                                 |
| Viajes y gastos                | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491)            | Problema de pago de gasto cuando el importe del gasto es mayor que el importe del anticipo en efectivo.                                                                                                                                                                          |
| Viajes y gastos                | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556)            | La información del Id. de proyecto debajo de un informe de gastos de empresas vinculadas está vacía si el rol de usuario está asignado a una organización específica.                                                                                                                                           |
| Viajes y gastos                | [513845](https://fix.lcs.dynamics.com/Issue/Details/?bugId=513845)            | El flujo de trabajo de registro automático del informe de gastos está completo, pero la factura no está registrada.                                                                                                                                                                                          |

### <a name="regulatory-updates"></a>Actualizaciones regulatorias
Para obtener información sobre actualizaciones normativas para aplicaciones de Finance and Operations, vea [Actualizaciones regulatorias](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). También puede iniciar sesión en LCS y ver las actualizaciones normativas planificadas mediante la herramienta de búsqueda de problemas. La búsqueda de problemas le permite buscar por país, tipo de función y lanzamiento.