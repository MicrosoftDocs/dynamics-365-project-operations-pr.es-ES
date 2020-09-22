---
title: Sincronizar las estimaciones del proyecto y los proyectos directamente desde Project Service Automation a Finance and Operations
description: Este tema describe las plantillas y las tareas subyacentes que se utilizan para sincronizar las estimaciones de horas del proyecto y de los gastos del proyecto directamente desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755994"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizar las estimaciones del proyecto y los proyectos directamente desde Project Service Automation a Finance and Operations

[!include[banner](../includes/banner.md)]

Este tema describe las plantillas y las tareas subyacentes que se utilizan para sincronizar las estimaciones de horas del proyecto y de los gastos del proyecto directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE]
> - La integración de tareas del proyecto, las categorías de transacciones de gastos, las estimaciones de horas, las estimaciones de gastos y el bloqueo de funciones están disponibles en la versión 8.0.
> - Las integraciones de datos reales están disponibles a partir de la versión 8.0.1.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flujo de datos para Project Service Automation con Finance

La solución de integración de Project Service Automation con Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Project Service Automation y Finance. Las plantillas de integración que están disponibles con la característica de integración de datos permiten el flujo de datos sobre las estimaciones de horas y de los gastos del proyecto desde Project Service Automation a Finance.

La siguiente ilustración muestra cómo se sincronizan los datos entre Project Service Automation y Finance.

[![Flujo de datos para la integración de Project Service Automation con Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimaciones de horas del proyecto

### <a name="template-and-tasks"></a>Plantilla y tareas

Para tener acceso a las plantillas disponibles, en el centro de administración de Microsoft Power Apps, seleccione **Proyectos** y luego, en la esquina superior derecha, seleccione **Nuevo proyecto** para seleccionar plantillas públicas.

La siguiente plantilla y las tareas subyacentes se utilizan para sincronizar las estimaciones de horas del proyecto de Project Service Automation a Finance:

- **Nombre de la plantilla en Integración de datos**: estimaciones de horas del proyecto (PSA a Fin and Ops)
- **Nombre de las tareas en el proyecto**:

    - Relaciones de transacción
    - Estimaciones de gastos

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanzas                                       |
|----------------------------|-----------------------------------------------|
| Tareas de proyecto              | Entidad de integración para las estimaciones de horas del proyecto |

### <a name="entity-flow"></a>Flujo de entidades

Las estimaciones de horas del proyecto se administran en Project Service Automation y se sincronizan con Finance como previsiones de horas del proyecto.

### <a name="prerequisites"></a>Requisitos previos

Antes de que pueda producirse la sincronización de las estimaciones de horas del proyecto, debe sincronizar proyectos, tareas del proyecto y categorías de transacciones de gastos del proyecto.

### <a name="power-query"></a>Power Query

En la plantilla de estimaciones de horas del proyecto, debe usar Microsoft Power Query para Excel para completar estas tareas:

- Establezca el identificador del modelo de previsión predeterminado que se utilizará cuando la integración cree nuevas previsiones de horas.
- Excluya los registros específicos de recursos de la tarea que no se integrarán como previsiones de horas.
- Excluya cualquier fila de categoría de transacción vacía. Si no se completa esta tarea puede generar previsiones de horas incorrectas.

#### <a name="set-the-default-forecast-model-id"></a>Defina el identificador del modelo predeterminado

Para actualizar el identificador del modelo de previsión predeterminado en la plantilla, haga clic en la flecha **Asignar** para abrir la asignación. Después, seleccione el vínculo **Consulta y filtrado avanzados**.

- Si está utilizando la plantilla predeterminada de estimaciones de horas del proyecto (PSA a Fin and Ops), seleccione la última **Condición insertada** en la lista **Pasos aplicados**. En la entrada **Función**, sustituya **O\_forecast** con el nombre del identificador del modelo de previsión que se debe utilizar con la integración. La plantilla predeterminada tiene un identificador del modelo de previsión de los datos de demostración.
- Si está creando una nueva plantilla, debe agregar esta columna. En Power Query, seleccione **Agregar columna condicional** y especifique un nombre para la nueva columna, como **ModelID**. Indique la condición para la columna, donde, si la tarea del proyecto no es Null, entonces \<especificar el Id. del modelo de previsión\>; de lo contrario Null.

#### <a name="filter-out-resource-specific-records"></a>Filtrar registros específicos de recursos

La plantilla de estimaciones de horas del proyecto (PSA a Fin and Ops) tiene un filtro predeterminado que elimina los registros específicos de recursos. Si crea su propia plantilla, debe agregar este filtro. Seleccione el vínculo **Consulta y filtrado avanzados** para filtrar en la columna **msdyn\_islinetask** para que solo se incluyan los registros con **False**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Excluir las filas de categoría de transacción vacía

Debe agregar un filtro para eliminar las filas que tengan categorías de transacciones vacías. Esta tarea es necesaria, independientemente de si está utilizando la plantilla predeterminada o si está creando su propia plantilla. Este filtro elimina las filas de resumen de Project Service Automation que podrían provocar que las previsiones de horas en Finance sean incorrectas. Seleccione el vinculo **Consulta y filtrado avanzados** para filtrar los registros Null en la columna **msdyn\_transaccion\_valor**.

### <a name="template-mapping-in-data-integration"></a>Asignación de plantillas en la integración de datos

La siguiente ilustración muestra un ejemplo de la asignación de tareas de plantilla en Integración de datos. La asignación muestra la información del campo que se sincronizará de Project Service Automation a Finance.

[![Asignación de plantillas](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Estimaciones de gastos del proyecto

### <a name="template-and-tasks"></a>Plantilla y tareas

La siguiente plantilla y las tareas subyacentes se utilizan para sincronizar las estimaciones de gastos del proyecto de Project Service Automation a Finance:

- **Nombre de la plantilla en Integración de datos**: estimaciones de gastos del proyecto (PSA a Fin and Ops)
- **Nombre de las tareas en el proyecto**:

    - Relaciones de transacción 
    - Estimaciones de gastos

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanzas                                                  |
|----------------------------|----------------------------------------------------------|
| Conexiones de transacciones    | Entidad de integración para las relaciones de transacciones del proyecto |
| Líneas de estimación             | Entidad de integración para las estimaciones de gastos del proyecto         |

### <a name="entity-flow"></a>Flujo de entidades

Las estimaciones de gastos del proyecto se administran en Project Service Automation y se sincronizan con Finance como previsiones de gastos del proyecto.

### <a name="prerequisites"></a>Requisitos previos

Antes de que pueda producirse la sincronización de las estimaciones de gastos del proyecto, debe sincronizar proyectos, tareas del proyecto y categorías de transacciones de gastos del proyecto.

### <a name="power-query"></a>Power Query

En la plantilla de actualización de las estimaciones de gastos del proyecto, debe usar Power Query para completar las siguientes tareas:

- Filtrar para incluir solo registros de línea de estimación de gastos.
- Establezca el identificador del modelo de previsión predeterminado que se utilizará cuando la integración cree nuevas previsiones de horas.
- Transformar los tipos de facturación.
- Transformar los tipos de transacción.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrar para incluir solo líneas de estimación de gastos

La plantilla de estimaciones de gastos del proyecto (PSA a Fin and Ops) tiene un filtro predeterminado que incluye solo líneas de gastos en la integración. Si crea su propia plantilla, debe agregar este filtro. Seleccione la tarea **Relaciones de transacciones** y luego haga clic en la flecha **Asignar** para abrir la asignación. Seleccione el vínculo **Consulta y filtrado avanzados**. Filtre la columna **msdyn\_transacciontype1** para que incluya solo **msdyn\_estimación**.

#### <a name="set-the-default-forecast-model-id"></a>Defina el identificador del modelo predeterminado

Para actualizar el identificador del modelo de previsión predeterminado en la plantilla, seleccione la tarea **Estimaciones de gastos** y, luego, haga clic en la flecha **Asignar** para abrir la asignación. Seleccione el vínculo **Consulta y filtrado avanzados**.

- Si está utilizando la plantilla predeterminada de estimaciones de gastos del proyecto (PSA a Fin and Ops), en Power Query, seleccione la primera **Condición insertada** en la sección **Pasos aplicados**. En la entrada **Función**, sustituya **O\_forecast** con el nombre del identificador del modelo de previsión que se debe utilizar con la integración. La plantilla predeterminada tiene un identificador del modelo de previsión de los datos de demostración.
- Si está creando una nueva plantilla, debe agregar esta columna. En Power Query, seleccione **Agregar columna condicional** y especifique un nombre para la nueva columna, como **ModelID**. Indique la condición para la columna, donde, si el identificador de la línea de la estimación no es Null, entonces \<especificar el Id. del modelo de previsión\>; de lo contrario Null.

#### <a name="transform-the-billing-types"></a>Transformar los tipos de facturación

La plantilla de estimaciones de gastos del proyecto (PSA a Fin and Ops) incluye una columna condicional que se utiliza para transformar los tipos de facturación que se reciben de Project Service Automation durante la integración. Si crea su propia plantilla, debe agregar esta columna condicional. Selecciona el vínculo **Consulta y filtrado avanzados** y luego seleccione **Agregar columna condicional**. Especifique un nombre para la nueva columna, como **BillingType**. Después, escriba la siguiente condición:

If **msdyn\_billingtype** = 192350000, entonces **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, entonces **Chargeable**  
else if **msdyn\_billingtype** = 192350002, entonces **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformar los tipos de transacción

La plantilla de estimaciones de gastos del proyecto (PSA a Fin and Ops) incluye una columna condicional que se utiliza para transformar los tipos de transacción que se reciben de Project Service Automation durante la integración. Si crea su propia plantilla, debe agregar esta columna condicional. Selecciona el vínculo **Consulta y filtrado avanzados** y luego seleccione **Agregar columna condicional**. Especifique un nombre para la nueva columna, como **TransactionType**. Después, escriba la siguiente condición:

If **msdyn\_transactiontypecode** = 192350000, entonces **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, entonces **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Asignación de plantillas en la integración de datos

Las siguientes ilustraciones muestran ejemplos de asignaciones de tareas de plantilla en Integración de datos. La asignación muestra la información del campo que se sincronizará de Project Service Automation a Finance.

[![Asignación de plantillas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Asignación de plantillas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
