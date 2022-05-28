---
title: Datos reales
description: Este tema proporciona información sobre cómo trabajar con datos reales en Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581305"
---
# <a name="actuals"></a>Datos reales

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los datos reales representan el progreso financiero y de la programación revisado y aprobado en un proyecto. Se crean cuando se aprueban entradas de tiempo, gastos y uso de material, entradas de diario y facturas.

> [!IMPORTANT]
> Los datos reales no deben editarse ni eliminarse del sistema. De lo contrario, la integridad financiera y cualquier integración con otros sistemas financieros y contables podrían verse afectados negativamente. Microsoft Dynamics 365 Project Operations le permite revertir y reemplazar datos reales para editar datos reales en varios puntos del ciclo de vida del proceso de negocio de sus proyectos.

## <a name="recording-actuals-based-on-project-events"></a>Registro de datos reales basados en eventos de proyecto

Project Operations registra las transacciones financieras que ocurren durante el ciclo de vida de un proyecto como datos reales. La creación de datos reales en varios eventos del ciclo de vida varía, dependiendo de si el compromiso del proyecto usa el modelo de facturación de tiempo y materiales o el modelo de facturación de precio fijo, y de si está en la etapa de preventa o es un proyecto interno.

Los siguientes temas explican el impacto en la tabla Datos reales en varios eventos para diferentes variaciones:

- [Impacto de los valores reales en un compromiso de tiempo y materiales](ActualsonTM.md)
- [Impacto de los datos reales en una interacción de precio fijo](ActualonFP.md)
- [Impacto de los datos reales durante la etapa de preventa de un compromiso](ActualonPreSales.md)
- [Datos reales de impacto para un proyecto interno](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
