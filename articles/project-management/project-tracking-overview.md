---
title: Información general del seguimiento de proyectos
description: En este tema se proporciona información sobre cómo realizar un seguimiento del progreso y los costes del proyecto.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907384"
---
# <a name="project-tracking-overview"></a>Información general del seguimiento de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

La necesidad de realizar un seguimiento del progreso de acuerdo con una programación varía según el sector. Algunos sectores realizan un seguimiento de nivel granular, mientras que otros realizan uno de nivel superior. Este tema muestra cómo realizar una programación para cumplir con los requisitos de su organización.

## <a name="effort-tracking-view"></a>Vista de seguimiento del esfuerzo

La vista **Seguimiento del esfuerzo** realiza un seguimiento del progreso de las tareas de la programación comparando las horas de esfuerzo reales dedicadas a una tarea con las horas de esfuerzo planificadas de la tarea. Dynamics 365 Project Operations utiliza las siguientes fórmulas para calcular las métricas de seguimiento:

- **Porcentaje de progreso**: Esfuerzo real realizado hasta la fecha ÷ Estimación al finalizar (EAF) 
- **Estimación de finalización (ETC)**: Esfuerzo planificado - Esfuerzo real realizado hasta la fecha 
- **EAF**: Esfuerzo restante + Esfuerzo real realizado hasta la fecha 
- **Variación del esfuerzo proyectado**: Esfuerzo planificado - EAF

Project Operations muestra una proyección de la variación del esfuerzo en la tarea. Si el EAF es superior al esfuerzo planificado, se prevé que la tarea tardará más tiempo del planificado originalmente y va por detrás de la programación. Si el EAF es inferior al esfuerzo planificado, se prevé que la tarea tardará menos tiempo del planificado originalmente y va adelantada a la programación.

## <a name="reprojecting-effort"></a>Reproyección de esfuerzo

Es frecuente que los administradores de proyecto revisen las estimaciones originales de una tarea. Las reproyecciones de proyectos son la percepción de las estimaciones de un administrador de proyecto según estado actual de un proyecto. Sin embargo, no recomendamos que los gerentes de proyecto cambien los números de línea de base. Esto se debe que la línea de base del proyecto representa la fuente de verdad establecida para la programación y la estimación de costes del proyecto, y todos los interesados en el proyecto la han aceptado.

Existen dos formas en las que un jefe de proyecto puede reproyectar el esfuerzo en las tareas:

- Anular el ETC predeterminado con una nueva estimación del esfuerzo restante real en la tarea. 
- Anular el porcentaje de progreso predeterminado con una nueva estimación del progreso real de la tarea.

Cada enfoque genera un nuevo cálculo del ETC, EAF y el porcentaje de progreso de la tarea, y la variación del esfuerzo proyectado en una tarea. El EAF, ETC y el porcentaje de progreso en las tareas de resumen también se recalculan y producen una nueva proyección de la variación del esfuerzo.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reproyección de esfuerzo en tareas de resumen

El esfuerzo en tareas de resumen o tareas de contenedor se puede reproyectar. Independientemente de si el usuario efectúa la reproyección mediante el esfuerzo restante o el porcentaje de progreso en las tareas de resumen, se inicia el siguiente conjunto de cálculos:

- Se calculan el EAF, el ETC y el porcentaje de progreso en la tarea.
- El nuevo EAF se distribuye a las tareas secundarias en la misma proporción que el EAF original de la tarea.
- Se calcula el nuevo EAF en cada una de las tareas individuales hasta las tareas del nodo hoja. 
- Las tareas secundarias afectadas hasta los nodos hoja tienen su ETC y su porcentaje de progreso recalculado en función del valor de EAF. Esto da como resultado una nueva proyección para la variación de esfuerzo de la tarea. 
- Se vuelven a calcular los EAF de las tareas de resumen hasta el nodo raíz.

### <a name="cost-tracking-view"></a>Vista de seguimiento de costes 

La vista **Seguimiento de costes** compara el coste real que se gastó en una tarea con el coste planificado en una tarea. 

> [!NOTE]
> Esta vista muestra solo los costes laborales y no incluye los costes de las estimaciones de gastos. Project Operations utiliza las siguientes fórmulas para calcular las métricas de seguimiento:

- **Porcentaje del coste consumido**: Coste real gastado hasta la fecha ÷ Coste estimado al finalizar
- **Coste de finalización (CTC)**: Coste planificado - Coste real gastado hasta la fecha
- **EAF**: Coste restante + Coste real gastado hasta la fecha
- **Variación del coste proyectado**: Coste planificado - EAF

Se muestra una proyección de la variación de coste en la tarea. Si el EAF es superior al coste planificado, se prevé que la tarea costará más de lo planificado originalmente. Por lo tanto, la tendencia es que se supere el presupuesto. Si el EAF es inferior al coste planificado, se prevé que la tarea costará menos de lo planificado originalmente. Por lo tanto, la tendencia es que no se supere el presupuesto.

## <a name="project-managers-reprojection-of-cost"></a>Reproyección del coste del jefe de proyecto

Cuando se reproyecta el esfuerzo, el CTC, el EAF, el porcentaje de coste consumido y la variación del coste proyectado se recalculan en la vista **Seguimiento de costes**.

## <a name="project-status-summary"></a>Resumen del estado del proyecto

Los datos de seguimiento en las vistas **Seguimiento del esfuerzo** y **Seguimiento de costes** muestran el progreso y el consumo de costes en el nodo raíz del proyecto, las tareas de resumen y los niveles de tareas del nodo hoja. La sección **Estado** en la página **Entidad de proyecto** muestra un resumen del estado a nivel de proyecto.

## <a name="status-summary-fields"></a>Campos de resumen de estado

El campo **Estado general del proyecto** es un campo editable que muestra el estado general del proyecto. Utiliza códigos de colores, como verde, amarillo y rojo, para indicar un riesgo creciente. El campo **Comentarios** permite al jefe de proyecto introducir comentarios específicos sobre el estado. El campo **Última actualización del estado el** no es editable y el valor es una marca de tiempo que indica cuándo se actualizó por última vez.

Los campos **Rendimiento de programación** y **Rendimiento de coste** se establecen desde la fecha de seguimiento. Cuando la programación y la variación de costes para el nodo raíz en la vista **Seguimiento del esfuerzo** son positivas, puede establecer estos campos en **Adelantado**. Cuando la programación y la variación de coste para el nodo raíz sean negativas, puede establecerlas en **Retrasado**.
