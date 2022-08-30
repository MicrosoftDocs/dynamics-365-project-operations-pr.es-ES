---
title: 'Facturación de proveedores: concepto y creación'
description: Este artículo describe el concepto de facturas de proveedores, escenarios de uso y cómo crear facturas de proveedores en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261965"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Facturación de proveedores: concepto y creación

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

La facturación de proveedores en Microsoft Dynamics 365 Project Operations se puede utilizar para registrar los costes de las entregas de servicios y/o materiales en un proyecto por parte de los proveedores.

Cuando se subcontratan servicios y/o materiales a un proveedor, un subcontrato representa el acuerdo contractual con ese proveedor. A medida que el proveedor presta los servicios, o los materiales se reciben y utilizan en las tareas del proyecto, los costes se registran en el proyecto. Periódicamente, el proveedor envía facturas que se verifican y se comparan con los costes que se registran en el proyecto. Una vez que se completa el proceso de verificación, la factura del proveedor se confirma y se pasa para el pago.

## <a name="scenarios-for-use"></a>Escenarios a utilizar

Las facturas de proveedores en Project Operations se pueden usar para admitir dos escenarios distintos.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Los clientes utilizan las experiencias completas de subcontratación

Las experiencias de facturas de proveedores proporcionan una forma de verificar y hacer coincidir entradas de tiempo, uso de materiales y entradas de gastos que hacen referencia a componentes subcontratados con líneas de facturas de proveedores. Este proceso se puede utilizar para verificar la precisión de las líneas de factura del proveedor. Una vez que se completa el proceso de verificación y se confirma la factura del proveedor, la aplicación revertirá los datos reales registrados por los registros de tiempo, gastos y uso de materiales aprobados, y creará nuevos datos reales de costes utilizando las líneas de factura del proveedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Los clientes no utilizan las experiencias completas de subcontratación, pero desean tener una vista unificada de los costes de los proyectos en Project Operations

Si realiza un seguimiento del proceso de subcontratación en un sistema de terceros, puede registrar los costes de ese sistema de terceros en Project Operations mediante la creación de facturas de proveedores que no hagan referencia a subcontratos. De esta manera, sus gerentes de proyecto pueden tener una vista única y unificada de todos los costes en un proyecto determinado.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Creación de facturas de proveedores en Project Operations

Las facturas de proveedores se pueden crear de dos maneras:

- Desde la página de lista de facturas de proveedores o la página de detalles, para una sola factura de proveedor
- Desde la página de lista de subcontratos o la página de detalles, para un solo subcontrato

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Creación desde la página de lista de facturas de proveedor o la página de detalles

1. Vaya a **Compras** \> **Facturas de proveedores**.
2. En la página de lista de facturas de proveedor o en la página de detalles de una factura de proveedor único, seleccione **Nuevo** para crear una nueva factura de proveedor.

Las facturas de proveedor que se creen de esta manera también pueden hacer referencia a un subcontrato.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Creación desde la página de lista de subcontratos o la página de detalles

1. Vaya a **Compras** \> **Subcontratos**.
2. Seleccione uno o más subcontratos.
3. En la página de lista de subcontratos o en la página de detalles de un único subcontrato, seleccione **Crear factura de proveedor** para crear una nueva factura de proveedor.

Una nueva factura de proveedor en estado **Borrador** se crea para cada subcontrato que haya seleccionado.

Las facturas de proveedor que crea de esta manera siempre hacen referencia al subcontrato del encabezado de la factura de proveedor. Cada línea del subcontrato que tenga un método de facturación de tiempo y material hará que se cree una línea en la factura del proveedor. Cada línea del subcontrato que tenga un método de facturación de precio fijo hará que se cree una línea en la factura del proveedor para cada hito de línea de subcontrato que tenga un estado de **Listo para facturar**.

Los siguientes campos y registros relacionados se copiarán del subcontrato al encabezado de la factura del proveedor:

- Proveedor.
- Las listas de precios relacionadas se copiarán en la factura del proveedor como listas de precios.
- Divisa.
- Unidad de contratación.
- Términos de pago.

Para las líneas de subcontrato de tiempo y material, los siguientes campos y registros relacionados se copiarán de la línea de subcontrato a la línea de factura del proveedor:

- Referencias de subcontrato y línea de subcontrato
- Clase de transacción
- Role
- Categoría de transacción
- Campos de productos
- Project
- Task
- Recurso que se puede reservar

Para las líneas de subcontrato de precio fijo, los siguientes campos se copiarán de la línea de subcontrato y el hito de línea de subcontrato a la línea de factura del proveedor:

- Referencias de subcontrato y línea de subcontrato.
- Clase de transacción. Por defecto, el valor será **Hito**.
- El nombre y el importe del hito se copiarán del hito de línea de subcontrato relacionado.
- El usuario podrá seleccionar un proyecto y una tarea en la línea de factura del proveedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
