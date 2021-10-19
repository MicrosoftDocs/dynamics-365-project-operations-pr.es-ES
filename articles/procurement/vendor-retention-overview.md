---
title: Información general de retención de proveedores
description: Este tema proporciona una descripción general de las capacidades de retención de proveedores.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594631"
---
# <a name="vendor-retention-overview"></a>Información general de retención de proveedores

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Es posible que su organización desee retener una parte de los pagos a los proveedores que trabajan en proyectos para su organización. Por ejemplo, antes de pagarle a su proveedor, es posible que desee asegurarse de que los artículos y servicios que le brindan cumplan con sus expectativas.

Cuando negocia compras para proyectos con proveedores, puede especificar los términos de retención de proveedores que incluyen el porcentaje o el importe a retener. A medida que el proveedor entrega artículos y servicios, usted deduce el porcentaje o el importe de retención especificado de su pago al proveedor. Cuando el proyecto está completo o alcanza una etapa intermedia como se especifica en el contrato del proveedor, usted libera el importe retenido y crea un pago al proveedor.

## <a name="vendor-retention-example"></a>Ejemplo de retención de proveedores

El siguiente ejemplo muestra cómo se retiene un porcentaje del importe de la factura de un proveedor en función del porcentaje que está completo para un proyecto.

Contoso Robotics USA ha contratado al proveedor Fabrikam para proporcionar 100 horas de capacitación para el proyecto de renovación de equipos. El valor total del contrato es 30.000 USD con un precio de compra acordado de 300 USD por hora.

La formación se impartirá en tres fases con la siguiente programación:

- Fase 1: 50 horas, o el 50 por ciento del proyecto
- Fase 2: 30 horas, o el 80 por ciento del proyecto en total
- Fase 3: 20 horas, o el 100 por ciento del proyecto

La siguiente tabla enumera los términos de retención.

| **Porcentaje de unidades entregadas** | **Porcentaje a retener** | **Porcentaje a liberar** |
| --- | --- | --- |
| 50 % | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

Las transacciones dan como resultado los siguientes importes:

- Fase 1:
  - El importe a pagar es 50 x 300, o 15.000.
  - El 20 por ciento del importe, o 3.000, se retiene y se liberará en una etapa posterior.
  - El importe que se paga al proveedor es 12.000.
- Fase 2:
  - El importe a pagar es 30 x 300, o 9.000.
  - Se retiene el 10 por ciento del importe, o 900.
  - Se libera el 10 por ciento de los 3.000 que se retuvieron en la Fase 1, o 300.
  - El importe que se paga al proveedor es 8.400. Este importe es 9.000 menos la retención de 900 más los 300 que se liberaron de la retención de la Fase 1.
- Fase 3:
  - El importe a pagar es 20 x 300, o 6.000.
  - No se retiene ningún importe.
  - El importe que se libera es de 3.600. Este importe consiste en los 3.000 que se retuvieron en la Fase 1, menos los 300 de la Fase 1 que se liberaron en la Fase 2, más los 900 que se retuvieron en la Fase 2.
  - El importe que se paga al proveedor es 9.600. Este importe consiste en la cantidad retenida de 3.600 más los 6.000 para completar la Fase 3.

El importe total pagado al proveedor después de que se completen las tres fases es 30.000, que es el importe total del pedido de compra (15.000 + 9.000 + 6.000).
