---
title: Configuración del proyecto
description: En este tema se proporciona información sobre la configuración de administración del proyecto.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148169"
---
# <a name="project-settings"></a>Configuración del proyecto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Use la siguiente configuración para obtener acceso a las características de planificación del proyecto.

## <a name="work-template"></a>Plantilla de trabajo

Para crear una programación de proyecto, cree una plantilla de calendario de proyecto que defina la cantidad de horas de trabajo por día y los cierres de negocios. Para crear una plantilla de calendario de proyecto, asocie una plantilla de trabajo con el campo **Plantilla de calendario** para el proyecto. Siga estos pasos para crear una plantilla de trabajo.

1. En PSA, en el panel de navegación izquierdo, haga clic en **Recursos**. 
2. En la página de la lista **Recursos**, abra un registro de usuario y, a continuación, seleccione **Mostrar horas laborables**.

  > [!NOTE]
  > Asegúrese de permitir ventanas emergentes en la página del explorador. Esto le permitirá ver las horas de trabajo establecidas para el recurso.
  
3. En la pestaña **Vista mensual** , haga clic en **Configurar**. Aparecerá una lista con tres opciones: 

  - Nueva programación semanal
  - Programación de trabajo para un día
  - Tiempo libre

> ![Opciones de configuración](media/project-13.png)

4. Seleccione **Nueva programación semanal** y, a continuación, establezca las opciones para esta programación del recurso. Puede establecer una programación semanal recurrente, parámetros de horas diarias, cierres comerciales, etc.
5. Establezca el rango de fechas, seleccione **Guardar** y, a continuación, haga clic en **Cerrar**. 
6. Vuelva a la página de lista **Recursos** y seleccione el recurso para el que estableció las horas de trabajo. 
7. Seleccione **Establecer calendario como** para establecer la plantilla de trabajo. 
8. En el cuadro de diálogo **Plantilla de trabajo**, introduzca un nombre para la plantilla de trabajo y, a continuación, seleccione **Aplicar**. 

Ahora puede asociar la plantilla de trabajo con una plantilla de calendario de proyecto.

## <a name="resource-roles"></a>Roles de recursos

El término *rol de recurso* hace referencia al conjunto de conocimientos, competencias y certificaciones que una persona necesitará para poder realizar un conjunto específico de tareas en un proyecto. PSA le permite establecer el coste y facturar el tiempo de un recurso en función del rol al que está asociado el recurso. Cada organización debe configurar estos roles mediante la navegación izquierda en el menú **Project Service**.

Cada organización debe configurar estos roles en la página **Categorías de recursos activas**. Para abrir esta página, en el panel de navegación izquierdo, seleccione **Roles de recursos**.

## <a name="price-lists"></a>Listas de precios

Las listas de precios le permiten establecer costes y precios de venta para roles de recursos, categorías de gastos, productos y otros elementos en una organización. Antes de establecer estimaciones financieras para el trabajo que deben realizarse para un proyecto, debe crear un coste de apoyo y una lista de precios de venta. En la sección de parámetros, también debe configurar una lista predeterminada de costes y precios de venta que se aplique a todos los proyectos que se crean en la organización. En la página **Parámetros de proyecto activos**, asegúrese de configurar una lista predeterminada de costes y precios de venta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]