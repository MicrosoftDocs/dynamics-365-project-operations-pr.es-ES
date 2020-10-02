---
title: Campos de Project Operations como dimensiones de precios
description: En este tema se proporciona información sobre el uso de campos como dimensiones de precios en Dynamics 365 Project Operations.
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
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896437"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="e1fd7-103">Campos de Project Operations como dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="e1fd7-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="e1fd7-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="e1fd7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1fd7-105">La entidad **Datos reales** tiene muchos campos que se pueden usar como dimensiones de precios para los precios basados en recursos.</span><span class="sxs-lookup"><span data-stu-id="e1fd7-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="e1fd7-106">Por ejemplo, un campo común es **Recurso que se puede reservar**.</span><span class="sxs-lookup"><span data-stu-id="e1fd7-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="e1fd7-107">Es posible que las compañías más pequeñas, con menos de 20-30 recursos facturables, consideren que tener tasas de coste y facturas específicas para cada recurso es un enfoque más simple.</span><span class="sxs-lookup"><span data-stu-id="e1fd7-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="e1fd7-108">Sin embargo, a medida que crece el personal facturable, las tasas específicas de recursos podrían ser muy difícil de mantener.</span><span class="sxs-lookup"><span data-stu-id="e1fd7-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="e1fd7-109">El coste de los recursos y las tasas de facturación comienzan a variar a medida que los recursos ascienden, adquieran más experiencia o consiguen un conjunto de habilidades diferente.</span><span class="sxs-lookup"><span data-stu-id="e1fd7-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="e1fd7-110">Otro ejemplo es el de la categoría de transacción.</span><span class="sxs-lookup"><span data-stu-id="e1fd7-110">Another example is that of transaction category.</span></span> <span data-ttu-id="e1fd7-111">Los clientes y los implementadores han usado la categoría de transacción para clasificar el trabajo y usar el campo para determinar el precio y el coste según la categoría de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e1fd7-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
