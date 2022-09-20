---
title: Confirmar facturas de proveedor de proyecto
description: Este artículo explica cómo confirmar una factura de proveedor de proyecto en Microsoft Dynamics 365 Project Operations y describe el impacto financiero de confirmar una factura de proveedor del proyecto.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475446"
---
# <a name="confirm-project-vendor-invoices"></a>Confirmar facturas de proveedor de proyecto

**Se aplica a**: Project Operations para escenarios basados en recursos/no mantenidos en existencias

Cuando el parámetro **Se requiere confirmación manual del PM** está habilitado, las facturas de proveedor que se crean en Microsoft Dataverse tienen el estado **Borrador**. Las facturas de proveedor que se crean de esta manera deben revisarse y confirmarse manualmente. Cuando el parámetro **Se requiere confirmación manual del PM** está deshabilitado, las facturas de proveedor que se crean en Dataverse se confirman automáticamente. No tiene que hacer nada más. 

Después de haber verificado todas las líneas en una factura de proveedor en Dynamics 365 Project Operations, seleccione **Confirmar** para confirmar la factura del proveedor.

Cuando selecciona **Confirmar** en una factura de proveedor, se produce el siguiente comportamiento:

1. El estado de la factura de proveedor se actualiza a **Confirmado**.
1. La factura de proveedor confirmada y sus registros relacionados pasan a ser de solo lectura y no se pueden editar ni eliminar.
1. Si cualquier dato real de costo hace referencia a la línea de factura del proveedor como parte del proceso de coincidencia, todos los datos reales de coste que están asociados con la línea de factura del proveedor a la que se hace referencia se revierten.
1. Los nuevos costes reales se crean utilizando la información de la línea de factura del proveedor.
1. Ya no puede volver a crear diarios de corrección, procesar recuperaciones de entrada de tiempo ni cancelar la aprobación de los datos reales de tiempo, gasto o material originales que se revirtieron.
1. En Dynamics 365 Finance, el valor de **Coste del proyecto** se actualiza utilizando el diario de integración del proyecto, y la cuenta de integración de adquisición se *revierte* después de contabilizar el diario de integración del proyecto.

> [!NOTE]
> Si cualquier línea de una factura de proveedor tiene un estado de verificación distinto de **Completo**, la factura del proveedor no se puede confirmar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
