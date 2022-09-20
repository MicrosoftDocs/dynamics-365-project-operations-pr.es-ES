---
title: Cambios de características de Project Service Automation a Project Operations
description: Este artículo proporciona una descripción general de los cambios de características de Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459948"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Cambios de características de Project Service Automation a Project Operations

La actualización de Dynamics 365 Project Service Automation a Dynamics 365 Project Operations Lite se entregará en tres fases. Este artículo proporciona información sobre los principales cambios que puede esperar ver cuando se complete la actualización.

| Entrega de actualización | Fase 1 <br>(Enero de 2022) | Fase 2 <br>(Noviembre de 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Sin dependencia de la estructura de descomposición del trabajo (WBS) para proyectos. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS se incluye dentro de los límites actualmente admitidos de Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS fuera de los límites admitidos actualmente de Project Operations, incluida la compatibilidad con Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Administración de proyectos

Los cambios más significativos en la experiencia del usuario estarán en el área de planificación de proyectos. Project Operations adopta una nueva experiencia moderna para administrar una estructura de descomposición del trabajo (WBS) al aprovechar las capacidades de programación proporcionadas por [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Diferencias en la experiencia de programación

La siguiente tabla resume las diferencias de programación entre Project Service Automation y Project Operations.

|  Programando     |   Project Operations   |   APE   |
|-----------------|------------------------|---------|
| Plantillas de proyecto: capacidad para definir y aplicar plantillas de proyecto cuando se crea un proyecto  |  &nbsp;    | :heavy_check_mark: |
| Integración de la estructura de descomposición del trabajo del proyecto (WBS) con el cliente de escritorio   |    &nbsp;  | :heavy_check_mark: |
| Restricciones: comenzar no antes de, terminar no más tarde de  | :heavy_check_mark: |   &nbsp;  |
| Hitos: tareas con duración cero   | :heavy_check_mark:  |  &nbsp;  |
| Las tareas basadas en recursos respetarán la disponibilidad de los recursos asignados   | :heavy_check_mark: |  &nbsp;    |
| Edición por fases: edite planes y trabaje en el día a día   |   &nbsp;  | :heavy_check_mark: |
| Programación automática/manual: use el motor de programación de proyectos para programar tareas de forma automática o manual |  &nbsp; | :heavy_check_mark:  |
| Edite proyectos grandes directamente en la interfaz de usuario: no hay límite para el tamaño de los planes que se pueden editar  | Límite de 500 tareas  | :heavy_check_mark:       |
| Porcentaje completado: marcar el progreso de la tarea   | :heavy_check_mark:  |  &nbsp;  |
| [Modos de programación del proyecto](../project-management/scheduling-modes.md): definir el proyecto como unidades fijas, esfuerzo fijo o duración fija | :heavy_check_mark: | &nbsp; |
| Línea de tiempo: cree y personalice la vista de línea de tiempo para visualizar los detalles del cronograma y comunicarse con las partes interesadas. | :heavy_check_mark:  | &nbsp; |
| Tareas impulsadas por el esfuerzo: soporte del motor de programación para programar una tarea como impulsada por el esfuerzo  | :heavy_check_mark:  | &nbsp; |
| Cuadro de diálogo **Información de la tarea**: guarde los detalles de la tarea mediante un cuadro de diálogo | :heavy_check_mark:  |  &nbsp;  |
| Arrastrar y soltar: selección múltiple de tareas y modificación de su posición en la WBS | :heavy_check_mark: | &nbsp;  |
| Vistas persistentes flexibles: defina vistas más granulares de los atributos de la tarea   | :heavy_check_mark:  | &nbsp; |
| Ordenar y filtrar la WBS  | :heavy_check_mark:  | &nbsp; |
| Vista de tableros para entrega de proyectos no en cascada  | :heavy_check_mark:   | &nbsp; |
| Vista de línea de tiempo: diagrama de Gantt interactivo utilizado para visualizar y editar la WBS   | :heavy_check_mark:  | &nbsp; |
| Métodos abreviados de teclado: use métodos abreviados de teclado para operaciones comunes, como sangrar o insertar  | :heavy_check_mark:  |  &nbsp; |
| Deshacer multinivel: realice un análisis hipotético para comprender completamente el impacto de los cambios al revertir y volver a aplicar un conjunto completo de operaciones | :heavy_check_mark: | &nbsp; |
| Cortar/Copiar/Pegar: colabore en el desarrollo del cronograma copiando y pegando los detalles del cronograma entre aplicaciones  | :heavy_check_mark: | &nbsp; |
| Listas de verificación de tareas: agregue hasta 20 elementos de la lista de verificación a una tarea   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planificación del proyecto

La página **Proyecto** de Project Operations tiene un número significativo de diferencias en comparación con la página **Proyecto** de Project Service Automation.

Las siguientes acciones han sido eliminadas de la página **Proyectos** como parte de la actualización de la fase 1:

  - **Abrir en MS Project**
  - **Crear plantilla**
  - **Desvincular de MS Project**

La página **Proyecto** de Project Operations incluye las siguientes pestañas nuevas.

- **Estimaciones de materiales**
- **Configuración de facturación de tareas**

La pestaña **Estado** se ha eliminado y el campo **Estado** está ahora en la pestaña **Resumen** con el modo de programación del proyecto.

   ![Actualizaciones a la página del Proyecto.](media/projectform.png)

La pestaña **Programación** se ha renombrado a la pestaña **Tarea** y presenta la nueva experiencia de planificación de proyectos con Project for the Web.

   ![Nueva pestaña de tareas del proyecto.](media/tasktab.png)

## <a name="scheduling-modes"></a>Modos de programación

Project Operations ha introducido una nueva característica [Modos de programación](../project-management/scheduling-modes.md). Todos los proyectos existentes de Project Service Automation tendrán como valor predeterminado **Duración fija** en Project Operations. Sin embargo, el valor predeterminado para nuevos proyectos se puede administrar yendo a **Configuración** > **Parámetros** > **Parámetro** > **Modo de programación**.

   ![Configuración de parámetros de proyecto para el modo Programación.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Límites de planificación de proyectos

Project Operations se basa en Project for the Web para todas las operaciones de programación de proyectos. Project for the Web administra la estructura de descomposición del trabajo utilizando los límites de la siguiente tabla.

| **Campo**                                          | **Límite**             |
|----------------------------------------------------|-----------------------|
| Tareas totales máximas para un proyecto                  | 500                   |
| Duración total máxima para un proyecto               | 3650 días (10 años)  |
| Recursos totales máximos para un proyecto              | 300                   |
| Vínculos totales máximos (solo sucesor) para un proyecto | 600                   |
| Campos personalizados totales máximos para un proyecto          | 10                    |
| Nivel máximo de jerarquía                            | 10 niveles             |
| Vínculos máximos (sucesor + predecesor)            | 20                    |
| Duración máxima de la tarea hoja                      | 1250 días             |
| Duración máxima de una tarea de resumen                 | 3650 días (10 años)  |
| Recursos máximos asignados a una tarea               | 20 recursos          |
| Intervalo de fechas admitido para una tarea                    | 1/1/2000 - 31/12/2149 |
| Elementos de la lista de comprobación                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Extensibilidad y desarrollo de la planificación de proyectos

Después de actualizar a Project Operations, debe usar las API de planificación de proyectos para ejecutar operaciones de creación, actualización y eliminación en las siguientes entidades:

|   Nombre de entidad           |   Nombre lógico de la entidad       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tarea de proyecto            | msdyn_projecttask           |
| Dependencia de tareas de proyecto | msdyn_projecttaskdependency |
| Asignación de recursos     | msdyn_resourceassignment    |
| Cubo de proyecto          | msdyn_projectbucket         |
| Miembro del equipo del proyecto     | msdyn_projectteam           |

Si actualmente tiene personalizaciones que involucran a estas entidades, consulte [Usar las API de programación de proyectos para realizar operaciones con entidades de programación](../project-management/schedule-api-preview.md) para la guía de implementación.

## <a name="data-model-changes"></a>Cambios del modelo de datos

Como parte de la fase 1 de actualización, hay cambios en el modelo de datos. Estos cambios son principalmente cambios de campos en entidades existentes. En la fase 1, las entidades **msydn_project** y **msdyn_projectteam** son una refactorización de personalizaciones. 

> [!IMPORTANT]
> Esta sección se actualizará con entidades adicionales a medida que se completen las futuras fases de actualización.

Los siguientes campos se han reemplazado por nuevos campos.

|   Entity          |   Nombre lógico anterior   |   Nuevo nombre lógico    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Se han agregado los siguientes campos.

|   Entity          |   Nombre lógico                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Muestra el total acumulado de las ventas reales por tarifas del proyecto. Solo para usarse en Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Muestra el coste agregado real de los costes de materiales reales del proyecto. Solo para usarse en Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Muestra el agregado de las ventas reales de materiales del proyecto. Solo para usarse en Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | La línea de contrato asociada a este proyecto. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Este es un campo interno del sistema que se usa para **Copiar proyecto** en relación con el identificador de correlación. Solo para usarse en Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Este es un campo interno del sistema que se usa para **Copiar proyecto** en relación con el identificador de sesión. Solo para usarse en Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Última sincronización del token de revisión global xRM del servicio de programación de proyectos. |
| msdyn_project     | msdyn_msprojectdocument                      | El documento de Microsoft Project que pertenece al proyecto. |
| msdyn_project     | msdyn_plannedmaterialcost                    | El agregado real de los costes de materiales planeados del proyecto. Solo para usarse en Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | El agregado de las ventas de materiales planeadas del proyecto. Solo para usarse en Project Service Automation. |
| msdyn_project     | msdyn_program                                | El programa con el que está relacionado este proyecto. |
| msdyn_project     | msdyn_quotelineproject                       | La línea de oferta asociada a este proyecto. |
| msdyn_project     | msdyn_replaylogheader                        | Encabezado de los registros de reproducción. |
| msdyn_project     | msdyn_schedulemode                           | Modo de programación predeterminado usado para todas las tareas del proyecto.  |
| msdyn_project     | msdyn_taskearlieststart                      | La fecha de inicio más temprana de cualquier tarea del proyecto.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | El miembro del equipo del proyecto del que se copió este miembro del equipo del proyecto. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indica si se creará el requisito de recurso para un miembro de equipo genérico recién creado.  |
| msdyn_projectteam | msdyn_deletestatus                           | El estado de eliminación del miembro del equipo para realizar un seguimiento si se ha enviado una solicitud de eliminación al servicio de programación de proyectos y si este devuelve una respuesta correctamente y dentro de la ventana de tiempo esperada. |
| msdyn_projectteam | msdyn_effortcompleted                        | Sigue el esfuerzo realizado por el miembro del equipo en sus asignaciones. |
| msdyn_projectteam | msdyn_effortremaining                        | Sigue el esfuerzo por completar por el miembro del equipo en sus asignaciones. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | El período de espera desde que el miembro del equipo envía una solicitud de eliminación al servicio de programación de proyectos hasta que el miembro del equipo se elimina realmente en Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Marca de tiempo que se debe registrar cuando se envía la solicitud de eliminación de miembro del equipo al servicio de programación de proyectos. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Muestra el miembro del equipo del proyecto del que se copió este miembro del equipo del proyecto.  |

## <a name="project-templates"></a>Plantillas de proyecto

Project Operations no proporciona soporte para plantillas de proyecto. Sin embargo, puede replicar gran parte de la funcionalidad principal con el uso de la [API de copia de proyecto](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Compatibilidad con complementos de escritorio

La compatibilidad para el complemento de Microsoft Project Desktop no estará disponible en las primeras 2 fases de la actualización. En la fase 3, los clientes que tengan proyectos más grandes que los límites admitidos actualmente de Project for the Web podrán usar el complemento de escritorio.

## <a name="editing-resource-assignment-contours"></a>Edición de contornos de asignación de recursos

La capacidad de editar contornos de asignación de recursos estará disponible cuando la fase 2 de la actualización esté disponible.

## <a name="billing-and-pricing"></a>Facturación y precios

Se han agregado las siguientes características nuevas en Project Operations. Estas características son de naturaleza aditiva y no afectan el modelo de datos de Project Service Automation.

- [Registrar el uso de materiales en proyectos y tareas de proyectos](../material/material-usage-log.md)
- [Administración de subcontrataciones](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos basados en pagos a cuenta y anticipos](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Contrato sin exceder los estados y las validaciones](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Facturación basada en tareas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Componentes en desuso

Las siguientes tablas documentan todos los campos en desuso que se mueven a la actualización posterior a la solución de componentes en desuso. Para obtener más información y un enlace a la solución, consulte [Componentes en desuso de Dynamics 365 Project Service Automation 3x a Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

