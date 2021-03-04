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
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148979"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="c031e-103">¿Por qué no puedo eliminar registros de la entidad de datos reales?</span><span class="sxs-lookup"><span data-stu-id="c031e-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c031e-104">Project Service Automation (PSA) no permite la eliminación de datos reales porque sirven de fuente de datos para las transacciones que tienen implicaciones financieras en los sistemas dependientes, como, por ejemplo, la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="c031e-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="c031e-105">Si se pudiesen eliminar los datos reales, la integridad de las transacciones de informes financieros quedaría en entredicho.</span><span class="sxs-lookup"><span data-stu-id="c031e-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="c031e-106">Para establecer una traza de auditoría, los clientes deben usar los diarios para crear transacciones de compensación.</span><span class="sxs-lookup"><span data-stu-id="c031e-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

