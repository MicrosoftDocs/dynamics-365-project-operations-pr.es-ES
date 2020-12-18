---
title: Valores predeterminados de dimensiones financieras
description: Este tema proporciona información sobre cómo configurar los valores predeterminados de la dimensión financiera.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642384"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="91dd6-103">Valores predeterminados de dimensiones financieras</span><span class="sxs-lookup"><span data-stu-id="91dd6-103">Financial dimension defaults</span></span>

<span data-ttu-id="91dd6-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="91dd6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="91dd6-105">Dynamics 365 Project Operations usa el marco [Dimensiones financieras](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) en Dynamics 365 Finance para proporcionar información adicional sobre las transacciones del libro mayor auxiliar y del libro mayor general del proyecto.</span><span class="sxs-lookup"><span data-stu-id="91dd6-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="91dd6-106">Las dimensiones financieras predeterminadas se pueden establecer en un cliente, una fuente de financiación del proyecto, un hito, una línea de contrato del proyecto o un proyecto.</span><span class="sxs-lookup"><span data-stu-id="91dd6-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="91dd6-107">Definir dimensiones financieras predeterminadas para un cliente</span><span class="sxs-lookup"><span data-stu-id="91dd6-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="91dd6-108">Los valores predeterminados de la dimensión del cliente se especifican en Finance.</span><span class="sxs-lookup"><span data-stu-id="91dd6-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="91dd6-109">Complete los pasos siguientes para establecer los valores predeterminados de dimensión.</span><span class="sxs-lookup"><span data-stu-id="91dd6-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="91dd6-110">Vaya a **Clientes** > **Clientes** > **Todos los clientes**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="91dd6-111">Sobre la página **Clientes**, en la pestaña **Dimensiones financieras**, establezca los valores de la dimensión financiera para un cliente específico.</span><span class="sxs-lookup"><span data-stu-id="91dd6-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="91dd6-112">Definir dimensiones financieras predeterminadas para contratos de proyectos</span><span class="sxs-lookup"><span data-stu-id="91dd6-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="91dd6-113">Los contratos de proyecto se crean y mantienen en Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="91dd6-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="91dd6-114">Los atributos contables para los contratos de proyecto se establecen en el módulo **Gestión de proyectos y contabilidad** en Finance.</span><span class="sxs-lookup"><span data-stu-id="91dd6-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="91dd6-115">Establecer dimensiones financieras para una fuente de financiación de proyectos</span><span class="sxs-lookup"><span data-stu-id="91dd6-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="91dd6-116">Vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Contratos de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="91dd6-117">Seleccione el registro que desea actualizar y en la pestaña **Contrato de proyecto**, seleccione **Mostrar contabilidad predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="91dd6-118">Expanda **Información relacionada** y seleccione la pestaña **Fuentes de financiamiento**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="91dd6-119">Estalbezca los valores predeterminados de dimensiones financieras.</span><span class="sxs-lookup"><span data-stu-id="91dd6-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="91dd6-120">Observe que las dimensiones financieras usan los valores predeterminados de la cuenta del cliente.</span><span class="sxs-lookup"><span data-stu-id="91dd6-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="91dd6-121">Establecer dimensiones financieras para una línea de contrato de proyectos</span><span class="sxs-lookup"><span data-stu-id="91dd6-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="91dd6-122">Vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Contratos de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="91dd6-123">Seleccione el registro que desea actualizar y en la pestaña **Contrato de proyecto**, seleccione **Mostrar contabilidad predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="91dd6-124">Expanda **Información relacionada** y seleccione la pestaña **Líneas de contrato**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="91dd6-125">Estalbezca los valores predeterminados de dimensiones financieras.</span><span class="sxs-lookup"><span data-stu-id="91dd6-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="91dd6-126">Los valores predeterminados de la dimensión financiera son aplicables y solo se pueden usar con líneas de contrato de precio fijo (hito).</span><span class="sxs-lookup"><span data-stu-id="91dd6-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="91dd6-127">Estos valores predeterminados se utilizan en transacciones a cuenta del proyecto y líneas de factura relacionadas.</span><span class="sxs-lookup"><span data-stu-id="91dd6-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="91dd6-128">Definir dimensiones financieras predeterminadas para proyectos</span><span class="sxs-lookup"><span data-stu-id="91dd6-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="91dd6-129">Los proyectos se crean y mantienen en CDS.</span><span class="sxs-lookup"><span data-stu-id="91dd6-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="91dd6-130">Los atributos contables para proyectos se establecen en el módulo **Gestión de proyectos y contabilidad** en Finance.</span><span class="sxs-lookup"><span data-stu-id="91dd6-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="91dd6-131">Vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Todos los proyectos**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="91dd6-132">Seleccione el registro que desea actualizar y en la pestaña **Proyecto**, seleccione **Mostrar contabilidad predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="91dd6-133">Expanda **Información relacionada** y seleccione la pestaña **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="91dd6-134">Estalbezca los valores predeterminados de dimensiones financieras.</span><span class="sxs-lookup"><span data-stu-id="91dd6-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="91dd6-135">Observe que las dimensiones financieras usan los valores predeterminados de la cuenta del cliente.</span><span class="sxs-lookup"><span data-stu-id="91dd6-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="91dd6-136">Si el proyecto está asociado con una línea de contrato con varios clientes de contrato de proyecto, el cliente principal se utiliza para las dimensiones financieras predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="91dd6-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="91dd6-137">Las dimensiones financieras predeterminadas del proyecto se utilizan para establecer los valores predeterminados de las líneas de diario para las transacciones de tiempo, gastos y tarifas en el **Diario de integración de Project Operations** y en las líneas de factura de proyectos relacionados.</span><span class="sxs-lookup"><span data-stu-id="91dd6-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
