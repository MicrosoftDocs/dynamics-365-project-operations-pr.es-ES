---
title: Instalar y aplicar datos de configuración en Common Data Service para Project Operations
description: Este tema proporciona información sobre cómo instalar y aplicar los datos de configuración en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949090"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="23bdb-103">Instalar y aplicar datos de configuración en Common Data Service para Project Operations</span><span class="sxs-lookup"><span data-stu-id="23bdb-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="23bdb-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="23bdb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="23bdb-105">Instalar la configuración y los datos de configuración</span><span class="sxs-lookup"><span data-stu-id="23bdb-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="23bdb-106">Descargue, desbloquee y descomprima el [Paquete de instalación y datos de configuración](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="23bdb-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="23bdb-107">Navegue a la carpeta descomprimida y ejecute el archivo ejecutable *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="23bdb-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="23bdb-108">En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migración de la configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="23bdb-110">En la página 2 del asistente CMT, seleccione **Office 365** como **Tipo de implementación**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="23bdb-111">Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="23bdb-112">Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="23bdb-114">En la página 3, en la lista de organizaciones del inquilino, seleccione la organización a la que desea importar los datos de demostración y seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="23bdb-115">En la página 4, seleccione el archivo zip *SampleSetupAndConfigData* en la carpeta descomprimida.</span><span class="sxs-lookup"><span data-stu-id="23bdb-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selección de archivo zip](./media/3ZipFile.png)

![Seleccione un archivo](./media/4SelectAFile.png)

9. <span data-ttu-id="23bdb-118">Después de seleccionar el archivo zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-118">After the zip file is selected, select **Import Data**.</span></span>

![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="23bdb-120">La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red.</span><span class="sxs-lookup"><span data-stu-id="23bdb-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="23bdb-121">Una vez finalizada la importación, salga del asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="23bdb-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="23bdb-122">Compruebe si su organización dispone de datos en las siguientes 19 entidades:</span><span class="sxs-lookup"><span data-stu-id="23bdb-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="23bdb-123">Divisa</span><span class="sxs-lookup"><span data-stu-id="23bdb-123">Currency</span></span>
  - <span data-ttu-id="23bdb-124">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="23bdb-124">Organizational Unit</span></span>
  - <span data-ttu-id="23bdb-125">CONTACTO</span><span class="sxs-lookup"><span data-stu-id="23bdb-125">Contact</span></span>
  - <span data-ttu-id="23bdb-126">Grupo fiscal</span><span class="sxs-lookup"><span data-stu-id="23bdb-126">Tax Group</span></span>
  - <span data-ttu-id="23bdb-127">Grupo de clientes</span><span class="sxs-lookup"><span data-stu-id="23bdb-127">Customer Group</span></span>
  - <span data-ttu-id="23bdb-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="23bdb-128">Unit</span></span>
  - <span data-ttu-id="23bdb-129">Unidad de venta</span><span class="sxs-lookup"><span data-stu-id="23bdb-129">Unit Group</span></span>
  - <span data-ttu-id="23bdb-130">Lista de precios</span><span class="sxs-lookup"><span data-stu-id="23bdb-130">Price List</span></span>
  - <span data-ttu-id="23bdb-131">Lista de precios de parámetros de proyecto</span><span class="sxs-lookup"><span data-stu-id="23bdb-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="23bdb-132">Frecuencia de facturación</span><span class="sxs-lookup"><span data-stu-id="23bdb-132">Invoice Frequency</span></span>
  - <span data-ttu-id="23bdb-133">Categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="23bdb-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="23bdb-134">Categoría de transacción</span><span class="sxs-lookup"><span data-stu-id="23bdb-134">Transaction Category</span></span>
  - <span data-ttu-id="23bdb-135">Categoría de gastos</span><span class="sxs-lookup"><span data-stu-id="23bdb-135">Expense Category</span></span>
  - <span data-ttu-id="23bdb-136">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="23bdb-136">Role Price</span></span>
  - <span data-ttu-id="23bdb-137">Precio de categoría de transacciones</span><span class="sxs-lookup"><span data-stu-id="23bdb-137">Transaction Category Price</span></span>
  - <span data-ttu-id="23bdb-138">Característica</span><span class="sxs-lookup"><span data-stu-id="23bdb-138">Characteristic</span></span>
  - <span data-ttu-id="23bdb-139">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="23bdb-139">Bookable Resource</span></span>
  - <span data-ttu-id="23bdb-140">Asociación de categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="23bdb-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="23bdb-141">Característica del recurso reservable</span><span class="sxs-lookup"><span data-stu-id="23bdb-141">Bookable Resource Characteristic</span></span>

![Completar importación](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="23bdb-143">Actualizar configuraciones de operaciones de proyecto</span><span class="sxs-lookup"><span data-stu-id="23bdb-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="23bdb-144">Vaya al entorno CE.</span><span class="sxs-lookup"><span data-stu-id="23bdb-144">Navigate to the CE environment.</span></span> <span data-ttu-id="23bdb-145">Puede encontrarlo abriendo el [Centro de administración de Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionando el entorno y luego seleccionando **Abrir entorno**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir entorno](./media/7OpenEnvironment.png)

2. <span data-ttu-id="23bdb-147">Vaya a **Proyectos** > **Recursos** y luego seleccione **Nuevo** para crear un recurso que se pueda reservar para su usuario.</span><span class="sxs-lookup"><span data-stu-id="23bdb-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos que se pueden reservar](./media/8BookableResources.png)

3. <span data-ttu-id="23bdb-149">En la pestaña **General**, seleccione su usuario administrador.</span><span class="sxs-lookup"><span data-stu-id="23bdb-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="23bdb-150">Verifique que la zona horaria coincida con la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="23bdb-150">Verify that the time zone matches the one you are in.</span></span> 

![Nuevo recurso reservable](./media/9NewBookableResource.png)

4. <span data-ttu-id="23bdb-152">En la pestaña **Planificación** del campo **Empresa**, elija la empresa **USPM** y luego seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Pestaña de programación](./media/10SchedulingTab.png)

5. <span data-ttu-id="23bdb-154">Seleccione la pestaña **Horas de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-154">Select the **Work hours** tab.</span></span>  

![Horas laborables](./media/11WorkHours.png)

6. <span data-ttu-id="23bdb-156">Haga doble clic en cualquier valor del calendario y seleccione **Editar** > **Todos los eventos de la serie**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendario de trabajo](./media/12WorkCalendar.png)

7. <span data-ttu-id="23bdb-158">Cambie el horario laboral a un día laborable de ocho (8) horas, marque los fines de semana como días no laborables y asegúrese de que la zona horaria coincida con la suya.</span><span class="sxs-lookup"><span data-stu-id="23bdb-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="23bdb-159">Seleccione **Guardar y cerrar**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-159">Select **Save and close**.</span></span>

![Actualizar calendario](./media/13UpdateCalendar.png)

9. <span data-ttu-id="23bdb-161">Vaya a **Configuración** > **Plantillas de calendario** y seleccione **Nueva**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Plantillas de calendario](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="23bdb-163">Introduzca un nombre, seleccione el recurso de plantilla que creó y luego seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Guardar plantilla de calendario](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="23bdb-165">Vaya a **Parámetros** y haga doble clic en el registro.</span><span class="sxs-lookup"><span data-stu-id="23bdb-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parámetros de proyecto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="23bdb-167">Actualice los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="23bdb-167">Update the following fields:</span></span>

 - <span data-ttu-id="23bdb-168">**Empresa predeterminada**: USPM</span><span class="sxs-lookup"><span data-stu-id="23bdb-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="23bdb-169">**Unidad organizativa predeterminada**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="23bdb-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="23bdb-170">**Frecuencia de facturación**: séptimo y último día</span><span class="sxs-lookup"><span data-stu-id="23bdb-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="23bdb-171">**Plantilla de horas de trabajo**: cambia a la plantilla que creó.</span><span class="sxs-lookup"><span data-stu-id="23bdb-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="23bdb-172">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="23bdb-172">Select **Save**.</span></span> 

![Parámetros de proyecto actualizados](./media/17UpdatedProjectParameters.png)
