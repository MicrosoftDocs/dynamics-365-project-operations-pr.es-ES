---
title: Características quitadas o en desuso en Dynamics 365 Project Operations
description: En este artículo se describen las características que se han quitado (o cuya eliminación está prevista) de Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921507"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Características quitadas o en desuso en Dynamics 365 Project Operations

_**Se aplica a:** Project Operations para escenarios basados en recursos/no almacenados, implementación Lite - trato a facturación proforma y Project Operations para escenarios basados en existencias/producción_

En este artículo se describen las características que se han quitado (o cuya eliminación está prevista) de Dynamics 365 Project Operations.

- Una característica *quitada* ya no está disponible en el producto.
- Una característica *en desuso* no está en desarrollo activo y puede quitarse en una actualización futura.

Esta lista tiene como objetivo ayudar a considerar estas eliminaciones y características en desuso para su propia planificación.

> [!NOTE]
> La información detallada sobre los objetos de aplicaciones de finanzas y operaciones se puede encontrar en los [**Informes de referencia técnica**](/dynamics/s-e/global/axtechrefrep_61). Se pueden comparar las diferentes versiones de estos informes para conocer los objetos que se han modificado o quitado en cada versión de aplicaciones de finanzas y operaciones.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Características quitadas o en desuso en la versión de marzo de 2022 de Project Operations

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parámetro de Gestión de proyectos y contabilidad "Crear siempre transacción de ajuste"

| &nbsp; | &nbsp; |
|--------|--------|
| **Razón para características en desuso/eliminación** | Las transacciones de ajuste son necesarias con fines de auditoría. Después del desuso, este parámetro se ocultará. El sistema siempre creará transacciones de ajuste, tal y como lo hace actualmente cuando el parámetro se establece en **Sí**. |
| **¿Reemplazada por otra característica?** | No |
| **Áreas de producto afectadas** | Aplicación |
| **Opción de implementación** | Project Operations para escenarios mantenidos en existencias/orden de producción |
| **Estado** | Obsoleto: para el 1 de marzo de 2023, ocultaremos el parámetro y cambiaremos el comportamiento del sistema para que siempre se creen transacciones de ajuste. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parámetro de Gestión de proyectos y contabilidad "Usar fecha de ajuste como nueva fecha de proyecto"

| &nbsp; | &nbsp; |
|--------|--------|
| **Razón para características en desuso/eliminación** | Este parámetro se usó originalmente para permitir ajustes cuando se cerraba un período fiscal. Sin embargo, ya no es necesario, porque la fecha contable de la transacción se puede cambiar a la primera fecha del período abierto, si está configurado. La fecha del proyecto no debe cambiarse, porque representa la fecha en que ocurrió la transacción. |
| **¿Reemplazada por otra característica?** | No |
| **Áreas de producto afectadas** | Aplicación |
| **Opción de implementación** | Project Operations para escenarios mantenidos en existencias/orden de producción |
| **Estado** | En desuso: para el 1 de marzo de 2023, ocultaremos el parámetro y cambiaremos el comportamiento del sistema para que nunca se cambie la fecha del proyecto en los ajustes. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Flujo de trabajo de solicitud de recursos en Project Operations para escenarios basados en existencias/producción

| &nbsp; | &nbsp; |
|--------|--------|
| **Razón para características en desuso/eliminación** | En desuso debido al bajo uso y las limitaciones del volumen de transacciones. |
| **¿Reemplazada por otra característica?** | No |
| **Áreas de producto afectadas** | Aplicación |
| **Opción de implementación** | Project Operations para escenarios mantenidos en existencias/orden de producción |
| **Estado** | Obsoleto: para el 1 de marzo de 2023, deshabilitaremos la opción de solicitar recursos para el proyecto mediante el flujo de trabajo. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Página de propuesta de factura de proyecto sin vistas de encabezado y líneas

| &nbsp; | &nbsp; |
|--------|--------|
| **Razón para características en desuso/eliminación** | En desuso debido a las mejoras en la página que se introdujeron junto con la clave de característica **Utilizar la propuesta de factura del proyecto y los formularios de diario de facturas con la vista Encabezado y Líneas**. |
| **¿Reemplazada por otra característica?** | Sí |
| **Áreas de producto afectadas** | Aplicación |
| **Opción de implementación** | Project Operations para escenarios de producción/en existencias; Project Operations para escenarios de recursos/no mantenidos en existencias |
| **Estado** | En desuso: para el 1 de marzo de 2023, desactivaremos la página anterior (heredada) y activaremos la clave característica **Utilizar la propuesta de factura del proyecto y los formularios de diario de facturas con la vista Encabezado y Líneas** de forma predeterminada. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Características quitadas o en desuso en la versión de diciembre de 2021 de Project Operations

### <a name="collaboration-workspaces"></a>Áreas de trabajo de colaboración

[Crear o vincular a un espacio de trabajo de colaboración (proyecto)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razón para características en desuso/eliminación** | En desuso debido al bajo uso. Los clientes que utilizan Project Operations para escenarios de recursos / no almacenados pueden aprovechar [Colaboración con grupos de oficina](../project-management/collaboration-groups.md). |
| **¿Reemplazada por otra característica?** | No |
| **Áreas de producto afectadas** | Aplicación  |
| **Opción de implementación** | Project Operations para escenarios mantenidos en existencias/orden de producción |
| **Estado** | En desuso: para el 1 de diciembre de 2022, planeamos dejar de admitir espacios de trabajo de colaboración. |
