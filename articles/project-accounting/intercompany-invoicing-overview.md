---
title: Información general de facturación con empresas vinculadas
description: En este tema se proporciona información y ejemplos sobre la facturación con empresas vinculadas para proyectos.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595559"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="473ab-103">Información general de facturación con empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="473ab-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="473ab-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="473ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="473ab-105">Su organización puede tener varias divisiones, subsidiarias y otras entidades jurídicas que se transfieren productos y servicios entre sí para proyectos.</span><span class="sxs-lookup"><span data-stu-id="473ab-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="473ab-106">La entidad jurídica que proporciona el servicio o producto se denomina *entidad jurídica prestamista*.</span><span class="sxs-lookup"><span data-stu-id="473ab-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="473ab-107">La entidad jurídica que recibe el servicio o producto se denomina *entidad jurídica prestataria*.</span><span class="sxs-lookup"><span data-stu-id="473ab-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="473ab-108">La siguiente ilustración muestra un escenario típico en el que dos entidades jurídicas, Contoso Robotics USA (la entidad jurídica prestataria) y Contoso Robotics UK (la entidad jurídica prestamista) comparten recursos para entregar un proyecto para el cliente, Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="473ab-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="473ab-109">Para este escenario, se ha contratado a Contoso Robotics USA para entregar el trabajo a Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="473ab-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Facturación con empresas vinculadas](./media/IntercompanyScenario.png) 

<span data-ttu-id="473ab-111">Dynamics 365 Project Operations utiliza el siguiente flujo para procesar transacciones entre empresas vinculadas:</span><span class="sxs-lookup"><span data-stu-id="473ab-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="473ab-112">Los recursos de la entidad jurídica prestamista registran las transacciones de tiempo o gasto de empresas vinculadas reservando el tiempo y el gasto para proyectos en la entidad jurídica prestataria.</span><span class="sxs-lookup"><span data-stu-id="473ab-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="473ab-113">Los costes de tiempo y gasto se registran en la empresa prestamista utilizando la lista de precios de coste unitario de la empresa prestataria.</span><span class="sxs-lookup"><span data-stu-id="473ab-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="473ab-114">Las transacciones de venta sin facturar de empresas vinculadas se registran en la empresa prestamista utilizando la lista de precios de coste unitario de la empresa prestataria.</span><span class="sxs-lookup"><span data-stu-id="473ab-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="473ab-115">Los ingresos sin facturar se registran en la empresa prestataria utilizando la lista de precios de venta del contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="473ab-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="473ab-116">Se puede facturar al cliente cuando se registran los ingresos no facturados.</span><span class="sxs-lookup"><span data-stu-id="473ab-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="473ab-117">El cliente no tiene que esperar hasta que se complete el procesamiento de facturas de empresas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="473ab-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="473ab-118">Las facturas de clientes de empresas vinculadas se crean periódicamente en la empresa prestamista.</span><span class="sxs-lookup"><span data-stu-id="473ab-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="473ab-119">Las facturas se crean manualmente o mediante un proceso automatizado periódico.</span><span class="sxs-lookup"><span data-stu-id="473ab-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="473ab-120">Se puede crear una sola factura para cada entidad legal prestataria o se pueden crear facturas independientes por proyecto.</span><span class="sxs-lookup"><span data-stu-id="473ab-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="473ab-121">Cuando la factura del cliente de empresas vinculadas se registra en la entidad jurídica prestamista, se crea la factura de proveedor pendiente correspondiente en la entidad jurídica prestataria.</span><span class="sxs-lookup"><span data-stu-id="473ab-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="473ab-122">Los costes de la factura de proveedor pendiente se registrarán en el libro auxiliar del proyecto cuando se registre la factura.</span><span class="sxs-lookup"><span data-stu-id="473ab-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="473ab-123">El siguiente diagrama muestra la facturación de empresas vinculadas en relación con los eventos contables y los registros previstos en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="473ab-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Flujo de empresas vinculadas](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="473ab-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="473ab-125">Additional resources</span></span>

- [<span data-ttu-id="473ab-126">Configurar la facturación con empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="473ab-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="473ab-127">Registrar transacciones de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="473ab-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="473ab-128">Crear facturas de proveedores y clientes de empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="473ab-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
