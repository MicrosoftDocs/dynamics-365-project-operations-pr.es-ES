---
title: Asignar proyectos y tareas a una línea de oferta basada en proyecto
description: Este tema proporciona información sobre cómo asignar proyectos y tareas a una línea de tareas basada en proyectos.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272769"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Asignar proyectos y tareas a una línea de oferta basada en proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

En las líneas de oferta basadas en proyectos, puede asignar las tareas específicas de un proyecto que ya está asociado a una línea de oferta.

Cuando asigna tareas a una línea de oferta, los siguientes elementos que definió en la línea de oferta solo se aplicarán a esas tareas:

- Método de facturación
- Opciones de imputabilidad
- Límites a no exceder
- Clientes

Por ejemplo, puede tener un proyecto en el que una fase es de precio fijo y todas las demás fases son de tiempo y materiales. En este caso, puede asociar la primera fase, y todas sus tareas secundarias, a la línea de oferta para esa fase con un método de facturación de precio fijo. A continuación, puede asociar todas las demás fases a la línea de oferta basada en tiempo y materiales.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Asociar tareas a líneas de oferta basadas en proyectos

Puede asociar tareas con líneas de oferta de las siguientes ubicaciones:

- Página **Proyecto** > Pestaña **Facturación de tareas** (óptimo)
- Página **Línea de oferta** > Pestaña **Tareas cargables** 

### <a name="from-the-project-page"></a>Desde la página del proyecto

La página **Proyecto** proporciona la experiencia óptima para asociar tareas a líneas de oferta. Puede usar esta página para seleccionar varias tareas y asociarlas todas, más sus tareas secundarias, a la línea de oferta seleccionada.

1. En la pestaña **General** de una línea de oferta basada en proyecto, verifique que el campo **Proyecto** esté relleno.
2. En el campo **Tareas incluidas**, seleccione **Solo tareas seleccionadas**.
3. Guarde la línea de oferta basadas en proyecto. Cuando el formulario se actualiza, aparece la pestaña **Tareas cargables**.
4. En la pestaña **General**, seleccione el vínculo del proyecto en el campo **Proyecto**.
5. En la página **Proyecto**, seleccione la pestaña **Facturación de tareas**.
6. En la segunda cuadrícula, que se aplica a la configuración de facturación específica de la tarea, seleccione una o más tareas y luego seleccione **Líneas de oferta asociadas**.
7. En la página de diálogo que aparece, seleccione una línea de oferta que muestre líneas de oferta basadas en proyecto de la oferta.
8. En el campo **Tipo de facturación**, indique si estas tareas son cargables o no.
9. Seleccione la casilla de verificación para indicar si la asociación debe incluir tareas secundarias de las tareas seleccionadas. Al marcar la casilla, se asociarán las tareas secundarias de las tareas seleccionadas a la línea de oferta.
10. Seleccione **Aceptar** para cerrar el cuadro de diálogo.

### <a name="from-the-quote-line-page"></a>Desde la página de la línea de oferta

Puede asociar las tareas del proyecto a las líneas de oferta desde la pestaña **Tareas cargables** de la página **Línea de oferta**.

>[!NOTE]
>El lugar óptimo para asociar las tareas del proyecto a las líneas de oferta es la pestaña **Facturación de tareas** de la página **Proyecto**. Si asocia tareas de la pestaña **Tareas cargables** de la página **Línea de oferta**, debe asociar manualmente cada proyecto.

1. En la pestaña **General** de una línea de oferta basada en proyecto, verifique que haya un proyecto seleccionado en el campo **Proyecto**.
2. En el campo **Tareas incluidas**, seleccione **Solo tareas seleccionadas**.
3. Guarde la línea de oferta basadas en proyecto. Cuando el formulario se actualiza, aparece la pestaña **Tareas cargables**.
4. En la pestaña **Tareas cargables**, seleccione **Agregar una tarea de línea de oferta**.
5. En la página **Tarea de línea de oferta**, en el campo **Tareas**, seleccione la tarea, y en el campo **Tipo de facturación**, seleccione **Guardar**. 
6. Cierre la página. La tarea seleccionada ahora está asociada a la línea de oferta.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Disociar tareas de líneas de oferta basadas en proyectos

### <a name="from-the-project-page"></a>Desde la página del proyecto

Este método proporciona la experiencia óptima para disociar tareas de líneas de oferta. Puede seleccionar varias tareas y disociarlas todas, más sus tareas secundarias, de la línea de oferta seleccionada.

1. En la pestaña **General** de una línea de oferta basada en proyecto, en el campo **Proyecto**, seleccione el vínculo del proyecto.
2. En la página **Proyecto**, seleccione la pestaña **Facturación de tareas**.
3. En la segunda cuadrícula, que se aplica a la configuración de facturación específica de tareas, seleccione una o más tareas y luego seleccione **Dosociar oferta**.
4. En la página de diálogo que aparece, seleccione una línea de oferta.
5. Seleccione la casilla para indicar si la asociación debe también quitarse de las tareas secundarias de las tareas seleccionadas. Al marcar la casilla, se disociarán también las tareas secundarias de las tareas seleccionadas de la línea de oferta.
6. Seleccione **Aceptar**. Un mensaje de advertencia le informa de que, si elimina esta asociación, los datos reales registrados previamente en la tarea podrían revertirse. 
7. Seleccione **Aceptar** para continuar y eliminar la asociación entre la tarea y la línea de oferta basada en el proyecto.

### <a name="from-the-quote-line-page"></a>Desde la página de la línea de oferta

Puede disociar también las tareas del proyecto de las líneas de oferta desde la pestaña **Tareas cargables** de la página **Línea de oferta**.

1. En la pestaña **Tareas cargables**, seleccione **Eliminar una tarea de línea de oferta**.
2. Seleccione **Aceptar**. Un mensaje de advertencia le informa de que, si elimina esta asociación, los datos reales registrados previamente en la tarea podrían revertirse. 
3. Seleccione **Aceptar** para continuar y eliminar la asociación entre la tarea y la línea de oferta basada en el proyecto.

>[!NOTE]
> Este procedimiento no elimina la tarea del proyecto. Solo elimina la asociación de tareas de la línea de oferta basada en proyecto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]