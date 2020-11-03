---
title: Aplicar datos de demostración de Project Operations a un entorno hospedado en Finance Cloud
description: Este tema explica cómo aplicar datos de demostración de Project Operations a un entorno alojado en la nube de Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096643"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="128b4-103">Aplicar datos de demostración de Project Operations a un entorno hospedado en Finance Cloud</span><span class="sxs-lookup"><span data-stu-id="128b4-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="128b4-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="128b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="128b4-105">Este tema solo se aplica a Microsoft Dynamics 365 Finance, versión 10.0.13, y solo se puede ejecutar en un entorno alojado en la nube.</span><span class="sxs-lookup"><span data-stu-id="128b4-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="128b4-106">Complete los pasos de este tema **ANTES** de aplicar actualizaciones de calidad al entorno.</span><span class="sxs-lookup"><span data-stu-id="128b4-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="128b4-107">En su proyecto LCS, abra la página **Detalles del entorno**.</span><span class="sxs-lookup"><span data-stu-id="128b4-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="128b4-108">Tenga en cuenta que incluye los detalles necesarios para conectarse al entorno mediante el Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="128b4-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Detalles del entorno de](./media/1EnvironmentDetails.png)

<span data-ttu-id="128b4-110">El primer conjunto de credenciales resaltadas son las credenciales de la cuenta local y contienen un hipervínculo a la conexión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="128b4-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="128b4-111">Las credenciales incluyen el nombre de usuario y la contraseña del administrador del entorno.</span><span class="sxs-lookup"><span data-stu-id="128b4-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="128b4-112">El segundo conjunto de credenciales se utiliza para iniciar sesión en SQL Server en este entorno.</span><span class="sxs-lookup"><span data-stu-id="128b4-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="128b4-113">Conéctese remotamente con el entorno mediante el hipervínculo de **Cuentas locales** y use las **Credenciales de cuenta local** para autenticar.</span><span class="sxs-lookup"><span data-stu-id="128b4-113">Remote to the environment by the hyperlink in **Local Accounts** , and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="128b4-114">Vaya a **Servicios de Información de Internet** > **Grupos de aplicaciones** > **AOSService** y detenga el servicio.</span><span class="sxs-lookup"><span data-stu-id="128b4-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="128b4-115">Está deteniendo el servicio en este punto para poder continuar reemplazando la base de datos SQL.</span><span class="sxs-lookup"><span data-stu-id="128b4-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Detener AOS](./media/2StopAOS.png)

4. <span data-ttu-id="128b4-117">Vaya a **Servicios** y detenga los siguientes dos elementos:</span><span class="sxs-lookup"><span data-stu-id="128b4-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="128b4-118">Microsoft Dynamics 365 Unified Operations: Servicio de gestión de lotes</span><span class="sxs-lookup"><span data-stu-id="128b4-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="128b4-119">Microsoft Dynamics 365 Unified Operations: marco de importación y exportación de datos</span><span class="sxs-lookup"><span data-stu-id="128b4-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Detener servicios](./media/3StopServices.png)

5. <span data-ttu-id="128b4-121">Abrir Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="128b4-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="128b4-122">Inicie sesión con las credenciales del servidor SQL y use el usuario axdbadmin y la contraseña de la página **Detalles de entornos** LCS.</span><span class="sxs-lookup"><span data-stu-id="128b4-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="128b4-124">En el Explorador de objetos, **Bases de datos** y localice **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="128b4-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="128b4-125">Reemplazará la base de datos con una nueva base de datos que se encuentra en el [Centro de descargas](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="128b4-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="128b4-126">Copie el archivo zip en la VM a la que está conectado de forma remota y extraiga el contenido del zip.</span><span class="sxs-lookup"><span data-stu-id="128b4-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="128b4-127">En SQL Server Management Studio, haga clic con el botón derecho en **AxDB** y luego seleccione **Tareas** > **Restaurar** > **Base de datos**.</span><span class="sxs-lookup"><span data-stu-id="128b4-127">In SQL Server Management Studio, right-click **AxDB** , and then select **Tasks** > **Restore** > **Database**.</span></span>

![Restaurar base de datos](./media/5RestoreDatabase.png)

9. <span data-ttu-id="128b4-129">Seleccione **Dispositivo de origen** y navegue hasta el archivo extraído del zip que copió.</span><span class="sxs-lookup"><span data-stu-id="128b4-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Dispositivos de origen](./media/6SourceDevice.png)

10. <span data-ttu-id="128b4-131">Seleccione **Opciones** y luego seleccione **Sobrescribir la base de datos existente** y **Cerrar las conexiones existentes a la base de datos de destino**.</span><span class="sxs-lookup"><span data-stu-id="128b4-131">Select **Options** , and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="128b4-132">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="128b4-132">Select **OK**.</span></span>

![Restaurar configuracion](./media/7RestoreSetting.png)

<span data-ttu-id="128b4-134">Recibirá la confirmación de que la restauración de AXDB se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="128b4-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="128b4-135">Después de recibir esta confirmación, puede cerrar SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="128b4-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="128b4-136">Vuelva a **Servicios de Información de Internet** > **Grupos de aplicaciones** > **AOSService** e inicie AOSService.</span><span class="sxs-lookup"><span data-stu-id="128b4-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="128b4-137">Vaya a **Servicios** e inicie los dos servicios que detuvo antes.</span><span class="sxs-lookup"><span data-stu-id="128b4-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="128b4-138">Busque la herramienta AdminUserProvisioning en esta VM.</span><span class="sxs-lookup"><span data-stu-id="128b4-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="128b4-139">Busque en K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="128b4-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="128b4-140">Ejecute el archivo .ext con su dirección de usuario en el campo **Dirección de correo electrónico**.</span><span class="sxs-lookup"><span data-stu-id="128b4-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="128b4-141">Seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="128b4-141">Select **Submit**.</span></span>

![Aprovisionamiento de usuarios administradores](./media/8AdminUserProvisioning.png)

<span data-ttu-id="128b4-143">Esto puede tardar un par de minutos en completarse.</span><span class="sxs-lookup"><span data-stu-id="128b4-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="128b4-144">Debería recibir un mensaje de confirmación de que el usuario administrador se actualizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="128b4-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="128b4-145">Por último, ejecute el símbolo del sistema como administrador y realice iisreset</span><span class="sxs-lookup"><span data-stu-id="128b4-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Restablecimiento de IIS](./media/9IISReset.png)

18. <span data-ttu-id="128b4-147">Cierre la sesión de escritorio remoto y use la página **Detalles del entorno** LCS para iniciar sesión en el entorno y confirmar que funciona como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="128b4-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
