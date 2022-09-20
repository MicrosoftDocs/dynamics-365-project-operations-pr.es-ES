---
title: Crear facturas de proveedor
description: Este artículo describe el concepto de facturas de proveedores y explica cómo crearlas en Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475437"
---
# <a name="create-vendor-invoices"></a>Crear facturas de proveedor

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Para utilizar la funcionalidad que se describe en este artículo, debe habilitar la característica **Habilitar el procesamiento de datos reales de subcontratación con Project Operations para escenarios basados en recursos** en el espacio de trabajo **Administración de características**.

La facturación de proveedores en Microsoft Dynamics 365 Project Operations se puede utilizar para registrar los costes de las entregas de servicios y/o materiales en un proyecto completado por proveedores.

Cuando se subcontratan servicios y/o materiales a un proveedor, un subcontrato representa el acuerdo contractual con ese proveedor. A medida que el proveedor presta los servicios, o los materiales se reciben y utilizan en las tareas del proyecto, los costes se registran en el proyecto. A continuación, el proveedor envía facturas periódicamente. Esas facturas se verifican y se comparan con los costes que se registran en el proyecto. Una vez que se completa el proceso de verificación, la factura del proveedor se confirma y se pasa para el pago.

## <a name="scenarios-for-use"></a>Escenarios a utilizar

Las facturas de proveedores en Project Operations se pueden usar para admitir dos escenarios distintos:

- Los clientes utilizan las experiencias completas de subcontratación.
- Los clientes no utilizan las experiencias completas de subcontratación, pero desean tener una vista unificada de los costes de los proyectos en Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Los clientes utilizan las experiencias completas de subcontratación

Las experiencias de facturas de proveedores proporcionan una forma de verificar entradas de tiempo, uso de materiales y entradas de gastos que hacen referencia a componentes subcontratados y hacerlas coincidir con líneas de facturas de proveedores. Este proceso se puede utilizar para verificar la precisión de las líneas de factura del proveedor. Una vez que se completa el proceso de verificación y se confirma la factura del proveedor, el sistema revertirá los datos reales registrados por los registros de tiempo, gastos y uso de materiales aprobados, y después creará nuevos datos reales de costes utilizando las líneas de factura del proveedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Los clientes no utilizan las experiencias completas de subcontratación, pero desean tener una vista unificada de los costes de los proyectos en Project Operations

Si realiza un seguimiento del proceso de subcontratación en un sistema de terceros, puede registrar los costes de ese sistema de terceros en Project Operations mediante la creación de facturas de proveedores que no hagan referencia a subcontratos. De esta manera, sus gerentes de proyecto pueden tener una vista única y unificada de todos los costes en un proyecto determinado.

## <a name="create-vendor-invoices-in-project-operations"></a>Crear facturas de proveedores en Project Operations

Las facturas de los proveedores se crean en Dynamics 365 Finance, utilizando el módulo **Proveedores**. No puede crear facturas de proveedores directamente en Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configurar verificación de factura de proveedor

Si la factura del proveedor está destinada a una subcontratación en Dataverse, debe habilitar el parámetro **Se requiere confirmación manual del PM**. La configuración de la opción determina si la factura del proveedor debe ser confirmada automáticamente en Dataverse, o si requiere una confirmación manual. El encabezado de cada factura de proveedor de proyectos incluye una opción con el mismo nombre. De forma predeterminada, la opción en el encabezado de todas las facturas de proveedores del proyecto se establece en el valor que establezca aquí. Sin embargo, puede actualizar el valor según sea necesario en el encabezado de las facturas de proveedores individuales.

Si la opción está configurada en **Sí**, la factura de proveedor que se crea en Finance y se sincroniza con Dataverse tiene el estado **Borrador**. A continuación, la factura debe ser validada y verificada por el director del proyecto, y confirmada, antes de ser procesada y contabilizada en las cuentas específicas del proyecto y del libro mayor en Finance.

Si la opción se ajusta en **No**, la factura del proveedor se confirma automáticamente. No tiene que hacer nada más.

Para configurar la verificación de facturas de proveedor, siga estos pasos:

1. En Finance, vaya a **Gestión y contabilidad de proyectos** \> **Configuración** \> **Parámetros de gestión de proyectos y contabilidad**.
1. En la pestaña **Actividades financieras**, ajuste la opción **Se requiere confirmación manual del PM** en **Sí** si la política de la empresa requiere la verificación de las facturas de los proveedores subcontratados. Si la verificación por parte del director del proyecto no es necesaria en Dataverse, deje la opción ajustada en **No**. De forma predeterminada, la configuración se utilizará en la página **Factura del proveedor pendiente**.

> [!NOTE]
> Las facturas de los proveedores que se crean para los subcontratos en Dataverse solo pueden procesarse correctamente si la opción **Se requiere confirmación manual del PM** está ajustada en **Sí**. Los costes reales de tiempo, material y gastos que crean los subcontratistas pueden cotejarse manualmente con las líneas de factura de los proveedores por el director del proyecto sólo si esta opción está establecida en **Sí**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configurar una cuenta de integración de adquisiciones para las facturas de los proveedores

Cuando se contabiliza una factura de proveedor en Finance para Project Operations - Entorno integrado (no está en stock), las finanzas se contabilizan en la cuenta de integración de adquisiciones. El sistema genera los datos reales en Dataverse para la factura registrada. Estos datos reales se registran en Finance mediante el diario de integración de proyectos. El registro del diario de integración del proyecto contabiliza el coste real y anula la cuenta de integración de aprovisionamiento.

Para configurar una cuenta de integración de adquisiciones para las facturas de los proveedores, siga estos pasos.

1. En Finance, vaya a **Gestión y contabilidad de proyectos** \> **Configuración** \> **Parámetros de gestión de proyectos y contabilidad**.
1. En la pestaña **Project Operations en Dynamics 365 Customer Engagement**, seleccione **Materiales** \> **Cuenta de integración de adquisiciones**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Crear y contabilizar las facturas de los proveedores subcontratados

Cuando un empleado de proveedores recibe una factura del subcontratista, se crea una nueva factura en Finance.

1. En Finance, vaya a **Proveedores** \> **Facturas** \> **Facturas de proveedor abiertas**.
1. En el **Panel de acciones**, seleccione **Nuevo** para crear una factura de proveedor
1. En el encabezado de la factura, en el campo **Cuenta de factura**, seleccione **Subcontratista**.
1. Seleccione la fecha de factura.
1. En la pestaña **Encabezado**, ajuste la opción **Se requiere confirmación manual del PM** en **Sí**. La configuración por defecto de esta opción procede de la página **Parámetros de gestión de proyectos y contabilidad**. Sin embargo, se puede cambiar a nivel de factura de proveedor.
1. En la ficha desplegable **Línea de factura**, seleccione **Agregar línea** para crear una línea de factura de proveedor.
1. Seleccione la categoría de adquisiciones que se creó para las líneas de subcontratación e introduzca el precio unitario, la unidad de medida y la cantidad.
1. En la sección de líneas de factura del proveedor, en la pestaña **Proyecto**, seleccione el proyecto con el que el subcontratista comparte la factura de subcontratación.
1. Seleccione la categoría del proyecto. Puede ser de cualquier tipo de **Artículo**, **Gasto**, **Materiales** u **Horas**.
1. Seleccione el rol solo si la categoría de proyecto seleccionada es del tipo **Hora**.
1. Seleccione **Registrar** para registrar la factura del proveedor.

Alternativamente, para crear una factura de proveedor vaya a **Proveedores** \> **Facturas** \> **Facturas de proveedor abiertas** y seleccione **Nuevo**.

Cuando se contabiliza la factura del proveedor, esta pasa a estar disponible en Dataverse para su verificación y procesamiento por parte del administrador de proyectos.

## <a name="vendor-invoice-processing-in-dataverse"></a>Procesamiento de facturas de proveedor en Dataverse

En la factura de proveedor que se crea en Dataverse, algunos valores de campo proceden de la factura de proveedor que se registra en Finance. Otros valores son valores predeterminados que provienen del subcontrato.

Los siguientes campos y registros relacionados se copiarán del subcontrato al encabezado de la factura del proveedor:

- Moneda
- Unidad de contratación
- Condiciones de pago

En las líneas de factura del proveedor, Project Operations usa los siguientes valores de campo para ingresar el subcontrato predeterminado y la referencia de línea de subcontrato:

- Clase de transacción
- Role
- Categoría de transacción
- Campos de productos
- Project
- Task

> [!NOTE]
> Las líneas de subcontrato de precio fijo no se admiten en Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
