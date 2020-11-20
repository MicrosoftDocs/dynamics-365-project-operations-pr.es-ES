---
title: Crear una factura proforma manual (lite)
description: Este tema proporciona información sobre crear una factura proforma manual en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176407"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="48d0a-103">Crear una factura proforma manual (lite)</span><span class="sxs-lookup"><span data-stu-id="48d0a-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="48d0a-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="48d0a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48d0a-105">En Dynamics 365 Project Operations, las facturas proforma se pueden crear manualmente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="48d0a-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="48d0a-106">Puede crear manualmente una factura proforma desde la página de lista **Contratos de proyectos** o de la página de detalles **Contrato de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="48d0a-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="48d0a-107">Página de lista de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="48d0a-107">Project Contracts list page</span></span>

<span data-ttu-id="48d0a-108">Desde la página de lista **Contratos de proyectos**, seleccione uno o más contratos de proyecto y cree facturas para todos los registros seleccionados.</span><span class="sxs-lookup"><span data-stu-id="48d0a-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="48d0a-109">El sistema verifica cuál de los contratos de proyecto seleccionados tiene atrasos **Listo para facturar** con fecha anterior a la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="48d0a-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="48d0a-110">A partir de esos contratos, el sistema crea borradores de facturas proforma.</span><span class="sxs-lookup"><span data-stu-id="48d0a-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="48d0a-111">Si un contrato de proyecto tiene varios clientes, puede haber una factura creada por cliente y varias facturas por contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="48d0a-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="48d0a-112">Todas las facturas del proyecto creadas están disponibles en la página **Factura** en la sección **Facturación** de la zona **Ventas**.</span><span class="sxs-lookup"><span data-stu-id="48d0a-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="48d0a-113">Página de detalles de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="48d0a-113">Project Contract details page</span></span>

<span data-ttu-id="48d0a-114">También se puede crear una factura proforma a partir de la página de detalles **Contrato de proyecto**, que crea la factura para ese contrato de proyecto específico.</span><span class="sxs-lookup"><span data-stu-id="48d0a-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="48d0a-115">El sistema verifica que el contrato de proyecto tiene un atraso **Listo para facturar** con fecha anterior a la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="48d0a-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="48d0a-116">A partir de estos contratos, el sistema crea borradores de facturas proforma en función del número de clientes en cada línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="48d0a-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="48d0a-117">Cuando se crea una sola factura proforma, se abre la página **Factura**.</span><span class="sxs-lookup"><span data-stu-id="48d0a-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="48d0a-118">Si hay varias facturas creadas para ese contrato de proyecto, entonces se abre la página de lista **Facturas** para mostrar todas las facturas creadas.</span><span class="sxs-lookup"><span data-stu-id="48d0a-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
