---
title: Revisión del trabajo pendiente de facturación en proyectos y contratos de proyecto
description: En este tema se proporciona información sobre cómo revisar los trabajos pendientes en los productos, los gastos y el tiempo, y cómo marcarlos como listos para la facturación.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756055"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="6227b-103">Revisión del trabajo pendiente de facturación en proyectos y contratos de proyecto</span><span class="sxs-lookup"><span data-stu-id="6227b-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6227b-104">Cuando una transacción está lista para crear y procesar una factura, la transacción debe marcarse como **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="6227b-105">Este tema describe los tipos de transacciones que se pueden crear.</span><span class="sxs-lookup"><span data-stu-id="6227b-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="6227b-106">Revisión del tiempo y trabajo pendiente de facturación de material</span><span class="sxs-lookup"><span data-stu-id="6227b-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="6227b-107">Cuando se presenta y aprueba una entrada de tiempo o gasto para un proyecto, PSA crea un proyecto real.</span><span class="sxs-lookup"><span data-stu-id="6227b-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="6227b-108">Si la combinación del proyecto y la clase de transacción se asignan a una línea de contrato para un proyecto de tiempo y materiales, se crean dos datos reales cuando se aprueba la entrada:</span><span class="sxs-lookup"><span data-stu-id="6227b-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="6227b-109">Coste real</span><span class="sxs-lookup"><span data-stu-id="6227b-109">Cost actual</span></span> 
- <span data-ttu-id="6227b-110">Dato real de ventas sin facturar</span><span class="sxs-lookup"><span data-stu-id="6227b-110">Unbilled sales actual</span></span>

<span data-ttu-id="6227b-111">Los datos reales de ventas sin facturar representan el trabajo pendiente de facturación y su estado de facturación debe establecerse en **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="6227b-112">Cuando se crea una factura de proyecto, los datos reales de ventas sin facturar que están marcados como **Listo para facturar** se copian como detalles de línea de factura.</span><span class="sxs-lookup"><span data-stu-id="6227b-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="6227b-113">Para revisar el trabajo pendiente de facturación de tiempo y materiales, vaya a **Ventas** \> **Facturación** \> **Trabajo pendiente de facturación de tiempo y material**.</span><span class="sxs-lookup"><span data-stu-id="6227b-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="6227b-114">Seleccione todos los datos reales de ventas sin facturar que estén listos para facturar y, a continuación, seleccione **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="6227b-115">El estado de facturación de esos datos reales cambia a **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Trabajo pendiente de facturación de tiempo y material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="6227b-117">Revisión del trabajo pendiente de facturación de productos</span><span class="sxs-lookup"><span data-stu-id="6227b-117">Review the product billing backlog</span></span>

<span data-ttu-id="6227b-118">En PSA, cuando un contrato de proyecto tiene líneas de contrato basadas en productos, esas líneas se consideran para facturación cada vez que se crea una factura para el contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="6227b-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="6227b-119">Cualquier producto que tenga líneas contractuales marcadas **Listo para facturar** se copiará en la factura del proyecto como líneas de factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6227b-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="6227b-120">Para revisar la cartera de facturación de productos, vaya a **Ventas** \> **Facturación** \> **Trabajo pendiente de facturación de productos**.</span><span class="sxs-lookup"><span data-stu-id="6227b-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="6227b-121">Seleccione todas las líneas de contrato basadas en productos que estén listas para facturarse, y, a continuación, seleccione **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="6227b-122">El estado de facturación de estas líneas cambia a **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Trabajo pendiente de facturación de productos](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="6227b-124">Revisión de hitos de facturación en contratos de precio fijo</span><span class="sxs-lookup"><span data-stu-id="6227b-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="6227b-125">Las líneas de contrato de proyecto que tienen un método de facturación de precio fijo deben definir hitos del contrato.</span><span class="sxs-lookup"><span data-stu-id="6227b-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="6227b-126">Estos hitos del contrato solo se pueden facturar si están marcados como **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="6227b-127">Para revisar los hitos de facturación, vaya a **Ventas** \> **Facturación** \> **Hitos de precio fijo**.</span><span class="sxs-lookup"><span data-stu-id="6227b-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="6227b-128">Seleccione los hitos que están listos para facturar y, a continuación seleccione **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="6227b-129">El estado de facturación de estos hitos cambia a **Listo para facturar**.</span><span class="sxs-lookup"><span data-stu-id="6227b-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Hitos de precio fijo](media/FPBacklog.png)
