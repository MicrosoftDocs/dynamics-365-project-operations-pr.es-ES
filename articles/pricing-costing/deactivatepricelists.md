---
title: Desactivar listas de precios
description: Este tema explica cómo desactivar o eliminar listas de precios antiguas o no utilizadas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001357"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="b8780-103">Desactivar listas de precios</span><span class="sxs-lookup"><span data-stu-id="b8780-103">Deactivate price lists</span></span> 

<span data-ttu-id="b8780-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="b8780-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b8780-105">Para eliminar listas de precios antiguas o no utilizadas en Dynamics 365 Project Operations, hay dos pasos que debe completar.</span><span class="sxs-lookup"><span data-stu-id="b8780-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="b8780-106">Quite o elimine la lista de precios de páginas específicas.</span><span class="sxs-lookup"><span data-stu-id="b8780-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="b8780-107">Desactive o elimine la lista de precios de las listas de precios activas en la página **Lista de precios**.</span><span class="sxs-lookup"><span data-stu-id="b8780-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="b8780-108">Debe completar ambos pasos para eliminar por completo una lista de precios.</span><span class="sxs-lookup"><span data-stu-id="b8780-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="b8780-109">No basta con realizar el paso 2, que consiste en eliminar o desactivar directamente la lista de precios de la vista Listas de precios activas.</span><span class="sxs-lookup"><span data-stu-id="b8780-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="b8780-110">También debe eliminar la asociación de esta lista de precios de todos los lugares mencionados en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="b8780-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="b8780-111">Eliminar la lista de precios de páginas específicas</span><span class="sxs-lookup"><span data-stu-id="b8780-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="b8780-112">Para eliminar una lista de precios de Project Operations, vaya a las siguientes páginas:</span><span class="sxs-lookup"><span data-stu-id="b8780-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="b8780-113">Página **Parámetros del proyecto** > pestaña **Listas de precios**</span><span class="sxs-lookup"><span data-stu-id="b8780-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="b8780-114">Página **Unidad organizativa** > cuadrícula **Lista de precios**</span><span class="sxs-lookup"><span data-stu-id="b8780-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="b8780-115">Página **Cuenta** > cuadrícula **Listas de precios del proyecto**</span><span class="sxs-lookup"><span data-stu-id="b8780-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="b8780-116">Página **Cotizaciones del proyecto** > cuadrícula **Listas de precios del proyecto**: esto se aplica a todas las cotizaciones de proyectos activos.</span><span class="sxs-lookup"><span data-stu-id="b8780-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="b8780-117">Página **Contratos del proyecto** > cuadrícula **Listas de precios del proyecto**: esto se aplica a todos los contratos de proyectos activos.</span><span class="sxs-lookup"><span data-stu-id="b8780-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="b8780-118">Para cada página, debe seleccionar la lista de precios que desea eliminar y luego seleccionar **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="b8780-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="b8780-119">Desactivar o eliminar la lista de precios de la página Lista de precios</span><span class="sxs-lookup"><span data-stu-id="b8780-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="b8780-120">Para eliminar una lista de precios de las listas de precios activas, vaya a **Ventas** > **Clientes** > **Lista de precios**.</span><span class="sxs-lookup"><span data-stu-id="b8780-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="b8780-121">Seleccione la lista de precios que desea eliminar y, a continuación, seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="b8780-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="b8780-122">Si se hace referencia a la lista de precios en cualquier transacción existente, no podrá eliminarla.</span><span class="sxs-lookup"><span data-stu-id="b8780-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="b8780-123">Si esto sucede, puede desactivar la lista de precios para que no aparezca en ninguna vista.</span><span class="sxs-lookup"><span data-stu-id="b8780-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="b8780-124">Para desactivar la lista de precios, seleccione la lista de precios nuevamente y luego seleccione **Desactivar**.</span><span class="sxs-lookup"><span data-stu-id="b8780-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
