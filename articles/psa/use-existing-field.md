---
title: Uso de un campo existente en Project Service como dimensión de precios
description: En este tema se proporciona información sobre el uso de campos existentes de Project Service como dimensiones de precios.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 075461042724c92e480e0df5ba976baf58542f479661f4c615aa442a150d0f8a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004602"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Uso de un campo existente en Project Service como dimensión de precios

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) tiene muchos campos en la entidad **Datos reales** que se pueden usar como dimensiones de precios para precios basados en recursos en organizaciones de proyectos. Por ejemplo, un campo común es **Recurso que se puede reservar**. Es posible que las compañías más pequeñas, con menos de 20-30 recursos facturables, consideren que tener tasas de coste y facturas específicas para cada recurso es un enfoque más simple. Sin embargo, a medida que crece el personal facturable, las tasas específicas podrían ser muy difíciles de mantener, ya que el coste de los recursos y las tasas de facturación comienzan a variar a medida que los recursos ascienden, adquieren más experiencia o consiguen un conjunto de habilidades diferente. Puesto que este enfoque todavía funciona para compañías de cierto tamaño, consulte [Usar un recurso reservable como dimensión de precios](bookable-resource-pricing-dimension.md) para comprender cómo se puede usar un campo de Project Service existente como dimensión de precios.

Otro ejemplo es el de la categoría de transacción. Los clientes y los implementadores han usado la categoría de transacción en PSA para clasificar el trabajo y usar el campo para determinar el precio y el coste según la categoría de trabajo. Para obtener más información, consulte [Uso de la categoría de transacción como una dimensión de precios](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]