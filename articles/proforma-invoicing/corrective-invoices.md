---
title: Facturas corregidas
description: En este tema se proporciona información sobre las facturas corregidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122409"
---
# <a name="corrected-invoices"></a>Facturas corregidas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las facturas confirmadas se pueden editar. Cuando se edita una factura confirmada, se crea un borrador de la factura corregida. Puesto que se da por sentado que desea revertir todas las transacciones y las cantidades de factura original, la factura corregida incluye todas las transacciones de la factura original y todas sus cantidades son iguales a cero (0).

Cuando las transacciones no requieren corrección, puede quitarlas del borrador de la factura correctiva. Para revertir o devolver solo una cantidad parcial, puede editar el campo Cantidad en el detalle de la línea. Si abre el detalle de la línea de factura, podrá ver la cantidad de la factura original. A continuación, podrá editar la cantidad de la factura actual para que sea superior o inferior a la cantidad de la factura original.

Cuando se confirma una factura correctiva, el dato real de ventas facturadas originales se revierte y se crea un nuevo dato real de ventas facturadas. Si la cantidad se redujo, la diferencia también generará un nuevo dato real de ventas sin facturar. Por ejemplo, si la venta facturada original ascendía a ocho horas y el detalle de línea de factura corregida tenía una cantidad reducida de seis horas, se revierte la línea de ventas facturadas originales y se crean dos nuevos datos reales:

- Un dato real de ventas facturadas por seis horas.
- Un dato real de ventas sin facturar por las dos horas restantes. Esta transacción se puede facturar más adelante o se puede marcar como no imputable, en función de las negociaciones con el cliente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]