---
title: Configurar Project Service Automation
description: Pasos para la configuración de Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ec5381f91b1fe5198bd93ac8d6015b1fea38738d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146954"
---
# <a name="configure-project-service"></a><span data-ttu-id="e58c0-103">Configure Project Service</span><span class="sxs-lookup"><span data-stu-id="e58c0-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e58c0-104">Antes de poder usar las capacidades de automatización de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] para administrar los proyectos, cuentas, y recursos, debe completar unos pasos de configuración para asegurarse de que la solución de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] coincide con las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="e58c0-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="e58c0-105">Estos pasos incluyen:</span><span class="sxs-lookup"><span data-stu-id="e58c0-105">These steps include:</span></span>  
  
-   <span data-ttu-id="e58c0-106">[Establecer unidades de tiempo](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="e58c0-107">Configure las unidades de tiempo en el catálogo de productos que usará como base para programar y facturar los proyectos.</span><span class="sxs-lookup"><span data-stu-id="e58c0-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="e58c0-108">[Establecer divisas y tipos de cambio](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="e58c0-109">Configure las divisas que usará para los proyectos.</span><span class="sxs-lookup"><span data-stu-id="e58c0-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="e58c0-110">[Crear unidades organizativas](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="e58c0-111">Configure los grupos que su compañía use para dividir su negocio, sea por geografía, función de negocio u otra división lógica.</span><span class="sxs-lookup"><span data-stu-id="e58c0-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="e58c0-112">[Establecer frecuencias de facturas](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="e58c0-113">Configure periodos de tiempo que desea usar para facturar a los clientes.</span><span class="sxs-lookup"><span data-stu-id="e58c0-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="e58c0-114">[Configurar categorías de transacciones](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="e58c0-115">Configure categorías de transacción para que sus consultores puedan imputar sus gastos facturables y no facturables.</span><span class="sxs-lookup"><span data-stu-id="e58c0-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="e58c0-116">[Configurar categorías de gastos](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="e58c0-117">Configure las categorías para que sus consultores puedan imputar sus gastos facturables y no facturables.</span><span class="sxs-lookup"><span data-stu-id="e58c0-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="e58c0-118">[Crear artículos del catálogo de productos](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="e58c0-119">Agregue los productos que vende, como licencias de software, al catálogo de productos.</span><span class="sxs-lookup"><span data-stu-id="e58c0-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="e58c0-120">[Crear una lista de precios](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="e58c0-121">Configure varias listas de precios, en función de cuánto desea cobrar a sus clientes por cada rol que requiera su proyecto.</span><span class="sxs-lookup"><span data-stu-id="e58c0-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="e58c0-122">[Configuración de recursos](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="e58c0-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="e58c0-123">Agregue los conocimientos, las habilidades, los roles de recursos y otra información de recursos que necesitará para los proyectos.</span><span class="sxs-lookup"><span data-stu-id="e58c0-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e58c0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e58c0-124">See Also</span></span>  
 <span data-ttu-id="e58c0-125">[Información general de Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="e58c0-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="e58c0-126">[Configurar Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="e58c0-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="e58c0-127">[Guía de administrador de cuentas](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e58c0-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="e58c0-128">[Guía del jefe de proyecto](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e58c0-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="e58c0-129">[Guía del administrador de recursos](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e58c0-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="e58c0-130">Guía de tiempo, gastos y colaboración</span><span class="sxs-lookup"><span data-stu-id="e58c0-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
