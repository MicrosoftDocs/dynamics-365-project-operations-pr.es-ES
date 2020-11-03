---
title: Crear campos y entidades personalizados como dimensiones de precios
description: En este tema se proporciona información sobre cómo crear entidades o conjuntos de opciones personalizados.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085186"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Crear campos y entidades personalizados como dimensiones de precios

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Complete los pasos siguientes siempre que desee crear una entidad o un conjunto de opciones personalizado.

> [!IMPORTANT]
> Se recomienda realizar todos los cambios de dimensión de precios personalizados en una solución independiente. Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o quitar cambios según sea necesario. Esto le ayudará a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias. Tras realizar todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizar la configuración de cálculo de precios.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Crear una solución personalizada para las dimensiones de precios
1. Vaya a **Configuración** > **Soluciones** y después seleccione **Nuevo** para crear una nueva solución. 
2. Asigne un nombre a la solución, **dimensiones de precios de \<your organization name>** , especifique la información restante necesaria y después seleccione **Guardar**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear campos personalizados y conjuntos de opciones en la solución de la dimensión de precios

Las dimensiones de precios pueden ser una entidad o un conjunto de opciones. Ambas cosas deben crearse en su solución de cálculo de precios. Los pasos de este procedimiento explican cómo crear dimensiones basadas en entidades y dimensiones basadas en conjuntos de opciones.

### <a name="entity-based-dimensions"></a>Dimensiones basadas en entidades

1. Vaya a **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades**.
3. Seleccione **Nuevo** para crear una nueva entidad con el nombre **Título estándar**. 
4. Especifique la información necesaria restante y después seleccione **Guardar**.


### <a name="option-set-based-dimensions"></a>Dimensiones basadas en conjuntos de opciones 
Puede crear dos dimensiones basadas en conjuntos de opciones. Utilice **Ubicación de trabajo del recurso** para realizar el seguimiento del precio del trabajo de la ubicación **Domicilio** y del trabajo **In situ** y utilice **Horas de trabajo del recurso** con los valores **Regular** y **Horas extra** para aplicar un incremento cuando se complete el trabajo.


1. Vaya a **Configuración** > **Soluciones** y haga doble clic en **dimensiones de precios de \<your organization name>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Conjuntos de opciones**. 
3. Seleccione **Nuevo** para crear un nuevo conjunto de opciones, especifique la información necesaria restante y después seleccione **Guardar**.

## <a name="create-data-for-entity-based-dimensions"></a>Crear datos para las dimensiones basadas en entidades

Puede crear datos para las dimensiones basadas en entidades manualmente, o bien mediante llamadas de servicio o importaciones de Microsoft Excel. Use los pasos de este procedimiento para crear dos títulos estándar, **Ingeniero de sistemas** e **Ingeniero de sistemas sénior** desde la dimensión basada en entidades **Título estándar**. Si el tamaño de los datos que desea crear es pequeño, como en el siguiente ejemplo, puede usar un formulario estándar.

1. Seleccione **Búsqueda avanzada** , seleccione la entidad **Título estándar** y luego seleccione **Resultados**. Se mostrarán todas las filas de la entidad **Título estándar**.
2. Seleccione **Nuevo** y, en el campo **Nombre** , escriba "Ingeniero de sistemas" y seleccione **Guardar**.
3. Cerrar el formulario. 
4. Repita los pasos del 1 al 3 para crear el otro título estándar “Ingeniero de sistemas sénior”.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Agregue todas las entidades necesarias y los componentes relacionados a la solución de dimensión de precios
Deberá agregar las siguientes entidades a su solución de cálculo de precios. Use los pasos de este procedimiento para realizar cambios de esquema importantes en la solución de cálculo de precios para que las entidades estén al tanto de las nuevas dimensiones de precios.

1. Seleccione **Configuración** > **Soluciones** y haga doble clic en **dimensiones de precios de \<your organization name>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Agregar existente** > **Entidades**.
3. En el cuadro de diálogo **Componentes de la solución** , seleccione las siguientes entidades:

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


> [!NOTE]
> Asegúrese de incluir todos los formularios y las vistas de cada una de las entidades seleccionadas.

4. Cuando se le pida que incluya las entidades dependientes para las entidades seleccionadas anteriormente, seleccione **No**.

