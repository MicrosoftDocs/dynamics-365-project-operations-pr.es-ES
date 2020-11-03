---
title: Configurar la facturación de proyectos de empresas vinculadas
description: Este tema muestra cómo configurar la facturación de proyectos entre dos empresas de su organización.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085207"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="bb84d-103">Configurar la facturación de proyectos de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="bb84d-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb84d-104">Este tema muestra cómo configurar la facturación de proyectos entre dos empresas de su organización.</span><span class="sxs-lookup"><span data-stu-id="bb84d-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="bb84d-105">Esta tarea utiliza el conjunto de datos de USSI.</span><span class="sxs-lookup"><span data-stu-id="bb84d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="bb84d-106">En el panel de navegación, vaya a **Módulos > Proveedores > Proveedores > Todos los proveedores**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="bb84d-107">En la lista **Todos los proveedores** , busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="bb84d-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="bb84d-108">En el Panel de acciones, seleccione **General**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="bb84d-109">Seleccione **Empresas vinculadas**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="bb84d-110">Establezca **Activo** en **Sí** para permitir el comercio entre empresas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="bb84d-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="bb84d-111">En el campo **Empresa de cliente** , introduzca o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="bb84d-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="bb84d-112">En el campo **Mi cuenta** , introduzca o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="bb84d-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="bb84d-113">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-113">Select **Save**.</span></span>
9. <span data-ttu-id="bb84d-114">Cierre las páginas para volver a la página de inicio.</span><span class="sxs-lookup"><span data-stu-id="bb84d-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="bb84d-115">En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Gestión de proyectos y parámetros contables**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="bb84d-116">Seleccione la ficha **Empresas vinculadas**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="bb84d-117">Mueva el control deslizante a **Sí** para habilitar la programación de recursos y los partes de horas de empresas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="bb84d-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="bb84d-118">En la lista, marque la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="bb84d-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="bb84d-119">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-119">Select **New**.</span></span>
15. <span data-ttu-id="bb84d-120">En el campo **Tomar prestada entidad jurídica** , escriba o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="bb84d-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="bb84d-121">Active la casilla **Acumular ingresos**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="bb84d-122">En el campo **Categoría de hoja de horas predeterminada** , escriba o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="bb84d-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="bb84d-123">En el campo **Categoría de gasto predeterminada** , escriba o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="bb84d-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="bb84d-124">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-124">Select **Save**.</span></span>
20. <span data-ttu-id="bb84d-125">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="bb84d-125">Close the page.</span></span>
21. <span data-ttu-id="bb84d-126">En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Registro > Configuración de registro de libro mayor**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="bb84d-127">En el campo **Tipos de cuenta contable** , seleccione una opción.</span><span class="sxs-lookup"><span data-stu-id="bb84d-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="bb84d-128">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-128">Select **New**.</span></span>
24. <span data-ttu-id="bb84d-129">En el campo **Cuenta principal** de la nueva fila, especifique los valores que desee.</span><span class="sxs-lookup"><span data-stu-id="bb84d-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="bb84d-130">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-130">Select **Save**.</span></span>
26. <span data-ttu-id="bb84d-131">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="bb84d-131">Close the page.</span></span>
27. <span data-ttu-id="bb84d-132">En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de transferencia**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="bb84d-133">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-133">Select **New**.</span></span>
29. <span data-ttu-id="bb84d-134">En el campo **Fecha de vigencia** , especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="bb84d-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="bb84d-135">En el campo **Tomar prestada entidad jurídica** , escriba o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="bb84d-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="bb84d-136">En el campo **Modelo de precio de transferencia** , seleccione una opción.</span><span class="sxs-lookup"><span data-stu-id="bb84d-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="bb84d-137">En el campo **Precio** , especifique un número.</span><span class="sxs-lookup"><span data-stu-id="bb84d-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="bb84d-138">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bb84d-138">Select **Save**.</span></span>

