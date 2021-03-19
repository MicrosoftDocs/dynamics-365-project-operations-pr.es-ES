---
title: Cerrar una oferta (lite)
description: En este tema se proporciona información el cierre de una oferta en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272308"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="a07ea-103">Cerrar una oferta (lite)</span><span class="sxs-lookup"><span data-stu-id="a07ea-103">Close a quote - lite</span></span>

<span data-ttu-id="a07ea-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="a07ea-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a07ea-105">Las ofertas de proyectos se pueden cerrar como Ganadas o Perdidas.</span><span class="sxs-lookup"><span data-stu-id="a07ea-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="a07ea-106">Un borrador de oferta se puede cerrar porque en Microsoft Dynamics 365 Project Operations no se admiten las operaciones Activar y Revisar en las ofertas.</span><span class="sxs-lookup"><span data-stu-id="a07ea-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="a07ea-107">Cierre de oferta como Ganada</span><span class="sxs-lookup"><span data-stu-id="a07ea-107">Close a quote as Won</span></span>

<span data-ttu-id="a07ea-108">Al cerrar una oferta de proyecto como Lograda, el estado se establece en Cerrada y la razón para el estado será Lograda.</span><span class="sxs-lookup"><span data-stu-id="a07ea-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="a07ea-109">Cerrar las ofertas hace la oferta del proyecto de solo lectura y crea un borrador del contrato del proyecto que contiene la información de la oferta.</span><span class="sxs-lookup"><span data-stu-id="a07ea-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="a07ea-110">Puesto que una oferta cerrada no se puede volver a abrir, los cambios se confirmarán con un cuadro de diálogo de confirmación.</span><span class="sxs-lookup"><span data-stu-id="a07ea-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a07ea-111">Si la oferta se adjunta a una oportunidad, cualquier otra oferta de proyecto de la oportunidad se cierra automáticamente como Perdida.</span><span class="sxs-lookup"><span data-stu-id="a07ea-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="a07ea-112">Impacto financiero de cerrar una oferta como Ganada</span><span class="sxs-lookup"><span data-stu-id="a07ea-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="a07ea-113">Si hay datos reales de tiempo en un proyecto mientras aún está adjunto a un borrador de oferta, solo se registra el coste del tiempo o gasto.</span><span class="sxs-lookup"><span data-stu-id="a07ea-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="a07ea-114">Una vez que una oferta se cierra como Ganada, la aplicación refactorizará los costes al revertir los costes reales más antiguos y volver a crear nuevos costes reales.</span><span class="sxs-lookup"><span data-stu-id="a07ea-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="a07ea-115">La aplicación procesará estos costes reales según el método de facturación de la línea de contrato del proyecto asociado.</span><span class="sxs-lookup"><span data-stu-id="a07ea-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="a07ea-116">Si los datos reales de costes hacen referencia a una línea de contrato de tiempo y material, se crean los datos reales de ventas no facturados correspondientes para cuando se cierre la cotización y se cree el contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="a07ea-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="a07ea-117">Si el coste real hace referencia a una línea de contrato de precio fijo, la aplicación dejará de volver a procesar los costes reales que se basan en las reglas de facturación divididas para los clientes del contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="a07ea-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="a07ea-118">Cerrar una oferta como perdida:</span><span class="sxs-lookup"><span data-stu-id="a07ea-118">Closing a quote as lost:</span></span>

<span data-ttu-id="a07ea-119">Al cerrar una oferta de proyecto como Perdida, el estado se establece en Cerrada y la razón para el estado será Perdida.</span><span class="sxs-lookup"><span data-stu-id="a07ea-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="a07ea-120">Cerrar la oferta hace que la oferta del proyecto sea de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a07ea-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="a07ea-121">Debido a que una oferta cerrada no se puede volver a abrir, antes de cerrar una oferta, un cuadro de diálogo de confirmación confirmará sus cambios.</span><span class="sxs-lookup"><span data-stu-id="a07ea-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a07ea-122">Si la oferta de proyecto que se cierra como Perdida hace referencia a un proyecto en cualquiera de sus líneas, ese proyecto también se marcará como Cerrado.</span><span class="sxs-lookup"><span data-stu-id="a07ea-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="a07ea-123">Se cancelan todas las reservas de recursos a partir de ese día.</span><span class="sxs-lookup"><span data-stu-id="a07ea-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="a07ea-124">En Project Operations, cerrar una oferta como Ganada o Perdida no afectará el estado de la Oportunidad, que permanecerá abierta hasta que se cierre manualmente.</span><span class="sxs-lookup"><span data-stu-id="a07ea-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]