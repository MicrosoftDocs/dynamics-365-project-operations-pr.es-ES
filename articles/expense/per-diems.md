---
title: Dietas
description: Este tema proporciona información sobre las reglas de dietas que se utilizan en la gestión de gastos.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276324"
---
# <a name="per-diems"></a><span data-ttu-id="3e6e7-103">Dietas</span><span class="sxs-lookup"><span data-stu-id="3e6e7-103">Per diems</span></span>

<span data-ttu-id="3e6e7-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="3e6e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="3e6e7-105">Una dieta es un subsidio que se paga a un trabajador que viaja por trabajo.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="3e6e7-106">En la gestión de gastos, puede crear reglas de dietas para diversas situaciones de viaje.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="3e6e7-107">Las tarifas de dietas pueden basarse en la época del año, el lugar de viaje o ambos.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="3e6e7-108">Cuando crea una regla de dietas, puede especificar que se retendrá un porcentaje de la tarifa de dieta si un trabajador recibe comidas o servicios gratuitos.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="3e6e7-109">También puede establecer un número mínimo y máximo de horas que la tarifa de dieta puede aplicar al viaje de un trabajador.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="3e6e7-110">Configuración</span><span class="sxs-lookup"><span data-stu-id="3e6e7-110">Configuration</span></span> 

1. <span data-ttu-id="3e6e7-111">Para agregar ubicaciones de dietas, vaya a **Configurar** > **Cálculos y códigos** > **Ubicaciones de dietas**.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="3e6e7-112">Para cada una de las ubicaciones agregadas anteriormente, seleccione una tarifa de dieta y una moneda que sea válida entre una fecha de inicio y finalización específicas para el hotel, las comidas y otros gastos.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="3e6e7-113">Las tasas de dietas y las monedas se configuran en **Configurar** > **Cálculos y códigos** > **Dietas**.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="3e6e7-114">En la página **Ubicaciones de dietas**, configure niveles de tarifas de dietas.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="3e6e7-115">Los niveles de tarifas de dietas le permiten definir la división porcentual de una asignación diaria para hotel, comidas y otros gastos.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="3e6e7-116">Para especificar la reducción del porcentaje de comida para el desayuno, el almuerzo o la cena, actualice los campos de la página **Parámetros de gestión de gastos** en la pestaña **Dietas**.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="3e6e7-117">Enviar los gastos utilizando dietas</span><span class="sxs-lookup"><span data-stu-id="3e6e7-117">Submit expenses using per diem</span></span>
<span data-ttu-id="3e6e7-118">Para enviar gastos utilizando dietas, use la categoría de gastos **Dietas** al crear un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="3e6e7-119">Introduzca **Dietas desde la fecha**, **Dietas hasta la fecha**, y la **Ubicación de dietas**.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="3e6e7-120">La cantidad se calculará en función de las tarifas de dietas para la ubicación seleccionada y la reducción de comidas se calculará en función de los niveles de tarifas de dietas.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]