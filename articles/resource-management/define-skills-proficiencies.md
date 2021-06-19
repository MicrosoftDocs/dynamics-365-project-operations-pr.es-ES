---
title: Definir habilidades y competencias
description: En este tema se proporciona información sobre cómo configurar modelos de competencia para calificar recursos.
author: ruhercul
ms.date: 09/23/2020
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
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015352"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="0d054-103">Definir habilidades y competencias</span><span class="sxs-lookup"><span data-stu-id="0d054-103">Define skills and proficiencies</span></span>

<span data-ttu-id="0d054-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="0d054-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d054-105">Las habilidades son características de recursos que se comparten entre Dynamics 365 Project Operations y, si está presente, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="0d054-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="0d054-106">Para mantener el repositorio de habilidades en Project Operations, vaya a **Recursos** \> **Cualificaciones de recursos**.</span><span class="sxs-lookup"><span data-stu-id="0d054-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="0d054-107">Uso de modelos de competencia para calificar recursos</span><span class="sxs-lookup"><span data-stu-id="0d054-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="0d054-108">Las cualificaciones de recursos se clasifican mediante modelos de eficacia.</span><span class="sxs-lookup"><span data-stu-id="0d054-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="0d054-109">Las calificaciones individuales se encuentran en un modelo de competencia.</span><span class="sxs-lookup"><span data-stu-id="0d054-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="0d054-110">Para crear un modelo de competencia, vaya a **Recursos** \> **Modelos de competencia** y, a continuación, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="0d054-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="0d054-111">En el nuevo modelo de calificación, especifique el valor mínimo y máximo de calificación y la entidad que se está calificando.</span><span class="sxs-lookup"><span data-stu-id="0d054-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="0d054-112">En la subcuadrícula **Valores de clasificación**, puede definir los diferentes valores de clasificación, desde el mínimo hasta el máximo.</span><span class="sxs-lookup"><span data-stu-id="0d054-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="0d054-113">Estos valores de calificación se muestran en los filtros **Requisitos de recursos**, **Tablero de programación** y **Asistente de programación**.</span><span class="sxs-lookup"><span data-stu-id="0d054-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]