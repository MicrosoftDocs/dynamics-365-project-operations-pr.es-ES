---
title: Estimación de costes de asignaciones de recursos subcontratados
description: Este artículo explica cómo Microsoft Dynamics 365 Project Operations calcula la estimación de costos de las asignaciones de recursos subcontratados.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262081"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimación de costes de asignaciones de recursos subcontratados

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las asignaciones de tareas de los miembros del equipo del proyecto subcontratados se calculan utilizando la lista de precios **Compra** adjunta al subcontrato en el registro de miembro del equipo relacionado. Esto es diferente de cómo se calculan los costos de las asignaciones de recursos de los empleados donde las asignaciones de tareas de los recursos de los empleados se calculan utilizando la lista de precios **Costo** que se adjunta a la unidad de contratación del proyecto. 

Para los miembros del equipo del proyecto genéricos subcontratados, los costes de las asignaciones se calculan utilizando la lista de precios de compra adjunta al subcontrato. Los precios de compra también se pueden configurar específicamente para cada recurso. Se dará prioridad a estos precios de recursos específicos al calcular el costo de las asignaciones de tareas de los miembros del equipo del proyecto nombrados que son trabajadores contratados. 

La prioridad de utilizar el precio de compra específico de la función frente a un recurso específico está determinada por la configuración de la prioridad de la dimensión de precios en **Parámetros > Dimensiones de precios basados en importes**.

Esta funcionalidad de derivar precios dinámicamente en función de la configuración de dimensiones para los precios de compra de los subcontratistas es similar a cómo se derivan las tarifas de costos y facturas para los empleados a tiempo completo. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Crear asignaciones de tareas para obtener estimaciones de costos de los recursos de los subcontratistas

Las asignaciones de tareas para subcontratistas se pueden crear de dos formas: 
- Utilizando la pestaña **Tareas**.
- Utilizando la pestaña **Equipo**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Crear asignaciones de recursos usando la pestaña Tareas
Utilizando la lista **Recursos** de la pestaña **Tareas** para una tarea específica, puede crear una asignación de tarea para un recurso con nombre o un recurso genérico. Si selecciona un recurso con nombre del menú desplegable **Recursos asignados** de la tarea y este recurso es un trabajador por contrato, el recurso nombrado se asigna a la tarea y se crea un registro de miembro del equipo del proyecto correspondiente con el tipo de trabajador establecido en **Trabajador contratado** y **Validez** en **Inválido**. Como siguiente paso, deberá abrir el registro de miembros del equipo del proyecto y seleccionar un subcontrato y una línea de subcontrato. Esto actualizará la asignación de tareas para que tenga una referencia a la línea de subcontrato y subcontrato y también actualizará el estado del miembro del equipo a **Válido**.

Si opta por crear un miembro genérico del equipo a partir del desplegable **Recursos asignados** de la tarea, el diálogo **Creación de miembros genéricos del equipo** le permitirá seleccionar un subcontrato y una línea de subcontrato. Cuando se asigna el recurso genérico a la tarea y se crea el registro de miembro del equipo del proyecto correspondiente, notará que el registro de miembro del equipo del proyecto se crea con el tipo de trabajador establecido en **Trabajador contratado** y **Validez** en **Válido**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Crear miembros del equipo del proyecto usando la pestaña Equipo
Usando la pestaña Equipo en el proyecto, puede crear un miembro del equipo genérico o con nombre. Al crear el miembro del equipo, puede seleccionar la línea de subcontrato y subcontrato. Una vez creado el miembro del equipo, deberá asignarlo a una tarea mediante el desplegable **Recursos asignados** de la tarea. 

## <a name="updating-estimates"></a>Actualizando estimaciones
Una vez que haya asignado tareas a los miembros del equipo del proyecto, deberá navegar a la pestaña **Estimados** en el proyecto y seleccione **Actualizar precios** para garantizar que las tasas de costo de las asignaciones de recursos del subcontratista se actualicen en función de la lista de precios de compra adjunta al subcontrato. Las estimaciones no se generan para las tareas no asignadas en Microsoft Dynamics 365 Project Operations. Como resultado, deberá crear asignaciones de tareas para fijar el precio y el costo de varias tareas en su proyecto. 

> [¡NOTA!] Los miembros del equipo del proyecto que tienen **Tipo de trabajador** como **Trabajador contratado** pero no tienen una referencia de subcontrato están marcados como **Inválido** en la cuadrícula **Miembros del equipo del proyecto**. Si hay miembros del equipo del pryecto con este estado, abra el registro del miembro del equipo del proyecto y actualice los campos de subcontrato y línea de subcontraración para que la estimación del costo financiero refleje con precisión el costo del subcontratista en la pestaña **Estimaciones**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
