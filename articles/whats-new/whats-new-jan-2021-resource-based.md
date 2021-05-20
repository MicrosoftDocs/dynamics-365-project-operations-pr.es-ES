---
title: 'Novedades de enero de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de enero de 2021 de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ece05f1f551b18a5b30610af57d68baa120948fb
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951005"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de enero de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

  - Project Operations en el entorno de Dataverse versión 4.6.0.154
  - Gestión de proyectos y contabilidad en el entorno de Dynamics 365 Finance versión 10.0.16

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| **Implementación y configuración** | 2106818 | Se ha corregido el cambio de nombre del recurso web que causaba problemas relacionados con la personalización de una página. |
| **Facturación y precios** | 2091908 | Se ha corregido la visibilidad de las opciones **Bloquear precios** y **Usar precios actuales** en la página **Factura** cuando se instala Project Operations junto con Dynamics 365 Field Service. |
| **Facturación y precios** | 2103058 | Se ha renovado la opción **Totales del proyecto** de forma que pueda procesar valores nulos para el coste real en una tarea. |
| **Facturación y precios** | 2116100 | Se han mejorado los mensajes de error de la funcionalidad **Corregir entradas en datos reales**. |
| **Facturación y precios** | 2116129 | Se ha mejorado la visibilidad de las estimaciones de gastos en la pestaña **Estimaciones** de la página **Proyectos**. |
| **Facturación y precios** | 2119112 | Agregación fija de ventas reales y coste real cuando se utilizan diferentes tipos de cambio. |
| **Facturación y precios** | 2134705 | Se ha corregido el error "No se puede leer la propiedad **getResourceString** de algo indefinido" cuando se abre la página **Factura** con Field Service instalado. |
| **Administración de oportunidades** | 2022195 | La cuadrícula de facturación basada en tareas de la página **Proyecto** incluye un icono que indica que hay un contrato o una línea de contrato u oferta vinculada a esa tarea. |
| **Administración de oportunidades** | 2029135 | Se ha corregido el error del proceso empresarial que se produce cuando un usuario intenta abrir una línea de factura en una factura confirmada que tiene un pago a cuenta facturado. |
| **Administración de oportunidades** | 2040713 | Se ha corregido el error de script que se produce al crear una factura a partir de un contrato con Field Service instalado. |
| **Planificación y seguimiento de proyectos** | 2090202 | Se han marcado las reglas de negocio que ya no se utilizan como **En desuso**. |
| **Tiempo y gasto** | 2091249 | Se han establecido controles más estrictos para que los usuarios no puedan cambiar la tarea en una entrada de tiempo enviada o aprobada. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestión de proyectos y contabilidad en Dynamics 365 Finance

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| **Gestión de proyectos y contabilidad** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Importe incorrecto del contrato en la página **En cuenta** para un proyecto de precio fijo con múltiples fuentes de financiación. |
| **Gestión de proyectos y contabilidad** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | El marcador de posición **Invoiceproposal.PSAnfRefProjId** no muestra el id. de proyecto para el flujo de trabajo, **Revisar propuestas de factura de proyecto**. |
| **Gestión de proyectos y contabilidad** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Se utiliza una fecha de descuento por pronto pago incorrecta al registrar propuestas de factura de proyecto. |
| **Gestión de proyectos y contabilidad** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | La eliminación y lectura de la asignación de recursos en Project Operations duplica las entradas de previsión del proyecto en Finance. |
| **Gestión de proyectos y contabilidad** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | En Project Operations no se pueden crear estimaciones de proyecto en Dataverse sin tener una línea de contrato en el proyecto. |
| **Gestión de proyectos y contabilidad** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | La dimensión financiera de una transacción de gastos del proyecto no está sincronizada con el asiento relacionado y la distribución contable del informe de gastos cuando los costes se registran en Saldo. |
| **Gestión de proyectos y contabilidad** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | El filtro **Estado de la factura** en las transacciones de proyecto registradas para proyectos de precio fijo no funciona. |
| **Gestión de proyectos y contabilidad** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | La eliminación de estimación inversa no funciona en la sección **Periódica**. |
| **Gestión de proyectos y contabilidad** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Se pueden eliminar líneas de propuesta de factura en Project Operations cuando está integrado con Dataverse. |
| **Gestión de proyectos y contabilidad** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Hay que evitar habilitar la característica de varias líneas de contrato sin la integración de Dataverse. |
| **Gestión de proyectos y contabilidad** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Cuando la facturación en cuenta es igual a los beneficios y pérdidas, los ingresos facturados se muestran como cero en la página Estimaciones. |
| **Gestión de proyectos y contabilidad** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Las correcciones de facturas no funcionan en entornos integrados. |
| **Gestión de proyectos y contabilidad** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Al contabilizar el valor de ventas de un trabajo en curso en la facturación de proyectos de empresas vinculadas se selecciona una cuenta incorrecta. |
| **Gestión de proyectos y contabilidad** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | En Project Operations no se pueden actualizar las dependencias de las tareas de estimación en Dataverse. |
| **Gestión de proyectos y contabilidad** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | La eliminación repetida de los diarios de integración de Project Operations en Finance conduce a la pérdida de datos. |
| **Gestión de proyectos y contabilidad** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Se produce el siguiente error al registrar una propuesta de factura de proyecto: "La transacción no cuadra en la divisa de notificación cuando se agrega una factura anticipada deducida". |
| **Gestión de proyectos y contabilidad** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Se incluye un id. de proyecto incorrecto en las deducciones después de que se actualice el contrato de proyecto predeterminado en Project Operations. |
| **Gestión de proyectos y contabilidad** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | La estimación y el reconocimiento de ingresos no se pueden completar cuando Project Operations está habilitada. |
| **Gestión de proyectos y contabilidad** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | En Project Operations, quitar un proyecto de un contrato no restablece el proyecto predeterminado en el contrato. |
| **Gestión de proyectos y contabilidad** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | En Project Operations, en una factura de empresas vinculadas, las líneas de gastos incorrectas aparecen en la lista **Agregar línea**. |
| **Viajes y gastos** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Las líneas de gastos no se pueden registrar porque falta la configuración de la hora en la línea del contrato. |
| **Viajes y gastos** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Cuando la validación de proyecto/categoría es obligatoria, las categorías de gastos asociadas al proyecto no son visibles en el informe de gastos. |
| **Viajes y gastos** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | El saldo del anticipo en efectivo no se actualiza cuando se publica un informe de gastos por línea. |
| **Viajes y gastos** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Se produce un error del trabajo **Actualizar información de pago** después de revertir liquidaciones en las que se liquidaba una factura con dos o más transacciones de pago. |
| **Viajes y gastos** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Hay un problema con el cálculo de reducción de comida del último día para la categoría de gastos de dieta. |
| **Viajes y gastos** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | El informe **Tipo de gasto por empleado** no muestra los gastos detallados si la primera conexión del usuario fue en el idioma es-MX. |
| **Viajes y gastos** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | El pago de proveedor para una factura de informe de gastos utiliza una cuenta de resumen incorrecta para contabilizar la liquidación. |
| **Viajes y gastos** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Cuando se registra un informe de gastos con las opciones **Permitir la agrupación de transacciones según la cuenta de pago de compensación** y **Corrección de la fecha contable al contabilizar** activadas, las fechas contables no se agrupan en la tabla **Distribución contable**, lo que afecta a los registros de impuestos sobre las ventas. |
| **Viajes y gastos** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | La asignación de subcategorías de gastos se elimina cuando se desactiva la casilla Usar en gastos y luego se vuelve a activar. |
| **Viajes y gastos** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | No se puede crear un informe de gastos de empresas vinculadas si el id. de proyecto se agrega en el nivel del encabezado. |
| **Viajes y gastos** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Existe un problema de pagos de gastos cuando el importe del gasto es mayor que el importe del anticipo en efectivo. |
| **Viajes y gastos** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | El campo **Id. de proyecto** en un informe de gastos de empresas vinculadas está vacío si el rol de usuario está asignado a una organización específica. |
| **Viajes y gastos** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | La categoría de gastos se bloquea al agregar una nueva línea de gastos. |
| **Viajes y gastos** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | El desglose de las líneas del informe de gastos que ya están divididas da como resultado el registro incompleto de un asiento de proveedores/contabilidad general. A causa de la duplicación de **TRVEXPTRANS.SOURCEDOCUMENTLINE**, el Explorador de origen de contabilidad tampoco funciona. |
| **Viajes y gastos** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | El índice agregado en la tabla **TRVREQUISITIONLINE** para la que el cliente tiene duplicados genera un error durante la actualización. |
| **Viajes y gastos** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | En Project Operations, no se puede crear ni aprobar tiempo con tareas de empresas vinculadas en Dataverse. |

## <a name="regulatory-updates"></a>Actualizaciones regulatorias

Para obtener información sobre actualizaciones normativas para aplicaciones de Finance and Operations, vea [Actualizaciones regulatorias](/dynamics365/finance/localizations/regulatory-updates). También puede iniciar sesión en LCS y ver las actualizaciones normativas planificadas mediante la herramienta de búsqueda de problemas. La búsqueda de problemas le permite buscar por país, tipo de función y lanzamiento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]