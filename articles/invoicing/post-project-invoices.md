---
title: Información general sobre el proceso de facturación
description: Este tema proporciona información general sobre el proceso de facturación en Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369037"
---
# <a name="invoicing-process-overview"></a>Información general sobre el proceso de facturación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Project Operations para escenarios basados en recursos/no mantenidos en existencias ofrecen funciones integrales diseñadas para satisfacer las necesidades tanto del jefe de proyecto como del empleado o contable de proyecto del cliente. Para el proceso de facturación, el jefe de proyecto administra el trabajo pendiente de facturación del proyecto y el empleado o contable de proyecto del cliente crea un documento de factura para el cliente que cumple con los requisitos y es preciso.

![Diagrama de flujo de facturación](./media/invoicing-flow.png)

La línea del contrato del proyecto define el método de facturación para las transacciones de proyecto asociadas. Cuando el jefe de proyecto aprueba las transacciones de tiempo y gastos, el sistema registra las transacciones en la entidad **Datos reales del proyecto** y envía la información al módulo **Gestión de proyectos y contabilidad** en Dynamics 365 Finance. A continuación, el contable del proyecto revisa y contabiliza los registros a través del [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). Este diario incluye detalles contables importantes para los datos reales del proyecto, como los de facturación, grupo de impuestos, grupo de impuestos de artículos de facturación y dimensiones financieras.

El jefe de proyecto puede revisar las transacciones de ventas no facturadas mediante el método de facturación de tiempo y material en [Trabajo pendiente de facturación de tiempo y material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) y la facturación de precio fijo en [Hitos de precio fijo](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Estas vistas le permiten filtrar y seleccionar transacciones que deben incluirse en el siguiente ciclo de facturación y luego marcarlas como **Listo para facturar**.

Puede [crear manualmente una factura proforma](../proforma-invoicing/create-manual-proforma-invoice.md) o usar un [proceso periódico](../proforma-invoicing/configure-automated-invoice-creation.md). El jefe de proyecto puede [ajustar un borrador de factura proforma](../proforma-invoicing/manage-proforma-invoice.md) si es necesario, y confirmarlo a continuación.

La factura proforma confirmada se envía al módulo **Gestión de proyectos y contabilidad** de Finance. El contable del proyecto formatea y actualiza la propuesta de factura del proyecto y después registra e imprime el documento. Las facturas del proyecto publicadas se registran en el libro mayor, así como en los libros auxiliares del cliente y del proyecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]