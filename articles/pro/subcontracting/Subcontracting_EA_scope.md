---
title: Subcontratación en la versión de acceso anticipado de octubre de 2021
description: Este tema proporciona una descripción general de las capacidades de subcontratación en Project Operations que forman parte de la versión de acceso anticipado de octubre de 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383716"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Subcontratación en la versión de acceso anticipado de octubre de 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este tema proporciona una descripción general de las capacidades de subcontratación en Dynamics 365 Project Operations que forman parte de la versión de acceso anticipado de octubre de 2021. Este conjunto de características no está listo para entornos de producción o activos, por lo que estas características permanecerán en la versión de acceso anticipado hasta que se publique el conjunto completo de características. Recomendamos encarecidamente que no utilice el conjunto de funciones de subcontratación para escenarios de producción activos hasta que se elimine el banner de versión preliminar. 

La siguiente lista proporciona un resumen de lo que está disponible actualmente en las versiones de acceso anticipado de octubre de 2021:

1. El administrador del proyecto crea un subcontrato con un proveedor. De forma predeterminada, las listas de precios que se adjuntan al registro de proveedor se usan para el subcontrato. La cuenta de proveedor tiene un tipo de relación de **Proveedor** o **Distribuidor**.

2. El administrador del proyecto puede desglosar todas las compras como elementos de línea en el subcontrato. Las líneas del subcontrato pueden ser por tiempo, gastos o productos. La clase de transacción de la línea de subcontrato determina para qué es la línea.

3. El administrador de cuentas del proveedor y el administrador del proyecto pueden iterar sobre el subcontrato. Los precios se pueden ajustar en las listas de precios de compra que estén asociadas al subcontrato.

4. En este punto o más adelante en el proceso, si la línea de subcontrato es por tiempo, el administrador de cuentas del proveedor asocia los contactos del proveedor con cada línea de subcontrato. Esta asociación proporciona información al administrador del proyecto que está trabajando en el subcontrato. Cuando un contacto de proveedor está asociado con una línea de subcontrato, el sistema crea automáticamente un recurso reservable desde el contacto, si aún no existe un recurso reservable.

5. El método de facturación en cada línea de subcontrato puede ser **Precio fijo** o **Tiempo y material**. Para las líneas de subcontratos de precio fijo, se configura un programa de facturación basado en hitos.

Los pasos restantes del flujo de proceso de negocio para subcontratación que se describen en la descripción general no están disponibles actualmente. A medida que se agreguen nuevas funciones, se actualizará este tema. 

La siguiente ilustración representa la versión de acceso anticipado de subcontratación, en contraste con el proceso empresarial completo.

![Flujo del proceso de subcontratación](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Versión de acceso anticipado de líneas de subcontrato basadas en cantidad y líneas de subcontrato basadas en trabajo
En la versión de acceso anticipado de octubre de 2021, solo se admiten las líneas de subcontrato basadas en cantidad. Esto significa que una línea de subcontrato se puede utilizar para comprar tiempo, gastos o materiales de un proveedor, pero no todo el trabajo. Esto también significa que la cantidad que se compra (unidades de tiempo, gastos o cantidad de materiales) en una línea de subcontrato se puede utilizar en cualquier proyecto del sistema.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
