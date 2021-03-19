---
title: Configurar campos personalizados como dimensiones de precios
description: En este tema se proporciona información sobre cómo configurar dimensiones de precios usando campos personalizados.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1468c3396a01c1bee1bc0f47eac1ee8b44eaa459
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274884"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Configurar campos personalizados como dimensiones de precios

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Antes de comenzar, este tema supone que ha completado los procedimientos en los temas: [Creación de campos y entidades](create-custom-fields-entities-pricing-dimensions.md) y [Agregar campos personalizados requeridos a la configuración de precios y entidades transaccionales](add-custom-fields-price-setup-transactional-entities.md). Si no ha completado esos procedimientos, vuelva y complételos y, a continuación, regrese a este tema. 

En este tema se proporciona información sobre cómo configurar dimensiones de precios personalizadas. En la página **Parámetros**, en la pestaña **Dimensiones de precios basadas en el importe**, la pestaña muestra los registros en las entidades de dimensiones de precios. De forma predeterminada, hay dos filas en la cuadrícula de esta pestaña:

- **msdyn_resourcecategory** (Rol)
- **msdyn_OrganizationalUnit** (Unidad organizativa)

> [!IMPORTANT]
> No elimine estas filas. Sin embargo, si no las necesita, puede hacer que no sean aplicables en un contexto específico mediante el establecimiento de **Aplicable a costes**, **Aplicable a ventas** y **Aplicable a compras** en **No**. Establecer estos valores de atributo en **No** tiene el mismo efecto que no tener el campo como una dimensión de precios.

Para que un campo se convierta en una dimensión de precios, debe:

- Crearse como campo en las entidades **Precio de rol** y **Incrementos del precio de rol**. Para obtener más información sobre cómo hacer esto, consulte. [Adición de campos personalizados a la configuración de precios y entidades transaccionales](add-custom-fields-price-setup-transactional-entities.md).

- Crearse como una fila en la tabla **Dimensión de precios**. Por ejemplo, agregue filas de dimensión de precios como se muestra en el siguiente gráfico. 

![Importe: basado en las filas de dimensión de precios](media/Amt-based-PD.png)

Horas de trabajo del recurso (**msdyn_resourceworkhours**) se agrega como dimensión basada en el incremento y que se ha agregado a la cuadrícula en la pestaña **Dimensión de precios basada en el incremento**.

![Incremento: basado en las filas de dimensión de precios](media/Markup-based-PD.png)


> [!IMPORTANT]
> Cualquier cambio en los datos de dimensión de precios en esta tabla, existente o nuevo, se propaga a la lógica comercial de precios solo después de que se actualice la memoria caché. El tiempo de actualización de la memoria caché puede ser de hasta 10 minutos. Deje que transcurra ese período para ver los cambios en la lógica de incumplimiento de precios que deben generarse a partir de los cambios en los datos de dimensión de precios.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributos de la tabla Dimensiones de precios
Las siguientes secciones proporcionan información sobre los diferentes atributos en la tabla **Dimensiones de precios**.

### <a name="pricing-dimension-name"></a>Nombre de dimensión de precios
Este valor debe ser exactamente el mismo que el nombre del esquema del campo que se agrega a la tabla **Precio de rol** para dimensiones de precios personalizadas. Para obtener más información sobre cómo agregar campos a la tabla **Precio de rol**, consulte [Adición de campos personalizados a la configuración de precios y entidades transaccionales](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Tipo de dimensión
Existen dos tipos de dimensiones de precios:
  
  - **Dimensiones de precios basadas en el importe**: los valores de dimensión del contexto de entrada coinciden con los valores de dimensión en la línea **Precio de rol** y el precio/coste se predetermina directamente a partir de la tabla **Precio de rol**.
  - **Dimensiones de precios basadas en el incremento**: estas son dimensiones donde se utiliza el proceso de tres pasos para obtener el precio/coste:
 
    1. Los valores de dimensión no basados en incrementos del contexto de entrada coinciden con la línea Precio de rol para obtener la tasa base.
    2. Los valores de dimensión del contexto de entrada coinciden con la línea **Incremento de precio de rol** para obtener un porcentaje de incremento.
    3. El porcentaje de incremento del segundo paso se aplica a la tasa base obtenida de la tabla **Precio de rol** en el primer paso para llegar al precio/coste final.
   
   La siguiente tabla muestra el cálculo de los incrementos de precio.
  
| Rol        | Unidad organizativa    |Ubicación de trabajo      |Título estándar      |Horas de trabajo del recurso      |  Marcar|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|In situ            |                    |Horas extra                 |15     |
|             | Contoso India|Local             |                    |Horas extra                 |10     |
|             | Contoso US   |Local             |                    |Horas extra                 |20     |


Si un recurso de Contoso India cuya tasa base es de 100 USD está funcionando in situ, y registran 8 horas de tiempo regular y 2 horas extra en la entrada de tiempo, el motor de precios usará la tasa base de 100 para las 8 horas para registrar 800 USD. Para las 2 horas extra, se aplicará un incremento del 15 % a la tasa base de 100 para obtener un precio unitario de 115 USD y se registrará un coste total de 230 USD.

### <a name="applicable-to-cost"></a>Aplicable a costes 
Si se establece en **Sí**, indica que el valor de dimensión del contexto de entrada se debe utilizar para que coincida con **Precio de rol** e **Incremento del precio de rol** al recuperar las tasas de coste e incremento.

### <a name="applicable-to-sales"></a>Aplicable a ventas
Si se establece en **Sí**, indica que el valor de dimensión del contexto de entrada se debe utilizar para que coincida con **Precio de rol** e **Incremento del precio de rol** al recuperar las tasas de facturación e incremento.

### <a name="applicable-to-purchase"></a>Aplicable a compras
Si se establece en **Sí**, indica que el valor de dimensión del contexto de entrada se debe utilizar para que coincida con **Precio de rol** e **Incremento del precio de rol** al recuperar el precio de compra. Los escenarios de subcontratación no son compatibles, por lo que este campo no se utiliza. 

### <a name="priority"></a>Prioridad
Establecer la prioridad de dimensión ayuda a la fijación de precios incluso cuando no puede encontrar una coincidencia exacta entre los valores de la dimensión de entrada y los valores de las tablas **Precio de rol** o **Incremento del precio de rol**. En este escenario, se utilizan valores nulos para los valores de dimensión no coincidentes mediante la compensación de las dimensiones en orden de prioridad.

- **Prioridad de costes**: el valor de la prioridad de coste de una dimensión indicará el peso de esa dimensión cuando se compara con la configuración de precios de coste. El valor de **Prioridad de coste** debe ser único en todas las dimensiones con **Aplicable a costes**.
- **Prioridad de ventas**: el valor de la prioridad de ventas de la dimensión indicará el peso de esa dimensión cuando se compara con la configuración de precios de venta o tasas de facturación. El valor de **Prioridad de ventas** debe ser único en todas las dimensiones con **Aplicable a ventas**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]