---
title: Crear campos y entidades personalizados como dimensiones de precios
description: En este tema se proporciona información sobre cómo crear entidades o conjuntos de opciones personalizados.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642834"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Crear campos y entidades personalizados como dimensiones de precios

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Complete los siguientes pasos cuando desee crear una entidad o conjunto de opciones personalizada para usarla como dimensión de precios. Para obtener más información, consulte la [Información general de dimensiones de precios](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Se recomienda realizar todos los cambios de dimensión de precios personalizados en una solución independiente. Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o eliminar cambios según sea necesario. Esto también ayudará con la reutilización de su trabajo y facilitará la transferencia de estos cambios a otra instancia. Una vez que haya realizado todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para reutilizar su configuración de precios.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear campos personalizados y conjuntos de opciones en la solución de la dimensión de precios

Las dimensiones de precios pueden ser una entidad o un conjunto de opciones. Ambas cosas deben crearse en su solución de cálculo de precios. Los pasos de este procedimiento explican cómo crear dimensiones basadas en entidades y dimensiones basadas en conjuntos de opciones.

### <a name="entity-based-dimensions"></a>Dimensiones basadas en entidades
Para crear dimensiones basadas en entidades, siga los siguientes pasos:

1. Vaya a **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades**.
3. Seleccione **Nuevo** para crear una nueva entidad con el nombre **Título estándar**. 
4. Especifique la información necesaria restante y después seleccione **Guardar**.

> ![Definición de entidad de título estándar](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensiones basadas en conjuntos de opciones 
Puede crear dos dimensiones basadas en conjuntos de opciones. 

- Use la **Ubicación de trabajo del recurso** para realizar un seguimiento del precio del trabajo de la ubicación **Hogar** e **In situ**. 
- Use **Horas de trabajo del recurso** con los valores **Regular** y **Horas extra** para aplicar un incremento cuando finalice el trabajo.

El siguiente gráfico proporciona una vista de la dimensión **Ubicación de trabajo del recurso**. 

> ![Dimensión de precios basada en conjuntos de opciones con el nombre Ubicación de trabajo del recurso](media/Option-set-PD-called-Resource-Work-Location.png)

El siguiente gráfico proporciona una vista de la dimensión **Horas de trabajo del recurso**. 

> ![Dimensión de precios basada en conjuntos de opciones con el nombre Horas de trabajo del recurso](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Vaya a **Configuración** > **Soluciones** y haga doble clic en **dimensiones de precios de \<your organization name>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Conjuntos de opciones**. 
3. Seleccione **Nuevo** para crear un nuevo conjunto de opciones, especifique la información necesaria restante y después seleccione **Guardar**.

## <a name="create-data-for-entity-based-dimensions"></a>Crear datos para las dimensiones basadas en entidades

Puede crear datos para las dimensiones basadas en entidades manualmente, o bien mediante llamadas de servicio o importaciones de Microsoft Excel. Use los pasos de este procedimiento para crear dos títulos estándar, **Ingeniero de sistemas** e **Ingeniero de sistemas sénior** desde la dimensión basada en entidades **Título estándar**. Si el tamaño de los datos que desea crear es pequeño, como en el siguiente ejemplo, puede usar un formulario estándar.

1. Seleccione **Búsqueda avanzada**.
2. Seleccione la entidad **Título estándar** y, a continuación, **Resultados**. Se mostrarán todas las filas de la entidad **Título estándar**.
3. Seleccione **Nuevo** y, en el campo **Nombre**, escriba "Ingeniero de sistemas" y seleccione **Guardar**.
4. Cierre la página. 
5. Repita los pasos del 1 al 3 para crear el otro título estándar “Ingeniero de sistemas sénior”.

> ![Datos de ejemplo para la entidad Título estándar](media/ST-data.png)
