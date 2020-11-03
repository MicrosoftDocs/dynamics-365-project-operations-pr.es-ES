---
title: Desactivación de una dimensión de precios
description: En este tema se muestra cómo configurar dimensiones de precios en la solución de Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085233"
---
# <a name="turn-off-a-pricing-dimension"></a>Desactivación de una dimensión de precios

Es posible que deba revisar y actualizar su estrategia de precios cada pocos años. Cualquier actualización que realice puede precisar que tenga que desactivar una dimensión de precios existente y crear una nueva. Por ejemplo, es posible que antes haya fijado el precio por **Rol** , pero que ahora decida fijar el precio por **Experiencia laboral**. Esto puede requerir que desactive el **Rol** como dimensión de precios y cree **Experiencia laboral** como una nueva dimensión de precios. 

La desactivación de una dimensión de precios, sin importar si es de fábrica o personalizada, se puede hacer mediante el establecimiento de los campos **Aplicable a costes** y **Aplicable a ventas** de la dimensión de precios en **No**.

Sin embargo, cuando realice este procedimiento, es posible que reciba el siguiente mensaje de error.

![Error de proceso de negocio probable al desactivar una dimensión de precios](media/Business-Process-Error.png)


Este mensaje de error indica que hay registros de precios que se configuraron previamente para la dimensión que se está desactivando. Todos los registros **Precio de rol** e **Incremento del precio de rol** que hacen referencia a una dimensión deben eliminarse antes de que la aplicabilidad de la dimensión pueda fijarse en **No**. Esta regla se aplica tanto a las dimensiones de precios listas para usar como a las dimensiones de precios personalizadas que pueda haber creado. La razón de esta validación se debe a que Project Service tiene la restricción de que cada registro **Precio de rol** debe tener una combinación única de dimensiones. Por ejemplo, en una lista de precios llamada **Tasas de costes de Estados Unidos en 2018** , tendrá las siguientes filas **Precio de rol**. 

| Título estándar         | Unidad organizativa    |Unidad   |Precio  |Divisa  |
| -----------------------|-------------|-------|-------|----------|
| Ingeniero de sistemas|Contoso US|Hour| 100|USD|
| Ingeniero de sistemas sénior|Contoso US|Hour| 150| USD|


Cuando desactive **Título estándar** como la dimensión de precios, y el motor de precios de Project Service busque un precio, solo utilizará el valor de **Unidad organizativa** del contexto de entrada. Si la **Unidad organizativa** del contexto de entrada es "Contoso Estados Unidos", el resultado será no determinista porque ambas filas coincidirán. Para evitar este escenario, cuando cree registros **Precio de rol** , Project Service validará que la combinación de dimensiones sea única. Si la dimensión se desactiva después de que se creen los registros de **Precio de rol** , esta restricción se podrá infringir. Por lo tanto, es necesario que antes de desactivar una dimensión, elimine todas las filas de **Precio de rol** y **Incremento del precio de rol** que tienen ese valor de dimensión completo.

