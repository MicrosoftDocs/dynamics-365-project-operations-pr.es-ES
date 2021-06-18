---
title: Datos reales
description: Este tema proporciona información sobre cómo trabajar con datos reales en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996632"
---
# <a name="actuals"></a>Datos reales 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los datos reales representan el progreso financiero y de la programación revisado y aprobado en un proyecto. Se crean como resultado de la aprobación del plazo, gastos, movimientos de uso de material y movimientos de diario y facturas.

## <a name="journal-lines-and-time-submission"></a>Envío de líneas de diario y tiempo

Para obtener más información sobre movimientos de tiempo, consulte [Resumen de movimientos de tiempo](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tiempo y materiales

Cuando una entrada de tiempo que se envía está vinculada a un proyecto asignado a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.

### <a name="fixed-price"></a>Precio fijo

Cuando se envía una entrada de tiempo vinculada a un proyecto que está asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.

### <a name="default-pricing"></a>Precios predeterminados

La lógica para crear precios predeterminados se encuentra en la línea del diario. Los valores de campo de la entrada de tiempo se copian a la línea del diario. Estos valores incluyen la fecha de la transacción, la línea de contrato a la que está asignado el proyecto y el resultado de la divisa en la lista de precios correspondiente.

Los campos que afectan a los precios predeterminados, como, por ejemplo, **Rol** y **Unidad de dotación de recursos**, se utilizan para determinar el precio adecuado en la línea de diario. Puede agregar un campo personalizado en la entrada de tiempo. Si desea que el valor del campo se propague a los valores reales, cree el campo en las tablas **Datos reales** y **Línea de diario**. Utilice código personalizado para propagar el valor del campo seleccionado desde Entrada de tiempo a Datos reales a través de la línea del diario utilizando los orígenes de la transacción. Para obtener más información sobre los orígenes de las transacciones y las conexiones, consulte [Vinculación de datos reales a los registros originales](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Envío de líneas de diario y gastos básicos

Para obtener más información sobre movimientos de gastos, consulte [Resumen de gastos](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tiempo y materiales

Cuando una entrada de gasto básico enviada está vinculada a un proyecto asignado a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.

### <a name="fixed-price"></a>Precio fijo

Cuando una entrada de gastos básicos enviada se vincula a un proyecto que está asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.

### <a name="default-pricing"></a>Precios predeterminados

La lógica para introducir precios predeterminados para gastos se basa en la categoría de gastos. La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada. Los campos que afectan a los precios predeterminados, como, por ejemplo, **Categoría de transacción** y **Unidad**, se utilizan para determinar el precio adecuado en la línea de diario. Sin embargo, esto solo funciona cuando el método de fijación de precios en la lista de precios es **Precio por unidad**. Si el método de fijación de precios es **De coste** o **Incremento por encima del coste**, el precio indicado cuando se crea la entrada de gastos se usa para el coste y el precio en la línea del diario de ventas se calcula según el método de fijación de precios. 

Puede agregar un campo personalizado en la entrada de gastos. Si desea que el valor del campo se propague a los valores reales, cree el campo en las tablas **Datos reales** y **Línea de diario**. Utilice código personalizado para propagar el valor del campo seleccionado desde Entrada de tiempo a Datos reales a través de la línea del diario utilizando los orígenes de la transacción. Para obtener más información sobre los orígenes de las transacciones y las conexiones, consulte [Vinculación de datos reales a los registros originales](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Envío de registro de líneas del diario y uso de material

Para obtener más información sobre la entrada de gasto, consulte [ Registro de uso de material](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Tiempo y materiales

Cuando una entrada de registro de uso de material enviada se vincula a un proyecto que se asigna a una línea de contrato de tiempo y materiales, el sistema crea dos líneas de diario, una para el coste y otra para las ventas no facturadas.

### <a name="fixed-price"></a>Precio fijo

Cuando una entrada de registro de uso de material se vincula a un proyecto que está asignado a una línea de contrato de precio fijo, el sistema crea una línea de diario para el coste.

### <a name="default-pricing"></a>Precios predeterminados

La lógica para indicar precios predeterminados para el material se basa en la combinación de productos y unidades. La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada. Los campos que afectan a los precios predeterminados, como, por ejemplo, **Id. del producto** y **Unidad**, se utilizan para determinar el precio adecuado en la línea de diario. Sin embargo, esto solo funciona para productos de catálogo. Para los productos de escritura, el precio indicado cuando se crea la entrada del registro de uso de material se usa para el coste y el precio de venta en las líneas del diario. 

Puede agregar un campo personalizado en la entrada **Registro de uso de materiales**. Si desea que el valor del campo se propague a los valores reales, cree el campo en las tablas **Datos reales** y **Línea de diario**. Utilice código personalizado para propagar el valor del campo seleccionado desde Entrada de tiempo a Datos reales a través de la línea del diario utilizando los orígenes de la transacción. Para obtener más información sobre los orígenes de las transacciones y las conexiones, consulte [Vinculación de datos reales a los registros originales](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Utilizar diarios de movimientos para registrar costes

Puede usar diarios de movimientos para registrar costes o ingresos en materiales, precios, tiempo, gastos o clases de transacciones de impuestos. Los diarios se pueden usar para los siguientes propósitos:

- Mueva datos reales de transacciones de otro sistema a Microsoft Dynamics 365 Project Operations.
- Registrar cotes que ocurrieron en otro sistema. Estos costes pueden incluir costes de adquisición o subcontratación.

> [!IMPORTANT]
> La aplicación no valida el tipo de línea del diario ni el precio relacionado que se introduce en la línea del diario. Por lo tanto, solo un usuario que sea plenamente consciente del impacto contable que tienen los datos reales en el proyecto debe utilizar los diarios de movimientos para crear los datos reales. Debido al impacto de este tipo de diario, debe elegir cuidadosamente quién tiene acceso a crear diarios de movimientos.

## <a name="record-actuals-based-on-project-events"></a>Registrar datos reales basados en eventos de proyecto

Project Operations registra las transacciones financieras que se producen durante un proyecto. Estas transacciones se registran como datos reales. Las siguientes tablas muestran los diferentes tipos de datos reales que se crean dependiendo de si el proyecto es un proyecto de tiempo y materiales o de precio fijo, de si se encuentra en fase de preventas o de si se trata de un proyecto interno.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>El recurso pertenece a la misma unidad organizativa que la unidad de contratación del proyecto

<table>
<thead>
<tr>
<th rowspan="3">Evento</th>
<th colspan="4">Proyecto facturable o vendido</th>
<th rowspan="3">Proyecto en la fase de preventas</th>
<th rowspan="3">Proyecto interno</th>
</tr>
<tr>
<th colspan="2">Tiempo y materiales</th>
<th colspan="2">Precio fijo</th>
</tr>
<tr>
<th>Datos reales</th>
<th>Divisa de la transacción</th>
<th>Precio fijo</th>
<th>Divisa de la transacción</th>
</tr>
</thead>
<tbody>
<tr>
<td>Se crea una entrada de hora.</td>
<td colspan="6">No hay actividad en la entidad Datos reales</td>
</tr>
<tr>
<td>Se envía una entrada de hora.</td>
<td colspan="6">No hay actividad en la entidad Datos reales</td>
</tr>
<tr>
<td rowspan="2">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</td>
<td>Coste real</td>
<td>Divisa de la unidad de contratación</td>
<td rowspan="2">Coste real</td>
<td rowspan="2">Divisa de la unidad de contratación
<td rowspan="2">Coste real</td>
<td rowspan="2">Coste real</td>
</tr>
<tr>
<td>Dato real de ventas sin facturar: imputable</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="3">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</td>
<td>Coste real</td>
<td>Divisa de la unidad de contratación</td>
<td rowspan="3">Coste real</td>
<td rowspan="3">Divisa de la unidad de contratación</td>
<td rowspan="3">Coste real</td>
<td rowspan="3">Coste real</td>
</tr>
<tr>
<td>Dato real de ventas sin facturar: imputable por la nueva cantidad</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Dato real de ventas sin facturar: no imputable por la diferencia</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="2">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</td>
<td>Inversión de ventas sin facturar</td>
<td>Divisa de contrato de proyecto</td>
<td rowspan="2">Ventas facturadas para hito</td>
<td rowspan="2">Divisa de contrato de proyecto</td>
<td rowspan="2">No disponible</td>
<td rowspan="2">No disponible</td>
</tr>
<tr>
<td>Ventas facturadas</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="3">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</td>
<td>Inversión de ventas sin facturar</td>
<td>Divisa de contrato de proyecto</td>
<td rowspan="3">No disponible</td>
<td rowspan="3">No disponible</td>
<td rowspan="3">No disponible</td>
<td rowspan="3">No disponible</td>
</tr>
<tr>
<td>Ventas facturadas: imputables por la nueva cantidad</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Ventas facturadas: no imputables por la diferencia</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="2">Se corrige una factura para aumentar la cantidad imputable.</td>
<td>Ventas facturadas: inversión</td>
<td>Divisa de contrato de proyecto</td>
<td rowspan="5">
<ul>
<li>Inversión de ventas facturadas para hito</li>
<li>Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></li>
</ul>
</td>
<td rowspan="5">Divisa de contrato de proyecto</td>
<td rowspan="5">No disponible</td>
<td rowspan="5">No disponible</td>
</tr>
<tr>
<td>Ventas facturadas</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="3">Se corrige una factura para disminuir la cantidad imputable.</td>
<td>Ventas facturadas: inversión</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Ventas facturadas por la nueva cantidad</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Ventas sin facturar: imputables por la diferencia</td>
<td>Divisa de contrato de proyecto</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>El recurso pertenece a una unidad organizativa distinta de la unidad de contratación del proyecto

<table>
<thead>
<tr>
<th rowspan="3">Evento</th>
<th colspan="4">Proyecto facturable o vendido</th>
<th rowspan="3">Proyecto en la fase de preventas</th>
<th rowspan="3">Proyecto interno</th>
</tr>
<tr>
<th colspan="2">Tiempo y materiales</th>
<th colspan="2">Precio fijo</th>
</tr>
<tr>
<th>Datos reales</th>
<th>Divisa de la transacción</th>
<th>Precio fijo</th>
<th>Divisa de la transacción</th>
</tr>
</thead>
<tbody>
<tr>
<td>Se crea una entrada de hora.</td>
<td colspan="6">No hay actividad en la entidad Datos reales</td>
</tr>
<tr>
<td>Se envía una entrada de hora.</td>
<td colspan="6">No hay actividad en la entidad Datos reales</td>
</tr>
<tr>
<td rowspan="4">La hora se aprueba y no cambian ni aumentan las horas facturables durante la aprobación.</td>
<td>Coste real</td>
<td>Divisa de la unidad de contratación</td>
<td rowspan="4">Coste real</td>
<td rowspan="4">Divisa de la unidad de contratación</td>
<td rowspan="4">Coste real</td>
<td rowspan="4">Coste real</td>
</tr>
<tr>
<td>Dato real de ventas sin facturar: imputable</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Coste de unidad de dotación de recursos</td>
<td>Divisa de la unidad de dotación de recursos</td>
</tr>
<tr>
<td>Ventas entre organizaciones</td>
<td>Divisa de la unidad de contratación</td>
</tr>
<tr>
<td rowspan="5">La hora se aprueba y disminuyen las horas facturables durante la aprobación.</td>
<td>Coste real</td>
<td>Divisa de la unidad de contratación</td>
<td rowspan="5">Coste real</td>
<td rowspan="5">Divisa de la unidad de contratación</td>
<td rowspan="5">Coste real</td>
<td rowspan="5">Coste real</td>
</tr>
<tr>
<td>Coste de unidad de dotación de recursos</td>
<td>Divisa de la unidad de dotación de recursos</td>
</tr>
<tr>
<td>Ventas entre organizaciones</td>
<td>Divisa de la unidad de contratación</td>
</tr>
<tr>
<td>Dato real de ventas sin facturar: imputable por la nueva cantidad</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Dato real de ventas sin facturar: no imputable por la diferencia</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="2">Se confirma una factura y no cambian ni aumentan las horas facturables durante la aprobación.</td>
<td>Inversión de ventas sin facturar</td>
<td>Divisa de contrato de proyecto</td>
<td rowspan="2">Ventas facturadas para hito</td>
<td rowspan="2">Divisa de contrato de proyecto</td>
<td rowspan="2">No disponible</td>
<td rowspan="2">No disponible</td>
</tr>
<tr>
<td>Ventas facturadas</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="3">Se confirma una factura y disminuyen las horas facturables durante la aprobación.</td>
<td>Inversión de ventas sin facturar</td>
<td>Divisa de contrato de proyecto</td>
<td rowspan="3">No disponible</td>
<td rowspan="3">No disponible</td>
<td rowspan="3">No disponible</td>
<td rowspan="3">No disponible</td>
</tr>
<tr>
<td>Ventas facturadas: imputables por la nueva cantidad</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Ventas facturadas: no imputables por la diferencia</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="2">Se corrige una factura para aumentar la cantidad imputable.</td>
<td>Ventas facturadas: inversión</td>
<td>Divisa de contrato de proyecto</td>
<td rowspan="5">
<ul>
<li>Inversión de ventas facturadas para hito</li>
<li>Cambio del estado de hito de <strong>Facturado</strong> a <strong>Listo para facturación</strong></li>
</ul>
</td>
<td rowspan="5">Divisa de contrato de proyecto</td>
<td rowspan="5">No disponible</td>
<td rowspan="5">No disponible</td>
</tr>
<tr>
<td>Ventas facturadas</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td rowspan="3">Se corrige una factura para disminuir la cantidad imputable.</td>
<td>Ventas facturadas: inversión</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Ventas facturadas por la nueva cantidad</td>
<td>Divisa de contrato de proyecto</td>
</tr>
<tr>
<td>Ventas sin facturar: imputables por la diferencia</td>
<td>Divisa de contrato de proyecto</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
