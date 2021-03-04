---
title: Configurar la gestión de gastos
description: Este artículo describe las consideraciones y las decisiones que debe tomar durante el proceso de planificación antes de configurar la administración de gastos en Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960358"
---
# <a name="configure-expense-management"></a>Configurar la gestión de gastos

Este tema describe las consideraciones y las decisiones que debe tomar durante el proceso de planificación antes de configurar la administración de gastos. En la Gestión de gastos, puede almacenar información sobre métodos de pago, solicitudes de viaje, informes de gastos, políticas, etc.

Debido a que muchas de las decisiones que toma cuando planifica su configuración para la gestión de gastos se basan en la jerarquía y la estructura financiera de su organización, debe consultar los documentos de planificación para esas áreas.

## <a name="intercompany-expenses"></a>Gastos de empresas vinculadas

Cuando habilita los gastos de empresas vinculadas, permite que las entidades legales y los empleados incurran en gastos en nombre de otra entidad legal y cobren el pago de la entidad legal de empleo dentro de su organización. Por ejemplo, un empleado de la entidad legal A completa un proyecto para la entidad legal B y el proyecto incurre en gastos relacionados con viajes. Si los gastos de empresas vinculadas están habilitados, el empleado puede presentar un informe de gastos que contabilizará el gasto en la entidad jurídica B, y el gasto deberá pagarlo la entidad jurídica A. Si su organización no tiene varias entidades jurídicas, no t tiene que habilitar los gastos de empresas vinculadas.

**Decisión:** ¿Quiere habilitar los gastos de empresas vinculadas?

## <a name="financial-management"></a>Administración financiera

La gestión de gastos está estrechamente integrada con la gestión financiera de su organización. Gran parte de su configuración para la gestión de gastos se basará en las decisiones que haya tomado sobre las finanzas de su organización. Las siguientes secciones describen las diversas áreas que requieren planificación y decisiones, según las decisiones financieras de su organización y la orientación de su equipo de liderazgo.

### <a name="per-diems"></a>Dietas

Debe definir las dietas de los empleados que proporciona su organización. Debido a que las dietas se utilizan normalmente para cubrir gastos como comidas, alojamiento y otros gastos incidentales, puede crear reglas para las dietas que ofrece su organización. las tarifas de dietas pueden basarse en la época del año, el lugar de viaje o ambos. Cuando define una regla de dietas, puede especificar que se retendrá un porcentaje de la tarifa de dieta si un trabajador recibe comidas o servicios gratuitos. También puede definir niveles de tarifas de dietas para establecer el mínimo y máximo de horas que la tarifa de dieta puede aplicarse al viaje de un trabajador.

**Decisiones:**

- Reglas predeterminadas de dietas para el primer y último día:

    - ¿Cuál es la cantidad mínima de horas que un empleado puede reclamar por día y aún recibir dietas?
    - ¿Hay una reducción en la cantidad que se ofrece por las comidas del primer y último día? Si hay una reducción, ¿cuál es el porcentaje de la reducción?
    - ¿Hay una reducción en la cantidad que se ofrece por un hotel del primer y último día? Si hay una reducción, ¿cuál es el porcentaje de la reducción?
    - ¿Hay una reducción en la cantidad que se ofrece por un otros gastos del primer y último día? Si hay una reducción, ¿cuál es el porcentaje de la reducción?

- Reglas de dietas predeterminadas:

    - ¿Existe una reducción porcentual en la asignación de dietas para cada comida si, por ejemplo, la comida es gratuita? Si hay una reducción, ¿cuál es el porcentaje de la reducción para cada comida?
    - ¿Se calcula la reducción de comida por día, por viaje o por el número de comidas por día?
    - ¿Deben redondearse las cantidades de las dietas de la manera habitual o redondearlas hacia arriba?
    - ¿Se calculan las dietas en un período de 24 horas o en un día calendario?

- Reglas de dietas que se basan en la ubicación:

    - ¿Varían las tarifas de dietas según la ubicación? ¿Qué ubicaciones están incluidas?
    - Si las tarifas de dietas varían según la ubicación, para cada ubicación, qué porcentaje se proporciona para los siguientes tipos de gastos:

        - Comidas
        - Hotel
        - Otros gastos

### <a name="expense-management-journals-and-accounts"></a>Diarios y cuentas de gestión de gastos

La gestión de gastos requiere que utilice varios diarios y cuentas. Debe decidir, por ejemplo, si se utiliza la misma cuenta para adelantos en efectivo y disputas de tarjetas de crédito.

**Decisiones:**

- ¿En qué diario del libro mayor se registran los informes de gastos aprobados?
- ¿Qué cuenta se utiliza para adelantos en efectivo?
- ¿Deben contabilizarse los anticipos en efectivo inmediatamente?

### <a name="payment-methods"></a>Métodos de pago

Cuando permite que los empleados incurran en gastos en nombre de su empresa, debe definir los métodos de pago que los empleados pueden utilizar. Por ejemplo, puede permitir que los empleados usen efectivo o una tarjeta de crédito corporativa. También puede permitir que los empleados usen tarjetas de crédito personales y luego reembolsar a los empleados. Debe tomar las siguientes decisiones para cada método de pago que permita.

**Decisiones:**

- ¿Qué métodos de pago están permitidos?
- ¿A quién pertenecen los gastos del método de pago?
- ¿Existe un tipo de cuenta de compensación? Si hay un tipo de cuenta de compensación, ¿cuál es?
- Si hay una cuenta de compensación, ¿cuál es?
- Si el método de pago es una tarjeta de crédito, ¿debe utilizarse el método de pago solo con transacciones importadas?

### <a name="expense-categories-and-shared-categories"></a>Categorías de gasto y categorías compartidas

Cuando los empleados crean un informe de gastos, cada gasto que registran debe asociarse con una categoría de gastos. Las categorías de gastos se derivan de categorías compartidas que se pueden compartir entre las entidades legales de su organización. Estas categorías también se pueden compartir en Gestión de proyectos y contabilidad, según la forma en que se defina su organización. Según la definición de su organización y la orientación del equipo de implementación, debe determinar si las categorías que se utilizan en la gestión de gastos se utilizarán solo en la gestión de gastos o si deberían compartirse entre gestión de proyectos y contabilidad y gestión de gastos. Tenga en cuetna que estas categorías se pueden compartir entre proyecto y gastos o proyecto y producción, pero no entre gastos y producción. Debe tomar las siguientes decisiones para cada categoría de gastos.

**Decisiones:**

- ¿Cuál es la categoría de gastos? Los ejemplos incluyen categorías de vuelos, hotel o kilometraje.
- ¿Se puede utilizar también la categoría de gastos en la gestión y contabilidad de proyectos?
- ¿Cuál es el tipo de gastos?
- ¿Cuál es el método de pago predeterminado para la categoría de gastos?
- ¿Deben desglosarse los gastos de la categoría de gastos?
- ¿Cuál es la cuenta principal predeterminada para la categoría de gastos?
- ¿Cuál es el grupo de impuestos sobre ventas de artículos predeterminado para la categoría de gastos?
- ¿Se permiten métodos de pago adicionales para la categoría de gastos? Si se permiten métodos de pago adicionales, ¿cuáles son?
- ¿Hay subcategorías en esta categoría de gastos? Si hay subcategorías, deberá tomar también las siguientes decisiones:

    - ¿Alguna de las subcategorías está excluida de la recuperación de impuestos?
    - ¿Cuál es el grupo de impuestos sobre ventas de artículos de las subcategorías?

Si la categoría de gastos también se utiliza en la gestión y contabilidad de proyectos, responda las preguntas restantes. De lo contrario, vaya a la sección siguiente.

- ¿Qué cuentas de costes se utilizarán para los siguientes gastos?

    - Coste
    - Asignación de nómina
    - Valor de coste WIP
    - Elemento de coste
    - Elemento de valor de coste WIP
    - Pérdida acumulada
    - Pérdida acumulada WIP

- ¿Qué cuentas de ingresos se utilizarán para los siguientes?

    - Ingresos facturados
    - Valor acumulado de ingresos de ventas
    - Trabajo en curso - Valor de ventas
    - Ingresos acumulados - Producción
    - Trabajo en curso - Producción
    - Ingresos acumulados - Ganancias
    - Beneficio WIP
    - Suscripción de ingresos acumulados
    - Suscripción WIP

### <a name="taxes"></a>Impuestos

Para los impuestos relacionados con los gastos, debe determinar qué se incluye o habilita en los informes de gastos.

**Decisiones:**

- ¿El impuesto sobre las ventas está incluido en los montos de gastos?
- ¿Debe habilitarse la recuperación de impuestos sobre los gastos?

    > [!NOTE]
    > Cuando estaba planificando el libro mayor, si decidió aplicar las reglas del impuesto sobre las ventas y el impuesto sobre el uso de EE. (Para aplicar las reglas de impuestos sobre las ventas y sobre el uso de EE. UU., establezca la opción **Aplicar reglas de impuestos sobre las ventas** opción a **Sí**).

## <a name="policies"></a>Directivas

Al crear directivas de informes de gastos, puede ayudar a su organización a ahorrar tiempo y dinero cuando los empleados incurren en gastos en su nombre. Las directivas ayudan a garantizar que los empleados se mantengan dentro del presupuesto, proporcionen toda la información requerida y gasten el dinero solo cuando lo requieran. Debe tomar las siguientes decisiones para cada política de informe de gastos y cada política de aprobación de informe de gastos que cree.

**Decisiones:**

- ¿Cuál es el nombre de la directiva?
- ¿Para qué es la directiva de gastos?
- Si anteriormente decidió habilitar los gastos de empresas vinculadas, ¿a qué empresas de su organización se aplicará esta directiva?
- ¿Cuándo entra en vigencia la directiva?
- ¿Cuándo vence la directiva?
- ¿Qué es la regla de la directiva?
- ¿Cuál es el resultado de la regla de la directiva?
