---
title: Información general sobre estructuras de descomposición del trabajo
description: Una estructura de descomposición del trabajo (WBS) es una descripción del trabajo que se realizará para un proyecto. Es una jerarquía de tareas que representa la comprensión del equipo del proyecto sobre la composición del trabajo, y del tamaño, coste y duración de cada componente o tarea.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 713e38f4218b980c4256e433e90c12adccd70e11
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012247"
---
# <a name="work-breakdown-structures-overview"></a>Información general sobre estructuras de descomposición del trabajo

[!include [banner](../includes/banner.md)]

Una estructura de descomposición del trabajo (WBS) es una descripción del trabajo que se realizará para un proyecto. Es una jerarquía de tareas que representa la comprensión del equipo del proyecto sobre la composición del trabajo, y del tamaño, coste y duración de cada componente o tarea. Una WBS tiene tres objetivos principales:

-   Describe el desglose o composición del trabajo en tareas.
-   Programa el trabajo del proyecto.
-   Estima el coste de cada tarea.

El grado de detalle en una WBS depende del nivel de precisión que se requiera en las estimaciones y el nivel de seguimiento que se requiera frente a esas estimaciones. Los proyectos que tienen una tolerancia muy baja a los retrasos en el programa o el coste generalmente requieren una WBS más detallada y un seguimiento diligente del progreso del trabajo y el coste con respecto a la WBS. Este tipo de proyecto es común en los sectores de la construcción y la ingeniería. 

Por el contrario, los proyectos en sectores como los medios y la publicidad, el software y la infraestructura de TI tienden a ser únicos, y la productividad está relacionada con la experiencia y competencia del individuo que realiza la tarea. Por lo tanto, estos sectores usan una WBS para obtener una aproximación del tamaño de un proyecto, no para rastrear el progreso de ese proyecto en detalle. 

La construcción de una WBS es un proceso intensivo que generalmente se lleva a cabo durante un período prolongado y que requiere la colaboración y la información de una amplia variedad de personas. Este tema describe cómo puede utilizar las mejoras de WBS para cumplir con sus requisitos de estimaciones y seguimiento.

## <a name="prerequisites-for-creating-a-wbs"></a>Requisitos previos para crear una WBS
Para crear una WBS, debe poder crear un programa de trabajo y estimar el coste del trabajo.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Requisitos previos para crear un programa de trabajo

Para utilizar todas las funcionalidades de la programación de las características de WBS, complete la siguiente configuración:

1.  Configure un calendario predeterminado y un calendario de proyecto:
    1.  Haga clic en **Gestión y contabilidad de proyectos** &gt; **Configuración** &gt; **Parámetros de gestión de proyectos y contabilidad** &gt; **Programación**. En el campo **Calendario de trabajo predeterminado**, especifique un calendario predeterminado. Este será el calendario laboral predeterminado para cualquier proyecto nuevo que se cree.
    2.  Puede cambiar el calendario predeterminado para un proyecto específico. Haga clic en la página de detalles del proyecto y luego, en la ficha desplegable **Equipo de proyecto y programación**, actualice el campo **Calendario de programación** seleccionando otro calendario.

2.  Configure días laborables estándar y horas laborables. El calendario que establezca como calendario de trabajo para su proyecto se utilizará en la WBS para determinar la siguiente información:

-   Días laborables y festivos
-   El número de horas de trabajo en un día.

Para configurar los días laborables y las horas laborables de un calendario, o para crear un calendario nuevo, haga clic en **Administración de la organización** &gt; **Común** &gt; **Calendarios**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Requisitos previos para estimar el coste del trabajo

Para utilizar todas las capacidades de estimación de costes de la WBS, debe configurar los costes y los precios de venta para los trabajadores, las categorías de mano de obra, los gastos, las tarifas y los artículos.

-   Para configurar el coste y el precio de venta de las categorías de mano de obra, gastos y tarifas, haga clic en **Gestión de proyectos y contabilidad** &gt; **Configuración** &gt; **Precios**.
-   Para configurar el coste y el precio de venta de los artículos, use la página **Contratos comerciales** para cada elemento de página de la lista **Productos emitidos** en Gestión de información de productos.

## <a name="creating-a-wbs"></a>Crear un WBS
La creación de una WBS implica tres actividades:

1.  **Descomposición del trabajo**: cree un desglose del trabajo en partes o tareas manejables.
2.  **Horario de trabajo**: estime el tiempo necesario para completar una tarea, establezca las interdependencias de tareas y seleccione las fechas de inicio y finalización de las tareas.
3.  **Estimación de costes**: estimar costes para cada tarea.

Las siguientes secciones tratan cómo las capacidades de WBS pueden ayudar con cada una de estas actividades.

### <a name="work-decomposition"></a>Descomposición del trabajo

Crear un desglose o descomposición del trabajo suele ser el primer paso en el proceso de creación de una WBS. La funcionalidad WBS admite las siguientes construcciones básicas para el desglose o descomposición del trabajo. 

**Tarea raíz del proyecto**: la tarea raíz del proyecto es la tarea de resumen de nivel superior de un proyecto. El resto de las tareas del proyecto se crean por debajo. El nombre de la tarea raíz se establece siempre en el nombre del proyecto. El esfuerzo, las fechas y la duración del nodo raíz resumen los valores de las tareas por debajo de la tarea raíz. No puede modificar las propiedades del nodo raíz ni eliminarlo.

**Tareas de resumen o contenedor**: una tarea de resumen es una tarea que tiene tareas secundarias o tareas constituyentes debajo de ella. Una tarea de resumen no tiene ningún esfuerzo de trabajo ni coste propio. En cambio, el esfuerzo laboral y el coste de una tarea de resumen son la suma del esfuerzo laboral y el coste de las tareas que la constituyen. La primera fecha de inicio de la tarea constitutiva se utiliza como la fecha de inicio de las tareas del resumen, y la última fecha de finalización de las tareas constituyentes se usa como fecha de finalización. Puede modificar el nombre de una tarea de resumen, pero no puede modificar las propiedades de programación para esfuerzo, fechas y duración. Si elimina una tarea de resumen, también se eliminan todas sus tareas constituyentes. 

**Tareas del nodo hoja**: una tarea de nodo hoja representa el paquete de trabajo más granular del proyecto. Un nodo hoja tiene un esfuerzo estimado, un número previsto de recursos, fechas de inicio y finalización planeadas, y una duración. 

Puede completar las siguientes operaciones de jerarquía para permitir la creación de una jerarquía de trabajo o la descomposición de un proyecto. 

**Nueva tarea**: cualquier tarea nueva que cree se agrega automáticamente bajo el nodo raíz y se asigna automáticamente un número de WBS a la tarea. El número de WBS representa el nivel de la tarea en la jerarquía. Para las tareas en el primer nivel bajo la tarea raíz del proyecto, se utiliza un esquema de numeración de 1, 2, 3, etc. Para las tareas bajo el primer nivel, se usa un esquema de numeración de 1.1, 1.2, 1.3, etc. Para cada nivel que se agrega a un nivel anterior, se agrega una nueva serie de números con puntos. 

Actualmente, no puede personalizar la numeración de la WBS. 

**Tarea de sangría**: cuando aplica sangría a una tarea, se convierte en un elemento secundario de la tarea que la precede. El número de WBS de la nueva tarea secundaria se vuelve a calcular automáticamente en función del número del WBS de su nuevo elemento principal. La tarea principal es ahora una tarea de resumen o contenedor y, por lo tanto, se convierte en un resumen de sus tareas constituyentes. 

> [!NOTE] 
> Cuando aplica sangría a tareas en una tarea que era un nodo hoja antes de la operación de sangría, la tarea de resumen recién creada pierde sus propias fechas, esfuerzo y cantidad de recursos. Ahora utiliza un resumen de los valores de sus nuevas tareas constituyentes. 

**Tarea de sangría anulada**: cuando anula la sangría de una tarea, ya no es una tarea constituyente de su elemento principal. El número de WBS de esta tarea se vuelve a calcular automáticamente para reflejar el nuevo nivel de la tarea en la jerarquía. El esfuerzo, el coste y las fechas de las tarea principal anterior se vuelven a calcular para que excluir esa tarea. 

**Subir y bajar**: cuando hace clic en **Subir** y **Bajar**, cambia la posición de una tarea dentro de la jerarquía de su elemento principal. La posición de una tarea no afecta el esfuerzo, el coste, las fechas o la duración de la tarea. Sin embargo, el número de WBS de la tarea se vuelve a calcular automáticamente para reflejar su nueva posición.

### <a name="schedule-estimation"></a>Estimación de la programación

La estimación de la programación suele ser el segundo paso en la creación de una WBS. Se recomienda completar la estimación de la programación después de crear las tareas. La página **Estructura de descomposición del trabajo** de Finance tiene dos secciones. El panel superior está destinado a la estimación de los horarios, y el panel inferior incluye una pestaña **Costes e ingresos estimados** que puede utilizar para la estimación de costes. 
**Dependencias de tareas**: en una WBS, puede crear una relación predecesora entre tareas. Cuando asigna tareas predecesoras a una tarea, esta solo puede iniciarse tras completar todas las tareas predecesoras. La fecha de inicio planificada de la tarea se establece automáticamente en la última fecha de todos sus predecesores. 

**Programación de tareas**: los siguientes factores determinan la programación de las tareas del nodo hoja:

-   Predecesores
-   Esfuerzo
-   El número de recursos
-   Fechas de inicio y finalización

La fecha de inicio de una tarea del nodo hoja que no tiene valores predecesores se establece automáticamente en la fecha de inicio de programación del proyecto. La duración de una tarea de nodo hoja siempre se calcula como el número de días laborables entre sus fechas de inicio y finalización. 

*<strong><em>Reglas de programación</em></strong>*: cuando la asistencia de programación automática está activada, las siguientes reglas se aplican a la programación de tareas para las tareas del nodo hoja:

-   Las fechas de inicio y finalización de una tarea deben ser días laborables, según el calendario de programación del proyecto.
-   La fecha de inicio de una tarea que tiene predecesoras se establece automáticamente en la última fecha final de todas sus predecesoras.
-   El esfuerzo de una tarea se calcula automáticamente de la siguiente manera:

Número de personas × Duración × Número de horas en un día laborable estándar de calendario del proyecto. 

En algunos casos, es posible que desee desviarse de estas reglas. Puede desactivar la programación automática para evitar que Finance establezca o corrija automáticamente las propiedades de las tareas del nodo hoja. Cuando especifica información para una tarea que causa una infracción de las reglas de programación, se muestra un icono de error de programación para la tarea. Si no desea que se muestren los errores de programación, haga clic en **Se muestran los errores de programación** para desactivar la función. 

> [!NOTE] 
> Los valores de una tarea de resumen o contenedor se siguen calculando como la suma de los valores de las tareas que la componen, independientemente de si la asistencia de programación automática está activada o desactivada. 

**Solucionar errores de programación**: cuando la asistencia de programación automática está activada, no es probable que se produzcan errores de programación. Sin embargo, si desactiva la asistencia de programación automática y luego la vuelve a activar, es posible que aparezcan iconos de error de programación en la WBS. 

**Corregir errores de programación por tarea**: cuando hace doble clic en el icono de error de programación para una tarea específica, un cuadro de diálogo muestra todos los errores de programación para esa tarea. Puede decidir qué errores de programación corregir para la tarea. 

**Corrección de todos los errores de programación**: si desea que Finance corrija todos los errores de programación en la WBS, en el Panel de acciones, haga clic en **Corregir todas las discrepancias de programación**. 

> [!NOTE] 
> Esta función puede provocar modificaciones importantes en la WBS. Los errores se corrigen en el siguiente orden:

1.  El esfuerzo estimado en todas las tareas se modifica para que sea igual a la capacidad definida en el calendario del proyecto.
2.  La fecha de inicio de cada tarea se modifica para que la tarea comience después de que se completen todas sus tareas predecesoras.
3.  La fecha de inicio de cada tarea se modifica para eliminar los huecos en las fechas de inicio de las tareas predecesoras.

### <a name="cost-estimation"></a>Estimación de costes

Como se mencionó anteriormente en este documento, usted especifica la estimación de coste para cada tarea de nodo hoja usando la pestaña **Costes e ingresos estimados** en el panel inferior de la página **Estructura de descomposición del trabajo**. 

> [!NOTE] 
> No puede modificar la estimación de coste de una tarea de resumen o contenedor. La estimación de coste de una tarea de resumen es igual a la suma de la estimación de coste de sus tareas de nodo hoja. El coste total estimado de cada tarea se calcula como la suma de los importes de coste estimados de los siguientes tipos de transacciones:

-   Mano de obra
-   Artículo o material
-   Gastos

Una tipo de transacción de **Tarifa** se utiliza para estimar los ingresos basados en tarifas. Este tipo de transacción no tiene un componente de coste y, por lo tanto, no se considera cuando se calculan los costes. 

Un tipo de transacción **En cuenta** se utiliza para registrar el valor de las ventas contratadas en un tipo de proyecto de valor fijo. Este tipo de transacción tampoco se considera cuando se calculan los costes. 

Cuando calcula los costes de mano de obra, materiales y gastos de cada tarea, debe asignar una categoría de proyecto al coste estimado. 

**Estimación de costes laborales**: para cada tarea de nodo hoja, asigna un esfuerzo de trabajo en horas y una categoría predeterminada. Por lo tanto, al configurar el programa de una tarea, la estimación del coste laboral de dicha tarea se agrega automáticamente a la categoría predeterminada de mano de obra. Esta estimación de coste aparece en la pestaña **Costes e ingresos estimados** de la cuadrícula **Detalles de línea** de dicha tarea. Si necesita más estimaciones de costes laborales, puede agregarlas en esta pestaña. Si aumentan o disminuyen las horas en la estimación del coste de mano de obra, la programación de la tarea se vuelve a calcular automáticamente. 

**Estimación de gastos y costes de materiales**: la pestaña **Costes e ingresos estimados** también le permite estimar los gastos y los costes de materiales para una tarea, si necesita estimaciones. 

El coste y el precio de venta para cada línea de estimación de mano de obra o gastos se basan en la configuración que se define para cada categoría en las tablas de precios en **Gestión de proyectos y contabilidad** &gt; **Configuración** &gt; **Precios**. Los artículos, el coste y el precio de venta se agregan de forma predeterminada desde el artículo o los contratos comerciales en la página de la lista **Productos emitidos** en Gestión de información de productos.

## <a name="tracking-progress-on-the-wbs"></a>Seguimiento del progreso en la WBS
Algunos sectores rastrean el progreso de un proyecto relativo a una WBS a un nivel muy granular, mientras que otros rastrean el progreso a un nivel superior de la WBS. Esta sección describe cómo puede utilizar el seguimiento WBS para los requisitos de su proyecto. 

Finance tiene tres vistas para la WBS de un proyecto: la vista de planificación, la vista de seguimiento de esfuerzos y la vista de seguimiento de costes.

### <a name="planning-view"></a>Vista de planificación

La vista de planificación muestra la estimación planificada o de referencia de la programación y la información de costes. Aunque no hay funciones para realizar un seguimiento de la versión y la línea base de una WBS del proyecto, los valores de esta vista están destinados a representar la versión de referencia. Las secciones Estimación de programación y Estimación de costes de este tema describen esta vista y cómo se usa para crear una WBS.

### <a name="effort-tracking-view"></a>Vista de seguimiento del esfuerzo

La vista de seguimiento del esfuerzo muestra el seguimiento del progreso para las tareas en la WBS. Compara las horas de esfuerzo reales acumuladas para una tarea con las horas de esfuerzo planificadas. Las siguientes fórmulas proporcionan los valores en la vista de seguimiento de esfuerzos:

-   Porcentaje de progreso = Esfuerzo real hasta la fecha ÷ Esfuerzo planificado para la tarea
-   Esfuerzo restante (también conocido como Estimación para completar \[EPC\]) = Esfuerzo planificado - Esfuerzo real hasta la fecha
-   Estimación al finalizar (EAF) = Esfuerzo restante + Esfuerzo real hasta la fecha
-   Variación del esfuerzo proyectado = Esfuerzo planificado - EAF

La vista de seguimiento del esfuerzo muestra una proyección de la variación del esfuerzo para la tarea, según si el EAF es mayor o menor que el esfuerzo planificado:

-   Si el EAF es superior al esfuerzo planificado, se prevé que la tarea tardará más tiempo del planificado originalmente y se retrasa la programación.
-   Si el EAF es inferior al esfuerzo planificado, se prevé que la tarea tardará menos tiempo del planificado originalmente y se adelanta la programación.

**Volver a proyectar el esfuerzo del jefe de proyecto**: ocasionalmente, el jefe del proyecto u otra persona que esté siguiendo el progreso de un proyecto tendrá que revisar las estimaciones originales de una tarea. Es posible que la tarea esté avanzando más rápido o más lento de lo previsto originalmente por varias razones. Por ejemplo, el alcance se ha reducido o los trabajadores tienen menos experiencia de la planificada originalmente. Las proyecciones son la percepción de las estimaciones de un jefe de proyecto según estado actual de un proyecto. En general, no debería cambiar los números de referencia, porque la línea de base del proyecto representa un documento bien publicado para la programación de proyecto y las estimaciones de costes que todas las partes interesadas en el proyecto han aceptado. 

Existen dos formas en las que los jefes de proyecto pueden modificar el esfuerzo en las tareas:

-   Modifique el esfuerzo restante que se establece automáticamente para actualizar el esfuerzo restante real en la tarea.
-   Modifique el porcentaje del progreso que se establece automáticamente para actualizar el progreso real en la tarea.

Cada uno de estos enfoques genera un nuevo cálculo del EPC, EAF y porcentaje de progreso de la tarea, y la variación del esfuerzo proyectado en la tarea. El EAF, EPC y el porcentaje de progreso en las tareas de resumen también se recalculan y se actualiza la variación del esfuerzo proyectado. 

**Esfuerzo modificado en tareas de resumen**: puede modificar el esfuerzo en tareas de resumen o contenedor. Independientemente de si modifica estos valores mediante el esfuerzo restante o el porcentaje de progreso en las tareas de resumen, los cálculos se producen de forma automática en el siguiente orden:

1.  Se calculan el EAF, el ETC y el porcentaje de progreso en la tarea.
2.  El nuevo EAF se distribuye a las tareas secundarias en la misma proporción que el importe del EAF original.
3.  Se calcula el nuevo EAF en cada tarea de nodo hoja.
4.  El esfuerzo restante y el porcentaje de progreso se vuelven a calcular para todas las tareas secundarias afectadas, según el nuevo valor de EAF. También se vuelve a calcular la variación del esfuerzo de las tareas.
5.  El EAF de las tareas de resumen también se vuelve a calcular a partir de los nodos hoja.

Haga clic en **Expandir al nivel** en la vista de seguimiento del esfuerzo para establecer el nivel en el que realizar el seguimiento y mantener su WBS. La WBS se expande automáticamente a ese nivel en la vista de seguimiento del esfuerzo cada vez que la abre.

### <a name="cost-tracking-view"></a>Vista de seguimiento de costes

La vista de seguimiento de costes muestra el seguimiento del consumo de costes de una tarea. En esta vista, el coste real que se ha gastado en una tarea hasta la fecha se compara con el coste planificado para la tarea. Las siguientes fórmulas proporcionan los valores en la vista de seguimiento de costes:

-   Porcentaje del coste consumido = Coste real hasta la fecha ÷ Coste planificado para la tarea
-   Coste de finalización (CTC) = Coste planificado - Coste real hasta la fecha
-   Estimación al finalizar (EAF) = CTC + coste real hasta la fecha
-   Variación del coste proyectado = coste planificado - EAF

La vista de seguimiento del coste muestra una proyección de la variación del coste para la tarea, según si el EAF es mayor o menor que el coste planificado:

-   Si el EAF es superior al coste planificado, se prevé que la tarea usará más dinero del planificado originalmente y se sobrepasa el presupuesto.
-   Si el EAF es inferior al coste planificado, se prevé que la tarea usará menos dinero del planificado originalmente y se queda por debajo del presupuesto.

**Volver a proyectar el coste del jefe de proyecto**: los jefes de proyecto deben usar CTC para revisar la estimación de costes original de una tarea. El jefe de proyecto puede modificar el valor de CTC al coste que se requiere para completar la tarea. Si modifica el valor de CTC, se recalculan el CTC, el EAF y el porcentaje de coste consumido de la tarea, y la variación de coste proyectada en una tarea. El EAF, EPC y el porcentaje de coste consumido en las tareas de resumen también se recalculan y se actualiza la variación del coste proyectado. 

> [!NOTE] 
> Cuando revisa el esfuerzo para una tarea WBS en la vista de seguimiento del esfuerzo, el CTC, EAF, el porcentaje de coste consumido y la variación de coste proyectada de la tarea se recalculan en la vista de seguimiento de costes. Sin embargo, las revisiones de costes no afectan a los valores en la vista de seguimiento del esfuerzo, porque el coste por tipo de transacción (mano de obra, material o gasto) o categoría de proyecto no se revisa. 

**Revisión de la proyección de costes en tareas de resumen**: puede revisar los costes en las tareas de resumen y los cálculos se realizan automáticamente en el siguiente orden:

1.  Se vuelven a calcular el EAF, CTC y el porcentaje de coste consumido en la tarea.
2.  El nuevo EAF se distribuye a las tareas secundarias en la misma proporción que el EAF original de las tareas.
3.  Se calcula el nuevo EAF para cada tarea.
4.  El CTS y el porcentaje de coste consumido se vuelven a calcular para las tareas secundarias afectadas, según el valor de EAF. También se vuelve a calcular la variación del coste de las tareas.
5.  El EAF de todas las tareas de resumen se vuelve a calcular en función de este cambio.

Haga clic en **Expandir al nivel** en la vista de seguimiento del coste para establecer el nivel en el que realizar el seguimiento y mantener su WBS. La WBS se expande a ese nivel en la vista de seguimiento del coste cada vez que la abre.

### <a name="earned-value-management"></a>Gestión del valor ganado

Puede utilizar el método de valor ganado (EVM) para realizar un seguimiento del progreso de un proyecto. Puede ver las métricas de valor ganado en el Centro de roles de jefe de proyecto. El componente de la tabla de valor ganado muestra los valores de las fases de tiempo del valor planificado y el coste real. El valor ganado a la fecha actual se muestra como un punto. Actualmente, no están disponibles los datos por fases de tiempo para el valor ganado. 

La fase de tiempo en el gráfico de valor ganado se muestra por semana o por mes. Esta sección describe los tres pilares de EVM: valor planificado, valor ganado y coste real. 

**Valor planificado**: la teoría de EVM establece que la gráfica de valor planeado representa el índice al que el equipo del proyecto planeó ganar valor en el proyecto. 

Finance usa la regla de ganancia 0:100 cuando traza el valor planificado. Según esta regla, el valor de la tarea se publica en la tarea a partir de su fecha de finalización. No se publica ningún valor hasta que la tarea se completa al 100 %. 

En Gestión de proyectos y contabilidad, especifique la fecha de finalización de los nodos hoja y el coste planificado para ellos. Cuando el gráfico del valor planificado se muestra por semana, el valor planificado se resume por semana para todas las tareas del nodo hoja durante la duración del proyecto. 

**Valor obtenido**: la teoría de EVM establece que la gráfica de valor obtenido representa el índice al que el equipo del proyecto está obteniendo valor en el proyecto. 

Finance usa la regla de ganancia 0:100 cuando traza el valor obtenido. Según esta regla, el valor de la tarea se publica en la tarea a partir de su fecha de finalización. No se publica ningún valor hasta que la tarea se completa al 100 %. 

Cuando se calcula el valor obtenido, se considera el porcentaje de progreso de cada tarea. Según la regla de ganancia de 0:100, solo las tareas que se completan en un período determinado se consideran para el cálculo del valor obtenido al final de ese período. El valor obtenido en el proyecto se calcula para todas las tareas que se completaron cuando se crea el gráfico. 

> [!NOTE] 
> Actualmente, el sistema para el seguimiento de WBS no tiene estructuras de datos para almacenar porcentajes de progreso histórico en cada tarea. Por lo tanto, el valor obtenido solo se puede notificar a partir del momento en que se procesa el cubo. Procese el cubo con regularidad para actualizar los datos de valor obtenido que se muestran en el Área de trabajo. 

**Coste real**: la teoría de EVM establece que la gráfica de coste real representa la tasa a la que se gasta el dinero en el proyecto. 

Las transacciones que se registran en un proyecto se utilizan para trazar la línea de coste real. Los costes se resumen por fecha. Luego, estos datos se utilizan para crear gráficos de los costes reales por semana o por mes en la tabla de valor ganado.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Cómo utilizar los conceptos de valor planificado, valor ganado y coste real

**Variación del programa**: durante la planificación, crea una previsión para el trabajo en una escala de tiempo. Por lo tanto, el valor planificado es el ritmo al que los planificadores del proyecto pensaron que se completaría el trabajo en el proyecto. Una vez que un proyecto está en progreso, el trabajo se completa y el proyecto gana valor. Al comparar el valor planificado con el valor obtenido, puede ver cómo avanza el trabajo en un proyecto. El resultado de esta comparación se llama variación del programa. 

Si el valor planificado para un período es mayor que el valor obtenido, la cantidad de trabajo que se ha realizado en un proyecto es menor que la planificada. Por lo tanto, el proyecto está retrasado. Debido a que el valor planificado y el valor obtenido se expresan en términos monetarios, el tiempo de demora del proyecto también recibe un valor monetario. 

Si el valor planificado para un período es menor que el valor obtenido, la cantidad de trabajo que se ha realizado en un proyecto es mayor que la planificada. Por lo tanto, el proyecto está adelantado. A este plazo también se le asigna un valor monetario.

**Variación de coste**: debido a que el valor obtenido usa el precio de costo como multiplicador, el valor obtenido indica el coste del trabajo que se realiza en un proyecto. A medida que avanza un proyecto, el registro de transacciones proporciona un registro del dinero que realmente se gasta en ese proyecto. Al comparar el valor ganado con el coste real, puede ver la cantidad de dinero que se gasta frente al valor que se gana. El resultado de esta comparación se llama variación del coste. 

Si el coste real que se gasta durante un período es mayor que el valor obtenido, se gastó más dinero del que se ganó. Por lo tanto, el proyecto está por encima del presupuesto. 

Si el coste real que se gasta durante un período es menor que el valor obtenido, se ganó más dinero del que se gastó. Por lo tanto, el proyecto está por debajo del presupuesto.

## <a name="wbs-templates"></a>Plantillas de WBS
Puede utilizar la funcionalidad de plantillas WBS para crear plantillas estándar para proyectos. Si los proyectos que ofrece su empresa implican mucho trabajo repetible, debería considerar la posibilidad de crear una plantilla de WBS. 

Puede crear una plantilla de WBS a partir de la WBS de un proyecto existente, de modo que el conocimiento y las prácticas recomendadas que recopiló durante la planificación de ese proyecto se puedan reutilizar en proyectos similares en el futuro. Sin embargo, a veces, puede que no tenga sentido guardar toda la WBS como plantilla. Por lo tanto, también puede crear plantillas a partir de partes de la WBS para un proyecto.

### <a name="saving-a-projects-wbs-as-a-template"></a>Guardar la WBS de un proyecto como plantilla

Después de crear una plantilla, puede importarla a la WBS de un nuevo proyecto en el nodo raíz o en cualquier tarea de la WBS del proyecto.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importar una plantilla WBS a la WBS de un proyecto

Cuando importa tareas, las tareas de la plantilla se organizan en función de la fecha de inicio de la tarea en la que se importan. Durante la importación, las relaciones del predecesor en las tareas de la plantilla se utilizan para calcular las fechas de inicio de las tareas importadas. El calendario laboral estándar del proyecto de destino se aplica para calcular las fechas de finalización de las tareas importadas, de modo que se conserven los días laborables y las horas laborables estándar que se definen en el calendario laboral del proyecto actual. 

Los importes de los costes y los precios de venta en las líneas de estimación se aplican para garantizar que los precios que son específicos del proyecto o contrato del proyecto tengan fechas válidas.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Diferencias entre la WBS de un proyecto y una plantilla de WBS

-   Las tareas en las plantillas de WBS no tienen fechas de inicio ni de finalización.

Los días laborables y no laborables no están configurados para las plantillas de WBS.

-   Las plantillas de WBS siempre usan el calendario de programación que está configurado como el calendario predeterminado para todos los proyectos.

El calendario de programación predeterminado se usa solo para averiguar las horas en un día laboral estándar.

-   Las relaciones del predecesor no se copian en una plantilla WBS.

Debido a que las plantillas de WBS no tienen fechas, la lógica de fecha de inicio que se basa en la fecha de finalización de un predecesor no es necesaria.

-   Se crea automáticamente una línea de estimación de costes laborales cuando se crea una tarea en una plantilla WBS. El precio de venta y el importe del coste se copian desde el trabajador seleccionado.

Los costes de gastos y artículos se pueden crear manualmente, al igual que en la WBS de un proyecto.

-   Los errores de programación se muestran cuando hay desviaciones desde la siguiente fórmula:

Esfuerzo = Número de recursos × Duración × Número de horas en una jornada laboral estándar 

Puede corregir todos los errores de programación al mismo tiempo haciendo clic en **Corregir todos los errores de programación**. 

Como alternativa, puede corregir los errores de programación individualmente haciendo clic en el icono de advertencia de cada tarea.





[!INCLUDE[footer-include](../includes/footer-banner.md)]