---
title: Configurar plantillas de costes
description: Este tema proporciona información sobre cómo crear y usar plantillas de costes en Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f4a515db31a31028af4a60927ab360be6c261a3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013912"
---
# <a name="set-up-cost-templates"></a>Configurar plantillas de costes

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Este tema proporciona información sobre cómo crear y usar plantillas de costes en Project Operations. Una plantilla de coste determina:

- Las categorías de proyectos para las transacciones de previsión y reales que se incluirán en un porcentaje del cálculo de finalización del proyecto. El valor de porcentaje completado se usa a continuación para calcular cuántos ingresos se reconocen.
- Si el porcentaje completado se puede modificar si se calcula automáticamente.
- Si el porcentaje completado se calcula en función de importes o unidades.

## <a name="cost-template-example"></a>Ejemplo de plantilla de coste

Está trabajando en un proyecto de diseño de sitio web para un cliente en el que cobra una tarifa fija de 10 000 USD. Realiza una previsión de que se tardarán 100 horas (5000 USD) en completar el proyecto. También realiza una previsión de dos billetes de avión y cuatro noches en un hotel para viajes a la ubicación del cliente (1800 USD). Esto da como resultado un coste total previsto de 6800 USD.

Cuando ejecuta el proceso de reconocimiento de ingresos a precio fijo para crear una estimación al final del mes, descubre que ha trabajado 35 horas en el proyecto. Esto aún no incluye vuelos ni costes de hotel. También dispuso que un ayudante realizara cinco horas de investigación para el proyecto con un coste de 100 USD, que no había planeado.

Al calcular el valor de porcentaje completado para este proyecto, tiene las siguientes opciones para realizar:

- ¿Desea incluir todos los costes (horas y gastos) o solo horas?
- ¿Desea incluir todas las horas o solo las horas planificadas?
- ¿Desea calcular el porcentaje completado basándose en el coste en dólares de las horas planificadas (5000 USD) o simplemente en la cantidad de horas (100)?

Sus respuestas a estas preguntas determinan las opciones que establece en la plantilla de coste y las categorías que selecciona en las líneas de la plantilla de coste.

En la siguiente tabla se muestran los resultados de diferentes métodos de cálculo del valor de porcentaje completado para este escenario.

| Finalización basada en | Coste en dólares o unidades | Porcentaje completado | Cálculo |
| --- | --- | --- | --- |
| Todas las horas, sin gastos | Coste en dólares | 37 % 35 x 50 USD + 100 USD = 1850 USD 1850 USD/5000 USD |
| Todas las horas, sin gastos | Unidades de medida | 40 % | 40 horas/100 horas (incluidas cinco horas no planificadas) |
| Horas planificadas, sin gastos | Coste en dólares o unidad | 35 % | 35/100 horas o 35 x 50/5000 USD |
| Todas las horas y gastos | Coste en dólares | 27,2 % | 1850 USD /6800 USD |

Decidir qué enfoque tomar para crear una plantilla de coste puede depender de varias consideraciones:

- Si incluye horas no planificadas en la plantilla de coste, corre el riesgo de completar el 100 % antes de que finalice el proyecto. Esto se debe a que las horas reales serán superiores a las planificadas. Si usa cualquiera de los dos primeros métodos enumerados en la tabla, debe cambiar el plan (unidades previstas) cuando se dé cuenta de las desviaciones. En este caso, sumaría o restaría horas en función de su conocimiento de lo que se requiere para terminar el proyecto. Si el proyecto va a requerir otras 65 horas en completarse, agregaría cinco horas al plan para un total de 105. Si sabe que su ayudante va a dedicar otras cinco horas a investigación, el total será de 110 horas.
- Si usa el tercer método enumerado en la tabla, solo actualizará las horas planificadas para su propio tiempo, para mantener el cálculo del porcentaje completado preciso. Su rentabilidad cambiará cuando se registren horas no planificadas, pero permanecerá en una trayectoria de porcentaje completado conocido.
- Si utiliza el cuarto método enumerado en la tabla, el riesgo es que los gastos se produzcan en momentos irregulares y es posible que no se reflejen en su progreso de finalización. Por lo tanto, si se incluyen los gastos, pueden hacer que su porcentaje completado fluctúe más de lo deseable. Por ejemplo, debido a que aún no tomó un vuelo, su porcentaje completado fue del 27 por ciento en lugar del 35 por ciento o del 37 por ciento si tuviera que basar el cálculo solo en el tiempo. Si hubiera realizado un viaje durante dos noches y hubiera pronosticado con precisión los costes de vuelos y hotel, el porcentaje completado habría sido del 40,4 por ciento (1850 USD por mano de obra y 900 USD por gastos = 2750 USD/6800 USD = 40,4 por ciento). Por lo tanto, incurrir en los gastos de un solo viaje en avión cambiaría el porcentaje completado del 27 al 40 por ciento.

## <a name="create-cost-templates"></a>Crear plantillas de costes
Para crear plantillas de costes, siga estos pasos:

1. Para obtener acceso a las plantillas de costes, en el entorno de Dynamics 365 Finance, vaya a **Gestión de proyectos y contabilidad** > **Configuración** > **Estimaciones** > **Plantilla de coste**.
2. Seleccione **Nueva** para crear una plantilla de coste. Escriba un nombre y una descripción.
3. Proporcione el id. de línea de coste para cada tipo de transacción.
4. Seleccione un método de finalización predeterminado:

  - **Automático**: el porcentaje de finalización se calcula automáticamente en un proyecto. No se puede cambiar el valor resultante.
  - **Manual**: el porcentaje de finalización se calcula automáticamente en un proyecto. Se puede cambiar el valor resultante.

  > [!NOTE]
  > Para los cálculos manuales, el porcentaje de finalización se mantiene en **Cálculo manual** en la pestaña **General** de la página **Estimación**.

5. En **Finalización basada en**, seleccione uno de los siguientes valores:

  - **Importe**: el importe en divisa de contabilidad calcula el porcentaje de finalización.
  - **Unidad**: la cantidad calcula el porcentaje de finalización.
  - **Línea recta**: el sistema calcula el porcentaje de finalización de forma proporcional utilizando las fechas de inicio y finalización del proyecto para determinar la duración del proyecto.

6. Seleccione **Líneas de coste** para revisar las líneas de costes de la plantilla de coste. Se requiere al menos una línea de coste para cada tipo de transacción. Sin embargo, puede crear varias líneas de coste para los mismos tipos de transacciones y establecer los atributos deseados para estas líneas.
7. En la pestaña **Categorías**, seleccione las categorías de proyectos que se incluirán en la línea de la plantilla de coste.
8. En la pestaña **General**, seleccione si esta línea se incluirá en el cálculo del porcentaje de finalización.
9. Seleccione el método del coste de finalización que se utilizará al calcular el porcentaje de finalización.


[!INCLUDE[footer-include](../includes/footer-banner.md)]