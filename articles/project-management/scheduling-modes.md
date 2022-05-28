---
title: Modos de programación
description: En este tema se proporciona información sobre los modos de programación.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cb507528c4815f5149c813bba0a354f7d840a4a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588435"
---
# <a name="scheduling-modes"></a>Modos de programación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


Dynamics 365 Project Operations proporciona a las organizaciones la capacidad de definir cómo administran los cambios en variables clave en tareas dentro de la estructura de descomposición del trabajo. Según las necesidades específicas de la organización, los jefes de proyecto pueden realizar cambios en el modo de programación cuando se crea un proyecto.

Hay tres modos de programación disponibles en Project Operations:

  - Duración fija (este es el modo predeterminado)
  - Esfuerzo fijo (*Trabajo*)
  - Unidades fijas

Los valores afectados por la definición de un modo de programación específico se determinan mediante la siguiente fórmula:

  Esfuerzo = Duración x Unidades

Cuando define el modo de programación de un proyecto, está configurando uno de estos valores, que luego no se pueden cambiar. Mantener este valor como constante da prioridad a ese valor, lo que notifica al sistema que no lo cambie cuando cambien los otros dos valores. La siguiente tabla proporciona información sobre los impactos de seleccionar un modo específico.

| **En esta tarea**             | **Si revisa unidades**   | **Si revisa duración** | **Si revisa esfuerzo**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Tareas de unidades fijas     | Se recalcula la duración. | Se recalcula el esfuerzo.    | Se recalcula la duración. |
| Tarea de esfuerzo fijo    | Se recalcula la duración. | Se recalculan las unidades.    | Se recalcula la duración. |
| Tarea de duración fija  | Se recalcula el esfuerzo.   | Se recalcula el esfuerzo.    | Se recalculan las unidades.   |

Para obtener más información sobre las implicaciones de un modo determinado, consulte [Cambiar el tipo de tarea para una programación más precisa](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). En el tema, el término **Trabajo** se usa en lugar de **Esfuerzo**.

## <a name="change-the-organizations-scheduling-mode"></a>Cambiar el modo de programación de la organización

Complete los siguientes pasos para definir el modo de programación de una organización.

1. Vaya a **Configuración** \> **General** \> **Parámetros** y luego seleccione el parámetro del proyecto. 
2. En la página **Parámetros del proyecto**, seleccione el modo de programación predeterminado para la organización y luego defina la capacidad para que el jefe de proyecto reemplace la configuración al crear un nuevo proyecto.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Cambiar la configuración del modo de programación en un proyecto

Si una organización permite que el jefe de proyecto reemplace el modo de programación predeterminado, el jefe de proyecto puede realizar ese cambio cuando cree un nuevo proyecto. Sin embargo, una vez que se ha guardado el proyecto, el modo de programación no se puede cambiar.

## <a name="copied-projects"></a>Proyectos copiados

Dado que un proyecto se crea cuando se realiza la acción de copiar proyecto, el jefe de proyecto no puede establecer el modo de programación. El proyecto de destino siempre estará predeterminado en el modo definido a nivel organizativo.

## <a name="copied-tasks"></a>Tareas copiadas

Cuando se copia una tarea de un proyecto a otro, la tarea hereda el modo de programación del proyecto de destino.
