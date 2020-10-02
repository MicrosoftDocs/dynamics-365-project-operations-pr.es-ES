---
title: Definir habilidades y competencias
description: En este tema se proporciona información sobre cómo configurar modelos de competencia para calificar recursos.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897652"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="0785b-103">Definir habilidades y competencias</span><span class="sxs-lookup"><span data-stu-id="0785b-103">Define skills and proficiencies</span></span>

<span data-ttu-id="0785b-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="0785b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0785b-105">Las habilidades son características de recursos que se comparten entre Dynamics 365 Project Operations y, si está presente, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="0785b-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="0785b-106">Para mantener el repositorio de habilidades en Project Operations, vaya a **Recursos** \> **Cualificaciones de recursos**.</span><span class="sxs-lookup"><span data-stu-id="0785b-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="0785b-107">Uso de modelos de competencia para calificar recursos</span><span class="sxs-lookup"><span data-stu-id="0785b-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="0785b-108">Las habilidades para los recursos se clasifican según los modelos de competencia.</span><span class="sxs-lookup"><span data-stu-id="0785b-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="0785b-109">Las calificaciones individuales se encuentran en un modelo de competencia.</span><span class="sxs-lookup"><span data-stu-id="0785b-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="0785b-110">Para crear un modelo de competencia, vaya a **Recursos** \> **Modelos de competencia** y, a continuación, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="0785b-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="0785b-111">En el nuevo modelo de calificación, especifique el valor mínimo y máximo de calificación y la entidad que se está calificando.</span><span class="sxs-lookup"><span data-stu-id="0785b-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="0785b-112">En la subcuadrícula **Valores de calificación**, puede definir los diferentes valores de calificación, desde el mínimo hasta el máximo.</span><span class="sxs-lookup"><span data-stu-id="0785b-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="0785b-113">Estos valores de calificación se muestran en los filtros **Requisitos de recursos**, **Tablero de programación** y **Asistente de programación**.</span><span class="sxs-lookup"><span data-stu-id="0785b-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
