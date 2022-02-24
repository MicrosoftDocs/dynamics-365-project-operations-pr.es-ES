---
title: Programar un proyecto con una estructura de descomposición del trabajo
description: Cómo programar un proyecto con una estructura de descomposición del trabajo en Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149834"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Programe un proyecto con una estructura de descomposición del trabajo (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Una programación del proyecto comunica el trabajo debe realizarse, qué recursos realizarán el trabajo, y el calendario en el que debe completarse ese trabajo. La programación del proyecto refleja todo el trabajo asociado con la entrega del proyecto a tiempo. Uno de los primeros pasos en la fase de inicio del proyecto es elaborar una programación del proyecto. Para establecer una programación del proyecto, necesita crear una estructura de descomposición del trabajo.  
  
 Cree una estructura del proyecto con una estructura de descomposición del trabajo, lo que le ayuda a:  
  
- Desglosar el trabajo en tareas manejables  
  
- Estimar el tiempo necesario para completar una tarea  
  
- Establecer dependencias y duración de tareas  
  
- Determinar los roles necesarios para realizar cada tarea  
  
  La programación del proyecto en la estructura de descomposición del trabajo tiene una apariencia familiar e incluye un gráfico de Gantt interactivo.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Cree una estructura de descomposición del trabajo para un proyecto  
 Cree una estructura de descomposición del trabajo para representar la secuencia de tareas en un proyecto. La estructura de descomposición del trabajo incluye tareas, requisitos para cada tarea, y la información de los ingresos y costos. En la estructura de descomposición del trabajo, puede agregar:  
  
-   La secuencia de tareas en una jerarquía  
  
-   Otras tareas, en su caso, que deben completarse antes de que se pueda iniciar una tarea  
  
-   La fecha inicial, la fecha de finalización, y la duración de una tarea  
  
-   El número de horas necesarias para una tarea  
  
-   Las cualificaciones y educación necesarias de un trabajador  
  
-   Los trabajadores que están asignados a una tarea  
  
-   Ingresos y costes estimados  
  
## <a name="task-types"></a>Tipos de tarea  
Usará los siguientes tipos de tareas al crear la estructura de descomposición del trabajo:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nodo raíz del proyecto**. | La tarea de resumen de nivel superior del proyecto. El resto de las tareas del proyecto se crean por debajo. El nombre de la tarea raíz es el nombre del proyecto. El esfuerzo, fechas, y la duración del nodo raíz se basan en los valores de la jerarquía por debajo de él. No puede editar propiedades del nodo raíz ni eliminar el nodo raíz. | 
| **Tareas de informe o contenedor** | Una tarea de resumen es una tarea que tiene subtareas por debajo. Una tarea de resumen no tiene ningún esfuerzo de trabajo ni coste propio. Su esfuerzo y costo de trabajo son un resumen de sus subtareas. Puede cambiar el nombre de una tarea de resumen, pero no puede cambiar el esfuerzo, las fechas o la duración porque se calculan automáticamente. La eliminación de una tarea de resumen elimina la tarea y todas sus subtareas.|  
| **Tareas del nodo hoja** | Una tarea del nodo hoja representa el trabajo más detallado en el proyecto. Tiene un esfuerzo estimado, un número previsto de recursos, fechas de inicio y finalización planeadas, y una duración.|

  
## <a name="task-hierarchy"></a>Jerarquía de tarea  
 Tiene las siguientes opciones cuando cree una jerarquía de tareas:  
  
- **Agregar tarea**.   Puede agregar una tarea en una posición que elija en la jerarquía de tareas. Si no selecciona una posición, la nueva tarea aparece al final.  
  
- **Aplicar sangría a tarea**.   Aplique sangría una tarea para convertirla en secundaria de la tarea directamente por encima de ella.  
  
- **Anular sangría de tarea**.   Anule la sangría de una tarea para que deje de ser una subtarea de su tarea principal original.  
  
- **Subir y bajar**.   Suba y baja tareas en la jerarquía de su tarea primaria. Subir o bajar una tarea no tiene ningún efecto en su esfuerzo, costo, fechas, o duración.  
  
## <a name="task-attributes"></a>Atributos de tareas  
 Un nombre de tarea describe el trabajo que debe completarse. Use diferentes atributos de tarea para describir la programación y los requisitos de personal para la tarea.  
  
### <a name="schedule-attributes"></a>Atributos de programación

 - Asigne valores a **Horas de esfuerzo**, **Número de recursos**, **Fecha de inicio**, **Fecha de finalización**, **Duración** para determinar la programación de la tarea. 
 - **Esfuerzo** es una estimación de las horas que se tarda en llevar a cabo la tarea.
 - **Número de recursos** es cálculo que el jefe del proyecto incluye en la tarea para ayudar a elaborar la programación mejor posible. 
 - **Duración** (en días) indica el número de días laborables que se requiere para llevar a cabo la tarea.  
  
### <a name="staffing-attributes"></a>Atributos de personal

 - **Rol**, **Unidad organizativa de recursos**, **Número de recursos** y **Recursos** describen los requisitos de personal para la tarea. 
 - **Rol** describe el tipo de recurso necesario para llevar a cabo la tarea. 
 - **Unidad organizativa de recursos** indica la unidad organizativa de la que debe obtenerse de recursos de personal para esa tarea; esto también afecta a la estimación costes y ventas de la tarea, ya que se contabiliza al determinar el precio de venta unitario para el recurso. 
 - **Recursos** contiene un recurso genérico o un recurso con nombre cuando se encuentra uno.  
  
## <a name="task-dependencies"></a>Dependencias de tarea  
 Puede crear relaciones de predecesor entre una o varias tareas en la estructura de descomposición del trabajo. Puede establecer uno o varios valores del campo de predecesor en tareas para indicar las tareas de las que dependerá. Cuando asigna un valor de predecesora a una tarea, la tarea solo se puede iniciar cuando todas las tareas predecesoras se han completado. Establecer esta dependencia en una tarea producirá el recálculo de la fecha de inicio planeada de la tarea como el último final de todos sus predecesoras. Los impactos relacionados con las predecesoras en una programación no están limitados por el modo de tarea definido en la tarea.  
  
## <a name="task-mode"></a>Modo de tarea  
 El modo de tarea es uno de los factores importantes que determinan las tareas del nodo hoja de programación. Hay dos modos de tarea para cada tarea: modo de programación automática y modo de programación manual.  
  
-   **Programación automática**.   Cuando se establece el modo de tarea en Programado automáticamente, el motor de programación de tareas usa las reglas de programación en los siguientes atributos de tarea para determinar la programación de la tarea:  
  
    -   Predecesoras  
  
    -   Esfuerzo  
  
    -   Número de recursos  
  
    -   Fechas de inicio y finalización  
  
-   **Reglas de programación**.   La fecha de inicio de una tarea del nodo hoja que no tiene valores predecesores utiliza de manera predeterminada la fecha de inicio de programación del proyecto. La duración de una tarea del nodo hoja se calcula siempre como el número de días laborables entre sus fechas de inicio y finalización. Cuando una tarea se programa automáticamente, el motor de programación sigue estas reglas:  
  
    -   Las fechas de inicio y finalización de una tarea deben siempre ser días laborables según el calendario de programación del proyecto  
  
    -   La fecha de inicio de una tarea que tiene predecesoras utiliza de forma predeterminada la última fecha de finalización de las predecesoras  
  
    -   Esfuerzo = número de personas * duración * horas en un día laborable estándar de calendario del proyecto  
  
-   **Programación manual**.   En algunos, puede convenir desviarse de estas reglas. En estos casos, puede establecer el modo de tarea para que la tarea sea programada manualmente. Esto impide que el motor de programación calcule los valores de otros atributos de programación. Establecer predecesores en tareas afecta siempre a la fecha de inicio de la tarea dependiente.  
  
## <a name="create-a-work-breakdown-structure"></a>Crear una estructura de descomposición del trabajo  
  
1.  Vaya a **Project Service > Proyectos**.  
  
2.  Haga clic en el proyecto en el que desea trabajar.  
  
3.  En la barra en la parte superior de la pantalla, seleccione la flecha hacia abajo junto al nombre del proyecto, y después haga clic en Estructura de descomposición del trabajo.  
  
4.  Para agregar una tarea, haga clic en **Agregar tarea**. Complete los campos de la tarea y, a continuación, haga clic o pulse en **Guardar**.  
  
5.  Siga agregando tareas hasta que se complete la estructura de descomposición del trabajo. Cuando cree la estructura de descomposición del trabajo, puede hacer lo siguiente para organizar sus tareas:  
  
    -   Seleccione una tarea y haga clic en **Sangría** para moverla debajo de otra tarea o haga clic en anular sangría para sacarla de un nivel.  
  
    -   Seleccione una tarea y haga clic en **Subir** o **Bajar** para moverla arriba o abajo en la lista.  
  
    -   Haga clic en **Ocultar Gantt** para ocultar el gráfico de Gantt, y haga clic en **Mostrar Gantt** para mostrarlo de nuevo.  
  
    -   Seleccione otro período de tiempo para el gráfico de Gantt en **Escala de tiempo**.  
  
6.  Para agregar roles que especificó en la estructura de descomposición del trabajo a los integrantes del equipo del proyecto, haga clic en **Generar el equipo del proyecto**.  
  
7.  Haga clic en **Guardar** en la esquina inferior derecha de la pantalla cuando haya terminado de realizar los cambios.  
  
### <a name="see-also"></a>Vea también  
 [Guía del jefe de proyecto](../psa/project-manager-guide.md)
