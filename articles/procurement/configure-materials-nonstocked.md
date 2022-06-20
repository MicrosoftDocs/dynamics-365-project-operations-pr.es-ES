---
title: Configurar materiales no mantenidos en existencias y facturas de proveedor pendientes
description: Este artículo explica cómo habilitar materiales no almacenados y facturas de proveedores pendientes.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6473ef3510f0d3641a2d61b6a1b1f28980993277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913779"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Configurar materiales no mantenidos en existencias y facturas de proveedor pendientes

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

## <a name="minimum-version-requirement"></a>Versión mínima requerida

El uso de materiales no mantenidos en existencias y facturas de proveedor pendientes para escenarios basados en recursos/no mantenidos en existencias de Dynamics 365 Project Operations requiere las siguientes versiones:

Soluciones Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 o superior
- Solución de orquestación de aplicaciones de doble escritura: 2.2.2.23 o superior

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) o superior. Asegúrese de que su entorno de Finance esté actualizado y de que se apliquen todas las actualizaciones de calidad para cumplir los requisitos mínimos de la versión.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Ejecute asignaciones de doble escritura para integración de materiales no mantenidos en existencias y facturas de proveedores

Esta sección proporciona información sobre las asignaciones necesarias para los materiales no mantenidos en existencias y las facturas de proveedores. Verifique que los mapas de requisitos previos enumerados en el artículo [Aprovisionar un nuevo entorno](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) se están ejecutando en su entorno.

1. Vaya a Lifecycle Services (LCS), hasta su proyecto LCS y vaya a la página **Detalles del entorno**.
2. En la sección **Información del entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones**. Después de seleccionar el vínculo, se le redirigirá a la lista de entidades de las asignaciones.
3. Asegúrese de que se estén ejecutando las siguientes asignaciones. Si no se están ejecutando, inícielas y asegúrese de incluir todas las asignaciones de tablas relacionadas.

    - CDS lanzó distintos productos (productos)
    - Proveedores v2 (msdyn_vendors)
    - Tabla de Project Operations para estimaciones de materiales (msdyn_estimatelines)
    - Entidad de exportación de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoices)
    - Entidad de exportación de línea de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoicelines)
    - Datos reales de integración de Project Operations (msdyn_actuals). Asegúrese de que está ejecutando la versión de asignación 1.0.0.14 o superior. Puede ver la versión activa de la asignación en la columna **Versión** de la página **Doble escritura**. Puede activar una nueva versión de la asignación seleccionando **Versión de asignación de tabla** y luego guardando la versión seleccionada.

Si está utilizando datos de demostración estándar, es posible que también deba detener y reiniciar las siguientes asignaciones de entidad con sincronización inicial:
  - Días de pago CDS V2 (msdyn_paymentdays)
  - Programación de pagos (msdyn_paymentschedules)
  - Condiciones de pago (msdyn_paymentterms)
  - Grupos de proveedores (msdyn_vendorgroups)
  - Unidades (uom)

> [!NOTE]
> La sincronización inicial para grupos y unidades de proveedores puede fallar para algunos registros en el conjunto de datos de demostración existente. Puede ignorar los errores, ya que no le impedirán usar datos de demostración con Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Configurar requisitos previos en Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Activar el flujo de trabajo para crear cuentas basadas en la entidad del proveedor

La solución de orquestación de doble escritura proporciona [Integración maestra de proveedores](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Como requisito previo para esta característica, deben crearse datos del proveedor en la entidad **Cuentas**. Active un proceso de flujo de trabajo de plantilla para crear proveedores en la tabla **Cuentas** como se describe en [Cambiar entre diseños de proveedores](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Establecer productos que se crearán como activos

Los materiales no mantenidos en existencias deben configurarse como **Productos emitidos** en Finance. La solución de orquestación de doble escritura proporciona una [Integración predefinida de productos emitidos al Catalogo de productos de Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). De forma predeterminada, los productos de Finance se sincronizan con Dataverse en estado de borrador. Para sincronizar el producto con un estado activo para que pueda usarse directamente en documentos de uso de material o facturas de proveedor pendientes, vaya a **Sistema** > **Administración** > **Administración del sistema** > **Configuración del sistema**, y en la pestaña **Ventas**, establezca **Crear productos en estado activo** como **Sí**.

## <a name="configure-prerequisites-in-finance"></a>Configurar requisitos previos en Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Habilite la clave de característica para facturas de proveedor pendientes

Complete los siguientes pasos para habilitar la funcionalidad para agregar detalles del proyecto en líneas de factura de proveedor pendientes.

1. En Finance, vaya al área de trabajo **Administración de características**.
2. En la lista de características, busque la característica **Habilitar facturas de proveedor pendientes en Project Operations para escenarios basados en recursos/no mantenidos en existencias** y seleccione **Habilitar**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Defina grupos de categorías y categorías de proyectos para artículos.

Configure al menos un grupo de categorías para el tipo de transacción **Artículo** y al menos una categoría de proyecto que utilice este grupo. Para más información, vea [Configurar categorías de proyecto](../project-accounting/configure-project-categories.md#category-groups).

Revise los perfiles de costes e ingresos del proyecto y configure los ajustes de registro en el libro mayor para transacciones de artículos. Para más información, vea [Configurar contabilidad para proyectos facturables](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Configurar un producto fuera de catálogo

En Project Operations puede registrar estimaciones de material y uso para productos del catálogo que están configurados en el catálogo de productos publicado y para productos fuera de catálogo. El uso de productos fuera de catálogo requiere un único producto emitido que esté configurado en Finance para este propósito. Complete los siguientes pasos para configurar un producto fuera de catálogo. Repita estos pasos en cada entidad jurídica que utilice Project Operations para escenarios de recursos /no mantenidos en existencias.

1. En Finance, vaya a **Administración de información de productos** > **Productos** > **Productos emitidos** y seleccione **Nuevo**.
2. En el campo **Tipo de producto**, seleccione **Artículo** y en el campo **Subtipo de producto**, seleccione **Producto**.
3. Ingrese el número de producto (FUERA DE CATÁLOGO) y el nombre del producto (Producto fuera de catálogo).
4. Seleccione el grupo de modelos de artículo. Asegúrese de que el grupo de modelos de artículo que seleccione tenga el campo **Producto mantenido en existencias de política de inventario** establecido en **False**.
5. Seleccione valores en los campos **Grupo de artículos**, **Grupo de dimensiones de almacenamiento** y **Grupo de dimensiones de seguimiento**. Use la **Dimensión de almacenamiento** solo para **Sitio** y, en el campo **Dimensiones de seguimiento**, seleccione **Ninguna**.
6. Seleccione valores en el campo **Unidad de inventario**, **Unidad de compra** y **Unidad de ventas** y luego guarde los cambios.
7. En la pestaña **Plan**, establezca la configuración de orden predeterminada y en la pestaña **Inventario**, establezca el sitio y el almacén predeterminados.
8. Vaya a **Administración y contabilidad de proyectos** > **Configuración** > **Parámetros de administración y contabilidad de proyectos** y abra **Project Operations en Dynamics 365 Dataverse**. 
9. En la pestaña **Materiales**, en el campo **Producto fuera de catálogo**, seleccione el producto que creó.
10. En el entorno de Dataverse, en el mapa del sitio, abra la entidad **Productos** y busque el registro de producto fuera de catálogo. 
11. Abra los detalles del registro y establezca el estado del producto en **Retirado**. Este estado del producto evita que alguien utilice accidentalmente este registro directamente en estimaciones de materiales y documentos de uso.

### <a name="set-up-a-procurement-integration-account"></a>Configurar una cuenta de integración de adquisiciones

La cuenta de integración de adquisiciones se utiliza como cuenta de compensación cuando se registra una factura de proveedor pendiente con líneas atribuidas a un proyecto.

Cuando el sistema registra una factura de proveedor pendiente, esta cuenta se usa para el importe del coste del proyecto. Los detalles de la factura del proveedor se procesan en Dataverse y se crea un proyecto real correspondiente. La información del proyecto real se agrega al diario de integración de Project Operations. Cuando se registra el diario de integración, el importe se borra de la cuenta de integración de adquisiciones y se registra en el costo del proyecto.

1. Para configurar la cuenta de integración de adquisiciones, vaya a **Administración y contabilidad de proyectos** > **Configuración** > **Parámetros de administración y contabilidad de proyectos** y abra **Project Operations en Dynamics 365 Dataverse**. 
2. Seleccione la pestaña **Materiales** y seleccione un valor en el campo **Cuenta de integración de adquisiciones**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Configurar valores predeterminados de categoría de proyecto para un artículo

1. En Finance, vaya a **Administración y contabilidad de proyectos** > **Configuración** > **Parámetros de administración y contabilidad de proyectos** y abra **Project Operations en Dynamics 365 Dataverse**. 
2. En la pestaña **Valores predeterminados de categoría de proyecto**, en el campo **Artículo**, seleccione un valor. Esta categoría de proyecto se utiliza para transacciones de materiales si la categoría de proyecto no se estableció en el registro de datos reales del proyecto.
