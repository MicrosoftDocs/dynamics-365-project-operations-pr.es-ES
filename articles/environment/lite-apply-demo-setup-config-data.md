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
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949087"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="d6707-103">Aplique la configuración de demostración y los datos de configuración para la implementación simplificada de Project Operations: facturación de oferta a proforma</span><span class="sxs-lookup"><span data-stu-id="d6707-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="d6707-104">_\*\*Implementación simplificada: facturación de oferta a proforma_</span><span class="sxs-lookup"><span data-stu-id="d6707-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="d6707-105">Descargar el [Paquete de datos maestros](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="d6707-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="d6707-106">Navegue a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* y ejecute el archivo ejecutable *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d6707-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d6707-107">En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="d6707-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migración de la configuración](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d6707-109">En la página 2 del asistente CMT, seleccione **Office 365** como **Tipo de implementación**.</span><span class="sxs-lookup"><span data-stu-id="d6707-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d6707-110">Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="d6707-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d6707-111">Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="d6707-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d6707-113">En la página 3, en la lista de organizaciones del inquilino, seleccione a qué organización desea importar los datos de demostración y luego seleccione **Iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="d6707-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="d6707-114">En la página 4, seleccione el archivo zip *MasterAndSetupData* de la carpeta descomprimida *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="d6707-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Archivo Zip](./media/3ZipFile.png)

![Seleccione un archivo](./media/4SelectAFile.png)

9. <span data-ttu-id="d6707-117">Después de seleccionar el archivo zip, seleccione **Importar datos**.</span><span class="sxs-lookup"><span data-stu-id="d6707-117">After the zip file is selected, select **Import Data**.</span></span>

![Importar datos](./media/5ImportData.png)

10. <span data-ttu-id="d6707-119">La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red.</span><span class="sxs-lookup"><span data-stu-id="d6707-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d6707-120">Una vez finalizada, salga del asistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="d6707-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d6707-121">Compruebe si su organización dispone de datos en las siguientes 20 entidades:</span><span class="sxs-lookup"><span data-stu-id="d6707-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="d6707-122">Divisa</span><span class="sxs-lookup"><span data-stu-id="d6707-122">Currency</span></span>
- <span data-ttu-id="d6707-123">Unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="d6707-123">Organizational Unit</span></span>
- <span data-ttu-id="d6707-124">CONTACTO</span><span class="sxs-lookup"><span data-stu-id="d6707-124">Contact</span></span>
- <span data-ttu-id="d6707-125">Grupo fiscal</span><span class="sxs-lookup"><span data-stu-id="d6707-125">Tax Group</span></span>
- <span data-ttu-id="d6707-126">Grupo de clientes</span><span class="sxs-lookup"><span data-stu-id="d6707-126">Customer Group</span></span>
- <span data-ttu-id="d6707-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="d6707-127">Unit</span></span>
- <span data-ttu-id="d6707-128">Unidad de venta</span><span class="sxs-lookup"><span data-stu-id="d6707-128">Unit Group</span></span>
- <span data-ttu-id="d6707-129">Lista de precios</span><span class="sxs-lookup"><span data-stu-id="d6707-129">Price List</span></span>
- <span data-ttu-id="d6707-130">Lista de precios de parámetros de proyecto</span><span class="sxs-lookup"><span data-stu-id="d6707-130">Project Parameter Price List</span></span>
- <span data-ttu-id="d6707-131">Frecuencia de facturación</span><span class="sxs-lookup"><span data-stu-id="d6707-131">Invoice Frequency</span></span>
- <span data-ttu-id="d6707-132">Detalle de frecuencia de factura</span><span class="sxs-lookup"><span data-stu-id="d6707-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="d6707-133">Categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="d6707-133">Bookable Resource Category</span></span>
- <span data-ttu-id="d6707-134">Categoría de transacción</span><span class="sxs-lookup"><span data-stu-id="d6707-134">Transaction Category</span></span>
- <span data-ttu-id="d6707-135">Categoría de gastos</span><span class="sxs-lookup"><span data-stu-id="d6707-135">Expense Category</span></span>
- <span data-ttu-id="d6707-136">Precio de rol</span><span class="sxs-lookup"><span data-stu-id="d6707-136">Role Price</span></span>
- <span data-ttu-id="d6707-137">Precio de categoría de transacciones</span><span class="sxs-lookup"><span data-stu-id="d6707-137">Transaction Category Price</span></span>
- <span data-ttu-id="d6707-138">Característica</span><span class="sxs-lookup"><span data-stu-id="d6707-138">Characteristic</span></span>
- <span data-ttu-id="d6707-139">Recurso reservable</span><span class="sxs-lookup"><span data-stu-id="d6707-139">Bookable Resource</span></span>
- <span data-ttu-id="d6707-140">Asociación de categoría de recurso reservable</span><span class="sxs-lookup"><span data-stu-id="d6707-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="d6707-141">Característica del recurso reservable</span><span class="sxs-lookup"><span data-stu-id="d6707-141">Bookable Resource Characteristic</span></span>

![Completar importación](./media/6CompleteImport.png)
