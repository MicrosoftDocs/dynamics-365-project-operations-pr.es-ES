---
title: Configurar y aplicar datos de configuración en Common Data Service
description: Este tema proporciona información sobre cómo instalar y aplicar los datos de configuración en Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642249"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="b5289-103">Configurar y aplicar datos de configuración en Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b5289-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="b5289-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="b5289-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="b5289-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b5289-105">Prerequisites</span></span>

<span data-ttu-id="b5289-106">Antes de comenzar a configurar los datos en Common Data Service (CDS), se deben cumplir los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="b5289-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="b5289-107">Proporcione un entorno CDS y un entorno Dynamics 365 Finance para Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b5289-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="b5289-108">La información de entidad legal de Dynamics 365 Finance se comparte con el entorno CDS.</span><span class="sxs-lookup"><span data-stu-id="b5289-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="b5289-109">Esto significa que la entidad **Empresa** en CDS tiene los siguientes registros de empresa:</span><span class="sxs-lookup"><span data-stu-id="b5289-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="b5289-110">THPM</span><span class="sxs-lookup"><span data-stu-id="b5289-110">THPM</span></span>
  - <span data-ttu-id="b5289-111">USPM</span><span class="sxs-lookup"><span data-stu-id="b5289-111">USPM</span></span>
  - <span data-ttu-id="b5289-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="b5289-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="b5289-113">Instalar la configuración y los datos de configuración</span><span class="sxs-lookup"><span data-stu-id="b5289-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="b5289-114">Descargue, desbloquee y descomprima el [Paquete de instalación y datos de configuración](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="b5289-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="b5289-115">Navegue a la carpeta descomprimida y ejecute el archivo ejecutable *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="b5289-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="b5289-116">En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="b5289-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migración de la configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="b5289-118">En la página 2 del asistente CMT, seleccione **Microsoft 365** como **Tipo de implementación**.</span><span class="sxs-lookup"><span data-stu-id="b5289-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="b5289-119">Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="b5289-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="b5289-120">Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="b5289-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="b5289-122">En la página 3, en la lista de organizaciones del inquilino, seleccione la organización a la que desea importar los datos de demostración y seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="b5289-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="b5289-123">En la página 4, seleccione el archivo zip *SampleSetupAndConfigData* en la carpeta descomprimida.</span><span class="sxs-lookup"><span data-stu-id="b5289-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selección de archivo zip](./media/3ZipFile.png)

![Seleccione un archivo](./media/4SelectAFile.png)

9. <span data-ttu-id="b5289-126">Después de seleccionar el archivo zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="b5289-126">After the zip file is selected, select **Import Data**.</span></span>

![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="b5289-128">La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red.</span><span class="sxs-lookup"><span data-stu-id="b5289-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="b5289-129">Una vez finalizada la importación, salga del asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="b5289-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="b5289-130">Compruebe si su organización dispone de datos en las siguientes 19 entidades:</span><span class="sxs-lookup"><span data-stu-id="b5289-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="b5289-131">Divisa</span><span class="sxs-lookup"><span data-stu-id="b5289-131">Currency</span></span>
  - <span data-ttu-id="b5289-132">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="b5289-132">Organizational Unit</span></span>
  - <span data-ttu-id="b5289-133">CONTACTO</span><span class="sxs-lookup"><span data-stu-id="b5289-133">Contact</span></span>
  - <span data-ttu-id="b5289-134">Grupo fiscal</span><span class="sxs-lookup"><span data-stu-id="b5289-134">Tax Group</span></span>
  - <span data-ttu-id="b5289-135">Grupo de clientes</span><span class="sxs-lookup"><span data-stu-id="b5289-135">Customer Group</span></span>
  - <span data-ttu-id="b5289-136">Unidad</span><span class="sxs-lookup"><span data-stu-id="b5289-136">Unit</span></span>
  - <span data-ttu-id="b5289-137">Unidad de venta</span><span class="sxs-lookup"><span data-stu-id="b5289-137">Unit Group</span></span>
  - <span data-ttu-id="b5289-138">Lista de precios</span><span class="sxs-lookup"><span data-stu-id="b5289-138">Price List</span></span>
  - <span data-ttu-id="b5289-139">Lista de precios de parámetros de proyecto</span><span class="sxs-lookup"><span data-stu-id="b5289-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="b5289-140">Frecuencia de facturación</span><span class="sxs-lookup"><span data-stu-id="b5289-140">Invoice Frequency</span></span>
  - <span data-ttu-id="b5289-141">Categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="b5289-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="b5289-142">Categoría de transacción</span><span class="sxs-lookup"><span data-stu-id="b5289-142">Transaction Category</span></span>
  - <span data-ttu-id="b5289-143">Categoría de gastos</span><span class="sxs-lookup"><span data-stu-id="b5289-143">Expense Category</span></span>
  - <span data-ttu-id="b5289-144">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="b5289-144">Role Price</span></span>
  - <span data-ttu-id="b5289-145">Precio de categoría de transacciones</span><span class="sxs-lookup"><span data-stu-id="b5289-145">Transaction Category Price</span></span>
  - <span data-ttu-id="b5289-146">Característica</span><span class="sxs-lookup"><span data-stu-id="b5289-146">Characteristic</span></span>
  - <span data-ttu-id="b5289-147">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="b5289-147">Bookable Resource</span></span>
  - <span data-ttu-id="b5289-148">Asociación de categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="b5289-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="b5289-149">Característica del recurso reservable</span><span class="sxs-lookup"><span data-stu-id="b5289-149">Bookable Resource Characteristic</span></span>

![Completar importación](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="b5289-151">Actualizar configuraciones de operaciones de proyecto</span><span class="sxs-lookup"><span data-stu-id="b5289-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="b5289-152">Vaya al entorno CE.</span><span class="sxs-lookup"><span data-stu-id="b5289-152">Navigate to the CE environment.</span></span> <span data-ttu-id="b5289-153">Puede encontrarlo abriendo el [Centro de administración de Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionando el entorno y luego seleccionando **Abrir entorno**.</span><span class="sxs-lookup"><span data-stu-id="b5289-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir entorno](./media/7OpenEnvironment.png)

2. <span data-ttu-id="b5289-155">Vaya a **Proyectos** > **Recursos** y luego seleccione **Nuevo** para crear un recurso que se pueda reservar para su usuario.</span><span class="sxs-lookup"><span data-stu-id="b5289-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos que se pueden reservar](./media/8BookableResources.png)

3. <span data-ttu-id="b5289-157">En la pestaña **General**, seleccione su usuario administrador.</span><span class="sxs-lookup"><span data-stu-id="b5289-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="b5289-158">Verifique que la zona horaria coincida con la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="b5289-158">Verify that the time zone matches the one you are in.</span></span> 

![Nuevo recurso reservable](./media/9NewBookableResource.png)

4. <span data-ttu-id="b5289-160">En la pestaña **Planificación** del campo **Empresa**, elija la empresa **USPM** y luego seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="b5289-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Pestaña de programación](./media/10SchedulingTab.png)

5. <span data-ttu-id="b5289-162">Seleccione la pestaña **Horas de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="b5289-162">Select the **Work hours** tab.</span></span>  

![Horas laborables](./media/11WorkHours.png)

6. <span data-ttu-id="b5289-164">Haga doble clic en cualquier valor del calendario y seleccione **Editar** > **Todos los eventos de la serie**.</span><span class="sxs-lookup"><span data-stu-id="b5289-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendario de trabajo](./media/12WorkCalendar.png)

7. <span data-ttu-id="b5289-166">Cambie el horario laboral a un día laborable de ocho (8) horas, marque los fines de semana como días no laborables y asegúrese de que la zona horaria coincida con la suya.</span><span class="sxs-lookup"><span data-stu-id="b5289-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="b5289-167">Seleccione **Guardar y cerrar**.</span><span class="sxs-lookup"><span data-stu-id="b5289-167">Select **Save and close**.</span></span>

![Actualizar calendario](./media/13UpdateCalendar.png)

9. <span data-ttu-id="b5289-169">Vaya a **Configuración** > **Plantillas de calendario** y seleccione **Nueva**.</span><span class="sxs-lookup"><span data-stu-id="b5289-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Plantillas de calendario](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="b5289-171">Introduzca un nombre, seleccione el recurso de plantilla que creó y luego seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="b5289-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Guardar plantilla de calendario](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="b5289-173">Vaya a **Parámetros** y haga doble clic en el registro.</span><span class="sxs-lookup"><span data-stu-id="b5289-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parámetros de proyecto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="b5289-175">Actualice los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="b5289-175">Update the following fields:</span></span>

 - <span data-ttu-id="b5289-176">**Empresa predeterminada**: USPM</span><span class="sxs-lookup"><span data-stu-id="b5289-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="b5289-177">**Unidad organizativa predeterminada**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="b5289-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="b5289-178">**Frecuencia de facturación**: séptimo y último día</span><span class="sxs-lookup"><span data-stu-id="b5289-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="b5289-179">**Plantilla de horas de trabajo**: cambia a la plantilla que creó.</span><span class="sxs-lookup"><span data-stu-id="b5289-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="b5289-180">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="b5289-180">Select **Save**.</span></span> 

![Parámetros de proyecto actualizados](./media/17UpdatedProjectParameters.png)
