---
title: Escenarios de varias divisas (versión 3.x)
description: En este tema se proporciona información sobre escenarios de varias divisas.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 33e44297dc80801c3e4416cd9fc3bedae5f3c4ba
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291730"
---
# <a name="multiple-currency-scenarios"></a>Escenarios de varias divisas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 tiene dos conceptos de divisas:

- **Divisa de la transacción**: se trata de la divisa en la que se produce una transacción. 
- **Divisa base**: divisa de la instancia de Microsoft Dynamics 365. Esta divisa se configura cuando se aprovisiona una instancia de Microsoft Dynamics 365. No se puede cambiar.

Por ejemplo, Contoso Estados Unidos vendió 100 camisetas a un cliente del Reino Unido a 15 libras esterlinas (GBP) la unidad. La siguiente tabla muestra cómo se registra esta transacción en la entidad Producto del pedido.

| Producto | Cantidad | Precio unitario | Divisa | Importe | Tipo de cambio | Precio por unidad (base)| Importe (base)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Camiseta | 100      | 15             | GBP      | 1500   | 0,94          | 17.25 USD               | 1,725 USD       |

La columna **Divisa** muestra la divisa de la transacción, que es la divisa en la que se produjo la venta. La columna **Tipo de cambio** indica el tipo de cambio entre la divisa de la transacción y la divisa base. La divisa base es el dólar de EE. UU. (USD). Esta divisa base se configuró cuando se aprovisionó la instancia de Dynamics 365.
Tal como muestra la tabla, cada transacción se registra en la divisa de la transacción y en la divisa base. Dynamics 365 usa el tipo de cambio de divisa para calcular los importes en la divisa base.

## <a name="project-service-automation-extensions"></a>Extensiones de Project Service Automation

Dynamics 365 Project Service Automation afecta a la divisa de la transacción porque las transacciones comerciales suelen tener dos aspectos: coste y ventas.

A continuación se describen las entidades que se consideran transacciones comerciales:

- Detalle de línea de oferta
- Detalle de línea de contrato del proyecto
- Línea de estimación
- Línea de diario
- Detalle de línea de factura
- Real

En cada una de estas entidades existe un registro que representa el importe del coste o el importe de las ventas. Al igual que ocurre para cualquier entidad de Dynamics 365 que tenga un campo **Importe**, cada registro incluye importes tanto en la divisa de la transacción y la divisa base. 

PSA amplía el concepto de divisa de la transacción para el coste y las ventas de las maneras siguientes:

- La divisa de la transacción de coste de las transacciones de tiempo proceden siempre de la divisa de la unidad organizativa que posee o administra el proyecto. Esta unidad organizativa se conoce como unidad de contratación.
- La divisa de la transacción de ventas para las transacciones de tiempo y gasto siempre procede de la divisa del contrato del proyecto.
- La divisa de la transacción de coste de los gastos procede de la divisa con la que se creó la entrada de gastos.

## <a name="multiple-currency-scenario"></a>Escenario de varias divisas

Esta sección describe un ejemplo de un proyecto que Contoso UK entrega a un cliente denominado Fabrikam, Japan. A continuación se indica cómo se ha configurado el escenario:

1. La divisa GBP y el yen japonés (JPY) están configurados en **Configuración** \> **Administración de empresas** \> **Divisas**. 
2. Se configura una cuenta de cliente con el nombre **Fabrikam - Japan** y se selecciona el JPY como divisa en la cuenta.
3. Se configura una unidad organizativa con el nombre **Contoso UK** y se selecciona la GBP como divisa.
4. Se crea un contrato de proyecto donde se especifica **Contoso UK** como unidad de contratación y **Fabrikam – Japan** como cliente.
5. Las líneas de contrato del proyecto se crean en función de las organizaciones de facturación de las distintas clases de transacciones del proyecto, como, por ejemplo, la facturación de tiempo frente a la facturación de gastos.
6. Se crea un proyecto en el que se especifica **Contoso UK** como unidad de contratación. Este proyecto se crea y se asigna a las líneas de contrato del proyecto.


Durante la estimación que utiliza el detalle de la línea de presupuesto, el detalle de la línea de contrato del proyecto, o bien en la línea de estimación de la programación, siempre se crean dos registros en la entidad. Un registro es para el coste y el otro es para las ventas.

- De forma predeterminada, la divisa de la transacción del registro de costes se establece con la divisa de la unidad de contratación de proyecto. En este ejemplo, la divisa es GBP.
- De forma predeterminada, la divisa de la transacción del registro de ventas se establece con la divisa del contrato del proyecto. En este ejemplo, la divisa es JPY.

Cuando se crean los datos reales del tiempo utilizando la entrada de tiempo o la línea del diario, se crea el comportamiento siguiente:

- De forma predeterminada, la divisa de la transacción del registro de costes se establece con la divisa de la unidad de contratación de proyecto.
- De forma predeterminada, la divisa de la transacción del registro de ventas se establece con la divisa del contrato del proyecto.

Cuando se crean los datos reales de los gastos según la entrada de tiempo o la línea del diario, se crea el comportamiento siguiente:

- Puede registrar el importe del gasto en cualquier divisa. Seleccione la divisa con el selector de divisas de la página **Entrada de gastos** o la página **Línea de diario**. De forma predeterminada, la divisa de la transacción del registro de costes se establece con la divisa de la entrada de gastos. 
- De forma predeterminada, la divisa de la transacción para el registro de ventas se establece con la divisa del contrato del proyecto. Para establecer esta divisa, el sistema primero convierte el importe de la transacción a la divisa que el usuario especificó en la divisa base. A continuación, se convierte el importe a la divisa del contrato de proyecto. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Cálculo de acumulaciones cuando los datos reales de proyecto se registran en varias divisas de transacciones

Dynamics 365 gestiona las acumulaciones de importes en diferentes divisas de forma automática. A continuación se muestra un ejemplo.

| Clase de transacción | Tipo de transacción| Date   | Recurso | Categoría de transacción | Cantidad | Precio unitario | Importe      | Tipo de cambio | Importe en divisa base |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Ventas sin facturar   | 14 jun | Antonio  |                      | 8 h    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Time              | Ventas sin facturar   | 15 jun | Antonio  |                      | 8 h    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Gasto           | Ventas sin facturar   | 16 jun | Antonio  | Hotel                | 1 ea     | 250 EUR      | 250 EUR     | 0,94          | 265,95 USD     |
| Gasto           | Ventas sin facturar   | 17 jun | Antonio  | Alquiler de vehículos           | 1 ea     | 150 EUR      | 150 EUR     | 0,94          | 159,57 USD     |

Para calcular el valor de ventas sin facturar total en el proyecto, puede crear un campo de acumulación para el campo **Importe** en todos los datos reales relacionados con las ventas sin facturar. El campo de acumulación es una construcción de Dynamics 365 que permite utilizar fórmulas rápidas en registros relacionados.


[!INCLUDE[footer-include](../includes/footer-banner.md)]