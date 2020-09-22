---
title: ¿Por qué no puedo eliminar registros de la entidad de datos reales?
description: En este tema se proporciona información sobre por qué no se pueden eliminar los registros de la entidad de datos reales.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755959"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="a42cf-103">¿Por qué no puedo eliminar registros de la entidad de datos reales?</span><span class="sxs-lookup"><span data-stu-id="a42cf-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a42cf-104">Project Service Automation (PSA) no permite la eliminación de datos reales porque sirven de fuente de datos para las transacciones que tienen implicaciones financieras en los sistemas dependientes, como, por ejemplo, la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="a42cf-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="a42cf-105">Si se pudiesen eliminar los datos reales, la integridad de las transacciones de informes financieros quedaría en entredicho.</span><span class="sxs-lookup"><span data-stu-id="a42cf-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="a42cf-106">Para establecer una traza de auditoría, los clientes deben usar los diarios para crear transacciones de compensación.</span><span class="sxs-lookup"><span data-stu-id="a42cf-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

