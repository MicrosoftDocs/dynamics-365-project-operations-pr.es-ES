---
title: Anticipo de efectivo
description: En este tema se proporciona información sobre adelantos de efectivo.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6da50ac5611fcbd54aef8d8591ee112200468177
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276729"
---
# <a name="cash-advance"></a>Anticipo de efectivo

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Un anticipo en efectivo permite a los empleados pedir prestado dinero a su empresa antes de incurrir en gastos. Cuando se aprueba y paga un anticipo en efectivo solicitado, el empleado puede usar el dinero para los gastos comerciales en los que puede estar a punto de incurrir. 

## <a name="create-and-submit-a-cash-advance-request"></a>Crear y enviar una solicitud de anticipo en efectivo
Para crear un nuevo anticipo en efectivo y enviar una solicitud de anticipo en efectivo, haga lo siguiente: 

1. En **Mis gastos**, seleccione **Anticipos en efectivo** > **Nuevo**. 
2. En la página **Nueva solicitud de anticipo en efectivo**, introduzca el propósito del gasto y seleccione la ubicación donde se incurrirá en el gasto.
3. Introduzca el importe y la moneda solicitados, y luego seleccione **Guardar**. 
4. Cuando esté listo para enviar la solicitud de anticipo en efectivo, en la página **Solicitud de anticipo en efectivo**, seleccione **Flujo de trabajo** > **Enviar**.

## <a name="modify-a-cash-advance-request"></a>Modificar una solicitud de anticipo en efectivo

Puede modificar una solicitud de anticipo en efectivo si no se ha enviado para su aprobación.

1. En **Mis gastos: anticipos en efectivo**, busque y seleccione el anticipo en efectivo que desea editar.
2. Seleccione **Editar** y realice los cambios necesarios en la solicitud de anticipo en efectivo. 
3. Seleccione **Guardar y cerrar**.


## <a name="view-cash-advance-requests"></a>Ver solicitudes de anticipo en efectivo
Puede revisar la lista de todos los anticipos en efectivo que están en borrador, enviados, en revisión o pagados, en **Mis gastos: anticipos en efectivo**. 

## <a name="approve-cash-advance-requests"></a>Aprobar solicitudes de anticipo en efectivo

Los administradores o usuarios configurados como aprobadores en el flujo de trabajo podrán aprobar los adelantos en efectivo que se les envíen para su revisión. 

1. Para aprobar un anticipo en efectivo, en **Procesar anticipos en efectivo**, seleccione **Adelantos en efectivo para mi revisión**.
2. Seleccione el anticipo en efectivo que necesita revisar y seleccione **Aprobar**.  

## <a name="pay-cash-advances"></a>Pagar anticipos en efectivo 
El siguiente procedimiento generalmente lo completa un contable o un usuario con permisos de contabilidad.

1. Para contabilizar adelantos en efectivo aprobados, seleccione **Anticipos en efectivo aprobados** y luego seleccione **Pagar y transferir**.  
2. Proporcione los detalles del diario para los adelantos en efectivo y luego seleccione **Aceptar**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Presentar un informe de gastos frente a un anticipo en efectivo pagado 

Al crear y enviar un informe de gastos para el anticipo en efectivo que ya ha recibido, los gastos se ajustarán automáticamente con ese anticipo. Si su anticipo en efectivo es mayor que el importe registrado como gasto, debe devolver el saldo a la empresa utilizando la categoría de gastos **Devolver efectivo**. Si el anticipo en efectivo pagado por la empresa es menor que la cantidad que gastada, la empresa deberá reembolsarle el saldo. 

### <a name="example"></a>Ejemplo
Planea viajar de Seattle a Nueva York para una conferencia. Crea una solicitud de anticipo en efectivo de 3000,00 dólares estadounidenses por el coste estimado de la entrada en la conferencia, vuelos, hotel, comidas y taxis. No se le pagará a menos que su supervisor apruebe esta solicitud. Una vez que su gerente la aprueba, el anticipo en efectivo solicitado se paga en forma de 3.000,00 USD en su cuenta bancaria. Luego asiste a la conferencia. Después de completar su viaje, descubre que el gasto total fue solo de 2.790,00 USD. Seleccione **Efectivo** en el campo **Método de pago** y envíe sus gastos por valor de 2790,00 dólares estadounidenses. El importe de su gasto enviado se ajusta automáticamente contra el anticipo en efectivo de 3.000,00 USD que se le prestó. Ahora debe un saldo de 210,00 dólares estadounidenses (3000,00 - 2790,00), que puede devolver a la empresa a través de la categoría de gastos **Devolución de efectivo**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]