---
title: Consulta sobre el programa de gastos de las adjudicaciones federales
description: Este tema proporciona información sobre la consulta sobre el Programa de gastos de las adjudicaciones federales.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085132"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b99b6-103">Consulta sobre el programa de gastos de las adjudicaciones federales</span><span class="sxs-lookup"><span data-stu-id="b99b6-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b99b6-104">Según la Circular A-133 de la Oficina de Gestión y Presupuestos, las agencias que reciben fondos federales están sujetas a requisitos de auditoría, que también se conocen como auditorías únicas.</span><span class="sxs-lookup"><span data-stu-id="b99b6-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="b99b6-105">El proceso de auditoría se utiliza para informar sobre los ingresos y gastos de las subvenciones federales de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="b99b6-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="b99b6-106">Parte del informe de auditoría único incluye el Programa de gastos de las adjudicaciones federales (SEFA).</span><span class="sxs-lookup"><span data-stu-id="b99b6-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="b99b6-107">La consulta del Programa de gastos de las subvenciones federales incluye el título y número del Catálogo de asistencia doméstica federal (CFDA), el número de la subvención, el año de la subvención, el nombre de la agencia federal que proporciona los fondos y el nombre de la entidad de paso.</span><span class="sxs-lookup"><span data-stu-id="b99b6-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="b99b6-108">La consulta es por un período específico.</span><span class="sxs-lookup"><span data-stu-id="b99b6-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="b99b6-109">Normalmente, ese período es el mismo que el período del estado financiero, que es un año fiscal.</span><span class="sxs-lookup"><span data-stu-id="b99b6-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="b99b6-110">La consulta incluye subvenciones que tienen fechas de proyección en el rango de fechas seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b99b6-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="b99b6-111">La columna **Agencia concesionaria** de la consulta muestra el cliente de la concesión o, para una concesión de transferencia, la agencia concesionaria.</span><span class="sxs-lookup"><span data-stu-id="b99b6-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="b99b6-112">Para una concesión de transferencia, la columna **Agencia concesionaria** muestra el cliente de la concesión.</span><span class="sxs-lookup"><span data-stu-id="b99b6-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="b99b6-113">Si la concesión no es una concesión de transferencia, la columna **Agencia concesionaria** está en blanco.</span><span class="sxs-lookup"><span data-stu-id="b99b6-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="b99b6-114">Configuración de los grupos CFDA</span><span class="sxs-lookup"><span data-stu-id="b99b6-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="b99b6-115">Debe configurar los grupos de CFDA que se pueden asociar con los números de CFDA en la consulta de Lista de gastos de adjudicaciones federales.</span><span class="sxs-lookup"><span data-stu-id="b99b6-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="b99b6-116">Vaya a **Gestión de proyectos y contabilidad \> Configuración \> Concesiones \> Catálogo de grupos de Asistencia Doméstica Federal**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="b99b6-117">Para crear un clúster CFDA seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="b99b6-118">Especifique el nombre del clúster.</span><span class="sxs-lookup"><span data-stu-id="b99b6-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="b99b6-119">Seleccione **Guardar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b99b6-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="b99b6-120">Configurar números CFDA</span><span class="sxs-lookup"><span data-stu-id="b99b6-120">Set up CFDA numbers</span></span>

<span data-ttu-id="b99b6-121">Debe configurar los números de CFDA que se pueden agregar a las concesiones y se incluyen en la consulta de Lista de gastos de adjudicaciones federales.</span><span class="sxs-lookup"><span data-stu-id="b99b6-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="b99b6-122">Vaya a **Gestión de proyectos y contabilidad \> Configuración \> Concesiones \> Catálogo de números de Asistencia Doméstica Federal**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="b99b6-123">Seleccione **Nuevo** para crear un número CFDA.</span><span class="sxs-lookup"><span data-stu-id="b99b6-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="b99b6-124">En la columna **Número** , especifique el número CFDA.</span><span class="sxs-lookup"><span data-stu-id="b99b6-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="b99b6-125">Presione la tecla **Tabulador**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="b99b6-126">En la columna **Descripción** , introduzca el título CFDA.</span><span class="sxs-lookup"><span data-stu-id="b99b6-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="b99b6-127">Presione la tecla **Tabulador**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="b99b6-128">Opcional: en el campo **Clúster de programas** , agregue el clúster CFDA apropiado.</span><span class="sxs-lookup"><span data-stu-id="b99b6-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="b99b6-129">Seleccione **Guardar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b99b6-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b99b6-130">Configurar subvenciones para informar para la consulta del Programa de gastos de las subvenciones federales</span><span class="sxs-lookup"><span data-stu-id="b99b6-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="b99b6-131">Vaya a **Gestión de proyectos y contabilidad \> Concesiones \> Concesiones** y seleccione una concesión existente.</span><span class="sxs-lookup"><span data-stu-id="b99b6-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="b99b6-132">En la ficha desplegable **Configuración** , en el campo **Catálogo de Asistencia Doméstica Federal** , asigne el número CFDA.</span><span class="sxs-lookup"><span data-stu-id="b99b6-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="b99b6-133">El número de CFDA en la concesión determina el clúster de CFDA para informar.</span><span class="sxs-lookup"><span data-stu-id="b99b6-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="b99b6-134">En la ficha desplegable **Información del contacto** , introduzca la información del otorgante siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="b99b6-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="b99b6-135">En el campo **Cliente de concesión** , introduzca el cliente responsable de la subvención.</span><span class="sxs-lookup"><span data-stu-id="b99b6-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="b99b6-136">Para una subvención existente, es posible que esta información ya esté ingresada.</span><span class="sxs-lookup"><span data-stu-id="b99b6-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="b99b6-137">Indique si el cliente de la concesión es el financiador.</span><span class="sxs-lookup"><span data-stu-id="b99b6-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="b99b6-138">Si el cliente de la concesión es el financiador, deje la casilla de verificación **Pasar por** desactivada.</span><span class="sxs-lookup"><span data-stu-id="b99b6-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="b99b6-139">Si otro cliente es el financiador y el cliente de la concesión es responsable de gastar y seguir el dinero, seleccione la casilla de verificación **Pasar por**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="b99b6-140">Si seleccionó la casilla de verificación **Pasar por** en el paso anterior, en el campo **Agencia otorgante** introduzca el cliente que proporcionó la concesión.</span><span class="sxs-lookup"><span data-stu-id="b99b6-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="b99b6-141">La agencia otorgante y el cliente de la concesión no pueden ser el mismo cliente.</span><span class="sxs-lookup"><span data-stu-id="b99b6-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="b99b6-142">A continuación, se muestra un ejemplo de una concesión de transferencia:</span><span class="sxs-lookup"><span data-stu-id="b99b6-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="b99b6-143">El gobierno federal financió un proyecto de infraestructura para un estado.</span><span class="sxs-lookup"><span data-stu-id="b99b6-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="b99b6-144">El gobierno federal entregó el dinero al estado para que lo gastara.</span><span class="sxs-lookup"><span data-stu-id="b99b6-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="b99b6-145">En este caso, el gobierno federal es la agencia otorgante y el estado es el cliente de la concesión.</span><span class="sxs-lookup"><span data-stu-id="b99b6-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="b99b6-146">Cuando active la función por primera vez, los números CFDA iniciales se ingresarán utilizando los números existentes en las subvenciones.</span><span class="sxs-lookup"><span data-stu-id="b99b6-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="b99b6-147">Excluir las subvenciones de los informes SEFA según el tipo de subvención</span><span class="sxs-lookup"><span data-stu-id="b99b6-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="b99b6-148">Vaya a **Gestión de proyectos y contabilidad \> Configurar \> Concesiones \> Tipos de concesiones**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="b99b6-149">En la ficha desplegable **Información predeterminada** , seleccione la casilla de verificación **Excluir de la Lista de gastos de las adjudicaciones federales**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="b99b6-150">Seleccione **Guardar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b99b6-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b99b6-151">Ejecute la consulta del programa de gastos de las adjudicaciones federales</span><span class="sxs-lookup"><span data-stu-id="b99b6-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="b99b6-152">Vaya a **Gestión de proyectos y contabilidad \> Consultas e informes \> Solicitud de concesión \> Lista de gastos de las adjudicaciones federales**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="b99b6-153">En la sección **Parámetros** siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="b99b6-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="b99b6-154">En campo **Intervalo de fechas** , seleccione el código para el intervalo de fechas.</span><span class="sxs-lookup"><span data-stu-id="b99b6-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="b99b6-155">Alternativamente, en los campos **Desde fecha** y **Hasta fecha** , defina el intervalo de fechas.</span><span class="sxs-lookup"><span data-stu-id="b99b6-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="b99b6-156">Opcional: para incluir solo las transacciones facturadas como ingresos en la consulta, establezca la opción **Incluir solo los ingresos facturados** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="b99b6-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="b99b6-157">Columnas</span><span class="sxs-lookup"><span data-stu-id="b99b6-157">Columns</span></span>

<span data-ttu-id="b99b6-158">La consulta de Lista de gastos de adjudicaciones federales incluye las siguientes columnas:</span><span class="sxs-lookup"><span data-stu-id="b99b6-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="b99b6-159">Catálogo de nombre del grupo de Asistencia Doméstica Federal</span><span class="sxs-lookup"><span data-stu-id="b99b6-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="b99b6-160">Agencia otorgante</span><span class="sxs-lookup"><span data-stu-id="b99b6-160">Grantor agency</span></span>
- <span data-ttu-id="b99b6-161">Agencia de paso</span><span class="sxs-lookup"><span data-stu-id="b99b6-161">Pass-through agency</span></span>
- <span data-ttu-id="b99b6-162">Nombre de la concesión</span><span class="sxs-lookup"><span data-stu-id="b99b6-162">Grant name</span></span>
- <span data-ttu-id="b99b6-163">ID de concesión</span><span class="sxs-lookup"><span data-stu-id="b99b6-163">Grant ID</span></span>
- <span data-ttu-id="b99b6-164">Identificador de aplicación de concesión</span><span class="sxs-lookup"><span data-stu-id="b99b6-164">Grant application ID</span></span>
- <span data-ttu-id="b99b6-165">Catálogo de Asistencia Doméstica Federal</span><span class="sxs-lookup"><span data-stu-id="b99b6-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="b99b6-166">Recibos</span><span class="sxs-lookup"><span data-stu-id="b99b6-166">Receipts</span></span>
- <span data-ttu-id="b99b6-167">Gastos</span><span class="sxs-lookup"><span data-stu-id="b99b6-167">Expenditures</span></span>
