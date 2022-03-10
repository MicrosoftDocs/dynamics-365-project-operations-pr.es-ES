---
title: Use el complemento Project Service Add-in para planear el trabajo en Microsoft Project | MicrosoftDocs
description: En este tema se proporciona información sobre cómo agregar, configurar y usar el complemento de Microsoft Project para Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: ccebf1439f49092b23da5b4fc2ebb4fc484de4dd17c870eea9fe37b00fbb3689
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005322"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Use el complemento Project Service Automation para planear el trabajo en Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] hace que le resulte más fácil realizar planeamiento del proyecto, incluidas estimaciones. Puede definir el trabajo de modo que costos, esfuerzo y valor de ventas sean claros cuando se envíe la propuesta final.  

 Ahora puede instalar [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] y realizar su plan de trabajo en el entorno familiar de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Use las capacidades eficaces de planificación y administración de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y después actualice el plan del proyecto en Project Service Automation.  

> [!IMPORTANT]
> - Para usar la administración de documentos de SharePoint para almacenar los archivos de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para proyectos de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], el administrador de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] necesitará activar la administración de documentos. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] solo es compatible con [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Descargue e instale el complemento  
 Tenga lista la información de inicio de sesión de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Necesitará esta información para conectar desde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Desde el Centro de descarga, descargue el complemento para su versión compatible de Project Service, bien la versión [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) o la versión [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Haga clic en el vínculo de descarga.  

3.  Cuando la descarga esté completa, haga clic en **Sí** para instalar el complemento.  

## <a name="configure-the-add-in"></a>Configure el complemento  

1. Abra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y haga clic en la pestaña **Project Service**.  

2. Haga clic en **Conectar**.  

3. Escriba la información de inicio de sesión y después haga clic en **Iniciar sesión**.  

   Ahora puede empezar a utilizar el complemento.  

## <a name="read-from-a-template"></a>Leer desde una plantilla  
 Lea desde una plantilla que haya creado en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] y copiado en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para comenzar su planificación de proyectos. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crear una plantilla de proyecto (Project Service Automation)](../psa/create-project-template.md)  

1.  En la pestaña **Project Service**, haga clic en **Leer** > **Plantilla de proyecto de Project Service Automation**.  

2.  Elija una plantilla de proyecto de la lista y después haga clic en **Abrir**.  

    > [!NOTE]
    >  De forma predeterminada, las tareas que se copian desde la plantilla en Project se establecen como programadas manualmente.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Asignar roles de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a recursos de proyecto  

1.  Abra un proyecto y haga clic en la cinta de opciones **Tarea**.  

2.  Haga clic en el menú **Diagrama de Gantt** y después elija **Hoja de recursos**.  

3.  En la Hoja de recursos, haga clic en el menú desplegable **Rol de recurso de Project Service** y seleccione un rol de Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Provea de personal al proyecto con recursos  

1.  En la pestaña Project Service, seleccione una fila y haga clic en **Buscar recursos**.  

2.  En la pantalla **Reservar recurso**, seleccione el recurso que desee usar para el proyecto.  

3.  Haga clic en **Reservar** y, a continuación, en **Aceptar**.  

## <a name="publish-your-project"></a>Publicar el proyecto  
Cuando se completa el planeamiento de proyecto, el siguiente paso es importar y publicar el proyecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

El proyecto se importará en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Se aplica el proceso de generación de precios y equipos. Abra el proyecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para ver que se han generado el equipo, estimaciones de proyecto y estructura de descomposición del trabajo. La siguiente tabla muestra dónde encontrar los resultados:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gráfico de Gantt**   | Importaciones en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] la pantalla **Estructura de descomposición del trabajo** . |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Hoja de recursos** |   Importaciones en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] la pantalla **Integrantes del grupo del proyecto** .   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Uso**    |    Importaciones en la pantalla **Estimaciones del proyecto** de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].     |

**Para importar y publicar el proyecto**  
1. En la pestaña **Project Service**, haga clic en **Publicar** > **Nuevo proyecto de Project Service Automation**.  

2. En el cuadro de diálogo **Publicar en un nuevo proyecto en Project Service**, escriba el **Nombre del proyecto** y seleccione **Cliente**.  

3. Active opcionalmente **Vincular el plan del proyecto a Project Service Automation** para vincular el archivo de Project con Project Service Automation.  

4. Haga clic en **Publicar**.  

   Vinculando el archivo de proyecto con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] convierte al archivo de Project en el maestro y define la estructura de descomposición del trabajo en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como de solo lectura.  Para realizar cambios en el plan del proyecto, debe realizarlos en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y publicarlos como actualizaciones en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editar un proyecto que se ha importado  
 Para realizar cambios en un plan de proyecto que se ha importado en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], tiene dos opciones:  

- Abra el archivo maestro y edítelo en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Desvincule el archivo y edítelo directamente en Project Service. De forma predeterminada, un proyecto que se ha cargado desde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se bloquea y solo se puede editar en Project. Para editar el archivo en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], el archivo tiene que desvincularse.  

### <a name="edit-in-pn_microsoft_project"></a>Edición en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. En el menú principal, haga clic en **Project Service** > **Proyectos**.  

2. En la lista de proyectos, abra el que creó en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Haga clic en **Abrir en MS Project** de la cinta de opciones. Esto abrirá el archivo maestro vinculado en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Desvincule un archivo y edítelo en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service.  

1. En el menú principal, haga clic en **Project Service** > **Proyectos**.  

2. En la lista de proyectos, abra el que creó en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Haga clic en **Desvincular de MS Project** de la cinta de opciones.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Cargar un archivo de Project en SharePoint o en Grupos de Office  
 Puede cargar el archivo de Project en SharePoint y encontrarlo en los documentos asociados de su proyecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Deberá pedirle a su administrador que configure la administración de documentos de SharePoint y que la active para la entidad de Project. 

 También puede cargar el archivo de Project a [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] si tiene grupos de Office configurados.

### <a name="upload-a-file-for-sharepoint"></a>Cargar un archivo para SharePoint  

1. En el menú principal, haga clic en **Project Service** > **Cargar**.  

2. Seleccione **A documentos de proyecto de Project Service Automation**.  

3. En el diálogo **Habilitar Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccione **Sí** o **No**.  

   - Si hace clic en **Sí**, podrá seleccionar el botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** en Project Service Automation, iniciar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y cargar el archivo de Project desde la biblioteca de documentos de SharePoint.  

   - Si hace clic en **No**, el vínculo para abrir en el botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionará.  

4. El archivo [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se puede encontrar en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en **Documentos** para el proyecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.  

### <a name="upload-a-file-for-office-groups"></a>Cargar un archivo para grupos de Office  

1. En el menú principal, haga clic en **Project Service** > **Cargar**.  

2. Seleccione **A documentos de proyecto de Project Service Automation**.  

3. En el diálogo **Habilitar Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccione **Sí** o **No**.  

   - Si hace clic en **Sí**, podrá seleccionar el botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** en Project Service Automation, iniciar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y cargar el archivo de Project desde la biblioteca de documentos de SharePoint.  

   - Si hace clic en **No**, el vínculo para abrir en el botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionará.  

4. El archivo [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se puede encontrar en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en **Documentos** para el proyecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.  

## <a name="publish--your-project-as-a-template"></a>Publicar el proyecto como plantilla  
 Puede guardar el proyecto y reusarlo guardándolo como plantilla de proyecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Las plantillas de proyecto son planes de proyecto reutilizables en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crear una plantilla de proyecto (Project Service Automation)](../psa/create-project-template.md)  

1. En la pestaña **Project Service**, haga clic en **Publicar** > **Nueva plantilla de proyecto de Project Service Automation**.  

2. En la plantilla **Publicar un nuevo proyecto en Project Service**, escriba el **Nombre de plantilla de proyecto**.  

3. Active opcionalmente **Vincular el plan del proyecto a Project Service Automation** para vincular el archivo de Project con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Haga clic en **Publicar**.  

Vinculando el archivo de proyecto con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] convierte al archivo de Project en el maestro y define la estructura de descomposición del trabajo en la plantilla de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como de solo lectura.  Para realizar cambios en el plan del proyecto, debe realizarlos en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y publicarlos como actualizaciones en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Leer una programación cargada de recursos

Al leer un proyecto de Project Service Automation, el calendario del recurso no está sincronizado con el cliente de escritorio. Si hay diferencias en las duraciones, el esfuerzo o el final de las tareas, probablemente se deba a que los recursos y el cliente de escritorio no tengan el mismo calendario de plantilla de horas de trabajo aplicado al proyecto.


## <a name="data-synchronization"></a>Sincronización de datos

En la siguiente tabla se describe cómo se sincronizan los datos entre Project Service Automation y el complemento de escritorio de Microsoft Project.

| **Entidad** | **Campo** | **Microsoft Project a Project Service Automation** | **Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Tarea de proyecto | Fecha de vencimiento | ● | - |
| Tarea de proyecto | Esfuerzo estimado | ● | - |
| Tarea de proyecto | Id. de cliente de MS Project | ● | - |
| Tarea de proyecto | Tarea principal | ● | - |
| Tarea de proyecto | Project | ● | - |
| Tarea de proyecto | Tarea de proyecto | ● | - |
| Tarea de proyecto | Nombre de tarea de proyecto | ● | - |
| Tarea de proyecto | Unidad de dotación de recursos (obsoleto en la versión 3.0) | ● | - |
| Tarea de proyecto | Duración programada | ● | - |
| Tarea de proyecto | Fecha de inicio | ● | - |
| Tarea de proyecto | Id. de WBS | ● | - |

| **Entidad** | **Campo** | **Microsoft Project a Project Service Automation** | **Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Miembro del equipo | Id. de cliente de MS Project | ● | - |
| Miembro del equipo | Nombre de puesto | ● | - |
| Miembro del equipo | proyecto | ● | ● |
| Miembro del equipo | Equipo del proyecto | ● | ● |
| Miembro del equipo | Unidad de dotación de recursos | - | ● |
| Miembro del equipo | Rol | - | ● |
| Miembro del equipo | Horas laborables | No sincronizado | No sincronizado |

| **Entidad** | **Campo** | **Microsoft Project a Project Service Automation** | **Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Asignación de recursos | Desde la fecha | ● | - |
| Asignación de recursos | Horas | ● | - |
| Asignación de recursos | Id. de cliente de MS Project | ● | - |
| Asignación de recursos | Trabajo previsto | ● | - |
| Asignación de recursos | Project | ● | - |
| Asignación de recursos | Equipo del proyecto | ● | - |
| Asignación de recursos | Asignación de recursos | ● | - |
| Asignación de recursos | Tarea | ● | - |
| Asignación de recursos | Hasta la fecha | ● | - |

| **Entidad** | **Campo** | **Microsoft Project a Project Service Automation** | **Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Dependencias de tareas de proyecto | Dependencia de tareas de proyecto | ● | - |
| Dependencias de tareas de proyecto | Tipo de vínculo | ● | - |
| Dependencias de tareas de proyecto | Tarea predecesora | ● | - |
| Dependencias de tareas de proyecto | Project | ● | - |
| Dependencias de tareas de proyecto | Tarea sucesora | ● | - |

### <a name="see-also"></a>Vea también  
 [Guía del jefe de proyecto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]