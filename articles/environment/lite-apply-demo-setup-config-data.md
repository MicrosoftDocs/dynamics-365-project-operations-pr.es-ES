---
title: Aplicar datos de configuración y configuración de demostración (lite)
description: Este tema proporciona información sobre cómo aplicar la configuración de demostración y los datos de configuración para las operaciones de proyecto.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089140"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="90c55-103">Aplicar datos de configuración y configuración de demostración para Project Operations (lite)</span><span class="sxs-lookup"><span data-stu-id="90c55-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="90c55-104">_\*\*Implementación simplificada: facturación de oferta a proforma_</span><span class="sxs-lookup"><span data-stu-id="90c55-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="90c55-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="90c55-105">Prerequisites</span></span>

<span data-ttu-id="90c55-106">Antes de comenzar la configuración, debe tener un entorno de Common Data Service (CDS) aprovisionado para Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="90c55-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="90c55-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="90c55-107">Instructions</span></span>

1. <span data-ttu-id="90c55-108">Descargar el [Paquete de datos maestros](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="90c55-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="90c55-109">Navegue a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* y ejecute el archivo ejecutable *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="90c55-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="90c55-110">En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="90c55-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migración de la configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="90c55-112">En la página 2 del asistente CMT, seleccione **Microsoft 365** como **Tipo de implementación**.</span><span class="sxs-lookup"><span data-stu-id="90c55-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="90c55-113">Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="90c55-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="90c55-114">Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="90c55-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="90c55-116">En la página 3, en la lista de organizaciones del inquilino, seleccione a qué organización desea importar los datos de demostración y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="90c55-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="90c55-117">En la página 4, seleccione el archivo zip *MasterAndSetupData* de la carpeta descomprimida *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="90c55-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Archivo Zip](./media/3ZipFile.png)

   ![Seleccione un archivo](./media/4SelectAFile.png)

9. <span data-ttu-id="90c55-120">Después de seleccionar el archivo zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="90c55-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="90c55-122">La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red.</span><span class="sxs-lookup"><span data-stu-id="90c55-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="90c55-123">Una vez finalizada, salga del asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="90c55-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="90c55-124">Compruebe si su organización dispone de datos en las siguientes 20 entidades:</span><span class="sxs-lookup"><span data-stu-id="90c55-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="90c55-125">Moneda</span><span class="sxs-lookup"><span data-stu-id="90c55-125">Currency</span></span>
    -   <span data-ttu-id="90c55-126">Cuenta</span><span class="sxs-lookup"><span data-stu-id="90c55-126">Account</span></span>
    -   <span data-ttu-id="90c55-127">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="90c55-127">Organizational Unit</span></span>
    -   <span data-ttu-id="90c55-128">CONTACTO</span><span class="sxs-lookup"><span data-stu-id="90c55-128">Contact</span></span>
    -   <span data-ttu-id="90c55-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="90c55-129">Unit</span></span>
    -   <span data-ttu-id="90c55-130">Unidad de venta</span><span class="sxs-lookup"><span data-stu-id="90c55-130">Unit Group</span></span>
    -   <span data-ttu-id="90c55-131">Lista de precios</span><span class="sxs-lookup"><span data-stu-id="90c55-131">Price List</span></span>
    -   <span data-ttu-id="90c55-132">Lista de precios de parámetros de proyecto</span><span class="sxs-lookup"><span data-stu-id="90c55-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="90c55-133">Frecuencia de facturación</span><span class="sxs-lookup"><span data-stu-id="90c55-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="90c55-134">Categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="90c55-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="90c55-135">Categoría de transacción</span><span class="sxs-lookup"><span data-stu-id="90c55-135">Transaction Category</span></span>
    -   <span data-ttu-id="90c55-136">Categoría de gastos</span><span class="sxs-lookup"><span data-stu-id="90c55-136">Expense Category</span></span>
    -   <span data-ttu-id="90c55-137">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="90c55-137">Role Price</span></span>
    -   <span data-ttu-id="90c55-138">Precio de categoría de transacciones</span><span class="sxs-lookup"><span data-stu-id="90c55-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="90c55-139">Característica</span><span class="sxs-lookup"><span data-stu-id="90c55-139">Characteristic</span></span>
    -   <span data-ttu-id="90c55-140">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="90c55-140">Bookable Resource</span></span>
    -   <span data-ttu-id="90c55-141">Asociación de categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="90c55-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="90c55-142">Característica del recurso reservable</span><span class="sxs-lookup"><span data-stu-id="90c55-142">Bookable Resource Characteristic</span></span>

    ![Completar importación](./media/6CompleteImport.png)
