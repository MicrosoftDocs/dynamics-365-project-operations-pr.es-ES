---
title: Impacto de los datos reales en una interacción de precio fijo
description: Este tema proporciona información sobre el impacto en la tabla de valores reales en varios eventos durante el ciclo de vida de un compromiso de precio fijo en Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579249"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Impacto de los datos reales en una interacción de precio fijo

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

La siguiente tabla enumera los datos reales de diferentes tipos de transacciones que se crean en varios eventos en un compromiso de precio fijo.

| Evento | Coste real | Dato real de ventas sin facturar | Dato real de ventas facturadas | Ejemplo |
|---|---|---|---|---|
| La hora se ha creado. | No aplicable | No aplicable | No aplicable | <p>Bob Kozack, de la unidad organizativa de Fabrikam US, que tiene una tarifa de coste de 100 dólares estadounidenses (100 USD) por hora, está trabajando en un proyecto denominado "Instalación de brazos en Adatum". Este proyecto está asignado a un método de facturación de precio fijo en la línea de contrato. Aquí hay una entrada de tiempo de muestra de Bob Kozak:</p><p>Bob Kozack: 8 horas</p> |
| El tiempo se envía. | No aplicable | No aplicable | No aplicable | Se crea una línea de diario de costes para la entrada de tiempo. La tasa de coste predeterminada se ingresa en el asiento de diario. |
| La entrada de tiempo se recupera antes de que se apruebe. | No aplicable | No aplicable | No aplicable | |
| Tiempo aprobado. | Se crea un dato real de coste. | No aplicable | No aplicable | <p>Nuevo dato real que se crea:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD</li></ul> |
| Se cancela la aprobación de tiempo. | <p>El estado de ajuste del dato real de coste original se actualiza a **Ajustado**.</p><p>Se crea un coste real de reversión que tiene un estado de ajuste de **No ajustable**.</p> | No aplicable | No aplicable | <p>Dato real existente que se actualiza:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir el impacto financiero anterior:</p><ul><li>**Coste real:** Bob Kozack, (8 horas), (800 USD), *No ajustable*</li></ul> |
| La entrada de tiempo se recupera después de que se apruebe. | <p>El estado de ajuste del dato real de coste original se actualiza a **Ajustado**.</p><p>Se crea un coste real de reversión que tiene un estado de ajuste de **No ajustable**.</p> | No aplicable | No aplicable | <p>Dato real existente que se actualiza:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir el impacto financiero anterior:</p><ul><li>**Coste real:** Bob Kozack, (8 horas), (800 USD), *No ajustable*</li></ul> |
| El contrato está confirmado. | <p>El estado de ajuste de los datos reales de coste original se actualiza a **Ajustado**.</p><p>Se crean datos reales de coste de reversión que tiene un estado de ajuste de **No ajustable**.</p><p>Los nuevos costes reales se crean después de reevaluar las reglas contractuales.</p> | No aplicable | No aplicable | <p>Dato real existente que se actualiza:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir el impacto financiero anterior:</p><ul><li>**Coste real:** Bob Kozack, (8 horas), (800 USD), *No ajustable*</li></ul><p>Nuevo dato real que se crea para el impacto financiero reevaluado:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD</li></ul> |
| Se crea una factura. | No aplicable | No aplicable | No aplicable | |
| La factura se confirma con un hito. | No aplicable | No aplicable | Se crean nuevos datos reales de ventas facturados basados en hitos. | <p>Dato real existente que permanece sin cambios:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD</li></ul><p>Nuevo dato real que se crea para registrar los valores de ventas facturados:</p><ul><li>**Datos reales de ventas facturadas:** Hito, 5000 USD</li></ul> |
| La factura se corrige para acreditar el hito. | No aplicable | No aplicable | Se crean datos reales de reversión de ventas facturadas. | <p>Dato real existente que permanece sin cambios:</p><ul><li>**Coste real:** Bob Kozack, 8 horas, 800 USD</li></ul><p>Dato real existente que se actualiza:</p><ul><li>**Datos reales de ventas facturadas:** Hito, 5000 USD, *Ajustado*</li></ul><p>Nuevo dato real que se crea para revertir los anteriores valores de ventas facturados:</p><ul><li>**Datos reales de ventas facturadas:** Hito, (5000 USD), *No ajustable*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
