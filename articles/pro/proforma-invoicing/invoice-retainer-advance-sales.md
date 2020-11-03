---
title: Facturar a un autor de retención o anticipo
description: En este tema se proporciona información sobre cómo facturar a un autor de la retención o anticipo en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ed3b71d5f0ac035403de9fa213f3f45d14038e0
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088117"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Facturar a un autor de retención o anticipo

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Dynamics 365 Project Operations admite contratos basados en anticipos y anticipos únicos. En un contrato de proyecto, puede registrar un programa de anticipos o un anticipo único. Sin embargo, la grabación a nivel de contrato de proyecto no hace que un anticipo o anticipo esté disponible inmediatamente para su uso. Para utilizar una retención o anticipo en una factura que realmente cobra al cliente, primero se debe facturar el anticipo o anticipo.

Complete estos pasos para facturar a un autor de retención o un adelanto.

1. Seleccione **Ventas** > **Facturación** > **Retenciones y anticipos**. 
2. En la página **Anticipos y retenciones** , utilice el filtro para seleccionar el anticipo específico o avance a la factura y márquelo como **Listo para facturar**.
3. Cree una factura ya sea manualmente desde el **Contrato de proyecto** lista o página de detalles. La retención o anticipo se muestra en el borrador de la factura en la sección **Anticipos y retenciones** en la página **Factura**.
4. Confirmar la factura. Esto hará que el autor de la retención o adelanto esté disponible para su uso. Puede verificar la factura en la página de la lista **Retenciones y anticipos**. Para una retención o anticipo facturado, la cantidad disponible se muestra en la cuadrícula.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Cree una retención o adelanto desde la cuadrícula de facturas

Puede crear una retención o un anticipo directamente en una factura.

1. En un borrador de factura, en la subcuadrícula **Anticipos y retenciones** , seleccione **Nuevo** para crear un nuevo anticipo o retención. 
2. En la página **Creación rápida** , especifique la información necesaria y después seleccione **Guardar**. El anticipo o retención se crea en el contrato del proyecto relacionado con la factura. El autor de la retención o adelanto se marca automáticamente como **Listo para facturar** y se agrega a la subcuadrícula **Adelantos y retenciones** en la página **Factura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Reconciliar a un autor de retención o anticipo

Después de facturar una retención o anticipo, se pueden usar o conciliar en una factura con el tiempo, los gastos, los hitos u otros cargos basados en el proyecto. El cliente verá la cantidad de su factura reducido por el autor de la retención o la cantidad adelantada utilizado en esta factura.

En cada factura que se genera para un contrato de proyecto que ha facturado retenciones o anticipos, Project Operations aplica automáticamente la retención o anticipo a la factura.

Esto se puede ver en la cuadrícula **Retenciones y anticipos aplicados** en la página **Factura**. La siguiente tabla proporciona información sobre los campos de la cuadrícula **Anticipos y anticipos aplicados** de la página **Factura de proyecto**.

| Campo | Ubicación | Relevancia, propósito y orientación | Impacto posterior |
| --- | --- | --- | --- |
| Descripción | Cuadrícula **Retenciones y anticipos aplicados** en la página **Factura de proyecto** |Este campo de solo lectura proporciona una descripción de la retención o anticipo utilizado en esta factura. Este valor no se puede cambiar en la factura. Este valor se puede actualizar en la subcuadrícula de la página **Contrato de proyecto**. | Este campo se puede mostrar al cliente en la factura impresa para indicar qué anticipo o anticipo se aplica en la factura. |
| Entregado el | Cuadrícula **Retenciones y anticipos aplicados** en la página **Factura de proyecto**  | Este campo de solo lectura proporciona la fecha de la factura de la retención o anticipo utilizado en esta factura. Este valor no se puede cambiar en la factura. Este valor se puede actualizar en la subcuadrícula de la página **Contrato de proyecto**. | Este campo se puede mostrar al cliente en la factura impresa para indicar la fecha cuando la retención o adelanto se facturaron por primera vez al cliente. |
| Importe | Cuadrícula **Retenciones y anticipos aplicados** en la página **Factura de proyecto**  | Este campo de solo lectura proporciona la cantidad de la retención o anticipo utilizado en esta factura. Este valor no se puede cambiar en la factura. Este valor se puede actualizar en la subcuadrícula de la página **Contrato de proyecto**. | Este campo se puede mostrar al cliente en la factura impresa para indicar la cantidad original de la retención o adelanto que pagó el cliente. |
| Importe usado | Cuadrícula **Retenciones y anticipos aplicados** en la página **Factura de proyecto**  | Este campo de solo lectura proporciona el valor calculado que resume la cantidad de retención o anticipo que se ha utilizado. | Este campo se puede mostrar al cliente en la factura impresa para indicar la cantidad de esta retención o adelanto que ya se han usado. |
| Importe total | Cuadrícula **Retenciones y anticipos aplicados** en la página **Factura de proyecto**  | Este campo editable proporciona la cantidad de la retención o anticipo que se está usando en esta factura de proyecto. Esta cantidad no puede ser superior a la disponible en el anticipo. El sistema calcula automáticamente esto como la diferencia entre los campos **Cantidad** y **Cantidad usada** en la cuadrícula. Puede disminuir esta cantidad para usar menos de lo que está disponible, pero no puede aumentar la cantidad para usar más de lo que está disponible. | Este campo se puede mostrar al cliente en la factura impresa para indicar la cantidad de esta retención o adelanto que se está usando en la factura. |
| Importe del saldo de la retención. | Cuadrícula **Retenciones y anticipos aplicados** en la página **Factura de proyecto**  | Este campo de solo lectura proporciona el valor de cuánto de la retención o anticipo quedará después de que se confirme la factura. | Este campo se puede mostrar al cliente en la factura impresa para indicar la cantidad que quedará de esta retención o adelanto después de que se confirme y pague la factura. |
