---
title: Configurar categorías de gasto
description: Este tema proporciona información sobre cómo configurar categorías de gastos y categorías compartidas para informes de gastos.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085038"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="56895-103">Configurar categorías de gasto</span><span class="sxs-lookup"><span data-stu-id="56895-103">Set up expense categories</span></span>

<span data-ttu-id="56895-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="56895-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="56895-105">Cuando los empleados crean informes de gastos, cada gasto que registran debe asociarse con una categoría de gastos.</span><span class="sxs-lookup"><span data-stu-id="56895-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="56895-106">Las categorías de gastos se derivan de categorías compartidas que se pueden compartir entre las entidades legales de su organización.</span><span class="sxs-lookup"><span data-stu-id="56895-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="56895-107">Dependiendo de cómo se defina su organización, estas categorías de gastos también se pueden compartir en otras áreas.</span><span class="sxs-lookup"><span data-stu-id="56895-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="56895-108">Según la definición de su organización y la orientación del equipo de implementación, debe determinar si las categorías que se utilizan en la gestión de gastos se utilizarán solo en la gestión de gastos o deben compartirse en otras áreas.</span><span class="sxs-lookup"><span data-stu-id="56895-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="56895-109">Estas categorías se pueden compartir entre la gestión de proyectos y la contabilidad y la gestión de gastos, o entre la gestión de proyectos y la contabilidad y la producción.</span><span class="sxs-lookup"><span data-stu-id="56895-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="56895-110">Sin embargo, no se pueden compartir entre la gestión de gastos y la producción.</span><span class="sxs-lookup"><span data-stu-id="56895-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="56895-111">Para poder comenzar el proceso de configuración, se deben tomar las siguientes decisiones para cada categoría de gastos:</span><span class="sxs-lookup"><span data-stu-id="56895-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="56895-112">¿Cuál es la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-112">What is the expense category?</span></span> <span data-ttu-id="56895-113">Los ejemplos incluyen categorías de vuelos, hotel o kilometraje.</span><span class="sxs-lookup"><span data-stu-id="56895-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="56895-114">¿Se puede utilizar también la categoría de gastos en la gestión y contabilidad de proyectos?</span><span class="sxs-lookup"><span data-stu-id="56895-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="56895-115">Si puede hacerse, deberá tomar las siguientes decisiones:</span><span class="sxs-lookup"><span data-stu-id="56895-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="56895-116">¿Qué cuentas de costes se utilizarán para los siguientes gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="56895-117">Coste</span><span class="sxs-lookup"><span data-stu-id="56895-117">Cost</span></span>
        - <span data-ttu-id="56895-118">Asignación de nómina</span><span class="sxs-lookup"><span data-stu-id="56895-118">Payroll allocation</span></span>
        - <span data-ttu-id="56895-119">Valor de coste WIP</span><span class="sxs-lookup"><span data-stu-id="56895-119">WIP-cost value</span></span>
        - <span data-ttu-id="56895-120">Elemento de coste</span><span class="sxs-lookup"><span data-stu-id="56895-120">Cost-item</span></span>
        - <span data-ttu-id="56895-121">Elemento de valor de coste WIP</span><span class="sxs-lookup"><span data-stu-id="56895-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="56895-122">Pérdida acumulada</span><span class="sxs-lookup"><span data-stu-id="56895-122">Accrued loss</span></span>
        - <span data-ttu-id="56895-123">Pérdida acumulada WIP</span><span class="sxs-lookup"><span data-stu-id="56895-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="56895-124">¿Qué cuentas de ingresos se utilizarán para las siguientes fuentes de ingresos?</span><span class="sxs-lookup"><span data-stu-id="56895-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="56895-125">Ingresos facturados</span><span class="sxs-lookup"><span data-stu-id="56895-125">Invoiced revenue</span></span>
        - <span data-ttu-id="56895-126">Valor acumulado de ingresos de ventas</span><span class="sxs-lookup"><span data-stu-id="56895-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="56895-127">Valor de ventas WIP</span><span class="sxs-lookup"><span data-stu-id="56895-127">WIP-sales value</span></span>
        - <span data-ttu-id="56895-128">Producción de ingresos acumulados</span><span class="sxs-lookup"><span data-stu-id="56895-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="56895-129">Producción WIP</span><span class="sxs-lookup"><span data-stu-id="56895-129">WIP-production</span></span>
        - <span data-ttu-id="56895-130">Beneficios de ingresos acumulados</span><span class="sxs-lookup"><span data-stu-id="56895-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="56895-131">Beneficio WIP</span><span class="sxs-lookup"><span data-stu-id="56895-131">WIP-profit</span></span>
        - <span data-ttu-id="56895-132">Suscripción de ingresos acumulados</span><span class="sxs-lookup"><span data-stu-id="56895-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="56895-133">Suscripción WIP</span><span class="sxs-lookup"><span data-stu-id="56895-133">WIP-subscription</span></span>

- <span data-ttu-id="56895-134">¿Cuál es el tipo de gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-134">What is the expense type?</span></span>
- <span data-ttu-id="56895-135">¿Cuál es el método de pago predeterminado para la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="56895-136">¿Deben desglosarse los gastos de la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="56895-137">¿Cuál es la cuenta principal predeterminada para la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="56895-138">¿Cuál es el grupo de impuestos sobre ventas de artículos predeterminado para la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="56895-139">¿Se permiten métodos de pago adicionales para la categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="56895-140">En ese caso, ¿qué secciones hay?</span><span class="sxs-lookup"><span data-stu-id="56895-140">If so, what are they?</span></span>
- <span data-ttu-id="56895-141">¿Hay subcategorías en esta categoría de gastos?</span><span class="sxs-lookup"><span data-stu-id="56895-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="56895-142">Si hay subcategorías, deberá tomar también las siguientes decisiones:</span><span class="sxs-lookup"><span data-stu-id="56895-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="56895-143">¿Alguna de las subcategorías está excluida de la recuperación de impuestos?</span><span class="sxs-lookup"><span data-stu-id="56895-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="56895-144">¿Cuál es el grupo de impuestos sobre ventas de artículos de las subcategorías?</span><span class="sxs-lookup"><span data-stu-id="56895-144">What is the item sales tax group of the subcategories?</span></span>
