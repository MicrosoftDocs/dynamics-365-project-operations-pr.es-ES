---
title: Información general de datos reales
description: En este tema se proporciona información sobre datos reales del proyecto.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7ab2638d82eb5ba928d95ca6a524a1566f21e1ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587607"
---
# <a name="actuals-overview"></a>Información general de datos reales

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Los datos reales son la cantidad de trabajo que se ha completado en un proyecto. Es posible rastrear los datos reales del proyecto hasta sus documentos de origen. Dichos documentos de origen incluyen datos sobre el tiempo, el gasto, los movimientos de diario y también las facturas.

![Cómo se rastrean los datos reales del proyecto hasta los documentos de origen.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Envío de una entrada de hora

En PSA, cuando se envía una entrada de hora para un proyecto que está asignado a una línea de contrato de tiempo y materiales, se crean dos líneas de diario. Una línea es para el coste y la otra es para las ventas sin facturar. Cuando se envía una entrada de hora para un proyecto que está asignado a una línea de contrato de precio fijo, solo se crea una línea de diario para el coste. 

La lógica para especificar precios predeterminados se encuentra en la línea de diario. Todos los valores de campo de una entrada de hora se copian a la línea de diario. Estos campos incluyen la fecha de la transacción, la línea de contrato a la que está asignado el proyecto y el resultado de la divisa en la lista de precios correspondiente. 

Los campos que afectan a los precios predeterminados, como, por ejemplo, **Rol** y **Unidad organizativa**, hacen que se especifique el precio adecuado de manera predeterminada en la línea de diario. Si agrega un campo personalizado en la entrada de hora y desea que el valor de campo se propague a los datos reales, cree el campo en la entidad Datos reales y utilice las asignaciones de campos para copiar el campo de la entrada de hora a los datos reales.

## <a name="submitting-an-expense-entry"></a>Envío de una entrada de gastos

En PSA, cuando se envía una entrada de gastos para un proyecto que está asignado a una línea de contrato de tiempo y materiales, se crean dos líneas de diario. Una línea es para el coste y la otra es para las ventas sin facturar. Cuando se envía una entrada de gastos para un proyecto que está asignado a una línea de contrato de precio fijo, solo se crea una línea de diario para el coste.

La lógica para especificar los precios predeterminados para los gastos se basa en la categoría de gastos seleccionada en la página **Entrada de gastos**. La fecha de transacción, la línea de contrato a la que está asignado el proyecto y la divisa se utilizan para determinar la lista de precios adecuada. Sin embargo, para el precio sí mismo, el importe que especifica el usuario se establece directamente en las líneas de diario de gastos de costes y ventas de forma predeterminada.

En la versión actual de PSA, la especificación de precios predeterminados por entrada según la categoría en las entradas de gastos no está disponible.

## <a name="using-entry-journals-to-record-costs"></a>Utilización de diarios de movimientos para registrar costes

En PSA, los diarios de movimientos permiten registrar el coste o ingreso en las clases de materiales, cuotas, gastos o transacciones de impuestos. Los diarios disponen de encabezado, líneas y la acción **Confirmar**. Estos son algunas escenarios en los que puede utilizar un diario:

- Debe registrar ventas y costes reales de materiales en un proyecto.
- Debe mover datos reales de transacciones de otro sistema a PSA.
- Debe registrar los costes que se han producido en otro sistema, como, por ejemplo, los costes de adquisición o subcontratación.

> [!IMPORTANT]
> Solo un usuario que sea plenamente consciente del impacto contable que tienen los datos reales en el proyecto puede usar diarios de movimientos para crear datos reales. Esto se debe a que la aplicación no valida el tipo de línea del diario o el precio relacionado que se ingresa en la línea del diario. Debido al impacto de este tipo de diario, tenga la debida precaución con respecto a quién tiene acceso para crear diarios de movimientos.     


## <a name="recording-actuals-based-on-project-events"></a>Registro de datos reales basados en eventos de proyecto

El PSA registra las transacciones financieras que se producen durante un proyecto. Estas transacciones se registran como **datos reales**. Las siguientes tablas muestran los diferentes tipos de datos reales que se crean dependiendo de si el proyecto es un proyecto de tiempo y materiales o de precio fijo, de si se encuentra en fase de preventas o de si se trata de un proyecto interno.

**El recurso pertenece a la misma unidad organizativa que la unidad de contratación del proyecto**

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

**El recurso pertenece a una unidad organizativa distinta de la unidad de contratación del proyecto**

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
