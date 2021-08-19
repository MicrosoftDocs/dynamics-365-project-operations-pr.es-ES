---
title: Sincronizar los datos reales del proyecto directamente desde Project Service Automation con el diario de integración del proyecto para su publicación en Finance and Operations
description: Este tema describe las plantillas y las tareas subyacentes que se utilizan para sincronizar los datos reales del proyecto directamente desde Microsoft Dynamics 365 Project Service Automation a Finance and Operations.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85b6c07464e919e363f28d8bc62115e8fb4c72ea6631269b98fd00f324a01cba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988132"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sincronizar los datos reales del proyecto directamente desde Project Service Automation con el diario de integración del proyecto para su publicación en Finance and Operations

[!include[banner](../includes/banner.md)]

Este tema describe las plantillas y las tareas subyacentes que se utilizan para sincronizar los datos reales del proyecto directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.

La plantilla sincroniza las transacciones de Project Service Automation en una tabla de almacenamiento provisional en Finance. Una vez completada la sincronización, **debe** importar los datos de la tabla de almacenamiento provisal al diario de integración.

> [!NOTE]
> - La integración de datos reales del proyecto está disponible a partir de la versión 8.0.1.
> - Si utiliza la Enterprise Edition7.3.0 después de instalar KB 4132657 y KB 4132660, podrá usar las plantillas para integrar tareas del proyecto, categorías de transacciones de gastos, estimaciones de horas, estimaciones de gastos y datos reales, y para configurar el bloqueo de funcionalidades. Si debe restablecer las distribuciones contables, le recomendamos que también instale KB 4131710.
> - Si está utilizando la versión 7.3.0 y está transfiriendo transacciones de tarifas desde Project Service Automation, debe instalar KB 4345320 para incluir esas tarifas en la factura del proyecto.
> - Si especifica importes de impuestos en transacciones de tiempo o gastos en Project Service Automation, debe instalar la actualización 7 de Project Service Automation. De lo contrario, los datos reales de impuestos no se vincularán a los datos reales de tiempo o gastos asociados y no se sincronizarán con Finance. Para obtener más información, póngase en contacto con el equipo de soporte técnico.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flujo de datos para Project Service Automation con Finance

La solución de integración de Project Service Automation con Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Project Service Automation y Finance. Las plantillas de integración que están disponibles con la función de integración de datos permiten el flujo de datos sobre los datos reales del proyecto desde Project Service Automation a Finance.

La siguiente ilustración muestra cómo se sincronizan los datos entre Project Service Automation y Finance.

[![Flujo de datos para la integración de Project Service Automation con Finance and Operations.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Datos reales de proyecto desde Project Service Automation

### <a name="template-and-tasks"></a>Plantilla y tareas

Para tener acceso a las plantillas disponibles, en el centro de administración de Microsoft Power Apps, seleccione **Proyectos** y luego, en la esquina superior derecha, seleccione **Nuevo proyecto** para seleccionar plantillas públicas.

La siguiente plantilla y las tareas subyacentes se utilizan para sincronizar los datos reales del proyecto de Project Service Automation a Finance:

- **Nombre de la plantilla en Integración de datos**: datos reales del proyecto (PSA a Fin and Ops)
- **Nombre de las tareas en el proyecto**:

    - Datos reales
    - TransactionConnections

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanzas                                   |
|----------------------------|----------------------------------------------------------|
| Datos reales                    | Entidad de integración para datos reales del proyecto                   |
| Conexiones de transacciones    | Entidad de integración para las relaciones de transacciones del proyecto |

### <a name="entity-flow"></a>Flujo de entidades

Los datos reales del proyecto se administran en Project Service Automation y se sincronizan con el diario de integración del proyecto en Finance. La contabilidad se aplicará según las dimensiones financieras predeterminadas y la configuración de la publicación.

### <a name="prerequisites"></a>Requisitos previos

Antes de que pueda producirse la sincronización de los datos reales, debe configurar los parámetros de integración de Project Service Automation y sincronizar proyectos, tareas de proyectos y categorías de transacciones de gastos de proyectos.

### <a name="power-query"></a>Power Query

En la plantilla de datos reales del proyecto, debe usar Microsoft Power Query para Excel para completar estas tareas:

- Transforme el tipo de transacción en Project Service Automation al tipo de transacción correcto en Finance. Esta transformación ya está definida en la plantilla Datos reales del proyecto (PSA a Fin and Ops).
- Transforme el tipo de facturación en Project Service Automation al tipo de facturación correcto en Finance. Esta transformación ya está definida en la plantilla Datos reales del proyecto (PSA a Fin and Ops). Luego, el tipo de facturación se asigna a la propiedad de la línea, según la configuración en la página **Parámetros de integración de Project Service Automation**.
- Filtre por unidades organizativas de recursos específicas que deben sincronizarse con esta plantilla.
- Si el tiempo de empresas vinculadas o los datos reales de gastos de empresas vinculadas se van a sincronizar en Finance, debe transformar la unidad organizativa del contrato a la entidad jurídica correcta en Finance. En la plantilla de datos reales del proyecto (PSA a Fin and Ops), se define una columna condicional en función de los datos de demostración. Debe actualizar la última columna condicional insertada a las entidades jurídicas correctas. De lo contrario, podría producirse un error de integración o podrían importarse transacciones reales incorrectas a Finance.
- Si el tiempo de empresas vinculadas o los datos reales de gastos de empresas vinculadas no se van a sincronizar con Finance, debe eliminar la última columna condicional insertada de su plantilla. De lo contrario, podría producirse un error de integración o podrían importarse transacciones reales incorrectas a Finance.

#### <a name="contract-organizational-unit"></a>Unidad organizativa del contrato
Para actualizar la columna condicional insertada en la plantilla, haga clic en la flecha **Asignar** para abrir la asignación. Selecciona el vínculo **Consulta y filtrado avanzados** para abrir Power Query.

- Si está utilizando la plantilla predeterminada de datos reales del proyecto (PSA a Fin and Ops), en Power Query, seleccione la última **Condición insertada** en la sección **Pasos aplicados**. En la entrada **Función**, sustituya **USSI** con el nombre de la entidad jurídica que se debe utilizar con la integración. Agregue condiciones adicionales a la entrada **Función** que necesite y actualice la condición **else** en **USMF** para la entidad jurídica correcta.
- Si está creando una nueva plantilla, debe agregar la columna para admitir el tiempo y los gastos de empresas vinculadas. Seleccione **Agregar columna condicional** y especifique un nombre para la columna, como **EntidadJurídica**. Ingrese una condición para la columna, donde, si **msdyn\_contractorganizationalunitid.msdyn\_name** es \<organizational unit\>, luego \<enter the legal entity\>; más nulo.

### <a name="template-mapping-in-data-integration"></a>Asignación de plantillas en la integración de datos

Las siguientes ilustraciones muestran un ejemplo de la asignación de tareas de plantilla en Integración de datos. La asignación muestra la información del campo que se sincronizará de Project Service Automation a Finance.

[![Asignación de plantillas: datos reales.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Asignación de plantillas: conexiones de transacciones.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importar desde la tabla de almacenamiento provisional después de la integración desde Project Service Automation

El proceso periódico de importar desde la tabla de almacenamiento provisional debe ejecutarse después de la sincronización de los datos reales de Project Service Automation a Finance. Este proceso importará las transacciones del proyecto desde la tabla de almacenamiento provisional al diario de integración de Project Service Automation, donde se aplica la contabilidad y se pueden registrar las transacciones importadas. Le recomendamos que ejecute este proceso en modo por lotes; opcionalmente, se puede configurar para que se ejecute como un lote recurrente.

## <a name="update-actuals-from-finance"></a>Actualizar datos reales desde Finance

### <a name="template-and-tasks"></a>Plantilla y tareas

La siguiente plantilla y las tareas subyacentes se utilizan para sincronizar el número de comprobante y los impuestos para las transacciones del proyecto publicadas desde Finance a Project Service Automation:

- **Nombre de la plantilla en Integración de datos**: actualización de los datos reales del proyecto (Fin and Ops a PSA).
- **Nombre de las tareas en el proyecto**:

    - Datos reales 
    - TransactionConnections

### <a name="entity-set"></a>Conjunto de entidades

| Finanzas                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entidad de integración para datos reales del proyecto                   | Datos reales                    |
| Entidad de integración para las relaciones de transacciones del proyecto | Conexiones de transacciones    |

### <a name="entity-flow"></a>Flujo de entidades

Los datos reales del proyecto se administran en Project Service Automation y se sincronizan con el diario de integración del proyecto en Finance. Una vez que los datos reales se publican en Finance, se actualizan en Project Service Automation con el número de comprobante de Finance. Si se agregaron impuestos en Finance, se crean nuevos datos reales de impuestos en Project Service Automation.

### <a name="power-query"></a>Power Query

En la plantilla de actualización de datos reales del proyecto, debe usar Power Query para completar estas tareas:

- Transforme el tipo de transacción en Finance al tipo de transacción correcto en Project Service Automation. Esta transformación ya está definida en la plantilla de actualización de datos reales del proyecto (Fin and Ops a PSA).
- Transforme el tipo de facturación en Finance al tipo de facturación correcto en Project Service Automation . Esta transformación ya está definida en la plantilla de actualización de datos reales del proyecto (Fin and Ops a PSA).

### <a name="template-mapping-in-data-integration"></a>Asignación de plantillas en la integración de datos

Las siguientes ilustraciones muestran ejemplos de asignaciones de tareas de plantilla en Integración de datos. La asignación muestra la información del campo que se sincronizará de Finance a Project Service Automation.

[![Asignación de plantillas: actualización de reales.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Asignación de plantillas: actualización de transacción.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]