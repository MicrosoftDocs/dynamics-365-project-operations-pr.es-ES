---
title: Recursos del proyecto
description: En este tema se proporciona información sobre los recursos del proyecto.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755942"
---
# <a name="project-resourcing"></a>Recursos del proyecto

[!include [banner](../includes/banner.md)]

En este tema se proporciona información sobre los recursos del proyecto.

Un desafío para los jefes de proyectos y los administradores de recursos durante la etapa de planificación del proyecto es la asignación de recursos, donde deben determinar y reservar el recurso correcto para trabajar en un proyecto. En Dynamics 365 Finance, las funcionalidades de dotación de recursos para proyectos le permiten definir roles que se tratan como recursos temporales que se pueden reservar para un compromiso específico o parte de un compromiso. Este tipo de dotación de recursos permite a los jefes de proyectos y los de recursos completar las siguientes tareas:

- Definir un rol que tenga las competencias necesarias, de modo que sea fácil combinar los recursos.
- Utilizar roles para definir un programa de participación inicial que se base en recursos reservados.
- Calcular costes y determinar un presupuesto inicial, basado en roles y recursos asignados para un proyecto.
- Usar roles para estimar la cantidad de reservas de recursos que se requieren para cada interacción.
- Calcular la cantidad de recursos necesarios para todo el ciclo de vida de un proyecto.
- Hacer un borrador de una estructura de descomposición del trabajo (WBS) utilizando las asignaciones de recursos iniciales.

[![Ciclo de vida del proyecto](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

A medida que avanza la planificación del proyecto, los recursos planificados se pueden reemplazar con recursos de personal. El jefe de proyectos también puede volver atrás y actualizar las reservas de dotación de recursos durante cualquier etapa del proyecto.

## <a name="set-up-project-resources"></a>Configurar los recursos del proyecto
Debe configurar un calendario y asociarlo con un empleado o un trabajador. El calendario se utiliza para programar el proyecto y el tiempo de trabajo de los recursos que están reservados para el proyecto. Durante la configuración del calendario, los administradores de proyectos pueden nivelar los recursos como parte de la optimización de los recursos. Según la programación del calendario, se pueden imponer restricciones a los recursos. Puede configurar un calendario en la página **Calendarios**.

Cuando configura un trabajador como recurso del proyecto, puede seleccionar entre los trabajadores que trabajan en la empresa para la que está configurando los recursos. Alternativamente, puede seleccionar trabajadores de otras empresas de su organización. Estos trabajadores se conocen como recursos de empresas vinculadas.

Los siguientes procedimientos explican cómo configurar un trabajador como recurso de proyecto en su empresa y cómo configurar un recurso de proyecto de empresas vinculadas.

### <a name="set-up-a-worker-as-a-project-resource"></a>Configurar un trabajador como recurso de proyecto

1. En la página **Trabajadores**, en lista **Trabajadores**, seleccione el trabajador que está agregando como recurso del proyecto y abra el registro del trabajador.
2. En el panel de acciones, seleccione **Proyecto** &gt; **Configurar** &gt; **Configuración del proyecto**.
3. Seleccione un calendario y cierre la página.

También puede especificar proyectos predeterminados para un recurso como un tipo de asignación previa. Las asignaciones previas se pueden usar cuando el administrador de recursos o el administrador de proyectos sepan con anticipación en qué proyectos trabajará el recurso. Las asignaciones previas también pueden basarse en la solicitud de un cliente o patrocinador del proyecto. Para asignar previamente un proyecto, en la página **Asignar proyectos**, en la pestaña **Proyectos**, en la lista **Proyectos restantes**, seleccione el proyecto apropiado.

### <a name="set-up-an-intercompany-resource"></a>Configurar un recurso de empresas vinculadas

Cuando configura un trabajador como recurso de empresas vinculadas, debe completar la configuración tanto en la empresa prestamista como en la empresa prestataria.

**En la empresa prestamista**

1. En Finance, verifique que la empresa prestamista esté seleccionada y luego complete el procedimiento de la sección anterior, "Configurar un trabajador como recurso de proyecto".
2. En la página **Contabilidad de empresas vinculadas**, seleccione **+Nuevo**.
3. En el campo **Id. de entidad legal**, seleccione la empresa prestamista. Rellene los campos restantes como corresponda y seleccione **Guardar**.
4. En la página **Transferir precios**, seleccione **Nuevo**.
5. En el campo **Entidad legal prestataria**, seleccione la empresa apropiada.
6. Para prestar a la empresa prestataria solo el recurso que creó al principio de esta sección, en el campo **Recurso**, seleccione el nombre del recurso que creó. Para que todos los recursos de la empresa prestamista estén disponibles para la empresa prestataria, deje el campo **Recurso** en blanco.
7. En la página **Parámetros de gestión de proyectos y contabilidad**, en la pestaña **Empresas vinculadas**, establezca la opción **Habilitar la programación de recursos y las hojas de horas de empresas vinculadas** en **Sí**.

**En la empresa prestataria**

- En la página **Lista de recursos**, en el filtro de búsqueda, especifique el nombre del recurso que creó para la empresa prestamista, para verificar que el nombre esté incluido en la lista de recursos para la empresa prestataria.

## <a name="manage-resource-competencies"></a>Administrar competencias de recursos
Las competencias de recursos son una parte esencial de la gestión de recursos. Las competencias se pueden utilizar como referencia para determinar los recursos que tienen un equilibrio correcto de habilidades, educación, certificación y experiencia en proyectos. Debe configurar esta información para cada recurso y actualizarla periódicamente. De esta manera, puede maximizar las capacidades cuando se asignan competencias de recursos específicos durante la asignación de recursos del proyecto.

[![Ejemplos de habilidades, certificaciones, educación y experiencia en proyectos](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Los siguientes procedimientos explican cómo configurar algunas de las competencias para un recurso.

Para configurar las competencias de un trabajador, puede utilizar la página de la lista **Trabajadores** en Recursos humanos o la página de la lista **Recursos** de lista en Gestión de proyectos y contabilidad. Para los siguientes procedimientos, se usa la página de la lista **Trabajadores** en Recursos humanos.

### <a name="set-up-competencies-certificates"></a>Configurar competencias: Certificados

1. En página de la lista **Trabajadores**, seleccione la línea para que el trabajador agregue la información del certificado.
2. En el panel de acciones, en la pestaña **Trabajador**, en el grupo **Competencias**, seleccione **Certificados**.
3. Seleccione **Nuevo** y, después, en el campo **Tipo de certificado**, seleccione **PMP**.
4. En el campo **Fecha de inicio**, seleccione **1/10/2015** y **Guardar**.

### <a name="set-up-competencies-skills"></a>Configurar competencias: Aptitudes

1. En página de la lista **Trabajadores**, asegúrese de que el trabajador que utilizó en el procedimiento anterior aún esté seleccionado. Después, en el panel de acciones, en la pestaña **Trabajador**, en el grupo **Competencias**, seleccione **Aptitudes**.
2. Seleccione **Nuevo**.
3. En el campo **Aptitud**, seleccione **Gestión de proyectos**.
4. En el campo **Nivel**, seleccione **Experto 5**.
5. En el campo **Fecha del nivel**, seleccione **1-/14/2014**.
6. En el campo **Años de experiencia**, escriba **10**.
7. Seleccione **Guardar** y cierre la página.

## <a name="create-a-new-project"></a>Crear un nuevo proyecto
1. En la página **Gestión de proyectos**, seleccione **Nuevo proyecto**, e indique los valores siguientes:

    - **Tipo de proyecto**: Tiempo y material
    - **Nombre del proyecto**: Fase 2 de la actualización XYZ
    - **Grupo de proyecto**: TM\_WIP
    - **Id. de contrato de proyecto**: 00000002

2. Seleccione **Crear proyecto**.

### <a name="assign-a-resource-to-a-project"></a>Asignar un recurso a un proyecto

1. En la página **Trabajadores**, en la lista **Trabajadores**, seleccione el registro del trabajador para el que definió las competencias anteriormente y abra el registro del trabajador.
2. En el panel de acciones, en la pestaña **Proyecto**, en el grupo **Configurar**, seleccione **Asignar proyectos**.
3. En la página **Asignaciones de proyectos de validación de recursos**, en la pestaña **Proyectos**, en el campo **Agregar el proyecto a los proyectos seleccionados**, filtrar en el proyecto **Fase 2 de la actualización XYZ**.
4. En el panel **Proyectos restantes**, seleccione un proyecto y luego seleccione el botón de flecha para agregarlo al panel **Proyectos seleccionados**.

También puede asignar categorías para un recurso según lo requiera. El tipo de categoría es **Coste** o **Ingresos**. El tipo de categoría lo determina su organización. Si no se asignan categorías para un recurso, Finance busca la categoría predeterminada en precios por hora para costes e ingresos.

### <a name="set-up-project-resource-and-role-characteristics"></a>Configurar las características de los roles y los recursos del proyecto

Un jefe de proyecto puede utilizar la funcionalidad de dotación de recursos de proyecto para crear los roles necesarios para el proyecto. Los roles se pueden usar si los recursos confirmados aún se desconocen cuando se reservan los recursos. Los roles se pueden reservar temporalmente como recursos planificados, para que pueda continuar con las etapas de planificación del proyecto.

[![Ejemplo de un rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Escenario**: Contoso fue contratado para completar un proyecto de tiempo y material que tiene un estado de proyecto aprobado. El jefe de proyecto junior aún está completando el alcance del proyecto. El administrador de recursos actualmente está identificando recursos específicos que se reservarán para trabajar en el nuevo proyecto. Debido a la naturaleza crítica del proyecto, el patrocinador del proyecto solicitó jefe de proyecto senior como uno de los roles. El administrador de recursos debe adquirir el nuevo recurso y definir el rol en el sistema en caso de que el jefe de proyectos junior requiera la información de recursos durante la planificación del proyecto.

Los siguientes pasos muestran cómo el administrador de recursos puede configurar el rol de jefe de proyectos senior y asociar características de recursos con él. Posteriormente, el rol se puede utilizar para buscar recursos disponibles que coincidan con las competencias de recursos requeridas.

1. En la página **Configurar roles**, seleccione **Nuevo**, e indique los valores siguientes:

    - **Id. del rol**: jefe de proyectos sénior
    - **Descripción**: jefe de proyectos sénior

2. Seleccione **Crear**.
3. Selecciona el rol **Jefe de proyectos sénior** y luego seleccione **Configurar características**.
4. En el campo **Tipo de característica**, seleccione **Aptitud**.
5. En el campo **Características disponibles**, indique la aptitud que desea buscar.
6. En el campo **Tipo de característica**, seleccione **Certificado**.
7. En el campo **Características disponibles**, indique el tipo de certificado que desea buscar.

### <a name="assign-a-project-resource-to-a-project"></a>Asignar un recurso de proyecto a un proyecto

1. En la página **Todos los proyectos**, seleccione el proyecto **Fase 2 de la actualización XYZ**.
2. En la pestaña **Equipo de proyecto y programación**, seleccione **Agregar**.
3. En el campo **Rol** campo, seleccione **Miembro del equipo**.
4. Seleccione **Reservar en el calendario**.
5. En la página **Disponibilidad de recursos**, seleccione **Ver configuraciones**.
6. En la página **Ajustar la configuración de la vista**, escriba los siguientes valores:

    - **Formato para la vista de rango de fechas**: Día
    - **Mostrar descripciones de disponibilidad**: Sí
    - **Mostrar capacidad restante**: Sí

7. En la lista de recursos, seleccione un recurso.
8. Seleccione **Reserva manual** y **Capacidad completa**.


### <a name="assign-a-resource-to-a-default-role"></a>Asignar un recurso a un rol predeterminado

Para ayudar a los administradores de proyectos o recursos pueden explorar en profundidad más sobre los recursos que se pueden reservar para un proyecto. Puede asociar un rol predeterminado con un recurso existente o un recurso recién adquirido. Por ejemplo, cuando contrataron a Daniel, tenía la experiencia y las aptitudes para ocupar el puesto de analista comercial. El administrador de recursos asignó este rol como el rol predeterminado de Daniel. Por lo tanto, el administrador de recursos agregó a Daniel a un grupo de analistas comerciales que están disponibles para trabajar en proyectos.

Durante la reserva de recursos, los jefes de proyecto pueden filtrar los recursos de roles que están disponibles para trabajar en proyectos. Pueden utilizar esta información como un criterio cuando realizan análisis de decisiones de criterios múltiples durante la ejecución de los recursos. También pueden agregar otras características de recursos al filtro para buscar recursos que tengan aptitudes, educación y experiencia específicas para un proyecto determinado.

**Escenario**: se ha iniciado un proyecto aprobado y se reservó el rol de jefe de proyecto sénior como recurso planificado durante la etapa de planificación del proyecto. El administrador de recursos ahora ha adquirido un recurso para ejecutar el rol de jefe de proyectos senior.

1. En la página **Lista de recursos**, seleccione **Daniel Goldschmidt**.
2. En la página **Rol del recurso**, seleccione **Nuevo**, e indique los valores siguientes:

    - **Vigencia a partir de**: indique la fecha actual.
    - **Vencimiento**: especificar **Nunca**.
    - **Rol**: especifique **Jefe de proyectos sénior**.

3. Seleccione **Guardar** y cierre la página.
4. En la pestaña **Competencias**, agregue la aptitud **ProjectMgmt** y el certificado **PMP**.

## <a name="set-up-role-based-pricing"></a>Configurar los precios basados en roles
Todos los costes, ventas y precios de transferencia se pueden configurar para roles.

1. En la página **Precio de venta (hora)**, seleccione **Nuevo** e indique una fecha de entrada en vigor.
2. En la columna **Rol**, seleccione un rol.
3. En la columna **Precios**, especifique un precio para el rol del recurso seleccionado.

## <a name="form-a-project-team"></a>Formar un equipo de proyecto
Para utilizar los roles que se configuraron previamente en un proyecto, un jefe de proyecto debe asociar los roles con el proyecto. Se pueden asignar varios roles a un proyecto. Para evitar confusiones, estos roles se etiquetan automáticamente durante la reserva. Por ejemplo, si el jefe de proyecto requiere tres ingenieros de software, se generan automáticamente tres roles de ingeniero de software que tengan **ingeniero de software 1**, **ingeniero de software 2** e **ingeniero de software 3** como sus etiquetas. Si las características del rol se establecieron previamente para el rol, se aplican como filtro durante las búsquedas de un recurso. Se pueden agregar características adicionales según sea necesario para refinar aún más la búsqueda.

La configuración de visualización también se puede personalizar para ofrecer una mejor visión de la disponibilidad de recursos. Hay opciones para mostrar la disponibilidad horaria, diaria, semanal, mensual, trimestral y anual. También hay una opción para mostrar la capacidad disponible y restante en los recursos. Esta opción es útil para la administración del tiempo, cuando tiene previsto tener tiempo disponible para actividades o disponibilidad de recursos.

El jefe de proyecto puede seleccionar un rol en la página y luego, si hay un recurso disponible que se ajuste al requisito, seleccionar reservar un recurso para llenar el rol. Tenga en cuenta que no es necesario reservar los recursos en este punto de la etapa de planificación. Cuando crea una WBS, puede reemplazar roles con recursos de personal para el proyecto. Si los roles se reemplazan con recursos de personal en la WBS, la configuración de recursos actualiza automáticamente la lista y la programación del equipo del proyecto.

[![Listado del equipo del proyecto que incluye tanto roles como recursos reales](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

El jefe de proyecto tiene varias opciones para reservar un recurso para un proyecto, como **Capacidad restante**, **Capacidad completa**, **Porcentaje de capacidad** y **Especificar horas**. Estas opciones de reserva se pueden cancelar en cualquier momento si cambian las asignaciones de recursos. Se admiten dos tipos de reserva:

- **Reserva manual**: la reserva de recursos fue aprobada y confirmada para trabajar en la interacción por la duración especificada.
- **Reserva automática**: las reservas de recursos se configuró provisionalmente para trabajar en la interacción por la duración especificada.

El proceso siguiente explica cómo crear un equipo de proyecto.

### <a name="create-a-project-team"></a>Crear un equipo de proyecto

1. En la página de lista **Todos los proyectos**, seleccione un proyecto y luego seleccione **Editar**.
2. En la pestaña **Equipo de proyecto y programación**, en el campo **Programar fecha de finalización**, especifique la fecha de inicio del programa más un mes. Por ejemplo, si la fecha de inicio del programa es el 24 de junio de 2017 (24/06/2017), especifique **24/07/2017**.
3. Seleccione **Agregar**.
4. En el panel **Agregar roles al proyecto**, en el campo **Rol**, seleccione **Jefe de proyectos sénior**.
5. Seleccione **Competencias requeridas**.
6. En la página **Elegir características**, las características que estableció previamente para el rol de jefe de proyecto sénior están seleccionadas de manera predeterminada. Seleccione **Aceptar**.
7. En la página **Agregar roles al proyecto**, en el campo **Cantidad de recursos**, especifique **1**.
8. En el campo **Recurso**, la búsqueda muestra todos los recursos que tienen las competencias requeridas. Seleccione **Daniel Goldschmidt** y, a continuación seleccione **Crear**.
9. En la página **Proyecto**, seleccione **Agregar**.
10. En el panel **Agregar roles al proyecto**, en el campo **Rol**, seleccione **Miembro del equipo**. En el campo **Número de recursos**, indique **5**.
11. Seleccione **Crear**.
12. En la página **Proyectos**, seleccione **Ejecutar recurso**.

## <a name="resource-capacity-synchronization"></a>Sincronización de la capacidad de los recursos
Los procesos para la sincronización de recursos ayudan a garantizar que la información para el calendario y el calendario base se incorpore a la programación de recursos del proyecto. Si se cambia el calendario, los procesos realizan las actualizaciones necesarias en la programación de los recursos del proyecto. Los procesos también ayudan a mejorar el rendimiento, porque la información de recursos del calendario se sincroniza de antemano. Por lo tanto, las actualizaciones de la información de programación de recursos se producen más rápidamente. Le recomendamos que programe los procesos por lotes en lugar de uno a la vez. De lo contrario, existe el riesgo de que alguien olvide las fechas inclusivas cuando se sincronizó la información por última vez. Si no se utilizan fechas inclusivas, pueden producirse vacíos durante la sincronización de fechas.

![Sincronización de calendario](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizar acumulaciones de capacidad de los recursos

El proceso de sincronización está diseñado para sincronizar toda la información del calendario de recursos. Esta información incluye información del calendario base sobre cualquier cambio en la tabla de capacidad del calendario de recursos del proyecto. Si se agregan nuevos recursos al proyecto, la sincronización ayuda a garantizar que la información actualizada del calendario esté disponible. Esta sincronización se puede realizar en cualquier momento.

Se recomienda usar un lote. Las opciones están disponibles durante la sincronización de las reservas de capacidad.

1. Seleccione **Gestión de proyectos y contabilidad** &gt; **Periódico** &gt; **Sincronización de capacidad** &gt; **Sincronizar acumulaciones de capacidad de recursos**.
2. Configure las opciones en la tabla siguiente.

    | Opción      | Descripción |
    |-------------|-------------|
    | Código de período | Opcionalmente, seleccione el código de intervalo de fechas del Libro de contabilidad para establecer las fechas de inicio y finalización del proceso de sincronización para acumulaciones de capacidad de recursos. |
    | Fecha de inicio  | Especifique la fecha de inicio del proceso de sincronización para las acumulaciones de capacidad de recursos. |
    | Fecha de finalización    | Especifique la fecha de finalización para el proceso de sincronización para las acumulaciones de capacidad de recursos. |

[![Procreso de sincronización](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Configurar roles en plantillas WBS
Los jefes de proyecto pueden configurar plantillas de WBS que pueden aplicar cuando crean una WBS para nuevos proyectos. Los jefes de proyecto pueden agregar roles cuando crean una plantilla. Utilice el siguiente procedimiento para asignar un rol a una plantilla WBS.

1. Seleccione **Gestión de proyectos y contabilidad** &gt; **Configuración** &gt; **Proyectos** &gt; **Plantillas de estructura de descomposición del trabajo**.
2. Seleccione **Detalles** para una plantilla WBS seleccionada.
3. Seleccione una tarea en la lista y luego, en el campo **Rol**, seleccione un rol para asignar a la tarea.

### <a name="work-with-a-wbs"></a>Trabajar con una WBS

Puede crear una nueva WBS o puede copiar una WBS de una plantilla de WBS existente. Un jefe de proyecto puede administrar fácilmente los recursos asignando roles a nuevas tareas en la WBS. Los roles se pueden reemplazar después de adquirir un recurso o después de identificar un recurso confirmado para trabajar en la tarea. Esta flexibilidad permite a los jefes de proyecto realizar las siguientes tareas:

- Identificar la cantidad de recursos que se requieren para los paquetes de trabajo de WBS.
- Calcular los costes del proyecto.
- Determinar un presupuesto preliminar.
- Estimar la duración de la actividad, según los roles y los recursos.
- Desarrollar algunos planes de gestión de proyectos, basados en la información disponible del proyecto.

Se han agregado opciones adicionales en la WBS para utilizar mejor la funcionalidad de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Asignaciones de recursos</td>
<td>Consulte los recursos asignados, las fechas, la cantidad de horas y el tipo de reserva para las tareas en la WBS.</td>
</tr>
<tr class="even">
<td>Equipo de generación automática</td>
<td>Agregue automáticamente recursos planificados utilizando roles asociados con una tarea. Finance sugiere automáticamente los recursos planificados mediante el uso de análisis de decisiones de criterios múltiples que se basan en roles. Una vez que se hayan establecido los roles y el esfuerzo (horas) para las tareas en una WBS, y después de que se haya liberado la estructura, seleccione <strong>Equipo de generación automática</strong>. La cantidad requerida de recursos planificados se agrega a la WBS y la pestaña <strong>Programación de proyectos y equipos</strong>.</td>
</tr>
<tr class="odd">
<td>Recurso (lista desplegable)</td>
<td>En la página <strong>Lanzar asignación de recursos</strong>, puede seleccionar recursos para la reserva manual o automática, según la duración especificada. Puede ajustar la configuración de la vista para ver y establecer la duración de las actividades de los recursos. Puede seleccionar y asignar recursos a nivel de paquete de trabajo mediante las siguientes opciones:
<ul>
<li><strong>Aceptar</strong> : confirmar cambios en el recurso asignado a una tarea.</li>
<li><strong>Cancelar</strong> : cancelar cambios en el recurso asignado a una tarea.</li>
<li><strong>Asignar automáticamente</strong>: un recurso de personal disponible que tiene un rol coincidente se selecciona y asigna automáticamente a la tarea seleccionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. En la página **Todos los proyectos**, seleccione el proyecto **Fase 2 de la actualización XYZ**.
2. Seleccione **Plan** &gt; **Actividades** &gt; **Estructura de desglose del trabajo**.
3. Seleccione **Nuevo** para agregar las siguientes actividades de nivel uno a la WBS:

    - Iniciación
    - Planificación
    - Ejecutando
    - Supervisión y control
    - Cerrada

4. Configure las fechas y el esfuerzo (horas), como se muestra en la siguiente ilustración.

    [![Configuración de las fechas y el esfuerzo](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Seleccione la línea de tarea **Iniciando** y, luego, en el campo **Rol**, seleccione **Jefe de proyectos sénior**.
6. Seleccione **Publish**.
7. En la misma línea, en el campo **Recurso**, seleccione **Daniel Goldschmidt** y luego seleccione **Aceptar**.
8. Seleccione la línea de tarea **Planificación** y luego, en el campo **Rol**, seleccione **Analista de negocios**.
9. Seleccione **Publicar** y luego seleccione **Equipo de generación automática**.
10. En el cuadro mensaje que aparece, seleccione **Sí**.
11. En el campo **Recurso**, verifique que el valor sea **Analista de negocios 1**.
12. Para el recurso **Analista de negocios 1**, abra la búsqueda y seleccione **Lanzar asignaciones de recursos**. Luego seleccione un trabajador para la tarea.
13. Seleccione **Asignación automática** &gt; **Capacidad completa**.

    > [!NOTE] 
    > No recibe una advertencia de que el recurso especificado ahora es 2, porque la cantidad de recursos sigue siendo 1.

14. En la página **Estructura de descomposición del trabajo**, valide la asignación de recursos en la WBS y luego seleccione **Guardar**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ejecución de recursos para recursos planificados
Un jefe de proyecto puede planificar los roles de recursos necesarios para un proyecto. El administrador de recursos verá estos recursos planificados como solicitudes en la página **Ejecución de recursos** y puede asignar recursos reales.

1. En la página **Todos los proyectos**, seleccione el proyecto **Fase 2 de la actualización XYZ**.
2. Seleccione **Proyecto** y, a continuación, seleccione **Editar**.
3. En la pestaña **Equipo de proyecto y programación**, seleccione **Agregar**.
4. En el cuadro de diálogo **Agregar roles**, seleccione el rol **Desarrollador de software**.
5. Seleccione **Crear** y cierre la página del proyecto.
6. En la página **Ejecución de recursos**, seleccione **Desarrollador de software 1** para el proyecto **Fase 2 de la actualización**.
7. Seleccione un trabajador y, después, **Asignar**.
8. Verifique que la línea para **Desarrollador de software 1** ha sido eliminada para el proyecto **Fase 2 del proyecto de la actualización XYZ**.
9. En la pestaña **Equipo de proyecto y programación**, para el proyecto **Fase 2 de la actualización XYZ**, compruebe que el trabajador que seleccionó en el paso anterior se haya agregado como **Desarrollador de software**.

## <a name="requests-for-project-resources"></a>Solicitudes de recursos del proyecto
La funcionalidad para la programación de recursos del proyecto solo permite a los administradores de recursos distribuir los recursos del personal en compromisos o proyectos. Para habilitar esta funcionalidad, complete las siguientes tareas o verifique que se hayan completado:

- Configurar las secuencias numéricas.
- Configurar los flujos de trabajo de gestión de proyectos y contabilidad.
- Habilite los flujos de trabajo de solicitud de recursos.

Una vez completadas las tareas anteriores, puede completar las siguientes tareas según sea necesario:

- Cree una solicitud de recurso a partir de un recurso con personal reservado temporalmente.
- Supervise solicitudes de recursos.
- Ejecute solicitudes de recursos.
- Solicite un recurso con personal de una WBS.
- Reserve recursos para un proyecto sin tener una solicitud de recursos con personal.

## <a name="monitor-project-teams"></a>Supervisar equipos de proyectos
1. En la página **Todos los proyectos**, seleccione vínculo **Id. de proyecto** para el proyecto **Fase 2 de la actualización XYZ**.
2. En la ficha desplegable **Equipo de proyecto y programación**, verifique que los recursos del proyecto que se enumeran sean correctos.
