---
title: Crear una plantilla de horas de trabajo
description: Este tema explica cómo crear una plantilla de horas laborables en Project Service.
author: ruhercul
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997217"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="7d67d-103">Crear una plantilla de horas laborables (Project Service)</span><span class="sxs-lookup"><span data-stu-id="7d67d-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7d67d-104">Para crear y administrar un proyecto, debe aplicar una plantilla de calendario al proyecto.</span><span class="sxs-lookup"><span data-stu-id="7d67d-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="7d67d-105">La plantilla de calendario define los siguientes atributos del proyecto:</span><span class="sxs-lookup"><span data-stu-id="7d67d-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="7d67d-106">Horas laborables, incluida la hora de inicio y finalización</span><span class="sxs-lookup"><span data-stu-id="7d67d-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="7d67d-107">Días laborables</span><span class="sxs-lookup"><span data-stu-id="7d67d-107">Working days</span></span>
- <span data-ttu-id="7d67d-108">Excepciones de calendario, como días no laborables</span><span class="sxs-lookup"><span data-stu-id="7d67d-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="7d67d-109">La plantilla de calendario que se aplica a un proyecto es una copia de la plantilla de calendario definida en la configuración de su organización.</span><span class="sxs-lookup"><span data-stu-id="7d67d-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="7d67d-110">Si cambia la plantilla del calendario, esos cambios no se propagan a las horas laborables del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7d67d-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="7d67d-111">Para cambiar las horas laborables del proyecto se debe aplicar una nueva plantilla.</span><span class="sxs-lookup"><span data-stu-id="7d67d-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="7d67d-112">Para crear una plantilla de calendario para su organización, existen dos requisitos clave:</span><span class="sxs-lookup"><span data-stu-id="7d67d-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="7d67d-113">Defina las horas laborables deseadas de la plantilla utilizando un recurso que se puede reservar nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="7d67d-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="7d67d-114">Cree una nueva plantilla de calendario y asóciela con el recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="7d67d-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="7d67d-115">**Defina las horas laborables de la plantilla**</span><span class="sxs-lookup"><span data-stu-id="7d67d-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="7d67d-116">Vaya a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="7d67d-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="7d67d-117">Cree un nuevo recurso al que hacer referencia en la plantilla de calendario o seleccione un recurso existente.</span><span class="sxs-lookup"><span data-stu-id="7d67d-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="7d67d-118">Seleccione la pestaña **Horas laborables** del recurso y complete las instrucciones de [Establecer horas laborables para un recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar las reglas del calendario.</span><span class="sxs-lookup"><span data-stu-id="7d67d-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="7d67d-119">**Cree una nueva plantilla de calendario**</span><span class="sxs-lookup"><span data-stu-id="7d67d-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="7d67d-120">Vaya a **Configuración** \> **Plantilla de calendario**.</span><span class="sxs-lookup"><span data-stu-id="7d67d-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="7d67d-121">Seleccione **Nuevo** e ingrese un nombre, una descripción y un recurso de plantilla.</span><span class="sxs-lookup"><span data-stu-id="7d67d-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="7d67d-122">Cuando se hace referencia a un recurso en una plantilla de calendario, se asocia una copia del calendario del recurso con la plantilla de calendario.</span><span class="sxs-lookup"><span data-stu-id="7d67d-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="7d67d-123">Si cambian las horas laborables de la plantilla copiada, esos cambios no se propagarán a la plantilla del calendario.</span><span class="sxs-lookup"><span data-stu-id="7d67d-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="7d67d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d67d-124">See Also</span></span>  
 [<span data-ttu-id="7d67d-125">Configuración de recursos</span><span class="sxs-lookup"><span data-stu-id="7d67d-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
