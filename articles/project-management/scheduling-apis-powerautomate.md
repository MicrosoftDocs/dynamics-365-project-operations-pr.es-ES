---
title: Usar las API de programación de proyectos con Power Automate
description: Este tema proporciona un flujo de muestra que utiliza las interfaces de programación de aplicaciones (API) de la programación del proyecto.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597727"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Usar las API de programación de proyectos con Power Automate

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Este tema describe un flujo de ejemplo que muestra cómo crear un plan de proyecto completo usando Microsoft Power Automate, cómo crear un conjunto de operaciones y cómo actualizar una entidad. El ejemplo demuestra cómo crear un proyecto, un miembro del equipo del proyecto, conjuntos de operaciones, tareas del proyecto y asignaciones de recursos. Este tema también explica cómo actualizar una entidad y ejecutar un conjunto de operaciones.

La siguiente es una lista completa de los pasos que están documentados en el flujo de muestra en este tema:

1. [Crear un desencadenador de PowerApps](#1)
2. [Crear un proyecto](#2)
3. [Inicializar una variable para el miembro del equipo](#3)
4. [Crear un miembro del equipo genérico](#4)
5. [Crear un conjunto de opciones](#5)
6. [Crear un cubo de proyecto](#6)
7. [Inicializar una variable para el estado del vínculo](#7)
8. [Inicializar una variable para el número de tareas](#8)
9. [Inicializar una variable para el id. de tarea de proyecto](#9)
10. [Hacer hasta](#10)
11. [Establecer una tarea de proyecto](#11)
12. [Crear una tarea de proyecto](#12)
13. [Crear una asignación de recurso](#13)
14. [Decrementar una variable](#14)
15. [Renombrar una tarea de proyecto](#15)
16. [Ejecutar un conjunto de opciones](#16)

## <a name="assumptions"></a>Supuestos

Este tema asume que tiene un conocimiento básico de la plataforma de Dataverse, flujos en la nube y la interfaz de programación de aplicaciones (API) de la programación del proyecto. Para obtener más información, consulte la sección [Referencias](#references) más adelante en este tema.

## <a name="create-a-flow"></a>Creación de un flujo

### <a name="select-an-environment"></a>Seleccionar un entorno

Puede crear el flujo de Power Automate en su entorno.

1. Vaya a <https://flow.microsoft.com> e inicie sesión con sus credenciales de administrador.
2. En la esquina superior derecha, seleccione **Entornos** .
3. En la lista, seleccione el entorno donde esté instalado Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Crear una solución

Siga estos pasos para crear un [flujo compatible con la solución](/power-automate/overview-solution-flows). Al crear un flujo compatible con la solución, puede exportar más fácilmente el flujo para usarlo más tarde.

1. En el panel de navegación, seleccione **Soluciones**.
2. En la página **Soluciones**, seleccione **Nueva solución**.
3. En el cuadro de diálogo **nueva solución**, establezca los campos requeridos y, a continuación, seleccione **Crear**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Paso 1: crear un desencadenador de PowerApps

1. En la página **Soluciones**, seleccione la solución que creó y, a continuación **Nuevo**.
2. En el panel izquierdo, seleccione **Flujos de nube** \> **Automatización** \> **Flujo de nube** \> **Instantáneo**.
3. En el campo **Nombre de flujo**, introduzca **Programar flujo de demostración de API**.
4. En la lista **Elegir cómo desencadenar este flujo**, seleccione **Power Apps**. Cuando cree un desencadenador de Power Apps, la lógica depende de usted como autor. En este tema, deje los parámetros de entrada en blanco con fines de prueba.
5. Seleccione **Crear**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Paso 2: crear un proyecto

Siga estos pasos para crear una estimación de proyecto.

1. En el flujo que creó, seleccione **Nuevo paso**.

    ![Adición de un nuevo paso.](media/newstep.png)

2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Realizar una acción no enlazada**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.

    ![Selección de una operación.](media/chooseactiontab.png)

3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.

![Cambio de nombre de un paso.](media/renamestep.png)

4. Cambie el nombre del paso **Crear proyecto**.
5. En el campo **Nombre de acción**, seleccione **msdyn\_CreateProjectV1**.
6. En el campo **msdyn\_subject**, seleccione **Agregar contenido dinámico**.
7. En la pestaña **Expresión**, en el campo de función, introduzca **Nombre del proyecto - utcNow()**.
8. Seleccione **Aceptar**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Paso 3: inicializar una variable para el miembro del equipo

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Inicializar variable**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Inicializar miembro del equipo**.
5. En el campo **Nombre**, escriba **TeamMemberAction**.
6. En el campo **Tipo**, seleccione **Cadena**.
7. En el campo **Valor**, introduzca **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Paso 4: crear un miembro del equipo genérico

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Realizar una acción no enlazada**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Crear miembro del equipo**.
5. Para el campo **Nombre de la acción**, seleccione **TeamMemberAction** en el cuadro de diálogo **Contenido dinámico** .
6. En el campo **Parámetros de acción**, introduzca la siguiente información del parámetro.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    A continuación se ofrece una explicación de los parámetros:

    - **\@\@odata.type**: nombre de entidad. Por ejemplo, introduzca **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid**: la clave principal del id. del equipo del proyecto. El valor es una expresión de identificador único global (GUID).   El id. se genera desde la pestaña de expresión.

    - **msdyn\_project\@odata.bind**: id. de proyecto del proyecto propietario. El valor será contenido dinámico que provenga de la respuesta del paso "Crear proyecto". Asegúrese de introducir la ruta completa y agregue contenido dinámico entre paréntesis. Se requieren comillas. Por ejemplo, introduzca **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name**: nombre para mostrar del miembro del equipo. Por ejemplo, escriba **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Paso 5: crear un conjunto de opciones

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Realizar una acción no enlazada**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Crear conjunto de operaciones**.
5. En el campo **Nombre de la acción**, seleccione la acción personalizada **msdyn\_CreateOperationSetV1** Dataverse.
6. En el campo **Descripción**, introduzca **ScheduleAPIDemoOperationSet**".
7. En el campo **Proyecto**, introduzca **/msdyn\_projects(**.
8. En el cuadro de diálogo **Contenido dinámico**, seleccione **msdyn\_CreateProjectV1Response ProjectId**.
9. En el campo **Proyecto**, introduzca **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Paso 6: crear un cubo de proyecto

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Agregar nueva fila**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Crear cubo**.
5. En el campo **Nombre de tabla**, seleccione **Cubos de proyecto**.
6. En el campo **Nombre**, escriba **ScheduleAPIDemoBucket1**.
7. En el campo **Proyecto**, seleccione **msdyn\_CreateProjectV1Response ProjectId** en el cuadro de diálogo **Contenido dinámico**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Paso 7: inicializar una variable para el estado del vínculo

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Inicializar variable**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Init linkstatus**.
5. En el campo **Nombre**, escriba **linkstatus**.
6. En el campo **Tipo**, seleccione **Entero**.
7. En el campo **Valor**, introduzca **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Paso 8: inicializar una variable para el número de tareas

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Inicializar variable**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Inicializar número de tareas**.
5. En el campo **Nombre**, escriba **Número de tareas**.
6. En el campo **Tipo**, seleccione **Entero**.
7. En el campo **Valor**, introduzca **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Paso 9: inicializar una variable para el id. de tarea de proyecto

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Inicializar variable**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Init ProjectTaskID**.
5. En el campo **Nombre**, escriba **Número de tareas**.
6. En el campo **Tipo**, seleccione **Cadena**.
7. Para el campo **Valor**, introduzca **guid()** en el generador de expresiones.

## <a name="step-10-do-until"></a><a id="10"></a>Paso 10: hacer hasta

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Hacer hasta**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. Establezca el primer valor de la declaración condicional en la variable **Número de tareas** del cuadro de diálogo **Contenido dinámico**.
4. Establezca la condición de **menor o igual que**.
5. Establezca el segundo valor de la declaración condicional en **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Paso 11: establecer una tarea de proyecto

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Establecer variable**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el nuevo paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Establecer tarea de proyecto**.
5. En el campo **Nombre**, seleccione **msdyn\_projecttaskid**.
6. Para el campo **Valor**, introduzca **guid()** en el generador de expresiones.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Paso 12: crear una tarea de proyecto

Siga estos pasos para crear una tarea de proyecto que tenga un id. único que pertenezca al proyecto actual y al cubo de proyectos que creó.

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Realizar una acción no enlazada**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Crear tarea de proyecto**.
5. En el campo **Nombre de acción**, seleccione **msdyn\_PssCreateV1**.
6. En el campo **Entidad**, introduzca la siguiente información del parámetro.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    A continuación se ofrece una explicación de los parámetros:

    - **\@\@odata.type**: nombre de entidad. Por ejemplo, introduzca **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid**: el id. único de la tarea. El valor debe establecerse en una variable dinámica de **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind**: id. de proyecto del proyecto propietario. El valor será contenido dinámico que provenga de la respuesta del paso "Crear proyecto". Asegúrese de introducir la ruta completa y agregue contenido dinámico entre paréntesis. Se requieren comillas. Por ejemplo, introduzca **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject**: cualquier nombre de tarea.
    - **msdyn\_projectbucket\@odata.bind**: el cubo del proyecto que contiene las tareas. El valor será contenido dinámico que provenga de la respuesta del paso "Crear cubo". Asegúrese de introducir la ruta completa y agregue contenido dinámico entre paréntesis. Se requieren comillas. Por ejemplo, introduzca **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start**: contenido dinámico para la fecha de inicio. Por ejemplo, mañana se representará como **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart**: la fecha inicial programada. Por ejemplo, mañana se representará como **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend**: la fecha de finalización programada. Seleccione una fecha futura. Por ejemplo, especifique **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus**: el estado del vínculo. Por ejemplo, escriba **"192350000"**.

7. En el campo **OperationSetId**, seleccione **msdyn\_CreateOperationSetV1Response** en el cuadro de diálogo **Contenido dinámico**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Paso 13: crear una asignación de recursos

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Realizar una acción no enlazada**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Crear asignación**.
5. En el campo **Nombre de acción**, seleccione **msdyn\_PssCreateV1**.
6. En el campo **Entidad**, introduzca la siguiente información del parámetro.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. En el campo **OperationSetId**, seleccione **msdyn\_CreateOperationSetV1Response** en el cuadro de diálogo **Contenido dinámico**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Paso 14: decrementar una variable

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Decrementar variable**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el campo **Nombre**, seleccione **Número de tareas**.
4. En el campo **Valor**, introduzca **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Paso 15: cambiar el nombre de una tarea de proyecto

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Realizar una acción no enlazada**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Renombrar tarea de proyecto**.
5. En el campo **Nombre de acción**, seleccione **msdyn\_PssUpdateV1**.
6. En el campo **Entidad**, introduzca la siguiente información del parámetro.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. En el campo **OperationSetId**, seleccione **msdyn\_CreateOperationSetV1Response** en el cuadro de diálogo **Contenido dinámico**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Paso 16: ejecutar un conjunto de opciones

1. En el flujo, seleccione **Nuevo paso**.
2. En el cuadro de diálogo **Elegir una operación**, en el campo de búsqueda, introduzca **Realizar una acción no enlazada**. Entonces, en la pestaña **Acciones**, seleccione la operación en la lista de resultados.
3. En el paso, selecciones los puntos suspensivos (**...**) y luego elija **Renombrar**.
4. Cambie el nombre del paso **Ejecutar conjunto de operaciones**.
5. En el campo **Nombre de acción**, seleccione **msdyn\_ExecuteOperationSetV1**.
6. En el campo **OperationSetId**, seleccione **msdyn\_CreateOperationSetV1Response OperationSetId** en el cuadro de diálogo **Contenido dinámico**.

## <a name="references"></a>Referencias

- [Descripción general de cómo integrar flujos con Dataverse y Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Usar las API de programación de proyectos para realizar operaciones con entidades de programación](schedule-api-preview.md)
- [Descripción general de los flujos en la nube: Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Información general de flujos que reconocen soluciones: Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
