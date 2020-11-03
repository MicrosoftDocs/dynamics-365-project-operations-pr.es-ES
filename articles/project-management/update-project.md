---
title: Actualizar un proyecto
description: En este tema se proporciona información sobre la actualización de proyectos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085003"
---
# <a name="update-a-project"></a><span data-ttu-id="ca8c3-103">Actualizar un proyecto</span><span class="sxs-lookup"><span data-stu-id="ca8c3-103">Update a project</span></span>

<span data-ttu-id="ca8c3-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="ca8c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ca8c3-105">A continuación se muestra un resumen de los campos que se pueden actualizar en un proyecto después de que se haya creado y las implicaciones aplicables de las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="ca8c3-106">Campos de detalle del proyecto</span><span class="sxs-lookup"><span data-stu-id="ca8c3-106">Project detail fields</span></span>

- <span data-ttu-id="ca8c3-107">**Nombre** el título del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="ca8c3-108">**Descripción** : una introducción general al proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="ca8c3-109">**Cliente** : la empresa a la que se entregará el proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="ca8c3-110">**Plantilla de calendario** : las horas laborables del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="ca8c3-111">Cuando se cambia el campo, se vuelve a calcular la programación completa.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="ca8c3-112">**Divisa** : la divisa del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="ca8c3-113">Este campo se predetermina en función de la moneda definida en la unidad de contratación.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="ca8c3-114">Cuando se actualiza la unidad de contratación, también se actualiza el campo.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="ca8c3-115">**Unidad de contratación** : unidad organizativa que representa el grupo o la división de la empresa responsable principalmente de lograr la venta y administrar la entrega del trabajo y los servicios al cliente.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="ca8c3-116">**Gerente de proyecto** : El miembro del equipo del proyecto que tiene autoridad para revisar y aprobar entradas de tiempo y gastos.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="ca8c3-117">Campos de estimación</span><span class="sxs-lookup"><span data-stu-id="ca8c3-117">Estimate fields</span></span>

- <span data-ttu-id="ca8c3-118">**Fecha estimada de inicio** : la fecha en que comenzará el proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="ca8c3-119">Cuando se actualiza este campo, las tareas del proyecto se moverán proporcionalmente con la nueva fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="ca8c3-120">**Fecha de finalización** : la fecha en la que el proyecto está programado para finalizar.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="ca8c3-121">**Esfuerzo** : el esfuerzo estimado del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="ca8c3-122">Cuando se agregan tareas al proyecto, este campo ya no se puede editar.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="ca8c3-123">**Coste laboral estimado** : el coste laboral estimado del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="ca8c3-124">Cuando se agregan costes laborales al proyecto, este campo ya no se puede editar.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="ca8c3-125">**Gastos estimados** : los gastos estimados del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="ca8c3-126">Cuando se agregan gastos al proyecto, este campo ya no se puede editar.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="ca8c3-127">Campos reales del proyecto</span><span class="sxs-lookup"><span data-stu-id="ca8c3-127">Project actual fields</span></span>
- <span data-ttu-id="ca8c3-128">**Inicio real** : la fecha en que comenzó el proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="ca8c3-129">**Finalización** : se actualizará cuando se complete un proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="ca8c3-130">Campos de estado del proyecto</span><span class="sxs-lookup"><span data-stu-id="ca8c3-130">Project status fields</span></span>

- <span data-ttu-id="ca8c3-131">**Estado general del proyecto** : el estado general del proyecto proporcionado por el administrador del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="ca8c3-132">**Comentarios** : una narración sobre el estado actual del proyecto proporcionada por el administrador del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8c3-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

