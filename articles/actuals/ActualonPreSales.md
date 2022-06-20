---
title: Impacto de los datos reales durante la etapa de preventa de un compromiso
description: Este artículo proporciona información sobre el impacto en la tabla de valores reales en varios eventos cuando un compromiso está en etapa preventas de Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922381"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impacto de los datos reales durante la etapa de preventa de un compromiso

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

La siguiente tabla enumera los datos reales de diferentes tipos de transacciones que se crean en varios eventos durante la etapa preventas de un compromiso de proyecto.

| Evento | Coste real | Ejemplo |
|---|---|---|
| La hora se ha creado. | No aplicable | <p>Bob Kozack, de la unidad organizativa de Fabrikam US, que tiene una tarifa de coste de 100 dólares estadounidenses (100 USD) por hora, está trabajando en un proyecto denominado "Instalación de brazos en Adatum". Este proyecto está asignado a un método de facturación de precio fijo en la línea de contrato. Aquí hay una entrada de tiempo de muestra de Bob Kozak:</p><p>Bob Kozack: 8 horas</p> |
| El tiempo se envía. | No aplicable | Se crea una línea de diario de costes para la entrada de tiempo. La tasa de coste predeterminada se ingresa en el asiento de diario. |
| La entrada de tiempo se recupera antes de que se apruebe. | No aplicable | |
| Tiempo aprobado. | Se crea un dato real de coste. | <p>Nuevo dato real que se crea:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD</li></ul> |
| Se cancela la aprobación de tiempo. | <p>El estado de ajuste del dato real de coste original se actualiza a **Ajustado**.</p><p>Se crea un coste real de reversión que tiene un estado de ajuste de **No ajustable**.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir el impacto financiero anterior:</p><ul><li>**Coste real:** Bob Kozack, (8 horas), (800 USD), *No ajustable*</li></ul> |
| La entrada de tiempo se recupera después de que se apruebe. | <p>El estado de ajuste del dato real de coste original se actualiza a **Ajustado**.</p><p>Se crea un coste real de reversión que tiene un estado de ajuste de **No ajustable**.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir el impacto financiero anterior:</p><ul><li>**Coste real:** Bob Kozack, (8 horas), (800 USD), *No ajustable*</li></ul> |
| Se gana la oferta y se crea un contrato. | <p>El estado de ajuste de los datos reales de coste original se actualiza a **Ajustado**.</p><p>Se crean datos reales de coste de reversión que tiene un estado de ajuste de **No ajustable**.</p><p>Los nuevos costes reales se crean después de reevaluar las reglas contractuales.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir el impacto financiero anterior:</p><ul><li>**Coste real:** Bob Kozack, (8 horas), (800 USD), *No ajustable*</li></ul><p>Nuevos datos reales que se crean para el impacto financiero reevaluado cuando se gana la oferta y se crea el contrato:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD</li><li>**Ventas no facturadas reales:** Bob Kozack, 8 horas, 1600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
