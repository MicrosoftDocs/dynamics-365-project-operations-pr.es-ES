---
title: Determinar los costes e ingresos del proyecto.
description: Cómo determinar estimaciones de costes e ingresos del proyecto en Project Service
author: ruhercul
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 851e98cf5481ec7df3f430801a9d3b327794f68c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284964"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Determinar los costes e ingresos del proyecto. 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Las estimaciones del proyecto proporcionan la vista financiera del trabajo estimado y programado en la estructura de descomposición del trabajo del proyecto. La vista de estimaciones le informa del impacto de costes y de ingresos del trabajo previsto. La vista de estimaciones proporciona una herramienta para ver la información en una serie de dimensiones predefinidas para informarle mejor del impacto financiero del proyecto.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Valor de coste y de ventas del proyecto  
Las listas de precios de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definen el coste y las tasas de facturación para los roles que utilizan los proyectos. En función de los roles asociados con las tareas en la estructura de descomposición del trabajo del proyecto, puede determinar el impacto del coste y los ingresos del trabajo implicado.  
  
## <a name="cost-price-defaulting"></a>Configuración predeterminada de precios de coste  
Cada proyecto pertenece a una organización (indicada en **Unidad propietaria** en el proyecto). La lista de precios asociada a la unidad organizativa propietaria determina el precio del coste unitario. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determinan los precios de coste para roles buscando la combinación de rol, unidad, y unidad organizativa en la lista de precios de coste para obtener el precio de coste correcto para la fecha efectiva en líneas de estimación.  
  
Si la combinación de rol, unidad y unidad organizativa no da lugar a un precio de coste de la lista de precios de la unidad propietaria, se ignora la unidad en favor de la combinación de rol y unidad organizativa. Si hay un precio de coste, este precio se convierte a la unidad que elija en la línea de estimación.  
  
Si la combinación de rol y unidad organizativa no da lugar a un precio de coste, se ignora la unidad organizativa en favor de combinación de rol y unidad, y el precio se establece de manera predeterminada después de aplicar cualquier conversión, si es necesario.  
  
 Si no hay un precio para el rol, el precio de coste se establece de manera predeterminada como 0,00 en la línea de estimación.  
  
 Todos los importes de coste en las líneas de estimación de coste del proyecto están en la divisa de la unidad organizativa propietaria.  
  
## <a name="sales-price-defaulting"></a>Configuración predeterminada de precios de venta  
La lista de precios de ventas se basa en la entidad de ventas a la que el proyecto está asociado. La lista de precios de ventas asociada a la oferta o el contrato determina el precio del venta unitario. Si la oferta o el contrato tienen una lista de precios personalizada, esta será la lista de precios de venta predeterminada para estimaciones del proyecto. Si no hay ninguna asociación con las entidades de ventas, la lista de precios de venta predeterminada configurada en parámetros será la lista de precios de venta predeterminada para el proyecto. Cada línea de estimación tiene una unidad organizativa de recursos asociada para indicar la unidad organizativa desde la cual se reservarán los recursos para llevar a cabo la tarea. El precio de venta para los roles asociados se determina buscando la combinación de rol, unidad, unidad y unidad organizativa del recurso en la lista de precios de venta para obtener el precio de venta correcto para la fecha efectiva en líneas de estimación.  
  
Si la combinación de rol de, unidad, y unidad organizativa de recursos no da lugar a un precio de venta de la lista de precios de venta, el sistema ignorará unidad y buscará la combinación de rol y unidad organizativa de recursos. Si se encuentra un precio de venta, se convierte a la unidad que elija en la línea de estimación de venta.  
  
Si el sistema no encuentra un precio para el rol, el precio de venta debe establecerse de manera predeterminada como 0,00 en la línea de estimación.  
  
La vista de estimaciones tiene una vista de cuadrícula que muestra una cuadrícula plana de líneas del cálculo con unidad, coste total y precio de venta.  
  
## <a name="time-phased-view-of-project-estimates"></a>Vista con fases temporales de estimaciones de proyecto  
En la vista con fases temporales de estimaciones de proyecto, los datos de estimaciones de la vista de cuadrícula se dinamizan de forma predeterminada por rol, y muestran una distribución de datos de estimación en la escala de tiempo elegida.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Asignación de asignación de esfuerzo basada en modo de tarea  
En la vista con fases temporales, el esfuerzo total estimado para la tarea se distribuye asignando un determinado número de horas de esfuerzo por el período de tiempo de unidad de la escala temporal elegida. En Project Service, el modo de tarea determina cómo se asigna el esfuerzo a lo largo de la duración de la tarea. Los dos tipos de asignación son: asignación uniforme y asignación basada en horas laborables. 
  
## <a name="work-hours-based-allocation"></a>Asignación basada en horas laborables  
El modo de tarea de programación automática para una tarea rige que para el número de recursos estimados en la tarea, se estiman para utilizarse durante las horas laborables completas por día. Esto se aplica al asignar el esfuerzo dividiéndolo por la duración de tareas en la vista con fases temporales también. Por ejemplo, en escala temporal de un 'Día', para una tarea que se estima que completará un recurso, el esfuerzo asignado por día no excederá las horas laborables por día definidas en el calendario del proyecto. Por consiguiente, la asignación de esfuerzo garantiza siempre que los recursos se estimarán para usar durante todo el día.  
  
## <a name="even-distribution"></a>Distribución uniforme  
El modo de tareas programadas manualmente no tiene en cuenta las horas laborables, el calendario del proyecto o el número de recursos definidos en la tarea. La programación de tarea se basa en la entrada del usuario. Para tales tareas, la asignación de esfuerzo por el período de tiempo de unidad de la escala temporal elegida no tiene ningún factor limitador. El esfuerzo total de la tarea se divide y asigna igualmente para cada período de tiempo de unidad en la escala temporal elegida.  
  
De esta manera, el modo de tarea definido en la tarea determina la distribución del esfuerzo o la asignación del esfuerzo por período de tiempo de unidad en estimaciones con fases temporales.  
  
## <a name="grouping-and-time-phasing-options"></a>Opciones de agrupación y fases temporales  
Esta vista ayuda a comprender la distribución de las estimaciones de esfuerzo, coste y ventas por día, semana, mes o año. La opción Agrupar por permite dinamizar los datos de estimaciones con otras dos dimensiones: categoría y recurso. En la vista de cuadrícula y la vista con fases temporales puede seleccionar los campos que se mostrarán. Los totales de cada uno de los bloques de tiempo se muestran en la parte inferior, indicando los valores de esfuerzo, coste y ventas para el día, la semana, el mes o el año.  
  
Los valores predeterminados de precio de coste y precio de venta tienen fecha de vigencia. Cuando los índices de los roles cambien, serán más transparentes en la vista con fases temporales al ver datos de estimaciones dinamizados con "Recurso" y con fases temporales por semana.  
  
## <a name="expense-estimates"></a>Estimaciones de gastos  
Cualquier gasto realizado en el proyecto que no esté relacionado directamente con la mano de obra que se gastará se puede registrar en la vista de cuadrícula de las estimaciones de proyecto. Mediante la opción **Agregar estimación de gastos** en la vista de cuadrícula, puede lograr esto. Se pueden registrar las estimaciones de gastos para una tarea específica o para todo el proyecto. Puede elegir categorías de gastos en estas líneas y elegir una fecha provisional en la que se prevé realizar el gasto. Si la lista de precios de coste y venta asociada tiene precios predeterminados o porcentajes de incremento definidos para las categorías de gastos, se configurará de manera predeterminada en la línea de estimación tras la asociación.  
  
### <a name="see-also"></a>Vea también  
 [Guía del jefe de proyecto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]