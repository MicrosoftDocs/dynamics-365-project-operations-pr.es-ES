---
title: Solucionar problemas de trabajo en la cuadrícula de tareas
description: Este artículo proporciona información acerca de la información necesaria al trabajar en la cuadrícula Tarea.
author: ruhercul
ms.date: 07/22/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 208ed55abf4cdf0ad2b035bd923e183ff3cae660
ms.sourcegitcommit: e91136d3335ee03db660529eccacd48907774453
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188253"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Solucionar problemas de trabajo en la cuadrícula de tareas 


_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos en existencias, implementación simplificada: de la oferta a la facturación proforma, Project for the Web_

La cuadrícula de tareas usada por Dynamics 365 Project Operations es un iframe hospedado en Microsoft Dataverse. Como resultado de este uso, se deben cumplir requisitos específicos para garantizar que la autenticación y la autorización funcionen correctamente. Este artículo describe los problemas comunes que pueden afectar a la capacidad de representar la cuadrícula o administrar tareas en la estructura de descomposición del trabajo (WBS).

Problemas comunes:

- La pestaña **Tarea** de la cuadrícula de tareas está vacía.
- Al abrir el proyecto, el proyecto no se carga y la interfaz de usuario (IU) se atasca en el control giratorio.
- Administración de privilegios para **Project for the Web**.
- Los cambios no se guardan cuando crea, actualiza o elimina una tarea.

## <a name="issue-the-task-tab-is-empty"></a>Problema: la pestaña Tarea está vacía

### <a name="mitigation-1-enable-cookies"></a>Mitigación 1: habilitar cookies

Project Operations requiere que las cookies de terceros estén habilitadas para representar la estructura de descomposición del trabajo. Si las cookies de terceros no están habilitadas, en lugar de ver tareas, verá una página en blanco al seleccionar la pestaña **Tareas** en la página **Proyecto**.

Para los exploradores Microsoft Edge o Google Chrome, los siguientes procedimientos describen cómo se actualiza la configuración del explorador para habilitar las cookies de terceros.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Abra el explorador Edge.
2. En la esquina superior derecha, seleccione el botón de **puntos suspensivos** (...) y seleccione **Configuración**.
3. En **Cookies y permisos del sitio**, seleccione **Cookies y datos del sitio**.
4. Desactive **Bloquear cookies de terceros**.
5. Actualice el explorador. 

#### <a name="google-chrome"></a>Google Chrome

1. Abra el explorador Chrome.
2. En la esquina superior derecha, seleccione los tres puntos verticales y, a continuación, seleccione **Configuración**.
3. En **Privacidad y seguridad**, seleccione **Cookies y otros datos del sitio**.
4. Seleccione **Permitir todas las cookies**.
5. Actualice el explorador. 

> [!NOTE]
> Si bloquea las cookies de terceros, se bloquearán todas las cookies y los datos del sitio de otros sitios, incluso si el sitio está permitido en la lista de excepciones.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Mitigación 2: validar que el extremo de PEX se haya configurado correctamente

Project Operations requiere que un parámetro del proyecto haga referencia al extremo de PEX. Este extremo es necesario para comunicarse con el servicio que se usa para representar la estructura de descomposición del trabajo. Si el parámetro no está habilitado, recibirá el error "El parámetro del proyecto no es válido". Para actualizar el extremo de PEX, complete los siguientes pasos.

1. Agregue el campo **Extremo de PEX** a la página **Parámetros del proyecto**.
2. Identifique el tipo de producto que está utilizando. Este valor se usa cuando se establece el extremo de PEX. Tras la recuperación, el tipo de producto ya está definido en el extremo de PEX. Mantenga ese valor.
3. Actualice el campo con el siguiente valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. La siguiente tabla proporciona el parámetro de tipo que debe usarse según el tipo de producto.

      | **Tipo de producto**                     | **Tipo de parámetro** |
      |--------------------------------------|--------------------|
      | Project for the Web en organización predeterminada   | type=0             |
      | Project for the Web en organización denominada CDS | type=1             |
      | Project Operations                   | type=2             |

4. Quite el campo de la página **Parámetros del proyecto**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Mitigación 3: iniciar sesión en project.microsoft.com.

En el navegador , abra una nueva pestaña, vaya a project.microsoft.com e inicie sesión con el rol de usuario que está usando para acceder a Project Operations. Es importante que solo un usuario inicie sesión en un producto de Microsoft en el navegador. El mensaje de error "login.microsoftonline.com se negó a conectarse" ocurre con mayor frecuencia cuando más de un usuario ha iniciado sesión, como se muestra en la siguiente ilustración.

![Elija una página de inicio de sesión de cuenta que muestre que dos usuarios han iniciado sesión.](media/MULTIPLE_USERS_LOGGED_IN.png)

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problema: el proyecto no se carga y la interfaz de usuario está bloqueada en el control giratorio

A los efectos de la autenticación, las ventanas emergentes deben estar habilitadas para que se cargue la cuadrícula de tareas. Si las ventanas emergentes no están habilitadas, la pantalla se bloqueará en el control giratorio de carga. El siguiente gráfico muestra la dirección URL con una etiqueta emergente bloqueada en la barra de direcciones, lo que hace que el control giratorio se atasque al intentar cargar la página. 

   ![Control giratorio bloqueado y bloque emergente.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Mitigación 1: habilitar elementos emergentes

Cuando su proyecto está bloqueado en el control giratorio, es posible que las ventanas emergentes no estén habilitadas.

#### <a name="microsoft-edge"></a>Microsoft Edge

Hay dos formas de habilitar las ventanas emergentes en su navegador Edge.

1. En su navegador Edge, seleccione la notificación en la esquina superior derecha del navegador.
2. Seleccione **Permitir siempre elementos emergentes y redirecciones de** el entorno de Dataverse específico.
 
     ![Ventana emergente bloqueada.](media/enablepopups.png)

Como alternativa, puede realizar los siguientes pasos.

1. Abra el explorador Edge.
2. En la esquina superior derecha, seleccione **puntos suspensivos** (...), y luego seleccione **Configuración** > **Permisos del sitio** > **Elementos emergentes y redireccionamientos**.
3. Desactive **Elementos emergentes y redireccionamientos** para bloquear los elementos emergentes, o actívelo para permitirlos en su dispositivo.
4. Después de habilitar los elementos emergentes, actualice su navegador. 

#### <a name="google-chrome"></a>Google Chrome
1. Abra el explorador Chrome.
2. Navegue a una página donde los elementos emergentes estén bloqueados.
3. En la barra de direcciones, seleccione **Elemento emergente bloqueado**.
4. Seleccione el enlace del elemento emergente que desea ver.
5. Después de habilitar los elementos emergentes, actualice su navegador. 

> [!NOTE]
> Para ver siempre los elementos emergentes del sitio, seleccione **Permitir siempre elementos emergentes y redireccionamientos de [sitio]** y luego seleccione **Hecho**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problema 3: administración de privilegios para Project for the Web

Project Operations se basa en un servicio de programación externo. El servicio requiere que un usuario tenga varios roles asignados que le permitan leer y escribir en entidades relacionadas con WBS. Estas entidades incluyen tareas de proyectos, asignaciones de recursos y dependencias de tareas. Si un usuario no puede representar WBS cuando navega a la pestaña **Tareas**, probablemente se deba a que no ha sido habilitado **Proyecto** para **Project Operations**. Un usuario puede recibir un error de rol de seguridad o un error relacionado con una denegación de acceso.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Mitigación 1: validar el usuario de la aplicación y los roles de seguridad del usuario final

1. Vaya a **Configuración** > **Seguridad** > **Usuarios** > **Usuarios de la aplicación**.  

   ![Lector de aplicación.](media/applicationuser.jpg)
   
2. Haga doble clic en el registro de usuario de la aplicación para verificar:

     - El usuario tiene acceso al proyecto. Puede hacer esto verificando que el usuario tenga rol de seguridad **Jefe de proyecto**.
     - El usuario de la aplicación de Microsoft Project existe y está configurado correctamente.
 
3. Si este usuario no existe, cree un nuevo registro de usuario. 
4. Seleccione **Usuarios nuevos**, cambie el formulario de inscripción a **Usuario de la aplicación** y luego agregue el **ID de aplicación**.

   ![Detalles del usuario de la aplicación.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problema 4: los cambios no se guardan cuando crea, actualiza o elimina una tarea

Cuando realiza una o más actualizaciones en la WBS, los cambios fallan y no se guardan. Se produce un error en la cuadrícula de programación con un mensaje que dice: "No se pudieron guardar los cambios recientes que realizó".

### <a name="mitigation-1-validate-the-license-assignment"></a>Mitigación 1: validar la asignación de licencia

1. Compruebe que al usuario se le haya asignado la licencia correcta y que el servicio esté habilitado en los detalles de los planes de servicio de la licencia.  
2. Compruebe que el usuario pueda abrir **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Mitigación 2: configuración de validación del usuario de la aplicación del proyecto
1. Compruebe que se ha creado el usuario de la aplicación del proyecto.
2. Aplique los siguientes roles de seguridad al usuario:
  
  - Usuario o usuario base de Dataverse
  - Sistema de Project Operations
  - Sistema de proyecto
  - Sistemas de doble escritura de Project Operations. Este rol es necesario para la implementación de escenarios basados en recursos/no mantenidos en existencias de Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
