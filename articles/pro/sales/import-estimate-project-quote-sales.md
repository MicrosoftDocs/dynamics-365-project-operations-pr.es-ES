---
title: Importar estimaciones de un proyecto a una línea de oferta basada en proyecto (lite)
description: En este tema se proporciona información sobre cómo importar estimaciones de un proyecto a una línea de oferta.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5ac7827f3499aafb63f6bc0b8580ca52e883f272464532bd353170a12b3ae55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986152"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importar estimaciones de un proyecto a una línea de oferta basada en proyecto 

_**Se aplica a:** Implementación lite: acuerdo para factura proforma, Project Operations para escenarios basados en recursos/no mantenidos_

Si se crea un proyecto durante la fase de preventa, puede seleccionar importar la estimación financiera del proyecto a la línea de oferta basada en el proyecto.

1. Asegúrese de que la línea de oferta basada en el proyecto tenga la información del campo **Proyecto**.
2. En la pestaña **Detalles de línea de oferta**, seleccione **Importar desde estimación de proyecto**.
3. En la página de diálogo que se abre, seleccione una de las siguientes opciones de resumen.

  - **Clase de transacción**
  - **Categoría**
  - **Rol** 
  - **Tarea de proyecto**

Según su selección, se copia la estimación del proyecto para todas las clases de transacciones incluidas en esta línea de oferta. Para comprobar qué clases de transacciones están incluidas, seleccione la pestaña **General** en la línea de cotización basada en el proyecto, y verifique los valores para **Incluir tiempo**, **Incluir gastos**, **Incluir materiales** e **Incluir tarifas**.  Para comprobar qué tareas están incluidas, seleccione la pestaña **Tareas facturables** en la línea de la oferta.

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
