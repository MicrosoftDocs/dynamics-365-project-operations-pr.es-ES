---
title: Transiciones de estado en una factura de proveedor
description: Este artículo explica las transiciones de estado en una factura de proveedor en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934341"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transiciones de estado en una factura de proveedor

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este artículo explica las transiciones de estado en una factura de proveedor en Microsoft Dynamics 365 Project Operations. Se utilizan los siguientes estados: **Borrador**, **En revisión**, **Confirmado**, **En retención** y **Cancelado**.

Las siguientes ilustraciones muestran las transiciones de estado.

![Modelo de transición de estado en un subcontrato](../media/VI_State_Model.jpg)

La siguiente tabla explica lo que representa cada estado en el ciclo de vida de una factura de proveedor en Project Operations.

| Valor | Description | Transiciones permitidas |
| --- | --- | --- |
| Borradores | Este estado es el estado inicial de una factura de proveedor. Las líneas y los precios están sujetos a modificación. Las facturas de proveedor en este estado pueden editarse y eliminarse. | En proceso |
| En revisión | Este estado representa el estado de procesamiento de una factura de proveedor. Al menos una línea de factura de proveedor tiene un estado de verificación de **En curso**. | Confirmado, En retención |
| Confirmadas | Este estado representa la fase de una factura de proveedor en la que la aplicación ha creado costos reales para cada línea de factura de proveedor. Todos los datos reales de costo vinculados que coincidieron con las líneas de factura del proveedor se revirtieron y reemplazaron con los datos reales de costo de esas líneas de factura del proveedor. Las facturas de proveedor en este estado no pueden editarse ni eliminarse. Puede usar el botón **Cancelar** para cancelar una factura de proveedor confirmada. La acción Cancelar revierte el impacto de la acción Confirmar. | Cancelado |
| En espera | <p>Este estado representa una etapa de una factura de proveedor en la que la factura de proveedor no se puede mover debido a un problema con la factura o el estado del proveedor. Las facturas de proveedor en este estado no pueden confirmarse, cancelarse, editarse ni eliminarse.</p><p>Puede utilizar la acción Reabrir para mover la factura de proveedor al estado **Borrador** o **En revisión**. Si al menos una línea de la factura de proveedor tiene un estado de verificación de **En curso** o **Completado**, la factura de proveedor se volverá a abrir en el estaado **En revisión**. Si todas las líneas de la factura de proveedor tienen un estado de verificación de **No empezado**, la factura de proveedor se volverá a abrir en estado **Borrador**.</p> | Borrador, En revisión |
| Cancelado | Este estado representa la etapa de un subcontrato cuando ya no es necesaria la entrega real de materiales y/o el trabajo de los recursos subcontratados. Un subcontrato en este estado no se puede utilizar para estimar y dotar de personal a los requisitos del proyecto para los recursos y materiales, ni tampoco se puede hacer referencia al tiempo, los gastos y el uso de materiales en un proyecto. Un subcontrato en este estado no se puede editar ni eliminar. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
