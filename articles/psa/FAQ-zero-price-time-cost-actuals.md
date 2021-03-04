---
title: ¿Por qué el precio se establece de forma predeterminada en cero en costes reales del tiempo?
description: Solución de problemas de por qué un precio se establece de forma predeterminada en cero en costes reales del tiempo.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146279"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="48714-103">¿Por qué el precio se establece de forma predeterminada en cero en costes reales del tiempo?</span><span class="sxs-lookup"><span data-stu-id="48714-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="48714-104">Estas preguntas más frecuentes se aplican a datos reales donde la clase de transacción se establece en Tiempo y el tipo de transacción es Coste.</span><span class="sxs-lookup"><span data-stu-id="48714-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="48714-105">Las tres comprobaciones siguientes le ayudarán a resolver el problema de que el precio se establezca de forma predeterminada en 0 en costes reales de tiempo.</span><span class="sxs-lookup"><span data-stu-id="48714-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="48714-106">Comprobación 1: Identificar la lista de precios de costes para el proyecto</span><span class="sxs-lookup"><span data-stu-id="48714-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="48714-107">Busque el proyecto en el campo de proyecto de los datos reales y vaya a la página de proyecto.</span><span class="sxs-lookup"><span data-stu-id="48714-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="48714-108">Haga clic en el vínculo de unidad de contratación en el campo.</span><span class="sxs-lookup"><span data-stu-id="48714-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="48714-109">En la página Unidad de contratación, compruebe si la unidad de contratación tiene una lista de precios en la cuadrícula Listas de precios de coste.</span><span class="sxs-lookup"><span data-stu-id="48714-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="48714-110">Si hay más de una lista de precios, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="48714-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="48714-111">Project Service sólo admite una lista de precios por unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="48714-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="48714-112">Quite todas las listas de precios de esta entidad hasta que quede sólo una lista de precios adjunta en la cuadrícula de Listas de precios de coste de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="48714-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="48714-113">Si no hay listas de precios adjuntadas a la unidad organizativa, anote la divisa de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="48714-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="48714-114">Vaya a Project Service y luego a Parámetros y abra la pestaña Listas de precios. Compruebe si existen listas de precios con contexto establecido para coste y divisa que coincida con la divisa de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="48714-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="48714-115">Si no hay listas de precios que coincidan con ese criterio, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="48714-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="48714-116">Asegúrese de tener al menos una lista de precios cuyo contexto esté establecido como Coste y cuya divisa coincida con la divisa de la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="48714-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="48714-117">Si hay más de una lista de precios que coincida con ese criterio, continúe leyendo este documento para hacer más comprobaciones.</span><span class="sxs-lookup"><span data-stu-id="48714-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="48714-118">Comprobación 2: ¿Alguna de las listas de precios identificadas anteriormente son válidas para el coste real del tiempo?</span><span class="sxs-lookup"><span data-stu-id="48714-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="48714-119">Para que Project Service considere una lista de precios para precio predeterminado, esa lista de precios debe ser aplicable a la fecha en el coste real del tiempo.</span><span class="sxs-lookup"><span data-stu-id="48714-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="48714-120">Compruebe lo siguiente para ver si es aplicable la lista o listas de precios identificadas antes:</span><span class="sxs-lookup"><span data-stu-id="48714-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="48714-121">Compruebe si no están vacías las fechas de inicio y finalización de la pestaña general para listas de precios adjuntas.</span><span class="sxs-lookup"><span data-stu-id="48714-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="48714-122">Si las fechas de inicio y finalización de las listas de precios identificadas anteriormente están vacías, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="48714-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="48714-123">Anote el campo de fecha de inicio en el coste real del tiempo y compruebe si alguna de las listas de precios identificadas es aplicable para esa fecha.</span><span class="sxs-lookup"><span data-stu-id="48714-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="48714-124">Por ejemplo, la fecha de costes reales del tiempo debe estar dentro de la fecha de inicio y la fecha de finalización de la lista de precios.</span><span class="sxs-lookup"><span data-stu-id="48714-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="48714-125">Si no hay ninguna lista de precios que cubra esa fecha en el coste real del tiempo, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="48714-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="48714-126">Modifique las fechas de inicio y finalización de la lista de precios para asegurarse de que la lista de precios cubre la fecha del coste real del tiempo.</span><span class="sxs-lookup"><span data-stu-id="48714-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="48714-127">Si hay varias listas de precios que cubren la fecha en el coste real del tiempo, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="48714-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="48714-128">Puede solucionarlo editando las fechas de inicio y finalización de la lista o listas de precios de modo que haya sólo una lista de precios que cubra la fecha del coste real del tiempo.</span><span class="sxs-lookup"><span data-stu-id="48714-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="48714-129">Si solo hay una lista de precios que cubre esa fecha del coste real del tiempo, pase a la siguiente comprobación del documento.</span><span class="sxs-lookup"><span data-stu-id="48714-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="48714-130">Cuando termine de hacer las correcciones necesarias, vuelva a crear una entrada de tiempo, apruébela, y compruebe que el coste real del tiempo muestra un precio válido.</span><span class="sxs-lookup"><span data-stu-id="48714-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="48714-131">Comprobación 3: ¿Existe un precio en la lista de precios para las dimensiones de precios en el coste real del tiempo?</span><span class="sxs-lookup"><span data-stu-id="48714-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="48714-132">Si ha completado correctamente la Comprobación 1 y la Comprobación 2, ahora debe tener únicamente una lista de precios que es aplicable al coste real del tiempo.</span><span class="sxs-lookup"><span data-stu-id="48714-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="48714-133">Abra esta Lista de precios y vaya a la pestaña Precios de rol. Asegúrese de que hay una fila en la cuadrícula para las dimensiones de precios en el coste real del tiempo.</span><span class="sxs-lookup"><span data-stu-id="48714-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="48714-134">Si no hay ninguna fila en la cuadrícula de precios de rol para las dimensiones de precios en el coste real del tiempo, ha aislado el problema.</span><span class="sxs-lookup"><span data-stu-id="48714-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="48714-135">Cree una fila en la cuadrícula Precios de rol para las dimensiones de precios en el coste real del tiempo.</span><span class="sxs-lookup"><span data-stu-id="48714-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="48714-136">Cuando termine, vuelva a crear una entrada de tiempo, apruébela, y compruebe que el coste real del tiempo muestra un precio válido.</span><span class="sxs-lookup"><span data-stu-id="48714-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="48714-137">Si aún no ve un precio válido en el coste real del tiempo después de realizar las tres comprobaciones anteriores, registre un vale de soporte.</span><span class="sxs-lookup"><span data-stu-id="48714-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



