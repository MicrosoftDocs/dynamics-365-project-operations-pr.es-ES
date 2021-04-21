---
title: Estimación de una línea de oferta basada en proyecto
description: En este tema se proporciona información sobre cómo crear una estimación en una línea de oferta basada en proyecto.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ef30df2921df7464aa2173161898121dc8e4f440
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858229"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimación de una línea de oferta basada en proyecto

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Una línea de oferta basada en proyecto tiene detalles que ayudan a estimar el coste y los ingresos potenciales del trabajo involucrado para entregar la línea de oferta.

Para estimar una línea de oferta basada en proyecto, en la línea de oferta basada en proyecto, seleccione la pestaña **Detalle de la línea de oferta**. Hay dos formas de crear una estimación en una línea de presupuesto basada en proyecto:

- Crear manualmente la estimación directamente en la línea de oferta utilizando los detalles de la línea de oferta. 
- Cree un proyecto y un plan de proyecto, y luego asocie el proyecto y las tareas del proyecto a la línea de oferta. Se habilitará el proceso para importar las estimaciones del plan del proyecto a la línea de oferta en función de la información que haya proporcionado.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Crear estimaciones directamente en una línea de oferta basada en proyecto

Para crear una estimación en una línea de oferta basada en proyecto, seleccione la pestaña **Detalle de la línea de oferta**. El artículo de línea que cree en esta pestaña resumirá el valor ofertado para esta línea de oferta. 

Para crear detalles de línea de cotización, seleccione **Detalle de nueva línea de cotización** sobre la subcuadrícula **Detalles de la línea de cotización**. Se abrirá un control deslizante de creación rápida. La siguiente tabla proporciona detalles sobre los campos de la página **Detalle de línea de cotización** página y cómo los valores afectan a la funcionalidad.

| **Campo** | **Ubicación** | **Descripción** | **Impacto posterior** |
| --- | --- | --- | --- |
| Descripción | Creación rápida | Descripción de la estimación específica. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Clase de transacción | Creación rápida | Esta lista desplegable proporciona las clases de transacciones que se incluyen en la pestaña **General** de la línea de cotización basada en el proyecto.  | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Seleccionar producto | Creación rápida | Se aplica cuando la clase de transacción es **Material**. Puede seleccionar especificar que esta línea de estimación sea para un producto **Existente** (catálogo) o un producto **Fuera de catálogo**. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Producto | Creación rápida | El identificador del producto del catálogo de productos. Este campo solo está habilitado cuando selecciona **Existente** en el campo **Seleccionar producto**. El identificador se utiliza para recuperar el precio de venta de la lista de precios del proyecto en la cotización. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Producto fuera de catálogo | Creación rápida | Un cuadro de texto para escribir el nombre del producto. Este campo solo está habilitado cuando selecciona **Fuera de catálogo** en el campo **Seleccionar producto**.| Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Rol | Creación rápida | El rol de la persona que realizará este trabajo o contraerá este gasto. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Categoría | Creación rápida | La categoría del trabajo o gasto. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Fecha de inicio | Creación rápida | La fecha de inicio del trabajo. | Este campo toma como valor predeterminado el detalle de la línea de cotización para el coste que se crea automáticamente. |
| Fecha de finalización | Creación rápida | La fecha de finalización del trabajo. | Este campo toma como valor predeterminado el detalle de la línea de cotización para el coste que se crea automáticamente. |
| Unidad de dotación de recursos | Creación rápida | La unidad de dotación de recursos que contraerá este coste y proporciona los recursos para trabajar en ellos. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente y se usa en la recuperación y se utiliza en la recuperación del precio de coste. |
| Programación de unidad | Creación rápida | El grupo unitario del trabajo, producto o gasto. Las unidades pertenecen a un programa de unidades o un grupo de unidades. Por ejemplo, millas y kilómetros son unidades que pertenecen a un grupo de unidades que describen la distancia. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Unidad | Creación rápida | La unidad de trabajo, producto o gasto. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Cantidad | Creación rápida | La cantidad de trabajo, producto o gasto. | Este valor toma como valor predeterminado el detalle de la línea de cotización relacionada para el coste que se crea automáticamente. |
| Precio unitario | Creación rápida |La tarifa de facturación del rol que está realizando el trabajo, el precio unitario del producto o el precio de venta del producto o la categoría de gastos. El valor predeterminado para este campo es **Hora** según la combinación de valores de dimensión de precios en la línea de precio del rol de la lista de precios del proyecto que está vigente para la fecha de inicio. Para **Gastos**, el valor predeterminado es la configuración de precio para la categoría de transacción en la lista de precios del proyecto que es efectiva para la fecha de inicio. Si el método de fijación de precios para la categoría de transacción no es el precio por unidad, no hay ningún valor predeterminado y este campo se deja en blanco. Para los productos, el valor predeterminado se basa en la línea **Elemento de lista de precios** en la lista de precios del proyecto que está vigente en la fecha de inicio.| La tarifa de coste del rol que está realizando el trabajo o el coste por unidad de la categoría e gastos o el coste unitario del producto. El valor predeterminado para este campo es **Hora** según la combinación de valores de dimensión de precios en la línea de precio del rol de la lista de precios del proyecto que está vigente para la fecha de inicio. Para **Gastos**, el valor predeterminado es la configuración de precio para la categoría de transacción en la lista de precios del proyecto que es efectiva para la fecha de inicio. Si el método de fijación de precios para la categoría de transacción no es el precio por unidad, no hay ningún valor predeterminado y este campo se deja en blanco. Para los productos, el valor predeterminado se basa en la línea **Elemento de lista de precios** en la lista de precios del proyecto que está vigente en la fecha de inicio.|
| Impuesto estimado | Creación rápida | Puede introducir manualmente el impuesto estimado para este trabajo o gasto. | No hay impacto posterior para este campo. |
| Importe | Creación rápida | Puede introducir información manualmente en este campo si los campos **Cantidad** y **Precio** se dejan en blanco. Si estos campos no están en blanco, este campo pasa a ser de solo lectura y se calcula como (Cantidad \* Precio unitario) + Impuesto. | No hay impacto posterior para este campo. |


## <a name="update-prices-on-quote-line-details"></a>Actualizar precios en los detalles de la línea de oferta

Si ha cambiado los precios en la lista de precios del proyecto que está asociada a la cotización, o en la lista de precios de coste de la unidad de contratación, puede seleccionar **Recalcular** en la página **Cita** para actualizar los precios en los detalles de la línea de cotización individual para reflejar este cambio. Cuando seleccione **Recalcular**, aparece una advertencia que le informa de que los precios en los detalles de la línea de cotización para todas las líneas de cotización en esta cotización se restablecerán. Seleccione **Sí** para actualizar los precios de las ventas y los detalles de la línea de oferta de costes.

## <a name="access-quote-line-details-for-cost"></a>Acceder a los detalles de la línea de oferta para conocer el coste

Sobre la pestaña **Detalles de la línea de oferta**, seleccione una fila en la cuadrícula para habilitar algunas acciones en la barra de herramientas de la subcuadrícula. La primera acción en la barra de herramientas de la subcuadrícula cuando se selecciona un detalle de línea de cotización es **Detalle de costos abiertos**. Seleccione **Detalle de costes abiertos** para ver la tasa de coste relacionada y el importe de esta línea de oferta.

> [!NOTE]
> El cambio de la unidad de recursos, la cantidad, las fechas, el rol o los valores de categoría en el detalle de la línea de oferta para el coste cambiará los valores correspondientes en los detalles de la línea de oferta para ventas.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Divisa en los detalles de la línea de oferta para costes y ventas

Moneda del detalle de la línea de oferta para los valores predeterminados de ventas de la lista de precios del proyecto vigente en la fecha de inicio del detalle de la línea de oferta.

Moneda del detalle de la línea de oferta para los valores predeterminados de costes de la lista de precios de la unidad de contratación de la oferta vigente en la fecha de inicio del detalle de la línea de oferta para el coste.

Los cálculos de rentabilidad convierten el importe en los detalles de línea de oferta para costes y ventas en la divisa base del entorno, para informar del margen estimado general en la oferta.

> [!NOTA
> > Pueden producirse errores de redondeo de divisas y márgenes modificados debido a la falta de tipos de cambio vigentes en la fecha. Utilice estos cálculos solo en contratos de proyectos, ya que son aproximaciones y no para informes legales reales o de otro tipo que requieran una mayor precisión de redondeo y conocimiento de la fecha de vigencia para los tipos de cambio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
