---
title: Trabajo con el modelo de datos de Project Service Automation
description: En este tema se proporciona información sobre cómo trabajar con el modelo de datos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25f1af15c03001a92f96689ff36a3159a5352a46
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283254"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Trabajo con el modelo de datos de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation amplía otras entidades de la aplicación e introduce sus propias entidades en el modelo de datos de Common Data Service. En este tema se describen algunas de las entidades que encontrará en los escenarios de informes típicos de PSA.

## <a name="reporting-on-opportunities"></a>Informes sobre oportunidades

Project Service Automation amplía la entidad **Oportunidad** de Dynamics 365 Sales mediante la adición de campos que permiten escenarios basados en proyectos. Estos campos se identifican por un nombre del esquema que tiene el prefijo **msdyn\_**. Un nuevo campo que es importante para los informes sobre las oportunidades de PSA es **Tipo de pedido**. Una valor para **Basado en trabajo** para este campo indica que la oportunidad es una oportunidad de PSA. Entre otros campos que se han agregado a la entidad se incluyen **Organización contratante**, que captura la organización que tiene la oportunidad, y **Administrador de cuentas**, que captura el nombre del administrador de cuentas responsable de la oportunidad.

La entidad **Línea de oportunidad** también incluye campos relacionados con Project Service. **Método de facturación** indica si la línea de oportunidad se debe facturar por tiempo y materiales o por un precio fijo, y **Proyecto** captura el nombre del proyecto en el que se apoya la oportunidad. Existen otros campos que pueden ofrecer información sobre los costes de captura y los importes del presupuesto del cliente para el elemento de línea.

## <a name="reporting-on-quotes"></a>Informes sobre ofertas

PSA extiende la entidad **Oferta** de Ventas mediante la adición de campos relacionados con el proyecto. **Tipo de pedido** distingue las ofertas de PSA de las ofertas que no son de PSA. Una valor para **Basado en trabajo** para este campo indica que la oferta es una oferta de PSA. Otros campos que pueden ser relevantes para informar sobre las ofertas de PSA incluyen campos de importe, como **Costes imputables**, **Costes no imputables**, **Margen bruto**, **Estimaciones** y **Presupuesto**. Otros campos útiles indican si la oferta es rentable, si se completará a tiempo y si cumple con las expectativas de presupuesto del cliente.

PSA también extiende la entidad **Línea de oferta** de Ventas. Un campo que agrega PSA es **Método de facturación**, que indica cómo se facturará la línea de oferta (tiempo y materiales o precio fijo). Otros campos agregados a la entidad capturan el proyecto relacionado que sirve de apoyo para la línea de oferta, la facturación, el coste y el presupuesto.

PSA también agrega nuevas entidades relacionadas con ofertas al modelo de datos de Dynamics 365. A continuación, encontrará algunos ejemplos:

- **Detalle de línea de oferta**: esta entidad contiene los detalles de la estimación del proyecto de la línea de oferta. Tiene dos registros para cada línea de oferta. Un registro almacena el coste y los detalles del coste de la línea de oferta, y el otro registro almacena el importe y los detalles de ventas de la línea de oferta.
- **Programación de facturas de línea de oferta**: esta entidad contiene la programación de facturación de la línea de oferta. Esta programación se genera en función de la frecuencia de facturación asignada a la línea de oferta.
- **Hito de línea de oferta**: esta entidad contiene los hitos de facturación para las líneas de oferta de precio fijo.
- **Desglose de análisis de línea de oferta**: esta entidad contiene detalles financieros de la oferta de cotización. Estos detalles pueden ser útiles para informar de ventas ofertadas y los importes de los costes estimados por varias dimensiones.

Otras entidades que PSA se suma a las ofertas son **Lista de precios de proyecto de línea de oferta**, **Categoría de recursos de línea de oferta** y **Categoría de transacciones de línea de oferta**.

![Diagrama que muestra el presupuesto, la línea del presupuesto y relaciones del proyecto](media/PS-Reporting-image2.png "Diagrama que muestra el presupuesto, la línea del presupuesto y relaciones del proyecto")

## <a name="reporting-on-project-contracts"></a>Informe sobre contratos de proyectos

PSA amplía la entidad **Pedido** que se utiliza cuando se registran los contratos del proyecto. Agrega un nuevo campo importante, **Tipo de pedido**, que identifica el contrato como un contrato de proyecto de PSA en lugar de un pedido de ventas. Una valor para **Basado en trabajo** para este campo indica que el pedido es un contrato de proyecto de PSA. Otros campos nuevos que se agregan a la entidad **Pedido** capturan detalles sobre los costes, el estado del contrato de PSA y la organización propietaria del contrato.

PSA también amplía la entidad **Línea de pedido de ventas**. Entre los campos que agrega se encuentran los campos que capturan el método de facturación (tiempo y materiales o precio fijo), los importes del presupuesto del cliente y el proyecto subyacente.

PSA también agrega nuevas entidades que están diseñadas para contratos de proyectos. A continuación, encontrará algunos ejemplos:

- **Detalle de línea de contrato de proyecto**: esta entidad contiene los detalles de nivel de línea que se acumulan hasta el importe de la línea de contrato. Estos pueden ser tan detallados como las líneas de pedido que se generan a partir de una programación del proyecto a nivel de tarea.
- **Programación de facturas de línea de contrato**: esta entidad contiene la programación de facturación que se genera en función de la frecuencia de facturación asignada a la línea de contrato.
- **Hito de contrato**: esta entidad contiene los hitos de facturación para las líneas de contrato que tienen un plazo de facturación de precio fijo.

Otras entidades que PSA agrega a los contratos son **Lista de precios del proyecto de línea de contrato del proyecto**, **Categoría de recursos de línea de contrato de proyecto** y **Categoría de transacciones de línea de contrato de proyecto**.

![Diagrama que muestra el pedido, la línea de pedido y relaciones del proyecto](media/PS-Reporting-image3.png "Diagrama que muestra el pedido, la línea de pedido y relaciones del proyecto")

## <a name="reporting-on-projects"></a>Informe sobre proyectos

La entidad **Proyectos** y sus entidades relacionadas son exclusivas de PSA. **Proyecto** es la entidad de nivel superior que se utiliza para capturar el trabajo y el coste de las operaciones. Aquí se muestra una lista de las entidades relacionadas:

- **Miembro del equipo de proyecto**: esta entidad contiene detalles sobre los recursos que se pueden reservar asignados al proyecto. Esos recursos pueden ser recursos que se pueden reservar genéricos, o pueden denominarse recursos que se pueden reservar introducidos por el jefe de proyecto o generados a partir de la programación del proyecto.
- **Tarea de proyecto**: esta entidad contiene las tareas que componen el plan o la programación del proyecto.
- **Asignación de recursos**: esta entidad contiene la asignación de tareas para el recurso que se puede reservar.
- **Requisito de recursos**: esta entidad contiene los requisitos para cualquier miembro genérico del equipo de recursos.
- **Estimación** y **Línea de estimación**: estas entidades tienen una relación encabezado/línea y contienen estimaciones de gastos para el proyecto. Las estimaciones de tareas se almacenan en la entidad **Estimación de recursos**.

![Diagrama que muestra el requisito de recursos y las relaciones del proyecto](media/PS-Reporting-image4.png "Diagrama que muestra el requisito de recursos y las relaciones del proyecto")

## <a name="reporting-on-resources"></a>Informe sobre recursos

Los recursos del proyecto utilizan las entidades **Recurso que se puede reservar** de Universal Resource Scheduling (URS) que se comparten con otras aplicaciones, como Microsoft Dynamics 365 Field Service. Aquí se muestra una lista de las entidades que podría tener que usar al informar sobre los recursos del proyecto:

- **Recurso que se puede reservar**: esta entidad representa al usuario, contacto, recurso genérico, cuenta, grupo o equipamiento que se utiliza en el equipo del proyecto.
- **Características de los recursos que se pueden reservar**: esta entidad incluye las habilidades, certificaciones o educación del recurso. Las características pueden tener valores de calificación definidos por el modelo de calificación.
- **Categoría de recurso que se puede reservar**: esta entidad representa el rol del recurso que se puede reservar.
- **Reservas de recursos que se pueden reservar**: esta entidad representa el tiempo que se reserva en los proyectos para el recurso. Cada reserva tiene una entidad de encabezado y entidades de línea, y cada línea tiene un estado que representa el estado de la reserva.

![Diagrama que muestra las relaciones de las características de recursos que se pueden reservar](media/PS-Reporting-image5.png "Diagrama que muestra las relaciones de las características de recursos que se pueden reservar")

## <a name="reporting-on-actual-transactions"></a>Informe sobre transacciones reales

Cuando aprueba una hoja de tiempo o gasto, o factura un contrato en PSA, la transacción comercial se captura en la entidad **Real**. Esta entidad puede servir como base para casi todos los informes relacionados con las finanzas en PSA. La entidad **Real** captura el coste y las transacciones de ventas para el evento comercial. También captura muchos atributos relevantes.

Cuando trabaje con la entidad **Real**, es importante que comprenda qué transacción o transacciones se registran en la entidad y cuándo se registran las transacciones. Este es el flujo típico cuando trabaja con entradas de tiempo (el flujo para las entradas de gastos es similar):

1. Cuando se guarda la entrada de tiempo, no se crean registros en la entidad **Real**.
2. Cuando se envía la entrada de tiempo, no se crean registros en la entidad **Real**.
3. Cuando se aprueba la entrada de tiempo, se crea un registro en la entidad **Real** y también se puede crear un segundo registro. El primer registro almacena el coste de la entrada de tiempo. El segundo registro almacena el importe de ventas no facturadas de la entrada de tiempo. El segundo registro depende de que el proyecto tenga asignado un cliente, una oferta o una línea de contrato.

    | Fecha del documento | Tipo de transacción | Clase de transacción | Cliente         | Contrato   | Recurso     | Rol de recurso | Tipo de facturación | Cantidad | Precio unitario | Importe |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3/2/18        | Costo             | Time              | Alpine ski house | Alpine CRM | Carmen Linares | Jefe de proyecto   | Imputable   | 8.0      | 50,00      | 400,00 |
    | 3/2/18        | Ventas sin facturar   | Time              | Alpine ski house | Alpine CRM | Carmen Linares | Jefe de proyecto   | Imputable   | 8.0      | 100,00     | 800,00 |

    Estos dos registros son registros separados pero relacionados. No son ni débitos ni créditos.

4. Si se asocia un contrato con el proyecto, cuando se factura la entrada de tiempo, se crean dos registros más en la entidad **Real**. Primero, se crea una cantidad negativa para el registro de ventas sin facturar. Este registro revierte fundamentalmente la venta no facturada. En segundo lugar, se crea una transacción para la venta facturada. Una vez más, esos registros son registros separados, pero relacionados (no débitos y créditos).

    | Fecha del documento | Tipo de transacción | Clase de transacción | Cliente         | Contrato   | Recurso     | Rol de recurso | Tipo de facturación | Cantidad | Precio unitario | Importe   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4/2/18        | Ventas sin facturar   | Time              | Alpine ski house | Alpine CRM | Carmen Linares | Jefe de proyecto   | Imputable   | - 8,0    | 100,00     | - 800,00 |
    | 4/2/18        | Ventas facturadas     | Time              | Alpine ski house | Alpine CRM | Carmen Linares | Jefe de proyecto   | Imputable   | 8.0      | 100,00     | 800,00   |

La entidad **Origen de la transacción** registra el origen del registro **Real** y la entidad **Conexión de transacciones** registra los registros relacionados para el registro **Real**. Además, el registro **Real** contiene referencias del proyecto, el contrato del proyecto (pedido), el recurso que se puede reservar y el cliente.

![Diagrama que muestra la conexión de la transacción, el origen y las relaciones reales](media/PS-Reporting-image6.png "Diagrama que muestra la conexión de la transacción, el origen y las relaciones reales")


[!INCLUDE[footer-include](../includes/footer-banner.md)]