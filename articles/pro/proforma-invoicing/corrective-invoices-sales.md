---
title: Facturas corregidas (lite)
description: Este tema proporciona información sobre facturas corregidas en Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176452"
---
# <a name="corrected-invoices---lite"></a>Facturas corregidas (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Una factura de proyecto confirmada se puede corregir para procesar cambios o créditos según se negocie con el cliente y el gerente de proyecto.

Para realizar modificaciones en una factura confirmada, abra la factura confirmada y seleccione **Corregir esta factura**. 

> [!NOTE]
> Esta selección no está disponible a menos que se confirme la factura del proyecto.

Se crea un nuevo borrador de factura a partir de la factura confirmada. Todos los detalles de la línea de factura de la factura previamente confirmada se copian en el nuevo borrador. Los siguientes son algunos de los puntos clave que debe comprender acerca de los detalles de la línea en la nueva factura corregida:

- Todas las cantidades se actualizan a cero. La aplicación asume que todos los artículos facturados se abonan por completo. Si es necesario, puede actualizar manualmente estas cantidades para reflejar la cantidad que se está facturando y no la cantidad que se está acreditando. Según la cantidad que introduce, la aplicación calcula la cantidad acreditada. Esta cantidad se refleja en los datos reales que se crean cuando se confirma la factura corregida. Si está realizando cambios en la cantidad del impuesto, debe introducir el monto del impuesto correcto y no el del impuesto que se acredita.
- Las líneas de contrato basadas en productos previamente confirmadas no se copian. No se admite el procesamiento de correcciones en una factura de proyecto basada en productos.
- Las correcciones de hitos siempre se procesan como créditos completos.
- Los montos de anticipo o anticipo pueden corregirse si al cliente se le facturó un monto incorrecto.
- Las conciliaciones de retenciones y anticipos se pueden corregir si se utilizó una cantidad incorrecta para conciliar los cargos en una factura previamente confirmada.

> [!IMPORTANT]
> Los detalles de la línea de la factura que son correcciones a otros cargos ya facturados tienen el campo **Corrección** establecido en **Sí**. Las facturas que tienen detalles de línea de factura corregidos tienen un campo llamado **Tiene correcciones** que también está configurado en **Sí**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Datos reales creados en la confirmación de una factura correctiva:

A continuación se muestran los datos reales creados por la aplicación al confirmar un correctivo en función de las operaciones realizadas en el borrador de la factura correctiva antes de la confirmación.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Confirmar la corrección de un anticipo o anticipo facturado.<strong></strong>
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
Se crea una reversión real de ventas facturadas por el monto del anticipo o anticipo para revertir las ventas facturadas originales.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Se crea un nuevo real de ventas facturadas para el monto corregido en el anticipo o en la línea de factura corregida basada en anticipos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una venta no facturada real del monto negativo del anticipo o línea de factura corregida basada en anticipos, que se utilizará para la conciliación.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Una confirmación de la corrección de un anticipo o anticipo previamente conciliado.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversión de ventas no facturadas del anticipo o anticipo que se creó para la conciliación. Este monto es positivo y está destinado a cancelar el negativo que se creó cuando tuvo lugar la conciliación anterior.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una reversión real de las ventas facturadas por el importe de la factura anterior.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una nueva venta facturada real para la cantidad corregida del anticipo que se aplicará en la factura corregida.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Una venta no facturada real con un monto negativo del resto del anticipo o avance corregido que se usará para la reconciliación en facturas posteriores.
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
La factura de hito o el estado de facturación en la línea del contrato del proyecto se actualiza a **Listo para facturar**.
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
Incompatible </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Créditos y correcciones de una línea de contrato basado en producto facturado previamente.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Incompatible </p>
            </td>
        </tr>
    </tbody>
</table>
