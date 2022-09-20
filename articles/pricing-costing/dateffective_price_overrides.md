---
title: Reemplazos de precios de la fecha de vigencia
description: Este artículo explica cómo configurar los reemplazos de precios para precios específicos en la lista de precios.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445979"
---
# <a name="date-effective-price-overrides"></a>Reemplazos de precios de la fecha de vigencia 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

*Reemplazos de precios de la fecha de vigencia* proporciona una forma de anular o cambiar precios específicos en la lista de precios. Por ejemplo, usted tiene una lista de precios estándar que está vigente desde el 1 de enero de 2022 hasta el 31 de diciembre de 2022. Esta lista de precios tiene precios para muchos roles. El precio que se establece para el rol de **Técnico de red** es de 100 dólares estadounidenses (USD) por hora. Cuando un técnico de la red registra tiempo entre el 1 de enero de 2022 y el 31 de diciembre de 2022, el tiempo tiene un precio de 100 USD. El 1 de octubre de 2022, deberá ajustar el precio *solo* para el rol **Técnico de red** de 100 USD por hora a 110 USD por hora. La función **Reemplazos de precios de la fecha de vigencia** le permite configurar este cambio como una anulación de la fila para ese precio de rol específico. Por lo tanto, no tiene que copiar toda la lista de precios y cambiar el precio de esa única fila.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Reemplazos de precios de la fecha de vigencia para los precios de la mano de obra

El proceso de configuración de reemplazos de precios de la fecha de vigencia para el tiempo de mano de obra en un proyecto consta de dos pasos básicos.

1. Habilite la función **Reemplazos de precios de la fecha de vigencia**.
1. Configure un reemplazo de precios de la fecha de vigencia.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Habilitar la función Reemplazos de precios de la fecha de vigencia

> [!NOTE]
> Una vez habilitada la función **Reemplazos de precios de la fecha de vigencia**, no se puede deshabilitar.

Para habilitar la función **Reemplazos de precios de la fecha de vigencia**, siga estos pasos.

1. Vaya a **Configuración** \> **Parámetros**.
1. Abra el registro **Parámetros**.
1. En el panel de acciones, en la pestaña **Control de características**, seleccione **Habilitar reemplazos de precios de la fecha de vigencia**.
1. En el cuadro de diálogo de confirmación, seleccione **Aceptar**.
1. Después de unos momentos, actualice su navegador. Ahora debería estar disponible la posibilidad de realizar reemplazos de precios de la fecha de vigencia. Sabrá que estas capacidades han sido habilitadas si **Habilitar reemplazos de precios de la fecha de vigencia** ya no aparece en el panel de acciones.

### <a name="set-up-a-date-effective-price-override"></a>Configurar un reemplazo de precios de la fecha de vigencia

Los reemplazos de precios de la fecha de vigencia se pueden configurar en las listas de precios de **Coste**, **Ventas** o **Compra**.

> [!NOTE]
>El comportamiento de **Reemplazos de precios de la fecha de vigencia** tiene actualmente las siguientes limitaciones:
>
> - Solo los precios de los roles y los recargos de los precios de los roles admiten la función de **Reemplazos de precios de la fecha de vigencia** en Project Operations.
> - Cuando copie una lista de precios mediante la acción **Copiar** de la página **Detalles de la lista de precios** y cuando cree una lista de precios del proyecto a partir de una lista de precios estándar o personalizada durante la creación del contrato, los reemplazos de precios de la fecha de vigencia **no** se copian de la lista de precios de origen.

Para configurar un reemplazo de precio con fecha de vigencia para un precio de rol o un incremento de precio de rol, siga estos pasos.

1. Abra la página de la lista de precios para la que desea configurar el reemplazo de precios de la fecha de vigencia.
1. Seleccione la pestaña **Precios de rol**. En esta pantalla se muestra una lista de todos los registros de **Precio de rol** en la lista de precios.
1. Seleccione el registro **Precio de rol** para el que desee establecer un nuevo reemplazo de precios con fecha de vigencia y, a continuación, pulse dos veces (o haga doble clic) en **Precio de rol** para abrir la página **Detalles de precio de rol**.
1. Seleccione la pestaña **Reemplazos de la fecha de vigencia**. La cuadrícula de esta pestaña muestra una lista de todas las anulaciones de precio con fecha de vigencia para el registro de **Precio de rol** seleccionado.
1. En la barra de herramientas encima de la cuadrícula, seleccione **Nuevo reemplazo del precio del rol**. Se abre el control deslizante **Nuevo reemplazo del precio del rol**.
1. Especifique la fecha de inicio de vigencia, la unidad y el nuevo precio para el reemplazo del precio. A continuación, seleccione **Guardar** y cierre el formulario.

> [!NOTE]
> - Un reemplazo de precios de la fecha de vigencia para un precio de rol o un recargo de precio de rol se aplica a la misma combinación de valores de dimensión de precios que existe en la fila **Precio de rol** o **Incremento del precio de rol** primaria.
> - La fecha que se selecciona en el campo **Efectivo desde** debe estar dentro de las fechas efectivas de la lista de precios primaria. El reemplazo del precio entrará en vigencia en la fecha que se seleccione en el campo **Efectivo desde** y se aplicará hasta el final de la fecha de finalización de la lista de precios primaria. Si configura otro reemplazo de precio con fecha de vigencia para el mismo precio de rol, el primer reemplazo de precio entrará en vigor en la fecha seleccionada en el campo **Efectivo desde** y se aplicará hasta el comienzo del segundo reemplazo.

## <a name="examples"></a>Ejemplos

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Ejemplo 1: Determinación de la vigencia de la fecha para un precio de rol que tiene reemplazos de precio de rol

El siguiente ejemplo muestra cómo se determina la vigencia de la fecha para un precio de rol específico para el que se configuran los reemplazos de precio de rol.

**Lista de precios A: del 1 de enero al 30 de junio**

*Precio de rol*

| Precio de rol | Unidad | Precio | Efecto sobre el precio para las transacciones entrantes |
|---|---|---|---|
| Técnico de red | Hora | 100 | Este precio se utilizará en todas las transacciones cuya fecha esté comprendida entre el 1 de enero y el 14 de marzo. |

*Reemplazo del precio del rol*

| Efectivo desde | Unidad | Precio | Efecto sobre el precio para las transacciones entrantes |
|---|---|---|---|
| Marzo de 15 | Hora | 110 | Este precio se utilizará en todas las transacciones cuya fecha esté comprendida entre el 15 de marzo y el 30 de marzo. |
| Abril de 1 | Hora | 120 | Este precio se utilizará en todas las transacciones cuya fecha esté comprendida entre el 1 de abril y el 30 de junio. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Ejemplo 2: Determinación de la vigencia de la fecha para un incremento de precio de rol que tiene reemplazos de incrementos de precio de rol

El siguiente ejemplo muestra cómo se determina la vigencia de la fecha para un incremento de precio de rol específico para el que se configuran los reemplazos de incremento de precio de rol.

**Lista de precios A: del 1 de enero al 30 de junio**

*Precio de rol*

| Precio de rol | Horas laborables | Unidad | Precio | Efecto sobre el precio para las transacciones entrantes |
|---|---|---|---|---|
| Técnico de red | La normal. | Hora | 100 | Este precio se utilizará en todas las transacciones cuya fecha esté comprendida entre el 1 de enero y el 14 de marzo. |

*Incremento del precio de rol*

| Unidad organizativa | Horas laborables | % de incremento |
|---|---|---|
| Contoso US | Horas extra | 10% |

*Reemplazo de incremento de precio de rol*

| Efectivo desde | Precio | Efecto sobre el precio para las transacciones entrantes |
|---|---|---|
| Marzo de 15 | 20% | Este porcentaje de incremento se utilizará en todas las transacciones cuya fecha esté comprendida entre el 15 de marzo y el 30 de marzo. |
| Abril de 1 | 25 % | Este incremento se utilizará en todas las transacciones cuya fecha esté comprendida entre el 1 de abril y el 30 de junio. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
