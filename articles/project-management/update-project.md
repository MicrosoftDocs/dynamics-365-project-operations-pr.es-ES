---
title: Actualizar un proyecto
description: En este tema se proporciona información sobre la actualización de proyectos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131454"
---
# <a name="update-a-project"></a>Actualizar un proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

A continuación se muestra un resumen de los campos que se pueden actualizar en un proyecto después de que se haya creado y las implicaciones aplicables de las actualizaciones.

## <a name="project-detail-fields"></a>Campos de detalle del proyecto

- **Nombre** el título del proyecto.
- **Descripción**: una introducción general al proyecto.
- **Cliente**: la empresa a la que se entregará el proyecto.
- **Plantilla de calendario**: las horas laborables del proyecto. Cuando se cambia el campo, se vuelve a calcular la programación completa.
- **Divisa**: la divisa del proyecto. Este campo se predetermina en función de la moneda definida en la unidad de contratación. Cuando se actualiza la unidad de contratación, también se actualiza el campo.
- **Unidad de contratación**: unidad organizativa que representa el grupo o la división de la empresa responsable principalmente de lograr la venta y administrar la entrega del trabajo y los servicios al cliente. 
- **Gerente de proyecto**: El miembro del equipo del proyecto que tiene autoridad para revisar y aprobar entradas de tiempo y gastos.

## <a name="estimate-fields"></a>Campos de estimación

- **Fecha estimada de inicio**: la fecha en que comenzará el proyecto. Cuando se actualiza este campo, las tareas del proyecto se moverán proporcionalmente con la nueva fecha de inicio.
- **Fecha de finalización**: la fecha en la que el proyecto está programado para finalizar.
- **Esfuerzo**: el esfuerzo estimado del proyecto. Cuando se agregan tareas al proyecto, este campo ya no se puede editar.
- **Coste laboral estimado**: el coste laboral estimado del proyecto. Cuando se agregan costes laborales al proyecto, este campo ya no se puede editar.
- **Gastos estimados**: los gastos estimados del proyecto. Cuando se agregan gastos al proyecto, este campo ya no se puede editar.

## <a name="project-actual-fields"></a>Campos reales del proyecto
- **Inicio real**: la fecha en que comenzó el proyecto.
- **Finalización**: se actualizará cuando se complete un proyecto.

## <a name="project-status-fields"></a>Campos de estado del proyecto

- **Estado general del proyecto**: el estado general del proyecto proporcionado por el administrador del proyecto.
- **Comentarios**: una narración sobre el estado actual del proyecto proporcionada por el administrador del proyecto.

