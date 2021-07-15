---
title: 'Novedades de mayo de 2021: implementación simplificada de Project Operations'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de mayo de 2021 de la implementación simplificada de Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060454"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a><span data-ttu-id="abf9d-103">Novedades de mayo de 2021: implementación simplificada de Project Operations</span><span class="sxs-lookup"><span data-stu-id="abf9d-103">What's new May 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="abf9d-104">_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="abf9d-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abf9d-105">Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="abf9d-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

   - <span data-ttu-id="abf9d-106">Project Operations en el entorno de Dataverse versión 4.10.0.186.</span><span class="sxs-lookup"><span data-stu-id="abf9d-106">Project Operations on Dataverse environment version 4.10.0.186.</span></span>

## <a name="features-included-in-this-release"></a><span data-ttu-id="abf9d-107">Características incluidas en esta versión</span><span class="sxs-lookup"><span data-stu-id="abf9d-107">Features included in this release</span></span>

<span data-ttu-id="abf9d-108">En esta versión se incluyen las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="abf9d-108">The following features are included in this release:</span></span>

- <span data-ttu-id="abf9d-109">[Modos de programación](../../project-management/scheduling-modes.md): los directores de proyecto ahora pueden definir si un proyecto debe administrarse utilizando un modo de programación de duración fija, trabajo fijo o unidades fijas.</span><span class="sxs-lookup"><span data-stu-id="abf9d-109">[Scheduling modes](../../project-management/scheduling-modes.md): Project managers can now define if a project should be managed using a fixed duration, fixed work, or fixed units scheduling mode.</span></span>

## <a name="quality-updates"></a><span data-ttu-id="abf9d-110">Actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="abf9d-110">Quality updates</span></span>

| <span data-ttu-id="abf9d-111">**Área de características**</span><span class="sxs-lookup"><span data-stu-id="abf9d-111">**Feature area**</span></span> | <span data-ttu-id="abf9d-112">**Número de referencia**</span><span class="sxs-lookup"><span data-stu-id="abf9d-112">**Reference number**</span></span> | <span data-ttu-id="abf9d-113">**Actualización de calidad**</span><span class="sxs-lookup"><span data-stu-id="abf9d-113">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="abf9d-114">Facturación y precios</span><span class="sxs-lookup"><span data-stu-id="abf9d-114">Billing and pricing</span></span> | <span data-ttu-id="abf9d-115">2224568</span><span class="sxs-lookup"><span data-stu-id="abf9d-115">2224568</span></span> | <span data-ttu-id="abf9d-116">Lógica agregada para habilitar personalizaciones que implican invocar el complemento de confirmación de factura.</span><span class="sxs-lookup"><span data-stu-id="abf9d-116">Added logic to enable customizations that involve invoking the invoice confirmation plug-in.</span></span> |
| <span data-ttu-id="abf9d-117">Facturación y precios</span><span class="sxs-lookup"><span data-stu-id="abf9d-117">Billing and pricing</span></span> | <span data-ttu-id="abf9d-118">2101098</span><span class="sxs-lookup"><span data-stu-id="abf9d-118">2101098</span></span> | <span data-ttu-id="abf9d-119">Se mejoró la lógica de los campos predeterminados para la factura proforma.</span><span class="sxs-lookup"><span data-stu-id="abf9d-119">Improved the logic of default fields to proforma invoice.</span></span> <span data-ttu-id="abf9d-120">Estos campos incluyen, **Dirección de la facturación**, **Nombre de facturación**, y **Condiciones de pago**.</span><span class="sxs-lookup"><span data-stu-id="abf9d-120">These fields include, **Bill-to address**, **Bill to name**, and **Payment terms**.</span></span> <span data-ttu-id="abf9d-121">Los campos ahora predeterminados del registro de cliente del contrato de proyecto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="abf9d-121">The fields now default from the corresponding project contract customer record.</span></span> |
| <span data-ttu-id="abf9d-122">Facturación y precios</span><span class="sxs-lookup"><span data-stu-id="abf9d-122">Billing and pricing</span></span> | <span data-ttu-id="abf9d-123">2021413</span><span class="sxs-lookup"><span data-stu-id="abf9d-123">2021413</span></span> | <span data-ttu-id="abf9d-124">Se actualizaron los campos **Coste real** y **Ventas** en la entidad **Tarea** para incluir los valores de ventas de los gastos facturados y no facturados en las tareas.</span><span class="sxs-lookup"><span data-stu-id="abf9d-124">Updated the **Actual cost** and **Sales** fields on the **Task** entity to include sales values from unbilled and billed expenses on tasks.</span></span> |
| <span data-ttu-id="abf9d-125">Facturación y precios</span><span class="sxs-lookup"><span data-stu-id="abf9d-125">Billing and pricing</span></span> | <span data-ttu-id="abf9d-126">2182110</span><span class="sxs-lookup"><span data-stu-id="abf9d-126">2182110</span></span> | <span data-ttu-id="abf9d-127">Al copiar un contrato de proyecto, el identificador de la línea del contrato se vuelve a generar en el contrato del proyecto de destino para garantizar que sea único.</span><span class="sxs-lookup"><span data-stu-id="abf9d-127">When copying a project contract, the contract line ID is regenerated in the destination project contract to ensure it's unique.</span></span> |
| <span data-ttu-id="abf9d-128">Administración de oportunidades</span><span class="sxs-lookup"><span data-stu-id="abf9d-128">Opportunity Management</span></span> | <span data-ttu-id="abf9d-129">2186741</span><span class="sxs-lookup"><span data-stu-id="abf9d-129">2186741</span></span> | <span data-ttu-id="abf9d-130">Validaciones agregadas para garantizar que el campo **Origen** y Tipo de transacción no se puede actualizar en los detalles de la línea de cotización existente.</span><span class="sxs-lookup"><span data-stu-id="abf9d-130">Added validations to ensure the **Origin** field and transaction type can't be updated on existing quote line details.</span></span> |
| <span data-ttu-id="abf9d-131">Administración de oportunidades</span><span class="sxs-lookup"><span data-stu-id="abf9d-131">Opportunity Management</span></span> | <span data-ttu-id="abf9d-132">2191353</span><span class="sxs-lookup"><span data-stu-id="abf9d-132">2191353</span></span> | <span data-ttu-id="abf9d-133">No se debe permitir crear hitos en una línea de contrato de tiempo y material.</span><span class="sxs-lookup"><span data-stu-id="abf9d-133">Milestone creation must not be allowed on a time and material contract line.</span></span> |
| <span data-ttu-id="abf9d-134">Administración de oportunidades</span><span class="sxs-lookup"><span data-stu-id="abf9d-134">Opportunity Management</span></span> | <span data-ttu-id="abf9d-135">2216956</span><span class="sxs-lookup"><span data-stu-id="abf9d-135">2216956</span></span> | <span data-ttu-id="abf9d-136">Se resolvieron los problemas con **Actualizar precios**.</span><span class="sxs-lookup"><span data-stu-id="abf9d-136">Fixed issues with **Update prices**.</span></span> |
| <span data-ttu-id="abf9d-137">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="abf9d-137">Planning and Tracking</span></span> | <span data-ttu-id="abf9d-138">2182979</span><span class="sxs-lookup"><span data-stu-id="abf9d-138">2182979</span></span> | <span data-ttu-id="abf9d-139">Se mejoró la función de copia del proyecto para garantizar que las líneas de estimación de gastos se copien desde el proyecto original.</span><span class="sxs-lookup"><span data-stu-id="abf9d-139">Project copy function improved to ensure that expense estimate lines are copied from the original project.</span></span> |
| <span data-ttu-id="abf9d-140">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="abf9d-140">Planning and Tracking</span></span> | <span data-ttu-id="abf9d-141">2184144</span><span class="sxs-lookup"><span data-stu-id="abf9d-141">2184144</span></span> | <span data-ttu-id="abf9d-142">Se mejoró la función de copia del proyecto para garantizar el nombre de posición del recurso se copie desde el proyecto original.</span><span class="sxs-lookup"><span data-stu-id="abf9d-142">Project copy function improved to ensure the resource position name is copied from the original project.</span></span> |
| <span data-ttu-id="abf9d-143">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="abf9d-143">Planning and Tracking</span></span> | <span data-ttu-id="abf9d-144">2184799</span><span class="sxs-lookup"><span data-stu-id="abf9d-144">2184799</span></span> | <span data-ttu-id="abf9d-145">Control más estricto al copiar un proyecto para garantizar que la fecha de inicio estimada no se puede cambiar mientras se realiza la copia.</span><span class="sxs-lookup"><span data-stu-id="abf9d-145">Tightened the control when copying a project to ensure the estimated start date can't be changed while the copy is in progress.</span></span> |
| <span data-ttu-id="abf9d-146">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="abf9d-146">Planning and Tracking</span></span> | <span data-ttu-id="abf9d-147">2185134</span><span class="sxs-lookup"><span data-stu-id="abf9d-147">2185134</span></span> | <span data-ttu-id="abf9d-148">Durante la copia del proyecto, la fecha de inicio estimada del proyecto de destino se establece en la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="abf9d-148">During the copy of a project, the destination project estimated start date is set to today's date.</span></span> |
| <span data-ttu-id="abf9d-149">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="abf9d-149">Planning and Tracking</span></span> | <span data-ttu-id="abf9d-150">2196373</span><span class="sxs-lookup"><span data-stu-id="abf9d-150">2196373</span></span> | <span data-ttu-id="abf9d-151">Al copiar un proyecto, asegúrese de que los registros del director de proyectos y los miembros del equipo no estén duplicados en el equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="abf9d-151">Ensure project manager and team member records are not duplicated in the project team when copying a project.</span></span> |
| <span data-ttu-id="abf9d-152">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="abf9d-152">Planning and Tracking</span></span> | <span data-ttu-id="abf9d-153">2211833</span><span class="sxs-lookup"><span data-stu-id="abf9d-153">2211833</span></span> | <span data-ttu-id="abf9d-154">Las asignaciones de recursos se copian desde la tarea del proyecto de origen al proyecto de destino.</span><span class="sxs-lookup"><span data-stu-id="abf9d-154">Resource assignments are copied from the source project task to the destination project.</span></span> |
| <span data-ttu-id="abf9d-155">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="abf9d-155">Planning and Tracking</span></span> | <span data-ttu-id="abf9d-156">2186541</span><span class="sxs-lookup"><span data-stu-id="abf9d-156">2186541</span></span> | <span data-ttu-id="abf9d-157">Problemas resueltos en la cuadrícula **Estimaciones** al agrupar por **recurso**.</span><span class="sxs-lookup"><span data-stu-id="abf9d-157">Fixed issues in the **Estimates** grid when grouping by **Resource**.</span></span> |
| <span data-ttu-id="abf9d-158">Planificación y seguimiento</span><span class="sxs-lookup"><span data-stu-id="abf9d-158">Planning and Tracking</span></span> | <span data-ttu-id="abf9d-159">2166906</span><span class="sxs-lookup"><span data-stu-id="abf9d-159">2166906</span></span> | <span data-ttu-id="abf9d-160">La categoría de transacción de una tarea se debe copiar en la entidad **Asignación de recursos**.</span><span class="sxs-lookup"><span data-stu-id="abf9d-160">The transaction category from a task must be copied to the **Resource assignment** entity.</span></span> |
| <span data-ttu-id="abf9d-161">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="abf9d-161">Resource Management</span></span> | <span data-ttu-id="abf9d-162">2125362</span><span class="sxs-lookup"><span data-stu-id="abf9d-162">2125362</span></span> | <span data-ttu-id="abf9d-163">Se solucionaron problemas con la creación de un miembro del equipo genérico utilizando un método de asignación basado en horas.</span><span class="sxs-lookup"><span data-stu-id="abf9d-163">Fixed issues with creating a generic team member using the hours-based allocation method.</span></span> |
| <span data-ttu-id="abf9d-164">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="abf9d-164">Time and Expense</span></span> | <span data-ttu-id="abf9d-165">2113603</span><span class="sxs-lookup"><span data-stu-id="abf9d-165">2113603</span></span> | <span data-ttu-id="abf9d-166">Se solucionó el problema relacionado con la personalización con la eliminación de atributos de la página **Entrada de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="abf9d-166">Fixed customization-related issue with removing attributes from the **Time entry** page.</span></span> <span data-ttu-id="abf9d-167">El sistema verifica si el atributo existe en la página antes de acceder a él mediante un script.</span><span class="sxs-lookup"><span data-stu-id="abf9d-167">The system checks if the attribute exists on the page before accessing the attribute by using a script.</span></span> |
| <span data-ttu-id="abf9d-168">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="abf9d-168">Time and Expense</span></span> | <span data-ttu-id="abf9d-169">2204377</span><span class="sxs-lookup"><span data-stu-id="abf9d-169">2204377</span></span> | <span data-ttu-id="abf9d-170">Las hojas de horas copiadas deben mostrarse automáticamente cuando seleccione **Copiar semana**.</span><span class="sxs-lookup"><span data-stu-id="abf9d-170">Copied timesheets must show automatically when you select **Copy Week**.</span></span> |
| <span data-ttu-id="abf9d-171">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="abf9d-171">Time and Expense</span></span> | <span data-ttu-id="abf9d-172">2209059</span><span class="sxs-lookup"><span data-stu-id="abf9d-172">2209059</span></span> | <span data-ttu-id="abf9d-173">El campo **Estado** se puede editar para las entradas de tiempo de Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="abf9d-173">The **Status** field is editable for Dynamics 365 Field Service time entries.</span></span> |