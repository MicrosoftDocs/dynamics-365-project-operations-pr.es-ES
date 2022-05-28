---
title: 'Orígenes de transacciones: vincular datos reales a su fuente'
description: Este tema explica cómo se utiliza el concepto de orígenes de transacciones para vincular los datos reales con los registros de origen originales, como la entrada de horas, la entrada de gastos o los registros de uso de materiales.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584847"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Orígenes de transacciones: vincular datos reales a su fuente

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los registros de origen de transacción se crean para vincular datos reales a su origen, como entradas de tiempo, entradas de gastos, registros de uso de materiales y facturas de proyectos.

El siguiente ejemplo muestra el procesamiento típico de las entradas de tiempo en el ciclo de vida de proyectos de Project Operations.

> ![Procesamiento de entradas de tiempo en Project Operations.](media/basic-guide-17.png)
 
1. El envío de una entrada de tiempo hace que se creen dos líneas de diario: una para el coste y otra para las ventas sin facturar.
2. La aprobación final de la entrada de tiempo desencadena que se creen dos datos reales: uno para el coste y otro para las ventas sin facturar.
3. Cuando el usuario crea una factura de proyecto, la transacción de la línea de la factura se crea a partir de los datos reales de ventas sin facturar.
4. Cuando se confirma la factura, se crean dos nuevos datos reales: una reversión de ventas sin facturar y un dato real de ventas sin facturar.

Cada evento de de este flujo de proceso de trabajo desencadena la creación de registros en las entidades Origen de la transacción para facilitar la trazabilidad de las relaciones entre estos registros que se crean en la entrada de tiempo, la línea de diario, el dato real y los detalles de la línea de factura.

La siguiente tabla muestra los registros de la entidad Origen de la transacción para el flujo de trabajo precedente.

| Evento                        | Origen                   | Tipo de origen                       | Transacción                       | Tipo de transacción         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Envío de la entrada de tiempo        | GUID del registro de entrada de tiempo   | Entrada de tiempo                        | GUID del registro de la línea de diario (coste)   | Línea del diario             |
| GUID del registro de entrada de tiempo       | Entrada de tiempo               | GUID del registro de la línea de diario (ventas)  | Línea del diario                      |                          |
| Aprobación de tiempo                | GUID del registro de la línea de diario | Línea del diario                      | GUID del registro de ventas sin facturar        | Real                   |
| GUID del registro de entrada de tiempo       | Entrada de tiempo               | GUID del registro de ventas sin facturar        | Real                            |                          |
| GUID del registro de la línea de diario     | Línea del diario             | GUID del registro de datos reales de coste           | Real                            |                          |
| GUID del registro de entrada de tiempo       | Entrada de tiempo               | GUID del registro de datos reales de coste           | Real                            |                          |
| Creación de factura             | GUID del registro de entrada de tiempo   | Entrada de tiempo                        | GUID de transacción de línea de factura     | Transacción de línea de factura |
| GUID del registro de la línea de diario     | Línea del diario             | GUID de transacción de línea de factura     | Transacción de línea de factura          |                          |
| Confirmación de factura         | GUID de línea de factura        | Línea de factura                      | GUID del registro de ventas facturadas          | Real                   |
| GUID de factura                 | Factura                  | GUID del registro de ventas facturadas          | Real                            |                          |
| GUID de detalle de la línea de factura     | Detalle de línea de factura      | GUID del registro de ventas facturadas          | Real                            |                          |
| GUID del registro de entrada de tiempo       | Entrada de tiempo               | GUID del registro de ventas facturadas          | Real                            |                          |
| GUID del registro de la línea de diario     | Línea del diario             | GUID del registro de ventas facturadas          | Real                            |                          |
| GUID del registro de entrada de tiempo       | Entrada de tiempo               | GUID de reversión de ventas sin facturar      | Real                            |                          |
| GUID del registro de la línea de diario     | Línea del diario             | GUID de reversión de ventas sin facturar      | Real                            |                          |
| Corrección borrador de factura     | GUID ILD antiguo             | Transacción de línea de factura          | GUID de ILD de corrección               | Transacción de línea de factura |
| GUID de IL antiguo                  | Línea de factura             | GUID de ILD de corrección               | Transacción de línea de factura          |                          |
| GUID de factura antiguo             | Factura                  | GUID de ILD de corrección               | Transacción de línea de factura          |                          |
| GUID del registro de entrada de tiempo       | Entrada de tiempo               | GUID de ILD de corrección               | Transacción de línea de factura          |                          |
| GUID del registro de la línea de diario     | Línea del diario             | GUID de ILD de corrección               | Transacción de línea de factura          |                          |
| Corrección de factura confirmada | GUID ILD antiguo             | Transacción de línea de factura          | GUID de datos reales de ventas facturadas revertidas | Real                   |
| GUID de IL antiguo                  | Línea de factura             | GUID de datos reales de ventas facturadas revertidas | Real                            |                          |
| GUID de factura antiguo             | Factura                  | GUID de datos reales de ventas facturadas revertidas | Real                            |                          |
| GUID del registro de entrada de tiempo       | Entrada de tiempo               | GUID de datos reales de ventas facturadas revertidas | Real                            |                          |
| GUID del registro de la línea de diario     | Línea del diario             | GUID de datos reales de ventas facturadas revertidas | Real                            |                          |
| GUID ILD antiguo                 | Transacción de línea de factura | GUID de datos reales de nuevas ventas sin facturar    | Real                            |                          |
| GUID de IL antiguo                  | Línea de factura             | GUID de datos reales de nuevas ventas sin facturar    | Real                            |                          |
| GUID de factura antiguo             | Factura                  | GUID de datos reales de nuevas ventas sin facturar    | Real                            |                          |
| GUID del registro de entrada de tiempo       | Entrada de tiempo               | GUID de datos reales de nuevas ventas sin facturar    | Real                            |                          |
| GUID del registro de la línea de diario     | Línea del diario             | GUID de datos reales de nuevas ventas sin facturar    | Real                            |                          |
| GUID de ILD de corrección          | Transacción de línea de factura | GUID de datos reales de nuevas ventas sin facturar    | Real                            |                          |
| GUID IL de corrección           | Línea de factura             | GUID de datos reales de nuevas ventas sin facturar    | Real                            |                          |
| GUID de factura de corrección      | Factura                  | GUID de datos reales de nuevas ventas sin facturar    | Real                            |                          |


La siguiente ilustración muestra los vínculos que se crean entre diferentes datos reales y sus orígenes, en diversos eventos, usando el ejemplo de entradas de tiempo en Project Operations.

> ![Cómo se vinculan los datos reales a los registros de origen en Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
