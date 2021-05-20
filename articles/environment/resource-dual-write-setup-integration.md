---
title: Integración de datos de instalación y configuración de Project Operations
description: Este tema proporciona información sobre cómo instalar y configurar asignaciones de doble escritura de Project Operations.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939051"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integración de datos de instalación y configuración de Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema proporciona información sobre la integración de doble escritura de Project Operations para entidades de instalación y configuración.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratos de proyecto, líneas de contrato y proyectos

Los contratos de proyecto, las líneas de contrato y los proyectos se crean en Dataverse y se sincronizan con aplicaciones de Finance and Operations para contabilidad adicional. Los registros de estas entidades se pueden crear y eliminar solo en Dataverse. Sin embargo, los atributos contables, como los valores predeterminados del grupo de impuestos sobre ventas y las dimensiones financieras, se pueden agregar a estos registros en las aplicaciones de Finance and Operations.

  ![Conceptos de integración de contratos de proyectos](./media/1ProjectContract.jpg)

Las actividades de ventas clientes potenciales, oportunidades y ofertas se siguen en Dataverse y no se sincronizan con aplicaciones de Finance and Operations porque no hay una contabilidad descendente asociada con esta actividad.

La funcionalidad del contrato del proyecto en Dataverse crea un registro de contrato de proyecto en aplicaciones de Finance and Operations que utilizan la asignación de tabla **Encabezados de contrato de proyecto (salesorders)**. Al guardar un contrato de proyecto en Dataverse también se inicia la creación de un registro de entidad de cliente de contrato de proyecto. Este registro se sincroniza con aplicaciones de Finance and Operations que utilizan la asignación de tabla **Origen de financiación del proyecto (msdyn\_projectcontractssplitbillingrules)**. Esta asignación también sincroniza las adiciones, actualizaciones y eliminaciones de clientes de contratos de proyectos. Los porcentajes de facturación dividida entre los clientes del contrato del proyecto se resuelven solo en Dataverse y no se sincronizan con aplicaciones de Finance and Operations.

Después de que se crea un contrato de proyecto en Dataverse, el contable del proyecto puede actualizar los atributos de contabilidad para este contrato de proyecto en aplicaciones de Finance and Operations yendo a **Administración y contabilidad de proyectos** > **Contratos de proyecto** > **Configuración** > **Mostrar contabilidad predeterminada**. El contable puede revisar los atributos del contrato del proyecto operativo, como la fecha de entrega solicitada y el importe del contrato, seleccionando el ID del contrato del proyecto en aplicaciones de Finance and Operations, lo que abre el registro del contrato del proyecto relacionado en Dataverse.

La entidad del proyecto se sincroniza con aplicaciones de Finance and Operations que utilizan la asignación de tabla **Proyectos V2 (msdyn\_projects)**. El contable del proyecto puede:

  - Revisar proyectos en aplicaciones de Finance and Operations yendo a **Administración y contabilidad de proyectos** > **Todos los proyectos**. 
  - Actualice los atributos de contabilidad del proyecto en aplicaciones de Finance and Operations yendo a **Administración y contabilidad de proyectos** > **Todos los proyectos** > **Configuración** > **Mostrar contabilidad predeterminada**.  
  - Revise los atributos operativos del proyecto, como las fechas estimadas de inicio y finalización, seleccionando el ID del proyecto en aplicaciones de Finance and Operations, lo que abre el registro del proyecto relacionado en Dataverse.

Un proyecto está asociado con un contrato de proyecto a través de la entidad **Línea de contrato de proyecto**.

Las líneas de contrato del proyecto en Dataverse crean una regla de facturación de contrato de proyecto en aplicaciones de Finance and Operations que utilizan la asignación de tabla **Líneas de contrato de proyecto (salesorderdetails)**. El método de facturación define el tipo de regla de facturación del contrato del proyecto en aplicaciones de Finance and Operations:

  - Las líneas de contrato de proyecto con un método de facturación de tiempo y material crean una regla de facturación de tipo tiempo y material.
  - Las líneas de contrato del método de facturación de precio fijo crean una regla de facturación de hitos.

Las líneas de contrato del proyecto pueden ser revisadas por el contable del proyecto en aplicaciones de Finance and Operations yendo a **Administración y contabilidad de proyectos** > **Contratos de proyecto** > **Configuración** > **Mostrar contabilidad predeterminada** y revisando los detalles de la pestaña **Líneas de contrato**. El contable también puede establecer dimensiones financieras predeterminadas para las líneas de contrato del método de facturación de precio fijo en esta pestaña.

## <a name="billing-milestones"></a>Hitos de facturación

Las líneas de contrato de proyecto que utilizan el método de facturación de precio fijo se facturan a través de hitos de facturación. Los hitos de facturación se sincronizan para proyectar transacciones a cuenta en aplicaciones de Finance and Operations mediante el uso de la asignación de tabla **Hitos de la línea de contrato de integración de Project Operations (msdyn\_ contractlinescheduleofvalues)**.

  ![Integración de hitos de facturación](./media/2Milestones.jpg)

El contable puede revisar las transacciones a cuenta y ajustar los atributos de contabilidad para esas transacciones yendo a **Administración y contabilidad de proyectos** > **Contratos de proyecto** > **Mantener** > **Transacciones a cuenta** o **Administración y contabilidad de proyectos** > **Todos los proyectos** > **Mantener** > **Transacciones a cuenta**.

Cuando crea por primera vez un hito de facturación para una línea de contrato de proyecto determinada, el sistema crea automáticamente un proyecto de estimación de ingresos de precio fijo para el proyecto asociado con esta línea de contrato. Los proyectos de estimación de ingresos de precio fijo se pueden revisar yendo a **Administración y contabilidad de proyectos** > **Proyectos de estimación de ingresos a precio fijo**.

### <a name="project-tasks"></a>Tareas de proyecto

Las tareas del proyecto se sincronizan con aplicaciones de Finance and Operations a través de la asignación de tabla **Tareas del proyecto (msdyn\_projecttasks)** solo con fines de referencia. No se admite la creación, actualización y eliminación de operaciones a través de aplicaciones de Finance and Operations.

  ![Integración de tareas de proyecto](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de proyecto

La entidad **Roles de recursos del proyecto** se sincroniza con aplicaciones de Finance and Operations que utilizan la asignación de tabla **Roles de recursos del proyecto para todas las empresas (bookableresourcecategories)** solo con fines de referencia. Dado que los roles de recursos en Dataverse no son específicos de la empresa, el sistema crea automáticamente los respectivos registros de roles de recursos específicos de la empresa en aplicaciones de Finance and Operations automáticamente para todas las entidades legales incluidas en el ámbito de la integración de doble escritura.

![Integración de roles de recursos](./media/5Resources.jpg)

Los recursos del proyecto en Project Operations se mantienen en Dataverse y no se sincronizan con aplicaciones de Finance and Operations.

### <a name="transaction-categories"></a>Categorías de transacciones

Las categorías de transacciones se mantienen en Dataverse y se sincronizan con aplicaciones de Finance and Operations que utilizan la asignación de tabla **Categorías de transacciones de proyecto (msdyn\_transactioncategories)**. Una vez sincronizado el registro de categoría de transacciones, el sistema automáticamente crea cuatro registros de categoría compartida. Cada registro corresponde a un tipo de transacción en aplicaciones de Finance and Operations y las vincula al registro de categoría de transacción.

![Integración de categorías de transacciones](./media/4TransactionCategories.jpg)

El uso de categorías de transacciones para estimaciones y datos reales requiere que el contable del proyecto o el administrador del sistema cree las categorías de proyecto correspondientes en cada entidad legal. Para más información, vea [Configurar categorías de proyecto](../project-accounting/configure-project-categories.md).
