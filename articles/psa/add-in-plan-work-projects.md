---
title: Planificar su trabajo en Microsoft Project con el complemento Project Service
description: En este tema se proporciona información sobre cómo usar el complemento de Microsoft Project para Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145964"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planificar su trabajo en Microsoft Project con el complemento Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] hace que le resulte más fácil realizar planeamiento del proyecto, incluidas estimaciones. Puede definir el trabajo de modo que costos, esfuerzo y valor de ventas sean claros cuando se envíe la propuesta final.  

Puede instalar [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] y realizar su trabajo de planificación en el entorno conocido de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Use las capacidades eficaces de planificación y administración de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y después actualice el plan del proyecto en Project Service Automation.  

> [!IMPORTANT]
> - Para usar la administración de documentos de SharePoint para almacenar los archivos de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para proyectos de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], el administrador de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] necesitará activar la administración de documentos. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] solo es compatible con [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Descargue e instale el complemento  
 Tenga lista la información de inicio de sesión de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Necesitará esta información para conectar desde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Desde el Centro de descarga, descargue el complemento para su versión compatible de Project Service, bien la versión [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) o la versión [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Seleccione el vínculo de descarga.  

3.  Cuando se haya completado la descarga, seleccione **Sí** para instalar el complemento.  

## <a name="configure-the-add-in"></a>Configure el complemento  

1. Abra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y seleccione la pestaña **Project Service**.  

2. Seleccione **Conectar**.  

3. Introduzca la información de inicio de sesión y seleccione **Iniciar sesión**.  

   Ahora puede empezar a utilizar el complemento.  

## <a name="read-from-a-template"></a>Leer desde una plantilla  
 Lea desde una plantilla que haya creado en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] y copiado en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para comenzar su planificación de proyectos. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crear una plantilla de proyecto (Project Service Automation)](../psa/create-project-template.md)  

1.  En la pestaña **Project Service**, seleccione **Leer** > **Plantilla de proyecto de Project Service Automation**.  

2.  Elija una plantilla de proyecto de la lista y, a continuación, seleccione **Abrir**.  

    > [!NOTE]
    >  De forma predeterminada, las tareas que se copian desde la plantilla en Project se establecen como programadas manualmente.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Asignar roles de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a recursos de proyecto  

1.  Abra un proyecto y seleccione la cinta de opciones **Tarea**.  

2. Seleccione el menú **Diagrama de Gantt** y después elija **Hoja de recursos**.  

3. En la Hoja de recursos, seleccione el menú desplegable **Rol de recurso de Project Service** y elija un rol de Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Provea de personal al proyecto con recursos  

1.  En la pestaña Project Service, seleccione una fila y seleccione **Buscar recursos**.  

2.  En la pantalla **Reservar recurso**, seleccione el recurso que desee usar para el proyecto.  

3.  Seleccione **Reservar** y, a continuación, seleccione **Aceptar**.  

## <a name="publish-your-project"></a>Publicar el proyecto  
Cuando se completa el planeamiento de proyecto, el siguiente paso es importar y publicar el proyecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

El proyecto se importará en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Se aplica el proceso de generación de precios y equipos. Abra el proyecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para ver que se han generado el equipo, estimaciones de proyecto y estructura de descomposición del trabajo. La siguiente tabla muestra dónde encontrar los resultados.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gráfico de Gantt**   | Importaciones en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] la pantalla **Estructura de descomposición del trabajo** . |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Hoja de recursos** |   Importaciones en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] la pantalla **Integrantes del grupo del proyecto** .   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Uso**    |    Importaciones en la pantalla **Estimaciones del proyecto** de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].     |

**Para importar y publicar el proyecto**  
1. En la pestaña **Project Service**, vaya a **Publicar** > **Nuevo proyecto de Project Service Automation**.  

2. En el cuadro de diálogo **Publicar en un nuevo proyecto en Project Service**, escriba el **Nombre del proyecto** y seleccione **Cliente**.  

3. Opcionalmente, seleccione **Vincular el plan del proyecto a Project Service Automation** para vincular el archivo de Project con Project Service Automation.  

4. Seleccione **Publish**.  

   Vinculando el archivo de proyecto con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] convierte al archivo de Project en el maestro y define la estructura de descomposición del trabajo en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como de solo lectura.  Para realizar cambios en el plan del proyecto, debe realizarlos en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y publicarlos como actualizaciones en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editar un proyecto que se ha importado  
 Para realizar cambios en un plan de proyecto que se ha importado en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], tiene dos opciones:  

- Abra el archivo maestro y edítelo en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Desvincule el archivo y edítelo directamente en Project Service. De forma predeterminada, un proyecto que se ha cargado desde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se bloquea y solo se puede editar en Project. Para editar el archivo en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], el archivo tiene que desvincularse.  

### <a name="edit-in-pn_microsoft_project"></a>Editar en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. En el menú principal, vaya a **Project Service** > **Proyectos**.  

2. En la lista de proyectos, abra el que creó en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Seleccione **Abrir en MS Project** de la cinta de opciones. Esto abrirá el archivo maestro vinculado en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Desvincule un archivo y edítelo en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service.  

1. En el menú principal, vaya a **Project Service** > **Proyectos**.  

2. En la lista de proyectos, abra el que creó en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Seleccione **Desvincular de MS Project** en la cinta de opciones.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Cargar un archivo de Project en SharePoint o en Grupos de Office  
 Puede cargar el archivo de Project en SharePoint y encontrarlo en los documentos asociados de su proyecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Deberá pedirle a su administrador que configure la administración de documentos de SharePoint y que la active para la entidad de Project. 

 También puede cargar el archivo de Project a [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] si tiene grupos de Office configurados.

### <a name="upload-a-file-for-sharepoint"></a>Cargar un archivo para SharePoint  

1. En el menú principal, vaya a **Project Service** > **Cargar**.  

2. Seleccione **A documentos de proyecto de Project Service Automation**.  

3. En el cuadro de diálogo **Habilitar Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccione **Sí** o **No**.  

   - Si selecciona **Sí**, podrá seleccionar el botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** en Project Service Automation, iniciar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y cargar el archivo de Project desde la biblioteca de documentos de SharePoint.  

   - Si selecciona **No**, el vínculo para **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionará.  

4. El archivo [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se puede encontrar en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en **Documentos** para el proyecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.  

### <a name="upload-a-file-for-office-groups"></a>Cargar un archivo para grupos de Office  

1. En el menú principal, vaya a **Project Service** > **Cargar**.  

2. Seleccione **A documentos de proyecto de Project Service Automation**.  

3. En el cuadro de diálogo **Habilitar Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccione **Sí** o **No**.  

   - Si selecciona **Sí**, podrá seleccionar el botón **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** en Project Service Automation, iniciar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y cargar el archivo de Project desde la biblioteca de documentos de SharePoint.  

   - Si selecciona **No**, el vínculo para **Abrir en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionará.  

4. El archivo [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se puede encontrar en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en **Documentos** para el proyecto de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.  

## <a name="publish--your-project-as-a-template"></a>Publicar el proyecto como plantilla  
 Puede guardar el proyecto y reusarlo guardándolo como plantilla de proyecto en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Las plantillas de proyecto son planes de proyecto reutilizables en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Para obtener más información, consulte [Crear una plantilla de proyecto (Project Service Automation)](../psa/create-project-template.md). 

1. En la pestaña **Project Service**, vaya a **Publicar** > **Nueva plantilla de proyecto de Project Service Automation**.  

2. En el cuadro de diálogo **Publicar en una nueva plantilla de proyecto de Project Service**, escriba el **Nombre de plantilla de proyecto**.  

3. Opcionalmente, seleccione **Vincular el plan del proyecto a Project Service Automation** para vincular el archivo de Project a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Seleccione **Publish**.  

Vinculando el archivo de proyecto con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] convierte al archivo de Project en el maestro y define la estructura de descomposición del trabajo en la plantilla de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como de solo lectura.  Para realizar cambios en el plan del proyecto, debe realizarlos en [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] y publicarlos como actualizaciones en [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Leer una programación cargada de recursos

Al leer un proyecto de Project Service Automation, el calendario del recurso no está sincronizado con el cliente de escritorio. Si hay diferencias en las duraciones, el esfuerzo o el final de las tareas, probablemente se deba a que los recursos y el cliente de escritorio no tengan el mismo calendario de plantilla de horas de trabajo aplicado al proyecto.


## <a name="data-synchronization"></a>Sincronización de datos
Las tablas de esta sección proporcionan información sobre la sincronización de datos de entidad entre Project Service Automation y el complemento de escritorio de Microsoft Project.

### <a name="project-task-entity-table"></a>Tabla de entidades de tarea de proyecto
En la siguiente tabla se describe cómo se sincronizan los datos de entidades de tarea de proyecto entre Project Service Automation y el complemento de escritorio de Microsoft Project.

| **Entidad** | **Campo** | **Microsoft Project a Project Service Automation** | **Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Tarea de proyecto | Fecha de vencimiento | Sincronizado | No sincronizado |
| Tarea de proyecto | Esfuerzo estimado | Sincronizado | No sincronizado |
| Tarea de proyecto | Id. de cliente de MS Project | Sincronizado | No sincronizado |
| Tarea de proyecto | Tarea principal | Sincronizado | No sincronizado |
| Tarea de proyecto | Project | Sincronizado | No sincronizado |
| Tarea de proyecto | Tarea de proyecto | Sincronizado | No sincronizado |
| Tarea de proyecto | Nombre de tarea de proyecto | Sincronizado | No sincronizado |
| Tarea de proyecto | Unidad de dotación de recursos (obsoleto en la versión 3.0) | Sincronizado | No sincronizado |
| Tarea de proyecto | Duración programada | Sincronizado | No sincronizado |
| Tarea de proyecto | Fecha de inicio | Sincronizado | No sincronizado |
| Tarea de proyecto | Id. de WBS | Sincronizado | No sincronizado |

### <a name="team-member-entity-table"></a>Tabla de entidades de miembros del equipo
En la siguiente tabla se describe cómo se sincronizan los datos de entidades de miembros del equipo entre Project Service Automation y el complemento de escritorio de Microsoft Project.

| **Entidad** | **Campo** | **Microsoft Project a Project Service Automation** | **Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Miembro del equipo | Id. de cliente de MS Project | Sincronizado | No sincronizado |
| Miembro del equipo | Nombre de puesto | Sincronizado | No sincronizado |
| Miembro del equipo | proyecto | Sincronizado | Sincronizado |
| Miembro del equipo | Equipo del proyecto | Sincronizado | Sincronizado |
| Miembro del equipo | Unidad de dotación de recursos | No sincronizado | Sincronizado |
| Miembro del equipo | Rol | No sincronizado | Sincronizado |
| Miembro del equipo | Horas laborables | No sincronizado | No sincronizado |

### <a name="resource-assignment-entity-table"></a>Tabla de entidades de asignación de recursos
En la siguiente tabla se describe cómo se sincronizan los datos de entidades de asignación de recursos entre Project Service Automation y el complemento de escritorio de Microsoft Project.

| **Entidad** | **Campo** | **Microsoft Project a Project Service Automation** | **Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Asignación de recursos | Desde la fecha | Sincronizado | No sincronizado |
| Asignación de recursos | Horas | Sincronizado | No sincronizado |
| Asignación de recursos | Id. de cliente de MS Project | Sincronizado | No sincronizado |
| Asignación de recursos | Trabajo previsto | Sincronizado | No sincronizado |
| Asignación de recursos | Project | Sincronizado | No sincronizado |
| Asignación de recursos | Equipo del proyecto | Sincronizado | No sincronizado |
| Asignación de recursos | Asignación de recursos | Sincronizado | No sincronizado |
| Asignación de recursos | Tarea | Sincronizado | No sincronizado |
| Asignación de recursos | Hasta la fecha | Sincronizado | No sincronizado |

### <a name="project-task-dependencies-entity-table"></a>Tabla de entidades de dependencias de tarea de proyecto
En la siguiente tabla se describe cómo se sincronizan los datos de entidades de dependencias de tarea de proyecto entre Project Service Automation y el complemento de escritorio de Microsoft Project.

| **Entidad** | **Campo** | **Microsoft Project a Project Service Automation** | **Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Dependencias de tareas de proyecto | Dependencia de tareas de proyecto | Sincronizado | No sincronizado |
| Dependencias de tareas de proyecto | Tipo de vínculo | Sincronizado | No sincronizado |
| Dependencias de tareas de proyecto | Tarea predecesora | Sincronizado | No sincronizado |
| Dependencias de tareas de proyecto | Project | Sincronizado | No sincronizado |
| Dependencias de tareas de proyecto | Tarea sucesora | Sincronizado | No sincronizado |

### <a name="additional-resources"></a>Recursos adicionales
 [Guía del jefe de proyecto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]