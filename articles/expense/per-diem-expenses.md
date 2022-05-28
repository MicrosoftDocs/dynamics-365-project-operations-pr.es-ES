---
title: Gastos de dietas
description: En este tema se proporciona información sobre cómo trabajar con gastos de dietas.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596071"
---
# <a name="per-diem-expenses"></a>Gastos de dietas

> [!IMPORTANT] 
> La funcionalidad que se describe en este tema estará disponible para los usuarios a los que está dirigida como parte de una versión preliminar.

Un pago de dieta es una asignación diaria fija y predeterminada que una empresa paga a sus empleados por alojamiento (hoteles), comidas y gastos imprevistos en los que incurren esos empleados mientras viajan por trabajo. La empresa paga este subsidio a los empleados en lugar de pagar los gastos de viaje reales. Los empleados pueden usar su asignación de dieta de **Incidentes/Otros** para cubrir propinas, servicios de habitaciones, lavandería o tintorería para reuniones de negocios importantes. La dieta diaria puede variar, dependiendo de si el empleador elige reembolsar el costo combinado de alojamiento y comidas, o solo el costo de las comidas y gastos imprevistos.

Las tarifas de dietas pueden basarse en la época del año, el lugar de viaje o ambos. Cuando crea una regla de dieta, puede especificar que se retendrá un porcentaje de la tarifa de dietas si un empleado recibe comidas o servicios de cortesía. También puede definir un número mínimo y máximo de horas que se pueden aplicar las tarifas de dietas al desplazamiento del empleado.

La dieta se calcula como la asignación total que se ofrece por día menos la reducción de comida (costo de las comidas de cortesía) que se le proporciona al empleado.

## <a name="configure-per-diems"></a>Configurar dietas

Para configurar los gastos de dietas, siga estos pasos.

1. Vaya a **Gestión de gastos** \> **Configuración** \> **General** \> **Parámetros de gestión de gastos**.
2. En la pestaña **Dieta**, en el campo **Calcular la reducción de comidas por**, seleccione cómo se deben calcular las dietas:

    - **Tipo de comida por viaje**: calcule la dieta en función del tipo de comida que se ingresa (desayuno, almuerzo o cena) y de la reducción de comida que se especifica para cada tipo de comida para la asignación de dietas durante la duración del viaje.
    - **Tipo de comida por día**: calcule la dieta en función del tipo de comida que se ingresa (desayuno, almuerzo o cena) y de la reducción de comida que se especifica para cada tipo de comida para la asignación de dietas por día.
    - **Número de comidas por día**: calcula la dieta en base a la cantidad de comidas que se ingresan por día y en la reducción de comida por la cantidad de comidas que se proporcionan por día.

3. Vaya a **Administración de gastos** \> **Configuración** \> **Cálculos y códigos** \> **Ubicaciones de dietas**.
4. Agregue ubicaciones donde se puedan usar las dietas.
5. Para cada ubicación que agregue, en la pestaña **Dietas**, seleccione la tarifa de dietas y la moneda que son válidas entre las fechas de inicio y finalización específicas para alojamiento, comidas y otros gastos. Para configurar las tarifas de dietas y divisas, vaya a **Gestión de gastos** \> **Configuración** \> **Cálculos y códigos** \> **Dietas**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dietas en la interfaz de gastos rediseñada

La función de dietas es compatible con el espacio de trabajola rediseñado **Administración de gastos** en Microsoft Dynamics 365 Finance, versión 10.0.25 y posteriores.

Para habilitar las dietas, siga estos pasos.

1. En el espacio de trabajo **Gestión de características**, busque y seleccione la característica **Informes de gastos rediseñados** en la lista y, a continuación, seleccione **Habilitar ahora**.
2. Busque y seleccione la característica **Interfaz rediseñada de informes de gastos de dietas** en la lista y, a continuación, seleccione **Habilitar ahora**.

## <a name="how-the-feature-works"></a>Cómo funciona la característica

Esta sección proporciona ejemplos para tres escenarios de configuración. Para cada ejemplo, el campo **Calcular la reducción de comida por** se establece en un valor diferente. Para los tres ejemplos, el importe total a pagar es el mismo, hasta que se aplica la reducción de comidas. Después de ese punto, el importe total a pagar difiere para cada ejemplo.

Para crear el gasto de dietas que se usa para los tres ejemplos, siga estos pasos.

1. Vaya a **Espacios de trabajo** \> **Gestión de gastos**.
2. Seleccione **Nuevo informe de gastos**, o seleccione un informe de gastos existente.
3. Agregue un nuevo gasto. En el campo **Categoría**, seleccione **Dieta**. Seleccione la ubicación y las fechas de inicio y finalización de su viaje. La dieta para alojamiento, comidas e imprevistos (otros gastos) se calcula en base a la asignación diaria que se establece para la ubicación seleccionada.

    Por ejemplo, seleccione **Redmon (Estados Unidos)** como la ubicación. La asignación diaria para ese lugar es de 150 dólares estadounidenses (150 USD) para alojamiento, 75 USD para comidas y 5 USD para gastos imprevistos. La fecha de inicio es el 10 de enero y la fecha de finalización es el 14 de enero. Por tanto, la duración seleccionada es de cinco días cuando la configuración seleccionada es de días naturales con tiempo, y el tiempo seleccionado comienza y termina a las 12:00 a.m. en las fechas de inicio y fin. Aquí están los cálculos:

    - Importe total a pagar = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
    - Comida y parte incidental del importe total = 5 × (75 + 5) = 400 USD

Si se proporcionó desayuno, almuerzo y cena durante el viaje, esas comidas deben contabilizarse como una reducción de comidas.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Ejemplo 1: dietas donde las reducciones de comida se basan en el tipo de comida por viaje

En este ejemplo, la reducción de comidas es del 30 por ciento para el desayuno, el 30 por ciento para el almuerzo y el 40 por ciento para la cena. En la página **Parámetros de gestión de gastos**, el campo **Calcular la reducción de comida por** se establece en **Tipo de comida por viaje**. Estos son los cálculos si se proporcionaron tres desayunos, dos almuerzos y cero cenas al empleado:

- Reducción de comidas = (3 × \[75 × 30%\]) + (2 × \[75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Comidas e imprevistos = 400 – 112,50 = 287,50 USD
- Importe total a pagar = Asignación total – Reducción de comidas = 1150 – 112,50 = USD 1037,50

![Gasto de dieta en el que la reducción de comidas se basa en el tipo de comida por viaje.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Ejemplo 2: dietas en las que las reducciones de comidas se basan en el tipo de comida por día

En este ejemplo, la reducción de comidas es del 30 por ciento para el desayuno, el 30 por ciento para el almuerzo y el 40 por ciento para la cena. En la página **Parámetros de gestión de gastos**, el campo **Calcular la reducción de comida por** se establece en **Tipo de comida por día**. En este caso, en la cuadrícula **Comidas** del cuadro de diálogo **Editar gasto**, desmarque las casillas para indicar qué comidas se le proporcionaron durante su viaje.

Por ejemplo, aquí están los cálculos si se proporcionó desayuno durante los primeros tres días del viaje:

- Reducción de comida diaria para cada uno de los primeros tres días = 75 × 30 % = 22,50
- Reducción total de comidas = 3 × 22,50 = 67,50 USD
- Comidas e imprevistos para los días 1 a 3 = 75 – 22,50 = 57,50
- Total de comidas e imprevistos = Suma de comidas e imprevistos en cinco días = 400 – 67,50 = 332,50 USD
- Importe total a pagar = Importe total – Reducción de comidas = 1150 – 67,50 = 1082,50 USD

![Gasto de dieta en el que la reducción de comidas se basa en el tipo de comida por día.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Ejemplo 3: dietas en las que las reducciones de comidas se basan en el número de comidas por día

En este ejemplo, la reducción de comidas se calcula en función de la cantidad de comidas que se proporcionaron por día (es decir, el campo **Calcular la reducción de comida por** de la página **Parámetros de gestión de gastos** está configurada para **Número de comidas por día**). En la cuadrícula **Comidas** del cuadro de diálogo **Editar gasto**, desmarque las casillas para indicar qué comidas se le proporcionaron.
En este caso, la reducción de comidas se basa únicamente en el número de comidas proporcionadas y no en el tipo de comida (desayuno/almuerzo/cena) proporcionada.

Estos son los cálculos de las dietas cuando la asignación diaria es de 150 USD para alojamiento, 75 USD para comidas y 5 USD para gastos imprevistos:

- **Importe total a pagar** = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
- **Una comida:** Reducción de comida = 20 % = 15 USD
- **Dos comidas:** Reducción de comida = 50 % = 37,50 USD
- **Tres comidas:** Reducción de comida = 100 % = 75 USD

Aquí están los cálculos para la **asignación para comidas y gastos imprevistos**, que incluye 5 USD para imprevistos:

- Día 1: se proporcionan dos comidas = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Día 2: se proporcionan dos comidas = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Día 3: se proporciona una comida = (75 – 15) + 5 = 60 + 5 = 65 USD
- Día 4: no se proporciona ninguna comida = (75 – 0) + 5 = 75 + 5 = 80 USD
- Día 5: se proporcionan tres comidas = (75 – 75) + 5 = 0 + 5 = 5 USD

- Total de comidas e imprevistos = Comidas e imprevistos del Día 1 + Día 2 + Día 3 + Día 4 + Día 5 = 235 USD
- Reducción total de comidas = Reducción de comidas para el Día 1 + Día 2 + Día 3 + Día 4 + Día 5= 37,5+ 37,5+ 15 + 0+ 75 = 165 USD
- Importe total a pagar = Asignación total – Reducción total de comidas = 1150 USD – 165 USD = 985 USD

![Gasto de dieta en el que la reducción de comidas se basa en el número de comidas por día.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A partir de la versión 10.0.23 de Finance, si usa la interfaz de gastos rediseñada, no puede crear gastos de dietas que tengan fechas superpuestas. Si lo intenta, recibirá un mensaje de error.
