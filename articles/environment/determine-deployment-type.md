---
title: Determinar el tipo de implementación
description: Este tema proporciona información para ayudarle a determinar el tipo de implementación correcto de las operaciones de proyecto para su empresa.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085152"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="57a25-103">Determinar el tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="57a25-103">Determine your deployment type</span></span>

<span data-ttu-id="57a25-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="57a25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57a25-105">Después de comprar la licencia, comience aquí para determinar el mejor modelo de implementación de Dynamics 365 Project Operations usando el [Flujo de instalación guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="57a25-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="57a25-106">Una vez que haya finalizado el flujo de instalación guiada, se le dirigirá al portal de administración correcto para completar su instalación.</span><span class="sxs-lookup"><span data-stu-id="57a25-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="57a25-107">Consulte los detalles de implementación para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="57a25-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="57a25-108">Clientes existentes de Dynamics que utilizan Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="57a25-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="57a25-109">Project Operations incluye las capacidades que se incluyen con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="57a25-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="57a25-110">Se lanzará una ruta de actualización para estos clientes en el futuro.</span><span class="sxs-lookup"><span data-stu-id="57a25-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="57a25-111">Clientes existentes de Dynamics 365 Finance que usan gestión de proyectos y contabilidad</span><span class="sxs-lookup"><span data-stu-id="57a25-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="57a25-112">Los clientes existentes de Finance que utilizan la funcionalidad de gestión de proyectos y contabilidad pueden seguir utilizándola tal cual.</span><span class="sxs-lookup"><span data-stu-id="57a25-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="57a25-113">Consulte [Project Operations para escenarios de pedidos en existencias/producción](#pma).</span><span class="sxs-lookup"><span data-stu-id="57a25-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="57a25-114">Tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="57a25-114">Deployment types</span></span>
<span data-ttu-id="57a25-115">Project Operations admite múltiples opciones de implementación para satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="57a25-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="57a25-116">Ya sea un cliente nuevo o existente de Dynamics 365, Project Operations puede satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="57a25-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="57a25-117">Nuestro [Cuestionario de implementación](https://aka.ms/provisionprojectoperations) le ayudará a determinar la implementación correcta.</span><span class="sxs-lookup"><span data-stu-id="57a25-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="57a25-118">Los resultados le guiarán hacia uno de los siguientes tipos de implementación:</span><span class="sxs-lookup"><span data-stu-id="57a25-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="57a25-119">Implementación lite: del acuerdo a la facturación proforma</span><span class="sxs-lookup"><span data-stu-id="57a25-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="57a25-120">Project Operations para escenarios de recursos/no mantenidos en existencias</span><span class="sxs-lookup"><span data-stu-id="57a25-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="57a25-121">Project Operations para escenarios mantenidos en existencias/orden de producción</span><span class="sxs-lookup"><span data-stu-id="57a25-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="57a25-122">Project Operations admite escenarios de pedidos de existencias/producción y escenarios de no existencias/basados en recursos en el mismo entorno a través de configuraciones a nivel de entidad legal.</span><span class="sxs-lookup"><span data-stu-id="57a25-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="57a25-123">Por ejemplo, Contoso puede usar las capacidades de pedidos de stock / producción en sus instalaciones de fabricación de EE. UU. (Entidad legal = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="57a25-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="57a25-124">Contoso puede usar las capacidades no almacenadas / basadas en recursos en su instalación de servicio Contoso Robotics Arms en el Reino Unido (entidad legal = Contoso Robotics Reino Unido).</span><span class="sxs-lookup"><span data-stu-id="57a25-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="57a25-125">Implementación lite: del acuerdo a la facturación proforma</span><span class="sxs-lookup"><span data-stu-id="57a25-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="57a25-126">La implementación simplificada incluye las siguientes capacidades:</span><span class="sxs-lookup"><span data-stu-id="57a25-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="57a25-127">Planificación de proyectos con Microsoft Project para la Web</span><span class="sxs-lookup"><span data-stu-id="57a25-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="57a25-128">Precios multidimensionales</span><span class="sxs-lookup"><span data-stu-id="57a25-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="57a25-129">Administración de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="57a25-129">Unified Resource Management</span></span>
- <span data-ttu-id="57a25-130">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="57a25-130">Time Tracking</span></span>
- <span data-ttu-id="57a25-131">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="57a25-131">Basic Expense</span></span>
- <span data-ttu-id="57a25-132">Propuesta de factura</span><span class="sxs-lookup"><span data-stu-id="57a25-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="57a25-133">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="57a25-133">Deployment steps</span></span>
<span data-ttu-id="57a25-134">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="57a25-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="57a25-135">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](lite-preview-subscription-sign-up.md) y [Aprovisionar un nuevo entorno](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="57a25-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="57a25-136">Project Operations para escenarios de recursos/no mantenidos en existencias</span><span class="sxs-lookup"><span data-stu-id="57a25-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="57a25-137">Project Operations para escenarios de recursos/no en existencias incluye las siguientes capacidades:</span><span class="sxs-lookup"><span data-stu-id="57a25-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="57a25-138">Planificación de proyectos con Microsoft Project para la Web</span><span class="sxs-lookup"><span data-stu-id="57a25-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="57a25-139">Precios multidimensionales</span><span class="sxs-lookup"><span data-stu-id="57a25-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="57a25-140">Administración de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="57a25-140">Unified Resource Management</span></span>
- <span data-ttu-id="57a25-141">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="57a25-141">Time Tracking</span></span>
- <span data-ttu-id="57a25-142">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="57a25-142">Basic Expense</span></span>
- <span data-ttu-id="57a25-143">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="57a25-143">Full Expense</span></span>
- <span data-ttu-id="57a25-144">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="57a25-144">Receipt OCR</span></span>
- <span data-ttu-id="57a25-145">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="57a25-145">Full Invoicing</span></span>
- <span data-ttu-id="57a25-146">Reconocimiento de ingresos</span><span class="sxs-lookup"><span data-stu-id="57a25-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="57a25-147">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="57a25-147">Deployment steps</span></span>
<span data-ttu-id="57a25-148">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="57a25-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="57a25-149">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](resource-sign-up-preview-subscription.md) y [Aprovisionar un nuevo entorno](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="57a25-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="57a25-150">Project Operations para escenarios mantenidos en existencias/orden de producción</span><span class="sxs-lookup"><span data-stu-id="57a25-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="57a25-151">Planificación del proyecto usando WBS</span><span class="sxs-lookup"><span data-stu-id="57a25-151">Project planning using WBS</span></span>
- <span data-ttu-id="57a25-152">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="57a25-152">Resource Management</span></span>
- <span data-ttu-id="57a25-153">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="57a25-153">Time Tracking</span></span>
- <span data-ttu-id="57a25-154">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="57a25-154">Full Expense</span></span>
- <span data-ttu-id="57a25-155">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="57a25-155">Receipt OCR</span></span>
- <span data-ttu-id="57a25-156">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="57a25-156">Full Invoicing</span></span>
- <span data-ttu-id="57a25-157">Reconocimiento de ingresos</span><span class="sxs-lookup"><span data-stu-id="57a25-157">Revenue Recognition</span></span>
- <span data-ttu-id="57a25-158">Órdenes de producción</span><span class="sxs-lookup"><span data-stu-id="57a25-158">Production Orders</span></span>
- <span data-ttu-id="57a25-159">Soporte de materiales</span><span class="sxs-lookup"><span data-stu-id="57a25-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="57a25-160">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="57a25-160">Deployment steps</span></span>
<span data-ttu-id="57a25-161">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="57a25-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="57a25-162">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) y [Aprovisionar un nuevo entorno](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="57a25-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

