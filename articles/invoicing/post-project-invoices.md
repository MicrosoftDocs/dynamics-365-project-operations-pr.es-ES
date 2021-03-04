---
title: Información general sobre el proceso de facturación
description: Este tema proporciona información general sobre el proceso de facturación en Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089307"
---
# <a name="invoicing-process-overview"></a>Información general sobre el proceso de facturación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Project Operations para escenarios basados en recursos/no mantenidos en existencias ofrecen funciones integrales diseñadas para satisfacer las necesidades tanto del jefe de proyecto como del empleado o contable de proyecto del cliente. Para el proceso de facturación, el jefe de proyecto administra el trabajo pendiente de facturación del proyecto y el empleado o contable de proyecto del cliente crea un documento de factura para el cliente que cumple con los requisitos y es preciso.

![Diagrama de flujo de facturación](./media/invoicing-flow.png)

La línea del contrato del proyecto define el método de facturación para las transacciones de proyecto asociadas. Cuando el jefe de proyecto aprueba las transacciones de tiempo y gastos, el sistema registra las transacciones en la entidad **Datos reales del proyecto** y envía la información al módulo **Gestión de proyectos y contabilidad** en Dynamics 365 Finance. A continuación, el contable del proyecto revisa y contabiliza los registros a través del [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). Este diario incluye detalles contables importantes para los datos reales del proyecto, como los de facturación, grupo de impuestos, grupo de impuestos de artículos de facturación y dimensiones financieras.

El jefe de proyecto puede revisar las transacciones de ventas no facturadas mediante el método de facturación de tiempo y material en [Trabajo pendiente de facturación de tiempo y material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) y la facturación de precio fijo en [Hitos de precio fijo](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Estas vistas permiten filtrar y seleccionar transacciones que hay que incluir en el siguiente ciclo de facturación, y marcarlas a continuación como **Listo para facturar**.

Puede [crear manualmente una factura proforma](../proforma-invoicing/create-manual-proforma-invoice.md) o usar un [proceso periódico](../proforma-invoicing/configure-automated-invoice-creation.md). El jefe de proyecto puede [ajustar un borrador de factura proforma](../proforma-invoicing/manage-proforma-invoice.md) si es necesario, y confirmarlo a continuación.

La factura proforma confirmada se envía al módulo **Gestión de proyectos y contabilidad** de Finance. El contable del proyecto formatea y actualiza la propuesta de factura del proyecto y después registra e imprime el documento. Las facturas de proyecto contabilizadas se registran en la contabilidad general, así como en los subdiarios del cliente y del proyecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]