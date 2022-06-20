---
title: Reservar para un proyecto
description: En este artículo se proporciona información sobre la reserva de recursos para un proyecto.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dca9d722eae595af7a81c2b4684729d7658ed012
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928545"
---
# <a name="book-to-a-project"></a>Reservar para un proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Hay ocasiones en las que un administrador de proyecto o un administrador de recursos necesitará asignar un recurso al proyecto sin que un miembro genérico del equipo defina un requisito específico. Esto se puede lograr de una de tres maneras.

- Reservar desde la cuadrícula de miembros del equipo
- Reservar desde el tablero de programación
- Reservar desde el formulario **Proyecto**

## <a name="book-from-the-team-member-grid"></a>Reservar desde la cuadrícula de miembros del equipo

Si su organización está operando en modo de asignación de recursos híbrido, el gerente de proyecto puede reservar un recurso directamente para el proyecto completando los siguientes pasos.

1. Desde el proyecto, vaya a la cuadrícula de miembros del equipo y seleccione **Nuevo**.
2. Defina el nombre del puesto y el rol del recurso.
3. Seleccione el recurso que se puede reservar desde el servicio de búsqueda disponible.
4. Tras seleccionar el recurso, defina la siguiente información de campo para reservar el recurso:

    - Fecha de inicio
    - Fecha de finalización
    - Método de asignación
    - Horas, si es aplicable
    - Aprobador de proyecto

6. Seleccione **Guardar y cerrar**

## <a name="book-from-the-schedule-board"></a>Reservar desde el tablero de programación

Cuando un administrador de recursos necesita reservar un recurso directamente para un proyecto, puede usar el tablero de programación y los requisitos del proyecto. El requisito del proyecto es un requisito de recursos que siempre está disponible para reservar respecto a él. Para reservar directamente para un proyecto desde el panel de programación, complete los pasos siguientes.

1. Navegue hasta el panel de programación y, en la página de la izquierda, filtre los recursos que está considerando para el requisito.
2. En el panel inferior, seleccione la pestaña **Proyecto** para ver una lista de los requisitos del proyecto.
3. Arrastre el requisito a un recurso y defina la siguiente información:

    - Fecha de inicio
    - Fecha de finalización
    - Estado de reserva
    - Método de reserva
    - Duration
   
   > [!NOTE]
   > Actualmente, Dynamics 365 Project Operations no es compatible con el tablero de programación.   

## <a name="book-from-the-project-form"></a>Reservar desde el formulario Proyecto

Como gerente de proyecto, es posible que deba reservar un recurso para un proyecto, pero solo conozca los criterios en lugar del nombre del recurso. Complete los siguientes pasos para utilizar el asistente de programación para encontrar un recurso en función de los atributos disponibles del recurso. 

1. Navegue hasta el proyecto y seleccione **Reservar** para abrir el Asistente de programación.
2. Usando los filtros del lado izquierdo del Asistente de programación, reduzca los criterios y seleccione **Buscar.**
3. Según los recursos devueltos en los resultados, puede reservar un recurso.

> [!NOTE]
> Este método no crea ninguna reserva para el recurso. En su lugar, agrega el recurso al equipo. Una vez que el miembro del equipo se ha agregado al proyecto, el administrador del proyecto puede usar el mantenimiento de reservas o la extensión de reservas para agregar las reservas necesarias al recurso.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
