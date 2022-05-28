---
title: Listas de precios predeterminadas
description: Este tema proporciona información sobre las ventas predeterminadas y listas de precio de costes en Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 83458d6f62c8790eb967cf07c21ffe7851e14a3a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591793"
---
# <a name="default-price-lists"></a>Listas de precios predeterminadas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

## <a name="sales-price-lists"></a>Listas de precios de venta

Cada cotización y contrato de proyecto en Dynamics 365 Project Operations contiene una lista de precios de venta predeterminada. 

### <a name="price-list-default-on-project-quotes"></a>Lista de precios predeterminada en cotizaciones de proyectos
El sistema completa el siguiente proceso para determinar qué lista de precios predeterminar en una cotización de proyecto:

1. El sistema examina las listas de precios que se adjuntan a las listas de precios del proyecto de la cuenta. 
2. Si hay listas de precios del proyecto adjuntas al registro de la cuenta, el sistema examina las listas de precios de venta adjuntas a los parámetros del proyecto que coinciden con la moneda de la cotización del proyecto.
3. A continuación, el sistema verifica la fecha de vigencia de las listas de precios que coinciden con el rango de fechas de la cotización del proyecto. Específicamente, la fecha en la que se creó la cotización.
4. Si hay varias listas de precios que son efectivas para la fecha de la cotización del proyecto, todas las listas de precios están predeterminadas en la cotización del proyecto.
5. Si no hay listas de precios vigentes para la fecha de la cotización del proyecto, no hay una lista de precios del proyecto predeterminada en la cotización del proyecto. Aparecerá un mensaje de advertencia en la cotización del proyecto. El mensaje indica que las cifras reales y estimadas en el proyecto no tendrán fijados los precios porque no se ha adjuntado la lista de precios del proyecto.

### <a name="price-list-default-on-project-contracts"></a>Lista de precios predeterminada en contratos de proyectos 
El sistema completa el siguiente proceso para determinar qué lista de precios predeterminar en un contrato de proyecto:

1. Si el contrato se crea a partir de una cotización, las listas de precios del proyecto en la cotización se copian por separado y se adjuntan al contrato del proyecto.
2. Si el contrato se crea desde cero, el sistema examina las listas de precios que se adjuntan a las listas de precios del proyecto de la cuenta. Si no hay listas de precios del proyecto adjuntas al registro de la cuenta, el sistema examina las listas de precios de venta adjuntas a los parámetros del proyecto que coinciden con la moneda del contrato del proyecto.
4. A continuación, el sistema verifica la fecha de vigencia de las listas de precios que coinciden con el rango de fechas del contrato del proyecto. Específicamente, la fecha en la que se creó el contrato.
5. Si hay varias listas de precios que son efectivas para la fecha del contrato, todas las listas de precios están predeterminadas en el contrato.
6. Si no hay listas de precios vigentes para la fecha del contrato, no hay una lista de precios del proyecto predeterminada en el contrato. Aparecerá un mensaje de advertencia en el contrato del proyecto. El mensaje indica que las cifras reales y estimadas en el proyecto no tendrán fijados los precios porque no se ha adjuntado la lista de precios del proyecto.

## <a name="cost-price-lists"></a>Listas de precios de coste

Las listas de precios de costo no tienen por defecto ninguna entidad en Project Operations. La determinación de la lista de precios de coste que se utilizará para los costes del proyecto siempre se realiza en el momento. El sistema completa el siguiente proceso para determinar qué lista de precios usar para costes de proyecto:

1. El sistema primero mira las listas de precios que están adjuntas a la unidad de organización contratante del proyecto.
2. Luego, el sistema analiza la fecha de vigencia de las listas de precios que coinciden con la fecha del presupuesto entrante o la línea real. En esta situación, *línea de estimación* se refiere a los tres contextos de estimación en Project Operations:

    - Línea de estimación del proyecto
    - Detalle de línea de oferta
    - Detalles de línea de contrato
  
3. Si hay varias listas de precios vigentes para la fecha de la estimación entrante o real, se selecciona la lista de precios creada más recientemente.
4. Si no hay listas de precios del proyecto adjuntas a la unidad de organización contratante del proyecto , el sistema examina las listas de precios de coste adjuntas a los parámetros del proyecto que coinciden con la moneda del proyecto.
5. Luego, el sistema analiza la fecha de vigencia de las listas de precios que coinciden con la fecha del presupuesto entrante o la línea real. 
6. Si hay varias listas de precios vigentes para la fecha de la estimación entrante o real, se selecciona la lista de precios creada más recientemente.
7. Si no hay listas de precios de coste adjuntas a los parámetros del proyecto que coincidan con la moneda y la fecha de vigencia, el sistema establece la tasa de coste por defecto en cero (0) en la estimación entrante o en la línea real.


[!INCLUDE[footer-include](../includes/footer-banner.md)]