---
title: Campos de Project Operations como dimensiones de precios
description: En este tema se proporciona información sobre el uso de campos como dimensiones de precios en Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274659"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="17f2e-103">Campos de Project Operations como dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="17f2e-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="17f2e-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="17f2e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="17f2e-105">La entidad **Datos reales** tiene muchos campos que se pueden usar como dimensiones de precios para los precios basados en recursos.</span><span class="sxs-lookup"><span data-stu-id="17f2e-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="17f2e-106">Por ejemplo, un campo común es **Recurso que se puede reservar**.</span><span class="sxs-lookup"><span data-stu-id="17f2e-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="17f2e-107">Es posible que las compañías más pequeñas, con menos de 20-30 recursos facturables, consideren que tener tasas de coste y facturas específicas para cada recurso es un enfoque más simple.</span><span class="sxs-lookup"><span data-stu-id="17f2e-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="17f2e-108">Sin embargo, a medida que crece el personal facturable, las tasas específicas de recursos podrían ser muy difícil de mantener.</span><span class="sxs-lookup"><span data-stu-id="17f2e-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="17f2e-109">El coste de los recursos y las tasas de facturación comienzan a variar a medida que los recursos ascienden, adquieran más experiencia o consiguen un conjunto de habilidades diferente.</span><span class="sxs-lookup"><span data-stu-id="17f2e-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="17f2e-110">Otro ejemplo es el de la categoría de transacción.</span><span class="sxs-lookup"><span data-stu-id="17f2e-110">Another example is that of transaction category.</span></span> <span data-ttu-id="17f2e-111">Los clientes y los implementadores han usado la categoría de transacción para clasificar el trabajo y usar el campo para determinar el precio y el coste según la categoría de trabajo.</span><span class="sxs-lookup"><span data-stu-id="17f2e-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]