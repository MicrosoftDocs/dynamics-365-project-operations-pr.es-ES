---
title: Confirmar una factura proforma
description: Este tema proporciona información sobre cómo confirmar una factura proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287889"
---
# <a name="confirm-a-proforma-invoice"></a>Confirmar una factura proforma

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Después de que se confirma una factura proforma, el estado de la factura del proyecto se actualiza a **Confirmado**. Cuando se confirma una factura, pasa a ser de solo lectura. En el futuro, la factura solo se puede corregir si hay correcciones o créditos iniciados por el cliente, o cuando se marca como pagada.

En la siguiente tabla se enumeran los datos reales creadas por el sistema. Estos datos reales se crean cuando se realizan determinadas operaciones en el borrador de la factura del proyecto antes de que se confirme.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Escenario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Datos reales creados en la confirmación</strong>
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
Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra para las horas y la cantidad restantes y la cantidad tras deducir las figuras corregidas de la línea de factura editada, una reversión de la venta real no facturada y un real de ventas facturado equivalente.
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