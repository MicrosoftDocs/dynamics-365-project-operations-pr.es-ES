---
title: Configurar costos estándar para mano de obra y gastos
description: Este tema explica cómo configurar los costos estándar de mano de obra y gastos para un proyecto.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 517e5ae776cff18aec81e5446a7aaedfba61ac0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011032"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="bb4cb-103">Configurar costos estándar para mano de obra y gastos</span><span class="sxs-lookup"><span data-stu-id="bb4cb-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb4cb-104">Este tema explica cómo configurar los costos estándar de mano de obra y gastos para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="bb4cb-105">Esta tarea utiliza el conjunto de datos de USSI.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="bb4cb-106">En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de coste (hora)**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="bb4cb-107">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-107">Select **New**.</span></span>
3. <span data-ttu-id="bb4cb-108">En el campo **Fecha de vigencia**, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="bb4cb-109">En el campo **Precio de coste**, introduzca un número.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="bb4cb-110">Puede configurar un precio de coste estándar para la categoría de proyecto, o puede configurar un precio de coste por número de trabajador, número de proyecto, categoría, fecha o cualquier combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="bb4cb-111">El precio de coste que se aplica es el precio de coste con el mayor nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="bb4cb-112">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-112">Select **Save**.</span></span>
6. <span data-ttu-id="bb4cb-113">En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de venta (hora)**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="bb4cb-114">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-114">Select **New**.</span></span>
8. <span data-ttu-id="bb4cb-115">En el campo **Fecha de vigencia**, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="bb4cb-116">En el campo **Válido para**, seleccione una opción.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="bb4cb-117">En el campo **Precio**, especifique un número.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="bb4cb-118">Puede configurar un precio de venta estándar para transacciones por hora o para una categoría de proyecto.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="bb4cb-119">También puede configurar los precios de venta por número de trabajador, número de proyecto, categoría, fecha de transacción o cualquier combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="bb4cb-120">El precio de venta real, que se aplica cuando un trabajador especifica una transacción en el diario de horas, es el precio de venta con el mayor nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="bb4cb-121">Por ejemplo, si se configura tanto un precio de venta general como un precio de venta específico del trabajador, se utiliza el precio de venta específico del trabajador.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="bb4cb-122">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-122">Select **Save**.</span></span>
12. <span data-ttu-id="bb4cb-123">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-123">Close the page.</span></span>
13. <span data-ttu-id="bb4cb-124">En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de coste (gasto)**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="bb4cb-125">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-125">Select **New**.</span></span>
15. <span data-ttu-id="bb4cb-126">En el campo **Fecha de vigencia**, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="bb4cb-127">En el campo **Precio de coste**, introduzca un número.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="bb4cb-128">Se pueden completar varios campos, pero este es el mínimo necesario para guardar el registro.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="bb4cb-129">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-129">Select **Save**.</span></span>
18. <span data-ttu-id="bb4cb-130">En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de venta (gasto)**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="bb4cb-131">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-131">Select **New**.</span></span>
20. <span data-ttu-id="bb4cb-132">En el campo **Fecha de vigencia**, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="bb4cb-133">En el campo **Válido para**, seleccione una opción.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="bb4cb-134">En el campo **Precio**, especifique un número.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="bb4cb-135">El precio de venta real, que se aplica cuando un trabajador especifica una transacción en el diario de gastos, es el precio de venta con el mayor nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="bb4cb-136">Por ejemplo, si se configura tanto un precio de venta general como un precio de venta específico del trabajador, se utiliza el precio de venta específico del trabajador.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="bb4cb-137">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bb4cb-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]