---
title: ¿Por qué no puedo eliminar registros de la entidad de datos reales?
description: En este tema se proporciona información sobre por qué no se pueden eliminar los registros de la entidad de datos reales.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002892"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>¿Por qué no puedo eliminar registros de la entidad de datos reales?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) no permite la eliminación de datos reales porque sirven de fuente de datos para las transacciones que tienen implicaciones financieras en los sistemas dependientes, como, por ejemplo, la contabilidad general. Si se pudiesen eliminar los datos reales, la integridad de las transacciones de informes financieros quedaría en entredicho. Para establecer una traza de auditoría, los clientes deben usar los diarios para crear transacciones de compensación.



[!INCLUDE[footer-include](../includes/footer-banner.md)]