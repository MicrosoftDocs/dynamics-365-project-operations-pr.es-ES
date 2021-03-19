---
title: Importar estimaciones de un proyecto a una línea de oferta basada en proyecto (lite)
description: En este tema se proporciona información sobre cómo importar estimaciones de un proyecto a una línea de oferta.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f3f18644a51d87cf3bb5b4effba2236eaf3d81a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273444"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line---lite"></a>Importar estimaciones de un proyecto a una línea de oferta basada en proyecto (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Si se crea un proyecto durante la fase de preventa, puede seleccionar importar la estimación financiera del proyecto a la línea de oferta basada en el proyecto.

1. Asegúrese de que la línea de oferta basada en el proyecto tenga la información del campo **Proyecto**.
2. En la pestaña **Detalles de línea de oferta**, seleccione **Importar desde estimación de proyecto**.
3. En la página de diálogo que se abre, seleccione una de las siguientes opciones de resumen.

  - **Clase de transacción**
  - **Categoría**
  - **Rol** 
  - **Tarea de proyecto**

Según su selección, se copia la estimación del proyecto para todas las clases de transacciones incluidas en esta línea de oferta. Para comprobar qué clases de transacciones están incluidas, seleccione la pestaña **General** de la línea de oferta basada en el proyecto, y verifique los valores para **Incluir tiempo**, **Incluir gastos** e **Incluir tarifas**.  Para comprobar qué tareas están incluidas, seleccione la pestaña **Tareas facturables** en la línea de la oferta.

Dependiendo de las tareas asociadas e incluidas y clases de transacción, las estimaciones para esas tareas y combinaciones de clase de transacción se importan a la línea de oferta.

Cuando importe estimaciones, el sistema establecerá el precio predeterminado según las listas de precios del proyecto adjuntas a la oferta y el tipo de facturación configurado en la línea de oferta basada en el proyecto. Si una tarea, rol o categoría se configura en la línea de oferta basada en el proyecto como no imputable, la línea de estimación importada se establecerá como no imputable y no se sumará al valor cotizado de la línea de oferta.

Cuando una línea de oferta tiene detalles de línea, los campos **Valor de oferta** e **Impuesto estimado** de la línea de oferta están resumidos y no se pueden editar.

Cuando se seleccionan varias opciones de resumen, el sistema intenta resumir conforme a todas las opciones seleccionadas. El resultado es que la salida de las líneas de cotización importadas será mayor que si seleccionara solo una opción de resumen.

Por ejemplo, si el proyecto tenía las siguientes líneas de estimación de gastos.

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| Tarea B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarea C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Cuando el usuario selecciona resumir por clase de transacción, se importará la siguiente información.

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
|||1/10/2020 | 3.34 | 840 | 2800 |

Cuando el usuario selecciona resumir por clase de transacción y categoría, se importará la siguiente información.

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| | Hotel | 1/10/2020 | 6 | 200 | 1200 |

Cuando el usuario selecciona resumir por clase de transacción, categoría y tarea de nodo hoja, se importará la siguiente información. Observe que este resultado es el mismo que el del proyecto.

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| Tarea B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarea C | Hotel | 1/11/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]