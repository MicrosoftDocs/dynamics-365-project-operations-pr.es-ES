---
title: Integración de factura de proyecto
description: Este tema proporciona información sobre la integración de doble escritura de Project Operations para facturación de clientes.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581259"
---
# <a name="project-invoice-integration"></a>Integración de factura de proyecto

Este tema proporciona información sobre la integración de doble escritura de Project Operations para facturación de clientes.

En Project Operations, el jefe de proyecto administra el trabajo pendiente de facturación del proyecto y crea una factura proforma para el cliente en Microsoft Dataverse. De acuerdo con esta factura proforma, el empleado de Proveedores o el contable del proyecto crea una factura de cara al cliente. La integración de doble escritura garantiza que los detalles de la factura proforma estén sincronizados con las aplicaciones de finanzas y operaciones. Una vez que se registra la factura de cara al cliente, el sistema actualiza los datos reales del proyecto relevantes en Dataverse con el detalle de contabilidad. El siguiente gráfico proporciona una descripción conceptual de alto nivel de esta integración.

   ![Integración de factura de proyecto.](./media/DW5Invoicing.png)

Después de que el jefe de proyecto confirme la factura proforma en Dataverse, la información del encabezado de la factura proforma se sincroniza con las aplicaciones de finanzas y operaciones mediante el mapa de tabla de doble escritura **Propuesta de factura de proyecto V2 (facturas)**. Esta es una integración unidireccional de Dataverse en las aplicaciones de Finanzas y Operaciones. No se admite la creación o eliminación de propuestas de facturas de proyectos directamente en las aplicaciones de finanzas y operaciones.

La confirmación de factura en Dataverse también desencadena la lógica de negocios para crear registros relacionados con facturación en la entidad **Datos reales**. Estos registros se sincronizan con Finanzas y operaciones mediante el mapa de tablas de doble escritura **Datos reales de integración de Project Operations (msdyn\_actuals).** Para obtener más información, consulte [Estimaciones y datos reales del proyecto](resource-dual-write-estimates-actuals.md). 

Las líneas de propuestas de factura de proyecto se crean por el proceso periódico, **Importar desde tabla de almacenamiento provisional**. Este proceso se basa en los detalles reales de las ventas facturadas en la tabla **Preparación de datos reales**. Para más información, vea [Administrar propuestas de facturas de proyectos](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
