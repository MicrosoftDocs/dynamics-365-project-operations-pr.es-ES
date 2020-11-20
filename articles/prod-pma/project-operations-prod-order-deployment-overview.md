---
title: Introducción a la implementación de Project Operations para escenarios basados en existencias/producción
description: Este tema proporciona información sobre el tipo de implementación, Project Operations para escenarios almacenados / basados en producción.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7bad4de10a508f0c1aa2cc6bb0c41081f81fb259
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365632"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="4779d-103">Introducción a la implementación de Project Operations para escenarios basados en existencias/producción</span><span class="sxs-lookup"><span data-stu-id="4779d-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="4779d-104">_**Se aplica a:** Project Operations para escenarios basados en existencias/producción_</span><span class="sxs-lookup"><span data-stu-id="4779d-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="4779d-105">Este tipo de implementación tiene las siguientes capacidades para empresas basadas en proyectos:</span><span class="sxs-lookup"><span data-stu-id="4779d-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="4779d-106">Planificación de proyectos utilizando las [Estructuras de desglose del trabajo](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="4779d-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="4779d-107">Adquirir y consumir inventario almacenado para proyectos</span><span class="sxs-lookup"><span data-stu-id="4779d-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="4779d-108">Gestionar ventas basadas en proyectos utilizando el módulo **Ventas y marketing** en aplicaciones de Dynamics 365 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4779d-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="4779d-109">Fijación de precios y costos del proyecto utilizando las configuraciones de tarifa de costo y tarifa de aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4779d-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="4779d-110">Administración de recursos para proyectos en aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4779d-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="4779d-111">Progreso del proyecto y seguimiento del tiempo en aplicaciones de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4779d-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="4779d-112">Experiencias de gestión de gastos para gastos de proyectos y no relacionados con proyectos con captura de recibos utilizando capacidades de OCR</span><span class="sxs-lookup"><span data-stu-id="4779d-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="4779d-113">Facturación utilizando un impuesto sobre las ventas de clase empresarial y un sistema de tipos de cambio vigentes</span><span class="sxs-lookup"><span data-stu-id="4779d-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="4779d-114">Grupos de proyectos configurables para contabilidad WIP y acumulaciones</span><span class="sxs-lookup"><span data-stu-id="4779d-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="4779d-115">Reconocimiento de ingresos de proyecto</span><span class="sxs-lookup"><span data-stu-id="4779d-115">Project revenue recognition</span></span>

<span data-ttu-id="4779d-116">Este tipo de implementación también proporciona una extensión a la funcionalidad proporcionada por las aplicaciones de Dynamics 365 Finance y Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4779d-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="4779d-117">Seleccione este tipo de implementación para usar Dynamics 365 Project Operations para el ciclo de vida completo del proyecto, incluidos los siguientes requisitos clave:</span><span class="sxs-lookup"><span data-stu-id="4779d-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="4779d-118">Un extenso sistema de gestión de proyectos que gestiona los artículos inventariados y el costeo de órdenes de trabajo / producción para proyectos internos y facturables para cronogramas y finanzas.</span><span class="sxs-lookup"><span data-stu-id="4779d-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="4779d-119">La organización ya tiene las aplicaciones de Dynamics 365 Finance o Dynamics 365 Supply Chain and Manufacturing, y la integración de transacciones basadas en proyectos simplificará el acceso a los datos y las necesidades de informes.</span><span class="sxs-lookup"><span data-stu-id="4779d-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="4779d-120">Un sistema de gestión de gastos completamente funcional que incluye el cumplimiento de políticas y reembolsos para realizar un seguimiento de los gastos del proyecto y fuera del proyecto.</span><span class="sxs-lookup"><span data-stu-id="4779d-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="4779d-121">Un motor de tipo de cambio e impuestos sobre las ventas de clase empresarial para generar facturas de proyectos para los clientes.</span><span class="sxs-lookup"><span data-stu-id="4779d-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="4779d-122">Un sistema de reconocimiento de ingresos y contabilidad de proyectos que cumple con las Normas Internacionales de Información Financiera (NIIF).</span><span class="sxs-lookup"><span data-stu-id="4779d-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>

