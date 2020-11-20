---
title: Información general sobre líneas de ofertas basadas en proyectos
description: Este tema proporciona información sobre el uso de líneas de oferta basadas en proyectos para trabajo de proyecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181878"
---
# <a name="project-based-quote-lines-overview"></a>Información general sobre líneas de ofertas basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las líneas de oferta basadas en proyectos están diseñadas para ayudar a estimar el trabajo del proyecto en un compromiso. La estructura de una línea de oferta basada en proyectos se amplía para las estimaciones de proyectos con los siguientes conceptos:

- Método de facturación
- Asignación de proyectos
- Clases de transacciones incluidas
- Límite a no exceder
- Configuración de imputabilidad
- Estimación utilizando los detalles de la línea de oferta
- Clientes de línea de oferta

La siguiente tabla proporciona información sobre los campos de la pestaña **General** de la línea de oferta basada en proyecto. Estos campos ayudan a establecer la base para una estimación detallada y desde cero para el trabajo del proyecto.

| **Campo** | **Descripción** | **Impacto posterior** |
| --- | --- | --- |
| Nombre | El nombre de la línea de oferta que debería ayudarle a identificar el componente discreto de la oferta que se está estimando. | Se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Método de facturación | En una oferta creada a partir de una oportunidad, este valor se copia del campo correspondiente en la línea de oportunidad. Este campo incluye los dos modelos de contratación principales admitidos por Dynamics 365 Project Operations:</br>- Precio fijo</br>- Tiempo y material.| Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Project | Utilice este campo opcional para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso. Cuando un proyecto se asigna a una línea de oferta, ayuda a configurar las tareas facturables y también a traer una estimación basada en el proyecto a la línea de oferta como detalles de la línea de oferta. Cuando un proyecto no está asignado a una línea de oferta basada en proyecto, la estimación debe crearse manualmente creando cada detalle de línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Incluir tiempo | Un indicador **Sí**/**No** indica si las transacciones de tiempo o los costes laborales del proyecto seleccionado se incluirán en la estimación de esta línea de oferta. Un valor **No** indica que las transacciones de tiempo o los costes laborales no se incluirán en la estimación de esta línea de oferta. Un valor **Sí** indica que las transacciones de tiempo o los costes laborales se incluirán en la estimación de esta línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Incluir gasto | Un indicador **Sí**/**No** indica si los costes de gastos del proyecto seleccionado se incluirán en la estimación de esta línea de oferta. Un valor **No** indica que el coste de gastos no se incluirá en la estimación de esta línea de oferta. Un valor **Sí** indica que el coste de gastos se incluirá en la estimación de esta línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Incluir tarifa | Un indicador **Sí**/**No** indica si las tarifas del proyecto seleccionado se incluirán en la estimación de esta línea de oferta. Un valor **No** indica que las tarifas no se incluirán en la estimación de esta línea de oferta. Un valor **No** indica que las tarifas se incluirán en la estimación de esta línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Importe de la oferta | Esta es la cantidad que se ofertará al cliente por todo el trabajo previsto en esta línea de oferta basada en el proyecto. En una oferta creada a partir de una oportunidad, este valor se copia del campo **Presupuesto del cliente** correspondiente en la línea de oportunidad. Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los detalles de la línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Impuesto estimado | Este es un campo editable para que el usuario agregue el importe del impuesto estimado en la línea de oferta. Cuando la línea de oferta basada en el proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del importe de los impuestos de los detalles de la línea de oferta. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Importe ofertado después de impuestos | Este campo es el importe de la línea de oferta después de impuestos y es de solo lectura. La cantidad de este campo se calcula como *Importe ofertado + Impuestos*. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Límite de No exceder | Este campo es editable y solo está disponible en líneas de oferta basadas en proyectos que tienen un método de facturación **Tiempo y material**. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |
| Presupuesto del cliente | Este campo es editable y se copia a partir del campo correspondiente de la línea de oportunidad si la oferta se creo a partir de una oportunidad. | Este valor de campo se copia en la línea de contrato del proyecto que se crea a partir de esta línea de oferta cuando se gana la oferta. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Reglas de validación para campos en la pestaña General de líneas de oferta basadas en proyectos

**Regla 1**: una determinada clase de transacción en el proyecto seleccionado solo se puede incluir en una línea de oferta basada en el proyecto de una oferta.

**Regla 2**: si una oportunidad tiene varias ofertas, puede haber líneas de oferta de ofertas diferentes que hagan referencia al mismo proyecto e incluyan la misma clase de transacción.

**Regla 3**: si las ofertas no pertenecen a la misma oportunidad, no pueden incluir el mismo proyecto y clase de transacción.

<table border="1" cellspacing="0" cellpadding="0">
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
                    <strong>tarifa</strong>
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
Infracción de la regla n.º 1. El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en ambas líneas de oferta, QL1 y QL2.
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
Infracción de la regla n.º 1. El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en ambas líneas de oferta, QL1 y QL2.
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
No hay superposición en lo que se incluye en cada línea de oferta, por lo que es válido.
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
Infracción de la regla n.º 1 anterior </p>
                <p>
Q1 incluye tiempo, gastos y tarifas para todo el proyecto P1.
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
Según la Regla n.° 2, Q1 y Q2 son dos ofertas de la misma oportunidad, por lo que ambas pueden estimar los mismos componentes de un proyecto.
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
QL1 en Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
Según la Regla n.° 3, Q1 y Q2 son dos ofertas de diferentes oportunidades, por lo que no pueden estimar los mismos componentes del mismo proyecto.
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

