---
title: Rendimiento de la programación de recursos del proyecto
description: Este tema proporciona información sobre cómo mejorar el rendimiento de la programación de recursos para una gran cantidad de proyectos.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010042"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="8d5d9-103">Rendimiento de la programación de recursos del proyecto</span><span class="sxs-lookup"><span data-stu-id="8d5d9-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="8d5d9-104">Los problemas de rendimiento relacionados con la programación de recursos pueden ocurrir cuando el número de proyectos llega a miles.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="8d5d9-105">Para mejorar el rendimiento de la programación de recursos, hay una función disponible que permite a los usuarios reducir el tiempo que lleva iniciar el formulario de disponibilidad de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="8d5d9-106">Específicamente, esto elimina el proceso de sincronización de acumulación de capacidad de recursos y utiliza la tabla **ResProjectResource** para acelerar la búsqueda de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="8d5d9-107">Tenga en cuenta que la tabla **ResRollup** ya no se utilizará.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d5d9-108">Si existe una dependencia del proceso de sincronización de acumulación de capacidad de recursos o de la tabla **ResProjectResource**, no utilice esta función.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="8d5d9-109">Habilite la mejora del rendimiento de la programación de recursos</span><span class="sxs-lookup"><span data-stu-id="8d5d9-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="8d5d9-110">Para habilitar la mejora del rendimiento de la programación de recursos, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="8d5d9-111">Vaya a **Gestión de funciones** > **Todos** y en la lista de funciones, ubique **Habilitar la función de mejora del rendimiento de la programación de recursos del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="8d5d9-112">Seleccione **Habilitar ahora**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="8d5d9-113">Si no puede encontrar la función en la lista, seleccione **Buscar actualizaciones** para actualizar la lista.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="8d5d9-114">Actualice su navegador y luego vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Recursos del proyecto** > **Sincronizar la capacidad de los calendarios de recursos en todas las empresas**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="8d5d9-115">Establezca **Eliminar registros de capacidad existentes** a **Sí** para eliminar los datos anteriores.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="8d5d9-116">Si desea generar datos incrementales, configúrelo en **No**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="8d5d9-117">En el campo **Código de período**, seleccione el período en el que se deben generar los datos.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="8d5d9-118">Si selecciona un código de período, no es necesario definir una fecha de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="8d5d9-119">Si deja el campo **Código de período** en blanco, seleccione fechas de inicio y finalización específicas para generar datos.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="8d5d9-120">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="8d5d9-121">Esto distribuirá datos generales a la tabla **ResCalendarCapacity** en todas las empresas de su entorno, por lo que el trabajo por lotes solo debe ejecutarse en una entidad legal.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="8d5d9-122">Los datos de este trabajo por lotes son necesarios para calcular la capacidad de recursos a través del calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="8d5d9-123">Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Recursos del proyecto** > **Completar los recursos del proyecto en todas las empresas** y luego seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="8d5d9-124">Este es el script de actualización de datos para datos generales en las tablas **ResProjectResource**, **ResCalendarDateTimeRange** y **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="8d5d9-125">Los valores para el campo **PSAPRojSchedRole.RootActivity** también se actualizan.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="8d5d9-126">Si no se ejecuta, recibirá una advertencia cuando intente ejecutar operaciones de programación de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="8d5d9-127">Desactive la mejora del rendimiento de la programación de recursos</span><span class="sxs-lookup"><span data-stu-id="8d5d9-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="8d5d9-128">Vaya a **Gestión de funciones** > **Todos** y busque **Habilitar la función de mejora del rendimiento de la programación de recursos del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="8d5d9-129">Seleccione la función y luego seleccione el botón **Deshabilitar**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="8d5d9-130">Actualice el explorador.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-130">Refresh your browser.</span></span>
4. <span data-ttu-id="8d5d9-131">Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Sincronización de capacidad** > **Sincronizar acumulaciones de capacidad de recurso**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="8d5d9-132">En la página **Sincronización de acumulación de capacidad**, establezca **Eliminar registros de capacidad existentes** a **Sí** para eliminar los datos anteriores.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="8d5d9-133">Si desea generar datos incrementales, configúrelo en **No**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="8d5d9-134">En el campo **Código de período**, seleccione el período en el que se deben generar los datos.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="8d5d9-135">Si selecciona un código de período, no es necesario definir una fecha de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="8d5d9-136">Si deja el campo **Código de período** en blanco, seleccione fechas de inicio y finalización específicas para generar datos.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="8d5d9-137">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="8d5d9-138">Esto distribuirá datos generales a la tabla **ResRollup** en todas las empresas de su entorno, por lo que el trabajo por lotes solo debe ejecutarse en una entidad legal.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="8d5d9-139">Este trabajo por lotes es necesario para todas las vistas **Disponibilidad de recursos**.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="8d5d9-140">Si este trabajo por lotes no se ejecuta, los datos de **ResRollup** se generarán sobre la marcha, lo que puede llevar tiempo.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]