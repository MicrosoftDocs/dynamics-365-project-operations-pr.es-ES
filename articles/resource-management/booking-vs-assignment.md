---
title: Reservas frente a asignaciones
description: Este tema proporciona información sobre las diferencias entre las reservas de recursos y las asignaciones de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130239"
---
# <a name="bookings-vs-assignments"></a>Reservas frente a asignaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las reservas son la asignación manual o automática de recursos a un proyecto. Las reservas manuales consumen la capacidad de un recurso. Las reservas representan conceptos organizativos para los equipos para que puedan comprender cómo se utilizarán los recursos en varios proyectos. Dynamics 365 Project Operations considera las reservas como un concepto a nivel de proyecto. 

A diferencia de las reservas, las asignaciones son el compromiso de recursos a las tareas del proyecto en la programación del proyecto. Los recursos pueden tener nombre o ser genéricos. 

Normalmente, la suma de las reservas de un recurso será igual a la suma de las asignaciones del recurso en una o varias tareas. Sin embargo, Project Operations no obliga a que se cumpla este contrato. La vista **Conciliación** muestra los lugares de un jefe de proyecto donde las reservas y asignaciones de un recurso no coinciden.
