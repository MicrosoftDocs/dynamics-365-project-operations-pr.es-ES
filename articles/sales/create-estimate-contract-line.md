---
title: Calcular una línea de contrato basada en proyecto
description: En este tema se proporciona información sobre las estimaciones de una línea de contrato basada en proyecto.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cdc8984e080d995e3a0b667fe662291b499235b2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278529"
---
# <a name="estimate-a-projectbased-contract-line"></a>Calcular una línea de contrato basada en proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_ 

En Dynamics 365 Project Operations, una línea de contrato basada en proyecto tiene detalles que ayudan a estimar el costo y los ingresos potenciales del trabajo involucrado para entregar la línea de contrato.

Para estimar una línea de contrato basada en proyecto, vaya a la pestaña **Detalle de la línea de contrato** en la **Línea de contrato** basada en proyecto.  Hay dos formas de crear un presupuesto en una línea de contrato basada en proyecto:

   - Cree un presupuesto directamente en la línea del contrato agregando manualmente los detalles de la línea del contrato.
   - Cree un proyecto y un plan de proyecto, y luego asocie el proyecto y las tareas a la línea de contrato del proyecto. Esto habilita el proceso mediante el cual puede importar el presupuesto del plan del proyecto en la línea de contrato en función de los componentes incluidos en la línea de contrato.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Crear una estimación directamente en una línea de contrato basada en proyecto

1. Vaya a la línea de contrato y seleccione la pestaña **Detalle de la línea de contrato**. Las líneas que crea en esta pestaña se resumen y se muestran como **Valor contratado** para esta **Línea de contrato**. 
2. En la subcuadrícula **Detalles de la línea de contrato**, seleccione **+ Detalle de nueva línea de contrato**. Se abre un control deslizante de creación rápida. Los siguientes campos están disponibles en el formulario **Detalles de la línea de contrato**:

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| **Descripción** | **Creación rápida** | Descripción de la estimación específica. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. |
| **Clase de transacción** | **Creación rápida** | Este menú desplegable es una lista de clases de transacciones incluidas en la pestaña **General** de la línea de contrato basado en proyecto. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. |
| **Rol** | **Creación rápida** | El papel de la persona que está realizando este trabajo o incurriendo en este gasto. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. |
| **Categoría** | **Creación rápida** | La categoría del trabajo o gasto. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. |
| **Fecha de inicio** | **Creación rápida** | La fecha de inicio del trabajo. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. |
| **Fecha de finalización** | **Creación rápida** | La fecha de finalización del trabajo. | Este campo tiene como valor predeterminado el detalle del coste que se crea automáticamente. |
| **Empresa de dotación de recursos** | **Creación rápida** | La empresa proveedora de recursos o la entidad legal que está incurriendo en este costo y proporciona el recurso para trabajar en él. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. Este campo también se utiliza en la recuperación de precios de coste. |
| **Unidad de dotación de recursos** | **Creación rápida** | La unidad de recursos que incurre en este costo y proporciona el recurso para trabajar en él. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. Este campo también se utiliza en la recuperación de precios de coste. |
| **Programación de unidad** | **Creación rápida** | El grupo unitario de la obra o gasto. Las unidades pertenecen a un programa de unidades o un grupo de unidades. Por ejemplo, *millas* y *kilómetros (Km)* son unidades que pertenecen a un grupo de unidades que describen la distancia. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. |
| **Unidad** | **Creación rápida** | La unidad de trabajo o el gasto. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. |
| **Cantidad** | **Creación rápida** | La cantidad de trabajo o el gasto. | Este campo tiene como valor predeterminado el detalle de la línea de contrato relacionada para los costos que se crean automáticamente. |
| **Precio unitario** | **Creación rápida** | La tarifa de facturación del rol que está realizando el trabajo o el precio de venta de la categoría de gastos. Este campo tiene como valor predeterminado el **Tiempo** en función de la combinación de rol y unidad de recursos en la lista de precios del proyecto vigente en la fecha de inicio. Para los gastos, el valor predeterminado de este campo es de la configuración de precio para la categoría de transacción en la lista de precios del proyecto que es efectiva para la fecha de inicio. Si el método de cálculo de precios para la categoría de transacción no es el **precio unitario**, no hay valor predeterminado y este campo se deja en blanco. | La tarifa de coste del rol que está realizando el trabajo o el coste unitario de la categoría de gastos. Este campo está predeterminado para **Tiempo basado en el rol** y la combinación de la unidad de recursos en la línea de precio de función de la lista de precios de costo adjunta a la unidad de contratación vigente para la fecha de inicio. Para los gastos, el valor predeterminado de este campo se basa en la línea de precio de la categoría de la lista de precios de coste asociada a la unidad de contrato que es efectiva para la fecha de inicio. Si el método de cálculo de precios para la categoría de transacción no es el precio unitario, no hay valor predeterminado y este campo se deja en blanco. |
| **Impuesto estimado** | **Creación rápida** | El impuesto estimado por este trabajo o gasto según lo ingresado por el usuario. | El impuesto estimado por este trabajo o gasto según lo ingresado por el usuario. |
| **Importe** | **Creación rápida** | El usuario puede agregar este valor en este campo si los campos **Cantidad** y **Precio** se dejan en blanco. Si se rellenan **Cantidad** y **Precio**, el campo **Cantidad** es de solo lectura y se calcula como **(Cantidad \* Precio unitario) + IVA**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Actualizar precios en los detalles de la línea del contrato

Si cambia los precios en la lista de precios del proyecto que se adjunta al contrato o la lista de precios de costo de la unidad contratante, puede actualizar los precios en los detalles de la línea de contrato individual para reflejar el cambio. Sobre la página **Contrato**, seleccione **Recalcular**. Se abre una advertencia para informarle que se restablecen los precios de todas las líneas de contrato de este contrato. Seleccione **Sí** para actualizar los precios de los detalles de la línea de contrato de costos y ventas.

## <a name="access-contract-line-details-for-cost"></a>Acceda a los detalles de la línea del contrato para conocer el costo

Sobre la pestaña **Detalles de la línea de contrato**, seleccione una fila en la cuadrícula para mostrar acciones en la barra de herramientas de la subcuadrícula. La primera acción en la barra de herramientas de la subcuadrícula es **Detalle de costos abiertos**. Para ver la tasa de costo relacionada y el monto de este detalle de línea de contrato, seleccione **Detalle de costos abiertos**. 

> [!NOTE]
> Cambiar la empresa de recursos, la unidad de recursos, la cantidad, las fechas, el rol o los valores de categoría en el detalle de la línea de contrato para **Costo** también cambia los valores correspondientes en el detalle de la línea de contrato para **Ventas**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moneda en los detalles de la línea del contrato para costos y ventas

El detalle de la línea de contrato para **Ventas** establece la moneda predeterminada de la lista de precios del proyecto que es efectiva para la fecha de inicio del detalle de la línea del contrato.

El detalle de la línea de contrato para **Coste** establece la moneda predeterminada de la lista de precios de la unidad de contrato que es efectiva para la fecha de inicio del detalle de la línea del contrato para **Coste**.

Los cálculos de rentabilidad convierten los importes de los detalles de la línea de contrato para **Costo** y **Ventas** en la moneda base del medio ambiente para informar los márgenes totales reales y estimados del contrato.

> [!NOTE]
> Pueden producirse errores de redondeo de divisas y márgenes modificados debido a la falta de tipos de cambio vigentes en la fecha. Utilice estos cálculos en los contratos de proyectos solo como aproximaciones y no para informes legales reales o de otro tipo que requieran una mayor precisión de redondeo y conocimiento de la vigencia de la fecha para los tipos de cambio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]