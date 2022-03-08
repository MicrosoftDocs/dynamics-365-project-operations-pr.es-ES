---
title: Parámetros de la integración de Project Service Automation
description: Este tema explica cómo configurar cómo se ingresan los datos predeterminados cuando se integra Microsoft Dynamics 365 for Project Service Automation con Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58f34cb74be531a98518100158f39d74f136afc34444468d666cd4e9394af6f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005862"
---
# <a name="project-service-automation-integration-parameters"></a>Parámetros de la integración de Project Service Automation

[!include[banner](../includes/banner.md)]

En la página **Parámetros de integración de Project Service Automation**, puede configurar cómo se especifican los datos predeterminados cuando integra Dynamics 365 Project Service Automation con Dynamics 365 Finance. Para que los proyectos se sincronicen correctamente de Project Service Automation a Finance, debe configurar los siguientes campos.

Para abrir la página **Parámetros de integración de Project Service Automation**, vaya a **Gestión de proyectos y contabilidad** \> **Configurar** \> **Parámetros de integración de Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - La integración de tareas del proyecto, las categorías de transacciones de gastos, las estimaciones de horas, las estimaciones de gastos y el bloqueo de funciones están disponibles en la versión 8.0.
> - Las integraciones de datos reales están disponibles a partir de la versión 8.0.1.


| Tabulador                    | Campo                | Descripción |
|------------------------|----------------------|-------------|
| General                | Tipo de proyecto predeterminado | Seleccione el tipo de proyecto predeterminado. Cuando los proyectos se sincronizan desde Project Service Automation, este valor se usa si no proporcionó un valor predeterminado en la plantilla de integración. Durante la sincronización, el campo **Tipo de proyecto** de nuevos proyectos se establece en este valor. Sin embargo, el valor puede actualizarse cuando las líneas de contrato del proyecto se sincronizan desde Project Service Automation. |
|                        | Categoría de tiempo        | Seleccione la categoría de tiempo predeterminada. Este valor se utiliza cuando las estimaciones de horas se sincronizan desde Project Service Automation. Cuando las estimaciones de horas y los datos reales de horas se sincronizan desde Project Service Automation, el campo **Categoría** de previsiones de horas de nuevo proyecto en Finance se establece en este valor. |
|                        | Categoría de tarifa         | Seleccione la categoría de tarifa predeterminada. Este valor se utiliza cuando los datos reales de tarifas se sincronizan desde Project Service Automation. Cuando los datos reales de tarifas se sincronizan desde Project Service Automation, el campo **Categoría** de transacciones de tarifas nuevas en Finance se establece en este valor. |
| Valores predeterminados del grupo de proyectos | Tipo de proyecto         | Haga clic en **Nuevo** para agregar una fila en la que pueda seleccionar el tipo de proyecto para el que establecer el grupo de proyectos predeterminado. Un tipo de proyecto específico se puede seleccionar solo una vez en la configuración. |
|                        | Grupo de proyectos        | Seleccione el grupo de proyectos predeterminado para el tipo de proyecto seleccionado. Cuando se sincronizan nuevos proyectos desde Project Service Automation, el campo **Grupo de proyecto** se establece en el valor predeterminado para el tipo de proyecto si no proporcionó un valor predeterminado en la plantilla de integración. |
| Valores predeterminados del tipo de facturación  | Tipo de facturación         | Haga clic en **Nuevo** para agregar una fila en la que pueda seleccionar el tipo de facturación para el que establecer la propiedad de línea predeterminada. Un tipo de facturación específico se puede seleccionar solo una vez en la configuración. |
|                        | Propiedad de línea        | Seleccione la propiedad de línea predeterminada para el tipo de facturación seleccionado. Cuando se sincronizan nuevas estimaciones de horas, nuevas estimaciones de gastos o nuevos datos reales desde Project Service Automation, el campo **Propiedad de línea** se establece en el valor predeterminado para el tipo de facturación. |
| Bloqueo de funcionalidades  | No aplicable       | Seleccione la funcionalidad para deshabilitar en Finance para proyectos y contratos que se originaron en Project Service Automation. Por ejemplo, puede desactivar la capacidad de editar contratos y proyectos, crear estructuras de descomposición del trabajo y especificar hojas de tiempo en Finance. Los campos relacionados con la contabilidad seguirán estando habilitados, incluso si no están disponibles mediante la configuración de parámetros. De forma predeterminada, todas las funciones están habilitadas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]