---
title: Plantillas de proyecto
description: En este tema se proporciona información sobre cómo usar plantillas de proyecto para una configuración rápida del proyecto.
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148079"
---
# <a name="project-templates"></a>Plantillas de proyecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Una plantilla de proyecto es un marco predefinido que le ayuda a iniciar un proyecto de manera rápida y sencilla. Puede usar una plantilla predefinida para crear un nuevo proyecto con un solo clic. En cuanto a los proyectos, debe definir los requisitos previos para las plantillas de proyecto. Debe definir un calendario de proyecto para cada plantilla de proyecto, y los roles y las listas de precios deben estar predefinidos en la organización de modo que los componentes de la plantilla tengan datos útiles.

Una plantilla de proyecto consta de tres componentes: una programación, estimaciones del proyecto y miembros del equipo del proyecto.

## <a name="schedule"></a>Programar

Una programación en una plantilla de proyecto tiene el mismo conjunto de elementos que una programación en un proyecto. Puede crear una jerarquía de tareas, asociar roles con tareas, definir atributos de programación y establecer dependencias. Una programación en una plantilla de proyecto también admite modos de tarea para cada tarea. Por lo tanto, es compatible con el motor de programación. Debe asociar un calendario de proyecto con el proyecto. Cuando cree una programación de trabajo, no habrá ninguna diferencia entre una plantilla de proyecto y un proyecto.

## <a name="project-estimates"></a>Estimaciones de proyecto

Las estimaciones de proyecto en una plantilla de proyecto funcionan de la misma manera que las estimaciones de proyecto en un proyecto. Sin embargo, el coste y los precios de venta se extraen de las listas predeterminadas de costes y precios de venta que se definen en los parámetros.

## <a name="creating-a-project-from-a-template"></a>Creación de un proyecto a partir de una plantilla
 
Existen varias formas de crear un proyecto a partir de una plantilla de proyecto:

- Cuando cree un proyecto a partir de una oferta, puede seleccionar una plantilla de proyecto en el cuadro de diálogo **Creación rápida: Proyecto**.

> ![Cuadro de diálogo Creación rápida: Proyecto](media/project-11.png)

- Cuando cree un proyecto seleccionando **Nuevo proyecto**, la página **Proyecto** aparecerá antes de guardar el registro. En el campo **Elegir una plantilla**, seleccione una de las plantillas de proyecto predefinidas en la organización.
- Use **Crear proyecto desde una plantilla** en la página **Entidad de plantilla**.

## <a name="copying-components-of-template-to-project"></a>Copia de componentes de una plantilla a un proyecto

Cuando copia los componentes de una plantilla de proyecto a un proyecto, pueden producirse algunos reemplazos según de la configuración del proyecto.

### <a name="copying-the-schedule"></a>Copia de la programación

Cuando copie la programación de una plantilla de proyecto, si el proyecto tiene un calendario de proyecto diferente al de la plantilla, las horas de trabajo del calendario del proyecto se aplicarán a la programación de tareas. De esta manera, la programación se ajusta para que coincida con el calendario del proyecto de apoyo. Del mismo modo, la primera tarea de la programación selecciona la fecha de inicio del proyecto, y la programación del resto de la jerarquía se actualiza en función de la duración y las dependencias que se especifican en la plantilla. 

### <a name="copying-project-estimates"></a>Copia de estimaciones de proyecto 

Cuando copie entre líneas de estimación de proyecto, se actualizarán las listas de precios. Para la lista de precios de costes, estas actualizaciones se basan en la unidad propietaria del proyecto. Para la lista de precios de venta, se basan en el cliente. Para los proyectos que están asociados con una entidad de ventas, el coste unitario y los precios de venta se determinan en función de estas listas de precios.

### <a name="copying-a-project-team"></a>Copia de un equipo de proyecto

Cuando se copia un equipo de proyecto de una plantilla de proyecto a un proyecto, se copian los recursos genéricos, junto con las habilidades y competencias que se definen en la plantilla. Las asignaciones de recursos genéricos también se mantienen como si estuvieran en la plantilla de proyecto. Los recursos con nombre no son compatibles con las plantillas de proyecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]