---
title: Aplicar datos de configuración y configuración de demostración (lite)
description: Este tema proporciona información sobre cómo aplicar la configuración de demostración y los datos de configuración para las operaciones de proyecto.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642114"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="98b42-103">Aplicar datos de configuración y configuración de demostración para Project Operations (lite)</span><span class="sxs-lookup"><span data-stu-id="98b42-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="98b42-104">_\*\*Implementación simplificada: facturación de oferta a proforma_</span><span class="sxs-lookup"><span data-stu-id="98b42-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="98b42-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="98b42-105">Prerequisites</span></span>

<span data-ttu-id="98b42-106">Antes de comenzar la configuración, debe tener un entorno de Common Data Service (CDS) aprovisionado para Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="98b42-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="98b42-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="98b42-107">Instructions</span></span>

1. <span data-ttu-id="98b42-108">Descargar el [Paquete de datos maestros](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="98b42-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="98b42-109">Navegue a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* y ejecute el archivo ejecutable *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="98b42-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="98b42-110">En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="98b42-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migración de la configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="98b42-112">En la página 2 del asistente CMT, seleccione **Microsoft 365** como **Tipo de implementación**.</span><span class="sxs-lookup"><span data-stu-id="98b42-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="98b42-113">Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="98b42-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="98b42-114">Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="98b42-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="98b42-116">En la página 3, en la lista de organizaciones del inquilino, seleccione a qué organización desea importar los datos de demostración y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="98b42-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="98b42-117">En la página 4, seleccione el archivo zip *MasterAndSetupData* de la carpeta descomprimida *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="98b42-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Archivo Zip](./media/3ZipFile.png)

![Seleccione un archivo](./media/4SelectAFile.png)

9. <span data-ttu-id="98b42-120">Después de seleccionar el archivo zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="98b42-120">After the zip file is selected, select **Import Data**.</span></span>

![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="98b42-122">La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red.</span><span class="sxs-lookup"><span data-stu-id="98b42-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="98b42-123">Una vez finalizada, salga del asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="98b42-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="98b42-124">Compruebe si su organización dispone de datos en las siguientes 20 entidades:</span><span class="sxs-lookup"><span data-stu-id="98b42-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="98b42-125">Moneda</span><span class="sxs-lookup"><span data-stu-id="98b42-125">Currency</span></span>
-   <span data-ttu-id="98b42-126">Cuenta</span><span class="sxs-lookup"><span data-stu-id="98b42-126">Account</span></span>
-   <span data-ttu-id="98b42-127">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="98b42-127">Organizational Unit</span></span>
-   <span data-ttu-id="98b42-128">CONTACTO</span><span class="sxs-lookup"><span data-stu-id="98b42-128">Contact</span></span>
-   <span data-ttu-id="98b42-129">Grupo fiscal</span><span class="sxs-lookup"><span data-stu-id="98b42-129">Tax Group</span></span>
-   <span data-ttu-id="98b42-130">Grupo de clientes</span><span class="sxs-lookup"><span data-stu-id="98b42-130">Customer Group</span></span>
-   <span data-ttu-id="98b42-131">Unidad</span><span class="sxs-lookup"><span data-stu-id="98b42-131">Unit</span></span>
-   <span data-ttu-id="98b42-132">Unidad de venta</span><span class="sxs-lookup"><span data-stu-id="98b42-132">Unit Group</span></span>
-   <span data-ttu-id="98b42-133">Lista de precios</span><span class="sxs-lookup"><span data-stu-id="98b42-133">Price List</span></span>
-   <span data-ttu-id="98b42-134">Lista de precios de parámetros de proyecto</span><span class="sxs-lookup"><span data-stu-id="98b42-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="98b42-135">Frecuencia de facturación</span><span class="sxs-lookup"><span data-stu-id="98b42-135">Invoice Frequency</span></span>
-   <span data-ttu-id="98b42-136">Categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="98b42-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="98b42-137">Categoría de transacción</span><span class="sxs-lookup"><span data-stu-id="98b42-137">Transaction Category</span></span>
-   <span data-ttu-id="98b42-138">Categoría de gastos</span><span class="sxs-lookup"><span data-stu-id="98b42-138">Expense Category</span></span>
-   <span data-ttu-id="98b42-139">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="98b42-139">Role Price</span></span>
-   <span data-ttu-id="98b42-140">Precio de categoría de transacciones</span><span class="sxs-lookup"><span data-stu-id="98b42-140">Transaction Category Price</span></span>
-   <span data-ttu-id="98b42-141">Característica</span><span class="sxs-lookup"><span data-stu-id="98b42-141">Characteristic</span></span>
-   <span data-ttu-id="98b42-142">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="98b42-142">Bookable Resource</span></span>
-   <span data-ttu-id="98b42-143">Asociación de categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="98b42-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="98b42-144">Característica del recurso reservable</span><span class="sxs-lookup"><span data-stu-id="98b42-144">Bookable Resource Characteristic</span></span>

![Completar importación](./media/6CompleteImport.png)
