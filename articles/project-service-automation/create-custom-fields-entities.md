---
title: Crear campos y entidades personalizados
description: En este tema se explica cómo crear conjuntos de opciones y entidades en su propia solución de la plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756071"
---
# <a name="create-custom-fields-and-entities"></a>Crear campos y entidades personalizados 

Complete los pasos siguientes siempre que desee crear una entidad o un conjunto de opciones personalizado en la plataforma Power Apps.  
Los procedimientos que se describen en este tema se deben completar mediante la interfaz web de Project Service Automation (PSA).

> [!IMPORTANT]
> Se recomienda realizar todos los cambios de dimensión de precios personalizados en una solución independiente. Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o quitar cambios según sea necesario. Esto le ayudará a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias. Tras realizar todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizar la configuración de cálculo de precios.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Crear una solución personalizada para las dimensiones de precios
1. En PSA, haga clic en **Configuración** > **Soluciones** y después haga clic en **Nuevo** para crear una nueva solución. 
2. Asigne un nombre a la solución, **dimensiones de precios de \<nombre de su organización> de la organización**, especifique la información restante necesaria y después haga clic en **Guardar**.

> ![Creación de una solución personalizada para las dimensiones de precios](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear campos personalizados y conjuntos de opciones en la solución de la dimensión de precios

Las dimensiones de precios pueden ser una entidad o un conjunto de opciones. Ambas cosas deben crearse en su solución de cálculo de precios. Los pasos de este procedimiento explican cómo crear dimensiones basadas en entidades y dimensiones basadas en conjuntos de opciones.

### <a name="entity-based-dimensions"></a>Dimensiones basadas en entidades

1. En PSA, haga clic en **Configuración** > **Soluciones** y después haga doble clic en **Dimensiones de precios de \<nombre de su organización>**.
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades**.
3. Haga clic en **Nuevo** para crear una nueva entidad con el nombre **Título estándar**. Especifique la información necesaria restante y después haga clic en **Guardar**.

> ![Definición de entidad de título estándar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensiones basadas en conjuntos de opciones 
Puede crear dos dimensiones basadas en conjuntos de opciones. Utilice **Ubicación de trabajo del recurso** para realizar el seguimiento del precio del trabajo de la ubicación **Domicilio** y del trabajo **In situ** y utilice **Horas de trabajo del recurso** con los valores **Regular** y **Horas extra** para aplicar un incremento cuando se complete el trabajo.


1. En PSA, haga clic en **Configuración** > **Soluciones** y después haga doble clic en **Dimensiones de precios de \<nombre de su organización>**. 
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

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Agregue todas las entidades de PSA necesarias y los componentes relacionados a la solución de dimensión de precios
Deberá agregar las siguientes entidades de Project Service a su solución de cálculo de precios. Use los pasos de este procedimiento para realizar cambios de esquema importantes en la solución de cálculo de precios para que las entidades estén al tanto de las nuevas dimensiones de precios.

1. En PSA, haga clic en **Configuración** > **Soluciones** y después haga doble clic en **Dimensiones de precios de \<nombre de su organización>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Agregar existente** > **Entidades**.
3. En el cuadro de diálogo **Componentes de la solución**, seleccione las siguientes entidades:

- Real
- Recurso que se puede reservar
- Línea de estimación
- Detalle de línea de factura
- Línea del diario
- Detalle de línea de contrato de proyecto
- Miembro del equipo del proyecto
- Detalle de línea de oferta
- Incremento del precio de rol
- Precio de rol 
- Entrada de tiempo 

> ![Agregar entidades existentes a la solución de dimensiones de precios](media/Existing-entities-to-PD-solution.png)

> ![Seleccionar componentes de la solución](media/Dimension-Components.png)

> [!NOTE]
> Asegúrese de incluir todos los formularios y las vistas de cada una de las entidades seleccionadas.

4. Cuando se le pida que incluya las entidades dependientes para las entidades seleccionadas anteriormente, haga clic en **No**.

> ![No incluya todos los componentes relacionados.](media/Do-not-include-required.png)


