---
title: Sincronizar los contratos de proyecto y los proyectos directamente desde Project Service Automation a Finance
description: Este tema describe la plantilla y las tareas subyacentes que se utilizan para sincronizar los contratos del proyecto y los proyectos directamente desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a470fd86ceccd7b6058da6972399a6d6be2a991
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764840"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Sincronizar los contratos de proyecto y los proyectos directamente desde Project Service Automation a Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tema describe la plantilla y las tareas subyacentes que se utilizan para sincronizar los contratos del proyecto y los proyectos directamente desde Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE] 
> Si utiliza la Enterprise Edition7.3.0, debe instalar KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flujo de datos para Project Service Automation con Finance

> [!NOTE]
> Antes de poder usar la solución de integración de Project Service Automation en Finance, debe estar familiarizado con la característica de integración de datos de Dynamics 365.

La solución de integración de Project Service Automation con Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Project Service Automation y Finance. La plantilla de integración que está disponible con la función de integración de datos permite el flujo de datos sobre contratos de proyecto, proyectos, líneas de contrato de proyecto e hitos de línea de contrato de proyecto desde Project Service Automation hasta Finance.

La siguiente ilustración muestra cómo se sincronizan los datos entre Project Service Automation y Finance.

[![Flujo de datos para la integración de Project Service Automation con Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Plantillas y tareas

Para tener acceso a las plantillas disponibles, en el centro de administración de Microsoft Power Apps, seleccione **Proyectos** y luego, en la esquina superior derecha, seleccione **Nuevo proyecto** para seleccionar plantillas públicas.

Las siguientes plantillas y las tareas subyacentes se utilizan para sincronizar los contratos de proyectos y los proyectos desde Project Service Automation a Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integración con Dynamics 365 Project Service Automation v2.x
- **Nombre de la plantilla en Integración de datos:** proyectos y contratos (Project Service Automation a Finance)
- **Nombre de las tareas en el proyecto**:

    - Contratos de proyecto: Project Service Automation a Finance
    - Proyectos: Project Service Automation a Finance
    - Líneas de contrato de proyecto: Project Service Automation a Finance
    - Hitos de línea de contrato de proyecto: Project Service Automation a Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integración con Dynamics 365 Project Service Automation v3.x
Hay un cambio de esquema en Project Service Automation que afecta a la plantilla de hito de la línea de contrato del proyecto y se requiere el uso de la versión v2 de la plantilla para integrar Project Service Automation v3.x con Dynamics 365.

- **Nombre de la plantilla en Integración de datos:** proyectos y contratos (Project Service Automation 3.x a Finance) - v2
- **Nombre de las tareas en el proyecto**:

    - Contratos de proyecto: Project Service Automation a Finance
    - Proyectos: Project Service Automation a Finance
    - Líneas de contrato de proyecto: Project Service Automation a Finance
    - Hitos de línea de contrato de proyecto: Project Service Automation a Finance

Antes de poder realizar la sincronización de proyectos y contratos de proyecto, debe sincronizar las cuentas.

## <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation       | Finanzas                                                |
|----------------------------------|--------------------------------------------------------|
| Pedidos                           | Entidad de integración para contratos de proyecto                |
| Proyectos                         | Entidad de integración para proyectos                         |
| Líneas de pedido                      | Entidad de integración para la línea del contrato de proyecto           |
| Hitos de línea de contrato de proyecto | Hito de integración para la línea del contrato de proyecto |

## <a name="entity-flow"></a>Flujo de entidades

Los contratos de proyecto se administran en Project Service Automation y se sincronizan con Finance como contratos de proyecto. Como parte de la plantilla de integración, puede establecer la fuente de integración en Finance para el contrato de proyecto.

Los proyectos de tiempo y material, y de precio fijo, se gestionan en Project Service Automation y se sincronizan con Finance como proyectos. Como parte de la integración de plantillas, puede establecer el origen de integración del proyecto en Finance. Actualmente, solo se admiten proyectos de tiempo y material, y de precio fijo.


Las líneas de contrato de proyecto se administran en Project Service Automation y se sincronizan con Finance como reglas de facturación de contratos de proyecto. Si el método de facturación difiere del tipo de proyecto predeterminado, la sincronización actualiza el tipo de proyecto para el proyecto de línea de contrato y el grupo de proyectos.

Los hitos de las líneas de contrato de proyecto se administran en Project Service Automation y se sincronizan con Finance como hitos de reglas de facturación de contratos de proyecto.

## <a name="project-service-automation-to-finance-integration-solution"></a>Solución de integración de Project Service Automation con Finance

El campo **Id. de contrato del proyecto** está disponible en la página **Contratos de proyecto**. Este campo se ha convertido en una clave natural y única para apoyar la integración.

Cuando se crea un nuevo contrato de proyecto, si un valor **Id. del contrato del proyecto** aún no existe, se genera automáticamente mediante el uso de una secuencia numérica. El valor consiste en **ORD** seguido de una secuencia numérica creciente y luego un sufijo de seis caracteres. Este es un ejemplo: **ORD-01022-Z4M9Q0**.

El campo **Número de proyecto** está disponible en la página **Proyectos**. Este campo se ha convertido en una clave natural y única para apoyar la integración.

Cuando se crea un nuevo proyecto, si un valor **Número proyecto** aún no existe, se genera automáticamente mediante el uso de una secuencia numérica. El valor consiste en **PRJ** seguido de una secuencia numérica creciente y luego un sufijo de seis caracteres. Este es un ejemplo: **PRJ-01049-CCNID0**.

Cuando se aplica la solución de integración de Project Service Automation con Finance, un script de actualización configura el campo **Id. de contrato del proyecto** para los contratos de proyecto existentes y el campo **Número de proyecto** para los proyectos existentes en Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Requisitos previos y configuración de las asignaciones

- Antes de poder realizar la sincronización de proyectos y contratos de proyecto, debe sincronizar las cuentas.
- En su conjunto de conexiones, agregue una asignación de campo de clave de integración para **msdyn\_organizationalunits** a **msdyn\_name \[Nombre\]**. Es posible que primero deba agregar un proyecto al conjunto de conexiones. Para más información, consulte [Integrar datos en Common Data Service para aplicaciones](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- En su conjunto de conexiones, agregue una asignación de campo de clave de integración para **msdyn\_projects** a **msdyn\_projectnumber \[Número de proyecto\]**. Es posible que primero deba agregar un proyecto al conjunto de conexiones. Para más información, consulte [Integrar datos en Common Data Service para aplicaciones](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** para los contratos de proyectos y los proyectos pueden actualizarse con un valor diferente o eliminarse de la asignación. El valor de plantilla predeterminado es **Project Service Automation**.
- La asignación **PaymentTerms** debe actualizarse para que refleje las condiciones de pago válidas en Finance. También puede eliminar la asignación de la tarea del proyecto. La asignación de valores predeterminados tiene valores predeterminados para los datos de demostración. La siguiente tabla muestra los valores en Project Service Automation.

    | Value | Descripción   |
    |-------|---------------|
    | 1     | Pago a 30 días        |
    | 2     | 2% 10, pago a 30 días |
    | 3     | Pago a 45 días        |
    | 4     | Pago a 60 días        |

## <a name="power-query"></a>Power Query

Si se cumplen las siguientes condiciones, filtre datos mediante Microsoft Power Query para Excel:

- Tiene pedidos de venta en Dynamics 365 Sales.
- Tiene varias unidades organizativas en Project Service Automation, y estas unidades organizativas se asignarán a varias entidades jurídicas en Finance.

Si debe usar Power Query, siga estas pautas:

- La plantilla de proyectos y contratos (PSA a Fin and Ops) tiene un filtro predeterminado que incluye solo los pedidos de venta del tipo **Elemento de trabajo (msdyn\_ordertype = 192350001)**. Este filtro ayuda a garantizar que no se creen contratos de proyecto para pedidos de ventas en Finance. Si crea su propia plantilla, debe agregar este filtro.
- Cree un filtro de Power Query que incluya solo las organizaciones contratadas que deben sincronizarse con la entidad jurídica del conjunto de conexiones de integración. Por ejemplo, los contratos de proyecto que tiene con la unidad organizativa de contrato de Contoso US deben sincronizarse con la entidad jurídica USSI, pero los contratos de proyecto que tiene con la unidad organizativa de contrato de Contoso Global deben sincronizarse con la entidad jurídica USMF. Si no agrega este filtro a su asignación de tareas, todos los contratos de proyecto se sincronizarán con la entidad jurídica definida para el conjunto de conexiones, independientemente de la unidad organizativa del contrato.

## <a name="template-mapping-in-data-integration"></a>Asignación de plantillas en la integración de datos

> [!NOTE] 
> Los campos **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** y **AddressZipCode** no se incluyen en la asignación predeterminada para contratos de proyecto. Puede agregar las asignaciones si necesita que estos datos se sincronicen para los contratos de proyecto.
>
> Los cmapos **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** y **ProjectType** no se incluyen en la asignación predeterminada para proyectos. Puede agregar las asignaciones si necesita que estos datos se sincronicen para los proyectos.

Las siguientes ilustraciones muestran ejemplos de asignaciones de tareas de plantilla en Integración de datos. La asignación muestra la información del campo que se sincronizará de Project Service Automation a Finance.

[![Asignación de plantilla de contrato de proyecto](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Asignación de plantilla de proyecto](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Asignación de plantilla de líneas contrato de proyecto](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Asignación de plantilla de líneas de hito contrato de proyecto](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Asignación de hitos de línea de contrato de proyecto en la plantilla de proyectos y contratos (PSA 3.x a Dynamics), v2:

[![Asignación de hito de línea de contrato de proyecto con plantilla versión dos](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
