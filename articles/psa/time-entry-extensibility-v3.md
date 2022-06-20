---
title: Personalizar la entrada de tiempo semanal
description: En este artículo se proporciona información sobre cómo implementar reglas de negocio personalizadas que respalden las prácticas de una organización.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: bdc8df4050d895504fa126e2ee55fcd3b4de123f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918977"
---
# <a name="customize-weekly-time-entry"></a>Personalizar la entrada de tiempo semanal 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En la versión 3.3 de Microsoft Dynamics 365 Project Service Automation, Microsoft introdujo una cuadrícula moderna que permite que los recursos del proyecto introduzcan rápidamente el tiempo de hasta una semana a la vez. La nueva cuadrícula de entrada de tiempo semanal puede mostrar los datos totales de las entradas por fecha, fila o semana. Los recursos pueden realizar copias de entradas de tiempo dentro de la semana y también copias masivas de semanas anteriores. Los personalizadores del sistema pueden personalizar la vista agregando campos, añadiendo búsquedas a otras entidades e implementando reglas comerciales personalizadas para respaldar las prácticas de su organización.

Se puede acceder a la entrada de tiempo y la nueva cuadrícula de tiempo semanal a través del mapa del sitio. La experiencia de entrada de tiempo personalizada no extensible que era parte de versiones anteriores de PSA se ha reemplazado por la cuadrícula de entrada de tiempo semanal extensible, y también por una experiencia alternativa en la cuadrícula y el calendario de solo lectura. Debido a este cambio, los usuarios pueden introducir el tiempo en cantidades semanales.

## <a name="page-layout"></a>Diseño de página
La nueva cuadrícula de entrada de tiempo semanal es un control personalizado que tiene una barra de herramientas y dos secciones principales: **Dimensiones** y **Duración**. La barra de herramientas incluye un botón que se aplica solo a este control personalizado para la cuadrícula de entrada de tiempo. Por el contrario, los botones del panel de acciones de la parte superior de la página se aplican a los tres tipos de controles admitidos para la entrada de tiempo: el control de entrada de tiempo semanal, el control de solo lectura y el control de calendario.

### <a name="dimensions"></a>Dimensiones
La sección **Dimensiones** muestra, como encabezados de columna, todas las dimensiones en las se puede introducir el tiempo. Las siguientes dimensiones son compatibles de fábrica:

- Proyecto
- Tarea de proyecto
- Rol
- Escriba
- Estado de entrada

La sección **Dimensiones** no permite la edición directa. Esta sección está respaldada por una vista que permite agregar campos personalizados a la cuadrícula de entrada de tiempo semanal. Para obtener información sobre cómo agregar campos personalizados, consulte la sección "Extensibilidad" más adelante en este artículo.

### <a name="duration"></a>Duration
La sección Duración muestra los días de la semana como encabezados de columna. Esta sección permite la edición directa. Después de crear una fila de entrada de tiempo que tenga dimensiones apropiadas, los usuarios pueden introducir rápidamente, de forma directa, la cantidad de tiempo que pasaron en esas dimensiones.

## <a name="create-a-new-time-entry"></a>Creación de una nueva entrada de tiempo
Para crear una nueva entrada de tiempo en la cuadrícula de entrada de tiempo, seleccione **Nuevo**. Aparecerá el cuadro de diálogo **Creación rápida de entrada de tiempo**. En este cuadro de diálogo, los usuarios pueden seleccionar la fecha de entrada de tiempo y, a continuación, escribir los datos para las dimensiones **Proyecto**, **Tarea de proyecto**, **Rol** y **Duración** en minutos, horas, días o escribiendo, **h**, **m** o **d** junto con el número. Los usuarios también pueden introducir una descripción y comentarios que se pueden compartir externamente para la entrada de tiempo. Cuando los usuarios guardan sus cambios, los valores que introdujeron en las dimensiones aparecen en la sección **Dimensiones**. La información de duración que introdujeron en el campo **Duración** aparece en la fecha para la que se creó la entrada de tiempo.

Los campos de búsqueda tienen el respaldo de las vistas del sistema. Por ejemplo, después de que un usuario introduzca un proyecto, el campo **Tarea de proyecto** se establece en la vista **Copiar** de forma predeterminada. Para crear entradas de tiempo para tareas que no están asignadas a un usuario, seleccione **Cambiar vista** en el cuadro de diálogo de búsqueda y, a continuación, seleccione la vista **Todas las tareas de proyecto activas**.

## <a name="edit-a-time-entry"></a>Edición de una entrada de tiempo
Los detalles de algunos campos en la página de entrada de hora, como **Descripción** y **Comentarios externos**, no se muestran en la cuadrícula de entrada de hora semanal. En cambio, aparece un pequeño indicador triangular en las celdas de duración que tienen estos detalles adicionales. Seleccione la celda y, a continuación, elija **Editar detalles** para ver los datos en el panel **Edición rápida**. Para editar o actualizar los detalles de una entrada de tiempo específica que no forma parte de la cuadrícula de entrada de tiempo semanal, los usuarios deben abrir el panel **Edición rápida**.

## <a name="copy-a-time-entry-row"></a>Copiado de una fila de entrada de tiempo
Después de crear la primera fila de entrada, los usuarios pueden seleccionar **Copiar fila** para copiar toda la fila en una nueva fila. Cuando una fila se copia de esta manera, también se copian las dimensiones y duraciones. Los usuarios también pueden seleccionar **Editar fila** para actualizar los valores de dimensión y las duraciones en línea en la sección **Duración**.

## <a name="open-a-time-entry"></a>Apertura de una entrada de tiempo
Para admitir una entrada óptima y rápida en los campos más destacados, la cuadrícula de entrada de tiempo semanal muestra un subconjunto de dimensiones y duraciones de tiempo seleccionadas. Para ver todos los detalles de una sola entrada de tiempo, en **Editar entrada**, seleccione **Abrir**.

## <a name="submit-a-time-entry"></a>Envío de una entrada de tiempo
Los usuarios pueden enviar una sola entrada de tiempo o un grupo de entradas de tiempo seleccionando un bloque de celdas o una fila de entrada de tiempo completo, y, a continuación, eligiendo **Enviar**. Las entradas de tiempo enviadas aparecen como entradas pendientes de aprobación en la página **Aprobación** de los aprobadores. Una vez que las entradas se envían correctamente, no se pueden editar.

## <a name="recall-a-time-entry"></a>Recuperación de una entrada de tiempo
Puede recuperar entradas de tiempo ya enviadas. Puede recuperar una sola entrada de tiempo, un bloque de entradas de tiempo o una fila completa de entradas de tiempo. Las entradas de tiempo recuperadas están disponibles para los recursos para su edición.

## <a name="time-entry-status"></a>Estado de la entrada de tiempo
A las nuevas entradas de tiempo se les asigna automáticamente un estado **Borrador**. Cuando se envía una entrada de tiempo, el estado se actualiza a **Enviado**. Cuando se aprueba una entrada de tiempo enviada, el estado se actualiza a **Aprobado**. Si se rechaza una entrada de tiempo, el estado se actualiza a **Devuelto** y la entrada pasa a estar disponible para su corrección y reenvío. Solo se pueden eliminar las entradas de tiempo que tienen un estado de **Borrador**.

## <a name="view-rejection-comments"></a>Visualización de comentarios de rechazo
Cuando un aprobador rechaza una entrada de tiempo, este puede agregar comentarios de rechazo para ayudar al recurso a comprender el motivo del rechazo. Para ver los comentarios de rechazo para una entrada de tiempo, seleccione **Abrir entrada**. Los comentarios de rechazo se mostrarán en la escala de tiempo. En la escala de tiempo, el recurso puede responder a los comentarios de rechazo antes de volver a enviar la entrada.

## <a name="copy-week"></a>Copia de semana
Después de que se hayan creado algunas entradas de tiempo, los usuarios pueden seleccionar **Copiar semana** para crear entradas de tiempo adicionales de forma masiva. Aparecerá el cuadro de diálogo **Copiar**. En la sección **Desde el período**, use los campos **Fecha de inicio** y **Fecha de finalización** para definir el rango de fechas desde el que copiar las entradas de tiempo. En la sección **Hasta el período**, en el campo **Fecha de inicio**, especifique la fecha para la que crear entradas de tiempo. A continuación, seleccione **Copiar**. Para la fecha especificada "Hasta el período", se crea una copia de las entradas de tiempo para el día de la semana correspondiente en "Desde el período". Por ejemplo, la entrada de tiempo del lunes de la semana pasada se copia en el lunes de la semana que se especifica como "Hasta el período".

## <a name="import"></a>Importar
Se utiliza el mismo proceso básico para importar desde reservas, asignaciones e intercambios. Los usuarios pueden especificar el rango de fechas desde el que se importan las reservas. Luego deben seleccionar explícitamente las reservas que deben copiarse en las entradas de tiempo Borrador. En la versión anterior, las entradas de tiempo sugeridas aparecían en la cuadrícula y el calendario, y se perdían cuando se actualizaba la sesión.

## <a name="extensibility"></a>Extensibilidad
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Adición de campos personalizados que tienen búsquedas a otras entidades
Existen tres pasos principales para agregar un campo personalizado a la cuadrícula de entrada de tiempo semanal.

1.  Agregue el campo personalizado al cuadro de diálogo de creación rápida.
2.  Configure la cuadrícula para mostrar el campo personalizado.
3.  Agregue el campo personalizado al flujo de tareas de edición de filas o al flujo de tareas de edición de celdas, según corresponda.

También debe asegurarse de que el nuevo campo tenga las validaciones requeridas en el flujo de tareas de edición de fila o celda. Como parte de este paso, debe bloquear el campo, en función del estado de entrada de tiempo.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adición del campo personalizado al cuadro de diálogo de creación rápida
Debe agregar el campo personalizado al cuadro de diálogo Crear entrada de tiempo, Creación rápida para que los usuarios puedan introducir un valor cuando agreguen entradas de tiempo mediante el botón **Nuevo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configuración de la cuadrícula para mostrar el campo personalizado
Existen dos formas de agregar un campo personalizado a la cuadrícula de entrada de tiempo semanal. La primera opción es personalizar la vista **Mis entradas de tiempo semanales** y agregarle el campo personalizado. Puede elegir la posición y el tamaño del campo personalizado en la cuadrícula editando esas propiedades en la vista.

La segunda opción es crear una nueva vista de entrada de tiempo personalizada y establecerla como la vista predeterminada. Esta vista debe contener los campos **Descripción** y **Comentarios externos**, además de las columnas que desea tener en la cuadrícula. Puede elegir la posición, el tamaño y el criterio de ordenación predeterminado de la cuadrícula editando esas propiedades en la vista. A continuación, configure el control personalizado para esta vista para que sea un control **Cuadrícula de entrada de tiempo**. Agregue este control a la vista y selecciónelo para la web, el teléfono y la tableta. A continuación, configure los parámetros para la cuadrícula de entrada de tiempo semanal. Establezca el campo **Fecha de inicio** en **msdyn_date**, el campo **Duración** en **msdyn_duration** y el campo **Estado** en **msdyn_entrystatus**. Para la vista predeterminada, el campo **Lista de estados de solo lectura** se establece en **192350002,192350003,192350004**, el campo **Flujo de tareas de edición de fila** en **msdyn_timeentryrowedit** y **Flujo de tareas de edición de celda** en **msdyn_timeentryedit**. Puede personalizar estos campos para agregar o eliminar el estado de solo lectura, o para usar una experiencia basada en tareas (TBX) diferente para la edición de filas o celdas. Estos campos deben estar vinculados a un valor estático.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Adición del campo personalizado al flujo de tareas de edición apropiado
Las páginas TBX que se usan para editar se pueden encontrar en **Procesos**. Las páginas predeterminadas son **Project Service: editar fila de entrada de tiempo** y **Project Service: editar entrada de tiempo**. Puede editar estas páginas predeterminadas o crear nuevas páginas TBX personalizadas.

> [!NOTE] 
> Ambas opciones eliminarán algunos filtros listos para usar en las entidades **Proyecto** y **Tarea de proyecto**, por lo que todas las vistas de búsqueda para las entidades serán visibles. Con los filtros listos para usar, solo se verán las vistas de búsqueda relevantes.

Debe determinar el flujo de tareas apropiado para el campo personalizado. Lo más probable es que si agregó el campo a la cuadrícula, debe ir en el flujo de tareas de edición de fila que se utiliza para los campos que se aplican a toda la fila de entradas de tiempo. Si el campo personalizado tiene un valor único todos los días, como un campo personalizado para **Hora de finalización**, debe ir en el flujo de tareas de edición de celda.

Para agregar el campo personalizado a un flujo de tareas, arrastre un elemento **Campo** a la posición adecuada en la página y, a continuación, configure sus propiedades. Establezca la propiedad **Origen** en **Entrada de tiempo** y la propiedad **Campo de datos** en el campo personalizado. La propiedad **Campo** especifica el nombre para mostrar en la página TBX. Seleccione **Aplicar** para guardar los cambios en el campo. A continuación, seleccione **Actualizar** para guardar cambios en la página.

Para utilizar una nueva página TBX personalizada, cree un nuevo proceso. Establezca la categoría en **Flujo de proceso de negocio**, la entidad en **Entrada de tiempo** y el tipo de proceso de negocio en **Ejecutar proceso como un flujo de tareas**. En **Propiedades**, la propiedad **Nombre de página** debe establecerse en el nombre para mostrar de la página. Agregue todos los campos relevantes a la página TBX. Guarde y active el proceso y, a continuación, actualice la propiedad de control personalizado para el flujo de tareas relevante al valor de **Nombre** en el proceso.

### <a name="add-new-option-set-values"></a>Adición de nuevos valores de conjunto de opciones
Para agregar valores de conjunto de opciones a un campo listo para usar, abra la página de edición para el campo y, a continuación, en **Tipo**, seleccione **Editar** junto al conjunto de opciones. A continuación, agregue una nueva opción que tenga una etiqueta y un color personalizados. Si desea agregar un nuevo estado de entrada de tiempo, el campo listo para usar se denomina **Estado de entrada**, no **Estado**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designación de un nuevo estado de entrada de tiempo como solo lectura
Para designar un nuevo estado de entrada de tiempo como de solo lectura, agregue el nuevo valor de entrada de tiempo (el número, no la etiqueta) a la propiedad **Lista de estados de solo lectura**. La parte editable de la cuadrícula de entrada de tiempo se bloqueará para las filas que tienen el nuevo estado.
A continuación, agregue reglas comerciales para bloquear todos los campos en las páginas TBX **Editar fila de entrada de tiempo** y **Editar entrada de tiempo**. Puede acceder a las reglas comerciales para estas páginas abriendo el editor de flujo de proceso de negocio para la página y, a continuación, seleccionando **Reglas de negocio**. Puede agregar el nuevo estado a la condición en las reglas de negocio existentes, o puede agregar una nueva regla comercial para el nuevo estado.

### <a name="add-custom-validation-rules"></a>Adición de reglas de validación personalizadas
Existen dos tipos de reglas de validación que puede agregar para la experiencia de la cuadrícula de entrada de tiempo semanal: • Reglas de negocio del lado del cliente que funcionan en cuadros de diálogo de creación rápida y en páginas TBX • Validaciones de complementos del lado del servidor que se aplican a todo el tiempo de entrada actualizaciones.

#### <a name="business-rules"></a>Reglas de negocio
Use reglas de negocio para bloquear y desbloquear campos, introducir valores predeterminados en los campos y definir validaciones que requieran información solo del registro de entrada de tiempo actual. Puede acceder a las reglas comerciales para una página TBX abriendo el editor de flujo de proceso de negocio para la página y, a continuación, seleccionando **Reglas de negocio**. Luego puede editar las reglas de negocio existentes o agregar una nueva. Para validaciones aún más personalizadas, puede usar una regla de negocio para ejecutar JavaScript.

#### <a name="plug-in-validations"></a>Validaciones de complementos
Debe usar validaciones de complementos para cualquier validación que requiera más contexto del que está disponible en un registro de entrada de tiempo único, o para cualquier validación que desee ejecutar en actualizaciones en línea en la cuadrícula. Para completar la validación, cree un complemento personalizado en la entidad **Entrada de tiempo**.

> [!IMPORTANT] 
> Actualmente, una incidencia conocida en las páginas TBX impide que los usuarios corrijan la información y vuelvan a seleccionar Listo cuando se produce un error en la actualización de la validación de un complemento. Como solución alternativa, configure validaciones de reglas de negocio para evitar esta situación en medida de lo posible.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
