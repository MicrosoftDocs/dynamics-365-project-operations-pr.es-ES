---
title: Navegación por la interfaz de usuario
description: Este tema proporciona información sobre la gestión de proyectos en las operaciones de proyectos de Dynamics 365.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 715a8bdb9a1f38f71b4c42f5307ed4a5c7170ef6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014272"
---
# <a name="navigating-the-user-interface"></a>Navegación por la interfaz de usuario

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

## <a name="overview"></a>Introducción

El formulario principal del proyecto se divide en varias pestañas. Cada pestaña representa un nivel de detalle diferente dentro del proyecto.

- **Resumen**: proporciona una descripción del proyecto y agrega tanto el rendimiento planificado como el real del proyecto.

    ![Pestaña y campos de resumen](media/navigation7.png)

- **Tareas**: proporciona los detalles sobre la estructura de descomposición del trabajo representada por una vista de cuadrícula, una vista de panel y un diagrama de Gantt.

    ![Pestaña y campos de tareas](media/navigation8.png)

- **Equipo**: proporciona detalles sobre los participantes del proyecto. El esfuerzo asignado a cada miembro del equipo también se resume en esta vista.

    ![Pestaña y campos de equipos](media/navigation9.png)

- **Asignaciones de recursos**: proporciona una vista por fases del esfuerzo para cada recurso en un proyecto.

    ![Pestaña y campos de asignaciones de recursos](media/navigation10.png)

- **Conciliación de recursos**: proporciona una vista por fases de tiempo de las diferencias entre las asignaciones de cada recurso nombrado y sus reservas.

    ![Pestaña y campos de conciliación de recursos](media/navigation11.png)

- **Estimados**: proporciona una vista por fases temporales de las estimaciones de costes y ventas de un proyecto.

    ![Pestaña y campos de estimaciones](media/navigation12.png)

- **Rastreo**: proporciona una vista que muestra el progreso de las tareas en estructura de descomposición del trabajo por esfuerzo, coste y ventas.

    ![Pestaña y campos de seguimiento](media/navigation13.png)

- **Ventas**: proporciona enlaces profundos a ofertas y contratos asociados con el proyecto.

- **Estimaciones de gastos**: proporciona una cuadrícula que define los gastos del proyecto en función de las categorías de gastos de la organización.

    ![Pestaña y campos de estimaciones de gastos](media/navigation14.png)

## <a name="grid-controls"></a>Controles de cuadrícula

A continuación se ofrece una breve descripción general de los controles típicos que se encuentran en las distintas pestañas de planificación de proyectos.

### <a name="refresh"></a>Actualizar

**Actualizar**: recupera los datos más recientes del servidor si se produjeron cambios después de cargar la cuadrícula.

![Botón Actualizar](media/navigation7.png)

### <a name="group-by"></a>Agrupar por

**Agrupar por**: actualiza la agrupación de filas en la cuadrícula para reflejar recursos, roles o categorías según las necesidades del usuario.

![Agrupar por botón](media/navigation6.png)

### <a name="previousnext"></a>Anterior/Siguiente

**Anterior**/**Siguiente**: actualiza los períodos de tiempo visibles en las cuadrículas de fases de tiempo.

![Botones Anterior y Siguiente](media/navigation2.png)

### <a name="timescale"></a>Escala temporal

**Escala de tiempo**: cambia la agregación de los datos por fases de tiempo entre días, semanas, meses y años.

![Botón de escala de tiempo](media/navigation3.png)

### <a name="expand"></a>Expandir

**Expandir**: representa la cuadrícula visible a pantalla completa, lo que brinda más capacidad para ver roles adicionales.

![Botón Expandir](media/navigation4.png)

### <a name="time-phase-by"></a>Fase temporal mediante

**Fase temporal mediante**: actualice la agrupación de las filas de la cuadrícula para reflejar las estimaciones de costes para las estimaciones de ventas. Este control también se aplica al script de estimación y la cuadrícula de seguimiento.

![Fase temporal mediante botón](media/navigation0.png)

### <a name="add-column"></a>Agregar columna

**Añadir columna**: permite al usuario definir las columnas visibles en la cuadrícula. Solo se pueden agregar columnas listas para usar a las cuadrículas en el formulario **Planificación de proyectos**.

![Agregar botón de columna](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]