---
title: Cancelar una factura de proveedor de proyecto
description: Este artículo explica cómo cancelar una factura de proveedor de proyecto en Microsoft Dynamics 365 Project Operations y el impacto financiero de cancelar una factura de proveedor del proyecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261112"
---
# <a name="cancel-a-project-vendor-invoice"></a>Cancelar una factura de proveedor de proyecto

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Una vez que se confirma una factura de proveedor, no se puede editar ni eliminar. Si hubo un error en una factura de proveedor que se confirmó, puede usar la acción Cancelar para revertir el impacto de la factura de proveedor y crear una nueva factura de proveedor.

Cuando selecciona **Cancelar** en una factura de proveedor, se produce el siguiente comportamiento:

1. El estado de la factura de proveedor se actualiza a **Cancelado**.
2. La factura de proveedor cancelada y sus registros relacionados pasan a ser de solo lectura y no se pueden editar ni eliminar.
3. Se revierten todos los datos reales de coste que se crearon en función de las líneas de factura del proveedor como parte de la confirmación de la factura del proveedor.
4. Si algún dato real de coste se vinculó a las líneas de la factura del proveedor como parte del proceso de correspondencia, la confirmación de la factura del proveedor original los revirtió. Durante la cancelación de la factura del proveedor, esos costes reales se vuelven a crear. Los orígenes apuntan a las entradas de tiempo, gasto o uso de material.
5. Después de cancelar la factura del proveedor, puede volver a crear diarios de corrección, procesar recuperaciones de entrada de tiempo y cancelar la aprobación de los datos reales de tiempo, gasto o material originales.

> [!NOTE]
> Solo se pueden cancelar las facturas de proveedores confirmadas. Las facturas de proveedores en otros estados no se pueden cancelar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
