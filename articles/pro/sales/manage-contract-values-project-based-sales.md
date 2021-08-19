---
title: Información general de líneas de contrato basadas en proyectos
description: En este tema se proporciona información sobre el trabajo con líneas de contrato basadas en proyecto.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 7da8a7f898e6f0bb46d4cf6de65812e3aabb7416a2fdf2f9d9c8bad07e77cd85
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999067"
---
# <a name="project-based-contract-lines-overview"></a>Información general de líneas de contrato basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las líneas de contrato basadas en proyectos en Dynamics 365 Project Operations están diseñadas para contener los acuerdos de estimación y facturación para componentes específicos del trabajo del proyecto en un compromiso. La estructura de una línea de contrato basada en un proyecto se extiende para los escenarios de estimaciones y facturación de proyectos con los siguientes conceptos:

- Método de facturación
- Asignación de proyecto y tareas
- Clases de transacciones incluidas
- Límite a no exceder
- Configuración de imputabilidad
- Estimaciones utilizando detalles de línea de contrato
- Clientes de líneas de contrato

La siguiente tabla incluye los campos en la pestaña **General** de líneas de contrato basadas en proyectos que ayudan a establecer la base para un presupuesto detallado y desde cero y arreglos de facturación para el trabajo basado en proyectos.

| Campo | Descripción | Impacto posterior |
| --- | --- | --- |
| **Nombre** | Nombre de la línea de contrato. Esto identifica el componente discreto del contrato que se está estimando. Para un contrato de proyecto creado a partir de una cotización, este valor se copia de un valor correspondiente de la línea de cotización basada en el proyecto. | El nombre que se copia en la línea de factura del proyecto que se crea a partir de esta línea de contrato cuando se crea la factura. |
| **Método de facturación** | En un contrato de proyecto creado a partir de una cotización, este valor se copia de un campo correspondiente de la línea de cotización. Este es un conjunto de opciones que representa los dos principales modelos de contratación soportados por Project Operations:</br>- **Precio fijo**</br>- **Tiempo y material** | Según el método de facturación de la línea de contrato referenciada, se procesará la transacción real. Si la línea de contrato a la que hace referencia el real tiene un método de facturación de tiempo y material, se crean un costo y registros reales de ventas no facturadas. Si la línea de contrato a la que hace referencia el real tiene un método de facturación de precio fijo, solo se crea un costo real. |
| **Project** | Utilice este campo para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso. | Este valor se utilizará junto con **Tareas incluidas** y **Clases de transacciones incluidas** para resolver la referencia de la línea del contrato en un registro de línea valor real o estimado. |
| **Tareas incluidas** | Indica si esta línea de contrato incluye todas las tareas del proyecto para el proyecto seleccionado o solo un subconjunto de las tareas. Es un conjunto de opciones que puede tener los valores siguientes:</br>- **Todas las tareas de proyecto**</br>- **Solo tareas de proyecto seleccionadas**. Un valor en blanco en este campo equivale a seleccionar **Todas las tareas del proyecto**. | Si **Solo tareas seleccionadas** está seleccionado, puede seleccionar tareas específicas y asociarlas a esta línea de contrato en la pestaña **Configuración de facturación de tareas** en la página **Proyecto**. El valor se utiliza junto con las clases **Proyecto** y **Transacción incluida** para resolver la referencia de línea de contrato en un registro de línea real o estimado. |
| **Incluir tiempo** | Un valor **Sí**/**No** indica si las transacciones de tiempo o los costes de mano de obra en el proyecto seleccionado se incluirán en esta línea de contrato. El valor **No** indica que las transacciones de tiempo o el coste de mano de obra no se incluirán en esta línea de contrato. El valor **Sí** indica que lo harán. | Este valor se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado. |
| **Incluir gasto** | Un valor **Sí**/**No** indica si los costes por gastos en el proyecto seleccionado se incluirán en esta línea de contrato. El valor **No** indica que el coste de gastos no se incluirá en esta línea de contrato. El valor **Sí** indica que lo hará. | Este valor se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado. |
| **Incluir materiales** | Un valor **Sí**/**No** indica si los costes por material en el proyecto seleccionado se incluirán en esta línea de contrato. Un valor **No** indica que los costes por material no se incluirán en esta línea de contrato. El valor **Sí** indica que lo hará. | Este valor se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado. |
| **Incluir tarifa** | Un valor **Sí**/**No** indica si las tarifas en el proyecto seleccionado se incluirán en esta línea de contrato. El valor **No** indica que los honorarios no se incluirán en esta línea de contrato. El valor **Sí** indica que lo harán. | Este valor se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado. |
| **Importe contratado** | En una línea de contrato de precio fijo, este importe es el valor acordado que se facturará al cliente por todos los componentes de trabajo asociados con esta línea de contrato. En una línea de contrato de tiempo y material, este importe es un valor estimado de lo que se facturará al cliente por todos los componentes de trabajo asociados con esta línea de contrato. En un contrato de proyecto que se crea a partir de una cotización, este valor se copia de un campo correspondiente de la línea de cotización. Cuando una línea de contrato basada en proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del monto en los detalles de la línea de contrato. | Cuando la línea del contrato tiene detalles de línea, este valor se puede modificar cambiando los importes en los detalles de la línea. En una línea de contrato de precio fijo, este valor se utiliza para generar el monto antes de impuestos sobre los hitos de facturación periódica. |
| **Impuesto estimado** | El usuario puede editar este campo para ingresar el monto del impuesto estimado en la línea del contrato. Cuando una línea de contrato basada en proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del monto de impuestos en los detalles de la línea de contrato. | Cuando la línea del contrato tiene detalles de línea, este valor se puede modificar cambiando los importes de impuestos en los detalles de la línea. En una línea de contrato de precio fijo, este valor se utiliza para generar impuestos sobre los hitos de facturación periódica. |
| **Importe contratado después de impuestos** | Importe de la línea de contrato después de impuestos. Este campo es de solo lectura y se calcula como **Importe contratado + Impuestos**. | En una línea de contrato de precio fijo, este valor se utiliza para generar hitos de facturación periódica. |
| **Límite a no exceder** | El usuario puede editar este campo y solo está disponible en líneas de contrato basadas en proyectos que tienen el método de facturación establecido como tiempo y material. | El usuario puede editar este campo. Cuando un valor real de tiempo y material hace referencia a esta línea de contrato por tiempo y material, la cantidad en el real se evalúa contra el límite que no debe excederse en esta línea de contrato después de contabilizar los montos ya gastados y comprometidos. Esta evaluación se completa después de contabilizar los montos ya gastados y comprometidos. |
| **Presupuesto del cliente** | Este campo es editable y se copia de un campo correspondiente de la línea de cotización si el contrato se creó a partir de una oferta. | Este campo solo se utiliza para información y no tiene ningún significado posterior. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Reglas de validación para las opciones de la pestaña General de las líneas de contrato basadas en proyectos

Regla 1: si el campo **Tareas incluidas** está en blanco o establecido en **Todas las tareas del proyecto**, todas las tareas del proyecto están incluidas en la línea de contrato.

Regla 2: cuando el campo **Tareas incluidas** está en blanco o se establece explícitamente en **Todas las tareas del proyecto**, un proyecto y una determinada clase de transacción solo se pueden incluir en una línea de contrato basada en proyecto de un contrato.

Regla 3: cuando el campo **Tareas incluidas** está en blanco o se establece explícitamente en **Solo las tareas del proyecto seleccionadas**, un proyecto y una determinada clase de transacción se pueden incluir en varias líneas de contrato basadas en proyecto de un contrato.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contrato</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Línea de contrato</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
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
                    <strong>Incluir materiales</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>Válido/no válido</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Razón</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En blanco </p>
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
No válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracción de la regla n.º 2. El tiempo, los gastos, los materiales y las tarifas del proyecto P1 se incluyen en las líneas de contrato CL1 y CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En blanco </p>
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En blanco </p>
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
No válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracción de la regla n.º 2. El tiempo, los materiales y las tarifas del proyecto P1 se incluyen en las líneas de contrato CL1 y CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En blanco </p>
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En blanco </p>
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
El tiempo, los materiales y las tarifas del proyecto P1 se incluyen en CL1.
                </p>
                <ul>
                    <li>
El gasto del proyecto P1 se incluyen en CL2.
                    </li>
                </ul>
                <p>
No hay superposición en lo que se incluye en cada línea del contrato y, por lo tanto, es válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En blanco </p>
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
No válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracción de la regla n.º 2 </p>
                <p>
C1 incluye tiempo, materiales, gastos y tarifas en un subconjunto de tareas en el proyecto P1.
                </p>
                <p>
CL2 incluye tiempo, materiales, gastos y tarifas para todo el proyecto P1 y, por lo tanto, se superpone con lo que se incluye en C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
En blanco </p>
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Según la regla n.° 3 </p>
                <p>
C1 incluye tiempo, gastos, materiales y tarifas en un subconjunto de tareas en el proyecto P1.
                </p>
                <p>
CL2 incluye tiempo, gastos, materiales y tarifas para un subconjunto de tareas en el proyecto P1.
                </p>
                <p>
La única validación adicional se refiere al subconjunto de tareas en CL1 y es diferente del subconjunto de tareas en CL2 para garantizar que no haya superposiciones. Esto lo hace el sistema cuando se asocian tareas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
