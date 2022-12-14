---
title: Configure la conversión de moneda para calcular precios de venta a partir de tasas de costes
description: Este artículo explica cómo configurar el comportamiento de conversión de moneda que se usará en Microsoft Dynamics 365 Project Operations cuando las transacciones de ventas se generen a partir de transacciones de costos.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816677"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Configure la conversión de moneda para calcular precios de venta a partir de tasas de costes

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

En Microsoft Dynamics 365 Project Operations, los precios de venta para las categorías de gastos se pueden configurar como valores numéricos o se pueden configurar para que se calculen en función del costo incurrido.

Cuando están configurados para calcularse en función del costo incurrido, las siguientes opciones están disponibles:

- De coste
- Porcentaje de margen sobre el costo

En escenarios en los que se incurre en el costo del gasto en una moneda que difiere de la moneda de venta del contrato del proyecto, se requiere la conversión de moneda para calcular el precio de venta en función del costo.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Comportamiento de conversión de divisas que utiliza tipos de cambio nativos de Dataverse

De forma predeterminada, Project Operations usa los tipos de cambio de moneda que se almacenan en la tabla Moneda en Dataverse. Para configurar Project Operations para usar tipos de cambio nativos para calcular los precios de venta a partir del costo, siga estos pasos.

1. Vaya a **Project Operations \> Configuración \> Parámetros**.
1. Abra la página de detalles **Parámetro del proyecto**.
1. Establezca el campo **Lógica de conversión de moneda** en un valor en blanco.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Comportamiento de conversión de moneda que utiliza tipos de cambio de aplicaciones de finanzas y operaciones

Los tipos de cambio de la tabla Moneda que está disponible de forma nativa en Dataverse no tienen fecha de vigencia. Por lo tanto, es posible que no siempre se ajusten a los requisitos que tiene para el cálculo de precios de venta a partir de tasas de costo.

Puede utilizar tipos de cambio del entorno de finanzas y operaciones para calcular el precio de venta en la divisa de venta a partir de una tasa de coste en la divisa de coste. Para configurar este comportamiento de conversión de moneda, siga estos pasos.

1. En la página **Parámetros del proyecto**, agregue el campo **Lógica de conversión de moneda**. Luego guarde y publique la personalización.
1. Vaya a **Project Operations \> Configuración \> Parámetros**.
1. Abra la página de detalles **Parámetro del proyecto**. 
1. Establezca el campo **Comportamiento de conversión de divisas** en **Extendido con respaldo predeterminado**.
1. Otorgue al rol de seguridad **Usuario de la aplicación de escritura dual** el permiso **Lectura global** para las siguientes tablas:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. En su entorno de finanzas y operaciones, ejecute los siguientes mapas de doble escritura con sincronización inicial:

    - Tipo de tasa de cambio (msdyn\_exchangeratetypes)
    - Par de divisas del tipo de cambio (msdyn\_currencyexchangeratepairs)
    - Tipos de cambio de CDS (msdyn\_currencyexchangerates)

Después de completar estos cambios, la escritura dual hará que los tipos de cambio del entorno de operaciones y finanzas estén disponibles en Dataverse. Project Operations luego utilizará esas tasas de cambio para convertir las tasas de costo a la moneda de venta del contrato.

> [!NOTE]
> Este comportamiento de conversión de moneda se aplica solo al cálculo de precios de venta a partir de tasas de costo. No se utilizará para calcular valores de moneda base de forma genérica. Los valores de moneda base siempre usarán tipos de cambio nativos de Dataverse, independientemente de si completa este procedimiento.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
