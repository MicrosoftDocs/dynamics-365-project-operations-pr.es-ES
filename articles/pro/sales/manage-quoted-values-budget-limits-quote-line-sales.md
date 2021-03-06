---
title: Líneas de ofertas basadas en proyectos (Pro)
description: Este tema proporciona información sobre el uso de líneas de oferta basadas en proyectos para trabajo de proyecto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908629"
---
# <a name="project-based-quote-lines-pro"></a>Líneas de ofertas basadas en proyectos (Pro)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las líneas de oferta basadas en proyectos están diseñadas para ayudar a estimar el trabajo del proyecto en un compromiso. La estructura de una línea de oferta basada en proyectos se amplía para las estimaciones de proyectos con los siguientes conceptos:

- Método de facturación
- Asignación de proyectos y tareas
- Clases de transacciones incluidas
- Límite a no exceder
- Configuración de imputabilidad
- Estimación utilizando los detalles de la línea de oferta
- Clientes de línea de oferta

La siguiente tabla proporciona información sobre los campos de la pestaña **General** de la línea de oferta basada en proyecto. Estos campos ayudan a establecer la base para una estimación detallada y desde cero para el trabajo del proyecto.

| **Campo** | **Relevancia, propósito y orientación** | **Impacto posterior** |
| --- | --- | --- |
| Nombre | El nombre de la línea de oferta que debería ayudarle a identificar el componente discreto de la oferta que se está estimando. | Se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Método de facturación | En una oferta creada a partir de una oportunidad, este valor se copia del campo correspondiente en la línea de oportunidad. Este campo incluye los dos modelos de contratación principales admitidos por Dynamics 365 Project Operations:</br>- Precio fijo</br>- Tiempo y material.| Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Project | Utilice este campo opcional para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso. Cuando un proyecto se asigna a una línea de oferta, ayuda a configurar las tareas facturables y también a traer una estimación basada en el proyecto a la línea de oferta como detalles de la línea de oferta. Cuando un proyecto no está asignado a una línea de oferta basada en proyecto, la estimación debe crearse manualmente creando cada detalle de línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta.|
| Tareas incluidas | Indica si esta línea de oferta se utiliza para todas o algunas de las tareas del proyecto para el proyecto seleccionado. Este campo tiene los siguientes posibles valores:</br>- Todas las tareas de proyecto</br>- Solo tareas de proyecto seleccionadas</br>Un valor en blanco en este campo es equivalente a la opción **Todas las tareas del proyecto**. | Cuando se selecciona **Solo tareas de proyecto seleccionadas** en la página del proyecto, la pestaña **Configuración de facturación de tareas** le permite seleccionar tareas específicas para asociarlas a esta línea de oferta. Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Incluir tiempo | Un indicador **Sí**/**No** indica si las transacciones de tiempo o los costes laborales del proyecto seleccionado se incluirán en la estimación de esta línea de oferta. Un valor **No** indica que las transacciones de tiempo o los costes laborales no se incluirán en la estimación de esta línea de oferta. Un valor **Sí** indica que las transacciones de tiempo o los costes laborales se incluirán en la estimación de esta línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Incluir gasto | Un indicador **Sí**/**No** indica si los costes de gastos del proyecto seleccionado se incluirán en la estimación de esta línea de oferta. Un valor **No** indica que el coste de gastos no se incluirá en la estimación de esta línea de oferta. Un valor **Sí** indica que el coste de gastos se incluirá en la estimación de esta línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Incluir tarifa | Un indicador **Sí**/**No** indica si las tarifas del proyecto seleccionado se incluirán en la estimación de esta línea de oferta. Un valor **No** indica que las tarifas no se incluirán en la estimación de esta línea de oferta. Un valor **No** indica que las tarifas se incluirán en la estimación de esta línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Importe de la oferta | Esta es la cantidad que se ofertará al cliente por todo el trabajo previsto en esta línea de oferta basada en el proyecto. En una oferta creada a partir de una oportunidad, este valor se copia del campo **Presupuesto del cliente** correspondiente en la línea de oportunidad. Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los detalles de la línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Impuesto estimado | Este es un campo editable para que el usuario agregue el importe del impuesto estimado en la línea de oferta. Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los impuestos de los detalles de la línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Importe ofertado después de impuestos | Este campo es el importe de la línea de oferta después de impuestos y es de solo lectura. La cantidad de este campo se calcula como *Importe ofertado + Impuestos*. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Límite de No exceder | Este campo es editable y solo está disponible en líneas de oferta basadas en proyectos que tienen un método de facturación **Tiempo y material**. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Presupuesto del cliente | Este campo es editable y se copia a partir del campo correspondiente de la línea de oportunidad si la oferta se creo a partir de una oportunidad. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Reglas de validación para campos en la pestaña General de líneas de oferta basadas en proyectos

**Regla 1**: si el campo **Tareas incluidas** está en blanco, o si está configurado en **Todas las tareas del proyecto**, se incluye un proyecto en la línea de oferta.

**Regla 2**: si el campo **Tareas incluidas** está en blanco, o si está configurado en **Todas las tareas del proyecto**, un proyecto y una determinada clase de transacción solo se pueden incluir en una línea de oferta basada en proyectos de una oferta.

**Regla 3**: si el campo **Tareas incluidas** está configurado en **Solo tareas del proyecto seleccionadas**, un proyecto y una determinada clase de transacción se pueden incluir en varias líneas de oferta basadas en proyectos de una oferta.

**Regla 4**: si una oportunidad tiene varias ofertas, puede haber líneas de oferta de ofertas diferentes que hagan referencia al mismo proyecto e incluyan la misma clase de transacción.

**Regla 5**: si las ofertas no pertenecen a la misma oportunidad, no pueden incluir el mismo proyecto y clase de transacción.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Oportunidad</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Oferta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Línea de oferta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>Tareas incluidas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluir tiempo</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluir gasto</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Incluir</strong>
                </p>
                <p>
                    <strong>Tarifa</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Válido/no válido</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Razón</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
No válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracción de la regla n.º 2. El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en las líneas de oferta QL1 y QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
No válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracción de la regla n.º 2. El tiempo y las tarifas del proyecto P1 se incluyen en las líneas de oferta QL1 y QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
El tiempo y las tarifas del proyecto P1 se incluyen en QL1.
El gasto del proyecto P1 se incluyen en QL2.
No hay superposición en lo que se incluye en cada línea de oferta y es válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Solo tareas seleccionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
No válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracción de la regla n.º 2 anterior </p>
                <p>
Q1 incluye tiempo, gastos y tarifas en un subconjunto de tareas en el proyecto P1.
                </p>
                <p>
QL2 incluye tiempo, gastos y tarifas para todo el proyecto P1 y se superpone con lo que se incluye en Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Solo tareas seleccionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Según la regla n.° 3 anterior, </p>
                <p>
Q1 incluye tiempo, gastos y tarifas en un subconjunto de tareas en el proyecto P1.
                </p>
                <p>
QL2 incluye tiempo, gastos y tarifas para un subconjunto de tareas en el proyecto P1.
                </p>
                <p>
La única validación adicional es alrededor del subconjunto de tareas de QL1 que son diferentes del subconjunto de tareas de QL2. Esto asegura que no haya superposiciones. Esto lo hace el sistema cuando se asocian tareas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Solo tareas seleccionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas las tareas del proyecto o en blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Según la Regla n.° 5, Q1 y Q2 son dos ofertas de la misma oportunidad, por lo que ambas pueden estimar los mismos componentes de un proyecto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas las tareas del proyecto o en blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas las tareas del proyecto o en blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Según la Regla n.° 4, Q1 y Q2 son dos ofertas de diferentes oportunidades, por lo que no pueden estimar los mismos componentes del mismo proyecto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas las tareas del proyecto o en blanco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" valign="top">
                <p>
No válido </p>
            </td>
        </tr>
    </tbody>
</table>

