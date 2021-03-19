---
title: Crear y aplicar términos de retención de pagos de proveedores
description: Este tema proporciona información sobre cómo configurar y mantener los términos de retención para los pagos a proveedores.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270969"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="94378-103">Crear y aplicar términos de retención de pagos de proveedores</span><span class="sxs-lookup"><span data-stu-id="94378-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="94378-104">La configuración de los términos de retención de pagos de proveedores para un proyecto es útil cuando su organización desea retener parte de los pagos realizados a un proveedor.</span><span class="sxs-lookup"><span data-stu-id="94378-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="94378-105">Por ejemplo, cuando desee retener el pago a un proveedor hasta que los productos entregados cumplan con sus expectativas.</span><span class="sxs-lookup"><span data-stu-id="94378-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="94378-106">Los términos de retención de pago del proveedor se pueden especificar cuando se negocia un contrato con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="94378-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="94378-107">Crear términos de retención de pagos de proveedores</span><span class="sxs-lookup"><span data-stu-id="94378-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="94378-108">Puede introducir el porcentaje del pago del proveedor para la retención y el porcentaje de las cantidades retenidas previamente que se liberarán.</span><span class="sxs-lookup"><span data-stu-id="94378-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="94378-109">Los importes se retienen automáticamente en las facturas del proveedor hasta que el contrato alcanza el estado especificado de finalización.</span><span class="sxs-lookup"><span data-stu-id="94378-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="94378-110">Después de configurar los términos de retención, puede aplicarlos a cualquier proyecto para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="94378-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="94378-111">Utilice los siguientes pasos para configurar y mantener los términos de retención para los pagos a proveedores.</span><span class="sxs-lookup"><span data-stu-id="94378-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="94378-112">Vaya a **Gestión de proyectos y contabilidad** > **Retencion** > **Condiciones de retención de pago del proveedor**.</span><span class="sxs-lookup"><span data-stu-id="94378-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="94378-113">Seleccione **Nuevo** para agregar un nuevo plazo de retención de proveedores.</span><span class="sxs-lookup"><span data-stu-id="94378-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="94378-114">El valor **Identificador de regla** para el nuevo término se ingresa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="94378-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="94378-115">Introduzca una breve descripción en el campo **Descripción** y en la ficha desplegable **Términos**, seleccione **Agregar línea** para ingresar valores de término para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="94378-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="94378-116">**Porcentaje de unidades entregadas**: introduzca un porcentaje de finalización del período.</span><span class="sxs-lookup"><span data-stu-id="94378-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="94378-117">Los importes se retienen automáticamente en las facturas del proveedor hasta que la fase de finalización del proyecto iguale al porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="94378-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="94378-118">Por ejemplo, si introduce 50,00, las cantidades se retienen hasta que el proyecto se completa en un 50 por ciento.</span><span class="sxs-lookup"><span data-stu-id="94378-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="94378-119">**Porcentaje a retener**: introduzca un porcentaje del monto de la factura del proveedor que se retendrá.</span><span class="sxs-lookup"><span data-stu-id="94378-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="94378-120">Por ejemplo, si introduce 10,00, el 10 por ciento del monto de la factura de un proveedor se retiene hasta que el proyecto alcanza el porcentaje de finalización establecido en el **Campo Porcentaje de unidades entregadas**.</span><span class="sxs-lookup"><span data-stu-id="94378-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="94378-121">**Porcentaje para liberar**: seleccione **Agregar línea** para introducir un porcentaje de los montos retenidos previamente que se liberarán para el nivel seleccionado de finalización del proyecto.</span><span class="sxs-lookup"><span data-stu-id="94378-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="94378-122">Si tiene más de un hito para diferentes niveles de finalización del proyecto, ingrese una línea de plazo de retención de proveedor separada para cada regla de retención.</span><span class="sxs-lookup"><span data-stu-id="94378-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="94378-123">Cada línea puede especificar un porcentaje de retención diferente y un porcentaje de liberación diferente para cada nivel designado de finalización del proyecto.</span><span class="sxs-lookup"><span data-stu-id="94378-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="94378-124">Después de crear los términos de retención de proveedor para un proveedor, puede aplicar los términos a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="94378-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="94378-125">Aplicar términos de retención de proveedores a un proyecto</span><span class="sxs-lookup"><span data-stu-id="94378-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="94378-126">Vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Todos los proyectos** y abra un proyecto desde la página de lista de proyectos.</span><span class="sxs-lookup"><span data-stu-id="94378-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="94378-127">En la ficha desplegable **Acuerdos de proveedor**, seleccione **Agregar línea**.</span><span class="sxs-lookup"><span data-stu-id="94378-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="94378-128">En el campo **Código de cuenta**, seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="94378-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="94378-129">**Tabla**: los términos de retención de proveedor se aplican a un solo proveedor.</span><span class="sxs-lookup"><span data-stu-id="94378-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="94378-130">**Grupo**: los términos de retención de proveedor se aplican a todos los proveedores de un grupo de proveedores.</span><span class="sxs-lookup"><span data-stu-id="94378-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="94378-131">**Todos**: los términos de retención de proveedor se aplican a todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="94378-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="94378-132">En el **Proveedor/ campo de grupo de proveedores**, seleccione el proveedor o el grupo de proveedores al que se aplican los términos de retención de proveedores.</span><span class="sxs-lookup"><span data-stu-id="94378-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="94378-133">Si seleccionó **Todos** en el paso anterior, este campo no está disponible.</span><span class="sxs-lookup"><span data-stu-id="94378-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="94378-134">En el campo **Términos de retención de proveedores**, seleccione los términos de retención que creó en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="94378-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="94378-135">Si el proyecto también tiene términos de pago cuando se paga (PWP) configurados para el proveedor, introduzca el porcentaje de umbral para el proyecto en el campo **Porcentaje de umbral de PWP**.</span><span class="sxs-lookup"><span data-stu-id="94378-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="94378-136">Los términos de retención de proveedores también se muestran en las órdenes de compra que crea para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="94378-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]