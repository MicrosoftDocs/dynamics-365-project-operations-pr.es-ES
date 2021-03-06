---
title: Revisar recursos propuestos
description: En este tema se proporciona información sobre cómo proponer recursos de proyecto.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897382"
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

- Proponer varios recursos para satisfacer la petición si no hay un solo recurso disponible para cumplir con las horas necesarias. Las horas propuestas se dividen entre varios recursos que pueden satisfacer las horas necesarias. En este escenario, las horas no pueden superponerse.
- Proponer menos recursos de los necesarios. En este escenario, la capacidad de recursos propuesta es menor que las horas requeridas que especificó el solicitante. Por lo tanto, cuando el solicitante acepta los recursos propuestos, se crea un requisito de recurso no cumplido para capturar la petición restante.
- Reservar varios recursos para satisfacer la petición si no hay un solo recurso disponible para completar el trabajo.
- Reservar menos recursos de los necesarios. En este escenario, las horas reservadas son menos que las horas necesarias. El sistema le guía para proponer recursos en lugar de reservas, de modo que el solicitante pueda verificar y realizar un seguimiento de la petición restante.

## <a name="billable-utilization"></a>Uso facturable

Los recursos pueden tener un uso facturable objetivo. Este uso objetivo se define como un atributo en el rol predeterminado de un recurso o se establece en el registro del recurso individual que se puede reservar. Los cálculos de uso se basan en las horas reales informadas por los recursos mediante entradas de tiempo aprobadas.

Se utilizan las siguientes fórmulas para calcular el uso:

- Uso facturable = Horas reales imputables ÷ Capacidad de recursos
- Uso no facturable = Tiempo real con Id. de tipo de facturación = No imputable, Complementario o No disponible ÷ Capacidad de recursos
- Interno = Tiempo real sin contrato de venta ÷ Capacidad de recursos
- Capacidad de recursos = Horas de trabajo de recursos - Fuera de la oficina - Días no laborables

Puede encontrar la vista **Uso de recursos** en el panel **Recursos**.

Cada celda de la cuadrícula representa el porcentaje de uso facturable del recurso en un período, como un día, una semana o un mes. Se usan las siguientes fórmulas para colorear las celdas:

- **Verde:** Uso facturable \>= Uso objetivo del recurso
- **Amarillo:** Uso objetivo – 20 \<= Uso facturable \< Uso objetivo
- **Rojo:** Uso facturable \< Uso objetivo – 20

Puesto que la vista **Uso de recursos** se basa en el tablero de programación, puede usar las capacidades de filtrado del tablero de programación para filtrar sus resultados.

La cuadrícula requiere que establezca un uso objetivo en el rol o en el recurso individual. Para realizar esta configuración, vaya a **Recursos** \> **Roles de recursos**.

Además, se debe asignar un rol predeterminado a cada recurso que se puede reservar. Vaya a **Recursos** \> **Recursos**. En la pestaña **Project Service**, verifique que se haya definido un rol de recurso y que el campo **Es predeterminado** esté establecido en **Sí**. Puede agregar roles adicionales en los que **Es predeterminado = No**. El rol en el que **Es predeterminado = Sí** se usa para evaluar el uso del recurso en relación el objetivo para ese rol.

En la pestaña **Project Service** también puede establecer un uso objetivo individual para el recurso. El cálculo de uso utiliza después ese uso objetivo para evaluar el objetivo del recurso en lugar del objetivo del rol predeterminado del recurso.

El uso se muestra para un recurso solo si ese recurso ha aprobado el tiempo imputable durante el período que se muestra en la cuadrícula.

## <a name="resource-availability"></a>Disponibilidad de recursos

Es fundamental que los administradores de recursos puedan ver la disponibilidad de recursos y actualizar las reservas. En algunos casos, no existe una petición formal (solicitud de recursos), pero un administrador de recursos debe responder a una petición no planificada que llegue a través de canales como un correo electrónico, una llamada telefónica o un mensaje instantáneo. Los administradores de recursos usan el tablero de programación para actualizar recursos y reservas.

Las horas de trabajo de los recursos se utilizan como base para calcular la disponibilidad de un recurso. Las reservas de recursos consumen la capacidad de los recursos.

El tablero de programación utiliza colores y sombras para mostrar las reservas, la disponibilidad y las reservas excesivas, y también el estado de las reservas. Una configuración en la configuración del tablero de programación le permite mostrar una leyenda.

Si aparece una flecha que apunta hacia la derecha al lado de un recurso individual que se puede reservar en el tablero de programación, el recurso se puede expandir para mostrar detalles del trabajo en el que se reserva el recurso.

Puesto que Dynamics 365 Project Operations utiliza el motor Universal Resource Scheduling, si ya dispone de Dynamics 365 Field Service instalado, puede ver los detalles de las reservas de recursos para proyectos, órdenes de trabajo y cualquier otra entidad a la que haya extendido la programación.

Para ver más detalles sobre un recurso individual, haga clic con el botón secundario en él para abrir la tarjeta de recursos.

