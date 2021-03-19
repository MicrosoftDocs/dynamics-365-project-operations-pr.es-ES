---
title: Actualizar estimado al finalizar
description: En este tema se proporciona información sobre cómo actualizar la proyección de esfuerzo en un proyecto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286449"
---
# <a name="update-estimate-at-completion"></a>Actualizar estimado al finalizar

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Es frecuente que un administrador de proyecto revise las estimaciones originales de una tarea. Las reproyecciones de proyectos son la percepción de las estimaciones de un administrador de proyecto según estado actual de un proyecto. Sin embargo, no recomendamos que los jefes de proyecto cambien los números de línea de base, ya que la línea de base del proyecto representa la fuente de verdad establecida para la programación y la estimación de costes del proyecto, y todos los interesados en el proyecto la han aceptado.

Existen dos formas en las que un jefe de proyecto puede reproyectar el esfuerzo en las tareas:

- Anule la estimación para finalizar (ETC) predeterminada con una nueva estimación del esfuerzo restante real en la tarea. 
- Anular el porcentaje de progreso predeterminado con una nueva estimación del progreso real de la tarea.

Cada uno de estos enfoques genera un nuevo cálculo del ETC, la estimación al finalizar (EAF) y el porcentaje de progreso de la tarea, y la variación del esfuerzo proyectado en una tarea. El EAF, ETC y el porcentaje de progreso en las tareas de resumen se recalculan y producen una nueva proyección de la variación del esfuerzo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]