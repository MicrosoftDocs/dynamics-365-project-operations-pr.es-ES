---
title: Vincular datos reales a registros originales
description: Este tema explica cómo vincular datos reales a los registros originales, como la entrada de tiempo, la entrada de gastos o los registros de uso de material.
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852610"
---
# <a name="link-actuals-to-original-records"></a>Vincular datos reales a registros originales

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


En Dynamics 365 Project Operations, una *transacción comercial* es un concepto abstracto que no se representan con una entidad. Sin embargo, algunos procesos y campos comunes de las entidades están diseñados para usar el concepto de las transacciones comerciales. A continuación se detallan las entidades que usan este concepto:

- Detalles de línea de oferta
- Detalles de línea de contrato
- Líneas de estimación
- Líneas de diario
- Datos reales

De estas entidades, **Detalles de línea de oferta**, **Detalles de línea de contrato** y **Líneas de estimación** se asignan a la fase de estimación en el ciclo de vida del proyecto. Las entidades **Líneas de diario** y **Datos reales** se asignan a la fase de ejecución en el ciclo de vida del proyecto.

Project Operations reconoce los registros de estas cinco entidades como transacciones comerciales. La única distinción es que los registros de las entidades asignadas a la fase de estimación se consideran previsiones financieras, mientras que los registros de las entidades que se asignan a la fase de ejecución se consideran hechos financieros que se han producido ya.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptos únicos para las transacciones comerciales
A continuación se detallan conceptos que son únicos para las transacciones comerciales:

- Tipo de transacción
- Clase de transacción
- Origen de la transacción
- Conexión de transacciones

### <a name="transaction-type"></a>Tipo de transacción

El Tipo de transacción representa el tiempo y el contexto del impacto financiero de un proyecto. Esto se representa mediante un conjunto de opciones que tiene los siguientes valores admitidos en Project Operations:

  - Coste
  - Contrato de proyecto
  - Ventas sin facturar
  - Ventas facturadas
  - Ventas entre organizaciones
  - Coste de unidad de dotación de recursos

### <a name="transaction-class"></a>Clase de transacción

La Clase de transacción representa los distintos tipos de costes en los que se incurre en los proyectos. Esto se representa mediante un conjunto de opciones que tiene los siguientes valores admitidos en Project Operations:

  - Tiempo
  - Gasto
  - Material
  - Tarifa
  - Hito
  - Impuestos

**Hito** suele utilizarse en la lógica de negocios para la facturación de precio fijo en Project Operations.

### <a name="transaction-origin"></a>Origen de la transacción

El **origen de la transacción** es una entidad que almacena el origen de cada transacción comercial. Cuando un proyecto se pone en marcha, cada transacción comercial dará lugar a otra transacción comercial que a su vez creará otra y así sucesivamente. La entidad de origen de la transacción está diseñada para almacenar datos sobre el origen de cada transacción para ayudar con los informes y la trazabilidad. 

### <a name="transaction-connection"></a>Conexión de transacciones

La **Conexión de transacciones** es una entidad que almacena la relación entre dos transacciones comerciales similares, como, por ejemplo, el coste y los datos reales relacionados con las ventas, o las reversiones de transacciones que se desencadenan con actividades de facturación, como, por ejemplo, la confirmación de facturas o las correcciones de facturas.

Juntas, las entidades **Origen de la transacción** y **Conexión de transacciones** le ayudan a mantener un seguimiento de las relaciones entre las transacciones comerciales y las acciones provocaron la creación de una transacción comercial específica.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Ejemplo: funcionamiento de la entidad Origen de la transacción con la entidad Conexión de transacciones

El siguiente ejemplo muestra el procesamiento típico de las entradas de tiempo en el ciclo de vida de proyectos de Project Operations.

> ![Procesamiento de entradas de tiempo en el ciclo de vida de Project Service](media/basic-guide-17.png)
 
1. Un envío de una entrada crea de dos líneas de diario: una línea para el coste y otra para las ventas sin facturar.
2. La aprobación puntual de la entrada de tiempo crea dos datos reales: uno para el coste y otro para las ventas sin facturar.
3. Cuando se crea una nueva factura de proyecto, la transacción de la línea de la factura se crea a partir de los datos reales de ventas sin facturar. 
4. Cuando se confirma la factura, se crean dos nuevos datos reales: una reversión de ventas sin facturar y un dato real de ventas sin facturar.

Cada uno de estos eventos crea un registro en las entidades **Origen de la transacción** y **Conexión de transacción**. Estos nuevos registros ayudan a crear un historial de relaciones entre los registros que se crean en la entrada de tiempo, la línea del diario, los datos reales y los detalles de la línea de la factura.

La siguiente tabla muestra los registros de la entidad **Origen de la transacción** para el flujo de trabajo precedente.

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

La siguiente tabla muestra los registros de la entidad **Conexión de la transacción** para el flujo de trabajo precedente.

| Evento                          | Transacción 1                 | Rol de transacción 1 | Tipo de transacción 1           | Transacción 2                | Rol de transacción 2 | Tipo de transacción 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Envío de la entrada de tiempo          | GUID de la línea de diario (ventas)     | Ventas sin facturar     | msdyn_journalline            | GUID de la línea de diario (coste)     | Costo               | msdyn_journalline  |
| Aprobación de tiempo                  | GUID de datos reales sin facturar (ventas)  | Ventas sin facturar     | msdyn_actual                 | GUID de datos reales de coste (coste)       | Costo               | msdyn_actual       |
| Creación de factura               | GUID de detalle de la línea de factura      | Ventas facturadas       | msdyn_invoicelinetransaction | GUID de datos reales de ventas sin facturar   | Ventas sin facturar     | msdyn_actual       |
| Confirmación de factura           | GUID de datos reales de reversión         | Reversión          | msdyn_actual                 | GUID de ventas sin facturar original | Original           | msdyn_actual       |
| GUID de ventas facturadas              | Ventas facturadas                  | msdyn_actual       | GUID de datos reales de ventas sin facturar   | Ventas sin facturar               | msdyn_actual       |                    |
| Corrección borrador de factura       | GUID de transacción de línea de factura | Reemplazo          | msdyn_invoicelinetransaction | GUID de ventas facturadas            | Original           | msdyn_actual       |
| Confirmar corrección de factura     | GUID de reversión de ventas facturadas    | Reversión          | msdyn_actual                 | GUID de ventas facturadas            | Original           | msdyn_actual       |
| GUID de datos reales de nuevas ventas sin facturar | Reemplazo                     | msdyn_actual       | GUID de ventas facturadas            | Original                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
