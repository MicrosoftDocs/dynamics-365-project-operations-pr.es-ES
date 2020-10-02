---
title: Información general de dimensiones de precios
description: En este tema se proporciona información sobre las dimensiones de precios en Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898237"
---
# <a name="pricing-dimensions-overview"></a>Información general de dimensiones de precios

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las dimensiones que se utilizan en los recursos humanos para establecer los precios y los costes se dividen en dos categorías:

- Personas
- Trabajo previsto

Debido a esto, hay dos tipos de valores de dimensión de precios disponibles:

- **Conjuntos de opciones**: dimensiones que son enumeraciones fijas para un conjunto de valores.
- **Valores basados en entidad**: dimensiones que son enumeraciones fijas para un conjunto de valores.

## <a name="pricing-dimensions"></a>Dimensiones de precios

Dynamics 365 Project Operations se envía con un conjunto predeterminado de dimensiones de precios. Puede ver estas dimensiones de precios yendo a **Project Operations** > **Parámetros**. En el registro de parámetros, en la pestaña **Dimensión de precios basados en importes**, verifique que el rol **msdyn_resourcecategory** y la unidad organizativa de recursos **msdyn_organizationalunit** tenga los campos **Aplicable a ventas** y **Aplicable a costes** establecido en **Sí**. Con estos cambios habilitados, puede configurar el precio y el coste de cada combinación de roles y unidades organizativas.

Si necesita fijar el precio o el coste de sus recursos mediante atributos adicionales, puede crear campos, entidades y dimensiones personalizados.

## <a name="pricing-human-resource-time"></a>Precios del tiempo de recursos humanos
La forma en que una organización establece el precio para el tiempo de los recursos humanos es a menudo una consideración estratégica importante que afecta directamente la rentabilidad de la organización. Trabaje con los equipos de finanzas y los directores de práctica cuando su organización esté lista para identificar cómo quiere establecer las tarifas y los costes del tiempo de recursos humanos.

Otras consideraciones para los precios incluyen si se deben reutilizar campos o entidades que actualmente no son dimensiones de precios, pero que se aplican como una dimensión de precios para su organización. Los campos como **Categoría de transacción** (**msdyn_transactioncategory**) y **Recurso que se puede reservar** (**bookableresource**) son ejemplos de dimensiones candidatas. 

Considere si su dimensión de precios debe ser una tabla o un conjunto de opciones. Si prevé cambios en los valores de una dimensión que supere 10 o 12 y necesita atributos adicionales en estos valores, puede crear una entidad en lugar de un conjunto de opciones. Mantener un conjunto de opciones, como agregar o eliminar valores, requiere un administrador o desarrollador, mientras que la mayoría de los usuarios pueden agregar nuevas filas a una tabla.

El siguiente ejemplo muestra las tasas de facturación que se configuran en función del rol y la unidad organizativa de recursos a la que pertenece el recurso. Las tasas de costes generalmente se basan en la banda salarial del empleado y la unidad organizativa a la que pertenecen. En este ejemplo, las tablas de tasa de facturación y tasa de coste tendrán el siguiente aspecto.

**Tasas de facturación de ejemplo**

| Rol        | Unidad organizativa    |Unidad      |Precio      |Divisa  |
| ------------|-------------|----------|----------:|----------|
| Desarrollador   | Contoso US  |Hour | 200|USD     |
| Desarrollador   | Contoso India |Hour|   112|USD     |


**Tasas de costes de ejemplo**

| Banda salarial     | Unidad organizativa    |Unidad      |Precio      |Divisa  |
| ----------------|-------------|----------|----------:|----------|
| Mi empresa_Banda1 | Contoso US  |Hour | 145|USD     |
| Mi empresa_Banda2 | Contoso India |Hour|   67|USD     |
