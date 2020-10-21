---
title: Actualizar estimado al finalizar
description: En este tema se proporciona información sobre cómo actualizar la proyección de esfuerzo en un proyecto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897787"
---
# <a name="update-estimate-at-completion"></a>Actualizar estimado al finalizar

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Es frecuente que un administrador de proyecto revise las estimaciones originales de una tarea. Las reproyecciones de proyectos son la percepción de las estimaciones de un administrador de proyecto según estado actual de un proyecto. Sin embargo, no recomendamos que los jefes de proyecto cambien los números de línea de base, ya que la línea de base del proyecto representa la fuente de verdad establecida para la programación y la estimación de costes del proyecto, y todos los interesados en el proyecto la han aceptado.

Existen dos formas en las que un jefe de proyecto puede reproyectar el esfuerzo en las tareas:

- Anule la estimación para finalizar (ETC) predeterminada con una nueva estimación del esfuerzo restante real en la tarea. 
- Anular el porcentaje de progreso predeterminado con una nueva estimación del progreso real de la tarea.

Cada uno de estos enfoques genera un nuevo cálculo del ETC, la estimación al finalizar (EAF) y el porcentaje de progreso de la tarea, y la variación del esfuerzo proyectado en una tarea. El EAF, ETC y el porcentaje de progreso en las tareas de resumen se recalculan y producen una nueva proyección de la variación del esfuerzo.