---
title: Listas de precios predeterminadas
description: Este artículo proporciona información sobre las ventas predeterminadas y las listas de precios en Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410284"
---
# <a name="default-price-lists"></a>Listas de precios predeterminadas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

## <a name="sales-price-lists"></a>Listas de precios de venta

Cada cotización y contrato de proyecto en Dynamics 365 Project Operations contiene una lista de precios de venta predeterminada. 

### <a name="price-list-default-on-project-quotes"></a>Lista de precios predeterminada en cotizaciones de proyectos
El sistema completa el siguiente proceso para determinar qué lista de precios predeterminar en una cotización de proyecto:

1. El sistema examina las listas de precios que se adjuntan a las listas de precios del proyecto de la cuenta. 
1. Si no hay listas de precios del proyecto adjuntas al registro de la cuenta, el sistema examina las listas de precios de venta adjuntas a los parámetros del proyecto que coinciden con la moneda de la cotización del proyecto.
1. A continuación, el sistema verifica la fecha de vigencia de las listas de precios que coinciden con el rango de fechas de la cotización del proyecto. Específicamente, la fecha en la que se creó la cotización.
1. Si hay varias listas de precios que son efectivas para la fecha de la cotización del proyecto, todas las listas de precios están predeterminadas en la cotización del proyecto.
1. Si no hay listas de precios vigentes para la fecha de la cotización del proyecto, no hay una lista de precios del proyecto predeterminada en la cotización del proyecto. Aparecerá un mensaje de advertencia en la cotización del proyecto. El mensaje indica que las cifras reales y estimadas en el proyecto no tendrán fijados los precios porque no se ha adjuntado la lista de precios del proyecto.

### <a name="price-list-default-on-project-contracts"></a>Lista de precios predeterminada en contratos de proyectos 
El sistema completa el siguiente proceso para determinar qué lista de precios predeterminar en un contrato de proyecto:

1. Si el contrato se crea a partir de una cotización, las listas de precios del proyecto en la cotización se copian por separado y se adjuntan al contrato del proyecto.
1. Si el contrato se crea desde cero, el sistema examina las listas de precios que se adjuntan a las listas de precios del proyecto de la cuenta. Si no hay listas de precios del proyecto adjuntas al registro de la cuenta, el sistema examina las listas de precios de venta adjuntas a los parámetros del proyecto que coinciden con la moneda del contrato del proyecto.
1. A continuación, el sistema verifica la fecha de vigencia de las listas de precios que coinciden con el rango de fechas del contrato del proyecto. Específicamente, la fecha en la que se creó el contrato.
1. Si hay varias listas de precios que son efectivas para la fecha del contrato, todas las listas de precios están predeterminadas en el contrato.
1. Si no hay listas de precios vigentes para la fecha del contrato, no hay una lista de precios del proyecto predeterminada en el contrato. Aparecerá un mensaje de advertencia en el contrato del proyecto. El mensaje indica que las cifras reales y estimadas en el proyecto no tendrán fijados los precios porque no se ha adjuntado la lista de precios del proyecto.

## <a name="cost-price-lists"></a>Listas de precios de coste

Las listas de precios de costo no tienen por defecto ninguna entidad en Project Operations. La determinación de la lista de precios de coste que se utilizará para los costes del proyecto siempre se realiza en función de la transacción. El sistema completa el siguiente proceso para determinar qué lista de precios usar para costes de proyecto:

1. El sistema mira las listas de precios que están adjuntas a la unidad de organización contratante del proyecto.
1. Luego, el sistema analiza la fecha de vigencia de las listas de precios que coinciden con la fecha del contexto estimado o real entrante.

    - *Contexto estimado* se refiere a cualquiera de los tres contextos de estimación en Project Operations:

        - Línea de estimación del proyecto
        - Detalle de línea de oferta
        - Detalles de línea de contrato

    - *Contexto real* se refiere a cualquiera de los tres orígenes de reales en Project Operations:

       - Líneas de diario de entrada que se crean manualmente o líneas de diario de corrección que se crean en un diario de corrección
       - Líneas de diario que se crean durante el envío de registros de tiempo, gastos o uso de material
       - Detalle de línea de factura

    Cuando Project Operations coincide con la fecha de vigencia de la línea del diario entrante o el detalle de la línea de la factura en el *contexto real*, utiliza el campo **Fecha de transacción**.

    - Si hay varias listas de precios vigentes para la fecha del contexto estimado o real entrante, se selecciona la lista de precios creada más recientemente.
    - Si no hay listas de precios del proyecto adjuntas a la unidad de organización contratante del proyecto , el sistema examina las listas de precios de coste adjuntas a los parámetros del proyecto que coinciden con la moneda del proyecto.

## <a name="enable-multi-currency-cost-price-list"></a>Habilitar la lista de precios de coste multidivisa

Esta configuración se puede encontrar en **Configuración** \> **Parámetros**. El valor predeterminado es **No**.

Cuando esta configuración está habilitada (es decir, el valor se establece en **Sí**), el sistema se comporta de la siguiente manera:

- Permite que las listas de precios de coste en cualquier divisa se asocien con la unidad organizativa. Por ejemplo, una lista de precios de coste en la moneda EUR se puede adjuntar a una unidad organizativa en la moneda USD. El sistema continuará validando que las listas de precios de coste que se adjuntan a una unidad organizativa no tengan fechas de vigencia superpuestas.
- Valida que las listas de precios de coste que se adjuntan a los parámetros del proyecto no tengan vigencia de fechas superpuestas, incluso si tienen monedas diferentes. Este comportamiento difiere del comportamiento predeterminado (es decir, el comportamiento cuando el valor se establece en **No**). En el comportamiento predeterminado, solo las listas de precios de coste que tienen la **misma** divisa se validan para la efectividad de la fecha no superpuesta.
- Para un contexto de transacción entrante, determina la lista de precios de coste basándose únicamente en la fecha de vigencia. Este comportamiento difiere del comportamiento predeterminado, en el que el sistema selecciona la lista de precios de coste que coincide tanto con la divisa del proyecto como con la fecha de vigencia.

Debido a estos cambios en el comportamiento, los clientes de Project Operations podrán mantener una lista de precios de coste global que será relevante para toda la empresa. No tendrán que tener listas de precios en cada divisa de operaciones. La lista de precios global tendrá fecha de vigencia y permitirá configurar tarifas de coste en cualquier moneda para una combinación específica de valores de dimensión de precios. La divisa de la lista de precios de coste solo se utiliza para introducir valores por defecto cuando se crean los registros de los elementos **Precios de rol**, **Precios de categoría** y **Lista de precios**. No se utilizará para determinar la lista de precios.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
