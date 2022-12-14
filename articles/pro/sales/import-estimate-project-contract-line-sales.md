---
title: Importar estimaciones desde un proyecto a una línea de contrato de proyecto
description: Este artículo proporciona información sobre la importación de estimaciones financieras desde un proyecto a una línea de contrato.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824696"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Importar estimaciones desde un proyecto a una línea de contrato de proyecto

_**Se aplica a:** Implementación Lite: del acuerdo a la factura proforma, Project Operations para escenarios basados en recursos/no mantenidos_ _

En Dynamics 365 Project Operations puede importar estimaciones de un proyecto a una línea de contrato basada en proyecto.

1. Verifique que el campo **Proyecto** en la línea de contrato basada en proyecto se ha rellenado.
2. En la pestaña **Detalles de línea de contrato**, en la subcuadrícula, seleccione **Importar desde estimación de proyecto**. Se abre una página de diálogo con opciones de resumen. Las opciones de resumen disponibles son **Clase de transacción**, **Categoría**, **Rol** y **Tarea de proyecto**.
3. Según la selección de resumen, se copia la estimación del proyecto para todas las clases de transacciones y tareas incluidas en esta línea de contrato. Para comprobar qué clases de transacciones están incluidas, en la pestaña **General** de la línea de contrato basada en el proyecto, verifique los valores en los campos **Incluir tiempo**, **Incluir gastos** e **Incluir tarifas**. 
4. Para ver qué tareas están incluidas, seleccione la pestaña **Tareas facturables** en la línea del contrato. Según las tareas asociadas que tienen el campo **Clases de transacciones incluidas** establecido en **Sí**, todas las estimaciones para esas combinaciones de clases de tarea y transacción se importan a la línea de contrato.

Cuando importe estimaciones, el sistema establecerá el precio predeterminado según las listas de precios del contrato adjuntas a la oferta y el tipo de facturación configurado en la línea de contrato. Si una tarea, rol o categoría se configura en la línea de contrato como no imputable, la línea de estimación importada será no imputable y no se sumará al valor del contrato de la línea de contrato.

Cuando una línea de contrato tiene detalles de línea, los campos **Valor de compra** e **Impuesto estimado** de la línea de contrato están resumidos y no se pueden editar.

Cuando se seleccionan varias opciones de resumen, el sistema intenta resumir conforme a todas las opciones seleccionadas. La salida de resumen da como resultado más líneas de contrato importadas que si selecciona solo una opción de resumen.

Por ejemplo, si el proyecto tiene las siguientes líneas de estimación de gastos:

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| Tarea B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarea C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Cuando el usuario selecciona resumir por **Clase de transacción**, se importará la siguiente información:

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1/10/2020 | 3.34 | 840 | 2800 |

Cuando el usuario selecciona resumir por **Clase de transacción** y **Categoría**, se importará la siguiente información:

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 1/10/2020 | 6 | 200 | 1200 |

Cuando el usuario selecciona resumir por **Clase de transacción**, **Categoría** y **Tarea de nodo hoja**, se importará lo siguiente. Observe que este resultado es el mismo que el del proyecto:

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| Tarea B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarea C | Hotel | 1/11/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
