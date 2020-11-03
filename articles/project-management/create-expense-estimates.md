---
title: Estimaciones de gastos
description: Este tema proporciona información sobre cómo definir o estimar los gastos basados en proyectos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085070"
---
# <a name="expense-estimates"></a><span data-ttu-id="6e12d-103">Estimaciones de gastos</span><span class="sxs-lookup"><span data-stu-id="6e12d-103">Expense estimates</span></span>
<span data-ttu-id="6e12d-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="6e12d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e12d-105">Junto con la definición de estimaciones basadas en recursos, Dynamics 365 Project Operations permite a los administradores de proyectos definir los gastos basados en proyectos para cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="6e12d-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="6e12d-106">Cada elemento de gasto se puede asociar con una tarea de proyecto o categoría de gasto específica.</span><span class="sxs-lookup"><span data-stu-id="6e12d-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="6e12d-107">Las categorías de gastos se definen normalmente a nivel organizativo.</span><span class="sxs-lookup"><span data-stu-id="6e12d-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="6e12d-108">El precio de cada categoría de gastos se define normalmente en la siguiente jerarquía:</span><span class="sxs-lookup"><span data-stu-id="6e12d-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="6e12d-109">Organización</span><span class="sxs-lookup"><span data-stu-id="6e12d-109">Organization</span></span>
- <span data-ttu-id="6e12d-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="6e12d-110">Customer</span></span>
- <span data-ttu-id="6e12d-111">Oferta/contrato</span><span class="sxs-lookup"><span data-stu-id="6e12d-111">Quote/contract</span></span>

<span data-ttu-id="6e12d-112">Complete los siguientes pasos para ver, agregar o eliminar un gasto del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6e12d-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="6e12d-113">Vaya a **Proyectos** y seleccione el proyecto en el que desea trabajar.</span><span class="sxs-lookup"><span data-stu-id="6e12d-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="6e12d-114">Seleccione la pestaña **Estimaciones de proyecto** y vea la lista de gastos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6e12d-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="6e12d-115">Seleccione **Nuevo gasto** para agregar un gasto.</span><span class="sxs-lookup"><span data-stu-id="6e12d-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="6e12d-116">O bien, seleccione un gasto a eliminar y luego seleccione **Eliminar gasto**.</span><span class="sxs-lookup"><span data-stu-id="6e12d-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="6e12d-117">Los siguientes atributos se definen para cada elemento de línea de gastos:</span><span class="sxs-lookup"><span data-stu-id="6e12d-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="6e12d-118">**Categoría** : las agrupaciones comunes que se utilizan para describir todos los gastos incurridos en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="6e12d-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="6e12d-119">**Fecha de inicio** : la fecha en la que se prevé que se incurrirá en el gasto.</span><span class="sxs-lookup"><span data-stu-id="6e12d-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="6e12d-120">**Cantidad** : el número estimado de elementos de gastos para una categoría específica.</span><span class="sxs-lookup"><span data-stu-id="6e12d-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="6e12d-121">**Precio de coste unitario** : precio unitario utilizado para calcular el coste del gasto.</span><span class="sxs-lookup"><span data-stu-id="6e12d-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="6e12d-122">**Precio de venta unitario** : precio unitario utilizado para calcular los precios de venta del gasto.</span><span class="sxs-lookup"><span data-stu-id="6e12d-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

