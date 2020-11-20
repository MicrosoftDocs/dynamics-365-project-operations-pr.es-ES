---
title: Copiar un proyecto
description: Este tema proporciona información sobre la copia de proyectos en Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131814"
---
# <a name="copy-a-project"></a>Copiar un proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Con Dynamics 365 Project Operations, puede crear rápidamente nuevos proyectos seleccionando el formulario **Copiar proyecto** desde **Proyectos**. Para copiar un proyecto, abra el proyecto que desea copiar y luego seleccione **Copiar proyecto**. La acción copiará:

- Propiedades del proyecto
- La estructura de descomposición del trabajo
- Miembros del equipo del proyecto
- Estimaciones de proyecto
- Estimaciones de gastos del proyecto

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
- Fecha de inicio estimada
- Fecha de finalización
- Esfuerzo (horas)
- Coste estimado de la mano de obra
- Coste estimado de los gastos

## <a name="work-breakdown-structure"></a>Estructura de descomposición del trabajo

Cuando se copia el proyecto, se copia toda la estructura de descomposición del trabajo cargada por los recursos. Los recursos con nombre se sustituyen por recursos genéricos. Si los recursos con nombre no tienen las mismas horas de trabajo que el recurso genérico, la programación se volverá a calcular y la duración de las tareas puede cambiar.

## <a name="project-team-members"></a>Miembros del equipo del proyecto

Cuando un equipo de proyecto se copia desde el proyecto de origen, se copian los recursos genéricos. Las asignaciones de recursos genéricos también se mantienen como si estuvieran en el proyecto de origen. Los recursos con nombre se convertirán en miembros del equipo genéricos.

## <a name="estimates"></a>Estimaciones

Cuando se copia el proyecto, las líneas de estimación de recursos y gastos se copian del proyecto de origen. 

Para obtener información sobre cómo acceder mediante programación a Copiar proyecto, consulte [Desarrollar plantillas de proyectos con Copy Project](dev-copy-project.md).
