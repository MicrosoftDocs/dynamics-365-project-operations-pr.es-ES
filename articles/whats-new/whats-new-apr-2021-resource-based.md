---
title: 'Novedades en abril de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de abril de 2021 de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868014"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades en abril de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

- Project Operations en el entorno de Dataverse versión 4.9.0.221
- Gestión de proyectos y contabilidad en el entorno de Dynamics 365 Finance versión 10.0.17

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- Materiales no almacenados para proyectos. Entre las funcionalidades clave, se incluyen:
  - Estimación y precio de materiales no almacenados durante el ciclo de ventas de un proyecto. Para obtener más información, vea [Configurar tarifas de costes y ventas para productos de catálogo (lite)](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Seguimiento del uso de materiales no almacenados durante la entrega del proyecto. Para obtener más información, vea [Registrar uso de materiales en proyectos y tareas de proyectos](../material/material-usage-log.md).
  - La facturación utilizó los costes de materiales no almacenados. Para obtener más información, vea [Administrar el trabajo pendiente de facturación](../proforma-invoicing/manage-billing-backlog.md).
- Facturación basada en tareas: se agregó la capacidad de asociar las tareas del proyecto con las líneas del contrato del proyecto, de forma que se someten al mismo método de facturación, frecuencia de facturación y clientes que los de la línea del contrato. Esta asociación garantiza una facturación, contabilidad, estimación de ingresos y reconocimiento precisos para trabajar de acuerdo con esta configuración en las tareas del proyecto.
- Las nuevas API en Dynamics 365 Dataverse permiten crear, actualizar y eliminar operaciones con **Entidades de programación**. Para obtener más información, vea [Utilizar las API de programación para realizar operaciones con entidades de programación](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations en Dynamics 365 Dataverse

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2124532 | El botón **Factura correcta** se muestra en una factura proforma cuando el importe del anticipo o el importe del anticipo aplicado están presentes en la factura original. El botón se muestra solo para entornos con la versión 10.0.19 o posteriores de Finance. |
| Facturación y precios | 2224568 | Lógica agregada para habilitar personalizaciones que implican invocar el complemento de confirmación de factura. |
| Facturación y precios | 2101098 | Se mejoró la lógica de los campos predeterminados para la factura proforma: **Dirección de facturación**, **Facturar a un nombre**, y **Condiciones de pago** ahora resultan de forma predeterminada del registro de cliente del contrato del proyecto correspondiente. |
| Facturación y precios | 2021413 | Se actualizaron los campos **Coste real** y **Ventas** en la entidad **Tarea** para incluir los valores de ventas de los gastos facturados y no facturados en las tareas. |
| Facturación y precios | 2182110 | Al copiar un contrato de proyecto, el identificador de la línea del contrato se vuelve a generar en el contrato del proyecto de destino para garantizar que sea único. |
| Administración de oportunidades | 2186741 | Validaciones agregadas para garantizar que el campo **Origen** y **Tipo de transacción** no se puede actualizar en los detalles de la línea de cotización existente. |
| Administración de oportunidades | 2191353 | Los hitos no deben crearse en una línea de contrato de tiempo y material. |
| Administración de oportunidades | 2216956 | Se resolvieron los problemas con **Actualizar precios**. |
| Planificación y seguimiento | 2182979 | Se mejoró la función de copia del proyecto para garantizar que las líneas de estimación de gastos se copien desde el proyecto original. |
| Planificación y seguimiento | 2184144 | Se mejoró la función de copia del proyecto para garantizar el nombre de posición del recurso se copie desde el proyecto original. |
| Planificación y seguimiento | 2184799 | Copia del proyecto: control más estricto para garantizar que la fecha de inicio estimada no se puede cambiar mientras se realiza la copia. |
| Planificación y seguimiento | 2185134 | Copia del proyecto: la fecha de inicio estimada del proyecto de destino se establece en la fecha de hoy. |
| Planificación y seguimiento | 2196373 | Copia del proyecto: asegúrese de que los registros del director de proyectos y los miembros del equipo no estén duplicados en el equipo del proyecto. |
| Planificación y seguimiento | 2211833 | Copia del proyecto: las asignaciones de recursos se copian desde la tarea del proyecto de origen al proyecto de destino. |
| Planificación y seguimiento | 2186541 | Problemas resueltos en la cuadrícula **Estimaciones** al agrupar por recurso. |
| Planificación y seguimiento | 2166906 | La categoría de transacción de una tarea se debe copiar en la entidad **Asignación de recursos**. |
| Administración de recursos | 2125362 | Se solucionaron problemas con la creación de un miembro del equipo genérico utilizando un método de asignación basado en horas. |
| Tiempo y gasto | 2113603 | Se solucionó el problema relacionado con la personalización con la eliminación de atributos de la página **Entrada de tiempo**. El sistema ahora verifica si el atributo existe en la página antes de acceder a ellos mediante un script. |
| Tiempo y gasto | 2204377 | Las hojas de horas copiadas deben mostrarse automáticamente cuando seleccione **Copiar semana** durante la entrada de tiempo. |
| Tiempo y gasto | 2209059 | El campo **Estado** se puede editar para las entradas de tiempo de Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestión de proyectos y contabilidad en Dynamics 365 Finance

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Gestión de proyectos y contabilidad | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | La eliminación de estimación inversa no funciona en **Periódico**.  |
| Gestión de proyectos y contabilidad | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | La característica **Ajuste de contabilidad** crea un problema con las cuentas contables que tienen seleccionado **No permitir la entrada manual**. |
| Gestión de proyectos y contabilidad | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Se agregó la lógica de negocios para procesar facturas de corrección, incluido el importe del anticipo o el importe del anticipo aplicado. |
| Gestión de proyectos y contabilidad | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Trabajo en curso: la contabilización del valor de ventas en la facturación de proyectos de empresas vinculadas selecciona una cuenta inesperada. |
| Gestión de proyectos y contabilidad | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Cuando se trabaja con anticipos en Project Operations, cambiar el proyecto predeterminado en un contrato después de que se facturan los pagos anticipados causa problemas con las deducciones entrantes. |
| Gestión de proyectos y contabilidad | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | En Project Operations, eliminar un proyecto de un contrato debe restablecer el proyecto predeterminado del contrato, si es necesario. |
| Gestión de proyectos y contabilidad | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | En Project Operations, las líneas de gastos incorrectas se muestran en la lista **Añadir línea** en la factura de empresas vinculadas. |
| Gestión de proyectos y contabilidad | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | En Project Operations, la página **Acuerdo de compra** no está visible en las entidades legales de Fiance que están integradas con Project Operations. |
| Gestión de proyectos y contabilidad | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Debido a un error de integración de Dataverse, no puede convertir una cotización a cerrada en Project Operations. |
| Gestión de proyectos y contabilidad | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** puede establecer la dirección de la factura del origen de financiación de un cliente diferente.  |
| Gestión de proyectos y contabilidad | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | En Project Operations, no se seleccionan dimensiones cuando crea un registro de factura para una transacción. |
| Viajes y gastos | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | El saldo del anticipo en efectivo no se actualiza para un informe de gastos si está aprobado y registrado línea por línea. |
| Viajes y gastos | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Los impuestos para los informes de gastos de empresas vinculadas detallados no se calculan correctamente. |
| Viajes y gastos | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Los campos adicionales relacionados con los proyectos se muestran en la página **Informes de gastos de empresas vinculadas**. |
| Viajes y gastos | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Aparece un mensaje de error incorrecto en los recibos de encabezado de los informes de gastos. |
| Viajes y gastos | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Se contabiliza incorrectamente los informes de gastos en un escenario de empresas vinculadas si el impuesto sobre las ventas se contabiliza en la entidad jurídica de destino. |
| Viajes y gastos | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Las fechas de envío de informes no se imprimen en los informes de gastos aprobados. |
| Viajes y gastos | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Los campos **Fecha de aprobación** y **Fecha de rechazo** no se rellenan después de que se aprueba un gasto. |
| Viajes y gastos | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Una solicitud de viaje creada para un trabajador se puede utilizar para el informe de gastos de otro trabajador. |
| Viajes y gastos | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Las categorías de gastos se bloquean al agregar una nueva línea de gastos. |
| Viajes y gastos | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Detallar las líneas de un informe de gastos ya dividido da como resultado una contabilización incompleta del comprobante de Proveedores/Contabilidad general e interrumpe el Explorador de origen de contabilidad porque **TRVEXPTRANS.SOURCEDOCUMENTLINE** está duplicado. |
| Viajes y gastos | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | La directiva de solicitud de viaje no funciona como se esperaba. |
| Viajes y gastos | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | El nombre de la cuenta del proveedor no se muestra en las transacciones del proyecto registradas para los informes de gastos. |
| Viajes y gastos | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | En Project Operations, no puede aprobar el tiempo con una tarea para un proyecto de empresas vinculadas. |
| Viajes y gastos | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | La categoría de devolución de anticipos en efectivo no actualiza los saldos de anticipos en efectivo cuando se registran. |
| Viajes y gastos | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | El precio de venta se calcula incorrectamente en los informes de gastos que se crearon en una divisa extranjera utilizando transacciones de tarjetas de crédito importadas y están asociados con un proyecto. |
| Viajes y gastos | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Se revirtió la entidad de datos **TrvRequisitionLine** y el índice exclusivo asociado. |
| Viajes y gastos | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Se agregó instrumentación a la generación de **SOURCEDOCUMENTLINE**. |
| Viajes y gastos | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | El diario de subcontabilidad erróneo aparece en un escenario de empresas vinculadas si el impuesto sobre las ventas se contabiliza en la entidad jurídica de destino. |
| Viajes y gastos | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | En Project Operations, las estimaciones de gastos no se eliminan de Finance cuando se eliminan de Dataverse. |
| Viajes y gastos | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Cuando una categoría de gastos no es una categoría de proyecto, las dimensiones financieras seleccionadas en la página **Gastos** no se copian en el informe de gastos. |
