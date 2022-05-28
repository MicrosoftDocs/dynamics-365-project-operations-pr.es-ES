---
title: Transacciones comerciales en Project Operations
description: Este tema proporciona una descripción general del concepto de transacciones comerciales en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582225"
---
# <a name="business-transactions-in-project-operations"></a>Transacciones comerciales en Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

En Microsoft Dynamics 365 Project Operations, una *transacción comercial* es un concepto abstracto que no se representa con ninguna entidad. Sin embargo, algunos procesos y campos comunes de las entidades están diseñados para usar el concepto de las transacciones comerciales. A continuación se detallan las entidades que usan esta abstracción:

- Detalles de línea de oferta
- Detalles de línea de contrato
- Líneas de estimación
- Líneas de diario
- Datos reales

De estas entidades, Detalles de línea de oferta, Detalles de línea de contrato y Líneas de estimación se asignan a la *fase de estimación* en el ciclo de vida del proyecto. Las entidades Líneas de diario y Datos reales se asignan a la *fase de ejecución* en el ciclo de vida del proyecto.

Project Operations trata los registros de todas estas cinco entidades como transacciones comerciales. La única distinción es que los registros de las entidades asignadas a la fase de estimación (Detalles de línea de oferta, Detalles de línea de contrato y Líneas de estimación) se consideran *previsiones financieras*, mientras que los registros de las entidades que se asignan a la fase de ejecución (Líneas de diario y datos reales) se consideran *hechos financieros* que se han producido ya.

Para obtener más información, consulte [Estimaciones](../project-management/estimating-projects-overview.md) y [Datos reales](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptos únicos para las transacciones comerciales

A continuación se detallan conceptos que son únicos para las transacciones comerciales:

- Tipo de transacción
- Clase de transacción
- Origen de la transacción
- Conexión de transacciones

### <a name="transaction-type"></a>Tipo de transacción

El Tipo de transacción representa el tiempo y el contexto del impacto financiero de un proyecto. Se define mediante un conjunto de opciones que tiene los siguientes valores admitidos en Project Operations:

- Coste
- Contrato de proyecto
- Ventas sin facturar
- Ventas facturadas
- Ventas entre organizaciones
- Coste de unidad de dotación de recursos

### <a name="transaction-class"></a>Clase de transacción

La Clase de transacción representa los distintos tipos de costes en los que se incurre en los proyectos. Se define mediante un conjunto de opciones que tiene los siguientes valores admitidos en Project Operations:

- Tiempo
- Gasto
- Material
- Precio
- Hito
- Impuestos

> [!NOTE]
> El valor **Hito** suele utilizarse en la lógica de negocios para la facturación de precio fijo en Project Operations.

### <a name="transaction-origin"></a>Origen de la transacción

El origen de la transacción es una entidad que almacena el origen de cada transacción comercial para ayudar con los informes y la trazabilidad. Cuando comienza la ejecución del proyecto, cada transacción comercial crea otra transacción comercial que, a su vez, creará otra transacción comercial, y así sucesivamente.

### <a name="transaction-connection"></a>Conexión de transacciones

La conexión de transacción es una entidad que almacena la relación entre dos transacciones comerciales similares, como, por ejemplo, el coste y los datos reales de ventas relacionados, o las reversiones de transacciones que se desencadenan mediante actividades de facturación, como, por ejemplo, la confirmación de facturas o las correcciones de facturas.

Juntas, las entidades Origen de la transacción y Conexión de transacción le ayudan a realizar un seguimiento de las relaciones entre las transacciones comerciales y las acciones que desencadenan la creación de una transacción comercial específica.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
