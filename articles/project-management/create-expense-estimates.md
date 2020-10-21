---
title: Estimaciones de gastos
description: Este tema proporciona información sobre cómo definir o estimar los gastos basados en proyectos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908626"
---
# <a name="expense-estimates"></a>Estimaciones de gastos
_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Junto con la definición de estimaciones basadas en recursos, Dynamics 365 Project Operations permite a los administradores de proyectos definir los gastos basados en proyectos para cada proyecto. Cada elemento de gasto se puede asociar con una tarea de proyecto o categoría de gasto específica. Las categorías de gastos se definen normalmente a nivel organizativo. El precio de cada categoría de gastos se define normalmente en la siguiente jerarquía:

- Organización
- Cliente
- Oferta/contrato

Complete los siguientes pasos para ver, agregar o eliminar un gasto del proyecto.

1. Vaya a **Proyectos** y seleccione el proyecto en el que desea trabajar.
2. Seleccione la pestaña **Estimaciones de proyecto** y vea la lista de gastos del proyecto.
3. Seleccione **Nuevo gasto** para agregar un gasto. O bien, seleccione un gasto a eliminar y luego seleccione **Eliminar gasto**.

Los siguientes atributos se definen para cada elemento de línea de gastos:

- **Categoría**: las agrupaciones comunes que se utilizan para describir todos los gastos incurridos en un proyecto.
- **Fecha de inicio**: la fecha en la que se prevé que se incurrirá en el gasto.
- **Cantidad**: el número estimado de elementos de gastos para una categoría específica.
- **Precio de coste unitario**: precio unitario utilizado para calcular el coste del gasto.
- **Precio de venta unitario**: precio unitario utilizado para calcular los precios de venta del gasto.

