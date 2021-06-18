---
title: Definir calendarios de proyectos
description: Este tema proporciona información sobre cómo aplicar una plantilla de calendario a un proyecto para realizar un seguimiento de la programación del proyecto.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999017"
---
# <a name="define-project-calendars"></a><span data-ttu-id="2d4c0-103">Definir calendarios de proyectos</span><span class="sxs-lookup"><span data-stu-id="2d4c0-103">Define project calendars</span></span>

<span data-ttu-id="2d4c0-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="2d4c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2d4c0-105">Para crear y administrar un proyecto, debe aplicar una plantilla de calendario al proyecto.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="2d4c0-106">La plantilla de calendario define los siguientes atributos del proyecto:</span><span class="sxs-lookup"><span data-stu-id="2d4c0-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="2d4c0-107">Horas laborables, incluida la hora de inicio y finalización</span><span class="sxs-lookup"><span data-stu-id="2d4c0-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="2d4c0-108">Días laborables</span><span class="sxs-lookup"><span data-stu-id="2d4c0-108">Working days</span></span>
- <span data-ttu-id="2d4c0-109">Excepciones de calendario, como días no laborables</span><span class="sxs-lookup"><span data-stu-id="2d4c0-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="2d4c0-110">La plantilla de calendario que se aplica a un proyecto es una copia de la plantilla de calendario definida en la configuración de su organización.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="2d4c0-111">Si cambia la plantilla del calendario, esos cambios no se propagan a las horas laborables del proyecto.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="2d4c0-112">Para cambiar las horas laborables del proyecto se debe aplicar una nueva plantilla.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="2d4c0-113">Para crear una plantilla de calendario para su organización, existen dos requisitos clave:</span><span class="sxs-lookup"><span data-stu-id="2d4c0-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="2d4c0-114">Defina las horas laborables deseadas de la plantilla utilizando un recurso que se puede reservar nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="2d4c0-115">Cree una nueva plantilla de calendario y asóciela con el recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="2d4c0-116">**Defina las horas laborables de la plantilla**</span><span class="sxs-lookup"><span data-stu-id="2d4c0-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="2d4c0-117">Vaya a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="2d4c0-118">Cree un nuevo recurso al que hacer referencia en la plantilla de calendario o seleccione un recurso existente.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="2d4c0-119">Seleccione la pestaña **Horas laborables** del recurso y complete las instrucciones de [Establecer horas laborables para un recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar las reglas del calendario.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="2d4c0-120">**Cree una nueva plantilla de calendario**</span><span class="sxs-lookup"><span data-stu-id="2d4c0-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="2d4c0-121">Vaya a **Configuración** \> **Plantilla de calendario**.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="2d4c0-122">Seleccione **Nuevo** e ingrese un nombre, una descripción y un recurso de plantilla.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="2d4c0-123">Cuando se hace referencia a un recurso en una plantilla de calendario, se asocia una copia del calendario del recurso con la plantilla de calendario.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="2d4c0-124">Si cambian las horas laborables de la plantilla copiada, esos cambios no se propagarán a la plantilla del calendario.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="2d4c0-125">Ahora puede asociar la plantilla de trabajo con una plantilla de calendario de proyecto.</span><span class="sxs-lookup"><span data-stu-id="2d4c0-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

