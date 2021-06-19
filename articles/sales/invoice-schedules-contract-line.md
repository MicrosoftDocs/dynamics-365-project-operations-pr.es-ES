---
title: Crear un programa de factura en una línea de contrato basada en un proyecto
description: Este tema proporciona información sobre cómo crear programaciones e hitos de facturas en líneas de contrato.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f84d9935eec13666e3eaaa675908e9bc3d2097c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010132"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Crear un programa de factura en una línea de contrato basada en un proyecto 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Puede crear un programa de factura a una línea de contrato basada en un proyecto. La facturación solo se permite después de que se gana el contrato y usted está creando un contrato de proyecto. Un programa de facturas permite crear automáticamente borradores de facturas para una línea de contrato basada en proyecto. Sin embargo, si solo crea facturas manualmente, puede omitir la creación de programas de facturas en las líneas de contrato.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Crear una programación de facturación de tiempo y material para una línea de contrato

Cuando una línea de contrato basada en un proyecto tiene un método de facturación de tiempo y material, puede crear una programación de facturas basada en la fecha. Para generar automáticamente un programa de facturación basado en fecha, complete los siguientes pasos.

1. Vaya a **Configuración** > **Frecuencias de facturación** y configure una frecuencia de facturación.
2. Vaya al registro del contrato del proyecto y en la pestaña **Resumen**, en el campo **Fecha de entrega requerida**, seleccione una fecha.
3. Abra la línea de contrato **Tiempo y material** para la que prepara la programación de facturas basada en la fecha. 
4. En la pestaña **Programación de facturas**, seleccione la fecha de inicio de facturación y la frecuencia de facturación.
5. En la subcuadrícula, seleccione **Generar programación de facturas**. La programación de facturas se genera con los campos **Fecha de emisión de la factura**, **Fecha de cierre de la transacción** y **Estado de ejecución** de la siguiente manera:

    - **Fecha de emisión de la factura**: esta fecha se establece según la frecuencia de facturación.
    - **Fecha de cierre de la transacción**: el día anterior a la fecha de ejecución de la factura.
    - **Estado de ejecución**: se establece automáticamente en **No ejecutado**. Cuando el trabajo de creación automática de facturas se ejecute para una determinada fecha de ejecución de facturas, actualizará este campo a **Ejecución correcta** o **Ejecución fallida**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Crear una programación de facturación de precio fijo para una línea de contrato

Cuando la línea de contrato basada en proyecto tiene un método de facturación fijo, puede crear una programación de facturación basada en hitos. 

> [!NOTE]
> No se pueden crear hitos en una línea de contrato si no hay ningún proyecto asignado a la línea de contrato.

Complete los siguientes pasos para generar un programa de facturación basado en hitos para un conjunto fijo de hitos que se distribuyen para el período del calendario.

1. Vaya a **Configuración** > **Frecuencias de facturación** y configure una frecuencia de facturación.
2. Vaya al registro del contrato del proyecto y en la pestaña **Resumen**, en el campo **Fecha de entrega requerida**, seleccione una fecha.
3. Abra la línea de contrato **Precio fijo** para la que está creando la programación de hitos. En la pestaña **Hitos de facturación**, seleccione la fecha de inicio de facturación y la frecuencia de facturación. 
4. En la subcuadrícula, seleccione **Generar hitos periódicos**. La programación de la factura se genera con los campos **Nombre del hito**, **Fecha del hito** e **Importe del hito** campos configurados de la siguiente manera:

    - **Nombre del hito**: este nombre viene impuesto por la frecuencia de factura.
    - **Fecha del hito**: esta fecha se establece según la frecuencia de facturación.
    - **Cantidad del hito**: el importe se calcula dividiendo la cantidad del contrato en la línea de contrato por el número de hitos, según indiquen la frecuencia y el inicio de la facturación y las fechas de entrega solicitadas.

    Si la línea del contrato tiene un valor en el campo **Importe de impuesto estimado**, este campo también se distribuye por igual a cada hito al generar hitos periódicos.

Los hitos de facturación deben ser iguales al valor contratado de la línea de contrato. Si no lo hacen, recibirá un error en la página **Línea de contrato**. Puede corregir el error verificando que los hitos de facturación sumen el valor contratado de la línea creando, editando o eliminando hitos. Una vez realizados los cambios, actualice la página para eliminar el error.

### <a name="manually-create-milestones"></a>Crear hitos manualmente

Puede generar hitos de precio fijo manualmente cuando no se dividen periódicamente. Complete los pasos siguientos para crear un hito manualmente.

1. Abra la línea de contrato de precio fijo para la que está creando un hito y en la pestaña **Programación de facturas**, en la subcuadrícula, seleccione **+ Crear nuevo hito de línea de contrato**. 
2. En la página **Creación de hitos**, introduzca la información requerida según la siguiente tabla.

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| Nombre del hito | Creación rápida | Campo de texto para el nombre del hito. | Esto se lleva al hito de la línea del contrato del proyecto y la factura. |
| Tarea de proyecto | Creación rápida | Si el hito está vinculado a la tarea del proyecto, use esta referencia para agregar una lógica personalizada y establecer el estado del hito en función del estado de la tarea. | La aplicación no tiene ningún impacto posterior de esta referencia para ninguna tarea. |
| Fecha de hito | Creación rápida | Establezca la fecha en la que el proceso de creación automática de facturas debe buscar el estado de este hito para considerarlo para la facturación. | Esto se lleva al hito de la línea del contrato del proyecto y la factura. |
| Estado de la factura | Creación rápida | Cuando se crea un hito, este estado siempre se establece **No listo para facturación** o **No iniciado**. | Esto se lleva al hito de la línea del contrato del proyecto y la factura. |
| Importe de línea | Creación rápida | Importe o valor del hito que se facturará al cliente. | Esto se lleva al hito de la línea del contrato del proyecto y la factura. |
| Impuestos | Creación rápida | La cantidad del impuesto aplicado al hito. | Esto se lleva al hito de la línea del contrato del proyecto y la factura. |

3. Seleccione **Guardar y cerrar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]