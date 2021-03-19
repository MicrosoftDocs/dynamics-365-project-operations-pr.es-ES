---
title: Reservas frente a asignaciones
description: Este tema proporciona información sobre las diferencias entre las reservas de recursos y las asignaciones de recursos.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279924"
---
# <a name="bookings-vs-assignments"></a>Reservas frente a asignaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las reservas son la asignación manual o automática de recursos a un proyecto. Las reservas en firme consumen la capacidad de un recurso. Las reservas representan conceptos organizativos para los equipos de modo que puedan comprender cómo se utilizarán los recursos en varios proyectos. Dynamics 365 Project Operations considera las reservas como un concepto en el nivel de proyecto. 

A diferencia de las reservas, las asignaciones son el compromiso de recursos genéricos para las tareas del proyecto en la programación del proyecto. Los recursos pueden tener nombre o ser genéricos.  Cuando se deriva un requisito de recursos de las asignaciones de tareas de proyecto, Project Operations utiliza los perfiles de esfuerzo de la asignación de recursos para crear los perfiles de los detalles del requisito de recursos. Sin embargo, no se mantiene una referencia a las asignaciones de recursos. Las actualizaciones de las reservas derivadas del requisito de recursos no actualizan ninguna asignación de recursos.

Normalmente, la suma de las reservas de un recurso será igual a la suma de las asignaciones del recurso en una o varias tareas. Sin embargo, Project Operations no obliga a que se cumpla este contrato. La vista **Conciliación** muestra los lugares de un jefe de proyecto donde las reservas y asignaciones de un recurso no coinciden.




[!INCLUDE[footer-include](../includes/footer-banner.md)]