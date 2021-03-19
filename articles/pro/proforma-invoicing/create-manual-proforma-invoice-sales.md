---
title: Crear una factura proforma manual (lite)
description: Este tema proporciona información sobre crear una factura proforma manual en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274209"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="9c943-103">Crear una factura proforma manual (lite)</span><span class="sxs-lookup"><span data-stu-id="9c943-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="9c943-104">_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="9c943-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c943-105">En Dynamics 365 Project Operations las facturas proforma se pueden crear manualmente, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9c943-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="9c943-106">Puede crear manualmente una factura proforma desde la página de lista **Contratos de proyectos** o de la página de detalles **Contrato de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="9c943-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="9c943-107">Página de lista de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="9c943-107">Project Contracts list page</span></span>

<span data-ttu-id="9c943-108">Desde la página de lista **Contratos de proyectos**, seleccione uno o más contratos de proyecto y cree facturas para todos los registros seleccionados.</span><span class="sxs-lookup"><span data-stu-id="9c943-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="9c943-109">El sistema comprueba cuál de los contratos de proyecto seleccionados tiene un trabajo pendiente **Listo para facturar** con fecha anterior a la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="9c943-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="9c943-110">A partir de esos contratos, el sistema crea borradores de facturas proforma.</span><span class="sxs-lookup"><span data-stu-id="9c943-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="9c943-111">Si un contrato de proyecto tiene varios clientes, puede haber una factura creada por cliente y varias facturas por contrato de proyecto.</span><span class="sxs-lookup"><span data-stu-id="9c943-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="9c943-112">Todas las facturas del proyecto creadas están disponibles en la página **Factura** en la sección **Facturación** de la zona **Ventas**.</span><span class="sxs-lookup"><span data-stu-id="9c943-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="9c943-113">Página Detalles de contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="9c943-113">Project Contract details page</span></span>

<span data-ttu-id="9c943-114">También se puede crear una factura proforma a partir de la página de detalles del **Contrato de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="9c943-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="9c943-115">El sistema comprueba que el contrato de proyecto tenga un trabajo pendiente **Listo para facturar** anterior a la fecha actual.</span><span class="sxs-lookup"><span data-stu-id="9c943-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="9c943-116">A partir de estos contratos, el sistema crea borradores de facturas proforma en función del número de clientes en cada línea de contrato.</span><span class="sxs-lookup"><span data-stu-id="9c943-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="9c943-117">Cuando se crea una sola factura proforma, se abre la página **Factura**.</span><span class="sxs-lookup"><span data-stu-id="9c943-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="9c943-118">Si se crean varias facturas para ese contrato de proyecto, se abrirá la página de lista **Facturas** para mostrar todas las facturas creadas.</span><span class="sxs-lookup"><span data-stu-id="9c943-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]