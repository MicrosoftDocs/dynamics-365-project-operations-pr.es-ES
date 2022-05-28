---
title: Confirmar una factura de proveedor de proyecto
description: Este tema explica cómo confirmar una factura de proveedor de proyecto en Microsoft Dynamics 365 Project Operations y el impacto financiero de confirmar una factura de proveedor del proyecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595749"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmar una factura de proveedor de proyecto

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Después de haber verificado todas las líneas en una factura de proveedor en Microsoft Dynamics 365 Project Operations, puede utilizar la acción Confirmar para confirmar la factura del proveedor.

Cuando selecciona **Confirmar** en una factura de proveedor, se produce el siguiente comportamiento:

1. El estado de la factura de proveedor se actualiza a **Confirmado**.
2. La factura de proveedor confirmada y sus registros relacionados pasan a ser de solo lectura y no se pueden editar ni eliminar.
3. Si cualquier dato real de costo hace referencia a la línea de factura del proveedor como parte del proceso de coincidencia, todos los datos reales de coste que están asociados con la línea de factura del proveedor a la que se hace referencia se revierten.
4. Los nuevos costes reales se crean utilizando la información de la línea de factura del proveedor.
5. Después de confirmar la factura del proveedor, ya no puede volver a crear diarios de corrección, procesar recuperaciones de entrada de tiempo ni cancelar la aprobación de los datos reales de tiempo, gasto o material originales que se revirtieron.

> [!NOTE]
> Si cualquier línea de una factura de proveedor tiene un estado de verificación distinto de **Completo**, la factura del proveedor no se puede confirmar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
