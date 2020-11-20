---
title: ¿Por qué no puedo eliminar registros de la entidad de datos reales?
description: En este tema se proporciona información sobre por qué no se pueden eliminar los registros de la entidad de datos reales.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127179"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>¿Por qué no puedo eliminar registros de la entidad de datos reales?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) no permite la eliminación de datos reales porque sirven de fuente de datos para las transacciones que tienen implicaciones financieras en los sistemas dependientes, como, por ejemplo, la contabilidad general. Si se pudiesen eliminar los datos reales, la integridad de las transacciones de informes financieros quedaría en entredicho. Para establecer una traza de auditoría, los clientes deben usar los diarios para crear transacciones de compensación.

