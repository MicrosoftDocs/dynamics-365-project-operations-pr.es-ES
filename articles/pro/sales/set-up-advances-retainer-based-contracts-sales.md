---
title: Contratos basados en pagos a cuenta y anticipos (lite)
description: En este tema se proporciona información sobre modelos de contratos y adelantos basados en anticipos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180888"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Contratos basados en pagos a cuenta y anticipos (lite)


_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Dynamics 365 Project Operations admite contratos basados en anticipos. Un contrato basado en anticipos es un conjunto negociado de pagos igualmente distribuidos por los que se facturará al cliente durante la duración de un proyecto. Este tipo de contrato se usa típicamente para modelos de facturación basados en tiempo y material o consumo donde existe la necesidad de brindarle al cliente una factura predecible y un calendario de pago. Los ingresos reales acumulados en cada período se concilian con el pago recibido del cliente al comienzo del período. De acuerdo con el concepto del modelo de facturación de Tiempo y Material, los valores de los ingresos acumulados en cada período pueden variar con los costos incurridos. Si los ingresos acumulados superan la cantidad recibida al comienzo del período, la empresa de ejecución del proyecto podría:

- Facturar solo al cliente el exceso 
- Aplazar la conciliación de los ingresos hasta el próximo período de facturación y hacer una factura final al final del proyecto por cualquier ingreso restante no conciliado

La principal diferencia entre un modelo de contratación basado en anticipos y un modelo de contrato de precio fijo en Project Operations es que en el modelo de contrato de precio fijo, el monto de la factura no está vinculado ni vinculado a los costos incurridos. La facturación sigue un enfoque basado en hitos que está alineado con los costes incurridos durante ese período. En un contrato basado en anticipos, los ingresos que se pueden facturar se registran según el método de facturación en la línea del contrato. Cuando el método de facturación es por tiempo y material, los ingresos facturables están vinculados a los costes incurridos en un período determinado y pueden variar de un período a otro. Sin embargo, al cliente solo se le factura la cantidad del anticipo periódico. El sistema utiliza otra factura al final del período para conciliar los ingresos facturables registrados durante el período con el monto que se facturó al cliente al comienzo del período.

La ventaja de este método es que los costes del cliente se vuelven predecibles en el programa de retención a diferencia de un modelo típico de tiempo y material. La organización que entrega el proyecto también tiene cierto margen para cubrir el riesgo de recuperar los costes incurridos debido a cualquier aumento en el alcance que un modelo de precio fijo no les hubiera permitido.

Además de un programa periódico basado en anticipos, Project Operations puede registrar un anticipo único de un cliente y conciliarlo con los diferentes componentes de costes del proyecto.

El anticipo en Project Operations no está disponible para su uso hasta que se factura al cliente. Esto se indica mediante los siguientes campos en la subcuadrícula para anticipos y retenciones.

| Campo | Descripción | Impacto posterior |
| --- | --- | --- |
| Importe disponible | La cantidad que está disponible para ser utilizada en el anticipo o registro anticipado. | Hasta que se facture el anticipo o adelanto, no estará disponible para su uso, lo que significa que la cantidad disponible será cero. |
| Importe usado | La cantidad que ya se ha usado en la retención o anticipo. | Un anticipo o retención puede conciliarse parcialmente en una factura con los costes reales que tendrán una parte marcada como ya utilizada o consumida. El resto del anticipo o adelanto está disponible para conciliar en una factura futura con los costos reales. |
