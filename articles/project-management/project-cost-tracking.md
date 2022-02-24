---
title: Seguimiento de costes del proyecto
description: Este tema proporciona información sobre cómo Project Operations realiza un seguimiento del progreso respecto al coste laboral y el gasto en un proyecto.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711090"
---
# <a name="labor-cost-tracking-on-projects"></a>Seguimiento del coste de mano de obra en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations realiza un seguimiento de las estimaciones y el gasto de mano de obra con el menor detalle requerido en el plan del proyecto. La estimación financiera del coste de mano de obra se basa en el esfuerzo planificado y los recursos genéricos o con nombre que se asignan a cada tarea de nodo hoja en el plan del proyecto. Cuando comienza el proyecto y la gente comienza a notificar tiempo en varias tareas del proyecto, se resume el gasto real en mano de obra, lo que inicia un cálculo de las proyecciones.

## <a name="labor-cost-tracking-view"></a>Vista de seguimiento de costes de mano de obra

En la página **Proyectos**, en la pestaña **Seguimiento**, puede seleccionar **Seguimiento** > **Coste** para abrir la vista **Seguimiento de costes** y ver el progreso de la mano de obra invertida en cada tarea en el plan del proyecto. Esta vista también compara el coste de mano de obra real gastado en una tarea con el coste de mano de obra planificado de la tarea. Project Operations utiliza las siguientes fórmulas para calcular métricas de costes de mano de obra:

- **Coste planificado**: Coste estimado de todas las asignaciones de recursos en cada tarea de nodo hoja
- **Coste real**: suma de todos los costes reales por tiempo registrado en la tarea
- **Porcentaje de consumo de costes**: Coste real ÷ Estimación de coste al finalizar
- **Coste restante**: Estimación de coste al finalizar - Coste real
- **Coste al finalizar**: Coste restante + Coste real
- **Desviación de coste**: Coste planificado - Estimación de coste al finalizar

Cada tarea muestra una proyección de la variación de coste en la tarea. Si la estimación de costes al finalizar es mayor que el coste planificado, se proyecta que la tarea para que supere el presupuesto. Si la estimación de costes al finalizar es menor que el coste planificado, se proyecta la tarea para que se finalice por debajo del presupuesto.

>[!NOTE]
> Project Operations solo muestra los costes de mano de obra en la página **Proyecto** en la pestaña **Seguimiento**. Si bien los materiales y los gastos se pueden estimar y rastrear para el consumo, estos costes no se incluyen en los costes que se muestran en la pestaña **Seguimiento**. Esta pestaña está diseñada para funcionar solo para reproyectar costes de mano de obra por esfuerzo de reproyección.
Todos los importes de coste que se muestran se convierten a la divisa de coste del proyecto a partir de la divisa del precio de coste del proyecto que se utiliza para determinar la tasa de coste. La divisa de coste del proyecto es la divisa de la unidad contratante del proyecto. Los valores de coste estimados por tiempo que se muestran en la pestaña **Estimaciones** en la página **Proyecto** es posible que se sumen al coste planificado en la pestaña **Seguimiento**. La razón de esta discrepancia se debe a las diferencias de cómo se resume el coste estimado en la cuadrícula **Estimaciones** y cómo se calcula el coste planificado en la cuadrícula **Seguimiento**. 
>
> - La pestaña **estimaciones** calcula el coste estimado utilizando la misma divisa de la tasa de coste en la lista de precios. Luego, el coste estimado en la divisa de la lista de precios se convierte al coste estimado en la divisa de coste del proyecto. El coste estimado en la divisa del proyecto se muestra redondeado a 2 decimales. En ningún momento durante esta conversión se aplica la precisión de la divisa. 
> - En la pestaña **Seguimiento**, el cálculo del costo planificado sigue un orden de cálculo ligeramente diferente que implica la aplicación de la precisión de la divisa en dos etapas: 
   ><ol>
   ><li>El importe del coste estimado en la divisa de la lista de precios se convierte a la divisa base (conversión 1).</li>
   ><li>El importe del coste estimado en la divisa base se convierte a la divisa del coste del proyecto (conversión 2). </li>
   ></ol>
   >La precisión de la divisa se aplica en ambos pasos para obtener un coste planificado (en la pestaña **Seguimiento**) que se desvía ligeramente del coste estimado (en la vista **Tiempo - por fases** en la pestaña **Estimaciones**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Reproyección de costes en tareas de nodo hoja

Los costes de mano de obra en una tarea de nodo hoja no se pueden reproyectar directamente en la pestaña **Seguimiento** pestaña en la página **Proyecto**. Sin embargo, puede utilizar la vista **Seguimiento del esfuerzo** para reproyectar el esfuerzo restante en una tarea. Esto provoca un nuevo cálculo del coste restante de la tarea. Esta es una descripción de cómo funciona esto.

1. Un director de proyectos puede reproyectar el esfuerzo en las tareas actualizando el valor predeterminado en el campo **Esfuerzo restante** con una nueva estimación del esfuerzo restante en la tarea. La reproyección provoca un nuevo cálculo del esfuerzo estimado al finalizar (EEF) de la tarea, el porcentaje de progreso y la variación del esfuerzo proyectado en una tarea. La EEF, la estimación de finalización (ETC) y el porcentaje de progreso en las tareas de resumen también se recalculan y producen una nueva proyección de la variación del esfuerzo.
2. Basado en el nuevo valor para el esfuerzo restante en la tarea, el sistema calcula el coste restante en la vista **Seguimiento de costes**. Para calcular el coste restante basado en el esfuerzo restante, el sistema primero calcula el coste promedio de una hora de esfuerzo en la tarea como coste planeado o esfuerzo planeado. El coste planificado es la suma del coste de todas las asignaciones de recursos en la tarea. El coste promedio por hora se usa para calcular el coste restante de esfuerzo restante que se acaba de proyectar de la tarea.
3. El coste al finalizar y el porcentaje de consumo de costes en la tarea de nodo hoja se vuelven a calcular.
4. El valor del coste al finalizar de las tareas de resumen hasta el nodo raíz se vuelve a calcular.

## <a name="reprojecting-costs-on-summary-tasks"></a>Reproyección de costes en tareas de resumen

Puede reproyectar los costes laborales en tareas de resumen o tareas de contenedor. Sin embargo, no puede reproyectar directamente el coste de mano de obra en una tarea de proyecto de resumen en la pestaña **Seguimiento** en la página **Proyecto**. De forma similar a las tareas de nodo hoja, la reproyección de tareas de resumen y contenedor se puede realizar utilizando la vista **Seguimiento del esfuerzo**. En esta vista, puede reproyectar el esfuerzo restante en una tarea de resumen, lo que provoca un nuevo cálculo del coste restante en la tarea de resumen. Esta es una descripción de cómo funciona esto.

1. Un director de proyectos puede reproyectar el esfuerzo en las tareas de resumen actualizando el valor predeterminado en el campo del esfuerzo restante con una nueva estimación de la tarea. Esta actualización provoca un nuevo cálculo de la estimación de la tarea de resumen al finalizar (EEF), el porcentaje de progreso y la variación del esfuerzo proyectado en una tarea. El EAF, ETC y el porcentaje de progreso en las tareas de resumen también se recalculan y producen una nueva proyección de la variación del esfuerzo.
2. Basado en el nuevo valor para el esfuerzo restante en la tarea de resumen, el sistema calcula el coste restante en la vista **Seguimiento de costes**. Para calcular el coste restante basado en el esfuerzo restante, el sistema primero calcula el coste promedio de una hora de esfuerzo en la tarea de resumen como coste planeado o esfuerzo planeado. El coste promedio por hora se usa para calcular el coste del esfuerzo restante que se acaba de proyectar en la tarea de resumen.
3. El coste al finalizar y el porcentaje de consumo de costes en la tarea de resumen hoja se vuelven a calcular.
4. El nuevo coste al finalizar se distribuye a las tareas secundarias en la misma proporción que el coste planeado original de la tarea.
5. Se calcula el valor del coste al finalizar en cada una de las tareas individuales hasta llegar a las tareas del nodo hoja. Según este valor, las tareas secundarias afectadas hasta llegar a los nodos hoja tendrán su coste restante y el porcentaje de consumo de costes recalculados en función del valor del coste al finalizar. Este valor da como resultado una nueva proyección para la variación del coste de la tarea. 


El campo **Rendimiento de coste** se puede configurar a partir de los datos de seguimiento. Cuando la variación del coste para el nodo raíz en la vista **Seguimiento de costes** es negativa, puede establecer este campo en **Por debajo del presupuesto**. Cuando la variación de coste para el nodo raíz es positiva, puede establecer el valor en **Por encima del presupuesto**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
