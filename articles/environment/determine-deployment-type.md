---
title: Tipo de implementación
description: Este tema proporciona información para ayudarle a determinar el tipo de implementación correcto de las operaciones de proyecto para su empresa.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949088"
---
# <a name="deployment-types"></a><span data-ttu-id="02af8-103">Tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="02af8-103">Deployment types</span></span>

<span data-ttu-id="02af8-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="02af8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02af8-105">Después de comprar la licencia, comience aquí para determinar el mejor modelo de implementación de Dynamics 365 Project Operations usando el [Flujo de instalación guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="02af8-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="02af8-106">Una vez que haya finalizado el flujo de instalación guiada, se le dirigirá al portal de administración correcto para completar su instalación.</span><span class="sxs-lookup"><span data-stu-id="02af8-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="02af8-107">Consulte los detalles de implementación a continuación para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="02af8-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="02af8-108">Clientes existentes de Dynamics que utilizan Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="02af8-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="02af8-109">Project Operations incluye las capacidades que se incluyen con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="02af8-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="02af8-110">Se lanzará una ruta de actualización para estos clientes en el futuro.</span><span class="sxs-lookup"><span data-stu-id="02af8-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="02af8-111">Clientes existentes de Dynamics 365 Finance que usan gestión de proyectos y contabilidad</span><span class="sxs-lookup"><span data-stu-id="02af8-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="02af8-112">Los clientes existentes de Finance que utilizan la funcionalidad de gestión de proyectos y contabilidad pueden seguir utilizándola tal cual.</span><span class="sxs-lookup"><span data-stu-id="02af8-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="02af8-113">Consulte [Project Operations para escenarios de pedidos en existencias/producción](#pma).</span><span class="sxs-lookup"><span data-stu-id="02af8-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="02af8-114">Project Operations admite múltiples opciones de implementación para satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="02af8-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="02af8-115">Ya sea un cliente nuevo o existente de Dynamics 365, Project Operations puede satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="02af8-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="02af8-116">Nuestro [Cuestionario de implementación](https://aka.ms/provisionprojectoperations) le ayudará a determinar la implementación correcta.</span><span class="sxs-lookup"><span data-stu-id="02af8-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="02af8-117">Los resultados le guiarán hacia uno de los siguientes tipos de implementación:</span><span class="sxs-lookup"><span data-stu-id="02af8-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="02af8-118">Implementación lite: del acuerdo a la facturación proforma</span><span class="sxs-lookup"><span data-stu-id="02af8-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="02af8-119">Project Operations para escenarios de recursos/no mantenidos en existencias</span><span class="sxs-lookup"><span data-stu-id="02af8-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="02af8-120">Project Operations para escenarios mantenidos en existencias/orden de producción</span><span class="sxs-lookup"><span data-stu-id="02af8-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="02af8-121">Project Operations admite escenarios de pedidos de existencias/producción y escenarios de no existencias/basados en recursos en el mismo entorno a través de configuraciones a nivel de entidad legal.</span><span class="sxs-lookup"><span data-stu-id="02af8-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="02af8-122">Por ejemplo, Contoso puede aprovechar las capacidades de pedidos de existencias/producción en sus instalaciones de fabricación de EE. UU. (Entidad legal = Contoso Manufacturing United States) y las capacidades de no existencias/basadas en recursos en sus instalaciones de servicio de Contoso Robotics Arms en Reino Unido (Entidad legal = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="02af8-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="02af8-123"><a name="lite"><a/>Implementación lite: del acuerdo a la facturación proforma</span><span class="sxs-lookup"><span data-stu-id="02af8-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="02af8-124">La implementación simplificada incluye las siguientes capacidades:</span><span class="sxs-lookup"><span data-stu-id="02af8-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="02af8-125">Planificación de proyectos con Microsoft Project para la Web</span><span class="sxs-lookup"><span data-stu-id="02af8-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="02af8-126">Precios multidimensionales</span><span class="sxs-lookup"><span data-stu-id="02af8-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="02af8-127">Administración de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="02af8-127">Unified Resource Management</span></span>
- <span data-ttu-id="02af8-128">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="02af8-128">Time Tracking</span></span>
- <span data-ttu-id="02af8-129">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="02af8-129">Basic Expense</span></span>
- <span data-ttu-id="02af8-130">Propuesta de factura</span><span class="sxs-lookup"><span data-stu-id="02af8-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="02af8-131">Pasos de implementación:</span><span class="sxs-lookup"><span data-stu-id="02af8-131">Deployment steps:</span></span>
<span data-ttu-id="02af8-132">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="02af8-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="02af8-133">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](lite-preview-subscription-sign-up.md) y [Aprovisionar un nuevo entorno](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="02af8-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="02af8-134"><a name="integrated"><a/>Project Operations para escenarios de recursos/no mantenidos en existencias</span><span class="sxs-lookup"><span data-stu-id="02af8-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="02af8-135">Project Operations para escenarios de recursos/no en existencias incluye las siguientes capacidades:</span><span class="sxs-lookup"><span data-stu-id="02af8-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="02af8-136">Planificación de proyectos con Microsoft Project para la Web</span><span class="sxs-lookup"><span data-stu-id="02af8-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="02af8-137">Precios multidimensionales</span><span class="sxs-lookup"><span data-stu-id="02af8-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="02af8-138">Administración de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="02af8-138">Unified Resource Management</span></span>
- <span data-ttu-id="02af8-139">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="02af8-139">Time Tracking</span></span>
- <span data-ttu-id="02af8-140">Gasto básico</span><span class="sxs-lookup"><span data-stu-id="02af8-140">Basic Expense</span></span>
- <span data-ttu-id="02af8-141">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="02af8-141">Full Expense</span></span>
- <span data-ttu-id="02af8-142">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="02af8-142">Receipt OCR</span></span>
- <span data-ttu-id="02af8-143">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="02af8-143">Full Invoicing</span></span>
- <span data-ttu-id="02af8-144">Reconocimiento de ingresos</span><span class="sxs-lookup"><span data-stu-id="02af8-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="02af8-145">Pasos de implementación:</span><span class="sxs-lookup"><span data-stu-id="02af8-145">Deployment steps:</span></span>
<span data-ttu-id="02af8-146">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="02af8-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="02af8-147">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](resource-sign-up-preview-subscription.md) y [Aprovisionar un nuevo entorno](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="02af8-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="02af8-148">Project Operations para escenarios mantenidos en existencias/orden de producción</span><span class="sxs-lookup"><span data-stu-id="02af8-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="02af8-149">Planificación del proyecto usando WBS</span><span class="sxs-lookup"><span data-stu-id="02af8-149">Project planning using WBS</span></span>
- <span data-ttu-id="02af8-150">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="02af8-150">Resource Management</span></span>
- <span data-ttu-id="02af8-151">Seguimiento en el tiempo</span><span class="sxs-lookup"><span data-stu-id="02af8-151">Time Tracking</span></span>
- <span data-ttu-id="02af8-152">Gasto completo</span><span class="sxs-lookup"><span data-stu-id="02af8-152">Full Expense</span></span>
- <span data-ttu-id="02af8-153">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="02af8-153">Receipt OCR</span></span>
- <span data-ttu-id="02af8-154">Facturación completa</span><span class="sxs-lookup"><span data-stu-id="02af8-154">Full Invoicing</span></span>
- <span data-ttu-id="02af8-155">Reconocimiento de ingresos</span><span class="sxs-lookup"><span data-stu-id="02af8-155">Revenue Recognition</span></span>
- <span data-ttu-id="02af8-156">Órdenes de producción</span><span class="sxs-lookup"><span data-stu-id="02af8-156">Production Orders</span></span>
- <span data-ttu-id="02af8-157">Soporte de materiales</span><span class="sxs-lookup"><span data-stu-id="02af8-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="02af8-158">Pasos de implementación:</span><span class="sxs-lookup"><span data-stu-id="02af8-158">Deployment steps:</span></span>
<span data-ttu-id="02af8-159">Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="02af8-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="02af8-160">Para esta implementación, consulte [Registrarse para suscripciones de vista previa](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) y [Aprovisionar un nuevo entorno](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="02af8-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



