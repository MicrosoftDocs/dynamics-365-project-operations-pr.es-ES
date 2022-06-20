---
title: Seguimiento del esfuerzo del proyecto
description: En este artículo se proporciona información sobre cómo realizar un seguimiento del esfuerzo y progreso del trabajo.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c41dbc138f6fc92a9586de173ba5dfc89c7e44e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929281"
---
# <a name="project-effort-tracking"></a>Seguimiento del esfuerzo del proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

La necesidad de realizar un seguimiento del progreso de acuerdo con una programación varía según el sector. Algunos sectores realizan un seguimiento de nivel granular, mientras que otros realizan uno de nivel superior. Este artículo muestra cómo realizar una programación para cumplir con los requisitos de su organización.

## <a name="effort-tracking-view"></a>Vista de seguimiento del esfuerzo

La vista **Seguimiento del esfuerzo** realiza un seguimiento del progreso de las tareas de la programación comparando las horas de esfuerzo reales dedicadas a una tarea con las horas de esfuerzo planificadas de la tarea. Dynamics 365 Project Operations utiliza las siguientes fórmulas para calcular las métricas de seguimiento:

- **Porcentaje de progreso**: Esfuerzo real realizado hasta la fecha ÷ Estimación al finalizar (EAF) 
- **Esfuerzo restante**: Esfuerzo estimado al finalizar - Esfuerzo real invertido hasta la fecha 
- **EAF**: Esfuerzo restante + Esfuerzo real realizado hasta la fecha 
- **Desviación del esfuerzo proyectado**: Esfuerzo planificado - EAC

Project Operations muestra una proyección de la desviación del esfuerzo en la tarea. Si la EAC es superior al esfuerzo planificado, se proyecta que la tarea tardará más tiempo del planificado originalmente y está retrasada. Si el EAF es inferior al esfuerzo planificado, se prevé que la tarea tardará menos tiempo del planificado originalmente y va adelantada a la programación.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Reproyección de esfuerzo en tareas de nodo hoja

Es frecuente que los administradores de proyecto revisen las estimaciones originales de una tarea. Las reproyecciones de proyectos son la percepción que tiene un jefe de proyecto de las estimaciones, dado el estado actual de un proyecto. Sin embargo, no recomendamos que los directores de proyectos cambien las cifras de esfuerzo planificado. Esto se debe a que el esfuerzo planificado del proyecto representa el origen de la verdad establecido para la estimación de costes y el programa del proyecto y las partes interesadas del proyecto han dado su acuerdo.

Un director de proyectos puede reproyectar el esfuerzo en las tareas actualizando el valor predeterminado de **Esfuerzo distante** con una nueva estimación de la tarea. Esta actualización provoca un nuevo cálculo de la estimación de la tarea al finalizar (EEF), el porcentaje de progreso y la variación del esfuerzo proyectado en una tarea. La EAC, la ETC y el porcentaje de progreso en las tareas de resumen también se recalculan y producen una nueva proyección de la desviación del esfuerzo.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reproyección del esfuerzo en tareas de resumen

El esfuerzo en tareas de resumen o tareas de contenedor se puede reproyectar. Los directores de proyecto pueden actualizar el esfuerzo restante en las tareas de resumen. La actualización del esfuerzo restante desencadena el siguiente conjunto de cálculos en la aplicación:

- El CEF y el porcentaje de progreso en la tarea se calculan.
- El nuevo EAF se distribuye a las tareas secundarias en la misma proporción que el EAF original de la tarea.
- Se calcula el nuevo EAF en cada una de las tareas individuales hasta las tareas del nodo hoja. 
- Las tareas secundarias afectadas hasta los nodos hoja tienen su esfuerzo restante y su porcentaje de progreso recalculado en función del valor de EAF. Esto da como resultado una nueva proyección para la variación de esfuerzo de la tarea. 
- Se vuelven a calcular los EAF de las tareas de resumen hasta el nodo raíz.
- El esfuerzo aprobado en una tarea de resumen es la suma del esfuerzo aprobado en todas las tareas secundarias más el esfuerzo aprobado en la tarea de resumen.
- El esfuerzo restante en la tarea de resumen es la suma del esfuerzo restante en todas las tareas secundarias menos el esfuerzo aprobado en la tarea de resumen.

## <a name="project-status-summary"></a>Resumen del estado del proyecto

El seguimiento de los datos en la vista **Seguimiento del esfuerzo** y **Seguimiento de costes** muestra el progreso y el consumo de costes en el nodo raíz del proyecto, las tareas de resumen y los niveles de tareas del nodo hoja. La sección **Estado** en la página **Entidad de proyecto** muestra un resumen del estado a nivel de proyecto.

## <a name="status-summary-fields"></a>Campos de resumen de estado

El campo **Estado general del proyecto** es un campo editable que muestra el estado general del proyecto. Utiliza códigos de colores, como verde, amarillo y rojo, para indicar un riesgo creciente. El campo **Comentarios** permite al jefe de proyecto introducir comentarios específicos sobre el estado. El campo **Última actualización del estado el** no es editable y el valor es una marca de tiempo que indica cuándo se actualizó por última vez.

Los campos **Rendimiento de programación** y **Rendimiento de coste** se establecen desde la fecha de seguimiento. Cuando la programación y la variación de costes para el nodo raíz en la vista **Seguimiento del esfuerzo** son positivas, puede establecer estos campos en **Adelantado**. Cuando la programación y la desviación de coste para el nodo raíz son negativos, puede establecerlos en **Retrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
