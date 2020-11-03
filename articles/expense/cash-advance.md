---
title: Anticipo de efectivo
description: En este tema se proporciona información sobre adelantos de efectivo.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085031"
---
# <a name="cash-advance"></a>Anticipo de efectivo

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Un anticipo en efectivo permite a los empleados pedir prestado dinero a su empresa antes de incurrir en gastos. Cuando se aprueba y paga un anticipo en efectivo solicitado, el empleado puede usar el dinero para los gastos comerciales en los que puede estar a punto de incurrir. 

## <a name="create-and-submit-a-cash-advance-request"></a>Crear y enviar una solicitud de anticipo en efectivo

1. En **Mis gastos** , seleccione **Adelantos en efectivo** > **Nuevo** para crear un nuevo anticipo en efectivo. 
2. En la página **Nueva solicitud de anticipo en efectivo** , introduzca el propósito del gasto y seleccione la ubicación donde se incurrirá en el gasto.
3. Introduzca el importe y la moneda solicitados, y luego seleccione **Guardar**. 
4. Cuando esté listo para enviar la solicitud de anticipo en efectivo, en la página **Solicitud de anticipo en efectivo** , seleccione **Flujo de trabajo** > **Enviar**.

## <a name="modify-a-cash-advance-request"></a>Modificar una solicitud de anticipo en efectivo

Puede modificar una solicitud de anticipo en efectivo si no se ha enviado para su aprobación.

1. En **Mis gastos: anticipos en efectivo** localice y seleccione el anticipo en efectivo que desea editar.
2. Seleccione **Editar** y realice los cambios necesarios en la solicitud de anticipo en efectivo. 
3. Seleccione **Guardar y cerrar**.


## <a name="view-cash-advance-requests"></a>Ver solicitudes de anticipo en efectivo
Puede revisar la lista de todos los anticipos en efectivo que están en borrador, enviados, en revisión o pagados, en **Mis gastos: anticipos en efectivo**. 

## <a name="approve-cash-advance-requests"></a>Aprobar solicitudes de anticipo en efectivo

Los administradores o usuarios configurados como aprobadores en el flujo de trabajo podrán aprobar los adelantos en efectivo que se les envíen para su revisión. 

1. Para aprobar un anticipo en efectivo, en **Procesar anticipos en efectivo** , seleccione **Adelantos en efectivo para mi revisión**.
2. Seleccione el anticipo en efectivo que necesita revisar y seleccione **Aprobar**.  

## <a name="pay-cash-advances"></a>Pagar anticipos en efectivo 
El siguiente procedimiento generalmente lo completa un contable o un usuario con permisos de contabilidad.

1. Para contabilizar adelantos en efectivo aprobados, seleccione **Anticipos en efectivo aprobados** y luego seleccione **Pagar y transferir**.  
2. Proporcione los detalles del diario para los adelantos en efectivo y luego seleccione **Aceptar**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Presentar un informe de gastos frente a un anticipo en efectivo pagado 

Cuando crea y envía un informe de gastos para el anticipo en efectivo que ya recibió, los gastos se ajustarán automáticamente contra ese anticipo. Si su anticipo en efectivo es mayor que el importe registrado como gasto, debe devolver el saldo a la empresa utilizando la categoría de gastos **Devolver efectivo**. Si el anticipo en efectivo pagado por la empresa es menor que la cantidad que gastó, la empresa debe reembolsarle el saldo. 

### <a name="example"></a>Ejemplo
Tiene previsto viajar para asistir a una conferencia, desde Seattle a la ciudad de Nueva York. Usted crea una solicitud de anticipo en efectivo de 3.000,00 USD, ya que ha estimado que el coste de la entrada a la conferencia, los vuelos, el hotel, las comidas y los taxis suman aproximadamente esta cantidad. No se le pagará a menos que su gerente haya aprobado esta solicitud. Una vez que su gerente la aprueba, el anticipo en efectivo solicitado se paga en forma de 3.000,00 USD en su cuenta bancaria. Luego asiste a la conferencia. Después de completar su viaje, descubre que el gasto total fue solo de 2.790,00 USD. Seleccione **Efectivo** en el campo **Método de pago** y envíe los gastos por 2.790,00 USD. El importe de su gasto enviado se ajusta automáticamente contra el anticipo en efectivo de 3.000,00 USD que se le prestó. Ahora debe un saldo de 210,00 USD (3.000,00 - 2.790,00) a la empresa, que puede devolver a la empresa mediante la categoría de gastos **Devolver efectivo**. 
