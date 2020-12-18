---
title: Creación de un anticipo ad hoc en un contrato
description: Este tema proporciona información sobre cómo crear un anticipo en un contrato según sea necesario.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 790a0281f72eff5f241d11da025b5b4af643a567
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596033"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Creación de un anticipo ad hoc en un contrato

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Microsoft Dynamics 365 Project Operations admite escenarios de facturación que implican pagos anticipados y anticipos. El proceso de uso de **Avances** en **Project Operations** es parecido a los contratos de **Anticipo**. 

Complete los siguientes pasos para facturar al cliente un anticipo.

1. Vaya a la página **Contrato de proyecto** y luego seleccione la pestaña **Anticipos y retenciones**.
2. En la subcuadrícula que enumera todos los anticipos y prepagos registrados anteriormente, seleccione **+ Retenedor de contrato de nuevo proyecto**. 

    El formulario **Creación rápida** se abre para registrar un pago por adelantado o un anticipo.
    
3. La siguiente tabla enumera los campos para registrar un avance y las consideraciones a tener en cuenta al crear nuevos:

    | Campo | Descripción | Impacto posterior |
    | --- | --- | --- |
    | **Cliente de contrato de proyecto** | Este campo indica a qué cliente del contrato se le facturará este anticipo. | Si tiene varios clientes en el contrato y desea facturar a cada uno de ellos por un anticipo o monto de anticipo específico, cree un anticipo para cada cliente individualmente. |
    | **Descripción** | La descripción del propósito o el momento del avance para ayudar a identificar este avance. | Esta descripción se muestra en la línea de la factura de este anticipo. |
    | **Importe** | El importe del prepago o anticipo. | Este importe se muestra en la línea de la factura de este anticipo. |
    | **Fecha de factura** | La fecha en la que se factura este anticipo al cliente. | Esta es la fecha para que el proceso automatizado de creación de facturas cree una línea de factura para este anticipo. |
    | **Estado de la factura** | Esta es una configuración de opción que indica si este anticipo se agrega a un borrador de factura para este cliente. Los valores posibles son:</br>- **No listo para facturar**</br>- **Listo para facturar** | Cuando un anticipo o prepago se marca como **Listo para facturar**, se agrega como un tiempo de línea en un borrador de factura. Solo se puede utilizar un anticipo facturado en su totalidad para conciliar los costos del proyecto para el próximo período de facturación. |

4. Seleccione **Guardar y cerrar** en el cuadro de diálogo de creación rápida para registrar el anticipo o el prepago.
