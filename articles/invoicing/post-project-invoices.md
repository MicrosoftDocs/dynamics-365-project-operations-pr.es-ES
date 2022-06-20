---
title: Información general sobre el proceso de facturación
description: Este artículo proporciona una información general del proceso de facturación en Project Operations para escenarios basados en recursos/sin existencias.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923117"
---
# <a name="invoicing-process-overview"></a>Información general sobre el proceso de facturación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Project Operations para escenarios basados en recursos/no mantenidos en existencias ofrecen funciones integrales diseñadas para satisfacer las necesidades tanto del jefe de proyecto como del empleado o contable de proyecto del cliente. Para el proceso de facturación, el jefe de proyecto administra el trabajo pendiente de facturación del proyecto y el empleado o contable de proyecto del cliente crea un documento de factura para el cliente que cumple con los requisitos y es preciso.

![Diagrama de flujo de facturación.](./media/invoicing-flow.png)

La línea de contrato del proyecto define el método de facturación de las transacciones del proyecto asociadas. Cuando el administrador de proyecto aprueba transacciones de tiempo y gastos, el sistema registra las transacciones en la entidad **Datos reales del proyecto** y, a continuación, envía la información al módulo de **Gestión de proyectos y contabilidad** de Dynamics 365 Finance. A continuación, el contable del proyecto revisa y contabiliza los registros a través del [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). Este diario incluye detalles contables importantes para los datos reales del proyecto, como los de facturación, grupo de impuestos, grupo de impuestos de artículos de facturación y dimensiones financieras.

El jefe de proyecto puede revisar las transacciones de ventas no facturadas mediante el método de facturación de tiempo y material en [Trabajo pendiente de facturación de tiempo y material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) y la facturación de precio fijo en [Hitos de precio fijo](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Estas vistas le permiten filtrar y seleccionar transacciones que deben incluirse en el siguiente ciclo de facturación y luego marcarlas como **Listo para facturar**.

Puede [crear manualmente una factura proforma](../proforma-invoicing/create-manual-proforma-invoice.md) o usar un [proceso periódico](../proforma-invoicing/configure-automated-invoice-creation.md). El jefe de proyecto puede [ajustar un borrador de factura proforma](../proforma-invoicing/manage-proforma-invoice.md) si es necesario, y confirmarlo a continuación.

La factura proforma confirmada se envía al módulo **Gestión de proyectos y contabilidad** de Finance. El contable del proyecto formatea y actualiza la propuesta de factura del proyecto y después registra e imprime el documento. Las facturas del proyecto publicadas se registran en el libro mayor, así como en los libros auxiliares del cliente y del proyecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]