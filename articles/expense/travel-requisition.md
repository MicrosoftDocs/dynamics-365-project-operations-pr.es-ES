---
title: Solicitudes de viaje
description: En este tema se proporciona información sobre las solicitudes de viaje.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123759"
---
# <a name="travel-requisitions"></a>Solicitudes de viaje

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Una solicitud de viaje enumera los gastos en los que se incurrirá con el propósito de viajar. Se envía una solicitud de viaje para su revisión y se puede utilizar para autorizar gastos.

Es posible que deba presentar una solicitud de viaje antes de incurrir en cualquier gasto que se le cobre a la organización. Este requisito se aplica, independientemente de si carga los gastos a una tarjeta de crédito corporativa, gasta el efectivo que recibió de un anticipo en efectivo o incurre en gastos de bolsillo que reembolsará la organización.

Las solicitudes y directivas de viajes se pueden utilizar para ayudar a administrar los gastos de la organización. Por ejemplo, si su organización está trabajando en un proyecto de precio fijo que requiere viajes, los gastos de viaje de los miembros del equipo del proyecto deben ajustarse al presupuesto del proyecto. Al requerir que los gastos de viaje sean aprobados antes de incurrir en ellos, la organización puede ayudar a asegurarse de que el proyecto se mantenga dentro del presupuesto.

## <a name="configuration"></a>Configuración 

Las solicitudes de viaje se pueden configurar como "obligatorias" habilitando el parámetro "Autorización previa de viaje obligatoria" en los parámetros de gestión de gastos. 

## <a name="create-and-submit-a-travel-requisition"></a>Crear y enviar una solicitud de viaje

1. Vaya a **Mis gastos: solicitud de viaje** y seleccione **Nueva solicitud de viaje**.
2. Introduzca un propósito y destino para la solicitud.
3. En el campo **Descripción de viaje**, introduzca cualquier información adicional. 
4. Para cada uno de los gastos previstos, como vuelos, comidas o alquiler de coche, cree una partida de gastos. Incluya la fecha estimada, el monto estimado y la moneda de cada gasto. 
5. Cuando haya terminado de agregar los gastos esperados, seleccione **Guardar**.
6. Cuando esté listo para enviar la solicitud de viaje, seleccione **Flujo de trabajo** > **Enviar**.

Puede ver sus solicitudes de viaje aprobadas en **Mis gastos: solicitud de viaje**. 

## <a name="view-available-travel-requisitions"></a>Ver las solicitudes de viaje disponibles

Puede ver todas sus solicitudes de viaje en **Mis gastos: solicitudes de viaje**.

## <a name="approve-travel-requisitions"></a>Aprobar solicitudes de viaje

Seleccione la solicitud de viaje que desea aprobar y luego seleccione **Flujo de trabajo** > **Aprobar**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Envíe un informe de gastos utilizando su solicitud de viaje aprobada

1. Cree un nuevo informe de gastos y, en el encabezado del informe de gastos, desde la lista de solicitudes de viaje aprobadas, seleccione **Asignar a solicitud de viaje**.
2. El campo **Importe de la solicitud de viaje** se actualiza automáticamente en el encabezado del informe de gastos.
3. Agregue todos los gastos incurridos por el viaje. Si el campo **Preautorizado** está habilitado, se actualizarán el importe conciliado y el importe autorizado para la categoría de gasto específica.

> [!NOTE]
> Cuando asigna un informe de gastos a una solicitud de viaje aprobada, el importe de la transacción no puede ser mayor que el importe autorizado. 
