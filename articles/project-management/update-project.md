---
title: Crear y actualizar un proyecto
description: Este artículo proporciona información sobre actualizar proyectos en Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911111"
---
# <a name="create-and-update-a-project"></a>Crear y actualizar un proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

A continuación, se muestra un resumen de los campos que se pueden actualizar en un proyecto una vez creado. Esto también incluye las implicaciones aplicables basadas en estas actualizaciones.

## <a name="project-detail-fields"></a>Campos de detalle del proyecto

- **Nombre** el título del proyecto.
- **Descripción**: una introducción general al proyecto.
- **Cliente**: la empresa a la que se entregará el proyecto.
- **Plantilla de calendario**: las horas laborables del proyecto. Cuando se cambia el campo, se vuelve a calcular la programación completa.
- **Divisa**: la divisa del proyecto. El valor predeterminado de este campo se basa en la moneda que se define en la unidad de contratación. Cuando se actualiza la unidad de contratación, también se actualiza el campo.
- **Unidad de contratación**: unidad organizativa que representa el grupo o la división de la empresa responsable principalmente de lograr la venta y administrar la entrega del trabajo y los servicios al cliente.  Cuando la unidad organizativa del director del proyecto no está definida, este campo toma por defecto el valor definido en los parámetros del proyecto.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
