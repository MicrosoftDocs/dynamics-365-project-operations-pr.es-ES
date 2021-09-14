---
title: Revisar recursos propuestos
description: En este tema se proporciona información sobre cómo proponer recursos de proyecto.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b3077f98052fcac9989a81b2fab12fa30d65d970
ms.sourcegitcommit: ebcaec7806ee8aee1323ef532d5b7735d27edd04
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403816"
---
# <a name="review-proposed-resources"></a>Revisar recursos propuestos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los administradores de recursos pueden proponer un recurso al administrador del proyecto mediante una solicitud de recursos.

Para revisar los recursos propuestos, siga estos pasos:

1. Desde la cuadrícula **Solicitud** o la propia solicitud, seleccione **Buscar recursos**.
2. En la página **Asistente de programación**, seleccione el recurso y luego confirme que todas las horas propuestas están incluidas en la reserva propuesta.
3. En el panel **Crear reserva de recursos**, configure el campo **Estado de la reserva** en **Propuesto** y luego seleccione **Reservar**.

    > [!NOTE]
    > Establecer el **Estado de la reserva** en **Propuesto** no reserva el recurso de forma rígida y no reemplaza el recurso genérico con el miembro del equipo designado.

    Ocurren las siguientes actualizaciones de estado:

    - En la página **Asistente de programación**, los indicadores de estado se actualizan para indicar que la reserva está propuesta, no reservada en firme.
    - En la solicitud de recursos, el estado cambia a **Necesita revisión**.
    - En la pestaña **Equipo** del proyecto, el valor **Estado de la solicitud** del miembro del equipo genérico se cambia a **Necesita revisión**.

El administrador del proyecto puede aceptar o rechazar la propuesta.

Cuando los administradores de recursos procesan las solicitudes de recursos, pueden utilizar cualquiera de los siguientes enfoques:

- Proponer múltiples recursos para satisfacer la demanda si no hay un solo recurso disponible para cubrir las horas requeridas. Las horas propuestas se dividen entre varios recursos que pueden satisfacer las horas necesarias. En este escenario, las horas no pueden superponerse.
- Proponer menos recursos de los necesarios. En este escenario, la capacidad de recursos propuesta es menor que las horas requeridas que especificó el solicitante. Cuando el solicitante acepta los recursos propuestos, se crea un requisito de recursos sin cumplir para capturar la demanda restante.
- Reservar múltiples recursos para satisfacer la demanda si no hay un solo recurso disponible para completar el trabajo.
- Reserve menos recursos de los necesarios. En este escenario, las horas reservadas son menos que las necesarias. El sistema le guía para proponer recursos en lugar de reservas de modo que el solicitante pueda comprobar y realizar un seguimiento de la demanda restante.

## <a name="resource-availability"></a>Disponibilidad de recursos

Los administradores de recursos deben poder ver la disponibilidad de recursos y actualizar las reservas. En algunos casos, no existe una demanda formal (solicitud de recursos). Sin embargo, un administrador de recursos debe responder a una demanda no planificada que proviene de otros canales, como correos electrónicos, llamadas telefónicas o mensajes instantáneos. Los administradores de recursos usan el **Tablero de programación** para actualizar recursos y reservas.

Las horas de trabajo de los recursos se utilizan como base para el cálculo de la disponibilidad de un recurso. Las reservas de recursos consumen la capacidad de los recursos.

El **Tablero de programación** utiliza colores y sombras para mostrar las reservas, la disponibilidad, las reservas excesivas y el estado de las reservas. Una opción del **Tablero de programación** le permite mostrar una leyenda.

Si aparece una flecha que apunta hacia la derecha al lado de un recurso individual reservable en el **Tablero de programación**, el recurso se puede expandir para mostrar detalles del trabajo en el que se reserva el recurso.

Puesto que Dynamics 365 Project Operations utiliza el motor Universal Resource Scheduling, si ya dispone de Dynamics 365 Field Service instalado, puede ver los detalles de las reservas de recursos para proyectos, órdenes de trabajo y cualquier otra entidad a la que haya extendido la programación.

Para ver más detalles sobre un recurso individual, haga clic con el botón secundario en él para abrir la tarjeta de recursos.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
