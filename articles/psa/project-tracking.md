---
title: Progreso y costes del proyecto
description: En este tema se proporciona información sobre el seguimiento del progreso y los costes del proyecto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4fe6adf1a16c1eafc5e37dbd8878dda44cbca230
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009052"
---
# <a name="project-progress-and-cost-consumption"></a>Progreso y costes del proyecto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

La necesidad de realizar un seguimiento del progreso de acuerdo con una programación varía según el sector. Algunos sectores realizan un seguimiento de nivel granular, mientras que otros realizan uno de nivel superior. Este tema muestra cómo realizar una programación para cumplir con los requisitos de su organización.

## <a name="effort-tracking-view"></a>Vista de seguimiento del esfuerzo

La vista **Seguimiento del esfuerzo** rastrea el progreso de las tareas en la programación. Compara las horas de esfuerzo reales dedicadas a una tarea con las horas planeadas de esfuerzo de la tarea. Project Service Automation utiliza las siguientes fórmulas para calcular las métricas de seguimiento:

Inicialmente en la creación de la tarea: el coste planificado se establecerá en el coste estimado al finalizar. Una vez que se registren los datos reales en la tarea, se calculará lo siguiente en la vista Seguimiento para el esfuerzo

- Porcentaje de progreso = Esfuerzo real realizado hasta la fecha ÷ Estimación al finalizar (EAF) 
- Estimación de finalización (ETC) = Estimación al finalizar (EAC) - Esfuerzo real realizado hasta la fecha 
- EAC = Esfuerzo restante + Esfuerzo real realizado hasta la fecha 
- Variación del esfuerzo proyectado = Esfuerzo planificado - EAF

Project Service Automation muestra una proyección de la variación del esfuerzo en la tarea. Si el EAF es superior al esfuerzo planificado, se prevé que la tarea tardará más tiempo del planificado originalmente. Por lo tanto, se llevará a cabo después de lo programado. Si el EAF es inferior al esfuerzo planificado, se prevé que la tarea tardará menos tiempo del planificado originalmente. Por lo tanto, se llevará a cabo antes de lo programado.

## <a name="reprojecting-effort"></a>Reproyección de esfuerzo

Es frecuente que un administrador de proyecto revise las estimaciones originales de una tarea. Las reproyecciones de proyectos son la percepción de las estimaciones de un administrador de proyecto según estado actual de un proyecto. Sin embargo, no recomendamos que los jefes de proyecto cambien los números de línea de base, ya que la línea de base del proyecto representa la fuente de verdad establecida para la programación y la estimación de costes del proyecto, y todos los interesados en el proyecto la han aceptado.

Existen dos formas en las que un jefe de proyecto puede reproyectar el esfuerzo en las tareas:

- Reemplace la ETC predeterminada por una nueva estimación del esfuerzo restante real en la tarea. 
- Anular el porcentaje de progreso predeterminado con una nueva estimación del progreso real de la tarea.

Cada uno de estos enfoques genera un nuevo cálculo del ETC, EAF y porcentaje de progreso de la tarea, y la variación del esfuerzo proyectado en una tarea. El EAF, ETC y el porcentaje de progreso en las tareas de resumen también se recalculan y producen una nueva proyección de la variación del esfuerzo.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reproyección de esfuerzo en tareas de resumen

Se puede reproyectar el esfuerzo en tareas de resumen o tareas de contenedor. Independientemente de si el usuario vuelve a proyectar utilizando el esfuerzo restante o el porcentaje de progreso en las tareas de resumen, comienza la siguiente serie de cálculos:

- Se calculan la EAC, la ETC y el porcentaje de progreso en la tarea.
- El nuevo EAF se distribuye a las tareas secundarias en la misma proporción que el EAF original de la tarea.
- Se calcula el nuevo EAF en cada una de las tareas individuales hasta las tareas del nodo hoja. 
- Las tareas secundarias afectadas hasta los nodos hoja tienen su ETC y su porcentaje de progreso recalculado en función del valor de EAF. Esto da como resultado una nueva proyección para la variación de esfuerzo de la tarea. 
- Se vuelven a calcular los EAF de las tareas de resumen hasta el nodo raíz.

### <a name="cost-tracking-view"></a>Vista de seguimiento de costes 

La vista **Seguimiento de costes** compara el coste real que se gastó en una tarea con el coste planificado. 

> [!NOTE]
> Esta vista muestra solo los costes laborales y no incluye los costes de las estimaciones de gastos. 

Project Service Automation utiliza las siguientes fórmulas para calcular las métricas de seguimiento:

Cuando se crea una tarea, el coste planificado es igual al coste estimado al finalizar. Una vez que se registren los datos reales en la tarea, se calcula lo siguiente en la vista **Seguimiento** para el coste:

 - Porcentaje del coste consumido = Coste real gastado hasta la fecha ÷ Coste estimado al finalizar para la tarea
 - Coste de finalización (CTC) = Coste estimado al finalizar - Coste real gastado hasta la fecha
 - Coste estimado al finalizar = CTC + Coste real gastado hasta la fecha
 - Variación de coste proyectado = Coste planificado - Coste estimado al finalizar

Se muestra una proyección de la variación de coste en la tarea. Si el coste estimado al finalizar es superior al coste planificado, se prevé que la tarea costará más de lo planificado originalmente. Por lo tanto, la tendencia es que se supere el presupuesto. Si el coste estimado al finalizar es menor que el coste planificado, se prevé que la tarea costará menos de lo planificado originalmente y la tendencia es que no se supere el presupuesto.

## <a name="project-managers-reprojection-of-cost"></a>Reproyección del coste del jefe de proyecto

Cuando se reproyecta el esfuerzo, el CTC, el coste estimado al finalizar, el porcentaje de coste consumido y la variación del coste proyectado se recalculan en la vista **Seguimiento de costes**.

## <a name="project-status-summary"></a>Resumen del estado del proyecto

El seguimiento de los datos en la vista **Seguimiento del esfuerzo** y **Seguimiento de costes** muestra el progreso y el consumo de costes en el nodo raíz del proyecto, las tareas de resumen y los niveles de tareas del nodo hoja. La sección **Estado** en la página **Entidad de proyecto** muestra un resumen del estado a nivel de proyecto.

## <a name="status-summary-fields"></a>Campos de resumen de estado

El campo **Estado general del proyecto** es un campo editable que muestra el estado general del proyecto. Utiliza códigos de colores, como verde, amarillo y rojo, para indicar un riesgo creciente. El campo **Comentarios** permite al jefe de proyecto introducir comentarios específicos sobre el estado. El campo **Última actualización del estado el** no es editable y el valor es una marca de tiempo que indica cuándo se actualizó por última vez.

Los campos **Rendimiento de programación** y **Rendimiento de coste** se establecen desde la fecha de seguimiento. Cuando la programación y la variación de costes para el nodo raíz en la vista **Seguimiento del esfuerzo** son positivas, puede establecer estos campos en **Adelantado**. Cuando la programación y la desviación de coste para el nodo raíz son negativos, puede establecerlos en **Retrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]