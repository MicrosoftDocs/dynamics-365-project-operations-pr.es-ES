---
title: Determinar el tipo de implementación
description: Este tema proporciona información para ayudarle a determinar el tipo de implementación correcto de las operaciones de proyecto para su empresa.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401239"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="e7066-103">Determinar el tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="e7066-103">Determine your deployment type</span></span>

<span data-ttu-id="e7066-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="e7066-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7066-105">Después de comprar la licencia, comience aquí para determinar el mejor modelo de implementación de Dynamics 365 Project Operations usando el [Flujo de instalación guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="e7066-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="e7066-106">Una vez que haya finalizado el flujo de instalación guiada, se le dirigirá al portal de administración correcto para completar su instalación.</span><span class="sxs-lookup"><span data-stu-id="e7066-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="e7066-107">Consulte los detalles de implementación para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="e7066-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="e7066-108">Clientes existentes de Dynamics que utilizan Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e7066-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="e7066-109">Project Operations incluye las capacidades que se incluyen con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e7066-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="e7066-110">Se lanzará una ruta de actualización para estos clientes en la primera ola de versiones de 2021.</span><span class="sxs-lookup"><span data-stu-id="e7066-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="e7066-111">Clientes existentes de Dynamics 365 Finance que usan gestión de proyectos y contabilidad</span><span class="sxs-lookup"><span data-stu-id="e7066-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="e7066-112">Los clientes existentes de Finance que utilizan la funcionalidad de contabilidad y gestión de proyectos pueden seguir utilizándola tal cual.</span><span class="sxs-lookup"><span data-stu-id="e7066-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="e7066-113">Consulte [Project Operations para escenarios de pedidos en existencias/producción](#pma).</span><span class="sxs-lookup"><span data-stu-id="e7066-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="e7066-114">Tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="e7066-114">Deployment types</span></span>
<span data-ttu-id="e7066-115">Project Operations admite múltiples opciones de implementación para satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="e7066-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="e7066-116">Ya sea un cliente nuevo o existente de Dynamics 365, Project Operations puede satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="e7066-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="e7066-117">Nuestro [Cuestionario de implementación](https://aka.ms/provisionprojectoperations) le ayudará a determinar la implementación correcta.</span><span class="sxs-lookup"><span data-stu-id="e7066-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="e7066-118">Los resultados le guiarán hacia uno de los siguientes tipos de implementación:</span><span class="sxs-lookup"><span data-stu-id="e7066-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="e7066-119">Implementación lite: del acuerdo a la facturación proforma</span><span class="sxs-lookup"><span data-stu-id="e7066-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="e7066-120">Project Operations para escenarios de recursos/no mantenidos en existencias</span><span class="sxs-lookup"><span data-stu-id="e7066-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="e7066-121">Project Operations para escenarios mantenidos en existencias/orden de producción</span><span class="sxs-lookup"><span data-stu-id="e7066-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="e7066-122">Project Operations admite escenarios de pedidos de existencias/producción y escenarios de no existencias/basados en recursos en el mismo entorno a través de configuraciones a nivel de entidad legal.</span><span class="sxs-lookup"><span data-stu-id="e7066-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="e7066-123">Por ejemplo, Contoso puede usar las capacidades de pedidos de stock / producción en sus instalaciones de fabricación de EE. UU. (Entidad legal = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="e7066-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="e7066-124">Contoso puede usar las capacidades no almacenadas / basadas en recursos en su instalación de servicio Contoso Robotics Arms en el Reino Unido (entidad legal = Contoso Robotics Reino Unido).</span><span class="sxs-lookup"><span data-stu-id="e7066-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="e7066-125">Implementación lite: del acuerdo a la facturación proforma</span><span class="sxs-lookup"><span data-stu-id="e7066-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="e7066-126">La implementación simplificada incluye las siguientes capacidades:</span><span class="sxs-lookup"><span data-stu-id="e7066-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="e7066-127">Proceso de ventas para proyectos que amplía las experiencias de la aplicación Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="e7066-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="e7066-128">Planificación de proyectos con Microsoft Project para la Web</span><span class="sxs-lookup"><span data-stu-id="e7066-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="e7066-129">Precios multidimensionales</span><span class="sxs-lookup"><span data-stu-id="e7066-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="e7066-130">Administración de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="e7066-130">Unified resource management</span></span>
- <span data-ttu-id="e7066-131">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="e7066-131">Time tracking</span></span>
- <span data-ttu-id="e7066-132">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="e7066-132">Basic expense</span></span>
- <span data-ttu-id="e7066-133">Facturación proforma y de cara al cliente</span><span class="sxs-lookup"><span data-stu-id="e7066-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="e7066-134">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="e7066-134">Deployment steps</span></span>
<span data-ttu-id="e7066-135">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="e7066-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e7066-136">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](lite-preview-subscription-sign-up.md) y [Aprovisionar un nuevo entorno](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="e7066-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="e7066-137">Project Operations para escenarios de recursos/no mantenidos en existencias</span><span class="sxs-lookup"><span data-stu-id="e7066-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="e7066-138">Project Operations para escenarios de recursos/no en existencias incluye las siguientes capacidades:</span><span class="sxs-lookup"><span data-stu-id="e7066-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="e7066-139">Proceso de ventas para proyectos que amplía la aplicación Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="e7066-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="e7066-140">Planificación de proyectos con Microsoft Project para la Web</span><span class="sxs-lookup"><span data-stu-id="e7066-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="e7066-141">Precios multidimensionales</span><span class="sxs-lookup"><span data-stu-id="e7066-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="e7066-142">Administración de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="e7066-142">Unified resource management</span></span>
- <span data-ttu-id="e7066-143">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="e7066-143">Time tracking</span></span>
- <span data-ttu-id="e7066-144">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="e7066-144">Basic expense</span></span>
- <span data-ttu-id="e7066-145">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="e7066-145">Full expense</span></span>
- <span data-ttu-id="e7066-146">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="e7066-146">Receipt OCR</span></span>
- <span data-ttu-id="e7066-147">Facturación proforma y de cara al cliente</span><span class="sxs-lookup"><span data-stu-id="e7066-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="e7066-148">Reconocimiento de ingresos para proyectos</span><span class="sxs-lookup"><span data-stu-id="e7066-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="e7066-149">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="e7066-149">Deployment steps</span></span>
<span data-ttu-id="e7066-150">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="e7066-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e7066-151">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](resource-sign-up-preview-subscription.md) y [Aprovisionar un nuevo entorno](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e7066-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="e7066-152">Project Operations para escenarios mantenidos en existencias/orden de producción</span><span class="sxs-lookup"><span data-stu-id="e7066-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="e7066-153">Planificación del proyecto usando WBS</span><span class="sxs-lookup"><span data-stu-id="e7066-153">Project planning using WBS</span></span>
- <span data-ttu-id="e7066-154">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="e7066-154">Resource Management</span></span>
- <span data-ttu-id="e7066-155">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="e7066-155">Time Tracking</span></span>
- <span data-ttu-id="e7066-156">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="e7066-156">Full Expense</span></span>
- <span data-ttu-id="e7066-157">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="e7066-157">Receipt OCR</span></span>
- <span data-ttu-id="e7066-158">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="e7066-158">Full Invoicing</span></span>
- <span data-ttu-id="e7066-159">Reconocimiento de ingresos</span><span class="sxs-lookup"><span data-stu-id="e7066-159">Revenue Recognition</span></span>
- <span data-ttu-id="e7066-160">Órdenes de producción</span><span class="sxs-lookup"><span data-stu-id="e7066-160">Production Orders</span></span>
- <span data-ttu-id="e7066-161">Soporte de materiales</span><span class="sxs-lookup"><span data-stu-id="e7066-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="e7066-162">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="e7066-162">Deployment steps</span></span>
<span data-ttu-id="e7066-163">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="e7066-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e7066-164">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) y [Aprovisionar un nuevo entorno](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e7066-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

