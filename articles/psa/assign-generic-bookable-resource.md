---
title: Asignar recursos genéricos que se pueden reservar a un equipo de proyecto y tareas
description: En este tema se proporciona información sobre cómo reservar recursos genéricos para equipos de proyectos y tareas.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127089"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Asignar recursos genéricos que se pueden reservar a una tarea y generar requisitos de recurso 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Además de reservar y asignar a su proyecto recursos reales o con nombre, también puede asignar recursos genéricos a las tareas de un proyecto. Estos recursos pueden servir como marcadores de posición para los recursos con nombre hasta que esté listo para proporcionar recursos con nombre a su proyecto. 

1. En Project Service Automation (PSA), abra la página **Proyecto** y, en la pestaña **Programación**, escriba el nombre de la posición del recurso genérico en la celda **Recurso** de la programación. O bien, haga clic en el icono **Recurso** de la celda para abrir el selector de recursos y especificar el nombre del recurso genérico que desee crear.

![Creación y asignación de un miembro del equipo genérico](media/RM-how-to-9.png)

Se abrirá el panel **Creación rápida: Miembro del equipo del proyecto**. 

2. Escriba el rol y la unidad organizativa miembro del equipo del recurso genérico y después haga clic en **Guardar**.

![Creación rápida del miembro del equipo genérico](media/RM-how-to-10.png)

3. Tras crear el nuevo miembro del equipo de recurso genérico, se le asignará la tarea. Puede seguir asignando ese recurso genérico a otras tareas de la programación de tareas.

![Asignación de un miembro del equipo genérico existente a las tareas](media/RM-how-to-11.png)

4. Tras asignar el recurso genérico, puede generar un requisito de recurso y cumplirlo directamente reservando o enviando una solicitud de recurso a un administrador de recursos.

![Generación de un requisito para un miembro del equipo genérico](media/RM-how-to-12.png)

En la cuadrícula del miembro del equipo, además de poder usar el selector de recursos tal como se indicó anteriormente, también podrá agregar recursos genéricos directamente. Los recursos se agregan con un requisito de recursos que se basa en las fechas de inicio y de finalización y con el método de asignación que se especifica en el panel **Creación rápida: Miembro del equipo del proyecto**.

Puede ver diferencias si agrega el miembro del equipo genérico directamente y después asigna más tareas al recurso genérico y se superan las horas disponibles para realizarlas. Haga click en **Generar requisito** para regenerar el requisito de equilibrar las horas necesarias con respecto a las asignaciones.

También puede hacer clic en el vínculo **Requisito de recurso** en la cuadrícula de equipo para abrir el requisito y agregar conocimientos, recursos preferidos, etc.

![Requisito de recursos](media/RM-how-to-13.png)

