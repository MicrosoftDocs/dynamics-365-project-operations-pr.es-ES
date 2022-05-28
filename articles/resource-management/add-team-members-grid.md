---
title: Agregar miembros del equipo desde la cuadrícula Miembros del equipo
description: En este tema se proporciona información sobre cómo puede administrar los recursos de miembros del equipo.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 85dc7ab4b30359a24994f8f9bf38de3fc2325e60
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588113"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Agregar miembros del equipo desde la cuadrícula Miembros del equipo

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations incluye un panel de administrador de recursos que proporciona información general visual de la utilización y la demanda de recursos en la organización. Puede usar los gráficos de este panel para visualizar la siguiente información:

- **Demanda de recursos**: el gráfico **Solicitudes de recursos activas** muestra los recursos que se han enviado. Los recursos se agregan por rol o por proyecto.
- **Demanda de recursos no enviada**: el gráfico **Demanda de recursos sin asignar** muestra todos los requisitos de recursos que no se han enviado. Este gráfico ayuda a los administradores de recursos a ver la demanda que no es firme y que se puede enviar con una solicitud de recursos.
- **Utilización facturable de la última semana**: el gráfico **Uso por rol** muestra el porcentaje de uso facturable real de la organización por rol, con respecto al uso facturable objetivo por rol.

    > [!NOTE]
    > Para que el gráfico **Uso por rol** esté disponible, cree un trabajo que ejecute el flujo de trabajo **UpdateRoleUtilization**. Este trabajo periódico se ejecuta cada siete días para calcular el uso facturable de los siete días anteriores. Los resultados se agregan por rol.

## <a name="manage-project-team-members"></a>Administrar miembros del equipo del proyecto

Los administradores de proyecto pueden usar el panel Administrador de recursos para administrar los recursos de los proyectos. Por ejemplo, pueden agregar un miembro del equipo directamente a un proyecto y reservar un miembro del equipo para cumplir los requisitos de recursos que capturó un recurso genérico.

### <a name="add-a-team-member-directly-to-a-project"></a>Agregar un miembro del equipo directamente a un proyecto

Para agregar un miembro del equipo directamente a un proyecto, en el formulario **Proyectos**, en la pestaña **Equipo**, seleccione **Nuevo**. Aparecerá el cuadro de diálogo **Creación rápida: Miembro del equipo del proyecto**. En este cuadro de diálogo, podrá realizar las tareas siguientes:

- **Reservar un recurso con nombre**: en el campo **Recurso reservable**, seleccione el nombre del recurso. A continuación, seleccione el rol, establezca el periodo y seleccione un método de asignación. El recurso con nombre seleccionado se agrega al proyecto mediante el método de asignación seleccionado y el calendario de recursos.
- **Agregar un recurso genérico**: deje el campo **Recurso reservable** en blanco y después seleccione el rol, defina el período y seleccione el método de asignación preferido. Se agrega un recurso genérico al equipo como marcador de posición. El marcador de posición contiene el patrón de demanda que se usa para reservar recursos con nombre en el equipo. El requerimiento se realiza de acuerdo con el calendario del proyecto.
- **Agregar un recurso con nombre al equipo sin consumir capacidad del recurso**: en el campo **Recurso reservable**, seleccione un recurso. Seleccione el período y luego **Ninguno** como método de asignación. El recurso se agrega al equipo, pero no se consume la capacidad del recurso con la reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservar un miembro del equipo para cumplir los requisitos de recursos de un recurso genérico

En Operaciones de proyecto, puede reservar un recurso genérico en un equipo de proyecto. También puede especificar el rol, la capacidad requerida y cómo se distribuye esa capacidad. Para el requisito de recursos, puede especificar atributos que estén asociados al recurso genérico. Estos atributos incluyen los conocimientos necesarios, la unidad organizativa preferida y los recursos preferidos.

Complete estos pasos para especificar las habilidades necesarias en un recurso genérico para un desarrollador.

1. En el formulario **Proyectos**, en la pestaña **Equipo**, seleccione **Nuevo** para reservar un recurso genérico.
2. En la vista **Todos los miembros del equipo**, en la columna **Requisitos de recursos**, seleccione el vínculo para agregar los conocimientos necesarios para el recurso genérico.
3. En el formulario **Requisito de recursos** que aparece, en la cuadrícula **Conocimientos**, seleccione los puntos suspensivos (**...**) y después seleccione **Agregar nueva característica de requisito** para agregar los conocimientos necesarios para el desarrollador.
4. En el formulario de diálogo **Creación rápida: Característica de requisito** que aparece, en el campo **Característica**, seleccione el conocimiento necesario.
5. En el campo **Valor de clasificación**, seleccione el nivel de competencia para dicho conocimiento. 
6. En el campo **Requisitos de recursos**, establezca el requisito para tomar los recursos de las unidades organizativas o incluso recursos con nombre. Cuando haya terminado, seleccione **Guardar**.
7. En el formulario **Requisito de recursos**, seleccione **Reservar** para cumplir los requisitos de recursos. También puede seleccionar el recurso genérico en la cuadrícula **Todos los miembros del equipo** y después seleccionar **Reservar**.

    > [!NOTE]
    > En este ejemplo, se necesitan 40 horas pero no hay horas reservadas reales porque los recursos genéricos no tienen reservas. Además, no hay horas asignadas porque el recurso genérico se agregó directamente al equipo, en lugar de agregarlo mediante asignación de tareas.

    En el formulario **Asistente para programación**, podrá filtrar los recursos disponibles según los requisitos especificados en el requisito de recursos. Los recursos se clasifican según los parámetros de ordenación especificados en el Tablero de programación.

   Entre los filtros usados más habitualmente se enceuntran los siguientes:

    - **Características junto con una calificación**: permite filtrar por conocimientos, certificaciones y otras cualidades de recursos, además de las calificaciones de competencia.
    - **Roles**: permite filtrar por los roles predeterminados asignados a los recursos reservables.
    - **Unidades organizativas**: permite filtrar recursos reservables por las unidades organizativas a las que están asignados.

8. Si no queda satisfecho con los resultados de la búsqueda de requisitos inicial, puede cambiar los criterios de filtro. Expanda el panel **Vista de filtro** de la izquierda y después seleccione **Buscar** para buscar recursos adicionales. Para cambiar el modo en que se ordenan los resultados, seleccione **Ordenar**.
9. Seleccione los recursos según la demanda especificada en el requisito, tal como se indica en la parte superior de la cuadrícula. Puede eliminar la selección de celdas de la cuadrícula y dejar la capacidad del recurso abierta. Solo se puede seleccionar como reservado un recurso a la vez.
10. Seleccione **Reservar** para reservar el recurso seleccionado y deje el Tablero de programación abierto para seleccionar recursos adicionales. De manera alternativa, seleccione **Reservar y salir** para reservar el recurso seleccionado y cerrar el Tablero de programación.
11. Vuelva a la vista **Todos los miembros del equipo**. En la cuadrícula, observe que el recurso genérico se ha reemplazado con el recurso con nombre y que aparecen reservadas 40 horas para dicho recurso.

    > [!NOTE]
    > No se muestran horas asignadas porque se reservaron directamente en el equipo. No se reservaron mediante una asignación de tarea.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Asignar recursos genéricos a varias tareas y generar requisitos de recurso

En Project Operations, puede crear tareas y asignarles después recursos genéricos. Después, la demanda de recursos se puede representar mediante marcadores de posición mientras se calculan la programación y las cifras financieras. De este modo, puede generar requisitos de recursos para los recursos genéricos y cumplirlos.

1. En el formulario **Proyectos**, en la pestaña **Programación**, seleccione **Agregar** para crear una tarea.
2. En el campo **Recursos**, seleccione el símbolo de **Selector de recursos**. Aparecerá el selector de recursos para mostrar los miembros del equipo existentes para el proyecto.
3. Especifique el nombre del nuevo recurso genérico y después seleccione **Crear**.
4. En el cuadro **Creación rápida: Miembro del equipo del proyecto** que aparece, en el campo **Rol**, seleccione el rol del recurso genérico. 
5. En el campo **Unidad de dotación de recursos**, seleccione la unidad organizativa para el recurso genérico. Seleccione **Guardar**. Ahora el miembro del equipo genérico está asignado a la tarea.

   En la pestaña **Equipo**, se mostrará el nuevo miembro del equipo genérico. Tenga en cuenta que solo tiene horas asignadas. Estas horas son la suma de todas las tareas que están asignadas al miembro del equipo genérico. El miembro del equipo genérico no tiene las horas necesarias o un requisito de recursos.

6. Ahora puede asignar el miembro del equipo genérico a otras tareas con el selector de recursos.

   Cuando haya terminado de asignar el recurso genérico a las tareas, puede generar un requisito de recursos para el recurso genérico.

7. En la pestaña **Equipo**, seleccione el recurso genérico y después seleccione **Generar requisito**. Cuando se genera el requisito, el miembro del equipo genérico tendrá las horas necesarias y un vínculo para el requisito de recursos.

  Tras reservar un recurso con nombre, el recurso genérico se quitará del equipo y se reemplazará con el recurso con nombre. En la pestaña **Programación**, se han quitado las asignaciones de recursos genéricos y se han reemplazado con el recurso con nombre.

  > [!NOTE]
  > Este comportamiento se produce solo cuando un recurso con nombre está totalmente reservado para el requisito de recurso genérico. Cuando un recurso con nombre reemplaza parcialmente el requisito de recurso genérico o varios recursos con nombre reemplazan el requisito de recurso genérico, el recurso genérico se mantiene asignado a la tarea.

Project Operations no asigna los dos recursos a la tarea porque ese comportamiento generaría una programación menos fiable. En este ejemplo básico resulta sencillo dividir las horas por igual entre los dos recursos. Sin embargo, en escenarios más complejas que incluyen varias tareas y varios recursos, PSA tendría que hacer suposiciones para asignar las reservas recibidas de varios recursos para varias tareas.

Por lo tanto, en estos escenarios, el administrador del proyecto es el responsable de analizar las distintas reservas y de asignarlas según sea necesario. Para asignar las reservas, el administrador de proyecto asigna las tareas de los recursos genéricos a los recursos con nombre y después utiliza la vista **Conciliación** para asegurarse de que la asignación funciona con las reservas.

### <a name="edit-a-resource-requirement"></a>Editar un requisito de recursos

Tras crear un requisito de recursos, puede que el administrador de proyecto o el administrador de recursos deseen editar los detalles para refinar los criterios de búsqueda cuando se utilice el Panel de programación. Para editar el requisito de recursos, siga los pasos que se indican a continuación.

1. En el formulario **Proyectos**, en la pestaña **Equipo**, seleccione el vínculo a cualquier requisito de un recurso genérico.
2. En el formulario **Requisito de recursos** que aparece, introduzca la información de campo necesaria

   En el formulario **Requisito de recursos**, el administrador de proyectos o el administrador de recursos también pueden definir habilidades, roles, preferencias de recursos y la unidad organizativa preferida.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Actualizar reservas de recursos tras su reserva en un proyecto

Tras agregar un recurso genérico o un recurso con nombre a un equipo de proyecto, puede cambiar las reservas del recurso.

1. En el formulario **Proyectos**, en la pestaña **Equipo**, seleccione un miembro de equipo y después seleccione **Mantener reservas**.
 
   Aparecerá el Tablero de programación y mostrará las reservas del miembro del equipo del proyecto. Expanda el registro del miembro del equipo para ver las horas que se han reservados con este proyecto y otros proyectos que consumen consumiendo la capacidad del miembro del equipo.

2. Seleccione y arrastre la reserva para ampliarla o acortarla. Aparecerá el cuadro de diálogo **Crear reserva de recursos** donde podrá ajustar la reserva.
3. Haga clic con el botón derecho en la reserva. De este modo, podrá utilizar el menú de acceso directo para completar las siguientes acciones:

    - Cambiar el estado de la reserva
    - Editar la reserva
    - Sustituir un recurso del equipo del proyecto

### <a name="change-the-booking-status"></a>Cambiar el estado de la reserva

Puede cambiar cualquier estado de reserva predeterminado o personalizado.

Project Operations incluye los estados siguientes:

- **Cancelada**: cancela la reserva de un recurso y libera la capacidad del recurso.
- **Reserva firme**: consume la capacidad de un recurso. Las reservas suelen mostrar este estado cuando se abre **Mantener reservas** desde la cuadrícula **Todos los miembros del equipo** en el formulario **Proyectos**.
- **Reserva automática**: agrega un recurso a un equipo pero no consume la capacidad del recurso. Este estado indica que se ha reservado el recurso para un posible trabajo, pero que sigue teniendo capacidad si se necesita para otros trabajos. En la vista de la disponibilidad general de recursos, las reservas automáticas muestran un estado distinto del de las reservas manuales.
- **Propuesta**: representa una propuesta de recurso de un administrador de recursos o de un administrador de proyecto. Las propuestas no consumen la capacidad de un recurso y no agregan el recurso el equipo del proyecto. Para reservar manualmente el recurso en el equipo, el administrador de proyecto debe aceptar la propuesta.

### <a name="submit-resource-requests"></a>Enviar solicitudes de recursos

Las solicitudes de recursos se utilizan para transmitir la demanda, o requisito de recursos, que el administrador de recursos debe cumplir. Para recursos genéricos que ya están en el equipo, puede enviar directamente una solicitud de recursos. Las solicitudes de recursos se pueden cumplir de dos maneras:

- El administrador de recursos cumple directamente la solicitud. En este caso, el recurso genérico se reemplaza con una reserva manual que tiene un recurso con nombre.
- El administrador de recursos propone un recurso al administrador de proyecto y el administrador de proyecto aprueba o rechaza el recurso propuesto.

#### <a name="direct-fulfillment-of-resource-requests"></a>Cumplimiento directo de las solicitudes de recursos

Cuando se genera un requisito de recursos, el administrador de proyecto puede enviar una solicitud de recurso genérico seleccionando el recurso y con la opción **Enviar solicitud**. Puede proporcionar comentarios acerca del recurso al administrador de recursos que va a cumplir la solicitud. Tas enviar la solicitud, el campo **Estado** del miembro del equipo cambia **Enviado**. Cuando el administrador de recursos cumple la solicitud, el miembro del equipo genérico se reemplaza por el recurso con nombre en la cuadrícula **Todos los miembros del equipo**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Usar una propuesta de recursos para las solicitudes de recursos

En lugar de reservar directamente un recurso en una solicitud de recursos, el administrador de recursos puede proponer un recurso al administrador de proyecto. El administrador de recursos puede usar esta opción cuando no hay ninguna coincidencia exacta para los requisitos. Cuando un administrador de recursos propone un recurso, el administrador de proyecto ve que el campo **Estado** del miembro del equipo genérico cambia a **Necesita revisión**.

Puede ver el recurso propuesto junto con una visualización del efecto de la reserva de la propuesta. 

1. Haga doble clic en el miembro del equipo que tiene un estado de **Necesita revisión**. 
2. Seleccione la pestaña **Recursos propuestos**.
3. Seleccione **Aceptar todas las propuestas** para aceptar todos los recursos propuestos, o bien seleccione **Rechazar todas las propuestas** para rechazarlas. Si acepta los recursos propuestos, estos se reservan manualmente en el proyecto como miembros del equipo y reemplazan los recursos genéricos.

> [!NOTE]
> Debe aceptar o rechazar todos los recursos propuestos. No puede rechazarlos o aceptarlos parcialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Sustituir un recurso del equipo del proyecto

A veces, el administrador del proyecto debe sustituir un miembro del equipo reservado de un proyecto.

1. En el formulario **Proyectos**, en la pestaña **Equipo**, seleccione el recurso que necesita un sustituto y después seleccione **Mantener reservas**.
2. Expanda el recurso para ver proyectos a los que está asignado.
3. Haga clic con el botón secundario y después seleccione **Sustituir recurso**.
4. Si conoce el recurso que desea sustituir como recurso actual, seleccione o escriba el nombre y después seleccione **Reasignar**.

O bien. Si necesita buscar un recurso, complete los siguientes pasos.

1. Seleccione **Encontrar sustitución**.

   El Asistente de programación devuelve una lista con los sustitutos disponibles. En el Asistente de programación, podrá filtrar aún más los recursos disponibles para encontrar un sustituto adecuado.

2. Para sustituir el recurso, seleccione el recurso deseado y después seleccione **Sustituir**.   

   Las reservas y las asignaciones se sustituyen con el nuevo recurso.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Conciliar las asignaciones y las reservas de un miembro del equipo.

Para los miembros del equipo, las reservas y las asignaciones están emparejadas, pero no de manera vinculante. En otras palabras, los recursos pueden tener asignaciones pero no tener reservas, o bien pueden tener reservas pero no tener asignaciones. Idealmente, las reservas y las asignaciones deben estar alineadas para que los recursos tengan la capacidad comprometida para realizar las tareas asignadas. No obstante, las reservas pueden basarse en la disponibilidad y los tiempos de las tareas pueden cambiar a medida que continúa el proyecto. Por lo tanto, el emparejamiento no vinculante de las reservas y las asignaciones proporciona flexibilidad.

Project Operations dispone de la pestaña **Conciliación** que permite a los administradores de proyecto conciliar las reservas y las asignaciones de los miembros de sus equipos de proyecto.

La pestaña **Conciliación** muestra las reservas y las asignaciones hasta el nivel de las asignaciones de tareas individuales de cada miembro del equipo. Muestra horas en celdas que pueden representar períodos de meses a días.

La pestaña también muestra un total neto del proyecto, junto con una columna total.

Para cada recurso, la pestaña calcula la diferencia entre las reservas de un miembro del equipo y un resumen de las asignaciones de tareas del miembro del equipo. Idealmente, esta diferencia debería ser 0 (cero). Es decir, no debería haber diferencia entre las reservas y las asignaciones. Las diferencias se muestran en color y sombreadas para llamar la atención en torno a dos condiciones:

- **Escasez de reservas**: ocurre cuando un recurso tiene más asignaciones que reservas. Puesto que esta capacidad no se ha reservado, puede que el administrador de proyecto desee corregir esa condición extendiendo las reservas del recurso para cubrir el déficit.
- **Reservas en exceso**: ocurre cuando se ha reservado un recurso para el proyecto, pero no se ha asignado a tareas. Esta condición puede ser aceptable en los casos en los que el recurso se reservó en el proyecto antes de que se produjera la asignación de tareas. Sin embargo, en otros casos, el recurso no está planificado para la asignarse a las tareas. En estos casos, el administrador de proyecto debería considerar cancelar las reservas del recurso de modo que la capacidad pueda utilizarse para otro proyecto.

En algunos casos, cuando se visualiza el tiempo a un nivel superior al nivel de días (por ejemplo, al nivel de meses), puede ver una diferencia neta de cero para un recurso. En otras palabras, reservas = asignaciones. Sin embargo, si visualiza el tiempo en el nivel de semana, puede ver que hay asignaciones de cero horas y reservas de 40 horas en la primera semana, y asignaciones de 40 horas y reservas de cero horas en la segunda semana. En general, las reservas y las asignaciones se concilian, pero hay diferencias de una semana a la siguiente.

Cuando se visualiza el tiempo a niveles más altos, las celdas de la pestaña **Conciliación** muestran un indicador para informar de que hay diferencias en los niveles de tiempo más bajos. Haga doble clic en una celda para ampliar y ver la diferencia. A continuación, puede hacer clic con el botón secundario para alejarse. Al seleccionar un recurso y luego seleccionar **Siguiente diferencia** en la barra de tareas de la cuadrícula, podrá ir a la siguiente diferencia entre las reservas y las asignaciones de dicho recurso. Seleccione **Diferencia anterior** para volver. También puede desactivar el indicador de diferencias y el comportamiento de navegación en **Configuración**.

Si tiene asignaciones de tareas para un recurso pero no tiene reservas, en el formulario **Proyectos**, en la pestaña **Conciliación**, seleccione la escasez de reservas y luego seleccione **Ampliar reservas**. Aparecerá el cuadro de diálogo **Ampliar reservas** y mostrará la reserva necesaria para abordar la escasez de recursos. El cuadro de diálogo muestra las reservas existentes del recurso en todos los proyectos o en otras entidades que se pueden programar. Si se selecciona **Aceptar** para crear la para reservar del recurso independientemente de la disponibilidad del recurso, es posible que se produzca un problema de exceso de reserva.

El administrador de proyecto o el administrador de recursos pueden usar el Tablero de programación para administrar las situaciones de exceso de reserva de un recurso más allá de su capacidad.


[!INCLUDE[footer-include](../includes/footer-banner.md)]