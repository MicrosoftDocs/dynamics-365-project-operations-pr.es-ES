---
title: Administración de subcontratos en Project Operations
description: Este tema proporciona una descripción general del proceso de gestión de subcontratos de un extremo a otro en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994252"
---
# <a name="subcontract-management-in-project-operations"></a>Administración de subcontratos en Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

La subcontratación en Microsoft Dynamics 365 Project Operations admite el siguiente flujo de proceso de negocio.

![Flujo del proceso de subcontratación](../media/SubcontractingProcessFlow.png)

A continuación se describe paso a paso el proceso de subcontratación.

1. El administrador del proyecto crea un subcontrato con un proveedor. De forma predeterminada, las listas de precios que se adjuntan al registro de proveedor se usan para el subcontrato. La cuenta de proveedor tiene un tipo de relación de **Proveedor** o **Distribuidor**.
2. El administrador del proyecto puede desglosar todas las compras como elementos de línea en el subcontrato. Las líneas del subcontrato pueden ser por tiempo, gastos o productos. La clase de transacción que se selecciona en cada línea de subcontrato determina para qué es la línea.
3. El administrador de cuentas del proveedor y el administrador del proyecto pueden iterar sobre el subcontrato. Los precios se pueden ajustar en las listas de precios de compra que estén asociadas al subcontrato.
4. En este punto o más adelante en el proceso, si la línea de subcontrato es por tiempo, el administrador de cuentas del proveedor asocia los contactos con cada línea de subcontrato. Esta asociación proporciona información al administrador del proyecto que está trabajando en el subcontrato. Cuando un contacto está asociado con una línea de subcontrato, el sistema crea automáticamente un recurso que se puede reservar desde el contacto, si aún no existe un recurso que se puede reservar.
5. El método de facturación en cada línea de subcontrato puede ser **Precio fijo** o **Tiempo y material**. Para las líneas de subcontratos de precio fijo, puede configurar un programa de facturación basado en hitos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
