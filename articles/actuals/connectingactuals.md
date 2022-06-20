---
title: 'Conexiones de transacciones: vinculan datos reales de diferentes tipos de transacciones'
description: Este artículo explica cómo se utiliza una conexión de transacción para vincular datos reales de diferentes tipos para ayudar a realizar un seguimiento de la rentabilidad, la acumulación de facturación y los cálculos de ingresos facturados versus no facturados.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926107"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Conexiones de transacciones: vinculan datos reales de diferentes tipos de transacciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los registros de conexión de transacciones se crean para vincular datos reales de diferentes tipos a medida que el tiempo, el gasto o el uso de materiales se mueven en su ciclo de vida desde la etapa de oferta o preventa a la etapa de contrato, aprobaciones y/o retiros, facturación y, potencialmente, crédito o facturación correctiva.

El siguiente ejemplo muestra el procesamiento típico de las entradas de tiempo en el ciclo de vida de proyectos de Project Operations.

> ![Procesamiento de entradas de tiempo en Project Operations.](media/basic-guide-17.png)

El procesamiento de las entradas de tiempo en el ciclo de vida de Project Operations sigue estos pasos: 

1. El envío de una entrada de tiempo hace que se creen dos líneas de diario: una para el coste y otra para las ventas sin facturar. 
2. La aprobación final de la entrada de tiempo desencadena que se creen dos datos reales: uno para el coste y otro para las ventas sin facturar. Estos 2 datos reales están vinculados mediante conexiones de transacción.
3. Cuando el usuario crea una factura de proyecto, la transacción de la línea de la factura se crea a partir de los datos reales de ventas sin facturar.
4. Cuando se confirma la factura, esto crea dos nuevos datos reales: una reversión de ventas sin facturar y un dato real de ventas sin facturar. La reversión de ventas no facturadas y las ventas reales no facturadas originales se conectan mediante conexiones de transacciones de reversión. Las ventas facturadas y los datos reales de ventas no facturadas originales también están conectados para mostrar los vínculos entre lo que antes eran ingresos por trabajo pendiente o trabajo en curso (WIP) y lo que ahora son ingresos facturados.   

Cada evento en el flujo de trabajo de procesamiento desencadena la creación de registros en la tabla **Conexión de transacción**. Esto ayuda a crear un seguimiento de relaciones entre los registros que se crean en los detalles de entrada de tiempo, línea de diario, datos reales y línea de factura.

La siguiente tabla muestra los registros de la entidad **Conexión de transacciones** para el flujo de trabajo precedente.

|Evento                   |Transacción 1                 |Rol de transacción 1 |Tipo de transacción 1       |Transacción 2          |Rol de transacción 2 |Tipo de transacción 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Envío de la entrada de tiempo   |GUID de la línea de diario (ventas)     |Ventas sin facturar |msdyn_journalline            |GUID de la línea de diario (coste)     |Costo            |msdyn_journalline  |
|Aprobación de tiempo           |GUID de datos reales sin facturar (ventas)  |Ventas sin facturar |msdyn_actual                 |GUID de datos reales de coste (coste)       |Costo            |msdyn_actual       |
|Creación de factura        |GUID de detalle de la línea de factura      |Ventas facturadas   |msdyn_invoicelinetransaction |GUID de datos reales de ventas sin facturar   |Ventas sin facturar  |msdyn_actual       |
|Confirmación de factura    |GUID de datos reales de reversión         |Reversión      |msdyn_actual                 |GUID de ventas sin facturar original |Original        |msdyn_actual       |
|                        |GUID de ventas facturadas             |Ventas facturadas   |msdyn_actual                 |GUID de datos reales de ventas sin facturar   |Ventas sin facturar  |msdyn_actual       |
|Corrección borrador de factura |GUID de transacción de línea de factura|Reemplazo      |msdyn_invoicelinetransaction |GUID de ventas facturadas            |Original        |msdyn_actual       |
|Confirmar corrección de factura|GUID de reversión de ventas facturadas  |Reversión      |msdyn_actual                 |GUID de ventas facturadas            |Original        |msdyn_actual       |
|                        |GUID de nuevas ventas sin facturar |Reemplazo            |msdyn_actual                 |GUID de ventas facturadas            |Original        |msdyn_actual       |


La siguiente ilustración muestra los vínculos que se crean entre diferentes tipos de datos reales en varios eventos usando el ejemplo de entradas de tiempo en Project Operations.

> ![Cómo se vinculan los datos reales de diferentes tipos entre sí en Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
