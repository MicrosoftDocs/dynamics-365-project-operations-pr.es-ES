---
title: Definir calendarios de recursos
description: Este tema proporciona información sobre cómo definir los calendarios de horas de trabajo para los recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961952"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="75898-103">Definir calendarios de recursos</span><span class="sxs-lookup"><span data-stu-id="75898-103">Define resource calendars</span></span>

<span data-ttu-id="75898-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="75898-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="75898-105">Cada recurso reservable que trabaja en un proyecto debe tener un calendario de horas de trabajo para definir su disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="75898-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="75898-106">Las horas laborales de los recursos se pueden definir de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="75898-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="75898-107">Definir reglas de calendario individuales para un recurso</span><span class="sxs-lookup"><span data-stu-id="75898-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="75898-108">Aplicar una plantilla de calendario existente para el recurso</span><span class="sxs-lookup"><span data-stu-id="75898-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="75898-109">Definir las horas laborables de un recurso</span><span class="sxs-lookup"><span data-stu-id="75898-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="75898-110">En el menú **Recursos**, seleccione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="75898-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="75898-111">En la vista de cuadrícula, seleccione el **Recurso reservable**.</span><span class="sxs-lookup"><span data-stu-id="75898-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="75898-112">En la página **Detalles del recurso**, seleccione la pestaña **Horas Laborables**. De forma predeterminada, el calendario de recursos reservables tiene como valor predeterminado las horas de trabajo de la plantilla de horas de trabajo predeterminada que se define para la organización.</span><span class="sxs-lookup"><span data-stu-id="75898-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="75898-113">Para actualizar el horario laboral, haga clic con el botón derecho en la fecha de inicio de la regla de calendario propuesta a definir.</span><span class="sxs-lookup"><span data-stu-id="75898-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="75898-114">Utilice el menú de reglas de calendario para definir una regla de calendario para un día específico, el resto de la serie o el calendario completo.</span><span class="sxs-lookup"><span data-stu-id="75898-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="75898-115">Una vez seleccionada la opción, puede definir:</span><span class="sxs-lookup"><span data-stu-id="75898-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="75898-116">El día de la semana en el que se aplicará el horario laboral.</span><span class="sxs-lookup"><span data-stu-id="75898-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="75898-117">Las horas laborables de cada día.</span><span class="sxs-lookup"><span data-stu-id="75898-117">The working times within each day.</span></span>
    - <span data-ttu-id="75898-118">La zona horaria de la regla de calendario.</span><span class="sxs-lookup"><span data-stu-id="75898-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="75898-119">Si corresponde, también se puede especificar el tiempo no laborable para la regla.</span><span class="sxs-lookup"><span data-stu-id="75898-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="75898-120">Aplicción de un calendario a un recurso</span><span class="sxs-lookup"><span data-stu-id="75898-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="75898-121">En el menú **Recursos**, seleccione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="75898-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="75898-122">En la vista de cuadrícula, seleccione hasta 25 **Recursos reservables** para actualizar.</span><span class="sxs-lookup"><span data-stu-id="75898-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="75898-123">Seleccione **Establecer calendario** y un cuadro de diálogo le mostrará una lista de plantillas de horas de trabajo disponibles.</span><span class="sxs-lookup"><span data-stu-id="75898-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="75898-124">Seleccione la plantilla que desee utilizar y seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="75898-124">Select the template you want to use, and then select **Apply**.</span></span>
