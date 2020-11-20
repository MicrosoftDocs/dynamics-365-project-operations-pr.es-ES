---
title: Estimaciones de ventas y proyectos
description: En este tema se proporciona información sobre cómo aprovechar la programación y las estimaciones en el proceso de venta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120699"
---
# <a name="sales-estimates-and-projects"></a>Estimaciones de ventas y proyectos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durante el proceso de venta, puede crear estimaciones de ventas vinculando un proyecto a una oferta de ventas. De esta manera, la estimación determinista puede producirse durante el proceso de ventas para aprovechar las capacidades de programación y estimación del proyecto. Si la venta se lleva a cabo, puede usarse la programación que se utilizó para fines de estimación de ventas como base para un mayor refinamiento del plan del proyecto.

## <a name="linking-a-project-to-a-quote-line"></a>Vinculación de un proyecto a una línea de oferta

Cuando cree una línea de oferta basada en un proyecto, podrá crear un nuevo proyecto o asociar un proyecto existente en la página **Línea de oferta**. 

> ![Formulario de línea de oferta](media/project-8.png)
 
Cuando cree un proyecto nuevo a partir de los detalles de la línea de oferta, puede aprovechar las plantillas de proyecto. Las plantillas de proyecto son proyectos modelo que representan planes de proyecto estándar y estimaciones financieras que son típicas en una organización. También pueden representar copias de planes de proyectos y estimaciones de proyectos pasados.

> ![Detalles de línea de oferta](media/project-9.png)
  
Al crear el proyecto desde la oferta, el proyecto se asociará automáticamente con la línea de la oferta.

## <a name="components-of-estimates-in-a-project"></a>Componentes de estimaciones en un proyecto

Una programación le permite dividir el trabajo en tareas, mantener una jerarquía de ellas, determinar los recursos necesarios para completar una y asignar una estimación del esfuerzo necesario para completarla.

Puede definir el esfuerzo de trabajo y las estimaciones de programación mediante los campos en la pestaña **Programación** de la página **Proyecto**. Debido a que una lista de precios está asociada con el proyecto, las estimaciones financieras se calculan mediante los costes y los precios de venta definidos en la lista de precios.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importación de estimaciones de un proyecto a una oferta

Después de definir las estimaciones del proyecto, puede importarlas en la línea de oferta. En la página **Detalles de línea de oferta**, seleccione **Importar desde estimaciones** en la cinta para resumir las estimaciones de proyecto por tipo de transacción, rol o nivel de tarea.
