---
title: Estimaciones financieras de materiales en proyectos
description: Este tema proporciona información sobre cómo definir o estimar materiales basándose en el proyecto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1717abb8f37acb7ab5f4e24b9323b3d958b40b13d7da44c0bbfa88eea28b99ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992632"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimaciones financieras de materiales en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations permite a los gerentes de proyecto definir los costes de material basándose en el proyecto para cada proyecto o tarea. Cada estimación de material se puede asociar con una tarea de proyecto específica. Los gastos se clasifican en diferentes categorías de gastos, que se definen a nivel organizativo. El precio y los costes de cada categoría de gastos se definen en la lista de precios. 

Complete los siguientes pasos para ver, agregar o eliminar una estimación de material del proyecto.

1. Vaya a **Proyectos** y seleccione el proyecto que quiera actualizar.
2. En la pestaña **Estimaciones de materiales**, consulte la lista de estimaciones de materiales del proyecto.
3. Seleccione **Nueva estimación de materiales** para crear una nueva estimación de materiales. O seleccione una estimación de material para eliminar y luego seleccione **Eliminar estimación de material**.

La siguiente tabla proporciona información sobre los campos de **Línea de estimación de material** en un proyecto. 

| **Campo** | **Descripción** | **Impacto posterior** |
| --- | --- | --- |
| Tarea | Lista de tareas en el proyecto. Esto incluye tareas de resumen y de nodo hoja. | Cuando selecciona una tarea para una línea de estimación de material, el coste de material estimado y las ventas de material estimadas para una tarea se ven afectados. Si este campo se deja vacío, se realiza un seguimiento de la estimación de material y se resume solo a nivel de proyecto. |
| Seleccionar producto |  Puede especificar si esta línea de estimación es para un producto existente (catálogo) o un producto fuera de catálogo. | Este campo determina si selecciona un producto del catálogo o un producto fuera del catálogo. |
| Producto | El identificador del producto del catálogo de productos. Cuando selecciona un identificador de producto, el valor en el campo **Seleccionar producto** se actualiza automáticamente a **Producto existente**. El identificador se utiliza para recuperar los precios de coste y venta de la lista de precios. | No hay impacto posterior para este campo. |
| Descripción de producto fuera de catálogo | Un campo de texto para escribir el nombre del producto. Este campo debe utilizarse cuando selecciona **Fuera de catálogo** en el campo **Seleccionar producto**.| No hay impacto posterior para este campo. |
| Fecha de inicio | La fecha prevista en la que se espera que se utilice el material. | No hay impacto posterior para este campo. |
| Unidad de venta | El valor predeterminado en este campo proviene del grupo de unidades predeterminado en el producto del catálogo. Puede actualizar este campo para seleccionar otro grupo de unidades. | No hay impacto posterior para este campo. |
| Unidad | El valor de este campo proviene de la unidad predeterminada del producto seleccionado. Puede actualizar este campo para seleccionar otra unidad. | Cambiar la unidad da como resultado un precio y un coste unitarios predeterminados diferentes. |
| Cantidad | La cantidad estimada de producto que se utilizará en el proyecto. | No hay impacto posterior para este campo. |
| Coste unitario | El coste unitario del producto seleccionado y la combinación de unidades según lo establecido en la lista de precios de coste aplicable. | El coste unitario siempre se muestra en la divisa de coste del proyecto. Si no hay una configuración de coste unitario para la combinación del producto y la configuración de la unidad en la lista de precios, el coste unitario se establecerá por defecto en 0,00. |
| Precio por unidad | El precio del producto seleccionado y la combinación de unidades según lo establecido en la lista de precios de ventas aplicable. | El precio unitario siempre se muestra en la divisa de ventas del proyecto. Si no hay una configuración de coste unitario para la combinación del producto y la configuración de la unidad en la lista de precios, el precio unitario se establecerá por defecto en 0,00.|
| Coste total | El importe del coste que se calcula como cantidad \* coste unitario.| El importe de coste siempre se muestra en la divisa de coste del proyecto. |
| Total ventas | El importe de ventas que se calcula como cantidad \* precio unitario. | El importe de ventas siempre se muestra en la divisa de ventas del proyecto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
