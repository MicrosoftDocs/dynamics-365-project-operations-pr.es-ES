---
title: Ver el uso imputable de los recursos
description: En este tema se proporciona información acerca de la vista de uso de recursos.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992855"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="6798b-103">Ver el uso imputable de los recursos</span><span class="sxs-lookup"><span data-stu-id="6798b-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="6798b-104">La vista **Uso** de la página **Uso de recursos** de Project Service muestra el uso imputable de cada recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="6798b-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="6798b-105">Puesto que la vista se basa en el tablero de programación, encontrará muchas funciones iguales.</span><span class="sxs-lookup"><span data-stu-id="6798b-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Captura de Vista de uso](media/FAQ-utilization-1.png)
 

<span data-ttu-id="6798b-107">El cálculo de uso imputable funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6798b-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="6798b-108">Uso imputable = (Horas reales imputables)/(Capacidad del recurso).</span><span class="sxs-lookup"><span data-stu-id="6798b-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="6798b-109">Las celdas representan el uso imputable calculado para el período seleccionado (días, semanas, o meses).</span><span class="sxs-lookup"><span data-stu-id="6798b-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="6798b-110">Los colores de cada celda muestran el uso imputable para un recurso comparado con su uso imputable de destino.</span><span class="sxs-lookup"><span data-stu-id="6798b-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="6798b-111">El uso objetivo se puede establecer en cualquier rol predeterminado del recurso o en el propio recurso individual.</span><span class="sxs-lookup"><span data-stu-id="6798b-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="6798b-112">El cálculo considera el individual para el destino primero y después al rol predeterminado del recurso.</span><span class="sxs-lookup"><span data-stu-id="6798b-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="6798b-113">Definir el objetivo en un recurso</span><span class="sxs-lookup"><span data-stu-id="6798b-113">Set target on a resource</span></span>

1. <span data-ttu-id="6798b-114">Vaya a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="6798b-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="6798b-115">Seleccione un recurso para abrir el registro.</span><span class="sxs-lookup"><span data-stu-id="6798b-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="6798b-116">En la pestaña **Project Service**, puede establecer el uso objetivo de un recurso.</span><span class="sxs-lookup"><span data-stu-id="6798b-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Captura de pantalla de uso de la pestaña Project Service para establecer uso de destino](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="6798b-118">Definir un uso objetivo en un rol</span><span class="sxs-lookup"><span data-stu-id="6798b-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="6798b-119">Vaya a **Recursos** \> **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="6798b-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="6798b-120">Seleccione un rol y abra el registro.</span><span class="sxs-lookup"><span data-stu-id="6798b-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="6798b-121">Establezca el uso de destino para el rol.</span><span class="sxs-lookup"><span data-stu-id="6798b-121">Set the target utilization for the role.</span></span>

> ![Captura de pantalla de uso de Roles de recursos para establecer el uso de destino](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="6798b-123">Calcular el uso imputable para un recurso</span><span class="sxs-lookup"><span data-stu-id="6798b-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="6798b-124">Para calcular el uso imputable para un recurso, necesitará completar algunos requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="6798b-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="6798b-125">Establecer el rol predeterminado para un recurso individual</span><span class="sxs-lookup"><span data-stu-id="6798b-125">Set default role for individual resource</span></span>

<span data-ttu-id="6798b-126">Primero, el uso objetivo se puede establecer en el recurso individual o en roles de recursos.</span><span class="sxs-lookup"><span data-stu-id="6798b-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="6798b-127">Si va a usar roles de recursos para destinos, cada recurso individual debe tener un rol predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6798b-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="6798b-128">Para establecerlo, vaya a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="6798b-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="6798b-129">Seleccione un recurso, abra el registro y después seleccione la pestaña **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="6798b-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="6798b-130">En la cuadrícula **Rol de recurso**, asegúrese de que haya un rol para el recurso y de que la opción **Es predeterminado** está establecida en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="6798b-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="6798b-131">Cambiar el tipo de facturación para el rol de recurso</span><span class="sxs-lookup"><span data-stu-id="6798b-131">Change billing type for resource role</span></span>

<span data-ttu-id="6798b-132">Los roles de recursos se deben establecer para tener un tipo de facturación **Imputable**.</span><span class="sxs-lookup"><span data-stu-id="6798b-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="6798b-133">Vaya a **Recursos** \> **Roles de recursos**.</span><span class="sxs-lookup"><span data-stu-id="6798b-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="6798b-134">Abra el registro que desea actualizar y después establezca el valor predeterminado del tipo de facturación como **Imputable**.</span><span class="sxs-lookup"><span data-stu-id="6798b-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="6798b-135">Establecer las horas laborables de un rol de recursos</span><span class="sxs-lookup"><span data-stu-id="6798b-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="6798b-136">El recurso debe tener horas laborables para el cálculo de capacidad.</span><span class="sxs-lookup"><span data-stu-id="6798b-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="6798b-137">Vaya a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="6798b-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="6798b-138">Seleccione un recurso para abrir el registro y después seleccione **Mostrar horas laborables**.</span><span class="sxs-lookup"><span data-stu-id="6798b-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="6798b-139">Puede actualizar de forma masiva la lista de recursos aplicando una **Plantilla de horas laborables** desde la vista **Lista de recursos**.</span><span class="sxs-lookup"><span data-stu-id="6798b-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="6798b-140">Solución de problemas de horas reales imputables</span><span class="sxs-lookup"><span data-stu-id="6798b-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="6798b-141">Las horas reales imputables se obtienen de la entidad **Datos reales**.</span><span class="sxs-lookup"><span data-stu-id="6798b-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="6798b-142">Los datos reales con tipo de facturación **Imputable** se incluyen en el cálculo y por este motivo usted debe tener proyectos donde los datos reales sean imputables.</span><span class="sxs-lookup"><span data-stu-id="6798b-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="6798b-143">Si no ve uso imputable, estas son algunas cosas que puede comprobar:</span><span class="sxs-lookup"><span data-stu-id="6798b-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="6798b-144">El recurso tiene horas laborables definidas para capacidad.</span><span class="sxs-lookup"><span data-stu-id="6798b-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="6798b-145">El recurso tiene un destino de uso definido de forma individual o tiene un rol predeterminado asignado.</span><span class="sxs-lookup"><span data-stu-id="6798b-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="6798b-146">El rol tiene un destino de uso definido para él.</span><span class="sxs-lookup"><span data-stu-id="6798b-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="6798b-147">Los datos reales tienen un tipo de facturación **Imputable** para el período para el que está esperando un cálculo de uso.</span><span class="sxs-lookup"><span data-stu-id="6798b-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="6798b-148">Consulte lo siguiente si ve datos reales con tipos de facturación distintos de imputables:</span><span class="sxs-lookup"><span data-stu-id="6798b-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="6798b-149">El rol usado en los datos reales tiene un tipo predeterminado de facturación distinto de imputable.</span><span class="sxs-lookup"><span data-stu-id="6798b-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="6798b-150">El rol en la línea de contrato de proyecto que apoya el proyecto se ha establecido en no imputable.</span><span class="sxs-lookup"><span data-stu-id="6798b-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="6798b-151">El proyecto no tiene una línea de contrato asociada.</span><span class="sxs-lookup"><span data-stu-id="6798b-151">The project does not have an associated contract line.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]