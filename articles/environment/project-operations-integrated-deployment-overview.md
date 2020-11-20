---
title: Introducción a la implementación de Project Operations para escenarios basados en recursos/no mantenidos en existencias
description: Este tema proporciona información sobre el tipo de implementación, Project Operations para escenarios basados en recurso/no mantenidos en existencias.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 035ad22d2b51182c11e5c29d35f74f499fc903d5
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365629"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="a427c-103">Introducción a la implementación de Project Operations para escenarios basados en recursos/no mantenidos en existencias</span><span class="sxs-lookup"><span data-stu-id="a427c-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="a427c-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="a427c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a427c-105">El tipo de implementación, Dynamics 365 Project Operations para escenarios basados en recursos / no almacenados tiene las siguientes capacidades para empresas basadas en proyectos:</span><span class="sxs-lookup"><span data-stu-id="a427c-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="a427c-106">Planificación de proyectos con Microsoft Project para la Web</span><span class="sxs-lookup"><span data-stu-id="a427c-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a427c-107">Precios y costes multidimensionales de los recursos laborales</span><span class="sxs-lookup"><span data-stu-id="a427c-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="a427c-108">Precios basados en categorías para categorías de gastos</span><span class="sxs-lookup"><span data-stu-id="a427c-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="a427c-109">Gestión de ventas basada en proyectos con las capacidades de Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a427c-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="a427c-110">Universal Resource Scheduling, que se integra con otras aplicaciones como Dynamics 365 Field Service y Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="a427c-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="a427c-111">Progreso del proyecto y seguimiento del tiempo</span><span class="sxs-lookup"><span data-stu-id="a427c-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="a427c-112">Experiencias de gestión de gastos básicas y completas para gastos de proyectos y no relacionados con proyectos, incluida la captura de recibos utilizando capacidades de OCR</span><span class="sxs-lookup"><span data-stu-id="a427c-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="a427c-113">Facturación que se extiende desde la proforma hasta la cara al cliente y está respaldada por un impuesto a las ventas de clase empresarial y un sistema de tasa de cambio vigente.</span><span class="sxs-lookup"><span data-stu-id="a427c-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="a427c-114">Costos del proyecto configurables, perfiles de ingresos y reglas para la contabilidad y las acumulaciones del trabajo en curso (WIP)</span><span class="sxs-lookup"><span data-stu-id="a427c-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="a427c-115">Reconocimiento de ingresos de proyecto</span><span class="sxs-lookup"><span data-stu-id="a427c-115">Project revenue recognition</span></span>
- <span data-ttu-id="a427c-116">Extensibilidad a través de Power Platform</span><span class="sxs-lookup"><span data-stu-id="a427c-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="a427c-117">Este tipo de implementación proporciona una extensión a la funcionalidad proporcionada por las aplicaciones de Dynamics 365 Finance y Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a427c-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="a427c-118">Esta implementación debe elegirse si las expectativas de Project Operations son para todo el ciclo de vida del proyecto, incluidos los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="a427c-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="a427c-119">Capacidad para administrar ventas basadas en proyectos con otros tipos de ventas utilizando las capacidades de la aplicación Sales.</span><span class="sxs-lookup"><span data-stu-id="a427c-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="a427c-120">Un sistema de gestión de proyectos integrado que gestiona proyectos internos y facturables para cronogramas y finanzas desde la venta del proyecto hasta la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="a427c-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="a427c-121">Un sistema de gestión de gastos que incluye el cumplimiento de políticas y reembolsos para realizar un seguimiento de los gastos del proyecto y fuera del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a427c-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="a427c-122">Requiere un motor de tipo de cambio e impuestos sobre las ventas de clase empresarial eficaz para generar facturas de proyectos para los clientes.</span><span class="sxs-lookup"><span data-stu-id="a427c-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="a427c-123">Un sistema de reconocimiento de ingresos y contabilidad de proyectos que cumple con las Normas Internacionales de Información Financiera (NIIF).</span><span class="sxs-lookup"><span data-stu-id="a427c-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="a427c-124">Aplicaciones Finance o Supply Chain Management e integración de transacciones basadas en proyectos.</span><span class="sxs-lookup"><span data-stu-id="a427c-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>
