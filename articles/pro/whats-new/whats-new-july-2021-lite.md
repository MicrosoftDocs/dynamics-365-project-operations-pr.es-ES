---
title: 'Novedades de julio de 2021: implementación simplificada de Project Operations'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de julio de 2021 de la implementación simplificada de Project Operations.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8cff4c37e1c2df29041ef86cdcf05afa6093f890565a855024202e87fd533ea5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009237"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Novedades de julio de 2021: implementación simplificada de Project Operations

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

  - Project Operations en la versión del entorno 4.12.0.148 o 4.12.0.152 de Dataverse.

## <a name="quality-updates"></a>Actualizaciones de calidad
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
| General                       | 2376405              | Se solucionó el problema de actualización impulsado por el editor (la actualización de calidad está disponible en la versión 4.12.0.152)                                                                                                                     |
