---
title: Estimar una línea de contrato de proyecto
description: Este tema proporciona información sobre estimaciones en una línea de contrato de proyecto.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3aa46b017fa27572de807d5cf15ea93158177609
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007207"
---
# <a name="estimate-a-project-contract-line"></a>Estimar una línea de contrato de proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_ 

En Dynamics 365 Project Operations, una línea de contrato basada en proyecto tiene detalles que ayudan a estimar el costo y los ingresos potenciales del trabajo involucrado para entregar la línea de contrato.

Para estimar una línea de contrato basada en proyecto, vaya a la pestaña **Detalle de la línea de contrato** en la **Línea de contrato** basada en proyecto.  Hay dos formas de crear un presupuesto en una línea de contrato basada en proyecto:

   - Cree un presupuesto directamente en la línea del contrato agregando manualmente los detalles de la línea del contrato.
   - Cree un proyecto y un plan de proyecto, y luego asocie el proyecto y las tareas a la línea de contrato del proyecto. Esto habilita el proceso mediante el cual puede importar el presupuesto del plan del proyecto en la línea de contrato en función de los componentes incluidos en la línea de contrato.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Crear una estimación directamente en una línea de contrato de un proyecto

Para crear una estimación directamente en una línea de contrato de un proyecto, siga estos pasos:

1. Vaya a la línea de contrato y seleccione la pestaña **Detalle de la línea de contrato**. Las líneas que crea en esta pestaña se resumen y se muestran como **Valor contratado** para esta **Línea de contrato**. 
2. En la subcuadrícula **Detalles de la línea de contrato**, seleccione **Detalle de nueva línea de contrato**. Se abre un control deslizante de creación rápida. Los siguientes campos están disponibles en la página **Detalles de línea de contrato**.

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| **Descripción** | **Creación rápida** | Descripción de la estimación específica. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Clase de transacción** | **Creación rápida** | Esta lista de clases de transacciones se incluye en la pestaña **General** de la línea de contrato basada en proyecto. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Seleccionar producto** | **Creación rápida** | Se aplica cuando la clase de transacción es **Material**. Puede seleccionar especificar que esta línea de estimación sea para un producto **Existente** (catálogo) o un producto **Fuera de catálogo**. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Producto** | **Creación rápida** | El identificador del producto del catálogo de productos. Este campo solo está habilitado cuando selecciona **Producto existente** en el campo **Seleccionar producto**. El identificador se utiliza para recuperar el precio de venta de la lista de precios del proyecto en el contrato. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Producto fuera de catálogo** | **Creación rápida** | Un campo de texto para especificar el nombre del producto. Este campo solo está habilitado cuando selecciona **Fuera de catálogo** en el campo **Seleccionar producto**.| Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Rol** | **Creación rápida** | El papel de la persona que está realizando este trabajo o incurriendo en este gasto. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente.|
| **Categoría** | **Creación rápida** | La categoría del trabajo o gasto. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente.|
| **Fecha de inicio** | **Creación rápida** | La fecha de inicio del trabajo. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Fecha de finalización** | **Creación rápida** | La fecha de finalización del trabajo. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Empresa de dotación de recursos** | **Creación rápida** | La empresa de dotación de recursos o entidad legal que contrae en este coste y proporciona los recursos para trabajar en ellos. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente y se usa en la recuperación y se utiliza en la recuperación del precio de coste. |
| **Unidad de dotación de recursos** | **Creación rápida** | La unidad de dotación de recursos que contrae en este coste y proporciona los recursos para trabajar en ellos. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente y se usa en la recuperación y se utiliza en la recuperación del precio de coste. |
| **Programación de unidad** | **Creación rápida** | El grupo unitario del trabajo, producto o gasto. Las unidades pertenecen a un programa de unidades o un grupo de unidades. Por ejemplo, *millas* y *kilómetros (km)* son unidades que pertenecen a un grupo de unidades que describen la distancia. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Unidad** | **Creación rápida** | La unidad de trabajo, producto o gasto. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Cantidad** | **Creación rápida** | La cantidad de trabajo, producto o gasto. | Este valor toma como valor predeterminado el detalle de la línea de contrato relacionada para el coste que se crea automáticamente. |
| **Precio unitario** | **Creación rápida** | La tarifa de facturación del rol que está realizando el trabajo, el precio unitario del producto o el precio de venta del producto o la categoría de gastos. El valor predeterminado para **Hora** se basa en la combinación de valores de dimensión de precios en la línea de precio del rol de la lista de precios del proyecto que está vigente para la fecha de inicio. Para **Gastos**, el valor predeterminado para este campo es de la configuración de precio para la categoría de transacción en la lista de precios del proyecto que está vigente en la fecha de inicio. Si el método de cálculo de precios para la categoría de transacción no es el **precio unitario**, no hay valor predeterminado y este campo se deja en blanco. Para los productos, el valor predeterminado de este campo se basa en la línea **Elemento de lista de precios** en la lista de precios del proyecto que está vigente en la fecha de inicio.| La tarifa de coste del rol que está realizando el trabajo o el coste por unidad de la categoría e gastos o el coste unitario del producto. El valor predeterminado para **Hora** se basa en la combinación de valores de dimensión de precios en la línea de precio del rol de la lista de precios de coste asociada a la unidad contractual que está vigente para la fecha de inicio. Para **Gastos**, el valor predeterminado para este campo se basa en la línea de precio de categoría de la lista de precios de coste vinculada a la unidad contractual que está vigente en la fecha de inicio. Si el método de cálculo de precios para la categoría de transacción no es el precio unitario, no hay valor predeterminado y este campo se deja en blanco. Para los productos, el valor predeterminado para este campo se basa en la línea **Elemento de lista de precios** de la lista de precios de coste vinculada a la unidad contractual que está vigente en la fecha de inicio.|
| **Impuesto estimado** | **Creación rápida** | El impuesto estimado por este trabajo o gasto según lo ingresado por el usuario. | &nbsp; |
| **Importe** | **Creación rápida** | El valor de este campo se puede agregar si los campos **Cantidad** y **Precio** se dejan en blanco. Si los campos **Cantidad** y **Precio** están rellenados, el campo **Importe** es de solo lectura y se calcula como **(Cantidad \* Precio unitario) + Impuestos**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Actualizar precios en los detalles de la línea del contrato

Si cambia los precios en la lista de precios del proyecto que se adjunta al contrato o la lista de precios de costo de la unidad contratante, puede actualizar los precios en los detalles de la línea de contrato individual para reflejar el cambio. Sobre la página **Contrato**, seleccione **Recalcular**. Aparece una advertencia para informarle que se restablecen los precios de todas las líneas de contrato de este contrato. Seleccione **Sí** para actualizar los precios de los detalles de la línea de contrato de costos y ventas.

## <a name="access-contract-line-details-for-cost"></a>Acceda a los detalles de la línea del contrato para conocer el costo

Sobre la pestaña **Detalles de la línea de contrato**, seleccione una fila en la cuadrícula para mostrar acciones en la barra de herramientas de la subcuadrícula. La primera acción en la barra de herramientas de la subcuadrícula es **Detalle de costos abiertos**. Para ver la tasa de costo relacionada y el monto de este detalle de línea de contrato, seleccione **Detalle de costos abiertos**. 

> [!NOTE]
> Cambiar la empresa de recursos, la unidad de recursos, la cantidad, las fechas, el rol o los valores de categoría en el detalle de la línea de contrato para **Costo** también cambia los valores correspondientes en el detalle de la línea de contrato para **Ventas**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moneda en los detalles de la línea del contrato para costos y ventas

El detalle de la línea de contrato para **Ventas** establece la moneda predeterminada de la lista de precios del proyecto que es efectiva para la fecha de inicio del detalle de la línea del contrato.

El detalle de la línea de contrato para **Coste** establece la moneda predeterminada de la lista de precios de la unidad de contrato que es efectiva para la fecha de inicio del detalle de la línea del contrato para **Coste**.

Los cálculos de rentabilidad convierten los importes de los detalles de la línea de contrato para **Costo** y **Ventas** en la moneda base del medio ambiente para informar los márgenes totales reales y estimados del contrato.

> [!NOTE]
> Pueden producirse errores de redondeo de divisas y márgenes modificados debido a la falta de tipos de cambio vigentes en la fecha. Utilice estos cálculos solo en contratos de proyectos, ya que son aproximaciones y no para informes legales reales o de otro tipo que requieran una mayor precisión de redondeo y conocimiento de la fecha de vigencia para los tipos de cambio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
