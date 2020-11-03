---
title: Aplicar datos de configuración y de preparación de demostración
description: Este tema proporciona información sobre cómo aplicar la configuración de demostración y los datos de configuración para las operaciones de proyecto.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085013"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="a0af8-103">Aplique la configuración de demostración y los datos de configuración para la implementación simplificada de Project Operations: facturación de oferta a proforma</span><span class="sxs-lookup"><span data-stu-id="a0af8-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="a0af8-104">_\*\*Implementación simplificada: facturación de oferta a proforma_</span><span class="sxs-lookup"><span data-stu-id="a0af8-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="a0af8-105">Descargar el [Paquete de datos maestros](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="a0af8-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="a0af8-106">Navegue a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* y ejecute el archivo ejecutable *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="a0af8-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a0af8-107">En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="a0af8-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migración de la configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a0af8-109">En la página 2 del asistente CMT, seleccione **Microsoft 365** como **Tipo de implementación**.</span><span class="sxs-lookup"><span data-stu-id="a0af8-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a0af8-110">Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="a0af8-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a0af8-111">Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="a0af8-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a0af8-113">En la página 3, en la lista de organizaciones del inquilino, seleccione a qué organización desea importar los datos de demostración y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="a0af8-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="a0af8-114">En la página 4, seleccione el archivo zip *MasterAndSetupData* de la carpeta descomprimida *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="a0af8-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Archivo Zip](./media/3ZipFile.png)

![Seleccione un archivo](./media/4SelectAFile.png)

9. <span data-ttu-id="a0af8-117">Después de seleccionar el archivo zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="a0af8-117">After the zip file is selected, select **Import Data**.</span></span>

![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="a0af8-119">La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red.</span><span class="sxs-lookup"><span data-stu-id="a0af8-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a0af8-120">Una vez finalizada, salga del asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="a0af8-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a0af8-121">Compruebe si su organización dispone de datos en las siguientes 20 entidades:</span><span class="sxs-lookup"><span data-stu-id="a0af8-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="a0af8-122">Divisa</span><span class="sxs-lookup"><span data-stu-id="a0af8-122">Currency</span></span>
- <span data-ttu-id="a0af8-123">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="a0af8-123">Organizational Unit</span></span>
- <span data-ttu-id="a0af8-124">CONTACTO</span><span class="sxs-lookup"><span data-stu-id="a0af8-124">Contact</span></span>
- <span data-ttu-id="a0af8-125">Grupo fiscal</span><span class="sxs-lookup"><span data-stu-id="a0af8-125">Tax Group</span></span>
- <span data-ttu-id="a0af8-126">Grupo de clientes</span><span class="sxs-lookup"><span data-stu-id="a0af8-126">Customer Group</span></span>
- <span data-ttu-id="a0af8-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="a0af8-127">Unit</span></span>
- <span data-ttu-id="a0af8-128">Unidad de venta</span><span class="sxs-lookup"><span data-stu-id="a0af8-128">Unit Group</span></span>
- <span data-ttu-id="a0af8-129">Lista de precios</span><span class="sxs-lookup"><span data-stu-id="a0af8-129">Price List</span></span>
- <span data-ttu-id="a0af8-130">Lista de precios de parámetros de proyecto</span><span class="sxs-lookup"><span data-stu-id="a0af8-130">Project Parameter Price List</span></span>
- <span data-ttu-id="a0af8-131">Frecuencia de facturación</span><span class="sxs-lookup"><span data-stu-id="a0af8-131">Invoice Frequency</span></span>
- <span data-ttu-id="a0af8-132">Detalle de frecuencia de factura</span><span class="sxs-lookup"><span data-stu-id="a0af8-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="a0af8-133">Categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="a0af8-133">Bookable Resource Category</span></span>
- <span data-ttu-id="a0af8-134">Categoría de transacción</span><span class="sxs-lookup"><span data-stu-id="a0af8-134">Transaction Category</span></span>
- <span data-ttu-id="a0af8-135">Categoría de gastos</span><span class="sxs-lookup"><span data-stu-id="a0af8-135">Expense Category</span></span>
- <span data-ttu-id="a0af8-136">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="a0af8-136">Role Price</span></span>
- <span data-ttu-id="a0af8-137">Precio de categoría de transacciones</span><span class="sxs-lookup"><span data-stu-id="a0af8-137">Transaction Category Price</span></span>
- <span data-ttu-id="a0af8-138">Característica</span><span class="sxs-lookup"><span data-stu-id="a0af8-138">Characteristic</span></span>
- <span data-ttu-id="a0af8-139">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="a0af8-139">Bookable Resource</span></span>
- <span data-ttu-id="a0af8-140">Asociación de categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="a0af8-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="a0af8-141">Característica del recurso reservable</span><span class="sxs-lookup"><span data-stu-id="a0af8-141">Bookable Resource Characteristic</span></span>

![Completar importación](./media/6CompleteImport.png)
