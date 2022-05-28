---
title: Trabajar con líneas de contrato basadas en proyecto
description: En este tema se proporciona información sobre las líneas de contrato basadas en proyecto.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f67c0447c0b2a23d6f7d03dfc5ac7800943bbf36
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595197"
---
# <a name="work-with-projectbased-contract-lines"></a>Trabajar con líneas de contrato basadas en proyecto

Las líneas de contrato basadas en proyectos en Dynamics 365 Project Operations están diseñadas para contener los acuerdos de estimación y facturación para componentes específicos del trabajo del proyecto en un compromiso. La estructura de una línea de contrato basada en un proyecto se extiende para los escenarios de estimaciones y facturación de proyectos con los siguientes conceptos:

- Método de facturación
- Asignación de proyecto y tareas
- Clases de transacciones incluidas
- Límite a no exceder
- Configuración de imputabilidad
- Estimaciones utilizando detalles de línea de contrato
- Clientes de líneas de contrato

Los siguientes campos se incluyen en la pestaña **General** de líneas de contrato basadas en proyectos. Estos campos ayudan a sentar las bases para una estimación inicial detallada y los arreglos de facturación para el trabajo basado en proyectos.

| Campo | Descripción | Impacto posterior |
| --- | --- | --- |
| **Nombre** | El nombre de la línea del contrato que identifica el componente discreto del contrato que se está estimando. Para un contrato de proyecto creado a partir de una cotización, este valor se copia de un valor correspondiente de la línea de cotización basada en el proyecto. | Este valor de campo se copia en la línea de factura del proyecto que se crea a partir de esta línea de contrato cuando se crea la factura. |
| **Método de facturación** | En un contrato de proyecto creado a partir de una cotización, este valor se copia de un campo correspondiente de la línea de cotización. Este es un conjunto de opciones que representa los dos principales modelos de contratación soportados por Project Operations:</br>- **Precio fijo**</br>- **Tiempo y material** | Según el método de facturación de la línea de contrato referenciada, se procesará la transacción real. Si la línea de contrato a la que hace referencia el real tiene un método de facturación de tiempo y material, se crean un costo y un registro real de ventas no facturadas. Si la línea de contrato a la que hace referencia el real tiene un método de facturación de precio fijo, solo se crea un costo real. |
| **Project** | Utilice este campo para identificar el proyecto que se utilizará para entregar el trabajo en este compromiso. | El valor de este campo se utiliza junto con los campos **Tareas incluidas** y **Clases de transacciones incluidas** para resolver la referencia de línea de contrato en un registro de línea real o estimado. |
| **Incluir tiempo** | Una bandera indica si las transacciones de tiempo o los costos laborales en el proyecto seleccionado se incluyen en esta línea de contrato. El valor **No** indica que las transacciones de tiempo o los costos laborales no se incluirán en esta línea de contrato. El valor **Sí** indica que lo harán. | Este valor de campo se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado. |
| **Incluir gasto** | Una bandera indica si los costes de gastos del proyecto seleccionado se incluyen en esta línea de contrato. El valor **No** indica que el coste de gastos no se incluirá en esta línea de contrato. El valor **Sí** indica que lo hará. | Este valor de campo se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado. |
| **Incluir tarifa** | Una bandera indica si los honorarios del proyecto seleccionado se incluyen en esta línea de contrato. El valor **No** indica que los honorarios no se incluirán en esta línea de contrato. El valor **Sí** indica que lo harán. | Este valor de campo se utiliza junto con el proyecto para resolver la referencia de la línea del contrato en un registro de línea real o estimado. |
| **Importe contratado** | En una línea de contrato de precio fijo, este es el valor acordado que se facturará al cliente por todos los componentes de trabajo asociados con esta línea de contrato. En una línea de contrato de tiempo y material, este importe es un valor estimado de lo que se facturará al cliente por todos los componentes de trabajo asociados con esta línea de contrato. En un contrato de proyecto que se crea a partir de una cotización, este valor se copia de un campo correspondiente de la línea de cotización. Cuando una línea de contrato basada en proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del monto en los detalles de la línea de contrato. | Cuando la línea del contrato tiene detalles de línea, este valor se puede modificar cambiando los importes en los detalles de la línea. En una línea de contrato de precio fijo, este valor se utiliza para generar el monto antes de impuestos sobre los hitos de facturación periódica. |
| **Impuesto estimado** | El usuario puede editar este campo para ingresar el monto del impuesto estimado en la línea del contrato. Cuando una línea de contrato basada en proyecto tiene detalles de línea, este campo se bloquea para su edición y se resume a partir del monto de impuestos en los detalles de la línea de contrato. | Cuando la línea del contrato tiene detalles de línea, este valor se puede modificar cambiando los importes de impuestos en los detalles de la línea. En una línea de contrato de precio fijo, este valor se utiliza para generar impuestos sobre los hitos de facturación periódica. |
| **Importe contratado después de impuestos** | Importe de la línea de contrato después de impuestos. Este campo es de solo lectura y se calcula como **Importe contratado + Impuestos**. | En una línea de contrato de precio fijo, este valor se utiliza para generar hitos de facturación periódica. |
| **Límite a no exceder** | El usuario puede editar este campo y solo está disponible en líneas de contrato basadas en proyectos que tienen un método de facturación de tiempo y material. | El usuario puede editar este campo. Cuando un tiempo o gasto real hace referencia a esta línea de contrato por tiempo y material, la cantidad en el real se evalúa contra el límite que no debe excederse en esta línea de contrato después de contabilizar los montos ya gastados y comprometidos. |
| **Presupuesto del cliente** | Este campo es editable y se copia de un campo correspondiente de la línea de cotización, si el contrato se creó a partir de una oferta. | Este campo solo se utiliza para información y no tiene ningún significado posterior. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regla de validación para las opciones de la pestaña General de las líneas de contrato basadas en proyectos

Regla: un proyecto y una determinada clase de transacción solo se pueden incluir en una línea de contrato basada en proyecto en un contrato.

| Contrato | Línea de contrato | Project | Incluir tiempo | Incluir gasto | Incluir tarifa | Válido/no válido | Motivo                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Sí          | Sí             | Sí         | No válido       | Viola la regla. El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en ambas líneas de contrato, CL1 y CL2.                                                                                       |
| C1       | CL2           | P1      | Sí          | Sí             | Sí         | No válido       | Viola la regla. El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en ambas líneas de contrato, CL1 y CL2.                                                                                       |
| C1       | CL1           | P1      | Sí          | No              | Sí         | No válido       | Viola la regla. El tiempo y las tarifas del proyecto P1 se incluyen en ambas líneas de contrato, CL1 y CL2.                                                                                                   |
| C1       | CL2           | P1      | Sí          | Sí             | Sí         | No válido       | Viola la regla. El tiempo y las tarifas del proyecto P1 se incluyen en ambas líneas de contrato, CL1 y CL2.                                                                                                   |
| C1       | CL1           | P1      | Sí          | No              | Sí         | Válido           | El tiempo y las tarifas del proyecto P1 se incluyen en el CL1. El gasto del proyecto P1 se incluyen en CL2. </br>   No hay superposición en lo que se incluye en cada línea de contrato y, por lo tanto, es válido.  |
| C1       | CL2           | P1      | No           | Sí             | No          | Válido           | El tiempo y las tarifas del proyecto P1 se incluyen en el CL1. El gasto del proyecto P1 se incluyen en CL2. </br>   No hay superposición en lo que se incluye en cada línea de contrato y, por lo tanto, es válido.  |
| C1       | CL1           | P1      | Sí          | Sí             | Sí         | No válido       | Viola la regla. El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en las líneas de dos contratos.                                                                                               |
| CL2      | CL2           | P1      | Sí          | Sí             | Sí         | No válido       | Viola la regla. El tiempo, los gastos y las tarifas del proyecto P1 se incluyen en las líneas de dos contratos.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]