---
title: Eliminar una estimación de proyecto
description: Este tema proporciona información sobre cómo eliminar una estimación de proyecto una vez que se ha completado.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006937"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="11841-103">Eliminar una estimación de proyecto</span><span class="sxs-lookup"><span data-stu-id="11841-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11841-104">Las estimaciones del proyecto proporcionan la vista financiera del trabajo estimado y programado para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="11841-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="11841-105">Para trabajar con estimaciones para un proyecto, debe adjuntar el proyecto a un proyecto de estimación.</span><span class="sxs-lookup"><span data-stu-id="11841-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="11841-106">Un proyecto de estimación siempre se basa en un proyecto existente, sin embargo, varios proyectos pueden referirse a un solo proyecto de estimación.</span><span class="sxs-lookup"><span data-stu-id="11841-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="11841-107">Solo se pueden adjuntar proyectos de inversión y de precio fijo a los proyectos de estimación, y esos proyectos deben pertenecer al mismo grupo de proyectos que el proyecto de estimación.</span><span class="sxs-lookup"><span data-stu-id="11841-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="11841-108">Para eliminar un proyecto de presupuesto, debe estar completo.</span><span class="sxs-lookup"><span data-stu-id="11841-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="11841-109">Los siguientes pasos explican cómo eliminar una estimación.</span><span class="sxs-lookup"><span data-stu-id="11841-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="11841-110">Vaya a **Gestión de proyectos y contabilidad** > **Todos los proyectos** y abra el proyecto.</span><span class="sxs-lookup"><span data-stu-id="11841-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="11841-111">En la pestaña **Gestionar**, seleccione **Estimaciones**, y en la página **Estimación** seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="11841-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="11841-112">En la página **Eliminar estimación** en la pestaña **General**, configure las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="11841-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="11841-113">**Código de período**: seleccione el código de período para elegir los proyectos de estimación adecuados.</span><span class="sxs-lookup"><span data-stu-id="11841-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="11841-114">**Fecha estimada**: seleccione la fecha estimada adecuada para la eliminación.</span><span class="sxs-lookup"><span data-stu-id="11841-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="11841-115">**Eliminar con advertencias WIP**: habilite esta opción para proporcionar una notificación cuando se elimine una estimación asociada con un trabajo en curso (WIP).</span><span class="sxs-lookup"><span data-stu-id="11841-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="11841-116">Cuando esta opción no está habilitada, la eliminación no puede continuar si existen transacciones no estimadas.</span><span class="sxs-lookup"><span data-stu-id="11841-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="11841-117">Esta opción está disponible solo cuando la eliminación se aplica a un proyecto de estimación.</span><span class="sxs-lookup"><span data-stu-id="11841-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="11841-118">No está disponible si utiliza contabilizaciones periódicas.</span><span class="sxs-lookup"><span data-stu-id="11841-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="11841-119">Esta configuración funciona con la configuración de la pestaña **Estimación** en la página **Parámetros del proyecto**, en el grupo de campo **Permitir la eliminación cuando existan transacciones no estimadas**.</span><span class="sxs-lookup"><span data-stu-id="11841-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="11841-120">**Establecer escenario para Terminado**: habilite esta opción para establecer la etapa del proyecto de estimación en **Terminado** después de ejecutar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="11841-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="11841-121">**Imprimir lista de estimación**: seleccione la información que se incluirá cuando se imprima la lista de estimación.</span><span class="sxs-lookup"><span data-stu-id="11841-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="11841-122">**Mostrar Infolog**: habilite esta opción para mostrar el Infolog.</span><span class="sxs-lookup"><span data-stu-id="11841-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="11841-123">**Fecha de publicación**: elija la fecha de registro del libro mayor del presupuesto.</span><span class="sxs-lookup"><span data-stu-id="11841-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="11841-124">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="11841-124">Select **OK**.</span></span>
5. <span data-ttu-id="11841-125">Una vez completado el proceso de eliminación, el proyecto de estimación eliminado se muestra con un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="11841-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="11841-126">Si no tenía la intención de eliminar una estimación, puede seleccionar la estimación eliminada y seleccionar **Eliminación inversa**.</span><span class="sxs-lookup"><span data-stu-id="11841-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]