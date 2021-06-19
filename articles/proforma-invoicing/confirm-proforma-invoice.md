---
title: Confirmar una factura basada en proyecto proforma
description: Este tema proporciona información sobre cómo confirmar las facturas basadas en un proyecto proforma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012157"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Confirmar una factura basada en proyecto proforma

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Después de que se confirma una factura proforma, el estado de la factura del proyecto se actualiza a **Confirmado**. Cuando se confirma una factura, pasa a ser de solo lectura. En el futuro, la factura solo se puede corregir si hay correcciones o créditos iniciados por el cliente.

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
Las ventas reales no facturadas con un importe negativo del anticipo o avance que se utilizará para la conciliación.
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
Un nuevo valor real de ventas no facturadas que no es imputable por las horas restantes y el importe después de deducir las cifras corregidas en el detalle de la línea de factura editada, una reversión de los valores reales de las ventas y un valor real de ventas facturado equivalente.
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
Una venta real facturada para la cantidad y la coste en la aprobación del gasto original.
                </p>
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
Facturar una transacción de material sin modificaciones en el borrador de la factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de utilización de material original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valor real de ventas facturado por la cantidad y el importe de la aprobación de utilización de material original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturar una transacción de material que se editó para reducir la cantidad.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de tiempo original.
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
Facturar una transacción de material que se editó para aumentar la cantidad.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una anulación de ventas sin facturar por la cantidad y el importe de la aprobación de utilización de material original.
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
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
