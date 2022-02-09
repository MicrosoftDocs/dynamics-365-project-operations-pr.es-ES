---
title: Transiciones de estado en un subcontrato
description: Este tema explica las transiciones de estado en un subcontrato en Microsoft Dynamics 365 Project Operations a medida que se crea, ejecuta y cierra el subcontrato.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903530"
---
# <a name="state-transitions-on-a-subcontract"></a>Transiciones de estado en un subcontrato 

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este tema explica las transiciones de estado en un subcontrato en Microsoft Dynamics 365 Project Operations. Cada estado se representa como borrador, confirmado, cerrado o cancelado. La siguiente imagen representa las transiciones de estado.

![Modelo de estado de subcontratación](../media/SubconStates.png)  

La siguiente tabla proporciona una descripción de lo que representa cada estado en el ciclo de vida de un subcontrato en Project Operations.

| Valor | Description | Transiciones permitidas |
| --- | --- | --- |
| Borradores | Esto representa el estado inicial de un subcontrato. Las negociaciones con el proveedor están en curso. Las líneas y los precios están sujetos a modificaciones. Se puede utilizar un subcontrato en este estado para estimar y dotar de personal a los requisitos del proyecto para recursos y materiales. También se puede hacer referencia a tiempo, gastos y uso de material en un proyecto. Un subcontrato en este estado se puede editar y eliminar. | Confirmadas |
| Confirmadas | Esto representa la etapa de un subcontrato después de que se completan las negociaciones con el proveedor sobre los precios y los artículos de línea que se compran. Sin embargo, la entrega real de materiales y / o trabajo por parte de recursos subcontratados aún está en curso. Se puede utilizar un subcontrato en este estado para estimar y dotar de personal a los requisitos del proyecto para recursos y materiales. También se puede hacer referencia a tiempo, gastos y uso de material en un proyecto. Un subcontrato en este estado no se puede editar o eliminar. El botón **Cancelar** le permite cancelar un subcontrato confirmado. El botón **Reabrir** le permite reabrir el subcontrato para traerlo de vuelta a estado **Borrador**. Utilice el botón **Cerrar** para cerrar un subcontrato confirmado. | Cerradas <br> Cancelado <br> Borradores |
| Cerradas | Esto representa la etapa de un subcontrato cuando se completa la entrega real de materiales y / o el trabajo de los recursos subcontratados. Ya no se puede utilizar un subcontrato en este estado para estimar y dotar de personal a los requisitos del proyecto para recursos y materiales. Tampoco se puede hacer referencia a tiempo, gastos y uso de material en un proyecto. Un subcontrato en este estado no se puede editar o eliminar. | None |
| Cancelado | Esto representa la etapa de un subcontrato cuando ya no es necesaria la entrega real de materiales y / o el trabajo de los recursos subcontratados. Un subcontrato en este estado no se puede utilizar para estimar y dotar de personal a los requisitos del proyecto para los recursos y materiales, ni tampoco se puede hacer referencia al tiempo, los gastos y el uso de materiales en un proyecto. Un subcontrato en este estado no se puede editar o eliminar. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]