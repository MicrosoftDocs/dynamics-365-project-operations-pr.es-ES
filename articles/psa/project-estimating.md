---
title: Costes e ingresos del proyecto
description: En este artículo se proporciona información sobre la estimación de costes e ingresos del proyecto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 745f6390d9987dfcb2557d0345e7444512d191fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919161"
---
# <a name="project-costs-and-revenue"></a>Costes e ingresos del proyecto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Las estimaciones del proyecto proporcionan la vista financiera del trabajo estimado y programado en la programación del proyecto. La pestaña **Estimaciones** en la página **Proyectos** muestra el impacto en los costes y los ingresos del trabajo que está planeando. También proporciona información sobre muchas dimensiones predefinidas. 

> ![Pestaña Estimaciones.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Valores de costes y de ventas del proyecto

Las listas de precios definen el coste y las tasas de facturación para los roles de un proyecto. Puede determinar el impacto en el coste y los ingresos del trabajo en función de los roles asociados con el nombre de puesto y el recurso con nombre asignado a una tarea. Si hay tareas que no tienen asignaciones (genéricas o con nombre), no puede obtener costes o estimaciones de ventas. Los valores de costes y ventas consideran la fecha definida en las listas de precios.

### <a name="default-cost-price"></a>Precio de coste predeterminado  

Cada proyecto pertenece a una organización. Esta organización se muestra en el campo **Unidad de contratación**. La lista de precios asociada con la unidad de contratación se utiliza para determinar el precio de coste unitario. Para determinar los precios de coste correctos en los roles para la fecha que se define en las líneas de estimación, busque la combinación de rol, la unidad y la unidad organizativa en la lista de precios de coste. 

Para poder calcular sus precios de coste, todas las tareas deben asignarse a un recurso. Cualquier tarea no asignada tendrá un precio de coste de 0,00.

Si la combinación de rol, unidad y unidad organizativa no devuelve un precio de coste de la lista de precios de la unidad contratante, el sistema ignora la unidad. En su lugar, busca la combinación de solo rol y unidad organizativa. Si se detecta un precio de coste, se utilizan los factores de conversión para convertirlo a la unidad que seleccionó en la línea de estimación.

Si la combinación de rol y unidad organizativa no devuelve un precio de coste, el sistema ignora la unidad organizativa. En su lugar, busca la combinación de rol y unidad para establecer el precio predeterminado (después de aplicar cualquier conversión).

Si el sistema no detecta un precio para el rol, el precio de coste en la línea de estimación se establece en un valor predeterminado de **0,00**. Todos los importes de costes en las líneas de estimación de costes del proyecto se registran en la divisa de la unidad contratante.

> [!NOTE]
> De forma predeterminada, Microsoft Dynamics 365 almacena los importes de coste en la divisa base. Sin embargo, los importes de coste que se muestran en la pestaña **Estimaciones** están en la divisa de la unidad contratante.  

### <a name="default-sales-price"></a>Precio de venta predeterminado 

La lista de precios de venta está determinada por la entidad de ventas a la que está vinculado el proyecto o por el cliente del proyecto. Cuando una entidad de ventas, como oportunidad, oferta o contrato, está asociada con el proyecto, el precio de venta de la entidad de ventas está determinado por la lista de precios asociada a la oferta o contrato. Si la oferta o contrato tiene una lista de precios personalizada, se utilizará esa lista de precios como lista de precios de venta predeterminada para estimaciones del proyecto. Si no hay asociación con las entidades de ventas, la lista de precios de venta predeterminada de los parámetros se usa como la lista de precios de venta predeterminada del proyecto que coincide con la divisa del cliente que se define en el proyecto.

Cada línea de estimación tiene una unidad de recursos asociada. La unidad de recursos indica la unidad organizativa desde la que se reservan los recursos para completar la tarea. Para determinar el precio de venta de los roles asociados, busque la combinación de rol, unidad y unidad de recursos en la lista de precios de venta. Si no hay asignaciones en la tarea, el precio de venta de la tarea será de 0,00.

Si la combinación de rol, unidad y unidad de recursos no devuelve un precio de venta de la lista de precios de venta, el sistema ignora la unidad. En cambio, busca la combinación de solo el rol y la unidad de recursos. Si se detecta un precio de venta, se utilizan los factores de conversión para convertirlo a la unidad que seleccionó en la línea de estimación de ventas. 

Si la combinación de rol y unidad de recursos no devuelve un precio de venta de la lista de precios de venta, el sistema ignora la unidad de recursos. En su lugar, busca la combinación de rol y unidad para establecer el precio predeterminado (después de aplicar cualquier conversión).

Si el sistema no detecta un precio para el rol, el precio de venta en la línea de estimación se establece en un valor predeterminado de **0,00**.

La pestaña **Estimaciones** tiene una vista de cuadrícula que muestra líneas de estimación. La cuadrícula incluye columnas para la unidad, el precio de coste total y el precio de venta total, como se muestra en la siguiente ilustración. 

> ![Vista de cuadrícula en la pestaña Estimaciones.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Vista con fases temporales de estimaciones de proyecto

La vista en fases temporales de las estimaciones del proyecto muestra los datos estimados de la vista de cuadrícula en la escala de tiempo, en una escala de tiempo que seleccione. De forma predeterminada, los datos estimados se dinamizan en la dimensión **Rol**.

> ![Vista con fases temporales de estimaciones de proyecto.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Asignación de esfuerzo estimado en función del modo de tarea

En la vista en fases de tiempo, distribuya el esfuerzo total estimado para la tarea asignando horas de esfuerzo por período de unidad en la escala de tiempo seleccionada. El modo de tarea determina cómo se asigna el esfuerzo a lo largo de la duración de la tarea. Los dos tipos de asignación son **Par** y **Basada en horas laborables**.

### <a name="work-hours-based-allocation"></a>Asignación basada en horas laborables
 
En el modo de tareas de programación automática, las horas diarias predeterminadas para los recursos de la tarea se establecen en la tarifa por hora de trabajo completa. Este comportamiento se aplica cuando el esfuerzo se asigna al dividirlo en la duración de la tarea en la vista en fases temporales. Por ejemplo, si estima que una tarea se completará con un recurso en la escala de tiempo **Día**, el esfuerzo que se asigna por día no excederá las horas de trabajo por día que se definen en el calendario del proyecto. Por lo tanto, la asignación de esfuerzo siempre garantiza que los recursos se estimen para utilizarse durante todo el día.

### <a name="even-allocation"></a>Asignación Par

En el modo de tarea programada manualmente, no se utilizan las horas de trabajo del calendario del proyecto. En cambio, la programación de tarea se basa en la entrada del usuario. Para estas tareas, la asignación de esfuerzo por período de unidad en la escala de tiempo seleccionada no tiene ningún factor limitante. El esfuerzo total en la tarea se divide por igual y se asigna para cada período de unidad de tiempo en la escala de tiempo seleccionada. Por lo tanto, el modo de tarea que se define en la tarea determina la distribución del esfuerzo, o la asignación del esfuerzo por unidad de período en estimaciones por fases.

## <a name="grouping-and-time-phasing-options"></a>Opciones de agrupación y fases temporales

La vista en fases temporales muestra la distribución de las estimaciones de esfuerzo, coste y ventas en forma diaria, semanal, mensual o anual. De forma predeterminada, los datos estimados se dinamizan en la dimensión **Rol**. Sin embargo, puede usar la opción **Agrupar por** para dinamizar en otras dos dimensiones: **Categoría** y **Recurso**.

Tanto en la vista de cuadrícula como en la vista en fases de tiempo, puede seleccionar qué campos se muestran. Los totales para cada bloque de tiempo se muestran en la parte inferior del proyecto. Muestran el esfuerzo total estimado, el coste y las ventas del día, semana, mes o año. El precio de coste predeterminado y el precio de venta tienen fecha de vigencia. Es decir, cambian para cada recurso en función de la vista en fases de tiempo que seleccione.

## <a name="expense-estimates"></a>Estimaciones de gastos

El botón **Agregar una nueva estimación de gastos** de la vista de cuadrícula le permite registrar los gastos asumidos en el proyecto, pero que no están directamente relacionados con la mano de obra. Puede registrar las estimaciones de gastos para una tarea específica o para todo el proyecto. Seleccione las categorías de gastos y la fecha tentativa en la que espera realizar en el gasto. Si la lista de precios de coste y la lista de precios de venta asociadas tienen precios predeterminados (o si los porcentajes de incremento se definen para las categorías de gastos), se introducen automáticamente en la línea de estimación cuando se produce la asociación.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
