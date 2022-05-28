---
title: Seguimiento de las ventas del proyecto
description: Este tema proporciona información sobre cómo Project Operations realiza un seguimiento de los ingresos de un proyecto.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fff5fa6b12dddd780eb6bf77edca85a3a0c0629c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583467"
---
# <a name="project-sales-tracking"></a>Seguimiento de las ventas del proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations realiza un seguimiento de las estimaciones y los ingresos de mano de obra con el menor detalle requerido en el plan del proyecto. La estimación de los ingresos por mano de obra se basa en el esfuerzo planificado y los recursos genéricos o con nombre que se asignan a cada tarea de nodo hoja en el plan del proyecto. Cuando comienza el proyecto y la gente comienza a notificar tiempo en varias tareas del proyecto, se resume los ingresos reales por mano de obra, lo que inicia un cálculo de las proyecciones.

## <a name="labor-revenue-tracking-view"></a>Vista de seguimiento de ingresos por mano de obra

En la página **Proyectos**, en la pestaña **Seguimiento**, puede seleccionar **Seguimiento** > **Coste** para abrir la vista **Seguimiento de costes**. O puede seleccionar **Usar** > **Tasa de facturación** para abrir la vista **Seguimiento de los ingresos**, que muestra el progreso de los ingresos por mano de obra en cada tarea del plan del proyecto. Esta vista también compara los ingresos por mano de obra real gastado en una tarea con los ingresos por mano de obra planificados de la tarea. Project Operations utiliza las siguientes fórmulas para calcular métricas de ingresos por mano de obra:

- **Ingreso planificado**: valores de ventas estimados de todas las asignaciones de recursos en cada tarea de nodo hoja
- **Ingreso real**: suma de todos las ventas reales sin facturar por tiempo registrado en la tarea
- **Ingresos facturables en %**: Ingresos reales ÷ Estimación de ingresos al finalizar
- **Ingresos restantes**: Estimación de ingresos al finalizar - Ingresos reales
- **Ingresos estimados al finalizar**: Ingresos restantes + Ingresos reales
- **Varianza de ingresos**: Ingreso planeados - Ingresos estimados al finalizar


> [!NOTE]
> Project Operations solo muestra los ingresos por mano de obra en la página **Proyecto** en la pestaña **Seguimiento**. Si bien los materiales y los gastos se pueden estimar y rastrear para el consumo, estos ingresos no se incluyen en los ingresos que se muestran en la pestaña **Seguimiento**. Esta pestaña está diseñada para funcionar solo para reproyectar ingresos de mano de obra por esfuerzo de reproyección.  
> Todos los importes de ingresos que se muestran se convierten a la divisa de coste del proyecto. La divisa de coste del proyecto es la divisa de la unidad contratante del proyecto. Para proyectos de precio fijo, las cifras de ingresos en la vista **Seguimiento de ingresos por mano de obra** no es relevante porque los datos reales de ventas no facturadas no se registran en la aprobación de tiempo.
> Los valores de ventas estimados por tiempo que se muestran en la pestaña **Estimar** del proyecto no pueden sumarse al valor de los ingresos planificados en la pestaña **Seguimiento**. El origen de esta discrepancia puede deberse a dos posibles razones:
><ol>
   ><li> La pestaña <b>Estimaciones</b> muestra los ingresos estimados en la divisa de venta, mientras que la pestaña <b>Seguimiento</b> muestra los ingresos planificados convertidos a la divisa de coste. </li>
   ><li> Cuando las ventas estimadas se convierten a la divisa del contrato como se muestra en la pestaña <b>Estimaciones</b>, a la divisa del proyecto, la conversión implica pasos que podrían resultar en cierta pérdida de precisión: </li>
><ol>
><li> El importe de las ventas estimado en la divisa del contrato se convierte primero a la divisa base (conversión 1).</li>
><li> El importe de ventas estimado en la divisa base se convierte a la divisa del coste del proyecto (conversión 2). </li>
></ol>
></ol>
> La precisión de la divisa se aplica en ambos pasos, lo que da como resultado una desviación de los ingresos planificados en la divisa del proyecto de las ventas planificadas en la divisa del contrato.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Reproyección de ingresos en tareas de nodo hoja

Los ingresos por mano de obra en una tarea de nodo hoja no se pueden reproyectar directamente en la pestaña **Seguimiento** pestaña en la página **Proyecto**. Sin embargo, puede utilizar la vista **Seguimiento del esfuerzo** para reproyectar el esfuerzo restante en una tarea. Esto provoca un nuevo cálculo de los ingresos restantes de la tarea. Esta es una descripción de cómo funciona esto.

1. Un director de proyectos puede reproyectar el esfuerzo en las tareas actualizando el valor predeterminado en el campo **Esfuerzo restante** con una nueva estimación del esfuerzo restante en la tarea. La reproyección provoca un nuevo cálculo del esfuerzo estimado al finalizar (EEF) de la tarea, el porcentaje de progreso y la variación del esfuerzo proyectado en una tarea. La EEF, la estimación de finalización (ETC) y el porcentaje de progreso en las tareas de resumen también se recalculan y producen una nueva proyección de la variación del esfuerzo.
2. Basado en el nuevo valor para el esfuerzo restante en la tarea, el sistema calcula los ingresos restantes en la vista **Seguimiento de ingresos**. Para calcular los ingresos restantes basados en el esfuerzo restante, el sistema primero calcula los ingresos promedio de una hora de esfuerzo en la tarea como ingresos planeado o esfuerzo planeado. Los ingresos planificados son la suma de los ingresos de todas las asignaciones de recursos en la tarea. El ingreso promedio por hora se usa para calcular el coste restante de ingresos restantes que se acaba de proyectar de la tarea.
3. Los ingresos estimados al finalizar y el porcentaje de consumo de ingresos en la tarea de nodo hoja se vuelven a calcular.
4. El valor de los ingresos al finalizar de las tareas de resumen hasta el nodo raíz se vuelve a calcular.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Reproyección de ingresos en tareas de resumen

Puede reproyectar los ingresos por mano de obra en tareas de resumen o tareas de contenedor. Sin embargo, no puede reproyectar directamente los ingresos de mano de obra en una tarea de proyecto de resumen en la pestaña **Seguimiento** en la página **Proyecto**. De forma similar a las tareas de nodo hoja, la reproyección de tareas de resumen y contenedor se puede realizar utilizando la vista **Seguimiento del esfuerzo**. En esta vista, puede reproyectar el esfuerzo restante en una tarea de resumen, lo que provoca un nuevo cálculo de ingresos restante en la tarea de resumen. Esta es una descripción de cómo funciona esto.

1. Un director de proyectos puede reproyectar el esfuerzo en las tareas actualizando el valor predeterminado en el campo **Esfuerzo restante** con una nueva estimación del esfuerzo restante en la tarea **Esfuerzo restante**. La reproyección provoca un nuevo cálculo del esfuerzo estimado al finalizar (EEF) de la tarea, el porcentaje de progreso y la variación del esfuerzo proyectado en una tarea. El EAF, ETC y el porcentaje de progreso en las tareas de resumen también se recalculan y producen una nueva proyección de la variación del esfuerzo.
2. Basado en el nuevo valor en el campo **Esfuerzo restante** en la tarea, el sistema calcula los ingresos restantes en la vista **Seguimiento de ingresos**. Para calcular los ingresos restantes basados en el esfuerzo restante, el sistema primero calcula los ingresos promedio de una hora de esfuerzo en la tarea como ingresos planeado o esfuerzo planeado. Los ingresos planificados son la suma de los ingresos de todas las asignaciones de recursos en la tarea. Este ingreso promedio por hora se usa para calcular los ingresos del esfuerzo restante proyectado recientemente para la tarea.
3. Los ingresos estimados al finalizar y los porcentajes de consumo de ingresos en la tarea de resumen se vuelven a calcular.
4. El nuevo valor para los ingresos estimados al finalizar se distribuye hasta llegar a las tareas secundarias en la misma proporción que los ingresos planeados originales de la tarea.
5. Se calculan los ingresos estimados al finalizar en cada una de las tareas individuales hasta llegar a las tareas del nodo hoja. Según este valor, las tareas secundarias afectadas hasta llegar a los nodos hoja tendrán sus ingresos restantes y el porcentaje de consumo de ingresos recalculados en función del valor del ingresos al finalizar. Esto da como resultado una nueva proyección para la variación de ingresos de la tarea. 
6. El valor de los ingresos al finalizar de las tareas de resumen hasta el nodo raíz se vuelve a calcular.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

