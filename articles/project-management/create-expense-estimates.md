---
title: Estimaciones financieras de gastos en proyectos
description: Este tema proporciona información sobre cómo definir o estimar los gastos basados en proyectos.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 18d8568fae35fc251d9cf48d900b8a436e2e4500
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014182"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Estimaciones financieras de gastos en proyectos
_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations permite a los gerentes de proyecto definir los gastos basados en proyectos para cada proyecto o tarea. Cada elemento de gasto se puede asociar con una tarea de proyecto específica. Los gastos se clasifican en diferentes categorías de gastos, que se definen a nivel organizativo. El precio y los costes de cada categoría de gastos se definen en la lista de precios. 

Complete los siguientes pasos para ver, agregar o eliminar un gasto del proyecto.

1. Vaya a **Proyectos** y seleccione el proyecto en el que desea trabajar.
2. Seleccione la pestaña **Estimaciones de proyecto** y vea la lista de gastos del proyecto.
3. Seleccione **Nuevo gasto** para agregar un gasto. O bien, seleccione un gasto a eliminar y luego seleccione **Eliminar gasto**.

La siguiente tabla proporciona información sobre los campos de **Línea de estimación de gastos** en un proyecto. 

| **Campo** | **Descripción** | **Impacto posterior** |
| --- | --- | --- |
| Tarea | Lista de tareas en el proyecto. Esto incluye tareas de resumen y de nodo hoja. | La selección de una tarea para una línea de estimación de gastos afectará al coste de los gastos estimados y las ventas de gastos estimados para una tarea. Si este campo se deja vacío, se realiza un seguimiento de la estimación de los gastos y se resume solo a nivel de proyecto. |
| Categoría | Una lista de categorías de transacciones que tienen categorías de gastos vinculadas en la aplicación. | La selección de una categoría determina los precios y los costes en la línea de estimación de gastos. |
| Fecha de inicio | La fecha prevista en la que se producirá el gasto. | No hay impacto posterior para este campo. |
| Unidad de venta | El valor predeterminado en este campo proviene del grupo de unidades que está configurado como valor predeterminado en la categoría seleccionada. Puede actualizar este campo para seleccionar otro grupo de unidades. | No hay impacto posterior para este campo. |
| Unidad | El valor de este campo toma como valor predeterminado la unidad predeterminada de la categoría seleccionada. Puede actualizar este campo para seleccionar otra unidad. | Cambiar la unidad da como resultado un precio y un coste unitarios predeterminados diferentes. |
| Cantidad | La cantidad del gasto estimado en el que incurrirá. | No hay impacto posterior para este campo. |
| Coste unitario | El coste de la categoría seleccionada y la combinación de unidades según lo establecido en la lista de precios de coste aplicable. | El coste unitario siempre se muestra en la divisa de coste del proyecto. |
| Precio por unidad | El precio de la categoría seleccionada y la combinación de unidades según lo establecido en la lista de precios de ventas aplicable. | El precio unitario siempre se muestra en la divisa de ventas del proyecto. |
| Coste total | El importe del coste que se calcula como cantidad \* coste unitario.| El importe de coste siempre se muestra en la divisa de coste del proyecto. |
| Total ventas | El importe de ventas que se calcula como cantidad \* precio unitario. | El importe de ventas siempre se muestra en la divisa de ventas del proyecto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
