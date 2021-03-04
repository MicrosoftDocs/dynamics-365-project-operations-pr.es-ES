---
title: Crear campos y entidades personalizados
description: En este tema se explica cómo crear conjuntos de opciones y entidades en su propia solución de la plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144884"
---
# <a name="create-custom-fields-and-entities"></a>Crear campos y entidades personalizados 

[!include [banner](../includes/psa-now-project-operations.md)]

Complete los pasos siguientes siempre que desee crear una entidad o un conjunto de opciones personalizado en la plataforma Power Apps.  
Los procedimientos que se describen en este tema se deben completar mediante la interfaz web de Project Service Automation (PSA).

> [!IMPORTANT]
> Se recomienda realizar todos los cambios de dimensión de precios personalizados en una solución independiente. Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o quitar cambios según sea necesario. Esto le ayudará a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias. Tras realizar todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizar la configuración de cálculo de precios.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear campos personalizados y conjuntos de opciones en la solución de la dimensión de precios

Las dimensiones de precios pueden ser una entidad o un conjunto de opciones. Ambas cosas deben crearse en su solución de cálculo de precios. Los pasos de este procedimiento explican cómo crear dimensiones basadas en entidades y dimensiones basadas en conjuntos de opciones.

### <a name="entity-based-dimensions"></a>Dimensiones basadas en entidades

1. En PSA, haga clic en **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades**.
3. Haga clic en **Nuevo** para crear una nueva entidad con el nombre **Título estándar**. Especifique la información necesaria restante y después haga clic en **Guardar**.

> ![Definición de entidad de título estándar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensiones basadas en conjuntos de opciones 
Puede crear dos dimensiones basadas en conjuntos de opciones. Utilice **Ubicación de trabajo del recurso** para realizar el seguimiento del precio del trabajo de la ubicación **Domicilio** y del trabajo **In situ** y utilice **Horas de trabajo del recurso** con los valores **Regular** y **Horas extra** para aplicar un incremento cuando se complete el trabajo.


1. En PSA, haga clic en **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Conjuntos de opciones**. 
3. Haga clic en **Nuevo** para crear un nuevo conjunto de opciones, especifique la información necesaria restante y después haga clic en **Guardar**.

> ![Dimensión de precios basada en conjuntos de opciones con el nombre Ubicación de trabajo del recurso ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensión de precios basada en conjuntos de opciones con el nombre Horas de trabajo del recurso ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Crear datos para las dimensiones basadas en entidades

Puede crear datos para las dimensiones basadas en entidades manualmente, o bien mediante llamadas de servicio o importaciones de Microsoft Excel. Use los pasos de este procedimiento para crear dos títulos estándar, **Ingeniero de sistemas** e **Ingeniero de sistemas sénior** desde la dimensión basada en entidades **Título estándar**. Si el tamaño de los datos que desea crear es pequeño, como en el siguiente ejemplo, puede usar un formulario estándar.

1. En PSA, haga clic en **Búsqueda avanzada**. Seleccione la entidad **Título estándar** y después haga clic en **Resultados**. Se mostrarán todas las filas de la entidad **Título estándar**.
2. Haga clic en **Nuevo**. En el campo **Nombre**, escriba "Ingeniero de sistemas" y después haga clic en **Guardar**.
3. Cierre el formulario . 
4. Repita los pasos del 1 al 3 para crear el otro título estándar “Ingeniero de sistemas sénior”.

> ![Datos de ejemplo para la entidad Título estándar ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]