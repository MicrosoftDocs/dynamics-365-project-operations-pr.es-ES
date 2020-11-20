---
title: ¿Cómo personalizo el flujo de proceso de negocio de las fases del proyecto?
description: Información general sobre cómo personalizar el flujo de proceso de negocio de fases del proyecto?
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125064"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="5fe6d-103">¿Cómo personalizo el flujo de proceso de negocio de las fases del proyecto?</span><span class="sxs-lookup"><span data-stu-id="5fe6d-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="5fe6d-104">Existe una limitación conocida en versiones anteriores de la aplicación Project Service que los nombres de las fases en el flujo de proceso de negocio de las fases de proyecto deben coincidir exactamente con los nombres esperados en inglés (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="5fe6d-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="5fe6d-105">En caso contrario, la lógica de negocios, que se basan en nombres de fases en inglés, no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="5fe6d-106">Por eso no se ven acciones familiares como **Cambiar proceso** o **Editar proceso** disponibles en el formulario de proyecto, y no se fomenta la personalización del flujo de proceso de negocio.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="5fe6d-107">Esta limitación se ha abordado en la versión 2.4.5.48 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="5fe6d-108">Este artículo ofrece las soluciones alternativas sugeridas si necesita personalizar el flujo de proceso de negocio predeterminado para versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="5fe6d-109">La lógica de negocios requiere un coincidencia exacta con nombres de fases en inglés</span><span class="sxs-lookup"><span data-stu-id="5fe6d-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="5fe6d-110">El flujo de proceso de negocio de las fases del proyecto incluye lógica de negocios que controla los comportamientos siguientes en la aplicación:</span><span class="sxs-lookup"><span data-stu-id="5fe6d-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="5fe6d-111">Cuando el proyecto se asocia a una oferta, el código establece el flujo de proceso de negocio en la fase **Quote**.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="5fe6d-112">Cuando el proyecto se asocia a un contrato, el código establece el flujo de proceso de negocio en la fase **Plan**.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="5fe6d-113">Cuando el flujo de proceso de negocio avanza a la fase **Close** , se desactiva el registro de proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="5fe6d-114">Cuando se desactiva el proyecto, el formulario y la estructura de descomposición del trabajo (WBS) del proyecto se establecen en de solo lectura, se liberan las reservas de recurso con nombre y se desactivan las listas de precios asociadas.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="5fe6d-115">Esta lógica de negocios se basa en los nombres ingleses para las fases del proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="5fe6d-116">Esta dependencia de los nombres de fases ingleses es la razón principal por la que la personalización del flujo de proceso de negocio de las fases de proyecto no se recomienda, además de la razón por la que no ve acciones de flujo de proceso de negocio comunes como **Cambiar proceso** o **Editar proceso** en la entidad del proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="5fe6d-117">¿Qué sucede si no coinciden los nombres de fases con los nombres ingleses?</span><span class="sxs-lookup"><span data-stu-id="5fe6d-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="5fe6d-118">En la aplicación Project Service versión 1.x en la plataforma 8.2, cuando no coinciden exactamente los nombres de fases en el flujo de proceso de negocio con los nombres de fases en inglés, se omite la lógica de negocios que establece la fase adecuada para ofertas o contratos, o que cierra el proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="5fe6d-119">No se muestra ningún mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-119">No error messages are displayed.</span></span> <span data-ttu-id="5fe6d-120">Por lo tanto parece que puede personalizar el flujo de proceso de negocio de las fases del proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="5fe6d-121">Sin embargo, no verá ninguno de los procesos automáticos trabajando para citas, contratos, y cierre de proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="5fe6d-122">En la aplicación Project Service versión 2.4.4.30 o anterior en la plataforma 9.0, se produjo un cambio arquitectónico relevante para los flujos de proceso de negocio, que requerían una reescritura de la lógica de negocios de flujo de proceso de negocio.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="5fe6d-123">Por ello, si no coinciden los nombres de fases de procesos con los nombres ingleses esperados, aparece un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="5fe6d-124">Por tanto, si desea personalizar el flujo de proceso de negocio de las fases de proyecto para la entidad de proyecto, solo puede agregar nuevas fases al flujo de proceso de negocio predeterminado para la entidad de proyecto, manteniendo las fases **Quote**, **Plan** y **Close** como se encuentran.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="5fe6d-125">Esta restricción garantiza que no recibe errores de la lógica de negocios que espera los nombres de fases ingleses en el flujo de proceso de negocio.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="5fe6d-126">En la versión 2.4.5.48 o versiones posteriores, la lógica de negocios descrita en este artículo se ha quitado del flujo de proceso de negocio predeterminado para la entidad de proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="5fe6d-127">La actualización a esa versión o posterior le permitirá personalizar o reemplazar el flujo de proceso de negocio predeterminado con uno propio.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="5fe6d-128">Soluciones alternativas para versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="5fe6d-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="5fe6d-129">Si la actualización no es una opción, puede personalizar el flujo de proceso de negocio de las fases de proyecto para la entidad de proyecto de una de estas dos formas:</span><span class="sxs-lookup"><span data-stu-id="5fe6d-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="5fe6d-130">Agregue fases adicionales a la configuración predeterminada, manteniendo los nombres de fases ingleses para **Quote**, **Plan** y **Close**.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Captura de pantalla de cómo agregar fases a la configuración predeterminada](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="5fe6d-132">Cree su propio flujo de proceso de negocio y conviértalo en el flujo de proceso de negocio principal para la entidad de proyecto, lo que le permite tener los nombres de etapa que desee.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="5fe6d-133">Sin embargo, si desea usar las mismas fases estándar de proyecto **Quote**, **Plan** y **Close**, necesita realizar algunas personalizaciones que se toman de sus nombres de fases personalizados.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="5fe6d-134">La lógica más compleja está en el cierre del proyecto, que usted puede desencadenar desactivando el registro del proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Personalización de BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="5fe6d-136">Consideraciones adicionales para la aplicación Project Service versión 2.4.4.30 o anterior en la plataforma 9.0</span><span class="sxs-lookup"><span data-stu-id="5fe6d-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="5fe6d-137">En Project Service 2.4.4.30 o anterior en la plataforma 9.0, con un flujo de proceso de negocio personalizado, el campo **Nombre de fase** en la entidad de proyecto usada en las vistas de gráfico y lista de proyecto **Proyecto por fase** no se actualizará porque está emparejado con el flujo de proceso de negocio predeterminado de las fases del proyecto.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="5fe6d-138">Puede resolver este problema con los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5fe6d-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="5fe6d-139">Agregue un campo personalizado para capturar la fase actual del flujo de proceso de negocio que se actualiza cuando el usuario avanza a través del flujo de proceso de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="5fe6d-140">Modifique el gráfico **Proyecto por fase** para trabajar con el campo personalizado en lugar de la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="5fe6d-141">Pasos para crear su propio flujo de proceso de negocio para la entidad de proyecto</span><span class="sxs-lookup"><span data-stu-id="5fe6d-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="5fe6d-142">Siga estas instrucciones para crear su propio flujo de proceso de negocio para la entidad de proyecto:</span><span class="sxs-lookup"><span data-stu-id="5fe6d-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="5fe6d-143">Vaya a **Configuración** > **Centro de procesos**.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="5fe6d-144">No copie el flujo de proceso de negocio de las fases de proyecto porque también se copiará la lógica de negocio de Project Service.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Crear proceso](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="5fe6d-146">Use el diseñador del proceso para crear los nombres de fases que desee.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="5fe6d-147">Si desea la misma funcionalidad que las fases predeterminadas para **Quote**, **Plan** y **Close**, tendrá que crearla basada en los nombres de fase del flujo de proceso de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Captura de pantalla del diseñador del proceso usado para personalizar BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="5fe6d-149">En el diseñador del proceso, haga clic en **Ordenar flujo de proceso** para convertir el flujo de proceso de negocio personalizado en el flujo de proceso de negocio principal para la entidad de proyecto moviéndolo por el flujo de proceso de negocio de las fases del proyecto hasta la parte superior de la lista.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="5fe6d-150">Captura de pantalla del uso de Ordenar flujo de proceso</span><span class="sxs-lookup"><span data-stu-id="5fe6d-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="5fe6d-151">Los pasos siguientes se aplican a la aplicación Project Service 2.4.4.30 o anterior de la plataforma 9.0</span><span class="sxs-lookup"><span data-stu-id="5fe6d-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="5fe6d-152">Agregue un nuevo campo personalizado a la entidad de proyecto para capturar las fases personalizadas en el flujo de proceso de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="5fe6d-153">Deberá agregar lógica de negocios (complemento/flujo de trabajo) para actualizar este campo cuando la fase del flujo de proceso de negocio personalizado se actualice.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Captura de pantalla de personalizar la entidad de proyecto](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="5fe6d-155">Modificar el gráfico **Proyecto por fase** para usar su nuevo campo personalizado para fases.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Captura de pantalla de usar el gráfico Proyecto por fase](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="5fe6d-157">Modifique cualquier vista de la entidad de proyecto para incluir su nuevo campo personalizado para fases.</span><span class="sxs-lookup"><span data-stu-id="5fe6d-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Captura de pantalla de cómo modificar vistas en la entidad de proyecto](media/FAQ-Customize-BPF-8-720.png)

