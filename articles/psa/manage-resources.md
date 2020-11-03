---
title: Administrar recursos
description: En este tema se proporciona información sobre cómo puede administrar los recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085349"
---
# <a name="manage-resources"></a>Administrar recursos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation incluye un panel de administrador de recursos que proporciona información general visual de la utilización y la demanda de recursos en la organización. Puede usar los gráficos de este panel para visualizar la siguiente información:

- **Demanda de recursos** : el gráfico **Solicitudes de recursos activas** muestra los recursos que se han enviado. Los recursos se agregan por rol o por proyecto.
- **Demanda de recursos no enviada** : el gráfico **Demanda de recursos sin asignar** muestra todos los requisitos de recursos que no se han enviado. Ayuda a los administradores de recursos a ver la demanda que no es firme y que se puede enviar con una solicitud de recursos.
- **Utilización facturable de la última semana** : el gráfico **Uso por rol** muestra el porcentaje de uso facturable real de la organización por rol con respecto al uso facturable objetivo por rol.

    > [!NOTE]
    > Para que el gráfico **Uso por rol** esté disponible, cree un trabajo que ejecute el flujo de trabajo UpdateRoleUtilization. Este trabajo periódico se ejecuta cada siete días para calcular el uso facturable de los siete días anteriores. Los resultados se agregan por rol.

## <a name="manage-project-team-members"></a>Administrar miembros del equipo del proyecto

Los jefes de proyecto pueden usar el panel de administrador de recursos para administrar los recursos de los proyectos. Por ejemplo, pueden agregar un miembro del equipo directamente a un proyecto y reservar un miembro del equipo para cumplir los requisitos de recursos que capturó un recurso genérico.

### <a name="add-a-team-member-directly-to-a-project"></a>Agregar un miembro del equipo directamente a un proyecto

Para agregar un miembro del equipo directamente a un proyecto, en la página **Proyectos** , en la pestaña **Equipo** , seleccione **Nuevo**. Aparecerá el cuadro de diálogo **Creación rápida: Miembro del equipo del proyecto**. En este cuadro de diálogo, podrá realizar las tareas siguientes:

- **Reservar un recurso con nombre** : en el campo **Recurso que se puede reservar** , seleccione el nombre del recurso. Después, seleccione el rol, defina el período y seleccione un método de asignación. El recurso con nombre seleccionado se agrega al proyecto mediante el método de asignación seleccionado y el calendario de recursos.
- **Agregar un recurso genérico** : deje el campo **Recurso que se puede reservar** en blanco y después seleccione el rol, defina el período y seleccione el método de asignación preferido. Se agregará al equipo un recurso genérico como marcador de posición para conservar el patrón de demanda que se utiliza para reservar recursos con nombre en el equipo. El requisito se crea según el calendario del proyecto.
- **Agregar un recurso con nombre al equipo sin consumir capacidad del recurso** : en el campo **Recurso que se puede reservar** , seleccione un recurso. Después, seleccione el período y seleccione **Ninguno** como método de asignación. El recurso se agrega al equipo, pero no se consume la capacidad del recurso con la reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservar un miembro del equipo para cumplir los requisitos de recursos de un recurso genérico

En PSA, puede para reservar un recurso genérico en un equipo de proyecto y puede especificar el rol, la capacidad necesaria y el modo en que se distribuirá dicha capacidad. En el requisito del recurso, puede especificar los atributos asociados al recurso genérico. Estos atributos incluyen los conocimientos necesarios, la unidad organizativa preferida y los recursos preferidos.

Siga estos pasos para especificar los conocimientos necesarios en un recurso genérico para un desarrollador.

1. En la página **Proyectos** , en la pestaña **Equipo** , seleccione **Nuevo** para reservar un recurso genérico.

    ![Recurso genérico reservado en el equipo.](media/Resource-Management-image9.png)

2. En la vista **Todos los miembros del equipo** , en la columna **Requisitos de recursos** , seleccione el vínculo para agregar los conocimientos necesarios para el recurso genérico.

    ![Vínculo de requisito.](media/Resource-Management-image10.png)

3. En la página **Requisito de recursos** que aparece, en la cuadrícula **Conocimientos** , seleccione los puntos suspensivos ( **...** ) y después seleccione **Agregar nueva característica de requisito** para agregar los conocimientos necesarios para el desarrollador.

    ![Comando para agregar nueva característica de requisito.](media/Resource-Management-image11.png)

4. En el cuadro **Creación rápida: Característica de requisito** que aparece, en el campo **Característica** , seleccione el conocimiento necesario. Después, el campo **Valor de clasificación** , seleccione el nivel de competencia para dicho conocimiento. Por último, en el campo **Requisitos de recursos** , establezca el requisito de tomar los recursos de las unidades organizativas o incluso recursos con nombre. Cuando haya terminado, seleccione **Guardar**.

    ![Cuadro de diálogo Creación rápida: Característica de requisito](media/Resource-Management-image12.png)

5. En la página **Requisito de recursos** , seleccione **Reservar** para cumplir los requisitos de recursos.

    ![Botón Reservar de en la página Requisito de recursos.](media/Resource-Management-image13.png)

    También puede seleccionar el recurso genérico en la cuadrícula **Todos los miembros del equipo** y después seleccionar **Reservar**.

    ![Botón Reservar sobre la cuadrícula Todos los miembros del equipo.](media/Resource-Management-image14.png)

    > [!NOTE]
    > En este ejemplo, se necesitan 40 horas pero no hay horas reservadas reales porque los recursos genéricos no tienen reservas. Además, no hay horas asignadas porque el recurso genérico se agregó directamente al equipo. No se agregó mediante la asignación de tareas.

    En la página **Asistente para programación** , podrá filtrar los recursos disponibles según los requisitos especificados en el requisito de recursos. Los recursos se clasifican según los parámetros de ordenación especificados en el Tablero de programación.

    ![Página Asistente para programación.](media/Resource-Management-image15.png)

    A continuación se describen algunos de los filtros que se utilizan más a menudo:

    - **Características junto con una calificación** : permite filtrar por conocimientos, certificaciones y otras cualidades de recursos, además de las calificaciones de competencia.
    - **Roles** : permite filtrar por los roles predeterminados asignados a los recursos que se pueden reservar.
    - **Unidades organizativas** : permite filtrar recursos que se pueden reservar por las unidades organizativas a las que están asignados.

6. Si no queda satisfecho con los resultados de la búsqueda de requisitos inicial, puede cambiar los criterios de filtro. Expanda el panel **Vista de filtro** de la izquierda y después seleccione **Buscar** para buscar recursos adicionales.

    ![Panel Vista de filtro.](media/Resource-Management-image16.png)

7. Para cambiar el modo en que se ordenan los resultados, seleccione **Ordenar**.

    ![Comando Ordenar.](media/Resource-Management-image17.png)

8. Seleccione los recursos según la demanda especificada en el requisito, tal como se indica en la parte superior de la cuadrícula. Puede eliminar la selección de celdas de la cuadrícula y dejar la capacidad del recurso abierta. Solo se puede seleccionar como reservado un recurso a la vez.

9. Seleccione **Reservar** para reservar el recurso seleccionado y deje el Tablero de programación abierto para seleccionar recursos adicionales. De manera alternativa, seleccione **Reservar y salir** para reservar el recurso seleccionado y cerrar el Tablero de programación.

    ![Recurso que se va a reservar.](media/Resource-Management-image19.png)

    Recibirá una notificación sobre horas reservadas. Los indicadores de demanda muestran la proporción de satisfacción del requisito de la reserva y cuánto falta por satisfacer. También puede ver la capacidad consumida del recurso seleccionado. Seleccione **Expandir** para ver más detalles sobre las reservas de recursos.

9. Vuelva a la vista **Todos los miembros del equipo**. En la cuadrícula, observe que el recurso genérico se ha reemplazado con el recurso con nombre y que aparecen reservadas 40 horas para dicho recurso.

    ![Cuadrícula Todos los miembros del equipo actualizada.](media/Resource-Management-image20.png)

    > [!NOTE]
    > No se muestran horas asignadas porque se reservaron directamente en el equipo. No se reservaron mediante una asignación de tarea.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Asignar recursos genéricos a varias tareas y generar requisitos de recurso

En PSA, puede crear tareas y asignar después recursos genéricos a ellas. De esta forma, se puede representar la demanda de recursos con marcadores de posición mientras realiza una estimación de su programación y de sus finanzas. De este modo, puede generar requisitos de recursos para los recursos genéricos y cumplirlos.

1. En la página **Proyectos** , en la pestaña **Programación** , seleccione **Agregar** para crear una tarea.

    ![Nueva tarea creada.](media/Resource-Management-image21.png)

2. En el campo **Recursos** , seleccione el símbolo de **Selector de recursos**. Aparecerá el selector de recursos para mostrar los miembros del equipo existentes para el proyecto.

    ![Selector de recursos.](media/Resource-Management-image22.png)

3. Especifique el nombre del nuevo recurso genérico y después seleccione **Crear**.

    ![Nombre del recurso genérico especificado.](media/Resource-Management-image23.png)

4. En el cuadro **Creación rápida: Miembro del equipo del proyecto** que aparece, en el campo **Rol** , seleccione el rol del recurso genérico. En el campo **Unidad de dotación de recursos** , seleccione la unidad organizativa para el recurso genérico. Seleccione **Guardar**.

    ![Cuadro de diálogo Creación rápida: Miembro del equipo del proyecto.](media/Resource-Management-image24.png)

    Ahora el miembro del equipo genérico está asignado a la tarea.

    ![Miembro del equipo genérico asignado a la tarea.](media/Resource-Management-image25.png)

    En la pestaña **Equipo** , se mostrará el nuevo miembro del equipo genérico. Tenga en cuenta que solo tiene horas asignadas. Estas horas son la suma de todas las tareas que están asignadas al miembro del equipo genérico. El miembro del equipo genérico aún no tiene horas necesarias o un requisito de recursos.

    ![Miembro del equipo genérico en la pestaña Equipo.](media/Resource-Management-image26.png)

5. Ahora puede asignar el miembro del equipo genérico a otras tareas con el selector de recursos.

    ![Miembro del equipo genérico en el selector de recursos.](media/Resource-Management-image27.png)

    Cuando haya terminado de asignar el recurso genérico a las tareas, puede generar un requisito de recursos para el recurso genérico.

5. En la pestaña **Equipo** , seleccione el recurso genérico y después seleccione **Generar requisito**.

    ![Comando Generar requisito.](media/Resource-Management-image28.png)

    Cuando se genera el requisito, el miembro del equipo genérico tendrá las horas necesarias y un vínculo para el requisito de recursos.

    ![Vínculo de requisito de recursos.](media/Resource-Management-image29.png)

    Tras reservar un recurso con nombre, el recurso genérico se quitará del equipo y se reemplazará con el recurso con nombre.

    ![Recurso genérico reemplazado por el recurso con nombre.](media/Resource-Management-image30.png)

    En la pestaña **Programación** , se han quitado las asignaciones de recursos genéricos y se han reemplazado con el recurso con nombre.

    ![Asignaciones de recursos genéricos reemplazadas con el recurso con nombre en la pestaña Programación.](media/Resource-Management-image31.png)

    > [!NOTE]
    > Este comportamiento se produce solo cuando un recurso con nombre está totalmente reservado para el requisito de recurso genérico. Cuando un recurso con nombre reemplaza parcialmente el requisito de recurso genérico o varios recursos con nombre reemplazan el requisito de recurso genérico, el recurso genérico se mantiene asignado a la tarea.

    En la siguiente ilustración, una tarea de 80 horas se ha planeado con una duración de cinco días (16 horas al día durante cinco días) y se ha asignado al recurso genérico con el nombre **Funcional**.

    ![Tarea de ochenta horas durante cinco días asignada al recurso genérico Funcional.](media/Resource-Management-image32.png)

    Cuando se genera el requisito, se genera para 80 horas durante cinco días.

    ![Requisito generado por 80 horas durante cinco días.](media/Resource-Management-image33.png)

    Puesto que los recursos disponibles solo trabajan 8 horas al día, se necesitan dos recursos para cumplir el requisito.

    ![Segundo recurso.](media/Resource-Management-image35.png)

    En la pestaña **Equipo** , ahora podrá ver que el recurso genérico no tiene horas necesarias, aunque las horas asignadas siguen apareciendo juntas con dos recursos con nombre que forman el cumplimiento.

    ![Dos recursos con nombre en la pestaña Equipo.](media/Resource-Management-image36.png)

    En la pestaña **Programación** , el recurso genérico permanece asignado a la tarea.

    ![Recursos genéricos en pestaña Programación.](media/Resource-Management-image37.png)

PSA, no asignar a los dos recursos a la tarea porque ese comportamiento generaría una programación menos fiable. En este ejemplo básico resulta sencillo dividir las horas por igual entre los dos recursos. Sin embargo, en escenarios más complejas que incluyen varias tareas y varios recursos, PSA tendría que hacer suposiciones para asignar las reservas recibidas de varios recursos para varias tareas.

Por lo tanto, en estos escenarios, el jefe del proyecto es el responsable de analizar las distintas reservas y de asignarlas según sea necesario. Para asignar las reservas, el jefe de proyecto asigna las tareas de los recursos genéricos a los recursos con nombre y después utiliza la vista **Conciliación** para asegurarse de que la asignación funciona con las reservas.

### <a name="edit-a-resource-requirement"></a>Editar un requisito de recursos

Tras crear un requisito de recursos, puede que el jefe de proyecto o el administrador de recursos deseen editar los detalles para refinar los criterios de búsqueda cuando se utilice el Tablero de programación. Para editar el requisito de recursos, siga los pasos que se indican a continuación.

1. En la página **Proyectos** , en la pestaña **Equipo** , seleccione el vínculo a cualquier requisito de un recurso genérico.
2. En la página **Requisito de recursos** que aparecerá, podrá actualizar varios atributos. A continuación, encontrará algunos ejemplos:

    - Nombre
    - Desde la fecha
    - Hasta la fecha
    - Duración
    - Tipo de recurso

En la página **Requisito de recursos** , el jefe de proyecto o el administrador de recursos también pueden definir la siguiente información:

- Aptitudes
- Roles
- Preferencias de recursos
- Unidad organizativa preferida

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Actualizar reservas de recursos tras su reserva en un proyecto

Tras agregar un recurso genérico o un recurso con nombre a un equipo de proyecto, puede cambiar las reservas del recurso.

1. En la página **Proyectos** , en la pestaña **Equipo** , seleccione un miembro de equipo y después seleccione **Mantener reservas**.

    ![Tablero de programación abierto para el miembro de equipo seleccionado.](media/Resource-Management-image40.png)

    Aparecerá el Tablero de programación y mostrará las reservas del miembro del equipo del proyecto. Expanda el registro del miembro del equipo para ver las horas que se han reservados con este proyecto y otros proyectos que consumen consumiendo la capacidad del miembro del equipo.

2. Seleccione y arrastre la reserva para ampliarla o acortarla. Aparecerá el cuadro de diálogo **Crear reserva de recursos** donde podrá ajustar la reserva.

    ![Cuadro de diálogo Crear reserva de recursos.](media/Resource-Management-image41.png)

3. Haga clic con el botón derecho en la reserva. De este modo, podrá utilizar el menú de acceso directo para completar las siguientes acciones:

    - Cambiar el estado de la reserva.
    - Editar la reserva.
    - Sustituir un recurso del equipo del proyecto.

### <a name="change-the-booking-status"></a>Cambiar el estado de la reserva

Puede cambiar cualquier estado de reserva predeterminado o personalizado.

![Comando Cambiar estado.](media/Resource-Management-image42.png)

PSA incluye los estados siguientes:

- **Cancelada** : este estado cancela la reserva de un recurso y libera la capacidad del recurso.
- **Reserva manual** : este estado consume la capacidad de un recurso. Las reservas suelen mostrar este estado cuando se abre **Mantener reservas** desde la cuadrícula **Todos los miembros del equipo** en la página **Proyectos**.
- **Reserva automática** : este estado agrega un recurso a un equipo pero no consume la capacidad del recurso. Indica que se ha reservado el recurso para un posible trabajo, pero que sigue teniendo capacidad si se necesita para otros trabajos. En la vista de la disponibilidad general de recursos, las reservas automáticas muestran un estado distinto del de las reservas manuales.
- **Propuesta** : este estado representa una propuesta de recurso de un administrador de recursos o de un jefe de proyecto. Las propuestas no consumen la capacidad de un recurso y no agregan el recurso el equipo del proyecto. Para reservar manualmente el recurso en el equipo, el jefe de proyecto debe aceptar la propuesta.

### <a name="submit-resource-requests"></a>Enviar solicitudes de recursos

Las solicitudes de recursos se utilizan para transmitir la demanda (requisito de recursos) que el administrador de recursos debe cumplir. Para recursos genéricos que ya están en el equipo, puede enviar directamente una solicitud de recursos. Las solicitudes de recursos se pueden cumplir de dos maneras:

- El administrador de recursos cumple directamente la solicitud. En este caso, el recurso genérico se reemplaza con una reserva manual que tiene un recurso con nombre.
- El administrador de recursos propone un recurso al jefe de proyecto y el jefe de proyecto aprueba o rechaza el recurso propuesto.

#### <a name="direct-fulfillment-of-resource-requests"></a>Cumplimiento directo de las solicitudes de recursos

Cuando se genera un requisito de recursos, el jefe de proyecto puede enviar una solicitud de recurso genérico seleccionando el recurso y con la opción **Enviar solicitud**.

![Botón Enviar solicitud.](media/Resource-Management-image45.png)

Puede proporcionar comentarios acerca del recurso al administrador de recursos que va a cumplir la solicitud. Tas enviar la solicitud, el campo **Estado** del miembro del equipo cambia **Enviado**.

![Especificación de comentarios opcionales.](media/Resource-Management-image46.png)

Cuando el administrador de recursos cumple la solicitud, el miembro del equipo genérico se reemplaza por el recurso con nombre en la cuadrícula **Todos los miembros del equipo**.

![Miembro del equipo genérico reemplazado por el recurso con nombre en la cuadrícula Todos los miembros del equipo.](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Usar una propuesta de recursos para las solicitudes de recursos

En lugar de reservar directamente un recurso en una solicitud de recursos, el administrador de recursos puede proponer un recurso al jefe de proyecto. El administrador de recursos puede usar esta opción cuando no hay ninguna coincidencia exacta para los requisitos. Cuando un administrador de recursos propone un recurso, el jefe de proyecto ve que el campo **Estado** del miembro del equipo genérico cambia a **Necesita revisión**.

![Cambio del estado del miembro del equipo genérico a Necesita revisión.](media/Resource-Management-image48.png)

Para ver el recurso propuesto junto a una visualización del efecto de la reserva de la propuesta, haga doble clic en el miembro del equipo que tiene el estado **Necesita revisión**. A continuación, seleccione la pestaña **Recursos propuestos**.

![Pestaña Recursos propuestos.](media/Resource-Management-image49.png)

Seleccione **Aceptar todas las propuestas** para aceptar todos los recursos propuestos, o bien seleccione **Rechazar todas las propuestas** para rechazarlas. Si acepta los recursos propuestos, estos se reservan manualmente en el proyecto como miembros del equipo y reemplazan los recursos genéricos.

> [!NOTE]
> Debe aceptar o rechazar todos los recursos propuestos. No puede rechazarlos o aceptarlos parcialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Sustituir un recurso del equipo del proyecto

A veces, el jefe del proyecto debe sustituir un miembro del equipo reservado de un proyecto.

1. En la página **Proyectos** , en la pestaña **Equipo** , seleccione el recurso que necesita un sustituto y después seleccione **Mantener reservas**.
2. Expanda el recurso para ver proyectos a los que está asignado.

    ![Recurso expandido para mostrar los proyectos asignados.](media/Resource-Management-image50.png)

3. Haga clic con el botón secundario y después seleccione **Sustituir recurso**.
4. Si conoce el recurso que desea sustituir como recurso actual, seleccione o escriba el nombre y después seleccione **Reasignar**.

    ![Especificación de un recurso de sustitución.](media/Resource-Management-image51.png)

    De manera alternativa, puede seguir estos pasos para buscar un recurso:

    1. Seleccione **Encontrar sustitución**.

        ![Búsqueda de un recursos de sustitución.](media/Resource-Management-image52.png)

        El Asistente de programación devuelve una lista con los sustitutos disponibles. En el Asistente de programación, podrá filtrar aún más los recursos disponibles para encontrar un sustituto adecuado.

        ![Lista de sustitutos disponibles.](media/Resource-Management-image53.png)

    2. Para sustituir el recurso, seleccione el recurso deseado y después seleccione **Sustituir**.

        ![Recurso de sustitución seleccionado.](media/Resource-Management-image54.png)

    Las reservas y las asignaciones se sustituyen con el nuevo recurso.

    ![Sustitución de las reservas y las asignaciones con el nuevo recurso.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Conciliar las asignaciones y las reservas de un miembro del equipo.

Para los miembros del equipo, las reservas y las asignaciones están emparejadas, pero no de manera vinculante. En otras palabras, los recursos pueden tener asignaciones pero no tener reservas, o bien pueden tener reservas pero no tener asignaciones. Idealmente, las reservas y las asignaciones deben estar alineadas para que los recursos tengan la capacidad comprometida para realizar las tareas asignadas. Sin embargo, las reservas pueden estar basadas en la disponibilidad y el control de tiempo de las tareas puede cambiar a medida que avanza el proyecto. Por lo tanto, el emparejamiento no vinculante de las reservas y las asignaciones proporciona flexibilidad.

PSA dispone de la pestaña **Conciliación** que permite a los jefes de proyecto conciliar las reservas y las asignaciones de los miembros de sus equipos de proyecto.

![Pestaña Conciliación.](media/Resource-Management-image56.png)

La pestaña **Conciliación** muestra las reservas y las asignaciones hasta el nivel de las asignaciones de tareas individuales de cada miembro del equipo. Muestra horas en celdas que pueden representar períodos de meses a días.

La pestaña también muestra un total neto del proyecto, junto con una columna total.

Para cada recurso, la pestaña calcula la diferencia entre las reservas de un miembro del equipo y un resumen de las asignaciones de tareas del miembro del equipo. Idealmente, esta diferencia debería ser 0 (cero). Es decir, no debería haber diferencia entre las reservas y las asignaciones. Las diferencias se muestran en color y sombreadas para llamar la atención en torno a dos condiciones:

- **Escasez de reservas** : la escasez de reservas se produce cuando un recurso tiene más asignaciones que reservas. Puesto que esta capacidad no se ha reservado, puede que el jefe de proyecto desee corregir esa condición extendiendo las reservas del recurso para cubrir el déficit.
- **Reservas en exceso** : las reservas en exceso se producen cuando se ha reservado un recurso para el proyecto, pero no se ha asignado a tareas. Esta condición podría ser aceptable en los casos en los que el recurso se reservó para el proyecto antes de que se produjera la asignación de tareas. Sin embargo, en otros casos, el recurso no está planificado para la asignarse a las tareas. En estos casos, el jefe de proyecto debería considerar cancelar las reservas del recurso de modo que la capacidad pueda utilizarse para otro proyecto.

En algunos casos, cuando se visualiza el tiempo a un nivel superior que el nivel de días (por ejemplo, el nivel de meses), puede ver una diferencia neta de cero para un recurso (es decir, reservas = asignaciones). Sin embargo, si visualiza el tiempo en el nivel de semana, puede ver que hay asignaciones de cero horas y reservas de 40 horas en la primera semana, y asignaciones de 40 horas y reservas de cero horas en la segunda semana. En general, las reservas y las asignaciones se concilian, pero hay diferencias de una semana a la siguiente.

Cuando se visualiza el tiempo a niveles más altos, las celdas de la pestaña **Conciliación** muestran un indicador para informar de que hay diferencias en los niveles de tiempo más bajos. Al hacer doble clic en una celda, podrá acercarse para ver la diferencia. A continuación, puede hacer clic con el botón secundario para alejarse. Al seleccionar un recurso y utilizar el control **Siguiente diferencia** de la barra de tareas de la cuadrícula, podrá ir a la siguiente diferencia entre las reservas y las asignaciones de dicho recurso. Puede usar posteriormente el control **Diferencia anterior** para volver. También puede desactivar el indicador de diferencias y el comportamiento de navegación en **Configuración**.

![Indicador de diferencia.](media/Resource-Management-image57.png)

Si tiene asignaciones de tareas para un recurso pero no tiene reservas, en la página **Proyectos** , en la pestaña **Conciliación** , seleccione la escasez de reservas y luego seleccione **Ampliar reservas**. Aparecerá el cuadro de diálogo **Ampliar reservas** y mostrará la reserva necesaria para abordar la escasez de recursos. También muestra las reservas existentes del recurso en todos los proyectos o en otras entidades que se pueden programar. Si se selecciona **Aceptar** para crear la para reservar del recurso independientemente de la disponibilidad del recurso, es posible que se produzca un problema de exceso de reserva.

![Cuadro de diálogo Ampliar reservas.](media/Resource-Management-image58.png)

El jefe de proyecto o el administrador de recursos pueden usar el Tablero de programación para administrar las situaciones de exceso de reserva de un recurso más allá de su capacidad.
