---
title: Importar una estimación a una línea de contrato basada en proyecto
description: En este tema se proporciona información sobre cómo importar estimaciones de un proyecto a una línea de contrato.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6dde924c24dcffe2a8fb690e6eb429e4c3d9fb28
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126414"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importar una estimación a una línea de contrato basada en proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

En Dynamics 365 Project Operations, puede importar estimaciones de un proyecto a una línea de contrato basada en proyecto.

1. Verifique que el campo **Proyecto** en la línea de contrato basada en proyecto se ha rellenado.
2. En la pestaña **Detalles de línea de contrato**, en la subcuadrícula, seleccione **Importar desde estimación de proyecto**. Se abre una página de diálogo con opciones de resumen. Las opciones de resumen disponibles son **Clase de transacción**, **Categoría**, **Rol** y **Tarea de proyecto**. Según la selección para resumir, se copia la estimación del proyecto para todas las clases de transacciones incluidas en esta línea de contrato. 
3. Para comprobar qué clases de transacciones están incluidas, en la pestaña **General** de la línea de contrato, verifique los valores en los campos **Incluir tiempo**, **Incluir gastos** e **Incluir tarifas**.

Cuando importe estimaciones, las aplicación establecerá el precio predeterminado según las listas de precios del contrato adjuntas a la oferta y el tipo de facturación configurado en la línea de contrato. Si una tarea, rol o categoría se configura en la línea de contrato como no imputable, la línea de estimación importada para ese rol o categoría será no imputable y no se sumará al valor del contrato de la línea de contrato.

Cuando una línea de contrato tiene detalles de línea, los campos **Valor de compra** e **Impuesto estimado** de la línea de contrato están resumidos y no se pueden editar.

Cuando se seleccionan varias opciones de resumen, el sistema intenta resumir conforme a todas las opciones seleccionadas. La salida de resumen da como resultado más líneas de contrato importadas que si selecciona solo una opción de resumen.

Por ejemplo, si el proyecto tenía las siguientes líneas de estimación de gastos:

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| Tarea B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarea C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Cuando el usuario selecciona resumir por **Clase de transacción**, se importará la siguiente información:

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 1/10/2020 | 3.34 | 840 | 2800 |

Cuando el usuario selecciona resumir por **Clase de transacción** y **Categoría**, se importará la siguiente información:

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 1/10/2020 | 6 | 200 | 1200 |

Cuando el usuario selecciona resumir por **Clase de transacción**, **Categoría** y **Tarea de nodo hoja**, se importará lo siguiente. Observe que este resultado es el mismo que el del proyecto:

| Tarea | Categoría | Fecha | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- | --- |
| Tarea A | Vuelos | 1/10/2020 | 4 | 400 | 1600 |
| Tarea B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarea C | Hotel | 1/11/2020 | 2 | 200 | 400 |