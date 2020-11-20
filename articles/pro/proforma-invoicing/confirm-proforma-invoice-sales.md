---
title: Confirmar una factura proforma (lite)
description: Este tema proporciona información sobre confirmar facturas proforma en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176542"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Confirmar una factura proforma (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_


Después de que se confirma una factura proforma, el estado de la factura del proyecto se actualiza a **Confirmado**. Cuando se confirma una factura, pasa a ser de solo lectura. En el futuro, la factura solo se puede corregir si hay correcciones o créditos iniciados por el cliente, o si la factura está marcada como pagada.

En la siguiente tabla se enumeran los datos reales creadas por el sistema. Estos datos reales se crean cuando se realizan determinadas operaciones en el borrador de la factura del proyecto antes de que se confirme.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Escenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Datos reales creados en la confirmación</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturar un avance o retención </p>
            </td>
            <td width="408" valign="top">
                <p>
Un tipo real de ventas facturadas, <strong>Anticipo</strong> se crea por el monto del anticipo o adelanto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una venta no facturada real de un monto negativo del anticipo o retención para usarse para la reconciliación.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Después de conciliar completamente un anticipo o adelanto de una factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación. Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un real de las ventas facturadas por el importe esta factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Después de conciliar parcialmente un anticipo o adelanto de una factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación. Este monto es positivo porque está destinado a cancelar el negativo que se creó cuando se facturó el anticipo o anticipo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un real de las ventas facturadas por el importe esta factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una venta negativa real no facturada de la cantidad restante del anticipo o retención que se usará para la reconciliación en futuras facturas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturar una transacción de tiempo sin modificaciones en el borrador de la factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una venta real facturada por las horas y la cantidad en la aprobación del tiempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturar una transacción de tiempo que se editó para reducir la cantidad.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra para las horas y la cantidad restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturar una transacción de tiempo que se editó para aumentar la cantidad.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas por las horas y la cantidad en la aprobación del tiempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturar una transacción de gastos sin modificaciones en el borrador de la factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una venta real facturada para la cantidad y la coste en la aprobación del gasto original </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturar una transacción de gastos que se editó para reducir la cantidad.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra para las cantidad y la cifra restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturar una transacción de gastos que se editó para aumentar la cantidad.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas para la cantidad y la coste en la aprobación del gasto original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación de una tarifa.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas por la cantidad del precio en la línea del diario original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una venta real facturada para la cantidad y la coste en la aprobación de la tarifa de la línea del diario.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturación de un hito.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una venta facturada real por la cantidad del hito en el hito original en la línea de contrato del proyecto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturar una línea de contrato basada en productos.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ventas facturadas reales para la línea de productos con la cantidad y el monto provenientes de la línea de contrato basada en productos.
                </p>
            </td>
        </tr>
    </tbody>
</table>