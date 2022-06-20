---
title: Cancelar una factura de proveedor de proyecto
description: Este artículo explica cómo cancelar una factura de proveedor de proyecto en Microsoft Dynamics 365 Project Operations y el impacto financiero de cancelar una factura de proveedor del proyecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911571"
---
# <a name="cancel-a-project-vendor-invoice"></a>Cancelar una factura de proveedor de proyecto

[!include [banner](../../includes/dataverse-preview.md)]

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
