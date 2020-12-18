---
title: Información general de Project Service Automation
description: Este tema proporciona información sobre la integración de Dynamics 365 Project Service Automation con la solución de integración de Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642474"
---
# <a name="project-service-automation-overview"></a>Información general de Project Service Automation

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

La solución de integración de Project Service Automation con Finance utiliza la característica de integración de datos para sincronizar datos entre instancias de Dynamics 365 Finance y Dynamics 365 Project Service Automation a través de Common Data Service. Las plantillas de integración que están disponibles con la función de integración de datos permiten el flujo de proyectos, contratos de proyecto, líneas de contrato de proyecto, hitos de línea de contrato de proyecto, tareas de proyecto, categorías de transacción de gastos, cálculos de horas y cálculos de gastos desde Project Service Automation hasta Finance.

> [!NOTE]
> - Si utiliza la versión 7.3.0, debe instalar KB 4074835. Entonces podrá integrar proyectos de precio fijo.
> - Si está utilizando la versión 7.3.0 y está transfiriendo transacciones de tarifas desde Project Service Automation, debe instalar KB 4345320 para incluir esas tarifas en la factura del proyecto.
> - Si utiliza la versión 8.0, podrá utilizar la integración de tareas, las categorías de transacciones de gastos, las estimaciones de horas, las estimaciones de gastos y el bloqueo de funciones.
> - Si está utilizando la versión 8.0.1 o posterior, podrá sincronizar los datos reales.

Antes de que pueda integrar Project Service Automation en Finance, debe configurar los parámetros de integración de Project Service Automation. Para más información, consulte [Parámetros de integración de Project Service Automation](PSA-parameters.md).

Esta solución de integración permite la sincronización directa en los siguientes escenarios:

- Mantenga los contratos del proyecto en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.
- Cree proyectos en los contratos en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.
- Mantenga las líneas de contratos del proyecto en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.
- Mantenga los hitos de las líneas de contratos del proyecto en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.
- Mantenga las tareas del proyecto en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.
- Mantenga los categorías de transacciones de gastos en Finance y sincronícelos directamente desde Finance a Project Service Automation.
- Cree cálculos de horas de proyectos en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.
- Cree cálculos de gastos de proyectos en Project Service Automation y sincronícelos directamente desde Project Service Automation a Finance.
- Cree datos reales de tiempo, gastos y tarifas del proyecto en Project Service Automation y cree transacciones del proyecto en el diario de integración de Project Service Automation para que se puedan registrar en Finance.

## <a name="data-synchronization"></a>Sincronización de datos

La siguiente ilustración muestra cómo se sincronizan los datos como parte de la integración entre Project Service Automation y Finance.

> [!NOTE]
> No todas las plantillas están disponibles actualmente. Las plantillas se publicarán a medida que se completen.

[![Integración de Project Service Automation con Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Requisitos del sistema para Finance

Para utilizar la solución de integración de Project Service Automation en Finance, debe instalar Enterprise Edition 7.3 con Platform update 12 o posterior.

## <a name="system-requirements-for-project-service-automation"></a>Requisitos del sistema para Project Service Automation

Para utilizar la solución de integración de Project Service Automation en Finance, debe instalar los siguientes componentes:

- Dynamics 365 Project Service Automation versión 9.0.0.0 o posterior
- Perspectiva de la solución de efectivo para Dynamics 365 Sales, versión 1.14.0.0 (v14) o posterior
- Solución de Project Service Automation para Finance para Dynamics 365 Project Service Automation, versión 1.0.0.0 o posterior

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instale la solución de integración de Project Service Automation con Finance en su instancia de Project Service Automation

Descargue la solución de integración de Project Service Automation con Finance de [Centro de descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) y siga las instrucciones que se incluyen con la solución.
