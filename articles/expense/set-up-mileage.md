---
title: Configurar el kilometraje utilizando niveles de tarifas por kilometraje
description: Este tema proporciona información sobre las tarifas por kilometraje y los niveles de tarifas por kilometraje.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083692"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Configurar el kilometraje utilizando niveles de tarifas por kilometraje

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Cuando se informa de un gasto y la categoría de gasto seleccionada es **Kilometraje**, el importe de esa línea de gastos se calcula de acuerdo con el importe de *tarifa por kilometraje*. Esta cantidad se determina utilizando niveles de kilometraje definidos o, si no se establecen niveles de tarifas por kilometraje, siguiendo una tarifa por kilometraje estándar. 

Los niveles de tarifas por kilometraje se pueden configurar yendo a **Administración de gastos** > **Configuración** > **General** > **Categorías de gastos** > **Kilometraje** > **Configuración de categoría**.

Después de actualizar a 10.0.18, si su organización usa la categoría de gastos de kilometraje, considere habilitar la función de kilometraje después de revisar los cambios de diseño a continuación. 

El nuevo diseño de niveles de tarifas por kilometraje impacta en cómo se procesa el campo **Cantidad**. Antes del lanzamiento de 10.0.18, el valor en el campo **Cantidad** se consideraba el límite inferior. Cuando la acumulación cruzaba ese valor, se utilizaba la tarifa correspondiente.  A partir de 10.0.18, el valor en el campo **Cantidad** se considera el límite superior. La tarifa correspondiente se utiliza cuando la acumulación de kilometraje es menor que el valor en el campo **Cantidad**.  El nuevo modelo para niveles de kilometraje ayuda a mantener la coherencia entre los niveles de kilometraje y mejorar la usabilidad.   

Todos los informes de gastos aprobados se volverán a calcular durante la publicación de acuerdo con el nuevo diseño.

## <a name="example"></a>Ejemplo
 
### <a name="before-version-10018"></a>Antes de la versión 10.0.18
Con dos niveles de tarifas por kilometraje, el campo **Cantidad** de cada nivel representa el límite de kilometraje inferior. Actualmente, el nivel uno tiene un valor de cero (0) y una tasa de 0,45, y el nivel dos tiene un valor de 1000 y una tasa de 0,25. Si las millas o kilómetros acumulados cruzan el valor en el campo, se usa la tarifa relacionada. Si no hay una línea con cantidad cero, el sistema utiliza la tarifa de kilometraje que se define en la Gestión de gastos. 
 
Si un empleado presenta un informe de gastos con 1500 millas, las dos líneas de kilometraje en el informe de gastos publicado serían: 1000 (tasa 0,45) + 500 (tasa 0,25) = 575,00.

### <a name="after-version-10018"></a>Después de la versión 10.0.18
En 10.0.18, el campo **Cantidad** de cada nivel representa el límite superior del nivel. Actualmente, el nivel uno tiene un valor de 999 y una tasa de 0,45, y el nivel dos tiene un valor de 999,999,999.00 y una tasa de 0,25. Si las millas o kilómetros acumulados cruzan el valor en el campo **Cantidad**, se usa la tarifa relacionada. Si se superan todos los límites superiores, el sistema utiliza la tarifa de kilometraje que se define en la Gestión de gastos. 
 
Para calcular correctamente el mismo escenario, se debe cambiar la configuración del nivel. El campo **Cantidad** del nivel uno tiene un valor de 999,00 y un valor de 999 999 999,00 en el nivel dos. Si un empleado excede la cantidad total de millas o kilómetros en el nivel uno, el sistema usa la tarifa de kilometraje que se define en Gestión de gastos. 
  
Si un empleado presenta un informe de gastos con 1,500 millas, las dos líneas de kilometraje en el informe de gastos publicado serían: 1000 (tasa 0,45) + 500 (tasa 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Habilite el cálculo de kilometraje para varios niveles de kilometraje con la misma función de tarifa

La característica **Cálculo de kilometraje para varios niveles de kilometraje con la misma función de tarifa** mejora el cálculo de la tarifa de kilometraje. Lleve a cabo los siguientes pasos para habilitar esta característica.

1. Vaya a **Áreas de trabajo** > **Administración de características**. 
2. En la lista, busque y seleccione **Cálculo de kilometraje para varios niveles de kilometraje con la misma función de tarifa** y luego seleccione **Habilitar ahora**.

Después de habilitar la característica, restablezca los niveles de kilometraje para reflejar correctamente el valor del campo **Cantidad**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
