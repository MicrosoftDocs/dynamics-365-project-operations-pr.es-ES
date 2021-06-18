---
title: Integración de doble escritura de Project Operations
description: Este tema proporciona una descripción general de la integración de doble escritura de Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998702"
---
# <a name="project-operations-dual-write-integration-overview"></a>Descripción general de la integración de doble escritura de Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Project Operations usa [capacidades de doble escritura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar datos en Microsoft Dataverse y Dynamics 365 Finance.

La siguiente ilustración muestra cómo se sincronizan los datos como parte de esta integración entre Dataverse y Finance.

![Descripción general de los flujos de datos de Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations en Dataverse proporciona una interfaz de usuario (UI) moderna y extensibilidad fácil sin código o con poco código usando capacidades de Power Platform. Los jefes de proyecto, jefes de recursos, miembros del equipo de proyecto y otras personas de la oficina principal realizan sus actividades en Project Operations en Dataverse.

Project Operations en Finance proporciona compatibilidad de reconocimiento de ingresos y contabilidad de proyectos. Project Operations se conecta al marco financiero en Finance para el cálculo de impuestos sobre las ventas, tipos de cambio de divisas, informes de dimensión financiera y más. Las experiencias de los contables de proyectos se basan principalmente en Finance.

La integración de Project Operations consiste en la siguiente integración de componentes:


- [Integración de datos de instalación y configuración de Project Operations](resource-dual-write-setup-integration.md) 
- [Estimaciones y datos reales del proyecto](resource-dual-write-estimates-actuals.md)
- [Facturas de proyecto](resource-dual-write-project-invoice.md)
- [Gestión de gastos](resource-dual-write-expense.md)
- [Factura del proveedor](resource-dual-write-vendor-invoice.md)
