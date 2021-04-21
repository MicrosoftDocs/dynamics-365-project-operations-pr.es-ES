---
title: Facturas basadas en proyecto correctivas
description: Este tema proporciona información sobre cómo crear y confirmar facturas basadas en proyectos correctivas en Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867062"
---
# <a name="corrective-project-based-invoices"></a>Facturas basadas en proyecto correctivas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Una factura de proyecto confirmada se puede corregir para procesar cambios o créditos según se negocie con el cliente y el gerente de proyecto.

Para realizar modificaciones en una factura confirmada, abra la factura confirmada y seleccione **Corregir esta factura**. 

> [!NOTE]
> Esta selección no está disponible a menos que se confirme una factura del proyecto o que la factura basada en el proyecto tenga anticipos o pagos a cuenta o conciliaciones de anticipos o pagos a cuenta.

Se crea un nuevo borrador de factura a partir de la factura confirmada. Todos los detalles de la línea de factura de la factura previamente confirmada se copian en el nuevo borrador. Los siguientes son algunos de los puntos clave que debe comprender acerca de los detalles de la línea en la nueva factura corregida:

- Todas las cantidades se actualizan a cero. Dynamics 365 Project Operations supone que todos los elementos facturados se abonan en su totalidad. Si es necesario, puede actualizar manualmente estas cantidades para reflejar la cantidad que se está facturando y no la cantidad que se está acreditando. Según la cantidad que introduce, la aplicación calcula la cantidad acreditada. Esta cantidad se refleja en los datos reales que se crean cuando se confirma la factura corregida. Si está realizando cambios en la cantidad del impuesto, debe introducir el monto del impuesto correcto y no el del impuesto que se acredita.
- Las correcciones de hitos siempre se procesan como créditos completos.


> [!IMPORTANT]
> Para los detalles de la línea de factura que son correcciones de otros cargos ya facturados, el campo **Corrección** está establecido en **Sí**. Para las facturas con detalles de línea de factura corregida, el campo **Tiene correcciones** está establecido en **Sí**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Datos reales creados cuando se confirma una factura correctiva

La siguiente tabla enumera los datos reales que se crean cuando se confirma una factura correctiva.

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
Facturación del crédito total de una transacción de tiempo facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas facturadas por las horas y el monto en el detalle de la línea de factura original por tiempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una venta nueva real sin facturar por las horas y el monto en el detalle de la línea de factura original por tiempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación del crédito parcial en una transacción a tiempo.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas facturadas por las horas y el monto facturado en el detalle de la línea de factura original por tiempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por las horas y el monto en el detalle de la línea de factura editada, una reversión de este y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por las horas restantes y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación del crédito total de una transacción de gastos facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los gastos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los gastos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación del crédito parcial de una transacción de gastos facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas facturadas por la cantidad y el monto facturado en el detalle de la línea de factura original por unos gastos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida, una reversión de este y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por la cantidad restante y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación del crédito total de una transacción de material facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una anulación de ventas facturada por la cantidad y el importe en el detalle de línea de factura original en concepto de material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo valor real de ventas sin facturar por la cantidad y el importe en el detalle de línea de factura original en concepto de material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturación del abono parcial de una transacción de material.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una anulación de ventas facturada por la cantidad y el importe facturados en el detalle de línea de factura original en concepto de material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo valor real de ventas no facturadas que es imputable por la cantidad y el importe en el detalle de la línea de factura editada, una reversión de esto y un valor real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por la cantidad restante y el monto después de deducir las cifras corregidas en el detalle de la línea de factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación del crédito total de una transacción de precio facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas facturadas por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una nueva venta sin facturar real por la cantidad y el monto en el detalle de la línea de factura original por los honorarios.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturación del crédito parcial de una transacción de precio facturada previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas facturadas por la cantidad y el monto facturados en el detalle de la línea de factura original por los honorarios.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuevo real de ventas no facturadas que se cobra por la cantidad y el monto en el detalle de la línea de factura corregida editada, una reversión de este y un real de ventas facturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturación del crédito total de un hito facturado previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas facturadas por el monto en el detalle de la línea de factura original para el hito.
                </p>
                <p>
El estado de la factura del hito se actualiza desde <b>Factura del cliente registrada</b> hasta <b>Listo para facturar</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturación del crédito parcial de un hito facturado previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Esto escenario no es compatible.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
