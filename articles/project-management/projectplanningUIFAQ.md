---
title: Solucionar problemas de trabajo en la cuadrícula de tareas
description: Este tema proporciona la información necesaria para solucionar problemas al trabajar en la cuadrícula de tareas.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031558"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Solucionar problemas de trabajo en la cuadrícula de tareas 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Este tema describe cómo solucionar los problemas que pueden surgir al trabajar con la gestión de costes.

## <a name="enable-cookies"></a>Habilitar cookies

Project Operations requiere que las cookies de terceros estén habilitadas para representar la estructura de descomposición del trabajo. Si las cookies de terceros no están habilitadas, en lugar de ver tareas, verá una página en blanco al seleccionar la pestaña **Tareas** en la página **Proyecto**.

![Pestaña en blanco cuando las cookies de terceros no están habilitadas](media/blankschedule.png)


### <a name="workaround"></a>Solución alternativa
Para los exploradores Microsoft Edge o Google Chrome, los siguientes procedimientos describen cómo se actualiza la configuración del explorador para habilitar las cookies de terceros.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Abra el explorador Edge.
2. En la esquina superior derecha, seleccione el botón de **puntos suspensivos** (...) y seleccione **Configuración**.
3. En **Cookies y permisos del sitio**, seleccione **Cookies y datos del sitio**.
4. Desactive **Bloquear cookies de terceros**.

#### <a name="google-chrome"></a>Google Chrome

1. Abra el explorador Chrome.
2. En la esquina superior derecha, seleccione los tres puntos verticales y, a continuación, seleccione **Configuración**.
3. En **Privacidad y seguridad**, seleccione **Cookies y otros datos del sitio**.
4. Seleccione **Permitir todas las cookies**.

> [!IMPORTANT]
> Si bloquea las cookies de terceros, se bloquearán todas las cookies y los datos del sitio de otros sitios, incluso si el sitio está permitido en la lista de excepciones.

## <a name="pex-endpoint"></a>Extremo de PEX

Project Operations requiere que un parámetro del proyecto haga referencia al extremo de PEX. Este extremo es necesario para comunicarse con el servicio utilizado para representar la estructura de descomposición del trabajo. Si el parámetro no está habilitado, recibirá el error "El parámetro del proyecto no es válido". 

### <a name="workaround"></a>Solución alternativa
 ![El campo Extremo de PEX en el parámetro del proyecto](media/projectparameter.png)

1. Agregue el campo **Extremo de PEX** a la página **Parámetros del proyecto**.
2. Actualice el campo con el siguiente valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Quite el campo de la página **Parámetros del proyecto**.

## <a name="privileges-for-project-for-the-web"></a>Privilegios de Project para web

Project Operations se basa en un servicio de programación externo. El servicio requiere que un usuario tenga varios roles asignados para leer y escribir en entidades relacionadas con la estructura de descomposición del trabajo. Estas entidades incluyen tareas de proyectos, asignaciones de recursos y dependencias de tareas. Si un usuario no puede representar la estructura de descomposición del trabajo cuando va a la pestaña **Tareas**, probablemente se deba a no se ha habilitado Project para Project Operations. Un usuario puede recibir un error de rol de seguridad o un error relacionado con una denegación de acceso.


## <a name="workaround"></a>Solución alternativa

1. Vaya a **Configuración > Seguridad > Usuarios > Usuarios de la aplicación**.  

   ![Lector de aplicación](media/applicationuser.jpg)
   
2. Haga doble clic en el registro de usuario de la aplicación para comprobar lo siguiente:

 - El usuario tiene acceso al proyecto. Esta comprobación suele realizarse asegurándose de que el usuario tenga el rol de seguridad **Jefe de proyecto**.
 - El usuario de la aplicación de Microsoft Project existe y está configurado correctamente.
 
3. Si este usuario no existe, puede crear un registro de usuario nuevo. Seleccione **Nuevos usuarios**. Cambie el formulario de entrada a **Usuario de la aplicación** y agregue el **Id. de aplicación**.

   ![Detalles del usuario de la aplicación](media/applicationuserdetails.jpg)

4. Compruebe que al usuario se le haya asignado la licencia correcta y que el servicio esté habilitado en los detalles de los planes de servicio de la licencia.
5. Compruebe que el usuario pueda abrir project.microsoft.com.
6. Compruebe a través de los parámetros del proyecto que el sistema apunte al extremo de proyecto correcto.
7. Compruebe que se ha creado el usuario de la aplicación del proyecto.
8. Aplique los siguientes roles de seguridad al usuario:

  - Usuario de Dataverse
  - Sistema de Project Operations
  - Sistema de Project

## <a name="error-when-updating-the-work-breakdown-structure"></a>Error al actualizar la estructura de descomposición del trabajo

Cuando se realizan una o más actualizaciones en la estructura de descomposición del trabajo, los cambios acaban por generar errores y no se guardan. Se produce un error en la cuadrícula de programación que indica que "No se pudo guardar el cambio realizado recientemente".

### <a name="workaround"></a>Solución alternativa

1. Compruebe que al usuario se le haya asignado la licencia correcta y que el servicio esté habilitado en los detalles de los planes de servicio de la licencia.
2. Compruebe que el usuario pueda abrir project.microsoft.com.
3. Compruebe que el sistema apunte al extremo de proyecto correcto.
4. Compruebe que se ha creado el usuario de la aplicación del proyecto.
5. Aplique los siguientes roles de seguridad al usuario:
  
  - Usuario o usuario base de Dataverse
  - Sistema de Project Operations
  - Sistema de Project
  - Sistema de doble escritura de Project Operations (este rol es obligatorio si se va a implementar el escenario basado en recursos/no mantenidos en existencias de Project Operations).
