---
title: Pedidos de venta de proyectos para proyectos de tiempo y materiales
description: Este tema explica cómo crear pedidos de cliente basados en proyectos para proyectos de tiempo y materiales.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009682"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="434b9-103">Pedidos de venta de proyectos para proyectos de tiempo y materiales</span><span class="sxs-lookup"><span data-stu-id="434b9-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="434b9-104">Este tema describe cómo crear un pedido de cliente para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="434b9-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="434b9-105">Los pedidos de venta solo se pueden crear para proyectos de tipo **tiempo y material**.</span><span class="sxs-lookup"><span data-stu-id="434b9-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="434b9-106">Si un proyecto de tiempo y material tiene varias fuentes de financiación en el contrato del proyecto, debe habilitar el parámetro **Permitir pedidos de ventas para proyectos con múltiples fuentes de financiación** en la página **Parámetros de gestión de proyectos y contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="434b9-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="434b9-107">El soporte para pedidos de ventas de proyectos con múltiples fuentes de financiación está disponible a partir de la versión de aplicación 10.0.2 y superiores.</span><span class="sxs-lookup"><span data-stu-id="434b9-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="434b9-108">El parámetro para habilitar el soporte para pedidos de ventas de proyectos con múltiples fuentes de financiación se eliminará en el lanzamiento de versiones de abril de 2020, después de lo cual la funcionalidad siempre estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="434b9-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="434b9-109">Puede crear pedidos de cliente basados en proyectos de dos formas:</span><span class="sxs-lookup"><span data-stu-id="434b9-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="434b9-110">Vaya al propio proyecto.</span><span class="sxs-lookup"><span data-stu-id="434b9-110">Go to the project itself.</span></span> <span data-ttu-id="434b9-111">En el panel de acciones, seleccione **Administrar > Tareas de artículo > Pedido de venta**.</span><span class="sxs-lookup"><span data-stu-id="434b9-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="434b9-112">La información del proyecto se establecerá de forma predeterminada en el pedido de venta del proyecto.</span><span class="sxs-lookup"><span data-stu-id="434b9-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="434b9-113">Si el contrato del proyecto tiene más de una fuente de financiación, deberá seleccionar la fuente de financiación para configurar el cliente para el pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="434b9-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="434b9-114">Si solo hay una fuente de financiación para el proyecto, el cliente se configurará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="434b9-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="434b9-115">Vaya la página de la lista **Todos los pedidos de venta** y cree un nuevo pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="434b9-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="434b9-116">Deberá seleccionar el proyecto para el pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="434b9-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="434b9-117">Después de seleccionar el proyecto, el cliente se establecerá a partir de la fuente de financiación o deberá seleccionar la fuente de financiación si el contrato del proyecto tiene varias fuentes de financiación.</span><span class="sxs-lookup"><span data-stu-id="434b9-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]