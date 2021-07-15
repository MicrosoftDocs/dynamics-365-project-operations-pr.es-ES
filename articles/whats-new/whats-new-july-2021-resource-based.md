---
title: 'Novedades de julio de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de julio de 2021 de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5dbf9c7158ce7d9e568e270791e7e7aaf8ce731d
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433539"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de julio de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

*Se aplica a: Project Operations para escenarios basados en recursos/no mantenidos en existencias*

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

   - Project Operations en la versión del entorno 4.12.0.148 de Microsoft Dataverse.
   - Gestión de proyectos y contabilidad en el entorno de la versión 10.0.20 de Dynamics 365 Finance.

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- Capacidad de los administradores para ver los registros de PSS y los registros de conjuntos de operaciones desde el menú de configuración. Los registros se almacenan durante 90 días.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de escritura dual de Project Operations en esta versión.

Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si la última versión de la asignación no está activada. Puede ver la versión activa de la asignación en la página **Escritura dual** en la columna **Versión**. Active una nueva versión de la asignación seleccionando **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado un mapa de asignación lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) en la guía de resolución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de características**              | **Número de referencia** | **Actualización de calidad**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facturación y precios           | 2224046              | El campo **Clase de transacción** se puede editar en la pestaña **Detalles de línea de oferta**, pero está bloqueada si está trabajando desde la página **Detalles de línea de oferta**.                                                                     |
| Facturación y precios           | 2224400              | La acción **Cerrar la oferta como ganada** falla cuando una oferta no tiene hitos de fecha.                                                                                                                                    |
| Facturación y precios           | 2234089              | Cuando introduce manualmente una descripción de producto, se borra después de introducir una cantidad para una estimación de material.                                                                                                                         |
| Facturación y precios           | 2234100              | La cuadrícula **Configuración de facturación de tareas** no incluye la columna **Material** y su valor en la pestaña **Facturación de tareas** del proyecto.                                                                                                       |
| Facturación y precios           | 2277409              | El id. del producto no está disponible en el detalle de la línea de contrato para una línea de tipo de material.                                                                                                                                        |
| Facturación y precios           | 2281728              | La creación de una línea de contrato reevalúa innecesariamente los datos reales, lo que provoca aumentos significativos en el volumen de datos y afecta al rendimiento.                                                                                |
| Facturación y precios           | 2298668              | Las líneas del diario asociadas a un gasto retirado y eliminado no se eliminan.                                                                                                                                     |
| Facturación y precios           | 2300192              | Cuando varios usuarios están editando una factura, es posible que se cree un nuevo detalle de línea de factura en una factura confirmada.                                                                                   |
| Facturación y precios           | 2301569              | Las facturas no se pueden corregir si se ha aplicado un saldo anticipado de 0 \$.                                                                                                                                        |
| Facturación y precios           | 2307965              | Se produce un error si se crea un precio de categoría al que le falten valores.                                                                                                                           |
| Facturación y precios           | 2326870              | Se produce un error en **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** si **producttypecode** es nulo.                                                                            |
| Facturación y precios           | 2332732              | Se produce un error si se crea un hito de línea de contrato sin una línea de pedido.                                                                                                                |
| Planificación y seguimiento de proyectos | 2181094              | La API de programación de proyectos ahora admite registros de PSS y registros de conjuntos de operaciones que se almacenan durante 90 días.                                                                                                                  |
| Planificación y seguimiento de proyectos | 2254201              | La etiqueta **Modo de programación** se actualiza con detalles que describen la lógica predeterminada.                                                                                                                                      |
| Planificación y seguimiento de proyectos | 2300252              | El caché de respuesta **openProject** se actualiza e incluye al propietario de la token en la clave del caché, **URL base** y **URL de segmento**, para que **Solicitar URL** siempre se puede volver a crear si **URL base** cambia. |
| Planificación y seguimiento de proyectos | 2301312              | **msdyn_membershipstatus** ha sido eliminado de la vista **Miembro del equipo del proyecto**.                                                                                                                                        |
| Planificación y seguimiento de proyectos | 2302759              | Los productos se obtienen innecesariamente en las pestañas **Asignaciones de recursos**, **Estimados** y **Estimaciones de gastos**.                                                                                                        |
| Planificación y seguimiento de proyectos | 2308050              | **CopyProject** falla con el error "No se pudo obtener el símbolo (token) para hablar con el servicio remoto".                                                                                                                           |
| Planificación y seguimiento de proyectos | 2322650              | La vista **Lista de tareas del proyecto** se ha actualizado para mostrar la fecha de la tarea de forma predeterminada.                                                                                                            |
| Planificación y seguimiento de proyectos | 2327266              | **CopyProject** genera el error "Clave no encontrada en el diccionario" al copiar estimaciones.                                                                                                      |
| Planificación y seguimiento de proyectos | 2328123              | **CopyProject** genera el error "No se pudo obtener el símbolo (token) para hablar con el servicio remoto".                                                                                                                          |
| Planificación y seguimiento de proyectos | 2336258              | **CopyProject** copia incorrectamente los nombres de posición de los recursos.                                                                                                                                                 |
| Facturación y precios           | 2224476              | El campo **Recurso que se puede reservar** no es el predeterminado correctamente para el usuario que inició sesión en la página **Uso de materiales**.                                                                                                            |
| Administración de recursos           | 2277249              | Se produce un error cuando se actualiza un requisito de recursos no basado en un proyecto.                                                                                                            |
| Administración de recursos           | 2323869              | El uso de recursos no reconoce correctamente los recursos filtrados.                                                                                                                                             |
| Tiempo y gasto              | 2176538              | Se aplican operadores de filtro incorrectos al control **Entrada de tiempo**.                                                                                                                                                   |
| Tiempo y gasto              | 2177462              | Eliminar una entrada de tiempo en la cuadrícula no actualiza el estado de los botones **Enviar**, **Recuperar**, **Eliminar** y **Editar entrada** como se esperaba.                                                                                        |
| Tiempo y gasto              | 2299985              | **TimeEntriesImportFromResourceAssignment** no mantiene la hora de inicio/fin de los contornos de asignación.                                                                                                  |
| Tiempo y gasto              | 2318426              | Después de enviar una entrada de tiempo, los campos bloqueados aún se pueden editar.                                                                                                                                   |
| Tiempo y gasto              | 2323749              | Se produce un error cuando se crea un gasto a partir de la pestaña **Relacionados** de un recurso que se puede reservar.                                                                                                      |
| Tiempo y gasto              | 2327678              | Cuando crea una entrada de tiempo desde la pestaña **Relacionados** de un recurso que se puede reservar, el recurso principal no se pasa al control de entrada de tiempo.                                                                            |
| General                       | 2296857              | Seguimiento del progreso para trabajos de larga duración.                                                                                                                                                                        |
| General                       | 2253682              | La solución de escritura dual de Project Operations no debe instalarse cuando el núcleo de escritura dual está instalado en un entorno sin la solución de orquestación de escritura dual.                                                |
| General                       | 2316420              | El aprovisionamiento del núcleo de Project Service falla si se cambia la unidad de negocio del usuario de la aplicación.                                                                                                                     |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestión de proyectos y contabilidad en Dynamics 365 Finance

| Área de características                      | Número de referencia | Actualización de calidad                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestión de proyectos y contabilidad | 4620267          | No se puede personalizar los formularios para añadir un campo **Finalidad** a las páginas **Transacción registrada del proyecto**, **Creación de propuesta de factura** o **Propuesta de factura**.                                                                                                                                                                                         |
| Gestión de proyectos y contabilidad | 4613449          | Cuando selecciona un Id. de contrato de proyecto en Finance, el entorno integrado de Project Operations abre la página para crear un nuevo registro en lugar de la página para contratos de proyectos ya creados.                                                                                                                                           |
| Gestión de proyectos y contabilidad | 4614445          | En la implementación del escenario integrado de Project Operations, no puede editar el **Grupo de impuestos de artículos** en la propuesta de factura que se importa desde el almacenamiento provisional. El grupo de impuestos de artículos debe ser editable para una propuesta de factura abierta de todos los tipos de transacciones, incluidos a cuenta, horas, gastos, tarifas y artículos. |
| Gestión de proyectos y contabilidad |                  | No se puede publicar una propuesta de factura que sea resultado de una corrección de transacción de tiempo negativa.                                                                                                                                                                                                                                              |
| Gestión de proyectos y contabilidad |                  | Las líneas de propuesta de factura se duplican debido a múltiples procesos periódicos de **Importar desde almacenamiento provisional** que se ejecutan al mismo tiempo.                                                                                                                                                                                                                |

