---
title: Configurar categorías de gasto
description: Este tema proporciona información sobre cómo configurar categorías de gastos y categorías compartidas para informes de gastos.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085038"
---
# <a name="set-up-expense-categories"></a>Configurar categorías de gasto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Cuando los empleados crean informes de gastos, cada gasto que registran debe asociarse con una categoría de gastos. Las categorías de gastos se derivan de categorías compartidas que se pueden compartir entre las entidades legales de su organización. Dependiendo de cómo se defina su organización, estas categorías de gastos también se pueden compartir en otras áreas. Según la definición de su organización y la orientación del equipo de implementación, debe determinar si las categorías que se utilizan en la gestión de gastos se utilizarán solo en la gestión de gastos o deben compartirse en otras áreas.

> [!NOTE]
> Estas categorías se pueden compartir entre la gestión de proyectos y la contabilidad y la gestión de gastos, o entre la gestión de proyectos y la contabilidad y la producción. Sin embargo, no se pueden compartir entre la gestión de gastos y la producción.

Para poder comenzar el proceso de configuración, se deben tomar las siguientes decisiones para cada categoría de gastos:

- ¿Cuál es la categoría de gastos? Los ejemplos incluyen categorías de vuelos, hotel o kilometraje.
- ¿Se puede utilizar también la categoría de gastos en la gestión y contabilidad de proyectos? Si puede hacerse, deberá tomar las siguientes decisiones:

    - ¿Qué cuentas de costes se utilizarán para los siguientes gastos?

        - Coste
        - Asignación de nómina
        - Valor de coste WIP
        - Elemento de coste
        - Elemento de valor de coste WIP
        - Pérdida acumulada
        - Pérdida acumulada WIP

    - ¿Qué cuentas de ingresos se utilizarán para las siguientes fuentes de ingresos?

        - Ingresos facturados
        - Valor acumulado de ingresos de ventas
        - Valor de ventas WIP
        - Producción de ingresos acumulados
        - Producción WIP
        - Beneficios de ingresos acumulados
        - Beneficio WIP
        - Suscripción de ingresos acumulados
        - Suscripción WIP

- ¿Cuál es el tipo de gastos?
- ¿Cuál es el método de pago predeterminado para la categoría de gastos?
- ¿Deben desglosarse los gastos de la categoría de gastos?
- ¿Cuál es la cuenta principal predeterminada para la categoría de gastos?
- ¿Cuál es el grupo de impuestos sobre ventas de artículos predeterminado para la categoría de gastos?
- ¿Se permiten métodos de pago adicionales para la categoría de gastos? En ese caso, ¿qué secciones hay?
- ¿Hay subcategorías en esta categoría de gastos? Si hay subcategorías, deberá tomar también las siguientes decisiones:

    - ¿Alguna de las subcategorías está excluida de la recuperación de impuestos?
    - ¿Cuál es el grupo de impuestos sobre ventas de artículos de las subcategorías?
