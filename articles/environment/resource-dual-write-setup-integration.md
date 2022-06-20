---
title: Integración de datos de instalación y configuración de Project Operations
description: Este artículo proporciona información sobre la instalación y configuración de mapas de escritura dual de Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914561"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integración de datos de instalación y configuración de Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo proporciona información sobre la instalación e integración de escritura dual de Project Operations para entidades de instalación y configuración.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratos de proyecto, líneas de contrato y proyectos

Los contratos de proyecto, las líneas de contrato y los proyectos se crean en Dataverse y se sincronizan con las aplicaciones de Finanzas y operaciones para contabilidad adicional. Los registros de estas entidades se pueden crear y eliminar solo en Dataverse. Sin embargo, los atributos contables, como los valores predeterminados del grupo de impuestos sobre las ventas y las dimensiones financieras, se pueden agregar a estos registros en las aplicaciones de Finanzas y operaciones.

  ![Conceptos de integración de contratos de proyectos.](./media/1ProjectContract.jpg)

Los prospectos de actividad de ventas, las oportunidades y las cotizaciones se rastrean en Dataverse y no se sincronizan con las aplicaciones de Finanzas y operaciones porque no hay contabilidad posterior asociada con esta actividad.

La funcionalidad del contrato de proyecto en Dataverse crea un registro de contrato de proyecto en aplicaciones de Finanzas y operaciones mediante el mapa de tabla **Encabezados de contrato de proyecto (pedidos de ventas)**. Al guardar un contrato de proyecto en Dataverse también se inicia la creación de un registro de entidad de cliente de contrato de proyecto. Este registro se sincroniza con las aplicaciones de Finanzas y operaciones mediante el mapa de tabla **Fuente de financiación del proyecto (msdyn\_projectcontractssplitbillingrules)**. Esta asignación también sincroniza las adiciones, actualizaciones y eliminaciones de clientes de contratos de proyectos. Los porcentajes de facturación divididos entre clientes de contrato de proyecto se controlan solo en Dataverse y no se sincronizan con las aplicaciones de Finanzas y operaciones.

Después de crear un contrato de proyecto en Dataverse, el contable del proyecto puede actualizar los atributos contables de este contrato de proyecto en las aplicaciones Finanzas y operaciones, yendo a **Gestión de proyectos y contabilidad** > **Contratos de proyecto** > **Configurar** > **Mostrar contabilidad predeterminada**. El contador puede revisar los atributos del contrato del proyecto operativo, como la fecha de entrega solicitada y el importe del contrato, seleccionando el id. del contrato del proyecto en las aplicaciones de Finanzas y operaciones, que abre el registro del contrato del proyecto relacionado en Dataverse.

La entidad del proyecto se sincroniza con las aplicaciones de Finanzas y operaciones mediante el mapa de tabla **Proyectos V2 (msdyn\_projects)**. El contable del proyecto puede:

  - Revise los proyectos en las aplicaciones de Finanzas y operaciones yendo a **Gestión de proyectos y contabilidad** > **Todos los proyectos**. 
  - Actualice los atributos de contabilidad del proyecto en las aplicaciones de Finanzas y operaciones yendo a **Gestión de proyectos y contabilidad** > **Todos los proyectos** > **Configurar** > **Mostrar contabilidad predeterminada**.  
  - Revise los atributos del proyecto operativo, como las fechas estimadas de inicio y finalización, seleccionando el id. del proyecto en las aplicaciones de Finanzas y operaciones, que abre el registro del proyecto relacionado en Dataverse.

Un proyecto está asociado con un contrato de proyecto a través de la entidad **Línea de contrato de proyecto**.

Las líneas del contrato de proyecto en Dataverse crean una regla de facturación de contrato en las aplicaciones de Finanzas y operaciones, mediante el mapa de tabla **Líneas de contrato de proyecto (salesorderdetails)**. El método de facturación define el tipo de regla de facturación del contrato del proyecto en las aplicaciones de Finanzas y operaciones:

  - Las líneas de contrato de proyecto con un método de facturación de tiempo y material crean una regla de facturación de tipo tiempo y material.
  - Las líneas de contrato del método de facturación de precio fijo crean una regla de facturación de hitos.

El contador del proyecto puede revisar las líneas de contrato del proyecto en las aplicaciones de Finanzas y operaciones yendo a **Gestión de proyectos y contabilidad** > **Contratos de proyecto** > **Configurar** > **Mostrar contabilidad predeterminada**, y revisando los detalles en la pestaña **Líneas de contrato**. El contable también puede establecer dimensiones financieras predeterminadas para las líneas de contrato del método de facturación de precio fijo en esta pestaña.

## <a name="billing-milestones"></a>Hitos de facturación

Las líneas de contrato de proyecto que utilizan el método de facturación de precio fijo se facturan a través de hitos de facturación. Los hitos de facturación se sincronizan con las transacciones a cuenta del proyecto en las aplicaciones de Finanzas y operaciones mediante el mapa de tabla **Hitos de línea de contrato de integración de Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integración de hitos de facturación.](./media/2Milestones.jpg)

El contable puede revisar las transacciones a cuenta y ajustar los atributos de contabilidad para esas transacciones yendo a **Administración y contabilidad de proyectos** > **Contratos de proyecto** > **Mantener** > **Transacciones a cuenta** o **Administración y contabilidad de proyectos** > **Todos los proyectos** > **Mantener** > **Transacciones a cuenta**.

Cuando crea por primera vez un hito de facturación para una línea de contrato de proyecto determinada, el sistema crea automáticamente un proyecto de estimación de ingresos de precio fijo para el proyecto asociado con esta línea de contrato. Los proyectos de estimación de ingresos de precio fijo se pueden revisar yendo a **Administración y contabilidad de proyectos** > **Proyectos de estimación de ingresos a precio fijo**.

### <a name="project-tasks"></a>Tareas de proyecto

Las tareas del proyecto se sincronizan con las aplicaciones de Finanzas y operaciones a través del mapa de tabla **Tareas del proyecto (msdyn\_projecttasks)** solo con fines de referencia. Las operaciones de creación, actualización y eliminación no se admiten a través de las aplicaciones de finanzas y operaciones.

  ![Integración de tareas de proyecto.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de proyecto

La entidad **Roles de recursos del proyecto** se sincroniza con las aplicaciones de Finanzas y operaciones mediante el mapa de tabla **Roles de recursos del proyecto para todas las empresas (bookableresourcecategories)** solo con fines de referencia. Debido a que los roles de recursos en Dataverse no son específicos de la empresa, el sistema crea automáticamente los respectivos registros de funciones de recursos específicos de la empresa en las aplicaciones de Finanzas y operaciones, automáticamente para todas las entidades jurídicas incluidas en el ámbito de integración de doble escritura.

![Integración de roles de recursos.](./media/5Resources.jpg)

Los recursos del proyecto en Project Operations se mantienen en Dataverse y no están sincronizados con las aplicaciones de Finanzas y operaciones.

### <a name="transaction-categories"></a>Categorías de transacciones

Las categorías de transacciones se mantienen en Dataverse y se sincronizan con las aplicaciones de Finanzas y operaciones mediante el mapa de tabla **Categorías de transacciones de proyectos (msdyn\_transactioncategories)**. Una vez sincronizado el registro de categoría de transacciones, el sistema automáticamente crea cuatro registros de categoría compartida. Cada registro corresponde a un tipo de transacción en las aplicaciones de Finanzas y operaciones y los vincula al registro de categoría de transacción.

![Integración de categorías de transacciones.](./media/4TransactionCategories.jpg)

El uso de categorías de transacciones para estimaciones y datos reales requiere que el contable del proyecto o el administrador del sistema cree las categorías de proyecto correspondientes en cada entidad legal. Para más información, vea [Configurar categorías de proyecto](../project-accounting/configure-project-categories.md).
