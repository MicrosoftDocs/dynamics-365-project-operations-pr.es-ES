---
title: Creación de entrada de tiempo
description: En este tema se proporciona información sobre cómo crear entradas de tiempo.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999287"
---
# <a name="create-time-entries"></a><span data-ttu-id="3a89d-103">Creación de entrada de tiempo</span><span class="sxs-lookup"><span data-stu-id="3a89d-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3a89d-104">En versiones anteriores de Dynamics 365 Project Service Automation, las entradas de tiempo se introducían semanalmente.</span><span class="sxs-lookup"><span data-stu-id="3a89d-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="3a89d-105">En la versión 3 de Project Service Automation, las entradas de tiempo se introducen diariamente.</span><span class="sxs-lookup"><span data-stu-id="3a89d-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="3a89d-106">Sin embargo, después de que se hayan creado algunas entradas de tiempo, puede crearlas o copiarlas de forma masiva.</span><span class="sxs-lookup"><span data-stu-id="3a89d-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="3a89d-107">Creación de una entrada de tiempo</span><span class="sxs-lookup"><span data-stu-id="3a89d-107">Create a time entry</span></span>

<span data-ttu-id="3a89d-108">Siga estos pasos para crear una entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a89d-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="3a89d-109">En la página **Entradas de tiempo**, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="3a89d-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="3a89d-110">En el cuadro de diálogo **Creación rápida: entrada de tiempo**, escriba la duración de la entrada de tiempo en minutos, horas o días.</span><span class="sxs-lookup"><span data-stu-id="3a89d-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="3a89d-111">La duración se debe especificar en el siguiente formato: *x* minutos, *x* horas o *x* días.</span><span class="sxs-lookup"><span data-stu-id="3a89d-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="3a89d-112">Las horas y los días también se pueden introducir como valores decimales, como *x,x* horas o *x,x* días.</span><span class="sxs-lookup"><span data-stu-id="3a89d-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="3a89d-113">Seleccione el tipo de entrada de tiempo y el proyecto para el que está introduciendo la entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a89d-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="3a89d-114">En el campo **Tarea de proyecto**, busque la tarea para esta entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a89d-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a89d-115">Si está creando una entrada de tiempo para una tarea no asignada a un usuario en el campo **Tarea de proyecto**, seleccione el botón **Buscar**, seleccione **Cambiar vista** y, a continuación, seleccione **Todas las tareas de proyecto activas** para ver todas las tareas.</span><span class="sxs-lookup"><span data-stu-id="3a89d-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="3a89d-116">Introduzca una descripción, si se requiere una descripción, y, a continuación, seleccione **Guardar y cerrar**.</span><span class="sxs-lookup"><span data-stu-id="3a89d-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="3a89d-117">Después de crear y guardar la entrada de tiempo, puede editarla en la cuadrícula de entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a89d-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="3a89d-118">La cuadrícula de entrada de tiempo admite dos formatos:</span><span class="sxs-lookup"><span data-stu-id="3a89d-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="3a89d-119">Puede introducir entradas de tiempo en formato **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="3a89d-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="3a89d-120">Este formato se convierte a horas y fracciones.</span><span class="sxs-lookup"><span data-stu-id="3a89d-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="3a89d-121">Puede introducir horas y fracciones directamente.</span><span class="sxs-lookup"><span data-stu-id="3a89d-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="3a89d-122">Tenga en cuenta que las fracciones de una hora no son minutos.</span><span class="sxs-lookup"><span data-stu-id="3a89d-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="3a89d-123">Por lo tanto, 1,5 horas representan 1 hora y 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="3a89d-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="3a89d-124">La misma regla se aplica a las fracciones de un día.</span><span class="sxs-lookup"><span data-stu-id="3a89d-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="3a89d-125">Un día son 24 horas, y 0,5 días representan 12 horas.</span><span class="sxs-lookup"><span data-stu-id="3a89d-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="3a89d-126">Creación de entrada de tiempo de forma masiva</span><span class="sxs-lookup"><span data-stu-id="3a89d-126">Bulk create time entries</span></span>

<span data-ttu-id="3a89d-127">Después de que se hayan creado algunas entradas de tiempo, puede copiarlas para crear entradas de tiempo adicionales de forma masiva.</span><span class="sxs-lookup"><span data-stu-id="3a89d-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="3a89d-128">En la página **Entradas de tiempo**, seleccione **Copiar semana**.</span><span class="sxs-lookup"><span data-stu-id="3a89d-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="3a89d-129">En el grupo de campos **Desde el período**, en los campos **Fecha de inicio** y **Fecha de finalización**, defina el rango de fechas desde el que copiar las entradas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a89d-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="3a89d-130">En el grupo de campos **Hasta el período**, en el campo **Fecha de inicio**, especifique la fecha para la que crear entradas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a89d-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="3a89d-131">Seleccione **Copiar** para crear una copia de las entradas de tiempo que corresponden al día de la semana que se especifica en el grupo de campos **Hasta el período**.</span><span class="sxs-lookup"><span data-stu-id="3a89d-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="3a89d-132">Por ejemplo, la entrada de tiempo para el lunes de la semana pasada se copia al lunes de la semana que se especifica en el grupo de campos **Hasta el período**.</span><span class="sxs-lookup"><span data-stu-id="3a89d-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="3a89d-133">Importación de datos para entradas de tiempo</span><span class="sxs-lookup"><span data-stu-id="3a89d-133">Import data for time entries</span></span>

<span data-ttu-id="3a89d-134">Puede importar datos de reservas y asignaciones de proyectos.</span><span class="sxs-lookup"><span data-stu-id="3a89d-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="3a89d-135">Cuando importe datos, puede especificar el rango de fechas de las reservas para importar y, a continuación, seleccionar explícitamente las reservas que se deben crear como entradas de hora de **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="3a89d-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="3a89d-136">Capacidades de agrupación, ordenación, búsqueda y filtrado</span><span class="sxs-lookup"><span data-stu-id="3a89d-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="3a89d-137">Puede agrupar y filtrar las entradas de tiempo por las dimensiones que se especifican en las columnas.</span><span class="sxs-lookup"><span data-stu-id="3a89d-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="3a89d-138">En el campo **Agrupar por**, seleccione la dimensión que se usará para filtrar las entradas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a89d-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="3a89d-139">También puede ordenar los registros de entrada de tiempo en orden ascendente o descendente mediante la flecha de ordenación en los encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="3a89d-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="3a89d-140">Además, puede mostrar u ocultar entradas seleccionando el botón **Filtrar** en los encabezados de las columnas y, a continuación, en el cuadro **Buscar** introduciendo el texto que se debe usar para buscar entradas de tiempo por nombre de proyecto, tarea de proyecto, entrada de tiempo o recurso.</span><span class="sxs-lookup"><span data-stu-id="3a89d-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]