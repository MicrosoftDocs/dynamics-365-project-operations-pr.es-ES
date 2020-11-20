---
title: Conceptos clave
description: En este tema se proporciona información sobre los conceptos clave para la administración de recursos en Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 862e277d8109e810401bdecd4c45c2696275f8a8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120384"
---
# <a name="key-concepts"></a>Conceptos clave

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En la siguiente tabla se definen los conceptos clave que se usan en la aplicación Dynamics 365 Project Service Automation.

| Concepto                    | Definición |
|----------------------------|------------|
| Miembro del equipo del proyecto        | Como parte del equipo del proyecto, un miembro del equipo del proyecto puede ser un recurso con nombre que tiene reservas, un recurso con nombre que no tiene reservas o un recurso genérico. Los recursos genéricos no tienen reservas, son locales para el proyecto y no tienen restricciones de capacidad en todos los proyectos. |
| Recurso genérico del proyecto   | Un marcador de posición de recursos que le permite formar un equipo y contratar un plan de proyecto sin tener que conocer el recurso con nombre. El calendario del proyecto se utiliza como calendario del recurso genérico. Los recursos genéricos pueden agregarse a un equipo del proyecto y asignarse a tareas. |
| Horas reservadas               | Las horas de recursos están reservadas para un proyecto con el fin de ayudar a garantizar que se complete el trabajo del proyecto. Las horas reservadas se consumen a partir de la capacidad total del recurso. Las reservas son solo para recursos con nombre, no para recursos genéricos. |
| Horas asignadas             | Las horas de recursos se asignan a tareas en la programación del proyecto. Las asignaciones pueden ser de recursos con nombre o de recursos genéricos. Las asignaciones pueden ser independientes de las reservas. |
| Horas necesarias             | La capacidad necesaria, pero que aún no cumple un recurso con nombre. Las horas necesarias son relevantes solo para los miembros del equipo genérico que han generado requisitos de recursos. |
| Petición                     | La carga de trabajo actual y entrante. En Project Service Automation, la petición se muestra como requisitos de recursos o solicitudes de recursos. |
| Requisito de recursos       | Una entidad que se utiliza para capturar las horas necesarias, las fechas de inicio y finalización, las habilidades, la geografía y otras dimensiones de precios para los recursos necesarios. Los requisitos de recursos se generan a partir de los miembros del equipo del proyecto o se crean individualmente. |
| Solicitud de recursos           | Una entidad que se utiliza como un "sobre" para llevar el requisito de recursos que debe cumplir un administrador de recursos. |
| Rol de recurso predeterminado      | El rol bajo el que se agrupa un recurso para el cálculo de uso. Se supone que el recurso tiene las habilidades necesarias para el rol y cumple con la utilización objetivo para ese rol. |
| Unidad de organización de recursos | La unidad organizativa a la que se asigna un recurso. |
| Perfil                    | Tareas, requisitos u horas de asignación, ya que se dividen en una distribución diaria. Por ejemplo, para una tarea de cinco días y 40 horas se puede establecer un perfil de ocho horas al día durante cinco días. |
| Vista de conciliación        | Una vista que muestra las reservas y asignaciones para cada miembro del equipo del proyecto. Esta vista permite al jefe de proyecto buscar cualquier desajuste entre las reservas y las asignaciones, y tomar medidas correctivas si hay alguno. |
| Horas laborables                 | Una entidad que se utiliza para identificar la capacidad de los recursos y las horas laborables y no laborables. Esta entidad también se conoce como "calendario de recursos". |
