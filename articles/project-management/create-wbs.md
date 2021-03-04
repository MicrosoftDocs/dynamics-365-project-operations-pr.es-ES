---
title: Crear una estructura de descomposición del trabajo
description: Este tema explica cómo se crea una estructura de descomposición del trabajo que incluye los controles básicos en la nueva interfaz de programación.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841406"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Crear una estructura de descomposición del trabajo

Una programación del proyecto comunica el trabajo que debe realizarse, qué recursos realizarán el trabajo y la programación para completar ese trabajo. La programación refleja todo el trabajo asociado con la entrega del proyecto a tiempo. Para crear una programación del proyecto en Dynamics 365 Project Operations, puede:

  - Desglosar el trabajo en tareas manejables.
  - Estimar el tiempo necesario para realizar cada tarea.
  - Establecer las dependencias de las tareas.
  - Establecer la duración de las tareas.
  - Estimar los recursos genéricos que realizarán las tareas. 

La programación del proyecto se crea en la pestaña **Programación** de la página **Proyecto**.

## <a name="tasks"></a>Tareas

El primer paso para crear un programa del proyecto es dividir el trabajo en partes manejables. La programación de Project Operations es compatible con las siguientes características:

- Tareas de informe o contenedor
- Tareas del nodo hoja

### <a name="summary-tasks"></a>Tareas de resumen

Las tareas de resumen pueden almacenar otras tareas de resumen o tareas de nodo hoja. No suponen ningún esfuerzo de trabajo ni tienen ningún coste por sí solas. En cambio, su esfuerzo y coste de trabajo son un informe del esfuerzo de trabajo y el coste de sus tareas de contenedor. La fecha de inicio de la tarea de resumen es la fecha de inicio de las tareas del contenedor, y la de finalización es la fecha de finalización de dichas tareas. El nombre de una tarea de resumen se puede editar, pero las propiedades de programación (como esfuerzo, fechas y duración) no se pueden editar. Si elimina una tarea de resumen, también se eliminan todas sus tareas de contenedor.

### <a name="leaf-node-tasks"></a>Tareas del nodo hoja

Las tareas de nodo hoja representan el trabajo más granular en el proyecto. Tienen un esfuerzo estimado, recursos, fechas de inicio y finalización planificadas, y una duración.

## <a name="create-a-task-hierarchy"></a>Creación de una jerarquía de tareas

### <a name="add-a-task"></a>Agregar una tarea

Complete los pasos que se indican a continuación para agregar una o más tareas.

1. Vaya a **Proyectos** y seleccione y abra el registro del proyecto para el que desea crear una programación. 
2. Seleccione la pestaña **Tareas**. 
3. Seleccione **Agregar nueva tarea**, escriba un nombre para la tarea y presione Entrar.
2. Escriba otro nombre de tarea y vuelva a presionar Entrar hasta que tenga la lista completa de tareas.

### <a name="manage-hierarchy-of-a-task"></a>Administrar la jerarquía de una tarea

Cuando se aplica la sangría a una tarea, se convierte en elemento secundario de la tarea que está directamente encima de ella. El Id. de programación de la tarea se recalcula para que se base en el Id. de programación de su nuevo elemento principal y siga el esquema de numeración del perfil. Ahora la tarea principal es una tarea de resumen. Por lo tanto, se convierte en un informe de sus tareas secundarias. Cuando se promociona una tarea, deja de ser un elemento secundario de la tarea que era su principal. El Id. de programación se recalcula para que refleje la profundidad y el puesto actualizados de la tarea en la jerarquía. El esfuerzo, el coste y las fechas de la tarea principal anterior se vuelven a calcular para que no incluyan esa tarea.

Para degradar una tarea o promocionarla, siga los pasos que se indican a continuación.

1. En la página **Proyecto**, en la pestaña **Tareas**, en **Tareas de resumen**, seleccione los tres puntos verticales que se muestran junto al nombre de la tarea y, a continuación, seleccione **Crear subtarea**. 
2. Seleccione la tarea que desea degradar o promocionar. Para seleccionar más de una tarea, empiece por seleccionar una tarea y mantenga presionada la tecla Ctrl mientras selecciona otras tareas.
2. Seleccione **Sangría** o **Promocionar subtarea** para mover tareas al resumen o sacarlas del resumen.

### <a name="move-tasks-up-and-down"></a>Subir y bajar tareas

Las tareas se pueden mover a cualquier nivel de la estructura de descomposición del trabajo de una de estas dos formas:

- Seleccionar una o varias tareas y arrastrarlas a la ubicación deseada.
- Seleccione una o varias tareas, hacer clic con el botón secundario y seleccionar **Cortar**, seleccionar la celda de destino en la programación y, a continuación, hacer con el botón secundario y seleccionar **Pegar**.

## <a name="task-attributes"></a>Atributos de tareas

El nombre de una tarea describe el trabajo que debe completarse. En Project Operations, los atributos asociados con una tarea describen el programa de la tarea y sus requisitos de personal.

## <a name="schedule-attributes"></a>Atributos de programación

Los atributos de **esfuerzo**, **fecha de inicio**, **fecha de finalización** y **duración** definen la programación de la tarea.

La tabla siguiente muestra atributos de programación adicionales.

| **Nombre para mostrar final** | **Descripción final** |
| --- | --- |
| Esfuerzo completado (horas) | Trabajo completado de la tarea en horas. |
| Duración | Muestra la duración de la tarea en días. |
| Esfuerzo total | Trabajo total de la tarea en horas. |
| Finalizar | Fecha y hora de finalización. |
| % completado | Porcentaje de la tarea que se ha completado. |
| Cubo de proyecto | El panel de tareas se puede agrupar por cubo, de modo que cada cubo tenga su propia columna. |
| Esfuerzo restante (horas) | Trabajo restante de la tarea en horas. |
| Principio | Fecha y hora de inicio. |
| Nombre | Nombre de la tarea. |
| Identificador | Id. de la tarea en la estructura de descomposición del trabajo. |

## <a name="staffing-attributes"></a>Atributos de personal

Puede obtener acceso a los atributos de personal a través del campo **Recursos** en la programación. Puede buscar un recurso existente o seleccionar **Crear** y, en el panel **Creación rápida** , agregar un miembro del equipo del proyecto como un nuevo recurso.

Los campos **Rol**, **Unidad de dotación de recursos** y **Nombre de puesto** se utilizan para describir los requisitos de personal para la tarea. Estos atributos de personal junto con la programación de tareas se utilizan para encontrar los recursos disponibles para realizar esta tarea.

   - **Rol**: especifique el tipo de recurso necesario para realizar la tarea.
   - **Unidad de dotación de recursos**: especifique la unidad desde la que se deben asignar los recursos para la tarea. Este atributo afecta al coste y la estimación de ventas de la tarea si el coste y la tasa de facturación del recurso se establecen en función de las unidades de recursos.
   - **Nombre de puesto**: escriba un nombre para el recurso genérico que sirve como marcador de posición para el recurso que finalmente realizará el trabajo.

El campo **Recursos** contiene el nombre de puesto del recurso genérico o del recurso con nombre cuando se encuentra uno.

El campo **Categoría** contiene los valores que indican un tipo más amplio de trabajo en el que se puede agrupar la tarea. Este campo no afecta la programación o la contratación del personal. En lugar de ello, el campo se usa solo para informes.

## <a name="task-dependencies"></a>Dependencias de tarea

Puede usar la programación de Project Operations para crear relaciones predecesoras entre tareas. El campo **Predecesora** usa uno o más valores para indicar las tareas de las que depende una tarea. Cuando se asignan valores predecesores a una tarea, la tarea solo puede comenzar después de que se hayan completado todas las tareas predecesoras. Debido a la dependencia, la fecha de inicio planificada de la tarea se restablece a la fecha en que se completan las tareas predecesoras.

El modo de tarea no tiene ningún efecto en las actualizaciones que se realizan a las fechas de inicio y finalización de las tareas predecesoras/dependientes.

## <a name="accessibility-and-keyboard-shortcuts"></a>Accesibilidad y métodos abreviados de teclado

La cuadrícula **Programar** es totalmente accesible y se puede usar con lectores de pantalla como Narrator, JAWS o NVDA. Puede moverse por el área de la cuadrícula mediante las teclas de flecha (como en Microsoft Excel), puede usar el tabulador para avanzar a través de los elementos interactivos de la interfaz de usuario, y puede usar la tecla de flecha hacia abajo, la tecla Intro o la barra espaciadora para seleccionar y abrir los menús desplegables.
