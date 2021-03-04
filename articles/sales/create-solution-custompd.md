---
title: Crear una solución para dimensiones de precios personalizadas
description: Este tema proporciona información sobre cómo crear soluciones para dimensiones de precios personalizadas.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514027"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Crear una solución para dimensiones de precios personalizadas

 _**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_ 

>[!IMPORTANT]
>Todos los cambios de dimensiones de precios personalizadas deben realizarse en una solución independiente. Esta importante práctica recomendada permite la flexibilidad en el futuro para actualizar o quitar cambios según sea necesario, ayuda a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias. Tras realizar todos los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizarla.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Crear una solución para dimensiones de precios personalizadas

1.  Seleccione **Configuración** > **Soluciones** y luego seleccione **Nuevo**.
2.  Asigne un nombre a la solución, *dimensiones de precios de <your organization name>*.
3. Especifique la información necesaria restante y después seleccione **Guardar**.

  ![Creación de una solución para dimensiones de precios personalizada](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Agregue todas las entidades necesarias y los componentes relacionados a la solución de dimensión de precios

Agregue las siguientes entidades de Project Service a su solución de precios para realizar cambios de esquema importantes en la solución de precios. Una vez que haya completado este procedimiento, las entidades reconocerán las nuevas dimensiones de precios.

1.  Seleccione **Configuración** > **Soluciones** y después haga doble clic en el **<*nombre de su organización*> dimensiones de precios**.
2.  En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Agregar existente** > **Entidades**.
3.  En el cuadro de diálogo **Componentes de la solución**, seleccione las siguientes entidades:
 
   - **Real**
   - **Recurso que se puede reservar**
   - **Línea de estimación**
   - **Tarea de proyecto**
   - **Detalle de línea de factura**
   - **Línea de diario**
   - **Detalle de línea de contrato de proyecto**
   - **Miembro del equipo del proyecto**
   - **Detalle de línea de oferta**
   - **Incremento del precio de rol**
   - **Precio de rol**
   - **Entrada de tiempo**
 
   ![Agregar solución de dimensión de precios personalizada de entidades existentes](./media/Existing-entities-to-PD-solution.png)
 
 4. Para cada entidad, revise los componentes que se agregan y la lista final de activos de la entidad para cada entidad. 

   >[!NOTE]
   > Incluya todos los formularios y las vistas de cada una de las entidades seleccionadas.

  ![Entidades agregadas](./media/solution-component-selection.png)


5.  Cuando se le solicite incluir cualquier entidad dependiente para las entidades seleccionadas, seleccione **No, no incluir los componentes necesarios**.

    ![Entidades dependientes incluidas](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]