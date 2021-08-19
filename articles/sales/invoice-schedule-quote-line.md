---
title: Facturar programaciones en líneas de oferta basadas en proyecto
description: Este tema proporciona información sobre cómo crear programaciones e hitos de facturas para las líneas de oferta.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0d07596b299d71b229487faf80a09e368059575ea37095d2c82d35561d009c96
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988627"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Facturar programaciones en líneas de oferta basadas en proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Una línea de oferta basada en proyectos brinda la capacidad de expresar una programación de facturas. Esto es opcional durante la fase de oferta, porque la aplicación no admite la facturación de un proyecto cuando está vinculado a una línea de oferta. La facturación solo se permite después de ganar la oferta. El único impacto posterior de la creación de un cronograma de facturas durante la fase de oferta es que este cronograma de facturas se copia en la línea de contrato basada en el proyecto. Si no crea un cronograma de facturas durante la fase de oferta, podrá hacerlo en la línea de contrato basada en proyecto.

En general, el propósito de las programaciones de facturas es permitir la creación automática de borradores de facturas para una línea de contrato basada en proyecto. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Cree una programación de facturación de tiempo y material para una línea de oferta basada en proyectos

Cuando el método de facturación para una línea de oferta basada en proyecto es Tiempo y material, el sistema genera una programación de facturación basado en fecha. Para generar automáticamente un programa de facturación basado en fecha, complete los siguientes pasos.

1. Vaya a **Configuración** > **Frecuencias de facturación** y configure una frecuencia de facturación.
2. En la página **Ofertas**, abra la oferta del proyecto y en la pestaña **Resumen** establezca una fecha de entrega solicitada.
3. Abra la línea de oferta de tiempo y material para la que necesita crear un programa de facturación basado en fecha. 
4. En la pestaña **Programación de facturas**, seleccione valores en los campos **Inicio de facturación** y **Frecuencia de facturación**. 
5. En la subcuadrícula, seleccione **Generación de programa de facturas**.
6. La aplicación genera la programación de facturas con los campos **Fecha de emisión de la factura**, **Fecha de cierre de la transacción** y **Estado de ejecución** configurados de la siguiente manera:

    - **Fecha de emisión de la factura** se establece en la fecha que se dicta en función de la frecuencia de facturación.
    - **Fecha de cierre de la transacción** se establece en el día anterior a la **Fecha de emisión de la factura**.
    - **Estado de ejecución** se establece automáticamente en **No ejecutado**. Cuando el trabajo de creación automática de facturas se ejecute para una determinada fecha de ejecución de facturas, actualizará este campo a **Ejecución correcta** o **Ejecución fallida**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Crear una programación de facturación de precio fijo para una línea de oferta basada en proyecto

Cuando la línea de oferta basada en proyecto tiene un método de facturación **Fijo**, el sistema crea una programación de facturación basada en hitos. Complete los siguientes pasos para generar automáticamente esta programación para un conjunto fijo de hitos que se distribuyen equitativamente para el período del calendario.

1. Vaya a **Configuración** > **Frecuencias de facturación** y configure una frecuencia de facturación.
2. En la página **Ofertas**, abra la oferta del proyecto y en la pestaña **Resumen** establezca una fecha de entrega solicitada.
3. Abra la línea de oferta de precio fijo para la que necesita crear un cronograma de hitos. 
4. En la pestaña **Programación de facturas**, seleccione valores en los campos **Inicio de facturación** y **Frecuencia de facturación**. 
5. En la subcuadrícula, seleccione **Generar hitos periódicos**.
6. La aplicación genera la programación de la factura con un nombre de hito, una fecha y el importe.

    - El nombre del hito se establece en la fecha que se dicta en función de la frecuencia de facturación.
    - La fecha del hito se establece en la fecha que se dicta en función de la frecuencia de facturación.
    - El importe del hito se calcula dividiendo el monto de la oferta en la línea de oferta basada en el proyecto por el número de hitos, según indiquen la frecuencia y el inicio de la facturación y las fechas de entrega solicitadas.
    - Si la línea de oferta también tiene un importe de impuestos estimado, este valor se divide entre cada hito por igual al generar hitos periódicos.

### <a name="manually-create-milestones"></a>Crear hitos manualmente

Los hitos de precio fijo también se pueden generar manualmente cuando no se dividen periódicamente. Para crear hitos manualmente:

Abra la línea de oferta de precio fijo para la que necesita crear un hito. En la pestaña **Programación de facturas**, en la subcuadrícula, seleccione **+ Crear un nuevo hito de línea de cotización** e ingrese la información requerida según la siguiente tabla.

| **Campo** | **Ubicación** | **Descripción** | **Impacto posterior** |
| --- | --- | --- | --- |
| Nombre del hito | Creación rápida | El nombre del hito. | Esto se propaga al hito de la línea del contrato del proyecto y a la factura |
| Tarea de proyecto | Creación rápida | Si el hito está vinculado a la tarea del proyecto, puede usar esta referencia para agregar una lógica personalizada y establecer el estado del hito en función del estado de la tarea. | La aplicación no tiene ningún impacto posterior de esta referencia para ninguna tarea. |
| Fecha de hito | Creación rápida | Establezca la fecha en la que el proceso de creación automática de facturas debe buscar el estado de este hito para considerarlo para la facturación. | Esto se propaga al hito de la línea del contrato del proyecto y a la factura. |
| Estado de la factura | Creación rápida | Cuando se crea un hito, este estado siempre se establece en **No listo para facturación**. | Esto se propaga al hito de la línea del contrato del proyecto y a la factura. |
| Importe de línea | Creación rápida | Importe o valor del hito que se facturará al cliente. | Esto se propaga al hito de la línea del contrato del proyecto y a la factura. |
| Impuestos | Creación rápida | Importe del impuesto que se aplicará al hito. | Esto se propaga al hito de la línea del contrato del proyecto y a la factura. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]