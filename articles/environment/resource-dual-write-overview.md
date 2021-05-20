---
title: Integración de doble escritura de Project Operations
description: Este tema proporciona una descripción general de la integración de doble escritura de Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955679"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="67487-103">Descripción general de la integración de doble escritura de Project Operations</span><span class="sxs-lookup"><span data-stu-id="67487-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="67487-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="67487-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="67487-105">Project Operations usa [capacidades de doble escritura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar datos en Microsoft Dataverse y Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="67487-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="67487-106">La siguiente ilustración muestra cómo se sincronizan los datos como parte de esta integración entre Dataverse y Finance.</span><span class="sxs-lookup"><span data-stu-id="67487-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Descripción general de los flujos de datos de Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="67487-108">Project Operations en Dataverse proporciona una interfaz de usuario (UI) moderna y extensibilidad fácil sin código o con poco código usando capacidades de Power Platform.</span><span class="sxs-lookup"><span data-stu-id="67487-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="67487-109">Los jefes de proyecto, jefes de recursos, miembros del equipo de proyecto y otras personas de la oficina principal realizan sus actividades en Project Operations en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67487-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="67487-110">Project Operations en Finance proporciona compatibilidad de reconocimiento de ingresos y contabilidad de proyectos.</span><span class="sxs-lookup"><span data-stu-id="67487-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="67487-111">Project Operations se conecta al marco financiero en Finance para el cálculo de impuestos sobre las ventas, tipos de cambio de divisas, informes de dimensión financiera y más.</span><span class="sxs-lookup"><span data-stu-id="67487-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="67487-112">Las experiencias de los contables de proyectos se basan principalmente en Finance.</span><span class="sxs-lookup"><span data-stu-id="67487-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="67487-113">La integración de Project Operations consiste en la siguiente integración de componentes:</span><span class="sxs-lookup"><span data-stu-id="67487-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="67487-114">Integración de datos de instalación y configuración de Project Operations</span><span class="sxs-lookup"><span data-stu-id="67487-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="67487-115">Estimaciones y datos reales del proyecto</span><span class="sxs-lookup"><span data-stu-id="67487-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="67487-116">Facturas de proyecto</span><span class="sxs-lookup"><span data-stu-id="67487-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="67487-117">Gestión de gastos</span><span class="sxs-lookup"><span data-stu-id="67487-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="67487-118">Factura del proveedor</span><span class="sxs-lookup"><span data-stu-id="67487-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
