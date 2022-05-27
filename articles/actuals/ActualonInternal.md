---
title: Datos reales de impacto para un proyecto interno
description: Este tema proporciona información sobre el impacto en la tabla de datos reales en varios eventos para un proyecto interno en Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579787"
---
# <a name="actuals-impact-for-an-internal-project"></a>Datos reales de impacto para un proyecto interno

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

La siguiente tabla enumera los datos reales de diferentes tipos de transacciones que se crean en varios eventos en un proyecto interno.

| Evento | Coste real | Ejemplo |
|---|---|---|
| La hora se ha creado. | No aplicable | <p>Bob Kozack, de la unidad organizativa de Fabrikam US, que tiene una tarifa de coste de 100 dólares estadounidenses (100 USD) por hora, está trabajando en un proyecto denominado "Instalación de brazos en Adatum". Este proyecto está asignado a un método de facturación de precio fijo en la línea de contrato. Aquí hay una entrada de tiempo de muestra de Bob Kozak:</p><p>Bob Kozack: 8 horas</p> |
| El tiempo se envía. | No aplicable | Se crea una línea de diario de costes para la entrada de tiempo. La tasa de coste predeterminada se ingresa en el asiento de diario. |
| La entrada de tiempo se recupera antes de que se apruebe. | No aplicable | |
| Tiempo aprobado. | Se crea un dato real de coste. | <p>Nuevo dato real que se crea:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD</li></ul> |
| Se cancela la aprobación de tiempo. | <p>El estado de ajuste del dato real de coste original se actualiza a **Ajustado**.</p><p>Se crea un coste real de reversión que tiene un estado de ajuste de **No ajustable**.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir el impacto financiero anterior:</p><ul><li>**Coste real:** Bob Kozack, (8 horas), (800 USD), *No ajustable*</li></ul> |
| La entrada de tiempo se recupera después de que se apruebe. | <p>El estado de ajuste del dato real de coste original se actualiza a **Ajustado**.</p><p>Se crea un coste real de reversión que tiene un estado de ajuste de **No ajustable**.</p> | <p>Dato real existente que se actualiza:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir el impacto financiero anterior:</p><ul><li>**Coste real:** Bob Kozack, (8 horas), (800 USD), *No ajustable*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
