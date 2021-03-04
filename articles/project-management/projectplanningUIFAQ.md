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
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="d70db-103">Solucionar problemas de trabajo en la cuadrícula de tareas</span><span class="sxs-lookup"><span data-stu-id="d70db-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="d70db-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="d70db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d70db-105">Este tema describe cómo solucionar los problemas que pueden surgir al trabajar con la gestión de costes.</span><span class="sxs-lookup"><span data-stu-id="d70db-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="d70db-106">Habilitar cookies</span><span class="sxs-lookup"><span data-stu-id="d70db-106">Enable cookies</span></span>

<span data-ttu-id="d70db-107">Project Operations requiere que las cookies de terceros estén habilitadas para representar la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d70db-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="d70db-108">Si las cookies de terceros no están habilitadas, en lugar de ver tareas, verá una página en blanco al seleccionar la pestaña **Tareas** en la página **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="d70db-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Pestaña en blanco cuando las cookies de terceros no están habilitadas](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="d70db-110">Solución alternativa</span><span class="sxs-lookup"><span data-stu-id="d70db-110">Workaround</span></span>
<span data-ttu-id="d70db-111">Para los exploradores Microsoft Edge o Google Chrome, los siguientes procedimientos describen cómo se actualiza la configuración del explorador para habilitar las cookies de terceros.</span><span class="sxs-lookup"><span data-stu-id="d70db-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="d70db-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d70db-112">Microsoft Edge</span></span>

1. <span data-ttu-id="d70db-113">Abra el explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="d70db-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="d70db-114">En la esquina superior derecha, seleccione el botón de **puntos suspensivos** (...) y seleccione **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="d70db-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="d70db-115">En **Cookies y permisos del sitio**, seleccione **Cookies y datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="d70db-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="d70db-116">Desactive **Bloquear cookies de terceros**.</span><span class="sxs-lookup"><span data-stu-id="d70db-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="d70db-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="d70db-117">Google Chrome</span></span>

1. <span data-ttu-id="d70db-118">Abra el explorador Chrome.</span><span class="sxs-lookup"><span data-stu-id="d70db-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="d70db-119">En la esquina superior derecha, seleccione los tres puntos verticales y, a continuación, seleccione **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="d70db-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="d70db-120">En **Privacidad y seguridad**, seleccione **Cookies y otros datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="d70db-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="d70db-121">Seleccione **Permitir todas las cookies**.</span><span class="sxs-lookup"><span data-stu-id="d70db-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d70db-122">Si bloquea las cookies de terceros, se bloquearán todas las cookies y los datos del sitio de otros sitios, incluso si el sitio está permitido en la lista de excepciones.</span><span class="sxs-lookup"><span data-stu-id="d70db-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="d70db-123">Extremo de PEX</span><span class="sxs-lookup"><span data-stu-id="d70db-123">PEX Endpoint</span></span>

<span data-ttu-id="d70db-124">Project Operations requiere que un parámetro del proyecto haga referencia al extremo de PEX.</span><span class="sxs-lookup"><span data-stu-id="d70db-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="d70db-125">Este extremo es necesario para comunicarse con el servicio utilizado para representar la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d70db-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="d70db-126">Si el parámetro no está habilitado, recibirá el error "El parámetro del proyecto no es válido".</span><span class="sxs-lookup"><span data-stu-id="d70db-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="d70db-127">Solución alternativa</span><span class="sxs-lookup"><span data-stu-id="d70db-127">Workaround</span></span>
 ![El campo Extremo de PEX en el parámetro del proyecto](media/projectparameter.png)

1. <span data-ttu-id="d70db-129">Agregue el campo **Extremo de PEX** a la página **Parámetros del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="d70db-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="d70db-130">Actualice el campo con el siguiente valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="d70db-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="d70db-131">Quite el campo de la página **Parámetros del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="d70db-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="d70db-132">Privilegios de Project para web</span><span class="sxs-lookup"><span data-stu-id="d70db-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="d70db-133">Project Operations se basa en un servicio de programación externo.</span><span class="sxs-lookup"><span data-stu-id="d70db-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="d70db-134">El servicio requiere que un usuario tenga varios roles asignados para leer y escribir en entidades relacionadas con la estructura de descomposición del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d70db-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="d70db-135">Estas entidades incluyen tareas de proyectos, asignaciones de recursos y dependencias de tareas.</span><span class="sxs-lookup"><span data-stu-id="d70db-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="d70db-136">Si un usuario no puede representar la estructura de descomposición del trabajo cuando va a la pestaña **Tareas**, probablemente se deba a no se ha habilitado Project para Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d70db-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="d70db-137">Un usuario puede recibir un error de rol de seguridad o un error relacionado con una denegación de acceso.</span><span class="sxs-lookup"><span data-stu-id="d70db-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="d70db-138">Solución alternativa</span><span class="sxs-lookup"><span data-stu-id="d70db-138">Workaround</span></span>

1. <span data-ttu-id="d70db-139">Vaya a **Configuración > Seguridad > Usuarios > Usuarios de la aplicación**.</span><span class="sxs-lookup"><span data-stu-id="d70db-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Lector de aplicación](media/applicationuser.jpg)
   
2. <span data-ttu-id="d70db-141">Haga doble clic en el registro de usuario de la aplicación para comprobar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d70db-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="d70db-142">El usuario tiene acceso al proyecto.</span><span class="sxs-lookup"><span data-stu-id="d70db-142">The user has access to the project.</span></span> <span data-ttu-id="d70db-143">Esta comprobación suele realizarse asegurándose de que el usuario tenga el rol de seguridad **Jefe de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="d70db-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="d70db-144">El usuario de la aplicación de Microsoft Project existe y está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d70db-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="d70db-145">Si este usuario no existe, puede crear un registro de usuario nuevo.</span><span class="sxs-lookup"><span data-stu-id="d70db-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="d70db-146">Seleccione **Nuevos usuarios**.</span><span class="sxs-lookup"><span data-stu-id="d70db-146">Select **New Users**.</span></span> <span data-ttu-id="d70db-147">Cambie el formulario de entrada a **Usuario de la aplicación** y agregue el **Id. de aplicación**.</span><span class="sxs-lookup"><span data-stu-id="d70db-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detalles del usuario de la aplicación](media/applicationuserdetails.jpg)

4. <span data-ttu-id="d70db-149">Compruebe que al usuario se le haya asignado la licencia correcta y que el servicio esté habilitado en los detalles de los planes de servicio de la licencia.</span><span class="sxs-lookup"><span data-stu-id="d70db-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="d70db-150">Compruebe que el usuario pueda abrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d70db-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="d70db-151">Compruebe a través de los parámetros del proyecto que el sistema apunte al extremo de proyecto correcto.</span><span class="sxs-lookup"><span data-stu-id="d70db-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="d70db-152">Compruebe que se ha creado el usuario de la aplicación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d70db-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="d70db-153">Aplique los siguientes roles de seguridad al usuario:</span><span class="sxs-lookup"><span data-stu-id="d70db-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="d70db-154">Usuario de Dataverse</span><span class="sxs-lookup"><span data-stu-id="d70db-154">Dataverse User</span></span>
  - <span data-ttu-id="d70db-155">Sistema de Project Operations</span><span class="sxs-lookup"><span data-stu-id="d70db-155">Project Operations System</span></span>
  - <span data-ttu-id="d70db-156">Sistema de Project</span><span class="sxs-lookup"><span data-stu-id="d70db-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="d70db-157">Error al actualizar la estructura de descomposición del trabajo</span><span class="sxs-lookup"><span data-stu-id="d70db-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="d70db-158">Cuando se realizan una o más actualizaciones en la estructura de descomposición del trabajo, los cambios acaban por generar errores y no se guardan.</span><span class="sxs-lookup"><span data-stu-id="d70db-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="d70db-159">Se produce un error en la cuadrícula de programación que indica que "No se pudo guardar el cambio realizado recientemente".</span><span class="sxs-lookup"><span data-stu-id="d70db-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="d70db-160">Solución alternativa</span><span class="sxs-lookup"><span data-stu-id="d70db-160">Workaround</span></span>

1. <span data-ttu-id="d70db-161">Compruebe que al usuario se le haya asignado la licencia correcta y que el servicio esté habilitado en los detalles de los planes de servicio de la licencia.</span><span class="sxs-lookup"><span data-stu-id="d70db-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="d70db-162">Compruebe que el usuario pueda abrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d70db-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="d70db-163">Compruebe que el sistema apunte al extremo de proyecto correcto.</span><span class="sxs-lookup"><span data-stu-id="d70db-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="d70db-164">Compruebe que se ha creado el usuario de la aplicación del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d70db-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="d70db-165">Aplique los siguientes roles de seguridad al usuario:</span><span class="sxs-lookup"><span data-stu-id="d70db-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="d70db-166">Usuario o usuario base de Dataverse</span><span class="sxs-lookup"><span data-stu-id="d70db-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="d70db-167">Sistema de Project Operations</span><span class="sxs-lookup"><span data-stu-id="d70db-167">Project Operations System</span></span>
  - <span data-ttu-id="d70db-168">Sistema de Project</span><span class="sxs-lookup"><span data-stu-id="d70db-168">Project System</span></span>
  - <span data-ttu-id="d70db-169">Sistema de doble escritura de Project Operations (este rol es obligatorio si se va a implementar el escenario basado en recursos/no mantenidos en existencias de Project Operations).</span><span class="sxs-lookup"><span data-stu-id="d70db-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
