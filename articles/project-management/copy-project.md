---
title: Copiar un proyecto
description: En este tema se proporciona información sobre la copia de proyectos en Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007212"
---
# <a name="copy-a-project"></a>Copiar un proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Con Dynamics 365 Project Operations, puede crear rápidamente nuevos proyectos seleccionando **Copiar proyecto** en el formulario **Proyectos**. Para copiar un proyecto, abra el proyecto que desea copiar y luego seleccione **Copiar proyecto**. La acción copiará lo siguiente:

- Propiedades del proyecto 
- Estructura de descomposición del trabajo
- Miembros del equipo del proyecto
- Estimaciones de proyecto
- Estimaciones de gastos del proyecto
- Estimaciones de materiales del proyecto

## <a name="project-properties"></a>Propiedades del proyecto

Cuando se copia el proyecto, se copian los valores de los siguientes campos:

- Nombre
- Descripción
- Cliente
- Plantilla de calendario
- Divisa
- Unidad de contratación
- Jefe de proyecto
- Estado
- Estado general del proyecto
- Comentarios
- Estimaciones
- Fecha estimada de inicio: es la fecha en la que se crea el proyecto a partir de la copia.
- Fecha estimada de finalización: esta fecha se ajusta en función de la fecha de inicio del nuevo proyecto que se realizó a partir de la copia.
- Esfuerzo (horas)
- Coste estimado de mano de obra
- Coste estimado de gastos
- Coste estimado de materiales

> [!NOTE]
> Copiar proyecto es una operación de larga duración. También se copian los registros del proyecto, sus atributos relevantes y muchas entidades relacionadas. Debido a la naturaleza de larga duración de la operación, una vez iniciada la copia, la página del proyecto de destino se bloquea para su edición hasta que se completa la operación de copia.

## <a name="work-breakdown-structure"></a>Estructura de descomposición del trabajo

Cuando se copia el proyecto, se copia toda la estructura de descomposición del trabajo cargada por los recursos. Los recursos con nombre se sustituyen por recursos genéricos. Si los recursos con nombre no tienen las mismas horas de trabajo que el recurso genérico, la programación se volverá a calcular y la duración de las tareas puede cambiar.

## <a name="project-team-members"></a>Miembros del equipo del proyecto

Cuando un equipo de proyecto se copia desde el proyecto de origen, se copian los recursos genéricos. Las asignaciones de recursos genéricos también se mantienen como si estuvieran en el proyecto de origen. Los recursos con nombre se convertirán en miembros del equipo genéricos.

## <a name="estimates"></a>Estimaciones

Cuando se copia el proyecto, las líneas de estimación de recursos, gastos y materiales se copian del proyecto de origen. 

Para obtener información sobre cómo acceder mediante programación a Copiar proyecto, consulte [Desarrollar plantillas de proyectos con Copy Project](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
