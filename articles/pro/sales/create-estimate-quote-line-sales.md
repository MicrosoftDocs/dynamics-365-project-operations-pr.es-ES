---
title: Estimación de una línea de oferta basada en proyecto
description: En este tema se proporciona información sobre cómo crear una estimación en una línea de oferta basada en proyecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085052"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimación de una línea de oferta basada en proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Una línea de oferta basada en proyecto tiene detalles que ayudan a estimar el coste y los ingresos potenciales del trabajo involucrado para entregar la línea de oferta.

Para estimar una línea de oferta basada en proyecto, en la línea de oferta basada en proyecto, seleccione la pestaña **Detalle de la línea de oferta**. Hay dos formas de crear una estimación en una línea de presupuesto basada en proyecto:

- Crear manualmente la estimación directamente en la línea de oferta utilizando los detalles de la línea de oferta 
- Cree un proyecto y un plan de proyecto, y luego asocie el proyecto y las tareas del proyecto a la línea de oferta. Se habilitará el proceso para importar las estimaciones del plan del proyecto a la línea de oferta en función de la información que haya proporcionado.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Crear estimaciones directamente en una línea de oferta basada en proyecto

Para crear una estimación en una línea de oferta basada en proyecto, seleccione la pestaña **Detalle de la línea de oferta**. El artículo de línea que cree en esta pestaña resumirá el valor ofertado para esta línea de oferta. 

Para crear detalles de línea de oferta, seleccione **+ Detalle de nueva línea de oferta** en la subcuadrícula **Detalles de la línea de oferta**. Se abrirá un control deslizante de creación rápida. Los siguientes campos del formulario **Línea de oferta** :

| **Campo** | **Ubicación** | **Relevancia, propósito y orientación** | **Impacto posterior** |
| --- | --- | --- | --- |
| Descripción | Creación rápida | Descripción de la estimación específica. | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Clase de transacción | Creación rápida | Esta lista desplegable proporciona las clases de transacciones que se incluyen en la pestaña **General** de la línea de oferta basada en proyecto.  | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Rol | Creación rápida | La persona que realizará este trabajo o incurrirá en este gasto. | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Categoría | Creación rápida | Categoría del trabajo o gasto. | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Fecha de inicio | Creación rápida | Fecha de inicio del trabajo. | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Fecha de finalización | Creación rápida | Fecha de finalización del trabajo. | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Unidad de dotación de recursos | Creación rápida | Unidad de recursos que incurrirá en este coste y proporcionará el recurso para trabajar en él. | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. Este campo también se utiliza en la recuperación de precios de coste. |
| Programación de unidad | Creación rápida | Unidad de venta del trabajo o gasto. Las unidades pertenecen a un programa de unidades o un grupo de unidades. Por ejemplo, millas y kilómetros son unidades que pertenecen a un grupo de unidades que describe la distancia. | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Unidad | Creación rápida | Unidad de trabajo o gasto. | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Cantidad | Creación rápida | Cantidad de trabajo o gasto | Este campo tiene como valor predeterminado el detalle de la línea de oferta relacionada para el coste que se crea automáticamente. |
| Precio unitario | Creación rápida | Tasa de facturación del rol que está realizando el trabajo o precio de venta de la categoría de gastos. Este campo tiene como valor predeterminado el tiempo en función de la combinación de rol y unidad de recursos en la lista de precios del proyecto vigente en la fecha de inicio. En el caso de los gastos, este campo tiene como valor predeterminado la configuración del precio para la categoría de transacción en la lista de precios del proyecto vigente en la fecha de inicio. Si el método de cálculo de precios para la categoría de transacción no es el precio unitario, no hay valor predeterminado y este campo se deja en blanco. | Tasa de coste del rol que está realizando el trabajo o el coste unitario de la categoría de gastos. Este campo tiene como valor predeterminado el tiempo en función de la combinación de rol y unidad de recursos en el precio de la unidad de contratación de la lista de precios de oferta vigente en la fecha de inicio. En el caso de los gastos, este campo tiene como valor predeterminado la configuración del precio para la categoría de transacción en la lista de precios de coste de la unidad de contratación vigente en la fecha de inicio. Si el método de cálculo de precios para la categoría de transacción no es el precio unitario, no hay valor predeterminado y este campo se deja en blanco. |
| Impuesto estimado | Creación rápida | Puede introducir manualmente el impuesto estimado para este trabajo o gasto. | No hay impacto posterior de este campo. |
| Importe | Creación rápida | Puede introducir información manualmente en este campo si los campos **Cantidad** y **Precio** se dejan en blanco. Si estos campos no están en blanco, este campo pasa a ser de solo lectura y se calcula como (Cantidad \* Precio unitario) + Impuesto. | No hay impacto posterior de este campo. |

## <a name="update-prices-on-quote-line-details"></a>Actualizar precios en los detalles de la línea de oferta

Si ha cambiado los precios en la lista de precios del proyecto que se adjunta a la oferta, o en la lista de precios de coste de la unidad contratante, puede seleccionar **Recalcular** en la página **Oferta** , para actualizar los precios en los detalles de la línea de oferta individual para reflejar este cambio. Cuando seleccione **Recalcular** , aparecerá una advertencia que le informa que se restablecerán los precios en los detalles de la línea de oferta para todas las líneas de oferta de esta oferta. Seleccione **Sí** , para actualizar los precios de las ventas y los detalles de la línea de oferta de costes.

## <a name="access-quote-line-details-for-cost"></a>Acceder a los detalles de la línea de oferta para conocer el coste

En la pestaña **Detalles de línea de oferta** , seleccione una fila de la cuadrícula para habilitar algunas acciones en la barra de herramientas de la subcuadrícula. La primera acción en la barra de herramientas de la subcuadrícula cuando se selecciona un detalle de línea de oferta es **Detalle de costes abiertos**. Seleccione **Detalle de costes abiertos** para ver la tasa de coste relacionada y el importe de esta línea de oferta.

> [!NOTE]
> El cambio de la unidad de recursos, la cantidad, las fechas, el rol o los valores de categoría en el detalle de la línea de oferta para el coste cambiará los valores correspondientes en los detalles de la línea de oferta para ventas.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Divisa en los detalles de la línea de oferta para costes y ventas

Moneda del detalle de la línea de oferta para los valores predeterminados de ventas de la lista de precios del proyecto vigente en la fecha de inicio del detalle de la línea de oferta.

Moneda del detalle de la línea de oferta para los valores predeterminados de costes de la lista de precios de la unidad de contratación de la oferta vigente en la fecha de inicio del detalle de la línea de oferta para el coste.

Los cálculos de rentabilidad convierten el importe en los detalles de línea de oferta para costes y ventas en la divisa base del entorno, para informar del margen estimado general en la oferta.

Esto podría producir errores de redondeo de moneda y márgenes cambiantes, debido a la falta de tipos de cambio vigentes en la fecha. Utilice estos cálculos en las ofertas de proyectos solo como aproximaciones y no como informes legales ni de otro tipo que requieran mayor precisión de redondeo y conocimiento de la fecha de vigencia de los tipos de cambio.
