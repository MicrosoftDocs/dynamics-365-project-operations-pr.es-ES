---
title: Crear programaciones de facturas en una línea de contrato basada en proyecto (lite)
description: Este tema proporciona información sobre cómo crear calendarios e hitos de facturas.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 548858f6d2257343a632657ca386da03f1f330a9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003252"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Crear programaciones de facturas en una línea de contrato basada en proyecto (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Puede asociar una programación de facturas en una línea de contrato basada en proyecto. La facturación solo se permite después de que se gana el contrato para crear un contrato de proyecto. Los cronogramas de facturas permiten la creación automática de borradores de facturas para una línea de contrato basada en proyecto. Si planea crear siempre facturas manualmente, puede omitir la creación de cronogramas de facturas en una línea de contrato basada en proyecto o en una línea de contrato.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Crear una programación de facturas de tiempo y material para una línea de contrato basada en proyecto

Cuando una línea de contrato basada en un en proyecto tiene un método de facturación basado en tiempo y materiales, puede crear un calendario de facturación basado en la fecha. Para generar automáticamente un programa de facturación basado en fecha, complete los siguientes pasos.

1. Vaya a **Configuraciones** > **Frecuencias de facturas** para configurar la frecuencia de facturación.
2. Abra el contrato del proyecto y en la pestaña **Resumen**, establezca la fecha de entrega solicitada.
3. Abra la línea de contrato de tiempo y material para la que desea crear una programación de factura basada en fecha. 
4. Sobre la pestaña **Programación de facturas**, seleccione una fecha de inicio de facturación y la frecuencia de facturación. 
5. En la subcuadrícula, seleccione **Generación de programa de facturas**.

    El sistema genera el programa de facturas con la siguiente información de campo:

    - **Fecha de ejecución de la factura** se establece en la fecha según la frecuencia de facturación.
    - **Fecha de corte de la transacción** se establece en el día anterior a la **Fecha de emisión de la factura**.
    - **Estado de ejecución** se establece automáticamente en **No ejecutado**. Cuando el trabajo de creación automática de facturas se ejecute para una determinada **fecha de ejecución de facturas**, actualizará este campo a **Ejecución correcta** o **Ejecución fallida**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Crear una programación de facturas de precio fijo para una línea de contrato basada en proyecto

Cuando una línea de contrato basada en proyecto tiene un método de facturación de precio fijo, puede crear un programa de facturación basado en hitos. Complete los siguientes pasos para generar automáticamente un programa de facturas basado en hitos para un conjunto fijo de hitos que se distribuyen equitativamente durante el período del calendario.

1. Vaya a **Configuraciones** > **Frecuencias de facturas** para configurar la frecuencia de facturación.
2. Abra el contrato del proyecto y en la pestaña **Resumen**, establezca la fecha de entrega solicitada.
3. Abra la línea de contrato de precio fijo en la que necesita crear un cronograma de hitos. 
4. Sobre la pestaña **Programación de facturas (hitos de facturación)**, seleccione la fecha de inicio de facturación y la frecuencia de facturación. 
5. En la subcuadrícula, seleccione **Generar hitos periódicos**.

    El sistema genera el programa de facturas con la siguiente información de hito.

    - **Nombre del hito** se establece en la fecha que se dicta en función de la frecuencia de facturación.
    - **Fecha del hito** se establece en la fecha que se dicta en función de la frecuencia de facturación.
    - **Importe del hito** se calcula dividiendo el monto del contrato en la línea del contrato basado en el proyecto por el número de hitos según lo dictado por la frecuencia, el inicio de la facturación y las fechas de entrega solicitadas.
    - Si la línea del contrato tiene un valor en el campo **Importe de impuesto estimado**, este campo también se distribuye a cada hito por igual cuando se generan hitos periódicos.

Los hitos de facturación deben ser iguales al valor contratado de la línea de contrato basada en el proyecto. Si no son iguales, se produce un error. Puede corregir ese error verificando que los hitos de facturación sumen el valor contratado de la línea ya sea creando, editando o eliminando hitos. Una vez realizados los cambios, actualice la página.

### <a name="manually-create-milestones"></a>Crear hitos manualmente

Los hitos de precio fijo se pueden generar manualmente cuando no se dividen periódicamente. Para crear un hito manualmente, complete los siguientes pasos.

1. Abra la línea de contrato de precio fijo en la que desea crear un hito. 
2. Sobre la pestaña **Programación de facturas**, en la subcuadrícula, seleccione **+ Crear nuevo hito de línea de contrato**.
3. Sobre el formulario **Creación de hitos**, ingrese la información requerida según la siguiente tabla. 

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| Nombre del hito | Creación rápida | Campo de texto para el nombre del hito. | Este campo se incluye en el hito de la línea del contrato del proyecto y en la factura. |
| Tarea de proyecto | Creación rápida | Si el hito está vinculado a una tarea del proyecto, use esta referencia para agregar lógica personalizada y establecer el estado del hito según el estado de la tarea. | No hay impacto posterior de esta referencia a una tarea. |
| Fecha de hito | Creación rápida | La fecha en la que el proceso de creación automática de factura debe buscar el estado de este hito para considerarlo para facturación. | Este se incluye en el hito de la línea del contrato del proyecto y en la factura. |
| Estado de la factura | Creación rápida | Cuando se crea el hito, este estado siempre se establece en **No está listo para facturar** o **No empezado**. | Este se incluye en el hito de la línea del contrato del proyecto y en la factura. |
| Importe de línea | Creación rápida | El importe o valor del hito que se facturará al cliente. | Este campo se incluye en el hito de la línea del contrato del proyecto y en la factura. |
| Impuestos | Creación rápida | La cantidad del impuesto aplicado al hito. | Este se incluye en el hito de la línea del contrato del proyecto y en la factura. |

4. Seleccione **Guardar y cerrar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]