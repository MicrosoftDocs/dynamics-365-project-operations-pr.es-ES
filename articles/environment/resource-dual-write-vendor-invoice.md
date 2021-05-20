---
title: Integración de facturas de proveedores
description: Este tema proporciona información sobre la integración de facturas del proveedor en Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955842"
---
# <a name="vendor-invoice-integration"></a>Integración de facturas de proveedores

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las adquisiciones relacionadas con el proyecto en Dynamics 365 Project Operations se pueden registrar en **Proveedores** > **Facturas** > **Facturas de proveedor pendientes** y utilizando un documento de factura de proveedor pendiente. Para más información, vea [Adquirir materiales no mantenidos en existencias utilizando una factura de proveedor pendiente](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Antes de utilizar la funcionalidad descrita en este tema, revise y aplique las configuraciones necesarias. Para más información, vea [Habilitar materiales no mantenidos en existencias y facturas de proveedor pendiente](../procurement/configure-materials-nonstocked.md).

En Project Operations, las facturas de proveedores relacionadas con el proyecto se registran mediante reglas de contabilización especiales:

- El coste relacionado con el proyecto (incluido el impuesto no recuperable) no se registra inmediatamente en la cuenta de costes del proyecto del libro mayor. En cambio, el coste se contabiliza en la **Cuenta de integración de adquisiciones**. Esta cuenta se configura en **Administración y contabilidad de proyectos** > **Configuración** > **Parámetros de administración y contabilidad de proyectos** en la pestaña **Project Operations en Dynamics 365 Customer engagement**.
- La doble escritura sincroniza los detalles de la factura del proveedor con Microsoft Dataverse utilizando las siguientes asignaciones de tabla:

     - **Entidad de exportación de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoices)**: Esta asignación de tabla sincroniza la información de encabezado de la factura del proveedor. Solo las facturas de proveedor con al menos una línea que contiene un ID de proyecto se sincronizan con Dataverse.
     - **Entidad de exportación de línea de facturas de proveedores de proyectos de integración de Project Operations (msdyn_projectvendorinvoices)**: Esta asignación de tabla sincroniza la información de línea de la factura del proveedor. Solo las líneas que contienen un ID de proyecto se sincronizan con Dataverse.

     > [!NOTE]
     > Los detalles de la factura del proveedor en Dataverse no son editables.

La subcontabilidad de impuestos, la subcontabilidad de proveedores y otras contabilizaciones financieras se registran según corresponda en Dynamics 365 Finance cuando se contabiliza la factura del proveedor.

![Integración de facturas de proveedores](media/DW7VendorInvoice.png)

Cuando los registros se escriben en una entidad **Factura del proveedor** en Dataverse, comienza un proceso de aprobación automatizado de los registros. Si es necesario, el estado del proceso de aprobación automatizado se puede revisar en Dataverse yendo a **Configuración avanzada** > **Sistema** > **Trabajos del sistema**. Una vez completada la aprobación, el sistema crea registros de clases de transacciones de material en la entidad **Datos reales**.

Los datos reales relacionados con material se procesan utilizando la asignación de tabla de doble escritura, **Datos reales de integración de Project Operations (msdyn_actuals)**. Para obtener más información, consulte [Estimaciones y datos reales del proyecto](resource-dual-write-estimates-actuals.md).

El proceso periódico **Importar desde tabla de almacenamiento provisional** crea líneas del diario de integración de Project Operations relacionadas con la factura del proveedor. La cuenta de contrapartida tiene como valor predeterminado la cuenta de integración de adquisiciones. Cuando se registra el diario de integración, el saldo de la cuenta se borra para la transacción de la factura del proveedor y el importe de la línea se mueve a la cuenta de coste del proyecto. Las transacciones de subcontabilidad del proyecto también se crean para fines de facturación descendente y reconocimiento de ingresos.
