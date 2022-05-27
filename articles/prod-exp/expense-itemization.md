---
title: Desglose de gastos
description: Este tema explica cómo detallar los gastos utilizando el espacio de trabajo de gastos reinventado.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574543"
---
# <a name="expense-itemization"></a>Desglose de gastos

[!include [banner](../includes/banner.md)]

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las organizaciones a menudo requieren que los empleados proporcionen un desglose detallado de los gastos incurridos durante el viaje. Por ejemplo, un folio de hotel puede contener varias líneas detalladas para tarifa de habitación, impuestos, estacionamiento y otros gastos diversos incurridos cada día durante la duración de la estadía. O un gasto de comida puede requerir que proporcione un desglose más detallado para el desayuno, el almuerzo o la cena. Cualesquiera que sean las necesidades de la organización, cada categoría de gasto se puede configurar para reflejar las subcategorías o los elementos de línea que componen un gasto. Si bien el desglose siempre se ha apoyado en **Administración de gastos**, el espacio de trabajo **Gasto reinventado** permite una enumeración más eficiente cuando la función **Capacidad para detallar los gastos recurrentes rápidamente** está habilitado.  

## <a name="enable-quick-itemization"></a>Habilitar desglose rápido 

Puedes usar la característica **Capacidad para detallar los gastos recurrentes rápidamente** para detallar los gastos recurrentes rápidamente mientras evita la necesidad de ingresar los gastos diarios cada vez durante la duración de la estadía. Complete los siguientes pasos para habilitar el desglose rápido.

1. Vaya al espacio de trabajo **Gestión de funciones** y en la lista de funciones, ubique y seleccione **Informes de gastos reinventados**. 
2. Seleccione **Habilitar ahora**. 
3. En la lista de funciones, busque y seleccione **Capacidad para detallar los gastos recurrentes rápidamente**.
4. Seleccione **Habilitar ahora**. 

## <a name="itemization-grid"></a>Cuadrícula de desglose 

Si una categoría de gastos tiene subcategorías o diferentes componentes que componen ese gasto, entonces se puede desglosar. Para detallar un gasto, seleccione la línea de gastos en el informe de gastos y en el panel **Detalles de gastos**, seleccione **Comportamiento** > **Desglosar**. El control deslizante **Desglose** revela una cuadrícula con campos. La siguiente tabla proporciona un ejemplo de cada campo en la cuadrícula y cómo se representa el campo en el informe de gastos. 

|     Campo          |     Description                                                                                  |     Ejemplo              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subcategoría    |     La lista de subcategorías configuradas bajo el tipo de categoría de gastos, **Hotel**.             |     Tarifa diaria de la habitación      |
|     Fecha de inicio     |     La fecha en la que se incurrió por primera vez en la partida de gastos.                                           |     13/09/2021           |
|     Tarifa diaria     |     El monto incurrido por la partida de gastos.                                                    |     200                  |
|     Cantidad       |     El número de veces que se repite la carga a lo largo de un período continuo.                       |     3                    |

![Desglosar gastos.](media/Itemization%20screen%201.png)

Cuando guarde un desglose, verá una línea desglosada individual para la cantidad especificada en la cuadrícula de Desglose. Cada línea comienza en la fecha que se especifica en la cuadrícula.

![Informe desglosado.](media/Itemization%20screen%202.png)

