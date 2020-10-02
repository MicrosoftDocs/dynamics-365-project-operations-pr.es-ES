---
title: Configurar la creación de una factura automatizada
description: En este tema se proporciona información sobre cómo configurar el sistema para generar facturas automáticamente.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898147"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="1f5b1-103">Configurar la creación de una factura automatizada</span><span class="sxs-lookup"><span data-stu-id="1f5b1-103">Configure automated invoice creation</span></span>

<span data-ttu-id="1f5b1-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="1f5b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1f5b1-105">Complete los siguientes pasos para configurar una ejecución automática de facturas en Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="1f5b1-106">Vaya a **Configuración** \> **Trabajos por lotes**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="1f5b1-107">Cree un trabajo por lotes y asígnele el nombre **Creación de facturas de Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="1f5b1-108">El nombre del trabajo por lotes debe incluir el término "creación de facturas".</span><span class="sxs-lookup"><span data-stu-id="1f5b1-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="1f5b1-109">En el campo **Tipo de trabajo**, seleccione **Ninguno**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="1f5b1-110">De forma predeterminada, las opciones **Frecuencia diaria** y **Está activo** están configuradas con el valor **Sí**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="1f5b1-111">Seleccione **Ejecutar flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-111">Select **Run Workflow**.</span></span> <span data-ttu-id="1f5b1-112">En el cuadro de diálogo **Buscar registros**, se mostrarán tres flujos de trabajo:</span><span class="sxs-lookup"><span data-stu-id="1f5b1-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="1f5b1-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="1f5b1-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="1f5b1-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="1f5b1-114">ProcessRunner</span></span>
    - <span data-ttu-id="1f5b1-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="1f5b1-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="1f5b1-116">Seleccione **ProcessRunCaller** y después seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="1f5b1-117">En el siguiente cuadro de diálogo, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="1f5b1-118">El flujo de trabajo **Reposo** va seguido de un flujo de trabajo **Proceso**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="1f5b1-119">También puede seleccionar **ProcessRunner** en el paso 5.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="1f5b1-120">A continuación, cuando se selecciona **Aceptar**, el flujo de trabajo **Proceso** va seguido del flujo de trabajo **Reposo**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="1f5b1-121">Los flujos de trabajo **ProcessRunCaller** y **ProcessRunner** crean facturas.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="1f5b1-122">**ProcessRunCaller** llama a **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="1f5b1-123">**ProcessRunner** es el flujo de trabajo que crea realmente las facturas.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="1f5b1-124">Pasa por todas las líneas de contrato para las que se deben crear facturas y crea las facturas para dichas líneas.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="1f5b1-125">Para determinar las líneas de contrato para las que se deben crear facturas, el trabajo busca fechas de ejecución de facturas para las líneas de contrato.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="1f5b1-126">Si hay líneas de contrato que pertenecen a un contrato que tiene la misma fecha de ejecución de factura, las transacciones se combinarán en una factura con dos líneas de factura.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="1f5b1-127">Si no hay transacciones para crear facturas, el trabajo omite la creación de factura.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="1f5b1-128">Cuando finaliza la ejecución de **ProcessRunner**, se llama al flujo de trabajo **ProcessRunCaller**, que proporciona la hora de finalización y después se cierra.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="1f5b1-129">A continuación, **ProcessRunCaller** pone en marcha un temporizador que se ejecuta durante 24 horas desde la hora de finalización especificada.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="1f5b1-130">Cuando se agota el tiempo del temporizador, el flujo de trabajo **ProcessRunCaller** se cierra.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="1f5b1-131">El trabajo del proceso por lotes para la creación de facturas es un trabajo recurrente.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="1f5b1-132">Si este proceso por lotes se ejecuta muchas veces, se crean varias instancias del trabajo y se generan errores.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="1f5b1-133">Por lo tanto, debe iniciar el proceso por lotes solo una vez y debe reiniciarlo solo si se detiene su ejecución.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="1f5b1-134">La facturación por lotes solo se ejecuta para las líneas de contrato del proyecto que se configuran mediante programas de facturación.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="1f5b1-135">Una línea de contrato con un método de facturación de precio fijo debe tener hitos configurados.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="1f5b1-136">Una línea de contrato de proyecto con un método de facturación de tiempo y material necesitará una programación de facturación basada en fecha.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="1f5b1-137">Lo mismo se aplica a una línea de contrato basada en proyectos.</span><span class="sxs-lookup"><span data-stu-id="1f5b1-137">The same applies to a project-based contract line.</span></span>     
