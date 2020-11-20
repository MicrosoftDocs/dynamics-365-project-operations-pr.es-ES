---
title: Configuración de tarifas de facturas de mano de obra
description: Este tema proporciona información sobre cómo configurar tarifas de facturación de la mano de obra en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e6294895857442f3a24a9d73ee07d2b90926a4fb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085210"
---
# <a name="setting-up-bill-rates-for-labor-rate-billing"></a>Configurar tarifas de facturación para la facturación de tarifas laborales 

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Cada lista de precios tiene un conjunto de precios o tarifas laborales que son efectivas para el contexto y fecha de vigencia incluida en el encabezado de la lista de precios. Las tarifas de facturación por tiempo en Dynamics 365 Project Operations se pueden configurar en una sola moneda, que es la moneda del encabezado de la lista de precios.

1. Para configurar tarifas de mano de obra para una lista de precios de venta, cree una lista de precios basada en el encabezado de la lista de precios. 
2. En la pestaña **Precios de rol** en la subcuadrícula seleccione **+ Nuevo precio de rol**. 
3. En el panel **Creación rápida** , introduzca la combinación de rol y unidad organizativa para la que necesita configurar la tarifa de facturación.

  La siguiente tabla incluye los campos en la pestaña **General** y el panel **Creación rápida** de una línea de precio de función que debe tener en cuenta al crear precios de función en una lista de precios de venta:

  | Campo | Ubicación | Relevancia, propósito y orientación | Impacto posterior |
  | --- | --- | --- | --- |
  | Rol | Pestaña **General** y panel **Creación rápida** | Seleccione el rol para el que está configurando la tarifa de facturación. | El rol en la estimación entrante o real se comparará con esta línea para predeterminar la tarifa de facturación del rol. |
  | Unidad de dotación de recursos | Pestaña **General** y panel **Creación rápida** | Seleccione la unidad organizativa o división de la empresa a la que pertenece este rol. Por ejemplo, un desarrollador de la división de robótica de Fabrikam India o un desarrollador de la división de software de Fabrikam USA. | La unidad de recursos en la estimación entrante o real se comparará con esta línea para predeterminar la tarifa de facturación del rol. |
  | Precio | Pestaña **General** y panel **Creación rápida** | Configure la tarifa de facturación para el rol de la empresa de recursos y combinación de unidad de recursos. Por ejemplo, un desarrollador de Fabrikam India tiene una tarifa de facturación de 100 USD o un desarrollador de Fabrikam USA tiene una tarifa de facturación de 150 USD. | Este precio es la tarifa de facturación predeterminada en el precio por unidad del estimado entrante o línea actual para la clase de transacción Hora. |
  | Divisa | Pestaña **General** y panel **Creación rápida**| De forma predeterminada, el valor de la moneda proviene del encabezado de la lista de precios de ventas. En una lista de precios de venta, la moneda no se puede anular. | Esta moneda es la moneda predeterminada en el precio por unidad de la línea actual de ventas entrante para la clase de transacción Hora. |
  | Programación de unidad | Pestaña **General** y panel **Creación rápida** | Esta programación unitaria tiene como valor predeterminado el Tiempo y no se puede cambiar en la entidad Precio de rol porque se utilizan tarifas rápidas por unidades de tiempo. | No hay impacto posterior para este campo. |
  | Unidad | Pestaña **General** y panel **Creación rápida** | El valor de unidad sale del campo **Unidad de tiempo** en el encabezado de la lista de precios de ventas. Pero el valor se puede sobrescribir. Por ejemplo, un desarrollador de Fabrikam India tiene una tarifa de facturación de 1000 USD por **Día de India**. Un desarrollador de Fabrikam USA tiene una tarifa de facturación de 1500 USD por **Día de EE. UU.**. | Cuando el precio por unidad usa el predeterminado en una estimación entrante o línea actual, el sistema usa el sistema de unidades y conversión en unidades base para calcular un precio por unidad. Por ejemplo, la estimación es de 10 **Días de la India** de trabajo para un desarrollador de la India, y la unidad Día de la india se define como 10 horas. Al fijar el precio de esa línea de estimación, la aplicación calcula el precio unitario en la estimación como 1000 USD / 10 horas = 100 USD por hora. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Transferir precios o configurar tarifas de facturación para recursos de otras unidades organizativas o divisiones 

En las empresas basadas en proyectos, es común utilizar empleados de diferentes divisiones de la compañía para trabajar en los proyectos. Los proyectos se pueden ejecutar desde una división mientras que los empleados o consultores provienen de la misma división diferente de la empresa. El proyecto también podría estar compuesto por una combinación de personas de diferentes divisiones. En Project Operations, la empresa propietaria de la entrega del proyecto se denomina **Unidad de contratación**. Todas las demás divisiones que proporcionan recursos se denominan **Unidades de recursos**. Debido a las diferencias en los costos laborales en varias geografías y mercados laborales en todo el mundo, las tarifas de facturación por mano de obra también se configuran de manera diferente para diferentes geografías.

Por ejemplo, un desarrollador de la división de Fabrikam India que trabaja en un proyecto de EE. UU. recibe una tarifa de 100 USD por hora. Un desarrollador de Fabrikam EE. UU. que trabaja en un proyecto de EE. UU. factura 150 USD por hora.

### <a name="example-set-up-a-bill-rate"></a>Ejemplo: configurar una tarifa de factura

1. Cree una lista de precios de venta llamada *Tarifas facturación de Fabrikam US* y establezca la fecha de vigencia.
2. En el la lista de precios de ventas introduzca la siguiente información de tarifa:

    | Rol | Unidad organizativa | Tasa de facturación |
    | --- | --- | --- |
    | Developer | Fabrikam India | 100 USD |
    | Developer | Fabrikam Filipinas | 90 $ |
    | Developer | Fabrikam US | 150 $ |

3. Adjunte la lista de precios de venta, **Tarifas de facturación de Fabrikam EE. UU.** a la lista de precios del proyecto del contrato del proyecto o a una cuenta determinada.