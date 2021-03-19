---
title: Crear soluciones personalizadas para las dimensiones de precios
description: En este tema se explica cómo crear una solución personalizada al crear dimensiones de precios personalizadas.
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
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285009"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Crear soluciones personalizadas para las dimensiones de precios

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Todos los cambios de dimensiones de precios personalizadas deben realizarse en una solución independiente. Esta importante práctica recomendada proporciona flexibilidad en el futuro para actualizar o quitar cambios según sea necesario. Esto le ayudará a reutilizar su trabajo y le facilitará el llevar estos cambios a otras instancias. Tras realizar los cambios necesarios, exporte esta solución como **Solución administrada** e impórtela en otras instancias para volver a utilizar la configuración de cálculo de precios.

1. Seleccione **Configuración** > **Soluciones** y luego seleccione **Nuevo**. 
2. Asigne un nombre a la solución, **dimensiones de precios de \<your organization name>**, especifique la información restante necesaria y después seleccione **Guardar**.

> ![Creación de una solución personalizada para las dimensiones de precios](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Agregue todas las entidades necesarias y los componentes relacionados a la solución de dimensión de precios
Deberá agregar las siguientes entidades de Project Service a su solución de cálculo de precios. Complete los pasos de este procedimiento para realizar cambios de esquema importantes en la solución de cálculo de precios para que las entidades estén al tanto de las nuevas dimensiones de precios.

1. Seleccione **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Agregar existente** > **Entidades**.
3. En el cuadro de diálogo **Componentes de la solución**, seleccione las siguientes entidades:

- Real
- Recurso que se puede reservar
- Línea de estimación
- Tarea de proyecto
- Detalle de línea de factura
- Línea de diario
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

4. Cuando se le pida que incluya las entidades dependientes para las entidades seleccionadas, seleccione **No**.

> ![No incluya todos los componentes relacionados.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]