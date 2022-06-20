---
title: Integración de doble escritura de Project Operations
description: Este artículo proporciona una descripción general de la integración de escritura dual de Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927993"
---
# <a name="project-operations-dual-write-integration-overview"></a>Descripción general de la integración de doble escritura de Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Project Operations usa [capacidades de doble escritura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar datos entre Microsoft Dataverse y Dynamics 365 Finance.

La siguiente ilustración muestra cómo se sincronizan los datos como parte de esta integración entre Dataverse y Finance.

![Descripción general de los flujos de datos de Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations en Dataverse proporciona una interfaz de usuario (UI) moderna y extensibilidad fácil sin código o con poco código usando capacidades de Power Platform. Los jefes de proyecto, jefes de recursos, miembros del equipo de proyecto y otras personas de la oficina principal realizan sus actividades en Project Operations en Dataverse.

Project Operations en Finance proporciona compatibilidad de reconocimiento de ingresos y contabilidad de proyectos. Project Operations se conecta al marco financiero en Finance para el cálculo de impuestos sobre las ventas, tipos de cambio de divisas, informes de dimensión financiera y más. Las experiencias de los contables de proyectos se basan principalmente en Finance.

La integración de Project Operations consiste en la siguiente integración de componentes:


- [Integración de datos de instalación y configuración de Project Operations](resource-dual-write-setup-integration.md) 
- [Estimaciones y datos reales del proyecto](resource-dual-write-estimates-actuals.md)
- [Facturas de proyecto](resource-dual-write-project-invoice.md)
- [Gestión de gastos](resource-dual-write-expense.md)
- [Factura del proveedor](resource-dual-write-vendor-invoice.md)
