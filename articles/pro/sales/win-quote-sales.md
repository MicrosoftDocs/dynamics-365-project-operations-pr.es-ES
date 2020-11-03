---
title: Cerrar ofertas
description: En este tema se proporciona información el cierre de una oferta en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085069"
---
# <a name="close-quotes"></a><span data-ttu-id="d7621-103">Cerrar ofertas</span><span class="sxs-lookup"><span data-stu-id="d7621-103">Close quotes</span></span> 

<span data-ttu-id="d7621-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="d7621-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d7621-105">Las ofertas de proyectos se pueden cerrar como Ganadas o Perdidas.</span><span class="sxs-lookup"><span data-stu-id="d7621-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="d7621-106">Las operaciones Activar y Revisar en ofertas no se admiten en Microsoft Dynamics 365 Project Operations, por lo que pueden cerrarse las ofertas en borrador.</span><span class="sxs-lookup"><span data-stu-id="d7621-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="d7621-107">Cierre de oferta como Ganada</span><span class="sxs-lookup"><span data-stu-id="d7621-107">Close a quote as Won</span></span>

<span data-ttu-id="d7621-108">Cerrar una oferta de proyecto como Ganada cerrará la oferta con el estado puesto en Cerrada y la razón para el estado en Ganada.</span><span class="sxs-lookup"><span data-stu-id="d7621-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="d7621-109">Cerrar las ofertas hace la oferta del proyecto de solo lectura y crea un borrador del contrato del proyecto que contiene la información de la oferta.</span><span class="sxs-lookup"><span data-stu-id="d7621-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="d7621-110">Debido a que una oferta cerrada no se puede volver a abrir, existe un diálogo de confirmación antes de que se realicen los cambios, ya que una oferta cerrada no se puede volver a abrir y los cambios son irreversibles.</span><span class="sxs-lookup"><span data-stu-id="d7621-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="d7621-111">Si la oferta se adjunta a una oportunidad, cualquier otra oferta de proyecto de la oportunidad se cierra automáticamente como Perdida.</span><span class="sxs-lookup"><span data-stu-id="d7621-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="d7621-112">Impacto financiero de cerrar una oferta como Ganada</span><span class="sxs-lookup"><span data-stu-id="d7621-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="d7621-113">Si ha habido datos reales del tiempo registrado en un proyecto mientras aún está adjunto a un presupuesto preliminar, solo se registra el coste del tiempo o el gasto.</span><span class="sxs-lookup"><span data-stu-id="d7621-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="d7621-114">Una vez que una oferta se cierra como Ganada, la aplicación refactorizará los costes al revertir los costes reales más antiguos y volver a crear nuevos costes reales.</span><span class="sxs-lookup"><span data-stu-id="d7621-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="d7621-115">La aplicación procesará estos costes reales según el método de facturación de la línea de contrato del proyecto asociado.</span><span class="sxs-lookup"><span data-stu-id="d7621-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="d7621-116">Si los costes reales hacen referencia a una línea de contrato de tiempo y material, el sistema creará automáticamente los correspondientes datos reales de ventas no facturadas para cuando se cierre la oferta y se cree el contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d7621-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="d7621-117">Si los costes reales hacen referencia a una línea de contrato de precio fijo, la aplicación dejará de volver a procesar los costes reales en función de las reglas de facturación dividida para los clientes del contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d7621-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="d7621-118">Cerrar una oferta como perdida:</span><span class="sxs-lookup"><span data-stu-id="d7621-118">Closing a quote as lost:</span></span>

<span data-ttu-id="d7621-119">Cerrar una oferta de proyecto como Perdida establecerá el estado de la oferta en Cerrado y la razón para el estado en Perdida.</span><span class="sxs-lookup"><span data-stu-id="d7621-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="d7621-120">Cerrar la oferta hace que la oferta del proyecto sea de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7621-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="d7621-121">Debido a que una oferta cerrada no se puede volver a abrir, antes de cerrar una oferta, un cuadro de diálogo de confirmación confirmará sus cambios.</span><span class="sxs-lookup"><span data-stu-id="d7621-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="d7621-122">Si la oferta del proyecto que se cierra como Perdido tiene un proyecto referenciado en cualquiera de sus líneas, ese proyecto también se marca como Cerrado y se cancelan las reservas de recursos desde ese día en adelante.</span><span class="sxs-lookup"><span data-stu-id="d7621-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="d7621-123">En Project Operations, cerrar una oferta como Ganada o Perdida no afectará el estado de la Oportunidad, que permanecerá abierta hasta que se cierre manualmente.</span><span class="sxs-lookup"><span data-stu-id="d7621-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
