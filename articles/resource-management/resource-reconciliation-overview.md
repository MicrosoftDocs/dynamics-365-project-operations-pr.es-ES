---
title: Información general de conciliación de recursos
description: En este tema se proporciona información sobre cómo garantizar que se alinean las reservas de recursos y las asignaciones a proyectos.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125739"
---
# <a name="resource-reconciliation-overview"></a>Información general de conciliación de recursos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Para los miembros del equipo, las reservas y las asignaciones están emparejadas, pero no de manera vinculante. En otras palabras, los recursos pueden tener asignaciones pero no tener reservas, o bien pueden tener reservas pero no tener asignaciones. Idealmente, las reservas y las asignaciones deben estar alineadas para que los recursos tengan la capacidad comprometida para realizar las tareas asignadas. Sin embargo, las reservas pueden estar basadas en la disponibilidad y el control de tiempo de las tareas puede cambiar a medida que avanza el proyecto. Por lo tanto, el emparejamiento no vinculante de las reservas y las asignaciones proporciona flexibilidad.

La pestaña **Conciliación** en el formulario **Proyectos** permite a los jefes de proyecto conciliar las reservas y las asignaciones de los miembros de sus equipos de proyecto.

La pestaña **Conciliación** también muestra las reservas y las asignaciones hasta el nivel de las asignaciones de tareas individuales de cada miembro del equipo. Las horas se muestras en celdas que pueden representar períodos de meses a días.

La pestaña también muestra un total neto del proyecto, junto con una columna **Total**.

Para cada recurso, la pestaña calcula la diferencia entre las reservas de un miembro del equipo y un resumen de las asignaciones de tareas del miembro del equipo. Idealmente, esta diferencia debería ser 0 (cero). Es decir, no debería haber diferencia entre las reservas y las asignaciones. Las diferencias se muestran en color y sombreadas para llamar la atención en torno a dos condiciones:

- **Escasez de reservas**: la escasez de reservas se produce cuando un recurso tiene más asignaciones que reservas. Puesto que esta capacidad no se ha reservado, puede que el jefe de proyecto desee corregir esa condición extendiendo las reservas del recurso para cubrir el déficit.
- **Reservas en exceso**: las reservas en exceso se producen cuando se ha reservado un recurso para el proyecto, pero no se ha asignado a tareas. Esta condición podría ser aceptable en los casos en los que el recurso se reservó para el proyecto antes de que se produjera la asignación de tareas. Sin embargo, en otros casos, el recurso no está planificado para la asignarse a las tareas. En estos casos, el jefe de proyecto debería considerar cancelar las reservas del recurso de modo que la capacidad pueda utilizarse para otro proyecto.

En algunos casos, cuando se visualiza el tiempo a un nivel superior que el nivel de días (por ejemplo, el nivel de meses), puede ver una diferencia neta de cero para un recurso (es decir, reservas = asignaciones). Sin embargo, si visualiza el tiempo en el nivel de semana, puede ver que hay asignaciones de cero horas y reservas de 40 horas en la primera semana, y asignaciones de 40 horas y reservas de cero horas en la segunda semana. En general, las reservas y las asignaciones se concilian, pero hay diferencias de una semana a la siguiente.

Cuando se visualiza el tiempo a niveles más altos, las celdas de la pestaña **Conciliación** muestran un indicador para informar de que hay diferencias en los niveles de tiempo más bajos. Al hacer doble clic en una celda, podrá acercarse para ver la diferencia. A continuación, puede hacer clic con el botón secundario para alejarse. Al seleccionar un recurso y utilizar el control **Siguiente diferencia** de la barra de tareas de la cuadrícula, podrá ir a la siguiente diferencia entre las reservas y las asignaciones de dicho recurso. Puede usar posteriormente el control **Diferencia anterior** para volver. También puede desactivar el indicador de diferencias y el comportamiento de navegación en **Configuración**.


Si tiene asignaciones de tareas para un recurso pero no tiene reservas, en la página **Proyectos**, en la pestaña **Conciliación**, seleccione la escasez de reservas y luego seleccione **Ampliar reservas**. Aparecerá el cuadro de diálogo **Ampliar reservas** y mostrará la reserva necesaria para abordar la escasez de recursos. También muestra las reservas existentes del recurso en todos los proyectos o en otras entidades que se pueden programar. Si se selecciona **Aceptar** para crear la para reservar del recurso independientemente de la disponibilidad del recurso, es posible que se produzca un problema de exceso de reserva.

El jefe de proyecto o el administrador de recursos pueden usar el Tablero de programación para administrar las situaciones de exceso de reserva de un recurso más allá de su capacidad.

