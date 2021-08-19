---
title: Asignar proyectos y tareas a una línea de contrato basada en proyecto (lite)
description: Este tema proporciona información sobre cómo agregar y eliminar proyectos y tareas a una línea de contrato.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ce99e6f770c5eb39e5f2740a861721cf3d210ac9743bbd9d2a1e1a7236f368c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989752"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Asignar proyectos y tareas a una línea de contrato basada en proyecto 

_**Se aplica a:** Implementación lite: acuerdo para factura proforma, Project Operations para escenarios basados en recursos/no mantenidos_

En líneas de contrato basadas en proyectos, puede asignar tareas específicas en un proyecto a la línea de contrato.

Cuando asigna tareas específicas a una línea de contrato, el método de facturación, las opciones de cargabilidad, los límites de No exceder y los clientes definidos en la línea de contrato serán aplicables solo a esas tareas específicas.

Si tiene un escenario en el que una fase de un proyecto, por ejemplo, la fase de prototipo, tiene un precio fijo y todas las demás fases son de tiempo y material, podrá asociar la fase de prototipo y todas las tareas secundarias asociadas a la línea de contrato. para esa fase con un método de facturación de precio fijo.

Todas las demás fases de la estructura de desglose del trabajo del proyecto (WBS) se pueden asociar a la línea de contrato basada en tiempo y material.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Asociar tareas a líneas de contrato basadas en proyecto

Las tareas se pueden asociar a líneas de contrato desde la pestaña **Tareas con cargo** en la página **Línea de contrato** o de la pestaña **Facturación de tareas** en la página **Proyecto**.

### <a name="from-the-contract-line-page"></a>En la página de línea de contrato

Complete los siguientes pasos para asociar las tareas del proyecto a la línea del contrato desde la pestaña **Tareas con cargo** de la página **Línea de contrato**.

1. En la pestaña **General** de una línea de contrato basada en proyecto, verifique que el campo **Proyecto** esté lleno.
2. En el campo **Tareas incluidas**, seleccione **Solo tareas seleccionadas**.
3. Guarda los cambios. El formulario se actualizará y la pestaña **Tareas con cargo** será visible.
4. Seleccione la pestaña **Tareas con cargo** y en la subcuadrícula seleccione **Agregar una tarea de línea de contrato**.
5. Sobre la página **Tareas de la línea de contrato**, en el desplegable **Tareas**, seleccione la tarea. 
6. Ingrese información en el campo **Tipo de facturación** y luego seleccione **Guardar y cerrar**. La tarea seleccionada está asociada a la línea de contrato.

> [!NOTE]
> Esta no es la experiencia más óptima para asociar tareas de proyectos a líneas de contrato. Cada proyecto deberá asociarse manualmente en esta experiencia. La forma preferida es desde la pestaña **Facturación de tareas** en la página **Proyecto**.

### <a name="from-the-project-page"></a>Desde la página del proyecto

Este es el método óptimo para asociar tareas a líneas de contrato. Puede seleccionar varias tareas y asociar todas ellas y sus tareas secundarias a la línea de contrato seleccionada. Complete los siguientes pasos para asociar tareas a la línea de contrato desde la página **Proyecto**.

1. En la pestaña **General** de una línea de contrato basada en proyecto, verifique que el campo **Proyecto** esté lleno.
2. En el campo **Tareas incluidas**, seleccione **Solo tareas seleccionadas**.
3. Guarde la línea de contrato basada en proyectos. El formulario se actualizará y la pestaña **Tareas con cargo** será visible. Este es solo para fines de verificación.
4. En la pestaña **General** de la línea de contrato basada en proyecto, en el campo **Proyecto**, seleccione el vínculo del proyecto.
5. Sobre la página **Proyecto**, seleccione la pestaña **Configuración de facturación de tareas**.
6. Hay dos cuadrículas. Una cuadrícula es para las líneas de contrato que se aplican a todo el proyecto. La segunda cuadrícula se aplica a la configuración de facturación específica de la tarea. En la segunda cuadrícula, seleccione una o más tareas y luego seleccione **Líneas de contrato asociadas**.
7. En la página de diálogo que se abre, seleccione una línea de contrato en el menú desplegable.
8. Utilizar el desplegable **Tipo de facturación** para marcar las tareas como cargables o no cargables.
9. Seleccione la casilla de verificación para indicar si la asociación también debe incluir tareas secundarias de las tareas seleccionadas. Al marcar la casilla, también se asociarán las tareas secundarias de las tareas seleccionadas a la línea del contrato.
10. Seleccione **Aceptar** para cerrar el cuadro de diálogo.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Desasociar tareas de líneas de contrato basadas en proyecto

### <a name="from-the-contract-line-page"></a>En la página de línea de contrato

Complete los siguientes pasos para desasociar las tareas del proyecto de la línea del contrato en la pestaña **Tareas con cargo** de la página **Línea de contrato**.

1. Sobre la pestaña **Tareas con cargo**, seleccione **Eliminar una tarea de línea de contrato**.
2. Un mensaje de advertencia indica que la eliminación de esta asociación podría dar como resultado la reversión de los datos reales registrados previamente en la tarea. Seleccione **Aceptar** en el cuadro de diálogo para eliminar la asociación entre la tarea y la línea de contrato basada en el proyecto. 

> [!NOTE]
> Esto no elimina la tarea del proyecto. En cambio, elimina la asociación de tareas de la línea de contrato basada en proyectos.

### <a name="from-the-project-page"></a>Desde la página del proyecto

Esta es la experiencia más óptima para desasociar tareas de proyectos de líneas de contrato. Puede seleccionar varias tareas y desasociar todas ellas y sus tareas secundarias de la línea de contrato seleccionada. Complete los siguientes pasos para desasociar tareas de la línea de contrato.

1. En la pestaña **General** de la línea de contrato basada en proyecto, en el campo **Proyecto**, haga clic en el vínculo del proyecto.
2. Sobre la página **Proyecto**, seleccione la pestaña **Configuración de facturación de tareas**.
3. Hay dos cuadrículas en la página. Una cuadrícula es para las líneas de contrato que se aplican a todo el proyecto y la segunda se aplica a la configuración de facturación específica de la tarea. En la segunda cuadrícula, seleccione una o más tareas y luego seleccione **Desasociar líneas de contrato**.
4. En la página de diálogo que se abre, seleccione una línea de contrato en el menú desplegable.
5. Seleccione la casilla de verificación para indicar si la asociación también deben eliminarse de las tareas secundarias de las tareas seleccionadas. Al marcar la casilla, también se desasociarán las tareas secundarias de las tareas seleccionadas de la línea del contrato.
6. Seleccione **Aceptar**. Un mensaje de advertencia indica que la eliminación de esta asociación podría dar como resultado la reversión de los datos reales registrados previamente en la tarea. Seleccione **Aceptar** en el cuadro de diálogo de advertencia para eliminar la asociación entre la tarea y la línea de contrato basada en el proyecto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
