---
title: Integración de factura de proyecto
description: Este tema proporciona información sobre la integración de doble escritura de Project Operations para facturación de clientes.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955839"
---
# <a name="project-invoice-integration"></a>Integración de factura de proyecto

Este tema proporciona información sobre la integración de doble escritura de Project Operations para facturación de clientes.

En Project Operations, el jefe de proyecto administra el trabajo pendiente de facturación del proyecto y crea una factura proforma para el cliente en Microsoft Dataverse. De acuerdo con esta factura proforma, el empleado de Proveedores o el contable del proyecto crea una factura de cara al cliente. La integración de doble escritura garantiza que los detalles de la factura proforma se sincronizan con aplicaciones de Finance and Operations. Una vez que se registra la factura de cara al cliente, el sistema actualiza los datos reales del proyecto relevantes en Dataverse con el detalle de contabilidad. El siguiente gráfico proporciona una descripción conceptual de alto nivel de esta integración.

   ![Integración de factura de proyecto](./media/DW5Invoicing.png)

Cuando el jefe del proyecto confirma la factura proforma en Dataverse, la información de encabezado de la factura proforma se sincroniza con aplicaciones de Finance and Operations que utilizan la asignación de tabla de doble escritura, **Propuesta de factura de proyecto V2 (facturas)**. Esta es una integración unidireccional de Dataverse con aplicaciones de Finance and Operations. No es posible crear o eliminar propuestas de factura de proyecto directamente en las aplicaciones de Finance and Operations.

La confirmación de factura en Dataverse también desencadena la lógica de negocios para crear registros relacionados con facturación en la entidad **Datos reales**. Estos registros se sincronizan con aplicaciones de Finance and Operations que utilizan la asignación de tabla de doble escritura **Datos reales de integración de Project Operations (msdyn\_actuals).** Para obtener más información, consulte [Estimaciones y datos reales del proyecto](resource-dual-write-estimates-actuals.md). 

Las líneas de propuestas de factura de proyecto se crean por el proceso periódico, **Importar desde tabla de almacenamiento provisional**. Este proceso se basa en los detalles reales de las ventas facturadas en la tabla **Preparación de datos reales**. Para más información, vea [Administrar propuestas de facturas de proyectos](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
