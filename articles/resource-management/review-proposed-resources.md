---
title: Revisar recursos propuestos
description: En este tema se proporciona información sobre cómo proponer recursos de proyecto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279294"
---
# <a name="review-proposed-resources"></a>Revisar recursos propuestos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los administradores de recursos pueden proponer un recurso al administrador del proyecto mediante una solicitud de recurso.

1. Desde la cuadrícula de solicitud o la propia solicitud, seleccione **Buscar recursos**.
2. En la página **Asistente de programación**, seleccione el recurso y, a continuación, en el panel **Crear reserva de recursos**, en el campo **Estado de reserva**, seleccione **Reservar**.

Se producen las siguientes actualizaciones de estado:

- En la página **Asistente de programación**, los indicadores de estado se actualizan para indicar que la reserva se propone, no se reserva manualmente.
- En la solicitud del recurso, el estado cambia a **Necesita revisión**.
- En la pestaña **Equipo** del proyecto, el valor de **Estado de la solicitud** del miembro del equipo genérico cambia a **Necesita revisión**.

El jefe de proyecto puede aceptar o rechazar la propuesta.

Cuando los administradores de recursos procesan las solicitudes de recursos, pueden usar cualquiera de los siguientes enfoques:

- Proponer múltiples recursos para satisfacer la demanda si no hay un solo recurso disponible para cubrir las horas requeridas. Las horas propuestas se dividen entre varios recursos que pueden satisfacer las horas necesarias. En este escenario, las horas no pueden superponerse.
- Proponer menos recursos de los necesarios. En este escenario, la capacidad de recursos propuesta es menor que las horas requeridas que especificó el solicitante. Por lo tanto, cuando el solicitante acepta los recursos propuestos, se crea un requisito de recursos sin cumplir para capturar la demanda restante.
- Reservar múltiples recursos para satisfacer la demanda si no hay un solo recurso disponible para completar el trabajo.
- Reservar menos recursos de los necesarios. En este escenario, las horas reservadas son menos que las necesarias. El sistema le guía para proponer recursos en lugar de reservas, de modo que el solicitante pueda verificar y realizar un seguimiento de la petición restante.

## <a name="resource-availability"></a>Disponibilidad de recursos

Es fundamental que los administradores de recursos puedan ver la disponibilidad de recursos y actualizar las reservas. En algunos casos, no existe una petición formal (solicitud de recursos), pero un administrador de recursos debe responder a una petición no planificada que llegue a través de canales como un correo electrónico, una llamada telefónica o un mensaje instantáneo. Los administradores de recursos usan el tablero de programación para actualizar recursos y reservas.

Las horas de trabajo de los recursos se utilizan como base para calcular la disponibilidad de un recurso. Las reservas de recursos consumen la capacidad de los recursos.

El tablero de programación utiliza colores y sombras para mostrar las reservas, la disponibilidad y las reservas excesivas, y también el estado de las reservas. Una configuración en la configuración del tablero de programación le permite mostrar una leyenda.

Si aparece una flecha que apunta hacia la derecha al lado de un recurso individual que se puede reservar en el tablero de programación, el recurso se puede expandir para mostrar detalles del trabajo en el que se reserva el recurso.

Puesto que Dynamics 365 Project Operations utiliza el motor Universal Resource Scheduling, si ya dispone de Dynamics 365 Field Service instalado, puede ver los detalles de las reservas de recursos para proyectos, órdenes de trabajo y cualquier otra entidad a la que haya extendido la programación.

Para ver más detalles sobre un recurso individual, haga clic con el botón secundario en él para abrir la tarjeta de recursos.



[!INCLUDE[footer-include](../includes/footer-banner.md)]