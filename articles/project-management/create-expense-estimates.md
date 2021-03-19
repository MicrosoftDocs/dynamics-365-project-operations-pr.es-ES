---
title: Estimaciones de gastos
description: Este tema proporciona información sobre cómo definir o estimar los gastos basados en proyectos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287079"
---
# <a name="expense-estimates"></a><span data-ttu-id="029e7-103">Estimaciones de gastos</span><span class="sxs-lookup"><span data-stu-id="029e7-103">Expense estimates</span></span>
<span data-ttu-id="029e7-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="029e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="029e7-105">Junto con la definición de estimaciones basadas en recursos, Dynamics 365 Project Operations permite a los gerentes de proyecto definir los gastos basados en proyectos para cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="029e7-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="029e7-106">Cada elemento de gasto se puede asociar con una tarea de proyecto o categoría de gasto específica.</span><span class="sxs-lookup"><span data-stu-id="029e7-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="029e7-107">Las categorías de gastos se definen normalmente a nivel organizativo.</span><span class="sxs-lookup"><span data-stu-id="029e7-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="029e7-108">El precio de cada categoría de gastos se define normalmente en la siguiente jerarquía:</span><span class="sxs-lookup"><span data-stu-id="029e7-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="029e7-109">Organización</span><span class="sxs-lookup"><span data-stu-id="029e7-109">Organization</span></span>
- <span data-ttu-id="029e7-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="029e7-110">Customer</span></span>
- <span data-ttu-id="029e7-111">Oferta/contrato</span><span class="sxs-lookup"><span data-stu-id="029e7-111">Quote/contract</span></span>

<span data-ttu-id="029e7-112">Complete los siguientes pasos para ver, agregar o eliminar un gasto del proyecto.</span><span class="sxs-lookup"><span data-stu-id="029e7-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="029e7-113">Vaya a **Proyectos** y seleccione el proyecto en el que desea trabajar.</span><span class="sxs-lookup"><span data-stu-id="029e7-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="029e7-114">Seleccione la pestaña **Estimaciones de proyecto** y vea la lista de gastos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="029e7-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="029e7-115">Seleccione **Nuevo gasto** para agregar un gasto.</span><span class="sxs-lookup"><span data-stu-id="029e7-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="029e7-116">O bien, seleccione un gasto a eliminar y luego seleccione **Eliminar gasto**.</span><span class="sxs-lookup"><span data-stu-id="029e7-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="029e7-117">Los siguientes atributos se definen para cada elemento de línea de gastos:</span><span class="sxs-lookup"><span data-stu-id="029e7-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="029e7-118">**Categoría**: las agrupaciones comunes que se utilizan para describir todos los gastos incurridos en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="029e7-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="029e7-119">**Fecha de inicio**: la fecha en la que se prevé que se incurrirá en el gasto.</span><span class="sxs-lookup"><span data-stu-id="029e7-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="029e7-120">**Cantidad**: el número estimado de elementos de gastos para una categoría específica.</span><span class="sxs-lookup"><span data-stu-id="029e7-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="029e7-121">**Precio de coste unitario**: precio unitario utilizado para calcular el coste del gasto.</span><span class="sxs-lookup"><span data-stu-id="029e7-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="029e7-122">**Precio de venta unitario**: precio unitario utilizado para calcular los precios de venta del gasto.</span><span class="sxs-lookup"><span data-stu-id="029e7-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]