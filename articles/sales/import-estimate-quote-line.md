---
title: Importar estimaciones de un proyecto a una línea de oferta basada en proyecto
description: En este tema se proporciona información sobre cómo importar estimaciones de un proyecto a una línea de presupuesto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908623"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importar estimaciones de un proyecto a una línea de oferta basada en proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


Si se crea un proyecto durante la fase de preventa, puede seleccionar importar la estimación financiera del proyecto a la línea de oferta basada en el proyecto.

1. Asegúrese de que la línea de oferta basada en el proyecto tenga la información del campo **Proyecto**.
2. En la pestaña **Detalles de línea de oferta**, seleccione **Importar desde estimación de proyecto**.
3. En la página de diálogo que se abre, seleccione una de las siguientes opciones de resumen.

  - **Clase de transacción**
  - **Categoría**
  - **Rol** 
  - **Tarea de proyecto**

Según su selección, se copia la estimación del proyecto para todas las clases de transacciones incluidas en esta línea de oferta. Para comprobar qué clases de transacciones están incluidas, seleccione la pestaña **General** de la línea de oferta basada en el proyecto, y verifique los valores para **Incluir tiempo**, **Incluir gastos** e **Incluir tarifas**.

Cuando importe estimaciones, el sistema establecerá el precio predeterminado según las listas de precios del proyecto adjuntas a la oferta y el tipo de facturación configurado en la línea de oferta basada en el proyecto. Si una función o categoría se configura en la línea de oferta basada en el proyecto como no imputable, la línea de estimación importada se establecerá como no imputable y no se sumará al valor cotizado de la línea de oferta.

Cuando una línea de oferta tiene detalles de línea, los campos **Valor de oferta** e **Impuesto estimado** de la línea de oferta están resumidos y no se pueden editar.

Cuando se seleccionan varias opciones de resumen, el resumen intenta resumir conforme a todas las opciones seleccionadas. Esto significa que la salida de las líneas de oferta importadas será mayor que si seleccionara solo una opción de resumen.

Por ejemplo, si el proyecto tiene las siguientes líneas de estimación de gastos.

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| Tarea B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarea C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Cuando el usuario selecciona resumir por clase de transacción, se importará la siguiente información.

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| | | 1/10/2020 | 3.34 | 840 | 2800 |

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