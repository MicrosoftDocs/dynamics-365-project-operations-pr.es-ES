---
title: Análisis de ofertas de proyecto
description: En este tema se proporciona información sobre el análisis de ofertas de proyecto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b50f419d2c13cff4914f4b589c8d7ad9099c8734834d75f8d17104d2db40049b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002847"
---
# <a name="analysis-of-project-quotes"></a>Análisis de ofertas de proyecto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analiza las ofertas de proyecto para estimar la rentabilidad. También analiza la alineación de la oferta con las expectativas del cliente en cuanto a la fecha de entrega, la fecha de finalización y el presupuesto.

## <a name="profitability-analysis"></a>Análisis de rentabilidad

Project Service Automation analiza la rentabilidad mediante el margen bruto y el margen bruto ajustado.

- Los márgenes brutos se calculan mediante la fórmula siguiente:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- El margen bruto ajustado se calcula mediante la fórmula siguiente:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Si los valores de margen bruto y de margen bruto ajustado difieren por un amplio margen, gran parte del trabajo de la oferta se clasificará como no imputable.

## <a name="analysis-of-customer-expectations"></a>Análisis de las expectativas del cliente

Puede analizar las ofertas y generar gráficos de expectativas del cliente acerca de la programación y el presupuesto si especifica valores para los siguientes campos:

- El campo **Fecha de entrega solicitada** en el encabezado de la oferta.
- El campo **Presupuesto del cliente** para cada línea de la oferta (para las líneas basadas en proyectos y las líneas basadas en productos).

El análisis de las expectativas del cliente acerca de la programación se realiza comparando la última fecha de finalización del detalle de la línea de la oferta con la fecha de entrega solicitada de todas las líneas de la oferta.

El análisis de las expectativas del cliente acerca del presupuesto se realiza comparando la suma del presupuesto del cliente total con el importe ofertado de todas las líneas de la oferta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]