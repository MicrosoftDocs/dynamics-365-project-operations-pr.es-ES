---
title: Habilidades y modelos de competencia
description: Este tema proporciona información sobre cómo usar las habilidades y los modelos de competencia.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008692"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="a08a8-103">Habilidades y modelos de competencia</span><span class="sxs-lookup"><span data-stu-id="a08a8-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a08a8-104">Las habilidades son características de recursos que se comparten entre Dynamics 365 Project Service Automation y, si está presente, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="a08a8-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="a08a8-105">Para mantener el repositorio de habilidades en Project Service Automation, vaya a **Recursos** \> **Cualificaciones de recursos**.</span><span class="sxs-lookup"><span data-stu-id="a08a8-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Cualificaciones de recursos](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="a08a8-107">Uso de modelos de competencia para calificar recursos</span><span class="sxs-lookup"><span data-stu-id="a08a8-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="a08a8-108">Las habilidades para los recursos se clasifican según los modelos de competencia.</span><span class="sxs-lookup"><span data-stu-id="a08a8-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="a08a8-109">Las calificaciones individuales se encuentran en un modelo de competencia.</span><span class="sxs-lookup"><span data-stu-id="a08a8-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="a08a8-110">Para crear un modelo de competencia, vaya a **Recursos** \> **Modelos de competencia** y, a continuación, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="a08a8-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="a08a8-111">En el nuevo modelo de calificación, especifique el valor mínimo y máximo de calificación y la entidad que se está calificando.</span><span class="sxs-lookup"><span data-stu-id="a08a8-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="a08a8-112">En la subcuadrícula **Valores de calificación**, puede definir los diferentes valores de calificación, desde el mínimo hasta el máximo.</span><span class="sxs-lookup"><span data-stu-id="a08a8-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Calificaciones mínimas y máximas definidas](media/Resource-Management-image85.png)

<span data-ttu-id="a08a8-114">Estos valores de calificación se muestran en los filtros **Requisitos de recursos**, **Tablero de programación** y **Asistente de programación**.</span><span class="sxs-lookup"><span data-stu-id="a08a8-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]