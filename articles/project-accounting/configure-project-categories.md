---
title: Configurar categorías de proyectos
description: En este tema se proporciona información sobre la configuración de categorías de proyecto.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131949"
---
# <a name="configure-project-categories"></a><span data-ttu-id="0352c-103">Configurar categorías de proyectos</span><span class="sxs-lookup"><span data-stu-id="0352c-103">Configure project categories</span></span>

<span data-ttu-id="0352c-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="0352c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0352c-105">Project Operations ofrece capacidades sólidas para categorizar ingresos y gastos en proyectos.</span><span class="sxs-lookup"><span data-stu-id="0352c-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="0352c-106">Las categorías brindan la capacidad de informar y analizar las transacciones del proyecto e impulsar la contabilización en el libro mayor.</span><span class="sxs-lookup"><span data-stu-id="0352c-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="0352c-107">El siguiente diagrama ilustra la correlación entre categorías de transacciones, categorías compartidas y categorías de proyectos.</span><span class="sxs-lookup"><span data-stu-id="0352c-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="0352c-108">Las categorías de transacciones son la agrupación básica para las transacciones de proyectos.</span><span class="sxs-lookup"><span data-stu-id="0352c-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="0352c-109">Dentro de esa agrupación, hay un conjunto de categorías compartidas que se pueden compartir entre aplicaciones y módulos.</span><span class="sxs-lookup"><span data-stu-id="0352c-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="0352c-110">Entrando aún más en los detalles, las categorías de proyectos son el nivel más granular de las categorías.</span><span class="sxs-lookup"><span data-stu-id="0352c-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="0352c-111">Las categorías de proyectos son específicas de la entidad jurídica, el módulo y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0352c-111">Project categories are specific to legal entity, module, and application.</span></span>

![Correlación entre categorías de transacciones, categorías compartidas y categorías de proyectos](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="0352c-113">Categorías de transacciones</span><span class="sxs-lookup"><span data-stu-id="0352c-113">Transaction categories</span></span>

<span data-ttu-id="0352c-114">Las categorías de transacciones representan la agrupación básica para las transacciones de proyecto y no son específicas de la empresa ni del tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="0352c-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="0352c-115">Por ejemplo, Contoso Robotics usa las categorías Diseño, Viaje, Instalación y Transacción de servicio para agrupar transacciones de proyecto.</span><span class="sxs-lookup"><span data-stu-id="0352c-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="0352c-116">Las categorías de transacciones se definen en el módulo Operaciones de proyecto.</span><span class="sxs-lookup"><span data-stu-id="0352c-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="0352c-117">Vaya a **Configuración** \> **Categorías de transacciones** para abrir el formulario.</span><span class="sxs-lookup"><span data-stu-id="0352c-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="0352c-118">Cree una nueva categoría de transacción seleccionando **Nueva** o seleccionando **Importar desde Excel**.</span><span class="sxs-lookup"><span data-stu-id="0352c-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="0352c-119">Categorías compartidas</span><span class="sxs-lookup"><span data-stu-id="0352c-119">Shared categories</span></span>

<span data-ttu-id="0352c-120">Dynamics 365 utiliza el concepto de categorías compartidas para categorizar los gastos en diferentes aplicaciones, como Dynamics 365 Finance, Dynamics 365 Supply Chain y Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0352c-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="0352c-121">Para cada categoría de transacción creada, Project Operations crea automáticamente cuatro categorías compartidas relacionadas: Horas, Gastos, Tarifas y Artículo.</span><span class="sxs-lookup"><span data-stu-id="0352c-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="0352c-122">Puede revisar y ajustar las categorías compartidas yendo a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Categorías compartidas**.</span><span class="sxs-lookup"><span data-stu-id="0352c-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="0352c-123">Categorías de proyecto</span><span class="sxs-lookup"><span data-stu-id="0352c-123">Project categories</span></span>

<span data-ttu-id="0352c-124">Las categorías de proyectos representan el nivel más granular de configuración de categorías y deben configurarse por separado, y para cada empresa, por medio de un contable de proyectos.</span><span class="sxs-lookup"><span data-stu-id="0352c-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="0352c-125">Vaya a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Categorías de proyectos**.</span><span class="sxs-lookup"><span data-stu-id="0352c-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="0352c-126">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="0352c-126">Select **New**.</span></span>
3. <span data-ttu-id="0352c-127">Seleccione el **Id. de categoria** de la categoría compartida que creó en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="0352c-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="0352c-128">Las operaciones de proyecto permiten usar solo las categorías compartidas que están asociadas con las categorías de transacciones.</span><span class="sxs-lookup"><span data-stu-id="0352c-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="0352c-129">Seleccione un grupo de categorías.</span><span class="sxs-lookup"><span data-stu-id="0352c-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="0352c-130">Grupos de categorías</span><span class="sxs-lookup"><span data-stu-id="0352c-130">Category groups</span></span>

<span data-ttu-id="0352c-131">Los grupos de categorías se utilizan para compartir propiedades, principalmente perfiles de registro, entre categorías de proyectos relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0352c-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="0352c-132">Debe haber al menos un grupo de categorías para cada tipo de transacción y a cada categoría de proyecto se le asigna un grupo.</span><span class="sxs-lookup"><span data-stu-id="0352c-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="0352c-133">Las especificaciones de contabilización de las operaciones de proyecto se definen mediante las reglas del perfil de costes e ingresos del proyecto, las categorías de proyectos y los grupos de categorías.</span><span class="sxs-lookup"><span data-stu-id="0352c-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="0352c-134">Puede configurar grupos de categorías yendo a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Grupos de categorías**.</span><span class="sxs-lookup"><span data-stu-id="0352c-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
