---
title: Comportamiento de la interfaz de usuario de entrada de tiempo
description: En este tema se proporciona información sobre el comportamiento de la interfaz de usuario de entrada de tiempo.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ef99f220e9ff207a7620a900aa0630e2803f4f7261eccfbf73ed79717648bf92
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999472"
---
# <a name="time-entry-ui-behavior"></a>Comportamiento de la interfaz de usuario de entrada de tiempo

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


La cuadrícula **Entrada de tiempo semanal** es un control personalizado que tiene dos secciones principales, **Dimensiones** y **Duración**.

## <a name="keyboard-shortcuts"></a>Métodos abreviados de teclado
| Acción        | Acceso directo                  |
|------------   |------------------------   |
| Nueva           | Alt + Mayús + n           |
| Copiar fila      | Alt + Mayús + c           |
| Editar entrada    | Alt + Mayús + e           |
| Editar fila      | Alt + Mayús + Ctrl + e    |
| Abrir entrada    | Alt + Mayús + o           |
| Enviar        | Alt + Mayús + s           |
| Recuperar        | Alt + Mayús + r           |
| Delete        | Alt + Mayús + d           |
| Copiar semana     | Alt + Mayús + w           |

## <a name="dimensions"></a>Dimensiones
La sección **Dimensiones** muestra las dimensiones en las se puede introducir el tiempo. Las siguientes dimensiones son compatibles y están listas para usar:

  - Project
  - Tarea de proyecto
  - Rol
  - Escribir
  - Estado de entrada

La sección **Dimensiones** no permite la edición directa. Esta sección está respaldada por una vista que permite agregar campos personalizados a la cuadrícula de entrada de tiempo semanal.

## <a name="duration"></a>Duración
La sección Duración muestra los días de la semana como encabezados de columna. Esta sección permite la edición directa. Después de crear una fila de entrada de tiempo con las dimensiones apropiadas, los usuarios pueden introducir rápidamente la cantidad de tiempo que pasaron en esas dimensiones.

## <a name="create-a-new-time-entry"></a>Creación de una nueva entrada de tiempo

1. En la cuadrícula de entrada de tiempo, seleccione **Nuevo**. 
2. En el cuadro de diálogo **Creación rápida de entrada de tiempo**, seleccione la fecha de entrada de tiempo.
3. Introduzca datos para las dimensiones **Proyecto**, **Tarea de proyecto**, **Rol** y **Duración**. Esta información debe agregarse en minutos, horas o días escribiendo **h**, **m** o **d**, junto con el número. 
4. Introduzca una descripción para la entrada y cualquier comentario que se pueda compartir externamente en relación con la entrada de tiempo. 

Cuando guarde la entrada, los valores introducidos aparecerán en la sección **Dimensiones**. La información introducida en el campo **Duración** aparece en la fecha para la que se ha creado la entrada de tiempo.

Los campos de búsqueda tienen el respaldo de las vistas del sistema. Por ejemplo, después de que un usuario introduzca un proyecto, el campo **Tarea de proyecto** se establece en la vista **Copiar** de forma predeterminada. Para crear entradas de tiempo para tareas que no están asignadas a un usuario, seleccione **Cambiar vista** en el cuadro de diálogo de búsqueda y, a continuación, seleccione la vista **Todas las tareas de proyecto activas**.

## <a name="edit-a-time-entry"></a>Edición de una entrada de tiempo 
Los detalles de algunos campos en la página de entrada de hora, como **Descripción** y **Comentarios externos**, no se muestran en la cuadrícula de entrada de hora semanal. En cambio, aparece un pequeño indicador triangular en las celdas de **Duración** que tienen estos detalles adicionales. 

1. Para editar una entrada de tiempo, seleccione la celda que desea actualizar en la entrada de tiempo.
2. Seleccione **Editar detalles** para actualizar los datos en el panel **Formulario principal de entrada de tiempo**. 

## <a name="copy-a-time-entry-row"></a>Copiado de una fila de entrada de tiempo
Después de crear la fila de entrada, puede seleccionar **Copiar fila** para copiar toda la fila en una nueva fila. Cuando una fila se copia de esta manera, también se copian las dimensiones y duraciones. También puede seleccionar **Editar fila** para actualizar los valores de dimensión y las duraciones en la sección **Duración**.

## <a name="open-a-time-entry-behavior"></a>Abrir un comportamiento de entrada de tiempo
Para admitir una entrada óptima y rápida en los campos más destacados, la cuadrícula de entrada de tiempo semanal muestra un subconjunto de dimensiones y duraciones de tiempo seleccionadas. Para ver todos los detalles de una sola entrada de tiempo, en **Editar entrada**, seleccione **Abrir**.

## <a name="submit-a-time-entry"></a>Envío de una entrada de tiempo
Puede enviar una sola entrada de tiempo o un grupo de entradas de tiempo seleccionando un bloque de celdas o una fila de tiempo entera, y, a continuación, eligiendo **Enviar**. Las entradas de tiempo enviadas aparecen como entradas pendientes de aprobación en la página **Aprobación** de los aprobadores. Una vez que las entradas se envían correctamente, no se pueden editar.

## <a name="recall-a-time-entry"></a>Recuperación de una entrada de tiempo
Puede recuperar entradas de tiempo ya enviadas. Puede recuperar una sola entrada de tiempo, un bloque de entradas de tiempo o una fila completa de entradas de tiempo. Las entradas de tiempo recuperadas se pueden editar.

## <a name="time-entry-status"></a>Estado de la entrada de tiempo

- **Borrador**: a las nuevas entradas de tiempo se les asigna automáticamente un estado de **Borrador**. Solo se pueden eliminar las entradas de tiempo que tienen un estado de **Borrador**.
- **Enviada**: cuando se envía una entrada de tiempo, el estado se actualiza a **Enviada**. 
- **Aprobada**: cuando se aprueba una entrada de tiempo enviada, el estado se actualiza a **Aprobada**. 
- **Devuelta**: si se rechaza una entrada de tiempo, el estado se actualiza a **Devuelta** y la entrada pasa a estar disponible para su corrección y reenvío. 

## <a name="view-rejection-comments"></a>Visualización de comentarios de rechazo
Cuando un aprobador rechaza una entrada de tiempo, este puede agregar comentarios para ayudar al recurso a conocer el motivo del rechazo. Para ver los comentarios de rechazo para una entrada de tiempo, seleccione **Abrir entrada**. Los comentarios de rechazo se mostrarán en la escala de tiempo. El usuario puede responder a los comentarios de rechazo antes de volver a enviar la entrada.

## <a name="copy-week"></a>Copiar semana
Después de que se hayan creado algunas entradas de tiempo, los usuarios pueden crear varias entradas de tiempo al mismo tiempo.

1. En el formulario **Entradas de tiempo**, seleccione **Copiar semana** para crear entradas de tiempo adicionales de forma masiva. 
2. En el cuadro de diálogo **Copiar**, en la sección **Desde el período**, use los campos **Fecha de inicio** y **Fecha de finalización** para definir el rango de fechas desde el que copiar las entradas de tiempo. 
3. En la sección **Hasta el período**, en el campo **Fecha de inicio**, especifique la fecha para la que crear entradas de tiempo. 
4. Seleccione **Copiar**. Para la fecha especificada en **Periodo hasta**, se crea una copia de las entradas de tiempo para el día de la semana correspondiente en **Periodo desde**. Por ejemplo, la entrada de tiempo del lunes de la semana pasada se copia en el lunes de la semana que se especifica en **Periodo hasta**.

## <a name="import"></a>Importar
Se utiliza el mismo proceso básico para importar desde reservas, asignaciones e intercambios. Puede especificar el rango de fechas desde el que se importan las reservas y luego seleccionar explícitamente las reservas que se deben copiar como entradas de tiempo de borrador. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
