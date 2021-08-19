---
title: Versiones de asignaciones de doble escritura para Project Operations
description: Este tema proporciona la lista de asignaciones de doble escritura necesarios para Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c8bc389c83eaf2a7720ef3fa969c677eed11e7959199b5f0083df5bf3b43ea43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003837"
---
# <a name="project-operations-dual-write-map-versions"></a>Versiones de asignaciones de doble escritura para Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

El uso de Dynamics 365 Project Operations para escenarios de recursos/no mantenidos en existencias requiere un conjunto de asignaciones de doble escritura que se ejecuten en el entorno. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Asignaciones de requisitos previos: solución de orquestación de doble escritura

Las siguientes asignaciones son requisitos previos necesarios para la solución Project Operations. Asegúrese de ejecutar las asignaciones enumeradas en la siguiente tabla y cualquier asignación de tabla relacionada en su entorno.

| Asignación de tabla | Sincronización inicial |
| --- | --- |
| Libro mayor (msdyn_ledgers) | Requiere sincronización inicial para el mapa de asignación y todos los requisitos previos. El maestro para sincronización inicial es aplicaciones de Finance and Operations. |
| Entidades legales (cdm_companies) | No necesario. El sistema completa esta entidad automáticamente cuando los entornos están vinculados mediante doble escritura. |
| Clientes V3 (accounts) | No es necesario para aprovisionamiento. |
| Proveedores V2 (msdyn_vendors) | No es necesario para aprovisionamiento. |

1. En la lista de mapas, seleccione la asignación Contabilidad **(msdyn\_ledgers)** con todos los requisitos previos y active la casilla **Sincronización inicial**. En el campo **Maestro para sincronización inicial**, seleccione **aplicaciones de Finance and Operations** tanto para la asignación de contabilidad como para todas las asignaciones de requisitos previos. Seleccione **Ejecutar**.

![Sincronización de asignaciones de contabilidad.](media/DW6.png)

2. Siga los mismos pasos para todas las asignaciones de tabla restantes enumeradas en la tabla anterior. No seleccione la casilla **Sincronización inicial** al ejecutar esas asignaciones.

## <a name="project-operations-dual-write-maps"></a>Asignaciones de doble escritura de Project Operations

Las siguientes asignaciones se requieren para una solución de Project Operations. Las versiones de mapas de doble escritura se enumeran a partir de la actualización de Project Operations de mayo de 2021, versión 4.10.0.186.

| **Asignación de entidad** | **Versión más reciente** | **Sincronización inicial** |
| --- | --- | --- |
| Entidad de integración para las relaciones de transacciones del proyecto (msdyn\_transactionconnections) | 1.0.0.0 | No es necesario para aprovisionamiento. |
| Encabezados de contrato de proyecto (pedidos de venta) | 1.0.0.1 | No es necesario para aprovisionamiento. |
| Líneas de contrato de proyecto (detalles de pedidos de ventas) | 1.0.0.0 | No es necesario para aprovisionamiento. |
| Origen de financiación del proyecto (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | No es necesario para aprovisionamiento. |
| Tabla de integración de Project Operations para estimaciones de materiales (msdyn\_estimatelines) | 1.0.0.0 | No es necesario para aprovisionamiento. |
| Propuestas de factura de proyecto V2 (invoices) | 1.0.0.3 | No es necesario para aprovisionamiento. |
| Datos reales de integración de Project Operations (msdyn_actuals) | 1.0.0.14 | No es necesario para aprovisionamiento. |
| Hitos de la línea de contrato de integración de Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | No es necesario para aprovisionamiento. |
| Entidad de integración de Project Operations para estimaciones de gastos (msdyn_estimateslines) | 1.0.0.2 | No es necesario para aprovisionamiento. |
| Entidad de integración de Project Operations para estimaciones de tiempo (msdyn_resourceassignments) | 1.0.0.5 | No es necesario para aprovisionamiento. |
| Entidad de exportación de categorías de gastos de proyecto de integración de Project Operations (msdyn_expensecategories) | 1.0.0.1 | No es necesario para aprovisionamiento. |
| Entidad de exportación de gastos de proyecto de integración de Project Operations (msdyn_expenses) | 1.0.0.2 | No es necesario para aprovisionamiento. |
| Entidad de exportación de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | No es necesario para aprovisionamiento. |
| Entidad de exportación de línea de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.1 | No es necesario para aprovisionamiento. |
| Roles de recursos del proyecto para todas las empresas (bookableresourcecategories) | 1.0.0.1 | Requiere una sincronización inicial para la asignación de tablas para sincronizar los roles de recursos de Jefe de proyecto y Miembro del equipo que se rellenan en el entorno de Dynamics 365 Dataverse durante el aprovisionamiento. Dataverse es el origen principal de la sincronización inicial. |
| Tareas del proyecto (msdyn_projecttasks) | 1.0.0.4 | No es necesario para aprovisionamiento. |
| Categorías de transacciones de proyectos (msdyn_transactioncategories) | 1.0.0.0 | No es necesario para aprovisionamiento. |
| Proyectos V2 (msdyn_projects) | 1.0.0.2 | No es necesario para aprovisionamiento. |

Complete los siguientes pasos para ejecutar las asignaciones enumeradas.

1. Habilite los roles de recursos del proyecto para la asignación de tabla **todas las empresas (bookableresourcecategories)** ya que esta asignación requiere la sincronización inicial. En el campo **Maestro para sincronización inicial**, seleccione **Common Data Service**. 

 ![Sincronización de asignaciones de tabla de roles de recursos.](media/6ResourceInitialSync.jpg)

 Espere hasta que el estado de la asignación sea **Ejecutando** antes de pasar al siguiente paso.

2. Seleccione todas las asignaciones requeridas restantes. Puede filtrarlas en la lista de asignación de doble escritura usando la palabra clave, **Proyecto** en la búsqueda en la esquina superior derecha. Puede realizar una selección múltiple de todas las asignaciones y luego ejecutarlas. Para más información, vea [Administrar múltiples asignaciones de tablas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Asegúrese de habilitar y ejecutar también asignaciones de entidades relacionadas.

### <a name="project-operations-dual-write-map-versions"></a>Versiones de asignaciones de doble escritura para Project Operations

Ejecute siempre la última versión de la asignación en su entorno. Es posible que algunas funciones y capacidades no funcionen correctamente si se presenta alguna de las siguientes condiciones:

- Una asignación no está activada.
- La última versión de la asignación no está activada. 
- Las asignaciones de tabla relacionadas no están activadas.

Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Puede activar una nueva versión de la asignación seleccionando **Versiones de asignación de tabla**, seleccionando la última versión y luego guardando la versión seleccionada. Si ha personalizado un mapa de asignación lista para usar, deberá volver a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
