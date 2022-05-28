---
title: Programaciones del proyecto
description: En este tema se proporciona información sobre cómo crear una programación.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 4b7b221c2b0c47ed02c59fb724cf65bc41697d82
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600625"
---
# <a name="project-schedules"></a>Programaciones del proyecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Una programación del proyecto comunica el trabajo que debe realizarse, qué recursos realizarán el trabajo y calendario en el que debe completarse ese trabajo. Refleja todo el trabajo asociado con la entrega del proyecto a tiempo. En Dynamics 365 Project Service Automation, puede crear una programación del proyecto dividiendo el trabajo en tareas manejables, estimando el tiempo que se requiere para realizar cada tarea, estableciendo dependencias de tareas, configurando duraciones de tareas y valorando los recursos genéricos que realizarán las tareas. La programación del proyecto se crea en la pestaña **Programar** de la página del proyecto.
 
## <a name="tasks"></a>Tareas

El primer paso para crear un programa del proyecto es dividir el trabajo en partes manejables. La programación de PSA es compatible con las siguientes características:

- Nodo raíz del proyecto.
- Tareas de informe o contenedor
- Tareas del nodo hoja

### <a name="project-root-node"></a>Nodo raíz del proyecto.

El nodo raíz del proyecto es la tarea de resumen de nivel superior para el proyecto. El resto de las tareas del proyecto se crean por debajo. El nombre del nodo de raíz se establece siempre en el nombre del proyecto. El esfuerzo, las fechas y la duración del nodo raíz se resumen según los valores de la jerarquía por debajo de él. No puede editar las propiedades del nodo raíz. Tampoco puede eliminar el nodo raíz.

### <a name="summary-or-container-tasks"></a>Tareas de informe o contenedor 

Las tareas de resumen tienen subtareas o tareas de contenedor en ellas. No suponen ningún esfuerzo de trabajo ni tienen ningún coste por sí solas. En cambio, su esfuerzo y coste de trabajo son un informe del esfuerzo de trabajo y el coste de sus tareas de contenedor. La fecha de inicio de la tarea de resumen es la fecha de inicio de las tareas del contenedor, y la de finalización es la fecha de finalización de dichas tareas. El nombre de una tarea de resumen se puede editar, pero las propiedades de programación (esfuerzo, fechas y duración) no se pueden editar. Si elimina una tarea de resumen, también se eliminan todas sus tareas de contenedor.

### <a name="leaf-node-tasks"></a>Tareas del nodo hoja

Las tareas de nodo hoja representan el trabajo más granular en el proyecto. Tienen un esfuerzo estimado, recursos, fechas de inicio y finalización planificadas, y una duración.
 
## <a name="creating-a-task-hierarchy"></a>Creación de una jerarquía de tareas

Puede crear una jerarquía de tareas mediante las siguientes opciones:

- Botón **Agregar tarea**
- Botón **Aplicar sangría a tarea**
- Botón **Anular sangría de tarea**
- Botones **Subir** y **Bajar**
- Accesibilidad y métodos abreviados de teclado

### <a name="add-task"></a>Agregar tarea

El botón **Agregar tarea** le permite crear una nueva tarea en la jerarquía. Si no selecciona un puesto, la tarea se inserta al final. 

Se asigna un Id. de programación a cada tarea. El Id. de programación representa la profundidad y el puesto de la tarea en la jerarquía. Utiliza la numeración del perfil. Para las tareas en el primer nivel bajo el nodo raíz del proyecto, se utiliza un esquema de numeración de 1, 2, 3, etc. Para tareas bajo el primer nivel, se usa un esquema de numeración de 1.1, 1.2, 1.3, etc.

### <a name="indent-task"></a>Aplicar sangría a tarea

Cuando se aplica la sangría a una tarea, se convierte en elemento secundario de la tarea que está directamente encima de ella. El Id. de programación de la tarea se recalcula para que se base en el Id. de programación de su nuevo elemento principal y siga el esquema de numeración del perfil. La tarea principal ahora es una tarea de resumen o una tarea de contenedor. Por lo tanto, se convierte en un informe de sus tareas secundarias.

### <a name="outdent-task"></a>Anular sangría de tarea 

Cuando se anula la sangría de una tarea, deja de ser un elemento secundario de la tarea que era su principal. El Id. de programación se recalcula para que refleje la profundidad y el puesto actualizados de la tarea en la jerarquía. El esfuerzo, el coste y las fechas de la tarea principal anterior se vuelven a calcular para que no incluyan esa tarea.

### <a name="move-up-and-move-down"></a>Subir y Bajar 

Los botones **Subir** y **Bajar** cambian el puesto de una tarea dentro de su jerarquía principal. Los cambios de este tipo no afectan el esfuerzo, el coste, las fechas o la duración de la tarea. Solo se ve afectada el Id. de programación de la tarea. El Id. de programación se vuelve a calcular para que refleje el nuevo puesto de la tarea en la lista de tareas secundarias del elemento principal.

### <a name="accessibility-and-keyboard-shortcuts"></a>Accesibilidad y métodos abreviados de teclado

La cuadrícula **Programar** es totalmente accesible y se puede usar con lectores de pantalla como Narrator, JAWS o NVDA. Puede moverse por el área de la cuadrícula mediante las teclas de flecha (como en Microsoft Excel), puede usar el tabulador para avanzar a través de los elementos interactivos de la interfaz de usuario, y puede usar la tecla de flecha hacia abajo, la tecla Intro o la barra espaciadora para seleccionar e invocar los menús desplegables. Los encabezados de columna también son interactivos. Puede ocultar y mostrar columnas, usar el tabulador y las teclas de flecha para moverse por los encabezados de columna y utilizar los botones de acción de la barra de herramientas. Además, puede usar los siguientes métodos abreviados de teclado:

- **Actualizar**: ALT+Mayús+F5
- **Agregar**: ALT+Mayús+Ins
- **Eliminar**: ALT+Mayús+Supr
- **Subir/bajar**: ALT+Mayús+Flechas de arriba/abajo
- **Aplicar sangría/Anular sangría**: ALT_Mayús+Flechas izquierda/derecha
- **Expandir/Contraer jerarquías**: ALT+Mayús+Teclas más/menos

## <a name="task-attributes"></a>Atributos de tareas

El nombre de una tarea describe el trabajo que debe completarse. En PSA, los atributos que están asociados con una tarea describen el programa de la tarea y sus requisitos de personal.

> ![Atributos de tareas.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Atributos de programación

Los atributos de **esfuerzo**, **fecha de inicio**, **fecha de finalización** y **duración** definen la programación de la tarea.

Entre los atributos de programación adicionales se incluyen los siguientes:

- **Horas de esfuerzo**: especifique una estimación de las horas necesarias para completar la tarea. 
- **Duración**: especifique el número de días laborables necesarios para completar la tarea.
- **Id. de programación**: este Id. generado automáticamente se usa para ordenar tareas en la jerarquía. Las dependencias entre las tareas administran el orden real en el que se trabajan las tareas.
 
### <a name="staffing-attributes"></a>Atributos de personal

Puede obtener acceso a los atributos de personal a través del campo **Recursos** en la programación. Puede buscar un recurso existente o hacer clic en **Crear** y, en el panel **Creación rápida** , agregar un miembro del equipo del proyecto como un nuevo recurso.

Los campos **Rol**, **Unidad de dotación de recursos** y **Nombre de puesto** se utilizan para describir los requisitos de personal para la tarea. Estos atributos de personal junto con la programación de tareas se utilizan para encontrar los recursos disponibles para realizar esta tarea.

**Rol**: especifique el tipo de recurso necesario para realizar la tarea.

**Unidad de dotación de recursos**: especifique la unidad desde la que se deben asignar los recursos para la tarea. Este atributo afecta al coste y la estimación de ventas de la tarea si el coste y la tasa de facturación del recurso se establecen en función de las unidades de recursos.

**Nombre de puesto**: escriba un nombre descriptivo para el recurso genérico que sirve como marcador de posición para el recurso que finalmente realizará el trabajo.

El campo **Recursos** contiene el nombre de puesto del recurso genérico o del recurso con nombre cuando se encuentra uno.

El campo **Categoría** contiene los valores que indican un tipo más amplio de trabajo en el que se puede agrupar la tarea. Este campo no afecta la programación o la contratación del personal. Se usa solo con fines informativos.

### <a name="task-dependencies"></a>Dependencias de tarea 

Puede usar la programación en PSA para crear relaciones predecesoras entre tareas. El campo **Predecesora** en **Tareas** selecciona uno o más valores para indicar las tareas de las que depende una tarea. Cuando se asignan valores predecesores a una tarea, la tarea solo puede comenzar después de que se hayan completado todas las tareas predecesoras. Debido a la dependencia, la fecha de inicio planificada de la tarea se restablece a la fecha en que se completan las tareas predecesoras.

El modo de tarea no tiene ningún efecto en las actualizaciones que se realizan a las fechas de inicio y finalización de las tareas predecesoras/dependientes.

## <a name="task-mode"></a>Modo de tarea 

El modo de tarea determina la programación de las tareas del nodo hoja. PSA admite dos modos de tarea para cada tarea: programación automática y programación manual.

### <a name="auto-scheduling"></a>Programación automática 
 
Cuando se establece el modo de tarea en **Programada automáticamente** para una tarea, el motor de programación de tareas usa las reglas de programación en los atributos de tarea para determinar la programación de la tarea.

#### <a name="scheduling-rules"></a>Reglas de programación

De forma predeterminada, si una tarea de nodo hoja no tiene predecesores, su fecha de inicio se establece en la fecha de inicio programada del proyecto. La duración de una tarea del nodo hoja se calcula siempre como el número de días laborables entre sus fechas de inicio y finalización. Cuando una tarea se programa automáticamente, el motor de programación sigue estas reglas:

- Las fechas de inicio y finalización de una tarea deben ser días laborables según el calendario de programación del proyecto. 
- Para cualquier tarea que tenga tareas predecesoras, la fecha de inicio se establece automáticamente en la última fecha de finalización de sus predecesoras.
- El esfuerzo se calcula mediante esta fórmula: Número de personas × Duración × Horas en un día laborable estándar en el calendario del proyecto.

### <a name="manual-scheduling"></a>Programación manual

Si las reglas de la programación automática no cumplen con sus requisitos, puede establecer el modo de tarea para la tarea en **Programada manualmente**. Esta configuración impide que el motor de programación calcule los valores de otros atributos de programación. Independientemente del modo de tarea, si establece predecesores en las tareas, siempre afecta la fecha de inicio de la tarea dependiente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
