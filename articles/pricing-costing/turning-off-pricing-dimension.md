---
title: Desactivación de una dimensión de precios
description: En este tema se proporciona información sobre cómo desactivar dimensiones de precios.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650070"
---
# <a name="turning-off-a-pricing-dimension"></a>Desactivación de una dimensión de precios

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Es posible que deba revisar y actualizar su estrategia de precios cada pocos años. Cualquier actualización que realice puede precisar que tenga que desactivar una dimensión de precios existente y crear una nueva. Por ejemplo, es posible que antes haya fijado el precio por **Rol**, pero que ahora decida fijar el precio por **Experiencia laboral**. Esto puede requerir que desactive el **Rol** como dimensión de precios y cree **Experiencia laboral** como una nueva dimensión de precios. 

La desactivación de una dimensión de precios, sin importar si es de fábrica o personalizada, se puede hacer mediante el establecimiento de los campos **Aplicable a costes** y **Aplicable a ventas** de la dimensión de precios en **No**.

Sin embargo, al hacer esto, es posible que reciba el mensaje de error, **La dimensión de precios no se puede actualizar ni eliminar si hay registros de precios asociados.**

![Error de proceso de negocio probable al desactivar una dimensión de precios](media/Business-Process-Error.png)

Este mensaje de error indica que hay registros de precios que se configuraron previamente para la dimensión que se está desactivando. Todos los registros **Precio de rol** e **Incremento del precio de rol** que hacen referencia a una dimensión deben eliminarse antes de que la aplicabilidad de la dimensión pueda fijarse en **No**. Esta regla se aplica tanto a las dimensiones de precios listas para usar como a las dimensiones de precios personalizadas que pueda haber creado. La razón de esta validación se debe a que cada registro **Precio de rol** debe tener una combinación única de dimensiones. Por ejemplo, en una lista de precios llamada **Tasas de costes de Estados Unidos en 2018**, tendrá las siguientes filas **Precio de rol**. 

| Título estándar         | Unidad organizativa    |Unidad   |Precio  |Divisa  |
| -----------------------|-------------|-------|-------|----------|
| Ingeniero de sistemas|Contoso US|Hour| 100|USD|
| Ingeniero de sistemas sénior|Contoso US|Hour| 150| USD|


Cuando desactive **Título estándar** como la dimensión de precios, y el motor de precios busque un precio, solo utilizará el valor de **Unidad organizativa** del contexto de entrada. Si la **Unidad organizativa** del contexto de entrada es "Contoso Estados Unidos", el resultado será no determinista porque ambas filas coincidirán. Para evitar este escenario, cuando cree registros **Precio de rol**, el sistema validará que la combinación de dimensiones sea única. Si la dimensión se desactiva después de que se creen los registros de **Precio de rol**, esta restricción se podrá infringir. Por lo tanto, es necesario que antes de desactivar una dimensión, elimine todas las filas de **Precio de rol** y **Incremento del precio de rol** que tienen ese valor de dimensión completo.
